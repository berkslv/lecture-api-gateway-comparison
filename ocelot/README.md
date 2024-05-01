# Ocelot

```bash

ab -k -n 10000 -c 50 http://localhost:9090/weather

Server Software:        Kestrel
Server Hostname:        localhost
Server Port:            8080

Document Path:          /weather
Document Length:        14 bytes

Concurrency Level:      50
Time taken for tests:   216.595 seconds
Complete requests:      10000
Failed requests:        0
Keep-Alive requests:    0
Total transferred:      1470000 bytes
HTML transferred:       140000 bytes
Requests per second:    46.17 [#/sec] (mean)
Time per request:       1082.977 [ms] (mean)
Time per request:       21.660 [ms] (mean, across all concurrent requests)
Transfer rate:          6.63 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    1   0.6      1       4
Processing:  1000 1073 439.8   1006    6977
Waiting:     1000 1072 439.8   1006    6977
Total:       1000 1074 439.9   1007    6978

Percentage of the requests served within a certain time (ms)
  50%   1007
  66%   1008
  75%   1009
  80%   1010
  90%   1011
  95%   1014
  98%   2506
  99%   3008
 100%   6978 (longest request)

```