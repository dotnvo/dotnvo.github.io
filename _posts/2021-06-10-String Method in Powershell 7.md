---
layout: post
title: Using .NET 5 split Method to split strings in PowerShell 7.1+
subtitle: Coding
tags: [powershell,scripting,dotnet,coding,tutorial]
comments: true
---

I started using Powershell in version 5, which is built on .NET 4.

Powershell 7 (well 7.1 and up anyway) is built on .NET 5. 7.1+ has implemented a ton of awesome features. As with any change, 


I use a mixture of .NET methods when I code in Powershell. One method I often use is Split. I was working on a project where I was matching culture to a region that a game supported to automagically identify a default Country Code for my end users. My goal was to get the country from the Display Name in `Get-Culture` In PowerShell 5, this might be how I do this:

```powershell
Get-Culture | Select-Object -ExpandProperty DisplayName
English (United States)
$SplitArray = (Get-Culture | Select-Object -ExpandProperty DisplayName).Split("()")
$SplitArray
English
United States
$SplitArray[1]
United States
```
Let's do the same command in PowerShell 7.1.3:

```powershell
Get-Culture | Select-Object -ExpandProperty DisplayName
English (United States)
$SplitArray = (Get-Culture | Select-Object -ExpandProperty DisplayName).Split("()")
$SplitArray
English (United States)
$SplitArray[1]
```
Wait, what happened in 7.1.3? The split didn't work, so the last item in the array wasn't returned.

Let's walk through it. We used the cmdlet `Get-Culture` to grab some basic information. When we use the split method on two characters, `(` and `)`. PowerShell 5 sees we are trying to split a string, but automatically converts it to split on the characters, `(` and `)`. In .NET 4, the string class only had methods that took characters as parameter types. PowerShell sees this and automagically converts it, to make life a little easier on you. Note there's an implied 'OR' (`|`) here as it's an array of characters.

Why is PowerShell 7 behaving differently? In .NET 5, the string class has some additional parameters that accept strings. PowerShell 7 does not take any automatic action.  To really Illustrate the difference here, I'll split on strings instead of characters using our `Get-Culture` from above to get the same output. Note this is an ugly way of doing it but it's for demo purposes:

```powershell
$SplitArray = (((Get-Culture | Select-Object -ExpandProperty DisplayName).Split("English ("))[1].Split(')'))[0]
$SplitArray
United States
```
Ok neat, but that's a little ugly. We're splitting twice. What might be a better way? We can use a character typecast array!

```powershell
$SplitArray = ((Get-Culture | Select-Object -ExpandProperty DisplayName).Split([char[]]"()"))[1]
$SplitArray
United States
```

Happy coding!
