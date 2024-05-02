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
Time taken for tests:   206.359 seconds
Complete requests:      10000
Failed requests:        9
   (Connect: 0, Receive: 0, Length: 9, Exceptions: 0)
Non-2xx responses:      9
Keep-Alive requests:    10000
Total transferred:      2439352 bytes
HTML transferred:       139874 bytes
Requests per second:    48.46 [#/sec] (mean)
Time per request:       1031.795 [ms] (mean)
Time per request:       20.636 [ms] (mean, across all concurrent requests)
Transfer rate:          11.54 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.1      0       3
Processing:  1000 1024 122.7   1010    3021
Waiting:     1000 1024 122.7   1010    3021
Total:       1000 1024 122.8   1010    3023

Percentage of the requests served within a certain time (ms)
  50%   1010
  66%   1012
  75%   1013
  80%   1015
  90%   1018
  95%   1023
  98%   1037
  99%   1520
 100%   3023 (longest request)

```
