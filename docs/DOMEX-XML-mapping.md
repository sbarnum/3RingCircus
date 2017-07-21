---
title: DOMEX-XML CASE UCO mapping
---

# DOMEX-XML CASE UCO mapping

## Concept mappings

|DOMEX-XML|CASE/UCO|
|:---|:---|
|Collection|Investigation|
|MicroCollectionLocation|N/A (GAP)  ; Propose new generalized location facet/property bundle|
|Media or Device Metadata||
|Subject Metadata||
|File Metadata||
|Cellular Phone Exploitation Metadata||
|||
|||

## Collection Metadata mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|DOMEXID|uco-core.UcoObject|uco-investigation.Investigation.id|||
|Providing Organization|||||
|Owning Organization|||||
|Collection Name|uco-core.UcoObject|uco-investigation.Investigation.name|||
|Batch Name|||||
|Collection ID Number|||||
|Date Acquired|||||
|Collection Location Coordinates|||||
|Collection Country|||||
|Collection Description|uco-core.UcoObject|uco-investigation.Investigation.description|||
|Draft(Boolean)|||||
|Contains Objectionable Material(Boolean)|||||
|Contains suspected CP data(Boolean)|||||
|Contains US Persons Data(Boolean)|||||
|Restricted(Boolean)|||||
|Acquisition Details|||||
|Number of Components|||||
|Legal Title|||||
|Collecting Unit Collection Identification Number|||||
|Nationality of Collecting Organization|||||
|Reason for Collecting|||||
|Homeland Security|||||
|International Sharing Agreement|||||
|Law Enforcement Warrant|||||
|DoD Operation|||||

## Micro Collection Location mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Location Narrative||||||
|On Person||||||
|In Vehicle||||||
|At Building||||||
|On Battlefield||||||
|Other||||||

## Media or Device Metadata mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Data Owner||||||
|  Person Name||||||
|  Phone Number||||||
|Item Serial Number||||||
|Collecting Device Distinct Name||||||
|Name of Device Image File||||||
|Media type||||||
|Collection ID Number||||||
|Date Imaged||||||
|Type of Component||||||
|Exploitation Results Classification||||||
|Priority of Component||||||
|Image SHA256 Hash- Raw||||||
|Image MD5 Hash - Raw||||||
|Image SHA1 Hash - Raw||||||
|Source Content MD5 Hash||||||
|Source Content SHA1 Hash||||||
|Source Content SHA256 Hash||||||
|Image Size||||||
|Image Type||||||
|Image Classification||||||
|Locked Image||||||
|Disposition of Original Source||||||
|Firmware Manufacture||||||
|Firmware Part Number||||||
|Firmware Version or Release||||||
|BIOS Date and Time||||||
|Actual Date and Time||||||
|Media Size||||||
|Manufacturer||||||
|Model Number||||||
|Source Manufacturer||||||
|Processing Site||||||
|Contact Information||||||
|Tools/Processes Used||||||
|Type of System where Forensically Pure Image was Created||||||
|Software Used to Process||||||
|Versioning of Software||||||
|Explanation of Process||||||
|Damaged Flag||||||
|Repairs Performed by Person||||||
|Relationship of Multiple Images to Single Document||||||
|Number of Videos||||||
|Number of Audio Files||||||
|Number of Pictures||||||
|Cable/Reference/Message Traffic ID||||||

## Subject Metadata mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Type of Subject|||||
|Classification of the Subject|||||
|FISA Related|||||
|FISA Case ID|||||
|Other ID Type|||||


## File Metadata mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Harmony Number||||||
|Document Classification||||||
|Title Classification||||||
|Descriptive Title||||||
|Translated Title||||||
|Original Title||||||
|Original Title Language||||||
|Primary Language||||||
|Additional Languages||||||
|Document Date||||||
|Date Acquired||||||
|Entry Date||||||
|Document Type||||||
|Format||||||
|Project||||||
|Owning Agency||||||
|Country of Information||||||
|Country of Publication||||||
|Keywords||||||
|Related Document Numbers||||||
|Remark||||||
|List of ISNs||||||
|BIR Detainee Name||||||
|Biometric URLs||||||
|Date Accessed||||||
|Date Created||||||
|Date Modified||||||
|Disposition||||||
|Filename (Transliterated)||||||
|Original Filename||||||
|Filetype||||||
|Number of Pages||||||
|Number of Words||||||
|Duration||||||
|Media||||||
|Size||||||
|Source Path||||||
|Hash Value||||||
|Number of Duplicates in CDR||||||
|Number of Similar Files in CDR||||||
|Properties Last Edited By||||||
|Date and Time of Last Modification||||||
|Reason for Modification||||||
|Imported By||||||
|Subtitles||||||
|SubTitle Language||||||
|Production Group||||||
|Speaker Identification||||||
|Multimedia Audio File||||||
|Compression||||||
|Bit Rate||||||
|sampleRate||||||
|Channels||||||
|codec||||||
|Multimedia Video File||||||
|Creator Tool||||||
|Frame Rate||||||
|Data Rate||||||
|Length||||||
|Codec||||||
|Resolution||||||
|Malware||||||
|Multimedia EXIF Image||||||
|Model||||||
|Make||||||
|cameraSerialNumber||||||
|dateTimeOriginal||||||
|imageWidth||||||
|Image Length||||||
|GPS Coordinates||||||
|Translation||||||
|Translation Status||||||
|Translation Agency||||||
|Translation Type||||||
|Translation Date||||||
|Language From||||||
|Language To||||||
|Translation Document||||||
|Priority||||||
|Remarks||||||
|Requester||||||
|Requester Agency||||||
|Request Date||||||
|Date Required||||||
|Machine Translation Tool||||||


