# FTP

### Show

>\# show version
>\# Show file systems
>\# show flash

### Copy

>\# copy "SRC" "DST" `( FTP or TFTP ( flash: `

### FTP Conf

>(conf)# ip ftp username "USR"
>(conf)# ip ftp password "PW"

### Cisco IOS 

**To Force boot**

>(conf)# boot system "FILEPATH" `( Flash: Cisco-V69.MK5`

Storage Management

># write `( Writest running config(DRAM) to startup config(NVRAM)`
># reload `( Restarts device`
># delete "FILE"