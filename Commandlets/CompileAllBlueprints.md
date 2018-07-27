#CompileAllBlueprints Commandlet

Recompiles all blueprints...

##Parameters

-ShowResultsOnly

Shows less log file output - not sure how useful it is to have it on or off

-DirtyOnly

Only builds Blueprints which are tagged as dirty by the editor

-CookedOnly

Ignores non-cooked blueprints

-CompileSkeletonOnly

-SimpleAssetList

Logs a list of the assets which have warnings and errors after the summary log output

-ExcludeTags=Tag1,Value1,Value2;Tag2,Value;....

Not sure what this does but it splits the params by the ';' character then expects comma seperated lists of strings.
Any asset tags (held in the TagsAndValues member of the Asset) which match one of the excluded tags will be skipped from the compile

-RequireAssetTags=Tag1,Value,...

An inclusive version of ExcludeTags. It will ONLY compile blueprints which match the tag pattern specified

-IgnoreFolder=/Folder1,/Folder2,...

Ignores blueprints which fit any of the folder paths specified.
