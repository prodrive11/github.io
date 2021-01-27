## rollin 

**Project description:** it's a commandline log streaming utility    

### 1. Features

* roll logs without stopping main application workflow  
* `roll` logs based on size, record count rules  
* archive old logs with given algorithm (gzip, lz4)  
* prune old archives - zero maintenance in prod   
* customize with different output sinks:  
  ** file  
  ** tcp  
  ** zmq  
  ** kdb  

### 1. Examples  

```bash
# 
$ cat file | rollin -n 100 -c 15 -p "$ENV.LOG.PATTERN.%T.out" -z lz4
```
