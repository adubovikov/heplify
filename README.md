# heplify

### Usage of ./heplify:

```bash
  -b int
        Interface buffersize (MB) (default 64)
  -d string
        Enable certain debug selectors
  -e    Log to stderr and disable syslog/file output
  -f string
        BPF filter (default "greater 300 and portrange 5060-5090")
  -hd
        Deduplicate HEP packets
  -hf string
        Filter out REGISTER, OPTIONS ...
  -hs string
        HEP Server address (default "127.0.0.1:9060")
  -i string
        Listen on interface
  -kl int
        Rotate the number of log files (default 4)
  -l string
        Log level [debug, info, notice, warning, error] (default "warning")
  -lp int
        Loop
  -n string
        Log filename (default "heplify.log")
  -o    Read packet for packet
  -p string
        Log filepath (default "./")
  -r uint
        Log filesize (KB) (default 51200)
  -rf string
        Read packets from file. Please use -t file
  -s int
        Snap length (default 65535)
  -t string
        Capture types are [af_packet, pcap, file] (default "af_packet")
  -ts
        Topspeed uses timestamps from packets
  -v    Log at INFO level
  -wf string
        Write packets to file. Please use -t file

################################################################
./heplify -i eth0 -hf REGISTER


The last command will send HEP messages to localhost Homer. Messages will be captured from eth0.
It will filter out REGISTER and the default BPF Filter is greater 300 and portrange 5060-5090.
```