# Hash FileReader JS
Hashing big file with FileReader JS

* website example: https://lvaccaro.github.io/hashfilereader/
* medium post: https://medium.com/@0xVaccaro/hashing-big-file-with-filereader-js-e0a5c898fc98

### Re-order chunk technique:
* time-shifting: post-process not in order chunks
* memory-buffered: storing not in order chunks and then process at each new ordered chunk

### Performance 
Tested on Chrome 65.0 on macOS 10.12.6 with chunk size of 1Mb and 10Mb.

| File size     | Time (1Mb)  | Time (10Mb) | Memory (1Mb)   | Memory (10Mb)     |
| ------------- |:------:|:------:|:------:| -----:|
| 1Mb   | 0.052 sec | 0.056 sec | 0.056 sec | 0.043 sec |
| 10Mb  | 0.478 sec  |  0.42 sec  |   0.414 sec | 0.414 sec|
| 100Mb | 4.259 sec  |  3.865 sec  |    4.014 sec | 3.681 sec|
| 500Mb | 50.459 sec |  21.778 sec  |    20.236 sec | 18.611 sec|
| 1Gb   |   ---  | --- |  41.568 sec   | 37.096 sec |
