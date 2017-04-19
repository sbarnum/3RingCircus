
---
title: Quincy CASE UCO mapping
---

# Quincy CASE UCO mapping


### File core properties

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|DisplayName|uco-observable.File|uco-observable.File.fileName||[file.json](https://github.com/casework/case/blob/master/examples/file.json)| //filename
|FileAttributes||||| //flags vector for readonly, hidden, etc
|CreationTime|uco-observable.File|uco-observable.File.createdTime||[file.json](https://github.com/casework/case/blob/master/examples/file.json)|
|LastAccessTime|uco-observable.File|uco-observable.File.accessedTime||[file.json](https://github.com/casework/case/blob/master/examples/file.json)|
|LastWriteTime|uco-observable.File|uco-observable.File.modifiedTime||[file.json](https://github.com/casework/case/blob/master/examples/file.json)|
|MD5Object|uco-observable.ContentData|uco-observable.ContentData.Hash.hashMethod="MD5" AND uco-observable.ContentData.Hash.hashValue|||
|SHA1Object|uco-observable.ContentData|uco-observable.ContentData.Hash.hashMethod="SHA1" AND uco-observable.ContentData.Hash.hashValue|||
|SHA256Object|uco-observable.ContentData|uco-observable.ContentData.Hash.hashMethod="SHA256" AND uco-observable.ContentData.Hash.hashValue||[file.json](https://github.com/casework/case/blob/master/examples/file.json)|
|Signature|uco-observable.ContentData|uco-observable.ContentData.magicNumber||[file.json](https://github.com/casework/case/blob/master/examples/file.json)| //magicnumber (first few bytes of file)
|TypeObject|uco-observable.ContentData|uco-observable.ContentData.mimeType||[file.json](https://github.com/casework/case/blob/master/examples/file.json)|  //Type of file (slightly more expressive than MIMEType) (e.g. WhatsAppDB)
|ParentFile|uco-core.Relationship|separate Trace with a “contained-within” Relationship to it||[file.json](https://github.com/casework/case/blob/master/examples/file.json)| //pointer to file or directory that contains this file
|Dispositions|uco-action.Action; uco-action.ActionReferences|Action with name = sourcing verb (e.g. recover, carve, delete) AND uco-action.ActionReferences.object = id of file Trace||| // e.g. recovered, deleted, carved, on file system
|Length|uco-observable.File OR uco-observable.ContentData|uco-observable.File.sizeInBytes (file system asserted) OR uco-observable.ContentData.sizeInBytes (actual)||[file.json](https://github.com/casework/case/blob/master/examples/file.json)| //size in bytes

### File from Filesystem

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|DiskOffset|uco-core.Relationship; uco-observable.DataRange|separate “contained-within” Relationship between disk Trace and file Trace with DataRange.rangeOffset||| //position of first cluster of file content
|Identifier|Dependent on file system type (uco-observable.ExtInode for EXT, uco-observable.MftRecord for NTFS, etc.)|Dependent on file system type (uco-observable.ExtInode.extInodeID for EXT, uco-observable.MftRecord.mftFileID for NTFS, etc.)||| //iNode id
|DataRuns|uco-observable.File; uco-observable.ContentData; uco-observable.DataRange; uco-observable.Fragment; uco-core.Relationship|Trace for the file; separate Trace with ContentData for each byte run; separate “contained-within” Relationship between fragment and image/disk with DataRange property bundle for each byte run; separate “has-fragment” Relationship between file and fragment with Fragment property bundle for each byte run||| //offsets and length for each fragment of clusters of file
|ParentID|uco-core.Relationship|separate Trace with a “contained-within” Relationship to it||[file.json](https://github.com/casework/case/blob/master/examples/file.json)| //iNode id of file or directory that contains this file
|SlackStart|uco-core.Relationship; uco-observable.DataRange|separate “contained-within” Relationship (name = 'SlackStart') between disk Trace and file Trace with DataRange.rangeOffset||| //byte offset of the start of the slack space for file
|SlackDataRuns|uco-observable.File; uco-observable.ContentData; uco-observable.DataRange; uco-observable.Fragment; uco-core.Relationship|Trace for the file; separate Trace with name = 'SlackFragment' and ContentData for each byte run; separate “contained-within” Relationship between fragment and image/disk with DataRange property bundle for each byte run; separate “has-fragment” Relationship between file and fragment with Fragment property bundle for each byte run||| //offsets and length for each fragment of slack space of file

### File from NTFS Filesystem

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|StreamNumber|||||
|StreamName|||||
|MftModifiedTime|||||
|MftEntry|||||

### File from EXT Filesystem

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|InodeNumber|||||
|DirectoryEntryOffset|||||

### Media (disk image) Object

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Length|uco-observable.File OR uco-observable.ContentData|uco-observable.File.sizeInBytes (file system asserted) OR uco-observable.ContentData.sizeInBytes (actual)||[file.json](https://github.com/casework/case/blob/master/examples/file.json)| //size in bytes of the original native disk imaged
|Partitions|uco-core.Relationship|separate “contained-within” Relationship between partition Trace and image/disk with DataRange property bundle for each partition|||
|DisplayName|_More information needed_||||

### Partition Object

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Length|uco-observable.DiskPartition|uco-observable.DiskPartition.partitionLength||[file.json](https://github.com/casework/case/blob/master/examples/file.json)| //size in bytes of space reserved for partition
|Offset|uco-observable.DiskPartition|uco-observable.DiskPartition.partitionOffset||| //byte address of start of partition within the media/image
|DisplayName|uco-core.UcoObject.name|name property on the partition Trace|||
|Bootable|N/A (Gap)|||| //boolean
|Flags|uco-observable.DiskPartition|uco-observable.DiskPartition.diskPartitionType||| //internal representation (enumeration) for what type of partition
|FileSystem|uco-observable.FileSystem|uco-observable.FileSystem.fileSystemType||[file.json](https://github.com/casework/case/blob/master/examples/file.json)| //file system on the partition
|Recovered|uco-action.Action; uco-action.ActionReferences|Action with name = 'Recovered' AND uco-action.ActionReferences.object = id of Partition Trace||| //boolean for whether the partition was reconstituted from other space
||||||


### File System

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|AllocatedLength|N/A (Gap)?|||| //maximum potential size in bytes for file system
|Length|N/A (Gap)?|||| //size in bytes of actual file system including file system metadata structures (bigger than AllocatedLength)
|VolumeLabel|uco-core.UcoObject.name|name property on the volume Trace|||
|AllocationUnitSize|uco-observable.FileSystem|uco-observable.FileSystem.clusterSize||| //cluster size in bytes
|VolumeSerialNumber|uco-observable.Volume|uco-observable.Volume.volumeID||| //unique value issued by some OSs
|RootFile|uco-observable.File; uco-core.Relationship|Trace representing the root directory with uco-observable.File.isDirectory = 'true' AND “has-root-directory” Relationship between file system Trace and root file/directory Trace||| //pointer to file that represents root directory of file system
|FreeSpace|uco-observable.ContentData; uco-observable.DataRange; uco-core.Relationship|separate Trace with name = 'Free Space' and ContentData for each byte run; separate “contained-within” Relationship between free space byte run Trace and image/disk Trace with DataRange property bundle for each byte run||| //data runs of all chunks currently unused
||||||

### Operating System

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Users|||||
|Applications|||||
|BackedFiles|||||
|Servers|||||
|Drivers|||||
|HardwareDevices|||||
|RegisteredAccounts|||||
|SystemMountPoints|||||
|NetworkAdapters|||||
|Printers|||||
|WirelessNetworks|||||

### Windows Operating System (subtype of Operating System)

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|RecycleBinItems|||||
|PasswordHashes|||||
|PreFetchItems|||||
|ShimCacheItems|||||
|MachineSID|||||
|MachineSID|||||
|CurrentDomain|||||
|AutoLogon|||||
|Build|||||
|ServicePack|||||
|ProductID|||||
|ProductActivationKey|||||
|DefaultUserName|||||
|RegisteredOwner|||||
|RegisteredOrganization|||||
|DefaultUserName|||||
|DefaultDomainName|||||
|CurrentControlSetKeyName|||||

### SAM Entry

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|NTPasswordHash|||||
|UserID|||||
|UserName|||||

### Application (installed application)

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|DisplayName|||||
|InstallationDate|||||

### Driver (device driver)

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|DisplayName|||||
|InstallationDate|||||

### Service (daemon)

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|DisplayName|||||
|InstallationDate|||||
|Status|||||


### Registry Key

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Name|||||
|Keys|||||
|Values|||||
|Parent|||||
|ClassName|||||
|LastWriteTime|||||


### Email Message

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|ReceivedDateGMT|||||
|Subject|||||
|From|||||
|To|||||
|CC|||||
|BCC|||||
|Attachments|||||
|Content|||||


### URL Visit Record

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|URL|||||
|Visited|||||
|Server|||||

### Object type

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
||||||
||||||
||||||
Targets

- accounts
- chat messages (SMS, MMS, in platform chat)
- GeoLocation (geoJSON)
- archives entries (ZIP, TAR) - see "File" above, all extracted file contents adhere to this interface
- HFS+/HFSx
- picture files
- Contacts
- Calendar Entries
- phone calls
- Domain names
- network Connection
- PCAP
- exif
- sqlite
- certificates (X509, etc.)
