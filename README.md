# README

`cleanes` is a script that clears up old snapshots from a ES repository and keeps only the number of snapshots from latest snapshot that are mentioned. The ES snapshot repository should exist otherwie it throws an error. It takes ES host, name of the snapshot repository, number of snapshots to keep. An optional variable is the connection timeout seconds to connect to the elasticsearch. Default timeout seconds is 30. It can be changed by specifying the appropriate flag. List of all the flags are given below.


## FLAGS:

| Flags | Usage|
| - | - | 
| `-e `	| Elastic Search Host whose snapshots are to be cleaned |
| `-n `	| Number of snapshots to keep |
| `-r `	| Repository name holding the snapshots |
| `-h `	| Help |
| `-t` 	| Timeout seconds to reach the ES Host.Default is 30 seconds |

## USAGE:

```
cleanes [FLAGS] [OPTIONS]
```

## Examples

> To delete snapshots from a host with connection timeout of 60 seconds(connection will be timed out after 60 seconds)
>```
>chmod +x cleanes
>
>./cleanes -e 'http://es:9200' -n 7 -r 'daily-snapshot' -t 60
>```

