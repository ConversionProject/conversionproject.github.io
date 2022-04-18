---
title: 'Sympa AMI: Prerequisites'
---

\[[Japanese](../ja/rerequisites.md)\]
\[**English**\]

\[[Sympa AMI](../en.md) &gt; Prerequisites\]


Sympa AMI
=========

Prerequisites
-------------

## Hardware requirements

### Recommended specifications

  - Physical memory: 2 GB or more.
  - Free disk space: 512 MB or more.

    If a large number of lists are to be managed, more physical memory and disk space than the above are required.

    The database and list configuration information consumes very little space, but
    mail archives are expected to consume about three times the total amount of  stored messages.

## Network requirements

### Network security

The following traffic should be allowed in the security group settings: 

  - Inbound:

    HTTP/HTTPS (80/443)

    SMTP (25)

  - Outbound:

    SMTP(25)


## SMTP restrictions

### Remove restrictions on sending emails on AWS

  - In the [Request form](https://aws.amazon.com/jp/premiumsupport/knowledge-center/ec2-port-25-throttle/), specify the IP address to be unrestricted.

    Note that, at this time, also specify the value of the reverse lookup record (FQDN) for that IP address in "Elastic IPs information". If the application is accepted, this record is automatically set.

  - Without this request, only a small amount of emails can be sent out.

  - User with Admin rights can submit request.

## Required parameters

  * Email domain name.

    Prepare the email domain name to be used for the Sympa mailing list service.

  * Email address(es) of the listmaster(s).

    Prepare the email address(es) to manage the Sympa mailing list.
    The addresses of real humans are required.

  * Web site URL prefix.

    This is required if the Sympa mailing list is managed via a web GUI.
    The host part of the URL can be different from the email domain name above.


MX and A records must be registered on the DNS server in advance so that the host name of email domain name and web site URL above can be resolved.
If Sympa is operated with multiple email domain names, these parameters are required for each email domain name.
The same listmaster email address(es) can be set for all email domains.
The web site URL prefix is required if you want to provide a web interface for that email domain. In this case, the prefixes for different email domains must not overlap.

