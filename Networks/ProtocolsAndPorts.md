# Protocols and Ports

- - - -

## Table of Contents

* [Overview](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Networks/OsiModel.md#overview)
* [Data transfer protocols](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Networks/OsiModel.md#data-transfer-protocols)
* [DNS](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Networks/OsiModel.md#dns)
* [NTP](https://github.com/Sam-Ballantyne/DevNotes/blob/main/Networks/OsiModel.md#ntp)

## Overview

* Protocols are part of the Application Layer (7) of the OSI model
* But protocols all have a layer 4 component (Transport layer) which is implemented via ports
* e.g. HTTP uses port 80, HTTPS 443

## Data transfer protocols

* HTTP : Hypertext transfer protocol
* HTTPS : HTTP Secure
* FTP : File Transmission protocol
* sFTP : Secure
* TFTP : Trivial File Transport Protocol (for very small file transfers)
* SMB : Server message block

### Email

* SMTP : Simple Mail Transfer Protocol
* POP3 / IMAP : Used by client to pull emails from a server

### Authentication

* LDAP : Lightweight Directory Access Protocol, used in Windows 10
* LDAPs : Encrypted version of the above

### Network Management

* SSH : Secure Shell
* Telnet : Unencrypted
  * Both used by network admin to communicate with other devices on the network
* SNMP : Simple Network Management protocol, sends out request to all devices and requests info like what ports are open, logs etc
* RDP : Remove desktop protocol : allows you to remotely control a device

## DNS

* Stands for Domain Name System Protocol
* Converts URLs to IP addresses
* Allows us to lookup addresses and communicate over the internet
* All devices on the internet must have a public IP address to be able to communicate

## NTP

* Network Time protocol
* NTP server can reply to client requests as to the exact time
* Replies are done in UTC to avoid timezone issues
