## Problem Statement
Build a file-based key-value data store that supports the basic CRD (create, read, and delete) operations. This data store is meant to be used as local storage for one single process on one laptop. The datastore must be exposed as a library to clients that can instantiate a class and work with the data store.

## Solution

 - C++ application to do CRD operation, satisfying the functional and non-Functional requirements.

## Operation Supported:

 - Create
 - Read
 - Delete

## Functionalities Supported:

 - [x] It can be initialized using an optional file path. If one is
       not provided, it will reliably create itself in a reasonable
       location on the laptop.
 - [x] A new key-value pair can be added to the data store using the
       Create operation. The key is always a string - capped at 32chars.
       The value is always a JSON object - capped at 16KB.
 - [x] If Create is invoked for an existing key, an appropriate error
       must be returned
 - [x] A Read operation on a key can be performed by providing the key,
       and receive the value in the response, as a JSON object.
 - [x] A Delete operation can be performed by providing the key.
 - [x] Appropriate error responses must always be returned to a client
       if it uses the data store in unexpected ways or breaches any
       limits.
 - [x] Every key supports setting a Time-To-Live property when it is created. 
       This property is optional. If provided, it will be evaluated as an integer 
       defining the number of seconds the key must be retained in the data store. 
       Once the Time-To-Live for a key has expired, the key will no longer be 
       available for or Delete operations
 
## Technology Stack
 -  C++

## Tools Used
 - Github
 - VS code