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

**IP Address** and **Subnet Mask**

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
The check_ip method will check the validity of the ip address.  If the address is valid, it will return 'True'.  If it is not valid, it will return 'False'
```
$ a.check_ip()
True
```
# check_mask method
The check_mask method will check the validity of the subnet mask.  If the subnet mask is valid, it will return 'True'.  If it is not valid, it will return 'False'
```
$ a.check_mask()
True
```


### Special Recognition
This library is largely a derivative of code developed by Mihai Catalin Teodosiu
