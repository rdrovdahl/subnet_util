# subnet_util

## Overview
Simple library that can be used to perform subnet calculations and validate
the format of IPv4 IP Addresses and Subnet Masks.

## Table of Contents
  * [Creating an object](#creating-an-object)
  * [check_ip method](#check_ip-method)
  * [check_mask method](#check_mask-method)
  * [ip method](#ip-method)
  * [subnet method](#subnet-method)
  * [network method](#network-method)
  * [broadcast method](#broadcast-method)
  * [subnet_bits method](#subnet_bits-method)
  * [host_count method](#host_count-method)

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
# ip method
The ip method will return the ip address in either dotted decimal format or binary format if the 'binary' argument is set to **True**.  By default, it will return the ip in dotted decimal format.
```
$ a.ip()
'10.0.0.1'
```
```
$ a.ip(binary=True)
'00001010000000000000000000000001'
```
# subnet method
The subnet method will return the subnet mask in either dotted decimal format or binary format if the 'binary' argument is set to **True**.  It is also possible to return the wildcard mask in either decimal or binary format when setting the wildcard argument to **True**.
```
$ a.subnet()
'255.255.0.0'
```
```
$ a.subnet(binary=True)
'11111111111111110000000000000000'
```
```
$ a.subnet(wildcard=True)
'0.0.255.255'
```
```
$ a.subnet(wildcard=True, binary=True)
'00000000000000001111111111111111'
```
# network method
The network method will return the network address in either dotted decimal format or binary format if the 'binary' argument is set to **True**.  By default, it will return the network address in dotted decimal format.
```
$ a.network()
'10.0.0.0'
```
```
$ a.network(binary=True)
'00001010000000000000000000000000'
```
# broadcast method
The broadcast method will return the broadcast address in either dotted decimal format or binary format if the 'binary' argument is set to **True**.  By default, it will return the broadcast address in dotted decimal format.
```
$ a.broadcast()
'10.0.255.255'
```
```
$ a.broadcast(binary=True)
'00001010000000001111111111111111'
```
# subnet_bits method
The subnet_bits method will return the number of subnet bits in the familiar shorthand version of '/' + number of bits.
```
$ a.subnet_mask
'255.255.0.0'
$ a.subnet_bits()
'/16'
```
# host_count method
The host_count method returns the number of valid hosts in a given network not including the **network address** and the **broadcast address**.
```
$ a.host_count()
65534
```
### Special Recognition
This library is largely a derivative of code developed by Mihai Catalin Teodosiu
