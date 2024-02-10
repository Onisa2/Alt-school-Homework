# Alt-school-Homework
Here are the commands i used to accomplish each task:
Prerequisite:Created altschool user 
Ans :sudo useradd -m altschool 
sudo passwd altschool
Making directories after logging into the user 
Ans : mkdir code tests personal misc

a. Change directory to the tests directory using absolute pathname:
Ans : cd /home/altschool/tests
b. Change directory to the tests directory using relative pathname:
Ans : cd ../tests
c. Use echo command to create a file named fileA with text content 'Hello A' in the misc directory:
Ans : echo 'Hello A' > /home/altschool/misc/fileA
d. Create an empty file named fileB in the misc directory. Populate the file with dummy content afterwards:
Ans : touch /home/altschool/misc/fileB
echo 'Dummy content' > /home/altschool/misc/fileB
e. Copy contents of fileA into fileC:
Ans: cp /home/altschool/misc/fileA /home/altschool/misc/fileC
f. Move contents of fileB into fileD:
Ans: mv /home/altschool/misc/fileB /home/altschool/misc/fileD
g. Create a tar archive called misc.tar for the contents of misc directory:
Ans tar -cf /home/altschool/misc.tar -C /home/altschool/misc .
h. Compress the tar archive to create a misc.tar.gz file:
Ans: gzip /home/altschool/misc/misc.tar
i. Create a user and force the user to change his/her password upon login:
Ans: sudo useradd -m -s /bin/bash -p $(openssl passwd -1 newpassword) alt
sudo passwd -e alt
j. Lock a user's password:
Ans: sudo passwd -l username
k. Create a user with no login shell:
Ans: sudo useradd -M username
l. Disable password-based authentication for SSH:
Ans : sudo nano /etc/ssh/sshd_config
found the PasswordAuthentication and changed it to no 
Then
Ans : sudo systemctl restart sshd
m. Disable root login for SSH:
Ans: sudo nano /etc/ssh/sshd_config
Found PermitRootLogin and changed it to no 
Then 
sudo systemctl restart sshd

