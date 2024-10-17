# Removing an Empty Directory

If the directory is empty, you can use rmdir:

``` bash
rmdir /path/to/directory
```

# Removing a Non-Empty Directory

If the directory contains files or subdirectories, you can use rm with the -r (recursive) option:

``` bash
rm -r /path/to/directory
```

# Upload files/directories from PC to HPC

To upload a file from your Mac to an HPC system, you can use the scp (Secure Copy) command, which allows you to securely transfer files between computers.

Basic Syntax:

``` bash
scp /path/to/local/file username@hpc-address:/path/to/remote/directory
```

Transfer a Directory: To upload an entire directory, use the -r flag to recursively copy the contents:

``` bash
scp -r ~/Documents/my_directory username@hpc-address:/home/username/project/
```

Authentication: After running the command, you will be prompted to enter your password for the HPC system. Once authenticated, the file will be transferred.

It's fine to upload files using scp even if you're already connected to the HPC through SSH. However, scp operates independently from the current SSH session.You can use scp in another terminal window on your Mac.
