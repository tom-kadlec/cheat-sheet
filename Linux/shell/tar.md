# tar

## Compress an Entire Directory or a Single File

Use the following command to compress an entire directory or a single file on Linux. It'll also compress every other directory inside a directory you specify — in other words, it works recursively.

```shell
tar -czvf name-of-archive.tar.gz /path/to/directory-or-file
```

Here's what those switches actually mean:

- -c: **C**reate an archive.
- -z: Compress the archive with g**z**ip.
- -v: Display progress in the terminal while creating the archive, also known as "**v**erbose" mode. The v is always optional in these commands, but it's helpful.
- -f: Allows you to specify the **f**ilename of the archive.

## Exclude Directories and Files

In some cases, you may wish to compress an entire directory, but not include certain files and directories. You can do so by appending an `--exclude` switch for each directory or file you want to exclude.

For example, let's say you want to compress /home/ubuntu, but you don't want to compress the /home/ubuntu/Downloads and /home/ubuntu/.cache directories. Here's how you'd do it:

```shell
tar -czvf archive.tar.gz /home/ubuntu --exclude=/home/ubuntu/Downloads --exclude=/home/ubuntu/.cache~
```

The `--exclude` switch is very powerful. It doesn't take names of directories and files — it actually accepts patterns. There's a lot more you can do with it. For example, you could archive an entire directory and exclude all .mp4 files with the following command:

```shell
tar -czvf archive.tar.gz /home/ubuntu --exclude=*.mp4
```

## Extract a Tar File

Once you have an archive, you can extract it with the tar command. The following command will extract the contents of archive.tar.gz to the current directory.

```shell
tar -xzvf archive.tar.gz
```

It's the same as the archive creation command we used above, except the `-x` switch replaces the `-c` switch. This specifies you want to e**x**tract an archive instead of create one.

You may want to extract the contents of the archive to a specific directory. You can do so by appending the `-C` switch to the end of the command. For example, the following command will extract the contents of the archive.tar.gz file to the /tmp directory.

```shell
tar -xzvf archive.tar.gz -C /tmp
```

Source: https://www.howtogeek.com/248780/how-to-compress-and-extract-files-using-the-tar-command-on-linux/
