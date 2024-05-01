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
Server Port:            9080

Document Path:          /weather
Document Length:        14 bytes

Concurrency Level:      50
Time taken for tests:   206.840 seconds
Complete requests:      10000
Failed requests:        0
Keep-Alive requests:    0
Total transferred:      1520000 bytes
HTML transferred:       140000 bytes
Requests per second:    48.35 [#/sec] (mean)
Time per request:       1034.201 [ms] (mean)
Time per request:       20.684 [ms] (mean, across all concurrent requests)
Transfer rate:          7.18 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.2      0       5
Processing:  1001 1027 126.7   1013    3612
Waiting:     1001 1027 126.7   1013    3612
Total:       1001 1028 126.8   1013    3614

Percentage of the requests served within a certain time (ms)
  50%   1013
  66%   1016
  75%   1018
  80%   1020
  90%   1025
  95%   1032
  98%   1059
  99%   1359
 100%   3614 (longest request)

```
