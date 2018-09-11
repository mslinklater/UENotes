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

**-buildconfigurationdoc=**

**-cmakefile**

**-codelitefiles**

**-deploy**

**-define**

**-eddieprojectfiles**

**-gather**

**-ignorejunk**

**-nogather**

**-gatheronly**

**-installed | -installedengine**

**-notinstalledengine**

**-invalidatemakefilesonly**

**-kdevelopfile**

**-log=**

**-makefile**

**-modulerulesdoc=**

**-modulewithsuffix**

**-nomutex**

Allows more than one instance of UBT to run at once. You probably don't want to do this.

**-progress**

**-projectfileformat=**

**-projectfiles**

**-qmakefile**

**-singlefile**

**-targetrulesdoc=**

**-validateplatform**

**-verbose**

**-vscode**

**-vsdebugandroid**

**-waitmutex**

If you run more than one instance of UBT at once this flag will try to make the new instance wait until the previous one(s) have completed before running.

**-xcodeprojectfiles**

**-xgeexport**

**-2012unsupported**

**-2013unsupported**

**-2015**

**-2017**

