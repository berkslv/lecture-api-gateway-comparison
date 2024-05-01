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
Time taken for tests:   207.663 seconds
Complete requests:      10000
Failed requests:        0
Keep-Alive requests:    0
Total transferred:      2730009 bytes
HTML transferred:       140000 bytes
Requests per second:    48.15 [#/sec] (mean)
Time per request:       1038.316 [ms] (mean)
Time per request:       20.766 [ms] (mean, across all concurrent requests)
Transfer rate:          12.84 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.2      0       5
Processing:  1003 1030 124.8   1017    3254
Waiting:     1003 1029 124.7   1016    3253
Total:       1003 1030 124.9   1017    3256

Percentage of the requests served within a certain time (ms)
  50%   1017
  66%   1020
  75%   1023
  80%   1024
  90%   1030
  95%   1036
  98%   1050
  99%   1341
 100%   3256 (longest request)

```
