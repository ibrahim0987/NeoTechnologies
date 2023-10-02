In this Github Repo you will find files the contains pipeline stages done by terraform, jenkinsfile


Steps Done:

**1. Define Project Scope and Requirements**
Review the provided assessment details to understand the project's objectives, requirements, and constraints.
Ensure you have a clear understanding of the Ghost CMS, AWS services, and the tools you'll be using (EC2, Jenkins, Terraform).
**2. Set Up AWS Environment**
Step 2.1: Sign Up for AWS and Configure AWS CLI
Sign up for an AWS account if you haven't already.
Install and configure the AWS CLI on your local machine.
**Step 2.2: Launch an EC2 Instance**
Use the AWS Management Console to launch an EC2 instance. Select the Amazon Linux AMI and choose an appropriate instance type.
Create a new key pair and download the private key file (key.pem).
**Step 2.3: Connect to the EC2 Instance**
SSH into the EC2 instance using the private key you downloaded.
**3. Set Up Jenkins on EC2**
**Step 3.1: Install Java**
Install Java on the EC2 instance using yum.
**Step 3.2: Install Jenkins**
Add the Jenkins repository and install Jenkins on the EC2 instance.
**Step 3.3: Start Jenkins Service**
Start the Jenkins service and enable it to start on boot.
**Step 3.4: Access Jenkins Web UI**
Open your web browser and navigate to http://<your-ec2-ip>:8080.
Follow the on-screen instructions to complete the setup. Retrieve the initial admin password.
**Step 3.5: Install Required Plugins
**Install necessary Jenkins plugins, including the Terraform plugin.
**4. Set Up Your GitHub Repository
**Step 4.1: Create a New GitHub Repository
Create a new GitHub repository where you'll store your Terraform code, Jenkins pipeline scripts, and other project files.
Step 4.2: Push Initial Code
Clone the repository to your local machine, add your Terraform files, and push them to GitHub.
5. Set Up Terraform on Jenkins
Step 5.1: Install Terraform on EC2
Connect to your EC2 instance and install Terraform.
Step 5.2: Install Terraform Plugin on Jenkins
In Jenkins, go to "Manage Jenkins" > "Manage Plugins" > "Available".
Search for and install the "Terraform Plugin".
Step 5.3: Configure Terraform in Jenkins
In Jenkins, go to "Manage Jenkins" > "Global Tool Configuration".
Add a Terraform installation, specifying the path where Terraform is installed on your EC2 instance.
6. Create a Jenkins Pipeline
Step 6.1: Create a New Jenkins Job
In Jenkins, click "New Item" to create a new job.
Select "Pipeline" and give it a name.
Step 6.2: Configure Jenkins Pipeline
In the pipeline settings, link it to your Git repository.
Step 6.3: Write Jenkinsfile
Create a Jenkinsfile in the root of your GitHub repository. This file defines your pipeline.
Step 6.4: Configure Pipeline Stages
Define stages in your Jenkinsfile, including:
	Pulling the code from GitHub.
	Running Terraform commands (init, plan, apply).
	Deploying your Ghost CMS.

8. Testing and Deployment
Step 8.1: Test Your Jenkins Pipeline
• Trigger the pipeline in Jenkins to ensure it pulls code, runs Terraform, and deploys Ghost CMS successfully.
Step 8.2: Verify Semgrep Results
• Check the Jenkins console output for Semgrep findings.
Step 8.3: Manual Testing
• Manually verify that Ghost CMS is accessible and functioning as expected.


