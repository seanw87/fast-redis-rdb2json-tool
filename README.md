# fastly transfer Redis rdb to json file


## parse redis rdb file as fast as you can imagine ##

This rdb file parsing tool is based on redis 4.0.2 source. Simply add cJSON module and push everything into json output.

\
### It's much faster than most of the tools based on python or lua plugin! ###
It’s based on the source file of Redis(C), so it’s much faster than any scripting languages.\
The memory usage is also tuned to occupy least(x MB for each instance)

Usage:
```
[allen@WXF_WORKSTATION root]$ path/to/rdb2json -f path/to/rdbfile -o path/to/json_outputfile [ -l path/to/logfile(default:/tmp/rdbtools.log) ]
```

applied redis key pattern: key1:key2:key3:...
the json output will be {"k1e2y1":"key1","k1e2y2":"key2","k1e2y3":"key3",...,"name1":"val1",...}, in which "name1" is the field name 

take a key for example: act:111:222.  In which 111 is the act id and 222 is the uid

take a shot at src/rdb.c and make it what you want!