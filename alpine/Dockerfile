FROM alpine:latest
ADD ./crontab /crontab
CMD /usr/bin/crontab /crontab && /usr/sbin/crond -f
