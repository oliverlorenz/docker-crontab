FROM alpine:latest
ADD ./alpine/crontab /crontab
CMD /usr/bin/crontab /crontab && /usr/sbin/crond -f
