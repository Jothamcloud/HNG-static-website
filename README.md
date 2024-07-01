# HNG Static Website

This is a static website created as part of the HNG Internship program.

## Author
- **Name:** Arinze Jotham
- **Username:** Majestic
- **Email:** ArinzeJotham60@gmail.com

## Project Description
This project includes a simple static website with the following content:
- A welcome message
- The author's name, username, and email
- A mention of the HNG Internship with a link to [HNG Internship](https://hng.tech)

## Files Included
- `index.html`: The main HTML file for the static website.

## Steps to Create the Project

1. **Set Up an EC2 Instance:**
   - Go to the AWS Management Console.
   - Navigate to the EC2 Dashboard.
   - Click on **Launch Instance**.
   - Choose the Amazon Linux 2 AMI.
   - Select an instance type (t2.micro is eligible for the free tier).
   - Configure instance details, storage, and security group (allow HTTP traffic on port 80).
   - Launch the instance and connect using EC2 Instance Connect.

2. **Install Apache Web Server:**
   Connect to your EC2 instance and run the following commands:
   ```sh
   sudo yum update -y
   sudo yum install httpd -y
   sudo systemctl start httpd
   sudo systemctl enable httpd

3. **Create the HTML File Using Echo:**
   ```sh
   echo 'Your HTML code' | sudo tee /var/www/html/index.html
