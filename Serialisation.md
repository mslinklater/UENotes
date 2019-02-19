# Serialisation

## Intro

Consists of a number of classes/systems/layers

### Platform Speciic File IO

/Source/Runtime/Core/Private/Windows/WindowsPlatformFile

### Platform Agnostic File IO

/Source/Runtime/Core/Private/HAL/PlatformFileManager

### API Layers

Archives
GenericFiles
PlatformFiles

### Classes

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
	FArchiveFileReaderGeneric			
	FArchiveFileWriterGeneric
	FArchiveLoadCompressedProxy
	FArchiveSaveCompressedProxy
	FArchiveProxy
		FArchiveFromStructuredArchive
			FArchiveUObjectFromStructuredArchive
		FMaterialResourceProxyReader
		FNameAsStringProxyArchive
			FObjectAndNameAsStringProxyArchive
		FShaderSaveArchive
	FArchiveUObject
	FAsyncWriter
	FBitArchive
	FBufferReaderBase
	FBufferWriter
	FHttpStreamFArchive
	FMemoryArchive											?
	FOutputDeviceMemory::FOutputDeviceMemoryProxyArchive	?