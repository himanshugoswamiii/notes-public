---
id: 9mvrjswcd2zbl9f22tcv7em
title: Tar Vs Zip
desc: ''
updated: 1708497806267
created: 1708495184521
---


## tar

The `tar` command itself *does not reduce file size*. It stands for "tape archive" and is used to **combine multiple files** and directories into one archive file, often for easy distribution or backup.

**Usage:**

```bash
tar -cf archive.tar *
```

> Make a tar file from all the files in the current dir (* is the regex)

However, tar is often used in conjunction with compression tools like gzip or bzip2 to reduce the size of files. When you see a file with extensions like .`tar.gz` or `.tar.bz2`, it means the tar file has been compressed with gzip or bzip2 respectively.


## .tar.gz

This means that a `.tar` file is compressed using `gzip`

#### Way-1

**2 step process to see the contents:**

```bash
gzip -d cn_core_host_dumpfile.tgz
```

> This will result in a `.tar` file

then you can unarchive these files

```bash
tar -xf cn_core_host_dumpfile.tar 
```

#### Way-2

```
tar -xzf archive.tar.gz
```

> This will uncompress the file as well  
> `-z` tells tar to uncompress the gzip-compressed archive.