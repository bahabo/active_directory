# Installing the Domain Controller

1. Use `sconfig` to:
- Change the hostname
- Change the IP adress to static
- Change the DNS server to our own IP adress

2. Install the Active Directory Windows Feature

```shell
Install-WindowsFeature - AD-Domain-Services -IncludeManagementTools
```


```
Get-NetIPAddress
```



# Joining the Workstation to the Domain

```
Add-Computer -DomainName xyz.com -Credential xyz\Administrator -Force -Restart
```