## Cellular Phone Exploitation Device Metadata mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Manufacturer||||||
|Model||||||
|Extraction Date||||||
|Owner||||||
|MSISDN||||||
|IMEI||||||
|Service Provider||||||
|Service Technology Type||||||
|  SIM Card Number||||||
|  SIM Card||||||
|  Hardware Version||||||
|Software Version||||||
|Time Set To||||||
|Actual Time||||||
|Memory Cards||||||
|Greeting Message||||||
|Keypad Lock Code||||||
|IMEI||||||
|  Make||||||
|  Model||||||
|  TAC||||||
|  Reporting Body||||||
|  Approved In||||||
|  Bands||||||
|SIM Cards||||||
|  MSISDN||||||
|  IMSI||||||
|  TMSI||||||
|  MMC||||||
|  MNC||||||
|  LAC||||||
|  ICCID||||||
|  SimCard Type||||||
|  ESN||||||

### Cellular Phone Exploitation Content: Contacts - Phone book entries mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Index|||||
|Name|||||
|Number|||||
|Original Name|||||
|Memory Location|||||
|Designation|||||


### Cellular Phone Exploitation Content: Call Log Entries mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Index|||||
|Name|||||
|Number|||||
|Original Name|||||
|Date/Time|||||
|Call Log Location|||||
|Memory Location|||||
|Duration|||||

### Cellular Phone Exploitation Content: SMS Messages mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Number|||||
|Date/Time|||||
|Original Message Text|||||
|Translated Message Text|||||
|Status|||||
|SMS Direction|||||
|Memory Location|||||

### Cellular Phone Exploitation Content: MMS Messages mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Name||||||
|Number||||||
|Date/Time||||||
|Original Message Text||||||
|Translated Message Text||||||
|MMS Direction||||||
|File Name||||||
|MD5 Hash Code Value||||||
|Status||||||
|Memory Location||||||

### Cellular Phone Exploitation Content: Calendar Events mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Original Title||||||
|Translated Title||||||
|Original Message Text||||||
|Translated Message Test||||||
|Event Location||||||
|Start Date/Time||||||
|End Date/Time||||||
|Is Reoccuring||||||

### Cellular Phone Exploitation Content: URL History mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|IP||||||
|URL||||||

### Cellular Phone Exploitation Content: Files mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|File Category||||||
|File Name||||||
|File Path Name||||||
|File Hash Code||||||
|File Size||||||

### Cellular Phone Exploitation Content: Email Messages mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Name||||||
|From Address||||||
|To Address||||||
|CC Address||||||
|Bcc Address||||||
|Date/Time||||||
|Original Message Text||||||
|Translated Message Text||||||
|Email Folder||||||
|Memory Location||||||

### Cellular Phone Exploitation Content: Selectors mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Selector||||||
|Realm||||||
|Is Validated||||||
|Identities||||||
|Locations||||||
|Normalized Tech Version||||||
|Selector Raw Value||||||

### Cellular Phone Exploitation Content: GPS Locations mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|GPS Way Point||||||
|Way Point Name||||||
|Last Selected DTG||||||
|Raw Latitude||||||
|Raw Longitude||||||
|Normalized Longitude||||||
|Normalized Latitude||||||
|Raw MGRS||||||
|Normalized MGRs||||||

### Cellular Phone Exploitation Content: Clocks mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Clocks||||||
|Location||||||
|Set Time||||||

### Cellular Phone Exploitation Content: User Defined Tags mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|User defined tags||||||

## Content and Analytic Metadata mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Person||||||
|Identity||||||
|Persona||||||
|Organization||||||
|Location||||||
|Equipment||||||
|Facility||||||
|systemUri||||||
|Email Address||||||
|Web Address||||||
|Credit Card Number||||||
|Personal ID||||||
|Money||||||
|Nationality||||||
|Religion||||||
|Distance||||||
|Time||||||
|Product||||||
|Financial Transaction||||||
|Travel||||||
|Event||||||

## Identity Metadata mapping

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|Person||||||
|Name||||||
|Alias (es)||||||
|ISN (Capture Tag Number)||||||
|Affiliations of Person||||||
|Date of Birth||||||
|Date of Death||||||
|Place of Birth||||||
|Place of Death||||||
|Gender||||||
|Occupation||||||
|Physical Description||||||
|Skill||||||
|Phone||||||
|Email Address||||||
|User ID||||||
|Affiliation||||||
|Citizenship||||||
|Education||||||
|Identification||||||
|Kinship||||||
|Location||||||
|Medical||||||
|Multimedia||||||
|     Reference Number/Control ID||||||
|     Biometric Link||||||
|     Remark||||||

## DDMS Security Attributes

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
|classification|||||
|ownerProducer|||||
|joint|||||
|SCIcontrols|||||
|SARIdentifier|||||
|atomicEnergyMarkings|||||
|disseminationControls|||||
|displayOnlyTo|||||
|FGISourceOpen|||||
|FGISourceProtected|||||
|releasableTo|||||
|nonICmarkings|||||
|classifiedBy|||||
|compilationReason|||||
|derivativelyClassifiedBy|||||
|nonUSControls|||||
|derivedFrom|||||
|declassDate|||||
|declassEvent|||||
|declassException|||||

## Object type

|DOMEX-XML|CASE/UCO Class|CASE/UCO Property|Mapping Examples|CASE/UCO Example|
|---|---|---|---|---|
||||||
||||||
||||||
