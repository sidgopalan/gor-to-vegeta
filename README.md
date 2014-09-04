Gor To Vegeta
=============

Generates a [Vegeta](https://github.com/tsenart/vegeta) attack based on a [GOR](https://github.com/buger/gor) output file.

This tool is useful to load-test a service. For instance:

1. Run some integration tests against the service and use GOR to capture the requests

   ``sudo gor --input-raw :9070 --output-file requests.gor``

2. Run gor-to-vegeta to load-test the service based on the requests in the integration test

	``gor-to-vegeta --input-file ./requests.gor --target-host "localhost:8081" --duration 120s --rate 50``

