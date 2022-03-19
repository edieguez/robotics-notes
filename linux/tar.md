# tar command

## Compress in tar.gz format

```shell
tar cvzf <filename>.tar.gz file1 [file2 file3 file4...]
```

- `-c, --create` Create a new archive.  Arguments supply the names of the files to be archived.  Directories are archived recursively, unless the --no-recursion option is given
- `-v --verbose` Verbosely list files processed.  Each instance of this option on the command line increases the verbosity level by one.  The maximum verbosity level is 3
- `-z, --gzip, --gunzip, --ungzip` Filter the archive through gzip
- `-f, --file=<filename>` Compress all the files into `filename`
