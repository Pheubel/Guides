Git ignore files are used to avoid tracking files, to make one, simply create a new file and call it `.gitignore`. They are useful for when a files is user specific, like settings for Visual Studio Code, or if files get automatically get fetched or generated.

## How does `.gitignore` work
Inside of a git ignore file you can put several patterns for files you want git to ignore, they will not have their changes tracked. You can ignore a specific file, any file file with a specific extension or even files inside a specific directory.

Here is a simple example of a git ignore file:
```sh
# You can create comments by starting lines with a #.
# This is useful for documenting why you are ignoring something or notating a group.

# This will ignore a specific file
ignoreMe.txt

# you can ignore all file of a specific type, in this case all PNG files
*.png

# you can also ignore everything in a specific folder
UserSettings/

# using two ** you can even use it as a wildcard for paths
**/UserInfo/secrets.json
```

Git ignore files use the patterns relative to the directory where they are located, so if you have a rule to exclude `foo/bar.txt`, it must be inside the same directory as the `foo` directory in order to ignore `bar.txt`.

Sometimes you find that you need to exclude almost all files from a specific folder, except for one file. In such situations, you can start a pattern with an `!`, any files that match that rule will be **included** instead.

For this example you work with a program that automatically installs any packages read from `Packages/packageList.json` into the `Packages` directory. In this case it is useful to not ignore it:
```sh
# excludes all packages in the package
Packages/

# after excluding all packages, include the package list again
!Packages/packageList.json
```

It should be noted that if a file is already being tracked inside of your git repository, putting it in your `.gitignore` will **not** stop it from being tracked.

This covers a good chunk of all you need to know about setting up a git ignore file. 
You can find the full documentation on git ignores here: https://git-scm.com/docs/gitignore

## Using existing git ignores
For most kind of projects, people have already made git ignore files that you can use. For example, there is one for [Unity](https://github.com/github/gitignore/blob/main/Unity.gitignore) and [Godot](https://github.com/github/gitignore/blob/main/Unity.gitignore). Some of them may even tell you where they need to be placed. In the case of the Unity git ignore, it tells you to put it inside of the root of your Unity project, rather than the root of your git project.

When creating a git repository, you might get offered to have a git ignore file created for you from a list of templates. If you want to see the full list of templates hosted by github, you can visit: https://github.com/github/gitignore

## Exercise
Go to https://github.com/Pheubel/GitPlayground and follow the instructions. You will fork the repository to create a copy of repository in order to have a safe environment to experiment in with git files.

After you have followed the instructions you should have forked the repository and have a handful of files.

Your exercise will be to edit the `.gitignore` file in order to satisfy certain criteria:
1. You must add all markdown files (files ending in `.md`) that are directly inside of the `IgnorePractice` directory.
2. Create an exception for `includeMe.md` so that it will **not** be excluded.
3. `IgnorePractice/Users` contains sensitive data, make sure that the data is excluded.
4. `IgnorePractice/Users` also has `ReadMe.md`, this file needs to stay included.

If you did it correctly your change tracker in Github Desktop will look something like this:
TODO: image

There are many roads leading to Rome, for this exercise you can use different tricks to satisfy all conditions and thus there is more than just one right answer. An implementation that satisfies all conditions can be found [here](https://gist.github.com/Pheubel/6bb2747738a2268dbd23fb455c678f8f).