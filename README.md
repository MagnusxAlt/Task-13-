### Task: Deploy and Access Free AWS VM ###

Step 1: Create a Free AWS EC2 Instance

Logged into AWS Console and navigated to the EC2 Dashboard.
Clicked Launch Instance.
Selected Amazon Linux 2023 AMI.
Chose t2.micro instance type (free tier eligible).
Configured the instance with default settings and created a key pair for SSH access.
Allowed inbound traffic (SSH on port 22) by editing the security group.
Launched the EC2 instance and noted down the Public IPv4 Address.
Public IP: your public ip addresss of the cloud 

Step 2: Ping the VM from Kali Linux

From my Kali Linux terminal, I attempted to ping the public IP of the AWS VM to check if it's reachable.
```bash```
          ```ping (public IPV4)```

Took a screenshot of the successful ping response.

Step 3: SSH into the AWS VM

Used SSH to connect to the EC2 instance:
  
sudo ssh -i ~/Documents/cloudkey.pem ec2-user@(public ip address)

Successfully logged into the VM.

Took a screenshot of the terminal showing the SSH connection.

Step 4: Run ip a Command on the VM

Ran the ip a command on the VM to display the network interfaces and IP addresses.
      
`ip a`

Took a screenshot of the command output showing the IP addresses.

Step 5: Ping Public IP from the AWS VM

Attempted to ping the public IP from the AWS VM to test outbound connectivity:

`ping (public IPV4)`

Step 6: Shutdown and Terminate the VM

Shutdown the VM once done:

`sudo shutdown - h now`
After ensuring the VM is stopped, went to the AWS EC2 console and terminated the instance to free up resources.
