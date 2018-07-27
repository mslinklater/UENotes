#ResavePackages Commandlet

Resaves project packages using latest engine serialisation. You should run this occassionally to update the timestamps and serialisation of old assets. Resaving packages should speed up cooking time.

##Parameters

-fixupredirects

Just fixes up redirects.

-ignorechangelist

Resaves packages regardless of changelist values

-projectonly

Ignores engine packages.

Q/ How to have it not create a P4 changelist ?
