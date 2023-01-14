## Intro
C# is a programming language with a lot of power. You can use it to make pretty much anything you set your mind to.

There are many IDE's you can use to write C# scripts, but my personal recommendation goes to [Visual studio](https://visualstudio.microsoft.com/vs/). When installing it, you get prompted to select packages to add to Visual Studio. They each give a good description of what they are intended for, but some notable ones are:
* .NET desktop development - You pretty much want to always install this, it sets you up for basic C# development, like console apps and forms.
* Game development with Unity - This adds features to better integrate with Unity, it allows you to see which scripts are used in what assets, Unity specific Intellisense hints, etc.
* ASP&#46;Net and web development - This provides a set of development tools in order to make your own website.

I will be using Visual Studio for my explanations, as that is the IDE I use.

## Set up
To create a console app project, Open Visual Studio and press "Create a new project" and then look for "Console App". You might also see "Console App (.NET Framework)", but that uses an older version of .NET that only works on windows. Now you can give your app a name and you can select the version of .NET you want to use. I recommend to use the latest available so you can toy around with all the features. Finally, hit Create.

![image](https://user-images.githubusercontent.com/22686676/212475172-1234ead7-37bb-41a9-a173-020eb1baa065.png)

Let's dissect what we are seeing here,
```cs
Console.WriteLine("Hello, World!");
```
* `Console` - This is the class that provides access to the console window. Notably, `Write` and `WriteLine`, which display text onto the console window.
* `WriteLine(string)` - This is a function that is part of the `Console` class. `WriteLine` is a function that takes the argument passed to it, turns it into a string and displays that string. After that, it continues to the next line on the console. If you do not want to go to the next line on the console, you can use `Write(string)` instead.
* `"Hello, World!"` - This is a string, all text between the quotation marks will be seen as part of the string.

In the next lesson i'll be talking a bit about types.

## Exercise:
Try to mess around with the console program to have it display different messages. You can also look at prociding it numbers instead, both as numbers and as strings.
