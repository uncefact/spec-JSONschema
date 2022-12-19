# UN/CEFACT JSON Schema draft 2020-12 meta-library publication

## Introduction

This directory contains JSON schema artefacts. They are fully based on the JSON schema draft 2020-12.
This means that they fully comply with the requirements of OpenAPI 3.1.x.  

The UN/CEFACT reference data models are provided in the library variant, with extended meta-information.  
This means that an individual meta-schema and an additional vocabulary is applied. The additional information
is included to support mapping-processes and the JSON-LD vocabulary creation. 

## Table of contents
<!-- TOC depthFrom:1 depthTo:3 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Basic schema design rules](#basicPrinciples)
  - [Basic Components](#basicComponents)
    - [Primitive data types](#pdt)
	- [Unqualified data types](#udt)
    - [Qualified data types](#qdt)	
- [JSON filenames and sub-folder structure](#jsonFilenames)
- [What is this meta-library ?](#metaLibrary)

<!-- /TOC -->

## Basic schema design principles

<a name="basicPrinciples" />
Basic rules of the UN/CEFACT Core Component Library can be [found here.](https://unece.org/trade/uncefact/ccts) The version CCTS 2.01 is applied.
In the linked PDF document abbreviations like ABIE, BBIE etc. are explained in detail.

The following figure shows how the different CCTS classes are interlinked and can be extended.
![Design principles](../../images/json_schema_principle.webp)

### Basic Components

<a name="basicComponents" />The lowest level provides all basic data types used throughout the complete Core Component Library. The include four different types of data types:

#### Primitive data types (PDT)

<a name="pdt" />The PDT summarize the representations of those types that are the foundation for all other data types. 
They include
1. __binaryType__  
to represent base64 encoded representation of binary information

2. __booleanType__
3. __decimalType__  
This type is defined to restrict a string to a pattern representing decimal representations of numbers. 
The JSON built-in numeric data type is not suitable when exchanging numbers that need to be uses as calculation
basis e.g. for prices, amounts, taxes, wages including roundings with the needed precision. Using only the standard JSON
numeric datatypes for those scenarios will lead to issues especially with rounding and accurracy.
4. __integerType__
5. __stringType__

PDTs are normally not used directly in any Core Component libary object. Moreover, they [UDTs](#udt) are used instead that amend the PDTs.

#### Unqualified data types (UDT)

<a name="udt" />UDTs are the real basic data types used in the Core Component library. They combine the value itself 
with supplementary components (SCs), where needed to bring the value into the correct context.

1. __amountType__ 
This type is used to represent all kind of amounts. 
2. __binaryObjectType__
3. __codeType__
4. __dateTimeType__
5. __dateType__
6. __graphicType__
7. __idType__
8. __indicatorType__
9. __measureType__
10. __numericType__
11. __percentType__
12. __pictureType__
13. __quantityType__
14. __rateType__
15. __soundType__
16. __textType__
17. __timeType__
18. __valueType__
19. __videoType__



## JSON filenames and sub-folder structure

<a name="jsonFilenames" />
<<<<<<< HEAD

* All files originally published by UN/CEFACT start with the prefix __UNECE-__
* The json schema file containing all basic components is named __UNECE-BasicComponents.json__
* All Reference Data Models (RDMs) and their contextualisations _end_ with the suffix __ContextCCL__.  
  The following files are representations of the official published RDMs. All other files ending with ContextCCL 
  are subsets of the corresponding RDMs.
    * Buy Ship Pay RDM: __UNECE-BSPContextCCL.json__
    * Multi Modal Transport RDM: __UNECE-MMTContextCCL.json__
    * Supply Chain RDM: __UNECE-SCRDMContextCCL.json__
    * Cross Border Management RDM: __UNECE-CBMContextCCL.json__
    * Pay RDM: __UNECE-PAYContextCCL.json__
    * eCertification RDM: __UNECE-eCertContextCCL.json__
    * Sustainable Development and Circular Economy RDM: __UNECE-SDCEContextCCL.json__
    * Experience Program RDM: __UNECE-EPContextCCL.json__
* All business documents (messages) are based on so called master-messages for the corresponding RDM. 
  All master message structures have a suffix __Master__.  
  For example the master message structure where all other business document structures are derived from
  is named __UNECE-BSPMaster.json__.
* All other json schema files with no special suffix are representations of business document message 
=======
- All files originally published by UN/CEFACT start with the prefix __UNECE-__
- The json schema file containing all basic components is named __UNECE-BasicComponents.json__
- All Reference Data Models (RDMs) and their contextualisations _end_ with the suffix __ContextCCL__.  
  The following files are representations of the official published RDMs. All other files ending with ContextCCL 
  are subsets of the corresponding RDMs.
    - Buy Ship Pay RDM: __UNECE-BSPContextCCL.json__
    - Multi Modal Transport RDM: __UNECE-MMTContextCCL.json__
    - Supply Chain RDM: __UNECE-SCRDMContextCCL.json__
    - Cross Border Management RDM: __UNECE-CBMContextCCL.json__
    - Pay RDM: __UNECE-PAYContextCCL.json__
    - eCertification RDM: __UNECE-eCertContextCCL.json__
    - Sustainable Development and Circular Economy RDM: __UNECE-SDCEContextCCL.json__
    - Experience Program RDM: __UNECE-EPContextCCL.json__
- All business documents (messages) are based on so called master-messages for the corresponding RDM. 
  All master message structures have a suffix __Master__.  
  For example the master message structure where all other business document structures are derived from
  is named __UNECE-BSPMaster.json__.
- All other json schema files with no special suffix are representations of business document message 
>>>>>>> 3fbc870a9a69c886e3e72407f1d27c24f818b36e
  structures. For example is the __UNECE-CrossIndustryInvoice.json__ the json schema represenation of
  the Cross Industry Invoice business document structure.


## What is this meta-library ?

<a name="metaLibrary" />
