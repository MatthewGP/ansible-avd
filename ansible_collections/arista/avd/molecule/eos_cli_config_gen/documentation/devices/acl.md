# acl

# Table of Contents

- [Management](#management)
  - [Management Interfaces](#management-interfaces)
  - [DNS Domain](#dns-domain)
  - [Name Servers](#name-servers)
  - [Domain Lookup](#domain-lookup)
  - [NTP](#ntp)
  - [Management SSH](#management-ssh)
  - [Management GNMI](#management-api-gnmi)
  - [Management API](#Management-api-http)
- [Authentication](#authentication)
  - [Local Users](#local-users)
  - [TACACS Servers](#tacacs-servers)
  - [IP TACACS Source Interfaces](#ip-tacacs-source-interfaces)
  - [RADIUS Servers](#radius-servers)
  - [AAA Server Groups](#aaa-server-groups)
  - [AAA Authentication](#aaa-authentication)
  - [AAA Authorization](#aaa-authorization)
  - [AAA Accounting](#aaa-accounting)
- [Management Security](#management-security)
- [Aliases](#aliases)
- [Monitoring](#monitoring)
  - [TerminAttr Daemon](#terminattr-daemon)
  - [Logging](#logging)
  - [SFlow](#sflow)
  - [Hardware Counters](#hardware-counters)
  - [VM Tracer Sessions](#vm-tracer-sessions)
  - [Event Handler](#event-handler)
- [MLAG](#mlag)
- [Spanning Tree](#spanning-tree)
- [Internal VLAN Allocation Policy](#internal-vlan-allocation-policy)
- [VLANs](#vlans)
- [Interfaces](#interfaces)
  - [Ethernet Interfaces](#ethernet-interfaces)
  - [Port-Channel Interfaces](#port-channel-interfaces)
  - [Loopback Interfaces](#loopback-interfaces)
  - [VLAN Interfaces](#vlan-interfaces)
  - [VXLAN Interface](#vxlan-interface)
- [Routing](#routing)
  - [Virtual Router MAC Address](#virtual-router-mac-address)
  - [IP Routing](#ip-routing)
  - [IPv6 Routing](#ipv6-routing)
  - [Static Routes](#static-routes)
  - [Router ISIS](#router-isis)
  - [Router BGP](#router-bgp)
  - [Router BFD](#router-bfd)
- [Multicast](#multicast)
  - [IP IGMP Snooping](#ip-igmp-snooping)
  - [Router Multicast](#router-multicast)
  - [Router PIM Sparse Mode](#router-pim-sparse-mode)
- [Filters](#filters)
  - [Community Lists](#community-lists)
  - [Peer Filters](#peer-filters)
  - [Prefix Lists](#prefix-lists)
  - [IPv6 Prefix Lists](#ipv6-prefix-lists)
  - [Route Maps](#route-maps)
  - [IP Extended Communities](#ip-extended-communities)
- [ACL](#acl)
  - [Standard Access-lists](#standard-access-lists)
  - [Extended Access-lists](#extended-access-lists)
  - [IPv6 Standard Access-lists](#ipv6-standard-access-lists)
  - [IPv6 Extended Access-lists](#ipv6-extended-access-lists)
- [VRF Instances](#vrf-instances)
- [Virtual Source NAT](#virtual-source-nat)
- [Platform](#platform)
- [Router L2 VPN](#router-l2-vpn)
- [IP DHCP Relay](#ip-dhcp-relay)

# Management

## Management Interfaces

### Management Interfaces Summary

IPv4

| Management Interface | description | VRF | IP Address | Gateway |
| -------------------- | ----------- | --- | ---------- | ------- |
| Management1 | oob_management | MGMT | 10.73.255.122/24 | 10.73.255.2 |

IPv6

| Management Interface | description | VRF | IPv6 Address | IPv6 Gateway |
| -------------------- | ----------- | --- | ------------ | ------------ |
| Management1 | oob_management | MGMT | not configured  | not configured |

### Management Interfaces Device Configuration

```eos
!
interface Management1
   description oob_management
   vrf MGMT
   ip address 10.73.255.122/24
```

## DNS Domain

DNS domain not defined

## Domain-List

Domain-list not defined

## Name Servers

No Name Servers defined

## Domain Lookup

DNS domain lookup not defined

## NTP

No NTP servers defined

## Management SSH

Management SSH is not defined

## Management API GNMI

Management API gnmi is not defined
  
## Management API HTTP


Management API HTTP is not defined

# Authentication

## Local Users

No Users Defined

## TACACS Servers

TACACS servers not configured

## IP TACACS Source Interfaces

IP TACACS source interfaces not defined

## RADIUS Servers

RADIUS servers not configured

## AAA Server Groups

AAA server groups not defined

## AAA Authentication

AAA authentication not defined

## AAA Authorization

AAA authorization not defined

## AAA Accounting

AAA accounting not defined

# Management Security

Management Security not defined

# Aliases

Aliases not defined

# Monitoring

## TerminAttr Daemon

TerminAttr Daemon not defined

## Logging

No logging settings defined

## SFlow

No sFlow defined

## Hardware Counters

No Hardware Counters defined

## VM Tracer Sessions

No VM tracer session defined

## Event Handler

No Event Handler Defined

# MLAG

MLAG not defined

# Spanning Tree

Spanning-Tree Not Defined

# Internal VLAN Allocation Policy

## Internal VLAN Allocation Policy Summary

**Default Allocation Policy**

| Policy Allocation | Range Beginning | Range Ending |
| ------------------| --------------- | ------------ |
| ascending | 1006 | 4094 |

# VLANs

No VLANs defined

# Interfaces

## Ethernet Interfaces

No Ethernet interface defined

## Port-Channel Interfaces

No Port-Channels defined

## Loopback Interfaces

No Loopback interfaces defined

## VLAN Interfaces

No VLAN interfaces defined

## VXLAN Interface

No VXLAN interface defined

# Routing

## Virtual Router MAC Address

IP Virtual Router MAC Address is not defined

## IP Routing

### IP Routing Summary

| VRF | Routing Enabled |
| --- | --------------- |
| default |  False| 

### IP Routing Device Configuration

```eos
```
## IPv6 Routing

### IPv6 Routing Summary

| VRF | Routing Enabled |
| --- | --------------- |
| default |  False | 

## Static Routes


## IPv6 Static Routes


## Router ISIS

Router ISIS not defined

## Router BGP

Router BGP not defined

## Router BFD

### Router BFD Multihop Summary

| Interval | Minimum RX | Multiplier |
| -------- | ---------- | ---------- |
| 300 | 300 | 3 |

*No device configuration required - default values

# Multicast

## IP IGMP Snooping

No IP IGMP configuration

## Router Multicast

Routing multicast not defined

## Router PIM Sparse Mode

Router PIM sparse mode not defined

# Filters

## Community Lists

Community Lists not defined

## Peer Filters

No Peer Filters defined

## Prefix Lists

Prefix lists not defined

## IPv6 Prefix Lists

IPv6 Prefix lists not defined

## Route Maps

No route maps defined

## IP Extended Communities

No Extended community defined

# ACL

## Standard Access-lists

### Standard Access-lists Summary

**ACL-API:**

| Sequence | Action |
| -------- | ------ |
| 10 | remark ACL to restrict access to switch API to CVP and Ansible |
| 20 | permit host 10.10.10.10 |
| 30 | permit host 10.10.10.11 |
| 40 | permit host 10.10.10.12 |

**ACL-SSH:**

| Sequence | Action |
| -------- | ------ |
| 10 | remark ACL to restrict access RFC1918 addresses |
| 20 | permit 10.0.0.0/8 |
| 30 | permit 172.16.0.0/12 |
| 40 | permit 192.168.0.0/16 |

**ACL-SSH-VRF:**

| Sequence | Action |
| -------- | ------ |
| 10 | remark ACL to restrict access RFC1918 addresses |
| 20 | permit 10.0.0.0/8 |
| 30 | permit 172.16.0.0/12 |
| 40 | permit 192.168.0.0/16 |

### Standard Access-lists Device Configuration

```eos
!
ip access-list standard ACL-API
   10 remark ACL to restrict access to switch API to CVP and Ansible
   20 permit host 10.10.10.10
   30 permit host 10.10.10.11
   40 permit host 10.10.10.12
!
ip access-list standard ACL-SSH
   10 remark ACL to restrict access RFC1918 addresses
   20 permit 10.0.0.0/8
   30 permit 172.16.0.0/12
   40 permit 192.168.0.0/16
!
ip access-list standard ACL-SSH-VRF
   10 remark ACL to restrict access RFC1918 addresses
   20 permit 10.0.0.0/8
   30 permit 172.16.0.0/12
   40 permit 192.168.0.0/16
```

## Extended Access-lists

Extended Access-lists not defined

## IPv6 Standard Access-lists

IPv6 Standard Access-lists not defined

## IPv6 Extended Access-lists

IPv6 Extended Access-lists not defined

# VRF Instances

No VRFs defined

# Virtual Source NAT

Virtual Source NAT is not defined

# Platform

No Platform parameters defined

# Router L2 VPN

Router L2 VPN not defined

# IP DHCP Relay

IP DHCP Relay not defined

# Custom Templates

No Custom Templates Defined