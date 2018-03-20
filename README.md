# COSbenchPLOT
Generates PDFs from COSbench CSV files

Requires two arguments: -d (directory) and -t (plotType)

NOTE: exclude CSV files ending with "-worker.csv" results from 'init' stages, since they are empty

Tested with python 2.7.5
## Sample usage:
* $ ./plotter.py -d w169-hybrid/ -t throughput
* $ ./plotter.py -d w161-delete_write -t latency

## Sample output 1:
```
$ ./plotter.py -d w161-delete_write/ -t latency
Skipping CSV file:  w161-delete_write/s2-osd_failure-worker.csv
Plotting CSV file:  w161-delete_write/s2-osd_failure.csv
PROCESSING - plotting Statistics: latency
> Reading data from: w161-delete_write/s2-osd_failure.csv
> File creation time:  2018-03-20 10:53:17.323245
Operation Column range:  5 7
Operations found:  ['write', 'delete']
>* Adding a day at:  2018-03-20 00:00:04
> Number of time values:  960
> Created PDF chart: w161-delete_write_s2-osd_failure_LATENCY.pdf
Skipping CSV file:  w161-delete_write/s1-no_failure-worker.csv
Plotting CSV file:  w161-delete_write/s1-no_failure.csv
PROCESSING - plotting Statistics: latency
> Reading data from: w161-delete_write/s1-no_failure.csv
> File creation time:  2018-03-20 10:53:17.322245
Operation Column range:  5 7
Operations found:  ['write', 'delete']
> Number of time values:  961
> Created PDF chart: w161-delete_write_s1-no_failure_LATENCY.pdf
Plotting CSV file:  w161-delete_write/s3-node_failure.csv
PROCESSING - plotting Statistics: latency
> Reading data from: w161-delete_write/s3-node_failure.csv
> File creation time:  2018-03-20 10:53:17.323245
Operation Column range:  5 7
Operations found:  ['write', 'delete']
> Number of time values:  961
> Created PDF chart: w161-delete_write_s3-node_failure_LATENCY.pdf
Skipping CSV file:  w161-delete_write/s3-node_failure-worker.csv
```

## Sample output 2:
```
$ ./plotter.py -d w169-hybrid/ -t latency
PROCESSING - plotting Statistics: latency
> Reading data from: w169-hybrid/s2-osd_failure.csv
> File creation time:  2018-03-19 15:14:01.153289
Operation Column range:  9 13
Operations found:  ['read', 'list', 'write', 'delete']
> Number of time values:  962
> Created PDF chart: w169-hybrid_s2-osd_failure_LATENCY.pdf
PROCESSING - plotting Statistics: latency
> Reading data from: w169-hybrid/s1-no_failure.csv
> File creation time:  2018-03-19 15:14:01.150289
Operation Column range:  9 13
Operations found:  ['read', 'list', 'write', 'delete']
> Number of time values:  962
> Created PDF chart: w169-hybrid_s1-no_failure_LATENCY.pdf
PROCESSING - plotting Statistics: latency
> Reading data from: w169-hybrid/s3-node_failure.csv
> File creation time:  2018-03-19 15:14:01.155289
Operation Column range:  9 13
Operations found:  ['read', 'list', 'write', 'delete']
> Number of time values:  964
> Created PDF chart: w169-hybrid_s3-node_failure_LATENCY.pdf
```
