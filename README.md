# XLDMTools: a set of tools to generate SQL scripts

* Author: Jens Mikkelsen
* Created: 2011 March 17

Licensed under the [GPL version 3] (http://www.gnu.org/licenses/) or later

## Introduction

XLDMTools is a set of tools to generate SQL scripts from XLDM files.
An XLDM file is a XML file describing a database Logic Data Model in a
platform agnostic format. Datatypes have to be specified in conformance
to ANSI-SQL.

XLDMTools generates SQL code for different RDBMSs, all datatypes are
translated to their corresponding types in the selected RDBMS.
All transformations use XSLT 1.0 which is supported by most browsers.
You can also use any other XLST 1.0 processor.

## Getting Started

There is a default test-schema.xml file that defines a simple database
schema and a set of target files that generate SQL create scripts for
different RDBMS.

All files starting with *build* are target files, they define the
schema to be used, and what action to do with it.
You can test any target file simply by opening it in your browser, you
should see the final SQL script right away.
