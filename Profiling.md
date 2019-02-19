# Profiling Your Project

## Stats

Easy cycle count timing..

In the module.h file add the following (replace Example with your module name)...

`DECLARE_STATS_GROUP(TEXT("Example"), STATGROUP_Example, STATCAT_Advanced);`

Then in a cpp file in your module, at the top...

`DECLARE_CYCLE_STAT(TEXT("My Cycle Stat"), STAT_MyCycleStat, STATGROUP_Example);`

in the function you want to measure...

`SCOPE_CYCLE_COUNTER(STAT_MyCycleStat);`

## NamedEvents

You can toggle Named Events by issuing the console command 'stat NamedEvents'

You can turn this on from boot by changine the line Core/Private/Misc/CoreGlobals.cpp:289 (GCycleStatsShouldEmitNamedEvents)
