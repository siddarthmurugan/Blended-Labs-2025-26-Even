# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**:SIDDARTH.M.V
* **Register Number**: 212225230267
* **Date of Submission**: 27/07/26

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Output Screenshots (Attach 3)


### Screenshot 1: VPC and Subnet Details

<img width="1905" height="916" alt="Screenshot 2026-08-17 134456" src="https://github.com/user-attachments/assets/1e682286-971f-4480-8f54-81c84c846940" />
<img width="1907" height="902" alt="Screenshot 2026-08-17 134334" src="https://github.com/user-attachments/assets/ac00f4a3-aea7-4962-b413-25cb5c929b15" />
<img width="1916" height="912" alt="Screenshot 2026-08-17 133657" src="https://github.com/user-attachments/assets/3e811895-90f2-4624-917a-e558c4a9d484" />
<img width="1915" height="926" alt="Screenshot 2026-08-17 133606" src="https://github.com/user-attachments/assets/ab7cb5ce-0bf4-4153-85bb-90b133285289" />
<img width="1907" height="912" alt="Screenshot 2026-08-17 133302" src="https://github.com/user-attachments/assets/5d393256-7dcf-407c-b853-249ca71a1f20" />

### Screenshot 2: EC2 Instance Running
<img width="1908" height="897" alt="Screenshot 2026-08-17 134941" src="https://github.com/user-attachments/assets/361bd890-7748-408d-8d99-bbc73a2e3e43" />
<img width="1895" height="860" alt="Screenshot 2026-08-17 135039" src="https://github.com/user-attachments/assets/b0acd653-b630-4895-9c4f-17ff77bc6c0d" />


### Screenshot 3: Web Server Output in Browser




## Result 
-17 135039" src="https://github.com/user-attachments/assets/4e9a85a7-802f-419d-887e-1de5a8783726" />

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
