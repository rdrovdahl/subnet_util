# subnet_util

## Overview
Simple library that can be used to perform subnet calculations and validate
the format of IPv4 IP Addresses and Subnet Masks.

## Table of Contents
  * [Creating an object](#creating-an-object)
  * [check_ip method](#check_ip-method)
  * [check_mask method](#check_mask-method)

# Creating an object
This library uses the Subnet_util class.  To create an object, you'll need to supply two arguments:

    * IP Address (attribute = ip_address)
        examples - 10.0.0.10, 192.168.10.1

    * Subnet Mask (attribute = subnet_mask)
        examples - 255.255.255.0, 255.255.192.0

Here's an example of creating an object and calling its attributes
```
$ a = Subnet_util('172.16.10.1', '255.255.255.0')
```
```
$ a.ip_address
'172.16.10.1'
```
```
$ a.subnet_mask
'255.255.255.0'
```
# check_ip method
do this like this...

# check_mask method
and do this like this....


### Special Recognition
This library is largely a derivative of code developed by Mihai Catalin Teodosiu
