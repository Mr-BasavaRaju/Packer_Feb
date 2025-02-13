Golden AMIs (Imp):
----------------- 
Golden AMI’s are templates which contains following
Recent security patches
Logging agents
Monitoring agents


(FAQ) How do you build golden images in your project?
-
We build golden AMIs using Hashicorp Packer tool.

first Install Chocolatey for Windows OS :
--
- Step 1: Open  as Administrator
Press Win + X and select Terminal (Admin) or  (Admin).
If prompted by User Account Control (UAC), click Yes.
Step 2: Check Execution Policy
Run the following command to ensure scripts can be executed:

- Get-ExecutionPolicy
If it returns Restricted, change it by running:

- Set-ExecutionPolicy AllSigned -Scope Process

Set-ExecutionPolicy Bypass -Scope Process -Force
Step 3: Install Chocolatey
Run the following command to install Chocolatey:

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
Step 4: Verify Installation
After installation, close and reopen , then check if Chocolatey is installed:

choco -v
It should display the installed Chocolatey version.

Step 5: Install Software Using Chocolatey (Example)
Once installed, you can install software using Chocolatey. 

For example, to install Packer run:




choco install Packer  -y
Install Packer for Windows OS using Chocolatey 

- choco install packer 

Configure AWS access to your local laptop
Install AWS CLI (https://aws.amazon.com/cli/)
Create IAM User in AWS Console
Create Access keys to IAM user
Configure accesskey in your computer using AWS CLI
- aws configure
