# Ocelot

```bash

ab -k -n 10000 -c 50 http://localhost:9090/weather

Server Software:        Kestrel
Server Hostname:        localhost
Server Port:            9090

Document Path:          /weather
Document Length:        14 bytes

Concurrency Level:      50
Time taken for tests:   207.739 seconds
Complete requests:      10000
Failed requests:        0
Keep-Alive requests:    0
Total transferred:      1470000 bytes
HTML transferred:       140000 bytes
Requests per second:    48.14 [#/sec] (mean)
Time per request:       1038.695 [ms] (mean)
Time per request:       20.774 [ms] (mean, across all concurrent requests)
Transfer rate:          6.91 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.1      0       2
Processing:  1001 1030 120.0   1016    3347
Waiting:     1001 1030 119.9   1016    3347
Total:       1001 1030 120.0   1016    3349

Percentage of the requests served within a certain time (ms)
  50%   1016
  66%   1020
  75%   1023
  80%   1025
  90%   1032
  95%   1040
  98%   1061
  99%   1359
 100%   3349 (longest request)

```