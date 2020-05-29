# Example of using K6 with grafana
Based on k6 example.
Includes a node.js server that will be tested

## Run node server

```bash
cd ./server
npm install
npm start
```

## Run grafana
```bash
./up.sh
```

In grafana it's a good idea to import a Dashboard in the right menu:
"+/import"
import via grafana.com

And import something like:
https://grafana.com/grafana/dashboards/2587
By inserting the number: 2098


## Run tests with k6
Test Simple Script
```bash
./test.sh     #Edit script to use or not grafana, vus, etc.
```

Test Script with modules (underscore, etc)
```bash
cd ./testlib
npm install
cd -
./testBundle.sh   #Edit script to use or not grafana, vus, etc.
```

## References
https://k6.io/docs/results-visualization/influxdb-+-grafana
https://k6.io/blog/k6-loves-grafana
https://github.com/loadimpact/k6
https://k6.io/docs/using-k6/modules
