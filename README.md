# Automate-Backup-in-Rsync-Crontab
Automate Backup in Rsync &amp; Crontab 


## Rsync

`rsync` is a powerful command-line tool for syncing files and directories between two locations. It's commonly used for backups and mirroring data, thanks to its efficiency and versatility.

`rsync` is a versatile tool that provides efficient file synchronization and copying capabilities. Whether you're performing local backups, syncing files across different systems, or automating routine tasks, `rsync` offers robust features that can be customized to suit various use cases in Linux environments.

## Crontab

The `crontab` command in Linux is used to schedule tasks (commands or scripts) to run automatically at specified intervals or times.
Using `crontab`, you can automate repetitive tasks, backups, system maintenance, and more, making it a powerful tool for managing routine tasks on Linux systems.

## Introduction

Automating backups in Linux using `cron` and `rsync` is a practical approach to ensure regular and reliable backups of your important data. Here’s a step-by-step guide to set it up:

- Launch two instances.
- Connect the instances.
- Check the repo list (yum repolist all)
- Install the rsync command (sudo yum install rsync -y)


- On the destination instance also check the repolist and install the rsync command.



- Create a Directory on the Source instance.
- And create files in the directory.



- Create a directory in the destination instance.



- Use the rsync command key authentication source-path destination-path

**sudo rsync -av -e "ssh -i /home/ec2-user/Linux-Key.pem" /home/ec2-user/sourceBackup/* ec2-user@ip-172-31-90-18:/home/ec2-user/destinationBackup**



- The files are transferred to the destination instance when the command is executed successfully.



- To automate the transfer of files, we use `crontab` to schedule the execution of commands or scripts at specific times or intervals.
- Every minute the command will be executed.


- Check the crontab -l



- The destination instance does not have any files.



- After a minute the files are transferred to the destination instance.


## **Summary**

Following these steps, you can effectively automate backups using `cron` and `rsync` on your Linux system. This setup provides a robust solution for maintaining regular backups of critical files.