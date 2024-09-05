To unzip or extract a .tar.gz file, you can use the tar command in a Bash environment. Here's the syntax:
```bash
tar -xzvf filename.tar.gz
```
Explanation:
x: Extracts the files from the archive.
z: Filters the archive through gzip (used for .gz files).
v: Verbose mode, showing the progress of the extraction.
f: Specifies the filename of the archive.
Example:
```bash
tar -xzvf my_files.tar.gz
```
This command will extract the contents of my_files.tar.gz into the current directory.

If you want to extract the files into a specific directory, you can add the -C option:
```bash
tar -xzvf my_files.tar.gz -C /path/to/destination
```
This will extract the files into the specified destination folder.