![Docker Cloud Automated build](https://img.shields.io/docker/cloud/automated/oliverlorenz/crontab) ![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/oliverlorenz/crontab)
# docker-cron

This is a image to run cronjobs inside a docker container. The image has nothing installed. So this is a pure base image.

# usage

* create a crontab file. for example:

  ```
  ## Every minute print the date
  * * * * * rsync /a/local/file user@host:/a/remote/location
  ```

* create a new Dockerfile

  ```
  FROM oliverlorenz/cron:alpine
  RUN apk add --no-cache rsync
  ADD crontab /crontab
  ```

* build and use
