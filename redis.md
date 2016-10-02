#### Installation

```
wget http://download.redis.io/redis-stable.tar.gz
tar xvzf redis-stable.tar.gz
cd redis-stable
make
```

#### Dependencies missing ?

```
cd deps
make hiredis jemalloc linenoise lua geohash-int
cd ..
make install
```

http://unix.stackexchange.com/questions/94479/jemalloc-and-other-errors-making-redis-on-centos-6-4

- [quickstart](http://redis.io/topics/quickstart)
- [jemalloc and other errors](http://unix.stackexchange.com/questions/94479/jemalloc-and-other-errors-making-redis-on-centos-6-4)
