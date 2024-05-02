# Kong

Run Kong with Postgres.

```bash

KONG_DATABASE=postgres docker compose --profile database up -d

```

# Results

```bash

ab -k -n 10000 -c 50 http://localhost:8000/weather

Server Software:        Kestrel
Server Hostname:        localhost
Server Port:            8000

Document Path:          /weather
Document Length:        14 bytes

Concurrency Level:      50
Time taken for tests:   207.499 seconds
Complete requests:      10000
Failed requests:        0
Keep-Alive requests:    0
Total transferred:      2730028 bytes
HTML transferred:       140000 bytes
Requests per second:    48.19 [#/sec] (mean)
Time per request:       1037.494 [ms] (mean)
Time per request:       20.750 [ms] (mean, across all concurrent requests)
Transfer rate:          12.85 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.2      0       4
Processing:  1002 1032 120.5   1018    3369
Waiting:     1002 1031 120.5   1018    3369
Total:       1002 1032 120.7   1019    3373

Percentage of the requests served within a certain time (ms)
  50%   1019
  66%   1023
  75%   1026
  80%   1028
  90%   1034
  95%   1043
  98%   1066
  99%   1326
 100%   3373 (longest request)

```
