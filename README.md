# dbcaster: a tool to define database structure and generate SQL scripts

*  Licensed under the [GPL version 3] (http://www.gnu.org/licenses/) or later.
*  Project Status: Alpha.

## Introduction

dbcaster is a tool to generate SQL output from XLDM files.
An XLDM file is a XML file describing a database structure in a
platform agnostic format.
This databse definition can be queried by different XSLT
scripts in order to generate different outputs.

To achieve platform independence certain conventions must be followed,
such as using ANSI SQL data types, which scripts will translate later into
platform specific data types.

Currently the available features include:  

* generating DDL code for creating and dropping tables, primary keys and foreign keys.
* syntax support for different RDBMSs. 
* type mappings between different RDBMSs (based on ANSI SQL).
* extensibility to add support for new RDBMSs syntax using template files.

Supported RDBMSs include:

* ANSI SQL (standard syntax, serves as reference and may be useful for compliant engines)
* MySQL
* Firebird
* MS SQL Server


## XLST processors support

All scripts require XSLT 1.0 and EXSLT. This features are supported by most
web browsers among other XSLT processors.
Currently this scripts have been tested with Firefox and Chromium, but you
should be able to use any processor with the mentioned features.

NOTE: If you are using Chromium you may have problems trying to use the files locally.
To solve this you can either access the files through a web server, or start
chromium with the --allow-file-access-from-files option.

## Getting Started

The quickest way to start defining a database is by modifying the default
test files included in the repository.

There is a default test-schema.xml file that defines a simple database
schema and a set of build files that generate DDL create scripts for
different RDBMS.

All files starting with *build* are examples of how to generate code, they
define the database schema to be used, and what target to execute with it.
Currently available targets are "create-all" and "drop-all".
You can test any build file simply by opening it in your browser, you
should see the final SQL script right away.

