In C# you can make use of various ways to represent data, you can even create your own. Inside C# there are several types already given out of the box, also known as builtin types. They each fulfill a role within programs to store and represent data.

## Built-in types
The most important among these types are:
* `int` - A type representing a whole number between `-2,147,483,648` and `2,147,483,647`. They are easy for computers to work with and work well in situations where you deal with whole numbers, for example going through a list of items.
* `long` - Like `int`, this type represents whole numbers. However with a larger range of values it can represent. It's range is between `-9,223,372,036,854,775,808` and `9,223,372,036,854,775,807`.
* `float` - A type to represent a floating point number, they are numbers with a decimal them, such as `13.37`. They are often used to represent values where small gaps between numbers are important. For example, with coordinates. An important thing to remember is that floating point numbers are not 100% precise, they are an approximate value and for situations like games, that is good enough.
* `double` - Like `float`, this type represents a floating point number. However, it does so with a higher precision.
* `bool` - A type that represents either `true` or `false`. They are often used for logic.
* `string` - This type represents a set of characters, for example `"Hello, world!"`. They are used often in applications for displaying info to a user. A game example would be with a dialogue box.
* `char` - This type represents a single character, like `a`, `@` and `Z`. An example of where they are useful is for determining if a `string` has a specific character.

You can find a full list on the [Ms docs page for built-in types](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/built-in-types).

In C# every variable needs to specify what type they are. This way you can prevent bugs that occur when you try mixing them accidentally. 

## Literals

To assign values to variables, you use literals. You don't have to remember much about them, as they are merely how the language detects the values you want to assign to your variables.

[![Example 1]()](https://try.dot.net/?bufferId=cs102S1.cs&fromGist=de48608070e9da1081f7cf5daaa0499e)

Outside of built-in types, C# allows you to create your own types with classes, they use the builtin types to form a new custom type. We'll be looking at them soon.

## Exercise 1
For each of the following values, what are the appropriate types to represent them?

\# | values    | \# | values
-- | --------- | -- | -------------
1  | `123`     | 6  | `true`
2  | `'c'`     | 7  | `102.203`
3  | `15.2f`   | 8  | `"12345"`
4  | `"Ditto"` | 9  | `0`
5  | `123L`    | 10 | `"s"`

Once you have written down your answers, you can compare them to the [correct answers](https://gist.github.com/Pheubel/3841d2c14ecd26535eab624c84b54eb9).

## Exercise 2
For each of the following types, come up with a value that would fit with the type.

\# | values    | \# | values
-- | --------- | -- | -------------
1  | `string`  | 6  | `float`
2  | `int`     | 7  | `string`
3  | `long`    | 8  | `double`
4  | `bool`    | 9  | `int`
5  | `char`    | 10 | `string`

As for this exercise there are not set answers, I recommend that you share your answers and compare them.

## Var
You might have seen `var` in other people's code, `var` acts as a stand-in for a type while assigning a variable. it can be useful to save on keystrokes, or when having the variable's type can already be deduced on the right side of the assignment. It is important to note that variables with `var` cannot change type, if you assign an `int` to it, you cannot assign a `string` after.

[![var example]()](https://try.dot.net/?bufferId=cs102S2.cs&fromGist=09107255c5fa5c26a7675472fbdfdd37)