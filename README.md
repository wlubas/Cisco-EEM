# Cisco-EEM
My cisco scripts
Speedtest for Cisco IOS devices. Checks changes on interface's counters basing on data taken via snmp.

By default Ciscos show interface command shows 5 minute rate per interface. This script checks CURRENT interface's usage in 1s tact. It is usefull when you want to see real highest acheived values. For the traffic above 2000kBit units changes to Mbits to be more readable.


All you have to adjust are:
- your snmp community, snmp interface OID (line 22 and 23)
- put following command: aaa authorization exec default local   # this allows executing snmp querys to local host (when aaa new-model is used)
- if you use an access-list for snmp services, just add your localhost ip to it permit 127.0.0.1
- put alias exec speedtest tclsh flash:/speedtest   #just to make an alias for your script file

