# orangetimelapsepi

Scripts used to take pictures and create timelapse video from stills.

#### takepicture
This script is meant to be running on Raspberry Pi with camera enabled. Scheduled with cron:

```
AWS_CONFIG_FILE="/root/.aws/config"
*/2 * * * * /bin/bash /root/takepicture >> /var/log/camera.log 2>&1
```
Pi needs to have AWS CLI installed and configured
Depending on the confituration this file may require static credentials (not recommended)

#### user-data
This is the user-data for an EC2 instace used to download full contents of the container and generate output video in /vid.
I used EC2 instance with Ubuntu 16.04, with IAM role allowing S3 access.

#### example result:
https://youtu.be/EV1gahKwuJY
