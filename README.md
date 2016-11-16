# Task:
Consume the logs and produce some statistics. Keep in mind that there might be a huge amount of logs.

A success log entry has the following structure:
```
HH:mm:ss:SS LEVEL - fetch http://www.server/endpoint.json took: timeInMilliseconds ms
```
A failure log entry has the following structure:
```
HH:mm:ss:SS LEVEL - error while fetching http://www.server/endpoint.json after timeInMilliseconds ms
```

## The output should look (roughly) like this:
```
http://srv1.kaufhof.de: avg: 215ms 478x success: 79%
 endpoints:
  products avg: 217ms count: 168x success: 81% (32 of 168 failed)
  teaser avg: 210ms count: 154x success: 76% (37 of 154 failed)
  profile avg: 220ms count: 156x success: 81% (31 of 156 failed)

http://srv2.kaufhof.de:
...
```