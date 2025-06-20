# Active Directory Enumeration for Credential Gathering and Lateral Movement

This guide demonstrates how to enumerate an Active Directory (AD) environment to gather valuable information and credentials that may assist in lateral movement within a network.
🔧 First Tool – PowerShell Module

We'll start by using the ActiveDirectory PowerShell module, a native tool that allows us to operate more stealthily, since it doesn't require external binaries.
# Check if the Module is Available

First, verify if the required module is loaded:

Get-Module

If the ActiveDirectory module is not listed, import it with:

Import-Module ActiveDirectory

# Gather Domain Information

To retrieve basic information about the current domain:

Get-ADDomain

This will display details such as:

    Domain name

    Domain SID

    Functional level

    Parent/child domains

# Enumerate Users with SPNs

To find user accounts with Service Principal Names (often useful for Kerberoasting attacks):

Get-ADUser -Filter {ServicePrincipalName -ne "$null"} -Properties ServicePrincipalName

# Enumerate AD Groups

To list all groups in the domain:

Get-ADGroup -Filter * | Select-Object Name
