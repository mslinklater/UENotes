# Unreal Automation Tool (UBT)

General purpose automation tool written in C#.

## Notes

Can be called via the RunUAT.bat batch file.

## Global Command Line Parameters

**-CompileOnly**

**-Verbose**

**-Submit**

**-NoSubmit**

**-NoP4**

**-P4**

**-Preprocess**

**-Compile**

**-NoCompile**

**-NoCompileEditor**

**-IncrementalBuildUBT**

**-Help**

**-List**

Outputs a list of all the commands UAT knows about.

**-2015**

**-NoKill**

**-Installed**

**-UTF8Output**

**-AllowStdOutLogVerbosity**

**-NoAutoSDK**

**-ignorejunk**

**-UseLocalBuildStorage**

**-NotInstalledEngine**

## Parameters

**-BuildMachine**

Tells UAT it is running on a build machine. You can also set the environment variable 'uebp_LOCAL_ROOT' [Automation.cs]

**-Telemetry**

Path to telemetry file - not sure what this does yet.

## Commands

### BuildPhysX

Builds the PhysX libraries using the CMake build system. You can select which platforms/libraries/configurations are built by passing in some extra command line arguments... [Details](https://github.com/EpicGames/UnrealEngine/blob/release/Engine/Source/Programs/AutomationTool/Scripts/BuildPhysX.Automation.cs)

### UpdateLocalVersion

Updates your local version based on a 'p4 sync' command. This modifies the contents of the following files:
```
Engine/Build/Build.version
Engine/Source/Runtime/Launch/Resources/Version.h
Engine/Source/Programs/DotNETCommon/MetaData.cs
```
You can override the values that are used by passing extra command line arguments in. [Details](https://github.com/EpicGames/UnrealEngine/blob/release/Engine/Source/Programs/AutomationTool/Scripts/BuildPhysX.Automation.cs)

This command is usually used before you package the engine into binary format. The packaged binary engine distribution will use the updated CL numbers to detect when binaries are out of date and need to be rebuilt. To find out the CL number of a binary file (library) is look at the .modules file contained in the same folder as the library. The 'BuildId' value inside the modules file is the CL of the engine from which it was built.
```
eg UpdateLocalVersion -Licensee -P4

```
