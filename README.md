# my-notes
how to generate ssh key-pair:
 ssh-keygen -f <any name>
 these keys will be available at /c/users/your name
 save the private key as .pem
 inorder to connect to the ec2 server, first import the keypair which was generated after importing public key
 IMPORTANT <LINUX COMMANDS>
 usermod -g <group name> <user name>
 here "g" is to represent main group for that perticular user
 similarly
 usermod -aG <group name> <user name>
 here -G is representing that it is a supplementary group for that user
 *****************************************************************************
 to delete the user from the group is
 gpasswd -d <user name> <group name> 
 _____________
 cut -d </ or : or any delimiter> -f1 ----- This command is used to devide the data in fragments with the help of using delimiter
 _____________
 awk -F </ or : / any delimiter> '{print 1F}' --- to represent the data column wise
**********************************************************************************
"EDITOR"
:/ -- search from the top
:? --- search from the bottom
:set nu --- to display numbers
:set nonu --- to remove numbers
:s/<word to find>/<word to replace with>/g
:2s/<word to find>/<word to replace>/g  -- to replace in the second line 
:%s/<word to find>/<word to replace>/g  -- to replace in the entire file
*********************************************************************************
how to configure firewall
__________________________
$ sudo yum install firewalld
$ sudo systemctl start firewalld.service
$ sudo systemctl enable firewalld.service
$ sudo systemctl status firewalld.service --- to check the status
$ sudo firewall-cmd --list-all
$ sudo firewall-cmd --permanent --add-port=80/tcp
$ sudo firewall-cmd --reload

how to configure selinux
________________________
$ sudo getenforce --- to see the status of selinux <enabled or permissive>
$ sudo semanage port -l --- to list all the ports
$ sudo semanage port -a -t <type like "http_port_t"> -p tcp <port number>

how to configure http service
_____________________________
$ sudo yum install httpd
---start, enable, and check the status using systemctl command
check the configuration file i.e /etc/httpd/conf/httpd.conf
*******************************************************************************************














