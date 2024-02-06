# Melissa - MatchUp Object Global Windows C++

## Purpose
This code showcases the Melissa MatchUp Object Global using C++.

Please feel free to copy or embed this code to your own project. Happy coding!

For the latest Melissa MatchUp Object Global release notes, please visit: https://releasenotes.melissa.com/on-premise-api/matchup-object-global/

For further details, please visit: https://wiki.melissadata.com/index.php?title=MatchUp_Object:Reference

The console will ask the user for:

- A txt file that contains global data you would like to matchup
- A txt file that contains US data you would like to matchup

And return 

- A txt file of global duplicate groups
- A txt file of US duplicate groups

## Tested Environments
- Windows 10 64-bit Microsoft Visual C++ 14.34, Powershell 5.1
- Melissa data files for 2024-Q1
- Nmake 14.34
- Visual Studio 2022 Developer Command Prompt v17.4.2 64-bit

## Required File(s) and Programs

#### Binaries
This is the c++ code of the Melissa Object.

- mdMatchup.dll
- mdGlobalParse.dll

#### Data File(s)
- icudt52l.dat
- mdMatchup.dat
- mdMatchup.mc
- mdMatchup.sac
- mdMatchup.cfg

#### Dependencies
- mdMatchup.h
- mdMatchupEnums.h
- mdMatchup.lib

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

#### Visual Studio Developer Command Prompt
It is important to note that you must be able to initialize the Visual Studio Developer Command Prompt environment for `x86_x64` in order to test the Melissa MatchUp Object Global. The Visual Studio Developer Command Prompt should already be downloaded if you have Microsoft Visual Studio installed. 

To check if you are able to intialize the Visual Studio Developer Command Prompt for `x86_x64`, you can open the start menu and search for `x86_x64 Cross Tools Command Prompt for VS 2022`. If this program exists, then you may continue to the next steps.

Alternatively, you can check to see if the following filepath exists: `C:\Program Files\Microsoft Visual Studio\2022\Professional\VC\Auxiliary\Build\vcvarsall.bat` (with Visual Studio 2022 installed). If the filepath exists, then you may continue to the next steps.

#### Set up Powershell settings
If running Powershell for the first time, you will need to run this command in the Powershell console: `Set-ExecutionPolicy RemoteSigned`.
The console will then prompt you with the following warning shown in the image below. 
 - Enter `'A'`. 
 	- If successful, the console will not output any messages. (You may need to run Powershell as administrator to enforce this setting).
	
 ![alt text](/screenshots/powershell_executionpolicy.png)

#### Download this project
```
$ git clone https://github.com/MelissaData/MatchUpObjectGlobal-Cpp
$ cd MatchUpObjectGlobal-Cpp
```

#### Set up Melissa Updater
Melissa Updater is a CLI application allowing the user to update their Melissa applications/data.
- Download Melissa Updater here: <https://releases.melissadata.net/Download/Library/WINDOWS/NET/ANY/latest/MelissaUpdater.exe>
- Create a folder within the cloned repo called `MelissaUpdater`.
- Put `MelissaUpdater.exe` in the `MelissaUpdater` folder you've just created.

#### Different ways to get data file(s)
1. Using Melissa Updater
    - It will handle all of the data download/path and dll(s) for you.
2. If you already have the latest zip, you can find the data file(s) and dll(s) in there
    - Use the location of where you've copied/installed the data and update the "$DataPath" variable in the powershell script.
    - Navigate into the `MelissaMatchupObjectGlobalWindowsCpp` project folder, create a folder named `Build`, and copy all the dll(s) mentioned above into the `Build` folder.
    - Copy all the dependencies mentioned above into the `MelissaMatchupObjectGlobalWindowsCpp` project folder.

## Run Powershell Script
Parameters:
- -global: a test global txt file
- -us: a test US txt file

  These are convenient when you want to get results for specific txt files in one run instead of testing multiple txt files in interactive mode.

- -license (optional): a license string to test the MatchUp Object Global
- -quiet (optional): add to the command if you do not want to get any console output from the Melissa Updater

  When you have modified the script to match your data location, let's run the script. There are two modes:
- Interactive 

    The script will prompt the user for a global txt file and a US txt file, then use the provided txt files to test MatchUp Object Global.  For example:
    ```
    $ .\MelissaMatchupObjectGlobalWindowsCpp.ps1
    ```
    For quiet mode:
    ```
    $ .\MelissaMatchupObjectGlobalWindowsCpp.ps1 -quiet
    ```
- Command Line 

    You can pass a global txt file, US txt file, and a license string into the `-global`, `-us`, and `-license` parameters respectively to test MatchUp Object Global. For example:
    ```
    $ .\MelissaMatchupObjectGlobalWindowsCpp.ps1 -global "MelissaMatchupGlobalSampleInput.txt" -us "MelissaMatchupUSSampleInput.txt"
    $ .\MelissaMatchupObjectGlobalWindowsCpp.ps1 -global "MelissaMatchupGlobalSampleInput.txt" -us "MelissaMatchupUSSampleInput.txt" -license "<your_license_string>"
    ```

	For quiet mode:
    ```
    $ .\MelissaMatchupObjectGlobalWindowsCpp.ps1 -global "MelissaMatchupGlobalSampleInput.txt" -us "MelissaMatchupUSSampleInput.txt" -quiet
    $ .\MelissaMatchupObjectGlobalWindowsCpp.ps1 -global "MelissaMatchupGlobalSampleInput.txt" -us "MelissaMatchupUSSampleInput.txt" -license "<your_license_string>" -quiet
    ```
This is the expected output from a successful setup for interactive mode:

![alt text](/screenshots/output.png)


## Contact Us
For free technical support, please call us at 800-MELISSA ext. 4 (800-635-4772 ext. 4) or email us at tech@melissa.com.

To purchase this product, contact the Melissa sales department at 800-MELISSA ext. 3 (800-635-4772 ext. 3).
