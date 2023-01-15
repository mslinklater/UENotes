# Unreal Build Tool (UBT)

Handles the build process.

## Notes

This is usually run from the buid batch files found in Engine/Build/BatchFiles/

## Command line Parameters

**Arguments[0]**

The target name

**Arguments[1]**

Platform (eg Win64)

**Arguments[2]**

Configuration (eg Development)

**Arguments[3]**

Path to .uproject file

**-assemble**

**-assembleonly**

**-noassemble**

**-autosdkonly**

**-buildconfigurationdoc=** *filename*

Produce a build configuration HTML documentation file

**-cmakefile**

Generate a CMake file for the project

**-clion**

Generate CLion file for the project

**-codelitefiles**

Generate CodeLite files for the project

**-deploy**

**-eddieprojectfiles**

Generate Eddie files for the project

**-frommsbuild**

**-gather**

**-gatheronly**

**-graph**

**-ignorejunk**

**-installed** | **-installedengine**

Sets bIsEngineInstalled to true

**-invalidatemakefilesonly**

**-kdevelopfile**

Generate a kdevelop file for the project

**-log=**

**-makefile**

Generate a makefile for the project

**-modulerulesdoc=** *filename*

Produce a module rules HTML documentation file

**-modulewithsuffix=**

Only build the specified module ?

**-nogather**

**-notinstalledengine**

Sets bIsEngineInstalled to false

**-nomutex**

Allows more than one instance of UBT to run at once. You probably don't want to do this.

**-progress**

**-projectfileformat=**

**-projectfiles**

**-qmakefile**

Generate a QMake file for the project

**-singlefile=filename**

Compile just a single file

**-targetrulesdoc=** *filename*

Produce a target rules HTML documentation file

**-timestamps**

**-validateplatform**

**-verbose**

Set verbose log output

**-veryverbose**

Set very verbose log output

**-vscode**

Generate Visual Code file for the project

**-vsdebugandroid**

**-vsmac**

Generate Visual Code Mac file for the project

**-waitmutex**

If you run more than one instance of UBT at once this flag will try to make the new instance wait until the previous one(s) have completed before running.

**-xcodeprojectfiles**

Generate XCode project file

**-xgeexport**

**-2012unsupported**

**-2013unsupported**

**-2015**

**-2017**

## Controlling the Build Environment

**To add a C preprocessor define**

Add to target.cs file:

GlobalDefinition.Add("BLAH=1");