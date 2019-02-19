# Compiling

## What Happens When You Hit Build...

When you hit 'Build' inside Visual Studio(VS) a number of things happen in the background. The first thing to know is that VS isn't in control of the build process at all... all UE4 building is handled by a custom build system built by Epic. The first stage of the build is to see what VS does when Build is triggered.

Right click on your project in the Solution Explorer and go to the 'NMake' section. What you will now see are the actual command lines that VS submits to initiate the build. We'll ignore most of the command line switches for now... the important thing is to know that VS actually just calls a batch file.

```
YOURPATH\Engine\Build\BatchFiles\Build.bat TARGET PLATFORM CONFIGURAITON YOUR_UPROJECT_FILE -WaitMutex -FromMsBuild
```

The values for TARGET, PLATFORM and CONFIGURATION may be different from mine, which is why I've replaced them here, but the TARGET is probably somethingEditor, platform is probably Win64 and configuration is probably Development. These values correlate with the build configuration selectors inside VS. If you go to the ENgine/Build/BatchFiles folder you'll see there are different batch files for build, rebuild and clean. For now lets just look in the Build.bat file. Go open it up in a text editor.

The Build.bat file is a pretty basic wrapper around UnrealBuildTool(UBT), which is Epic's C# tool which actually controls what gets built and how. Tracing through the code you'll see that the command line passed to UBT looks something like this:

```
YOURPATH\Engine\Binaries\DotNET\UnrealBuildTool.exe TARGET PLATFORM CONFIGURAITON YOUR_UPROJECT_FILE -WaitMutex -FromMsBuild -DEPLOY
```

## Unity Build and Precompiled Headers

To change Unity build and PCH generation settings modify the file:

```
%AppData%\Unreal Engine\UnrealBuildTool\BuildConfiguration.xml
```
And add/change the following setting:

```
<?xml version="1.0" encoding="utf-8" ?><Configuration xmlns="https://www.unrealengine.com/BuildConfiguration">
	<BuildConfiguration>
		<bUseUnityBuild>false</bUseUnityBuild>
		<bUsePCHFiles>false</bUsePCHFiles>
	</BuildConfiguration>
</Configuration>
```