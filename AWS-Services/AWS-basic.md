for audit purpose
use IAM Credentials reports - to know the users and their details
    IAM access advisor - for services used by users

m5.2xlarge instance:

m - instance class
5 - generation (AWS improves them over time)
2xlarge - size within instance class

General Purpose EC2 instance type:
balance between: Compute Memory Networking
 with t type

Compute Optimized type instance:

with C type instance c5 c2

Memory Optimized EC2 Instance type:

R (stands for RAM) series instance

Storage Optimized EC2 Instance type:

will start with I/D/H1 


Security Groups acts as firewall to the EC2 instance

SG controls inbound network (from outside to instance traffic)
   controls outbound network (from the instance to outside traffic)

Classic Ports to know:

22 = SSH (Secure Shell) - log into a Linux instance
21 = FTP (File transfer protocol) - upload files into a file share
22 = SFTP (Secure File Transfer Protocol) - upload files using SSH
80 = HTTP - access unsecured websites
443 = HTTPS = access secured websites
3389 = RDP (Remote Desktop Protocol) -Log into a windows instance

If there is a website timeout(like infinite website loading), it could definitely turn out to be a Security Group issue
