Start a screen session:
```bash
screen -S <session name>
```
Navigate to the desired directory and start the download:
```bash
cd /desired/directory
wget https://github.com/Files-com/files-cli/releases/download/v2.13.105/files-cli_linux_64bit.tar.gz
tar zxvf files-cli_linux_64bit.tar.gz
./files-cli --api-key="c918900f412cd0fc0c48dd704c50c2b63c8a903498c900b8d013b20ce36353fe" download "Bioinformatic_Support/Shasta-pre-sales-data-sharing/Shasta_Total_RNA_100K_PBMC_NovaSeq" custom/path/to/download
```
Detach from the screen session: Press Ctrl-a then d to detach from the screen session. Your download will continue to run in the background.

To reattach to the screen session later:
```bash
screen -r download_session
```
To stop the current download, you will need to open a new SSH session to your HPC transfer node and terminate the process from there. Here are the steps:
Open a new terminal window and connect to your HPC transfer node again:
```bash
ssh <username>@hpc-transfer1.usc.edu
```
Find the process ID (PID) of the download command: use the ps command to list the running processes and identify the PID of the files-cli command.
```bash
ps -u <your_username>
```

Terminate the process: use the kill command followed by the PID to stop the download.
```bash
kill <PID>
```

If the process does not stop, you can use the -9 option to forcefully terminate it.
```bash
kill -9 <PID>
```
