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

### UpdateLocalVersion

Updates your local version based on a 'p4 sync' command. This modifies the contents of the files 'Engine/Build/Build.version' and 'Engine/Source/Runtime/Launch/Resources/Version.h'.
