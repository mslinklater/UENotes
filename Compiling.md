# Compiling

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