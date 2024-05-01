# REST API Service

This is a simple REST API service that waits 1000ms before responding to a request.

## Run with Docker

```bash

docker build -t berkslv/service .

docker run -p 8080:8080 -d --network=docker-apisix_apisix --name service berkslv/service 

```

## Results

```bash

ab -k -n 10000 -c 50 http://localhost:8080/weather

Server Software:        Kestrel
Server Hostname:        localhost
Server Port:            8080

Document Path:          /weather
Document Length:        14 bytes

Concurrency Level:      50
Time taken for tests:   202.248 seconds
Complete requests:      10000
Failed requests:        0
Total transferred:      1470000 bytes
HTML transferred:       140000 bytes
Requests per second:    49.44 [#/sec] (mean)
Time per request:       1011.241 [ms] (mean)
Time per request:       20.225 [ms] (mean, across all concurrent requests)
Transfer rate:          7.10 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    2   0.8      2       6
Processing:  1000 1004   2.1   1004    1030
Waiting:     1000 1004   2.0   1004    1030
Total:       1000 1006   2.4   1006    1032

Percentage of the requests served within a certain time (ms)
  50%   1006
  66%   1007
  75%   1008
  80%   1008
  90%   1009
  95%   1009
  98%   1010
  99%   1011
 100%   1032 (longest request)

```
