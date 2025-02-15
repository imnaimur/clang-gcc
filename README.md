
`NO CLENG 
ONLY GCC ON  MAC`
## Installing GCC In Mac 

Mac's default C++ compiler Clang does not include many of the libraries provided by GCC, which is regularly used by competitive programmers, like #include <bits/stdc++.h> and Policy Based Data Structures. So you're missing out by not using GCC.
Make sure the terminal is at the root folder by typing cd ~. First set up homebrew in your mac and install gcc by typing brew install gcc in the terminal. To find more details about this step check the links provided at the end


## Using GCC to the fullest 

GCC already supports up to the latest C++ version but is defaulted to older ones for some reason. To remedy this you first need to know the version of gcc you are using.

>  #### 1.Open Finder and click Go > Go to Folder on the top menu bar.

>  #### 2.Type /opt/homebrew/Cellar/gcc/ in the search box and press Return to open.

>  #### 3.Then go to (whatever version number is here) -> bin. Here in the bin folder, you can see the gcc and g++ versions.

`Mine is version 14` 
Now that you know the version of your g++ compiler, the next time you compile a C++ code instead of using just g++ use g++-14 instead (I used 14 since that is my g++ compiler version).

Congratulations you can now use everything from #include <bits/stdc++.h> to Policy Based Data Structures. However, for some reason, this still compiles using C++17, which is fine, but if you want to use C++20 (which is the latest version as of writing this) just add -std=c++20 after g++-14.

So from now on, instead of executing your code using g++ <filename>.cpp, use  `g++-14 -std=c++20 <filename>.cpp`



## Configuring VS Code 

If you use VS code instead of compiling through the terminal like me, you can easily implement this. If you are using code runner for execution do the following:

Go to `Code>Preferences>Settings` then in the search bar at the top of settings type `code-runner.executormap`.

Select Edit in settings.json, A JSON file will open.

From this settings.json file change the line with the key cpp. This is basically what VS code uses to compile your C++ code and show it to you. So replace the `g++` here with `g++-14` and add `-std=c++20` after this. It would like `"cpp": "cd $dir && g++-14 -std=c++20 $fileName -o $fileNameWithoutExt && $dir$fileNameWithoutExt",`.


🎉Congratulatons🎉


### `if bit/stdc++ is not in your bin then get it from ` 
> https://gist.github.com/Einstrasse/ac0fe7d7450621a39364ed3b05cacd11
