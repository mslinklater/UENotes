#ResavePackages Commandlet

Resaves project packages using latest engine serialisation. You should run this occassionally to update the timestamps and serialisation of old assets. Resaving packages should speed up cooking time.

##Parameters

-STRIPEDITORONLY

Removes editor only content when pacakges are resaved

-SKIPFAILS

Disables the assert which fires if a package can't be loaded without error

-VERIFY

-OnlySaveDirtyPackages

Only resaves packages which have their birty bit set

-AutoCheckOutPackages or -AutoCheckOut

-AutoCheckIn or -AutoSubmit

-buildlighting

-buildtexturestreaming

-BuildHLOD

-BuildOptions=xxx,yyy,zzz
	Clusters
	Proxies
	ForceClusters
	ForceProxies
	ForceEnableHLOD
	ForceSingleCluster

-ForceHLODSetupAsset=xxx

-SkipToMap=xxx

System Environment Variable uebp_UATMutexNoWait

-AllowCommandletRendering

-Quality=xxx
	Preview
	Medium
	High
	Production

-FirstPackage=xxx

Allows you to set the first package so you can continue resaving from a specific point

-PackageSubString=xxx



-fixupredirects

Just fixes up redirects.

-ignorechangelist

Resaves packages regardless of changelist values

-projectonly

Ignores engine packages.

Q/ How to have it not create a P4 changelist ?
