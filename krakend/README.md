# KrakenD

Run KrakenD in a docker container.

```bash

docker-compose up -d

```

# Results

```bash

ab -k -n 10000 -c 50 http://localhost:9090/weather

Server Software:        
Server Hostname:        localhost
Server Port:            9090

Document Path:          /weather
Document Length:        14 bytes

Concurrency Level:      50
Time taken for tests:   206.298 seconds
Complete requests:      10000
Failed requests:        15
   (Connect: 0, Receive: 0, Length: 15, Exceptions: 0)
Non-2xx responses:      15
Keep-Alive requests:    10000
Total transferred:      2438920 bytes
HTML transferred:       139790 bytes
Requests per second:    48.47 [#/sec] (mean)
Time per request:       1031.488 [ms] (mean)
Time per request:       20.630 [ms] (mean, across all concurrent requests)
Transfer rate:          11.55 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.3      0       5
Processing:  1001 1024 122.7   1010    3076
Waiting:     1001 1024 122.7   1010    3076
Total:       1001 1024 122.9   1010    3081

Percentage of the requests served within a certain time (ms)
  50%   1010
  66%   1012
  75%   1014
  80%   1015
  90%   1019
  95%   1023
  98%   1041
  99%   1547
 100%   3081 (longest request)

```
