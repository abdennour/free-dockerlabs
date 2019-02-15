FROM jamtur01/redis
LABEL maintainer="mail@abdennoor.com"

ENV REFRESHED_AT 2019-02-14
ENTRYPOINT [ "redis-server", "--protected-mode no", "--logfile /var/log/redis/redis-replica.log", "--slaveof redis_primary 6379"]

