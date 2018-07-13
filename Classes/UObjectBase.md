# UObjectBase Class

## Description

The root class type of all UE4 managed objects. Provides a number of features that all instances of UObject use:

..* Flags to characterise the type of object
..* Provide a unique uint32 ID for each runtime instance
..* Pointer to the UClass instance representing the class type this is an instance of. Used for reflection.
..* Pointer to the 'outer' object instance which defines this instances parent object. Used for GC and hierarchy traversal
..* A unique FName for each instance
..* A StatID for each instance, used in profiling ?

## Object Flags

Each instance of a UObjectBase derived object has a number of flags which control the core behaviour:

..* RF_Public - Object is visible outside it's package.
..* RF_Standalone - Keep object around for editing even if unreferenced. If this flag is set the GC will not remove the instance.
..* RF_MarkAsNative - Object (UField) will be marked as native on construction. Don't know what 'native' means.
