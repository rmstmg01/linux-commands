# Linux Commands One Liner
### List out multiple IPv4/v6 IPs assigned to the server
IPv4: 
```
ip -4 a | grep global | sed 's/\/.*//g' | awk '{print $2}'
```
IPv6:
```
ip -6 a | grep global | sed 's/\/.*//g' | awk '{print $2}'
```
### Convert unix time stamp to human readable time format for access log

```
perl -pe 's/([\d]{10})/localtime $1/eg;'

```
###### For example:
```
cat access.log | perl -pe 's/([\d]{10})/localtime $1/eg;'
```


