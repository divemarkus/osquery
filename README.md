# Osquery
Osquery is an open-source tool developed at Facebook that exposes an operating system as a relational database, allowing users to query OS data like running processes, kernel modules, and network connections using SQL. It serves as a powerful framework for security visibility, compliance monitoring, and incident response by providing detailed, unified data across different platforms, including Windows, macOS, and Linux.

### Basics...

```
# open command prompt as administrator

# install osquery:
winget install osquery.osquery -e

# initiate osquery:
osqueryi

# if you can't initiate osquery, navigate cmd prompt to directory
# cd c:\program files\osquery
# initiate osquery
osqueryi

# once you initiate osquery, you will see the osquery prompt
osquery>

# paste a sample code from this repo and press 'enter'
osquery> SELECT
    ...>   lp.pid,
    ...>   p.name                          AS process_name,
    ...>   lp.protocol,
    ...>   lp.address,
    ...>   lp.port
    ...> FROM listening_ports lp
    ...> JOIN processes p ON p.pid = lp.pid
    ...> WHERE lp.address NOT IN ('127.0.0.1', '::1')
    ...> ORDER BY lp.port;
``` 



