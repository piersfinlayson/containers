# motion

A container used for running motion https://github.com/Motion-Project/motion.  Consists of:
- motion
- msmtp(to email results of backups)

XXX fix below

You should link a host directory to /data for any photos/videos to be stored, and the motion config file to /etc/motion/motion.conf witihn the container.  Motion is executed automatically.

Port 8080 on the container exposes a control UI, and port 8081 the camera video.  (Your motion.conf must use these port numbers.)

A sample docker run command:

  docker run -v /cameras:/data -v ~/motion.conf:/etc/motion/motion.conf -p 8080:8080 -p 8081:8081 piersfinlayson/motion
To run, you need hree directories on your host to be mapped to the container:

Uploaded to hub.docker.com as piersfinlayson/motion
