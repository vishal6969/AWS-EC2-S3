## Creating AWS account
* Signup on AWS,follow this link https://portal.aws.amazon.com/gp/aws/developer/registration/index.html?nc2=h_ct&src=header_signup
* After filling all details you will be asked to fill card details, this is a part of identification.
* AWS provides free tier account for 1 year. Read more about free tier to know better. https://aws.amazon.com/premiumsupport/knowledge-center/what-is-free-tier/

## Launch and Configure EC2 instance
*  Before moving forward, read about what is EC2 and its purpose. https://www.geeksforgeeks.org/what-is-elastic-compute-cloud-ec2/
* Open your AWS console and search EC2.
* After that go to instances section and launch an EC2 instance.
* Your EC2 instance should be launched with following specifications.
         1. Ubuntu 18
		 2. Auto-Assign Public IP: enable
		 3. TCP connection on Port 3000
* You will be asked to create a key pair, after creating store it somewhere safe on your device as it will be needed later.

## Connecting to EC2 instance from your device
* For this you need a powershell/cmd with ssh support or you can download git bash which already comes with ssh support.
* Open your chosen CLI in the folder where you saved the key pair.
* Now open AWS instances and click on connect after selecting your running EC2 instance.
* Now click on ssh client, follow the instructions and copy the command given, it must be something like this.

 ``
 ssh -i <key-pair-filename> username@<aws-dns-link>
 ``
* Paste the command in your CLI and you will enter your EC2 instance.

## Setup Nodejs Environment
* Copy and Paste the following commands to activate nvm on your machine.
 ``
 curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
 ``
 
 ``
 . ~/.nvm/nvm.sh
 ``
* Type following command to install node

 ``
 nvm install node
 ``
* Confirm proper installation of node by typing following command.
 
 ``
 node --version
``
 
## Running React Project 
* Clone your react project from github using following command.
``
 git clone <github project link>
``
* Navigate inside your project folder and type following commands one by one.

 ``
 npm install
 ``
 
 ``
 npm start
 ``
* Your project must be running on port 3000, you need to copy public IP DNS address of your EC2 instance and type following in browser.

 ``
 <Public IP DNS address>:3000
 ``
* Terminate the instance after this to avoid bills.

##### Video Tutorial: https://www.youtube.com/watch?v=TkJgvwJERK8&list=PLi32VcmBmvBgrrFpPe2BNkW83XSC0S_sm&index=1
