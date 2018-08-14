#Cook Commandlet

To enable detailed cook stats you need to add the following line to the 'UnrealEd.Build.cs' file:

PublicDefinitions.Add("ENABLE_COOK_STATS=1"); - doesn't seem to work

Example Visual Studio 'Command Arguments' entry for debugging...

"$(SolutionDir)$(ProjectName).uproject" -skipcompile -run=Cook -platform=Win64 -targetplatform=WindowsNoEditor

##Parameters

-cookonthefly

Enable cook-on-the-fly cooking. Additional switches...

	-forceclose

	InstanceId=<value>

	timeout=<value>


-cookall

Cook everything

-leaktest

Test for UObject leaks

-unversioned

Save all cooked packages without versions. These are then assumed to be current version on load. This is dangerous but results in smaller patch sizes.

-manifests

Generate manifests for building streaming install packages

-iterate

Enable iterative cooking

-skipeditorcontent

Skip saving any packages in Engine/Content/Editor - unless target has editoronly data, in which case it will save those anyway.

-errorenginecontentuse

Error is we access engine content - useful for DLC.

-useserializationforgeneratingpackagedependencies

Deprecated - use only for historical reasons.

-cooksinglepackage

Only cook package specified on command-line. Use for debugging purposes.

-verbosecookerwarnings

Output additional verbose cooker warnings

-partialgc

Only clean up objects which are not in use by the cooker when we Garbage Collect

-diffonly

Not used.....

-logcookstats

Log the results to the command line after the cook (happens automatically on a build machine)

Cook-by-the-book parameters

	-IterateSharedCookedbuild

	-TestCook

	-LogDebugInfo

	-IgnoreIniSettingsOutOfDate

	-IgnoreScriptPackagesOutOfDate

	-DLCNAME=<value>

	-cookchild=<value>

	-childIdentifier=<value>

	-numcookerstospawn=<value>

	-BasedOnReleaseVersion=<value>

	-CreateReleaseVersion=<value>

	-OutputDir=<value>

	-Map=<value>

	-Cookdir=<value>

	-Cookcultures=<value>

	-mapinisection=<value>

	-mapsonly

	-nodev

	-fullloadandsave

	-generatedependenciesformaps


