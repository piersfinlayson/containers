# backup

A container used for backups.  Consists of:
- rsync (to perform backups)
- msmtp (to email results of backups)
- ssh (to be used by rsync)

To run, you need three directories on your host to be mapped to the container:
/scripts (where your backup scripts live and will be run from)
/output (where output of backup scripts should be directed to)
/backup (where actual backups will be performed to)

A script could look something like this:

  rsync -aAXv -e "ssh -o StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null -i /scripts/id_rsa" user@host:/backup_this/ /backup/ >> /output/out.txt

  msmtp --host smtp.server.fqdn -f from@example.com to@example.com < /output/out.txt

Uploaded to hub.docker.com as piersfinlayson/backup
