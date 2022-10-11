# Batch-Telnet
Batch push a telnet command, with optional secondary command.

This is designed for use with "apc>" devices
as telnet will look for the apc> prompt.
#### SEE: https://docs.python.org/3/library/telnetlib.html

### Reads Device IP's from: [template.xlsx](https://github.com/Protocol73/Batch-Telnet/edit/main/template.xlsx) - Column C
On run, will prompt for username/password for the batch;

Script then attempts to login & run whatever is in VAR = TelnetBatchRun <br>
Then it will return the results back to this sheet for each device.

### Second comand is reboot by default, Can be disabled by setting:
  reboot_after = False

## Example Retuned info: 
[First two columns are not parsed] And can be used for your own purpose. 

|Site/Location|Device| IP Address | Notes | Online Last Run | Last Ping |Reboot Notes|
|-----------|------------------------| --- | --- | --- | --- |---|
|||10.10.10.10|Success|TRUE|2022-10-11|Reboot Sent|
|||10.10.10.11|Success|TRUE|2022-10-11|Reboot Sent|
|||10.10.99.10|Login Failed|TRUE|2022-10-11|Run Failed|
|||10.11.10.12|Telnet Refused|TRUE|2022-10-11|Failed|
|||10.11.10.99|ICMP Timeout|FALSE||	Offline?|

--Protocol73
