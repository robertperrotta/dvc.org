# import

Import file from URL to local directory and track changes in remote file.

Supported schemes:

* `local` - Local path
* `s3` - URL to a file on Amazon S3
* `gs` - URL to a file on Google Storage
* `azure` - URL to a file on Azure Blob Storage
* `ssh` - URL to a file on another machine with SSH access
* `hdfs` - URL to a file on HDFS
* `http` - URL to a file with a _strong ETag_ served with HTTP or HTTPS

```usage
    usage: dvc import [-h] [-q] [-v] url out

    positional arguments:
      url            URL
      out            Output

    optional arguments:
      -h, --help     show this help message and exit
      -q, --quiet    Be quiet.
      -v, --verbose  Be verbose.
```

## Examples

```dvc
    $ dvc import /path/to/data.csv local_data.csv
    $ dvc import s3://mybucket/data.csv s3_data.csv
    $ dvc import gs://mybucket/data.csv gs_data.csv
    $ dvc import azure://mybucket/data.csv azure_data.csv
    $ dvc import ssh://user@example.com:/path/to/data.csv ssh_data.csv
    $ dvc import hdfs://user@example.com/path/to/data.csv hdfs_data.csv
    $ dvc import https://example.com/path/to/data.csv http_data.csv
```
