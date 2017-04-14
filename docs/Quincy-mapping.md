---
title: Quincy CASE UCO mapping
---

# Quincy CASE UCO mapping


### File core properties

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|DisplayName||||| //filename
|FileAttributes|||| //flags vector for readonly, hidden, etc
|CreationTime||||
|LastAccessTime||||
|LastWriteTime||||
|MD5Object||||
|SHA1Object||||
|SHA256Object||||
|Signature|||| //magicnumber (first few bytes of file)
|TypeObject||||  //Type of file (slightly more expressive than MIMEType) (e.g. WhatsAppDB)
|ParentFile|||| //pointer to file or directory that contains this file
|Dispositions|||| // e.g. recovered, deleted, carved, on file system
|Length|||| //size in bytes
|||||
|||||

### File from Filesystem

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|DiskOffset||||| //position of first cluster of file content
|Identifier||||| //iNode id
|DataRuns||||| //offsets and length for each fragment of clusters of file
|ParentID||||| //iNode id of file or directory that contains this file
|SlackStart||||| //byte offset of the start of the slack space for file
|SlackDataRuns||||| //offsets and length for each fragment of slack space of file
||||||
||||||
||||||

### Media (disk image) Object

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Length||||| //size in bytes of the original native disk imaged
|Partitions|||||
|DisplayName|||||
||||||
||||||
||||||

### Partition Object

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Length||||| //size in bytes of space reserved for partition
|Offset||||| //byte address of start of partition within the media/image
|DisplayName|||||
|Bootable||||| //boolean
|Flags||||| //internal representation (enumeration) for what type of partition
|FileSystem||||| //file system on the partition
|Recovered||||| //boolean for whether the partition was reconstituted from other space
||||||


### File System

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|AllocatedLength||||| //maximum potential size in bytes for file system
|Length||||| //size in bytes of actual file system including file system metadata structures (bigger than AllocatedLength)
|VolumeLabel|||||
|AllocationUnitSize||||| //cluster size in bytes
|VolumeSerialNumber||||| //unique value issued by some OSs
|RootFile||||| //pointer to file that represents root directory of file system
|FreeSpace||||| //data runs of all chunks currently unused
||||||

### Foo Component

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|dd|||||

### Foo Component

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|dd|||||

### Foo Component

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|dd|||||

### Foo Component

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|dd|||||

### Foo Component

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|dd|||||

### Foo Component

|Quincy|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|dd|||||

Targets
- Operating System
- accounts
- applications
- chat messages (SMS, MMS, in platform chat)
- GeoLocation (geoJSON)
- email messages
- archives (ZIP, TAR)
- NTFS
- EXT
- HFS+
- HFSx
- picture files
- Contacts
- calendar Entries
- phone calls
- registry
- URLs
- Domain names
- network Connection
- MAC address
- ip address
- DNS
- TCP sessions
- HTTP sessions
- PCAP analysis
- exif
- sqlite
- certificates (X509, etc.)
