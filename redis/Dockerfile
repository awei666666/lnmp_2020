FROM  redis:6.0.8

MAINTAINER bravist <chenghuiyong1987@gmail.com>

ENV REDIS_PASSWORD developer

CMD ["sh", "-c", "exec redis-server --requirepass \"$REDIS_PASSWORD\""]
