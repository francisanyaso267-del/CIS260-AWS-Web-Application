
# AWS Web Application Deployment Steps

## Project Overview
This project demonstrates how to deploy a web application using Amazon Web Services (AWS). The application is hosted on an Amazon EC2 instance and accessed through an Application Load Balancer (ALB).

## Step 1: Create an EC2 Instance
- Open the AWS Management Console.
- Navigate to Amazon EC2.
- Launch an EC2 instance using Amazon Linux 2023.
- Name the instance CIS260-Web-Server-1.

## Step 2: Install and Configure Apache
The following user-data script was used to install and start the Apache web server automatically:

```bash
#!/bin/bash
dnf install -y httpd
systemctl enable httpd
systemctl start httpd
```

## Step 3: Configure the Target Group
- Create a target group for the EC2 web server.
- Register the EC2 instance with the target group.
- Check the target health status.
- Confirm that the registered instance is Healthy.

## Step 4: Create the Application Load Balancer
- Create an Application Load Balancer.
- Configure it to forward incoming traffic to the target group.
- Use the Load Balancer DNS name to access the web application.

## Step 5: Configure Security
- Review the security group settings.
- Configure AWS security features as part of the project.
- Review AWS WAF configuration where applicable.

## Step 6: Test the Web Application
- Open the Application Load Balancer DNS name in a web browser.
- Confirm that the web application loads successfully.
- Verify that the EC2 instance is healthy in the target group.

## Project Files
- `README.md` – Project overview.
- `index.html` – Web application HTML page.
- `user-data.sh` – EC2 startup script.
- `architecture.png` – AWS architecture diagram.
- `deployment-steps.md` – Deployment documentation.

## Conclusion
This project provided hands-on experience with AWS services, including Amazon EC2, Application Load Balancing, target groups, and basic web server configuration.
