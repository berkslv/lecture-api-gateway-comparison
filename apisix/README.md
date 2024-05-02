# Apache APISIX

Run Apache APISIX in a docker container.

```bash

docker-compose -p docker-apisix up -d

```

# Results


```bash

ab -k -n 10000 -c 50 http://localhost:9080/weather

Server Software:        APISIX/3.9.0
Server Hostname:        localhost
Server Port:            9090

Document Path:          /weather
Document Length:        14 bytes

Concurrency Level:      50
Time taken for tests:   206.130 seconds
Complete requests:      10000
Failed requests:        0
Keep-Alive requests:    0
Total transferred:      1520000 bytes
HTML transferred:       140000 bytes
Requests per second:    48.51 [#/sec] (mean)
Time per request:       1030.650 [ms] (mean)
Time per request:       20.613 [ms] (mean, across all concurrent requests)
Transfer rate:          7.20 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.2      0       7
Processing:   921 1025 126.2   1012    3376
Waiting:      921 1024 126.2   1011    3375
Total:        921 1025 126.3   1012    3378

Percentage of the requests served within a certain time (ms)
  50%   1012
  66%   1015
  75%   1017
  80%   1018
  90%   1023
  95%   1029
  98%   1047
  99%   1327
 100%   3378 (longest request)

```
