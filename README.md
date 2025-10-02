# osquery
Basics...

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



