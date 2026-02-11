Assignment day 3
Bishoy nabil asaad

1- Create a system user (no login shell, no home directory) named webapp_user. This user will own the application files. 

- `useradd -M -r -s /sbin/nologin webapp_usert`

2-Create a system group named webapp_support.   
- `Groupadd -r webapp_support`

3- Create a regular user named support1. Ensure this user is added to the webapp_support group as a secondary group.

- `useradd -m support1`
 
- `usermod -g webapp_support support1`

4-Create the following directory tree under /opt/webapp/:

- `mkdir -p /opt/webapp/bin/config/logs/`

5- Change the ownership of the entire /opt/webapp/ directory and all its contents to be owned by the user webapp_user and the group webapp_support.

- `chown -R webapp_user:webapp_support /opt/webapp`
 
6- Set directory permissions so that: webapp_user has full read, write, and execute access to everything. 
Members of the webapp_support group can: ▪Read and list contents of the config/ and logs/ directories. 
▪Read files inside config/ and logs/. 
▪Have no access (cannot list, read, or write) to the bin/ directory. 

All other users on the system (others) must have no access to any part of /opt/webapp/. 

- `chmod -R 700 /opt/webapp`
 
- `chmod g+rx /opt/webapp/bin/config/`
 
- `chmod g+rx /opt/webapp/bin/config/logs/`





             



          
             
