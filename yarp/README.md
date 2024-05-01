# YARP

Run YARP in a docker container.

```bash

docker-compose up -d

```

# Results

```bash

ab -k -n 10000 -c 50 http://localhost:9090/weather

Server Software:        Kestrel
Server Hostname:        localhost
Server Port:            8081

Document Path:          /weather
Document Length:        14 bytes

Concurrency Level:      50
Time taken for tests:   221.524 seconds
Complete requests:      10000
Failed requests:        0
Keep-Alive requests:    0
Total transferred:      1470000 bytes
HTML transferred:       140000 bytes
Requests per second:    45.14 [#/sec] (mean)
Time per request:       1107.619 [ms] (mean)
Time per request:       22.152 [ms] (mean, across all concurrent requests)
Transfer rate:          6.48 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    1   0.6      1       4
Processing:  1000 1100 667.4   1006   10509
Waiting:     1000 1100 667.4   1005   10509
Total:       1001 1101 667.4   1007   10509

Percentage of the requests served within a certain time (ms)
  50%   1007
  66%   1008
  75%   1009
  80%   1009
  90%   1010
  95%   1012
  98%   3010
  99%   5006
 100%  10509 (longest request)

```