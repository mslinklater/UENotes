# Serialisation

## Intro

Consists of a number of classes/systems/layers

### Platform Speciic File IO

/Source/Runtime/Core/Private/Windows/WindowsPlatformFile

### Platform Agnostic File IO

/Source/Runtime/Core/Private/HAL/PlatformFileManager

### API Layers
```
Archives
GenericFiles
PlatformFiles
```
### Classes
```
IFileHandle								Core/Public/GenericPlatform/GenericPlatformFile.h
	FAsyncBufferedFileReaderWindows		Core/Private/Windows/WindowsPlatformFile.cpp
	FFileHandleWindows					Core/Private/Windows/WindowsPlatformFile.cpp
	FCachedFileHandle					Core/Public/HAL/IPlatformFileCachedWrapper.h			?
	FLoggedFileHandle					Core/Public/HAL/IPlatformFileLogWrapper.h				?
	TProfiledFileHandle					Core/Public/HAL/IPlatformFileProfilerWrapper.h			?
	FPlatformFileReadStatsHandle		Core/Public/HAL/IPlatformFileProfilerWrapper.h			?
	FRegisteredFileHandle				Core/Public/HAL/PlatformFileCommon.h					deprecated or just used with PS4
	FNetworkFileHandle					NetworkFile/Public/NetworkPlatformFile.h
	FPakFileHandle						PakFile/Public/IPlatformFilePak.h
	FSandboxFileHandle					SandboxFile/Public/IPlatformFileSandboxWrapper.h		?
	FStreamingNetworkFileHandle			StreamingFile/Private/StreamingNetworkPlatformFile.cpp	?

FArchive													Core/Public/Serialization/Archive.h						Base class for archives
	FArchiveFileReaderGeneric								Core/Public/HAL/FileManagerGeneric.h
	FArchiveFileWriterGeneric								Core/Public/HAL/FileManagerGeneric.h
	FArchiveLoadCompressedProxy								Core/Public/Serialization/ArchiveLoadCompressedProxy.h
	FArchiveSaveCompressedProxy								Core/Public/Serialization/ArchiveSaveCompressedProxy.h
	FArchiveProxy											Core/Public/Serialization/ArchiveProxy.h
		FArchiveFromStructuredArchive						Core/Public/Serialization/ArchiveFromStructuredArchive.h
			FArchiveUObjectFromStructuredArchive			Core/Public/Serialization/ArchiveUObjectFromStructuredArchive.h
		FMaterialResourceProxyReader						CAN'T FIND THIS ???
		FNameAsStringProxyArchive							Core/Public/Serialization/NameAsStringProxyArchive.h
			FObjectAndNameAsStringProxyArchive				CoreUObject/Public/Serialization/ObjectAndNameAsStringProxyArchive.h
		FShaderSaveArchive									ShaderCore/Public/Shader.h
	FArchiveUObject											CoreUObject/Public/Serialization/ArchiveUObject.h
		FArchiveCountMem									CoreUObject/Public/Serialization/ArchiveCountMem.h
		FArchiveFindCulprit									CoreUObject/Public/Serialization/ArchiveFindCulprit.h
		FArchiveGenerateReferenceGraph
		FArchiveHasReferences
		FArchiveObjectCrc32
		FArchiveObjectGraph
		FArchiveObjectPropertyMapper
		FArchiveReferenceMarker
		FArchiveReplaceObjectRefBase
			FArchiveReplaceObjectRef
		FArchiveScriptReferenceCollector
		FArchiveShowReferences
		FArchiveTopLevelReferenceCollector
		FArchiveTraceRoute
		FDuplicateDataReader
		FDuplicateDataWriter
		FFindAssetsArchive
		FFindReferencesArchive
		FLinkerLoad
		FLinkerSave
		FReferenceCollectorArchive
		FTransaction::FObjectRecord::FReader
		FTransaction::FObjectRecord::FWriter
	FAsyncWriter
	FBitArchive
		FBitReader
			FNetBitReader
		FBitWriter
			FNetBitWriter
	FBufferReaderBase
		FBufferReader
		FBufferReaderWithSHA
	FBufferWriter
	FHttpStreamFArchive
	FMemoryArchive											?
		FArrayReader
		FLargeMemoryReader
			FArchiveStackTraceReader
		FLargeMemoryWriter
			FArchiveStackTrace
		FMemoryReader
		FMemoryWriter
			FBufferArchive
				FNetworkFileArchive
			FMaterialResourceMemoryWriter
			FObjectWriter
		FObjectReader
		FStaticMemoryReader
	FOutputDeviceMemory::FOutputDeviceMemoryProxyArchive	?
```