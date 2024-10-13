Here’s the process formatted in Markdown without the "Copy" labels:

Step 1: Generate SSH Private and Public Keys on VM-UBUNTU-ANSIBLE
Log into VM-UBUNTU-ANSIBLE (your controller node):


ssh username@68.219.176.233
Generate an SSH key pair:
Run the following command to create an SSH key pair. When prompted, press "Enter" to accept the default file location and leave the passphrase empty (or set one if desired).


ssh-keygen -t rsa -b 4096
You will see something like this:


Generating public/private rsa key pair.
Enter file in which to save the key (/home/username/.ssh/id_rsa):
[Press Enter]
Enter passphrase (empty for no passphrase): 
[Press Enter]
Enter same passphrase again: 
[Press Enter]
The public key will be saved in ~/.ssh/id_rsa.pub and the private key in ~/.ssh/id_rsa.

Step 2: Copy the Public Key to VM-UBUNTU-001
Copy the public key to the target VM (VM-UBUNTU-001):
Use the ssh-copy-id command to copy your public key from VM-UBUNTU-ANSIBLE to VM-UBUNTU-001:


ssh-copy-id username@20.224.65.3

If prompted to accept the host's fingerprint:
Type yes and enter the password for username on VM-UBUNTU-001 when prompted.