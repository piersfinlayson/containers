# smartmontools

A container used for smart analysis of disk.  Consists of:
- smartmontools
- msmtp (to email results of backups)

To run, you need three directories on your host to be mapped to the container:
/scripts (where any script to run with live and will be run from)
/output (where output of backup scripts should be directed to)

A script could look something like this:

  smartctl -a /dev/sda |grep Realloc > /output/output.txt
  msmtp --host smtp.server.fqdn -f from@example.com to@example.com < /output/out.txt

Uploaded to hub.docker.com as piersfinlayson/smartmontools
