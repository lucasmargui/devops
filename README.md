# 🧩 DevOps Documentation

DevOps professional focused on bridging development and operations to deliver **scalable**, **reliable**, and **automated solutions**.  
Experienced in CI/CD, Infrastructure as Code, cloud environments, containerization, monitoring, and microservices.  
Committed to collaboration, continuous improvement, and accelerating software delivery with quality and efficiency.


<details>
  <summary><b>📘 Table of Contents</b></summary>

- [🚀 DevOps Core Concepts](#devops-core-concepts)  
  - [Continuous Integration (CI)](#continuous-integration-ci)  
  - [Continuous Delivery/Deployment (CD)](#continuous-deliverydeployment-cd)  
  - [Microservices Architecture](#microservices-architecture)  
  - [Infrastructure as Code (IaC)](#infrastructure-as-code-iac)  
  - [Monitoring and Logging](#monitoring-and-logging)  
  - [Communication and Collaboration](#communication-and-collaboration)  

- [☁️ Infrastructure as Code (IaC) – Public Cloud](#infrastructure-as-code-iac--public-cloud)  
  - [Step 1 – Prerequisites](#step-1--prerequisites)  
  - [Step 2 – EC2](#step-2--ec2)  
  - [Step 3 – Create / Manage SSH Key Pair](#step-3--create--manage-ssh-key-pair)  
  - [Step 4 – Create a Security Group (Firewall Rules)](#step-4--create-a-security-group-firewall-rules)  
  - [Step 5 – Executing Script](#step-5--executing-script)  

- [🔐 Configuring AWS CLI Access Using IAM](#configuring-aws-cli-access-using-iam)  
  - [Step 1 – Install AWS CLI](#step-1--install-aws-cli)  
  - [Step 2 – Create a User Group (IAM Group)](#step-2--create-a-user-group-iam-group)  
  - [Step 3 – Create an IAM User](#step-3--create-an-iam-user)  
  - [Step 4 – Generate Access Keys](#step-4--generate-access-keys)  
  - [Step 5 – Configure the AWS CLI](#step-5--configure-the-aws-cli)  

- [🔑 Creating SSH Key Pair](#creating-ssh-key-pair)  
  - [Step 1 – Access the EC2 Service](#step-1--access-the-ec2-service)  
  - [Step 2 – Create a New Key Pair](#step-2--create-a-new-key-pair)  

- [💻 Creating an EC2 Instance with Terraform](#creating-an-ec2-instance-with-terraform)  
  - [Step 1 – Install and Configure Terraform](#step-1--install-and-configure-terraform)  
  - [Step 2 – Configure the Terraform Provider (main.tf)](#step-2--configure-the-terraform-provider-maintf)  
  - [Step 3 – Initialize the Terraform Project](#step-3--initialize-the-terraform-project)  
  - [Step 4 – Create EC2 Instance (ec2.tf)](#step-4--create-ec2-instance-ec2tf)  
  - [Step 5 – Configure Network (vpc.tf)](#step-5--configure-network-vpctf)  
  - [Step 6 – Create Security Group (security-group.tf)](#step-6--create-security-group-security-grouptf)  
  - [Step 7 – Create script (script.sh)](#step-7--create-script-scriptsh)
  - [Step 8 – Deploy the Infrastructure with Terraform](#step-8--deploy-the-infrastructure-with-terraform)  

- [🔌 Connecting to the EC2 Instance Using PuTTY](#connecting-to-the-ec2-instance-using-putty)  
  - [Step 1 – Get the Public IPv4 Address of Your Instance](#step-1--get-the-public-ipv4-address-of-your-instance)  
  - [Step 2 – Configure PuTTY](#step-2--configure-putty)  
  - [Step 3 – Start the SSH Session](#step-3--start-the-ssh-session)  

- [🧩 Microservices Overview](#microservices-overview)  
  - [Step 1 – Prerequisites Docker](#step-1--prerequisites-docker)  
  - [Step 2 – Concept Overview](#step-2--concept-overview)  
  - [Step 3 – Pulling the Official Apache Image](#step-3--pulling-the-official-apache-image)  
  - [Step 4 – Running an Apache Container](#step-4--running-an-apache-container)  
  - [Step 5 – Default Directory Structure](#step-5--default-directory-structure)  
  - [Step 6 – Stopping and Removing Containers](#step-6--stopping-and-removing-containers)  
  - [Step 7 – Listing and Removing Images](#step-7--listing-and-removing-images)  

- [🐳 Creating Custom Docker Images and Hosting in Docker Hub](#creating-custom-docker-images-and-hosting-in-docker-hub)  
  - [Step 1 – Clone the Website Repository](#step-1--clone-the-website-repository)  
  - [Step 2 – Create the Dockerfile](#step-2--create-the-dockerfile)  
  - [Step 3 – Build the Custom Image](#step-3--build-the-custom-image)  
  - [Step 4 – Run a Container from the Custom Image](#step-4--run-a-container-from-the-custom-image)  
  - [Step 5 – Push the Image to Docker Hub](#step-5--push-the-image-to-docker-hub)  
  - [Step 6 – Deploying the Image on Remote Servers](#step-6--deploying-the-image-on-remote-servers)  

- [🐳 Launching EC2 with Docker Image from Docker Hub](#launching-ec2-with-docker-image-from-docker-hub)  
  - [Step 1 – Prepare the Infrastructure with Terraform](#step-1--prepare-the-infrastructure-with-terraform)  
  - [Step 2 – Apply Terraform Configuration](#step-2--apply-terraform-configuration)  
  - [Step 3 – Connect to the Server Using PuTTY](#step-3--connect-to-the-server-using-putty)  
  - [Step 4 – Verify Docker Installation](#step-4--verify-docker-installation)  
  - [Step 5 – Check Downloaded Docker Images](#step-5--check-downloaded-docker-images)  
  - [Step 6 – Confirm the Running Container](#step-6--confirm-the-running-container)  

- [☁️ Create GitLab directory/repository](#-create-gitlab-directoryrepository)
  - [Step 1 – Create GitLab Account](#step-1--create-gitlab-account)
  - [Step 2 – Create a New Project](#step-2--create-a-new-project)
  - [Step 3 – Initialize Local Repository](#step-3--initialize-local-repository)
  - [Step 4 – Link Repository and Push Code](#step-4--link-repository-and-push-code)
  - [Step 5 – Provision EC2 Instance with Terraform](#step-5--provision-ec2-instance-with-terraform)
  - [Step 6 – Install GitLab Runner](#step-6--install-gitlab-runner)
  - [Step 7 – Register GitLab Runner](#step-7--register-gitlab-runner)
  - [Step 8 – Configure GitLab Runner User](#step-8--configure-gitlab-runner-user)
  - [Step 9 – Docker Hub Authentication](#step-9--docker-hub-authentication)

- [🐳 CI/CD Pipeline – Containerized Application](#-ci-cd-pipeline--containerized-application)
  - [Step 1 – Configure .gitignore](#step-1--configure-gitignore)
  - [Step 2 – Create Dockerfile](#step-2--create-dockerfile)
  - [Step 3 – Configure GitLab Pipeline](#step-3--configure-gitlab-pipeline)
  - [Step 4 – Build Docker Image](#step-4--build-docker-image)
  - [Step 5 – Deploy Container](#step-5--deploy-container)
  - [Step 6 – Update Application Version](#step-6--update-application-version)

</details>

---

## 🚀 DevOps Core Concepts

<details> <summary>Click to show details</summary> 

### Continuous Integration (CI)
Automated process of integrating code changes frequently into a shared repository with immediate validation through testing.

<details>
  <summary>Click to show details</summary>
  <img width="784" height="792" alt="CI Diagram" src="https://github.com/user-attachments/assets/bd54ec2c-7ce2-4c55-8e54-e63c3805c0f4" />
</details>

---

### Continuous Delivery/Deployment (CD)
Ensures software is always in a deployable state and automates releases to production environments safely and efficiently.

<details>
  <summary>Click to show details</summary>
  <img width="1358" height="586" alt="CD Diagram" src="https://github.com/user-attachments/assets/6d985365-aa09-4bc9-b863-16078a7e400c" />
</details>

---

### Microservices Architecture
Designing applications as **small**, **independent**, and **loosely coupled services** to improve scalability and maintainability.

<details>
  <summary>Click to show details</summary>
  <img width="1143" height="742" alt="Microservices Diagram" src="https://github.com/user-attachments/assets/49226623-610d-4e18-b117-f04c99f16f6c" />
</details>

---

### Infrastructure as Code (IaC)
Managing and provisioning infrastructure using **code and automation** rather than manual processes.

<details>
  <summary>Click to show details</summary>
  <img width="1338" height="751" alt="IaC Diagram" src="https://github.com/user-attachments/assets/126f4250-3a96-4897-808b-0778f4b8849e" />
</details>

---

### Monitoring and Logging
Collecting and analyzing application and infrastructure data to detect issues, ensure performance, and support proactive incident response.

### Communication and Collaboration
Promoting cross-team alignment and transparency through shared responsibilities, tools, and workflows.

</details>

---

## ☁️ Infrastructure as Code (IaC) – Public Cloud

Creating an Instance Directly in AWS

<details>
  <summary>Click to show details</summary>

### Step 1 – Prerequisites
  
- AWS account created and verified (credit card / phone).
- IAM user with EC2/IAM permissions (root user acceptable for learning).
- **Windows:** download PuTTY and PuTTYgen.  
- **Linux/macOS:** ensure `ssh` is installed.

### Step 2 – EC2  
<details>
  <summary>Click to show details</summary>
  <img width="1053" height="604" alt="EC2 Creation" src="https://github.com/user-attachments/assets/42738fa8-1f2a-4765-ac32-a5142ea54608" />
</details>

### Step 3 – Create / Manage SSH Key Pair
Create via AWS Console or locally (`ssh-keygen`) and import the public key into AWS.  
Path: **EC2 → Key Pairs → Create Key Pair**

<details>
  <summary>Click to show details</summary>
  <img width="1067" height="319" alt="Key Pair" src="https://github.com/user-attachments/assets/dacaf6b5-8271-4fc4-874f-743678d677e1" />
</details>

### Step 4 – Create a Security Group (Firewall Rules)
Allow:
- SSH (port 22) — restricted to your IP.
- HTTP (port 80) — open to all (0.0.0.0/0).

<details>
  <summary>Click to show details</summary>
  <img width="1080" height="455" alt="Security Group" src="https://github.com/user-attachments/assets/34a39759-232d-4f39-b00a-0950574281e3" />
</details>

### Step 5 – Executing Script
In **Advanced settings**, attach the `script.sh` file to:
- Update the VM
- Install Apache
- Deploy the application

<details>
  <summary>Click to show details</summary>
  <img width="1042" height="724" alt="User Data Script" src="https://github.com/user-attachments/assets/4a4aa97b-4375-481e-bde7-ed0335215a24" />
</details>

</details>

---

## 🔐 Configuring AWS CLI Access Using IAM

This section explains how to set up AWS CLI authentication using **IAM (Identity and Access Management)**, allowing secure command-line access to your AWS resources.

<details> <summary>Click to show details</summary> 

### Step 1 – Install AWS CLI

Install and configure the **AWS Command Line Interface (AWS CLI)** — a unified tool that enables you to manage AWS services directly from your terminal.

<details>
  <summary>Click to show details</summary>
  <img width="1130" height="622" alt="AWS CLI Installation" src="https://github.com/user-attachments/assets/43bb56e1-bf6b-40fe-bd60-e54fa4cec711" />
</details>

---

### Step 2 – Create a User Group (IAM Group

1. In the AWS Management Console, navigate to **IAM (Identity and Access Management)**.  
2. On the sidebar, select **Groups → Create Group**.  
3. Name the group **cli-users**.  
4. Attach the **AdministratorAccess** policy (recommended only for testing environments).  
5. Click **Create Group** to finalize.

<details>
  <summary>Click to show details</summary>
  <img width="1047" height="225" alt="IAM Groups Navigation" src="https://github.com/user-attachments/assets/92650f80-33c6-4d39-8235-16ae47407761" />
  <br>
  <img width="1062" height="252" alt="IAM Group Creation" src="https://github.com/user-attachments/assets/2fad42b5-2c87-4ba2-b765-ac3d529f1ea1" />
</details>

---

### Step 3 – Create an IAM User

1. Still inside **IAM**, go to **Users → Add User**.  
2. Set the username to **lucasmarguaws**.  
3. Select the **Programmatic access** option (for CLI access).  
4. Add the user to the previously created **cli-users** group.  
5. Click **Create User** to complete the process.

<details>
  <summary>Click to show details</summary>
  <img width="728" height="140" alt="IAM User Creation Step 1" src="https://github.com/user-attachments/assets/ae621945-2f48-447f-9837-8ec394ad1b0f" />
  <br>
  <img width="1037" height="540" alt="IAM User Group Association" src="https://github.com/user-attachments/assets/4e0ecf82-1d45-43f4-b0b5-5c740d6c08f8" />
</details>

---

### Step 4 – Generate Access Keys

1. After the user is created, click the username (**lucasmarguaws**) to view its details.  
2. Go to the **Security credentials** tab.  
3. Click **Create access key** and choose the **Command Line Interface (CLI)** usage type.  
4. Copy and securely store the **Access Key ID** and **Secret Access Key** — they will be required for AWS CLI authentication.

<details>
  <summary>Click to show details</summary>
  <img width="1072" height="201" alt="Access Key Creation" src="https://github.com/user-attachments/assets/19d9bdb2-5f9f-41e0-a718-2936f005f8e0" />
  <br>
  <img width="1036" height="185" alt="Access Key Output" src="https://github.com/user-attachments/assets/002ec936-e699-486f-8693-9a9b4d515215" />
</details>

---

### Step 5 – Configure the AWS CLI

Open your terminal or Command Prompt and run:

```bash
aws configure
```

Provide your credentials when prompted:

```bash
AWS Access Key ID [None]: <your-access-key-id>
AWS Secret Access Key [None]: <your-secret-access-key>
Default region name [None]: us-east-1
Default output format [None]: json
```

<details> <summary>Click to show details</summary> <img width="996" height="142" alt="AWS Configure Example" src="https://github.com/user-attachments/assets/407e723f-8e12-4aae-8f38-4a7d4367a333" /> </details>

✅ Once completed, your AWS CLI is fully authenticated and ready to execute AWS commands or apply Terraform scripts securely and automatically.

</details>

---

## 🔑 Creating SSH Key Pair

This section describes how to create a **Key Pair** in AWS to enable secure **SSH access** to your EC2 instance.


<details> <summary>Click to show details</summary> 

### Step 1 – Access the EC2 Service

1. Open the **AWS Management Console**.  
2. Navigate to the **EC2** service.  

---

### Step 2 – Create a New Key Pair

1. In the left navigation pane, go to **Key Pairs** under **Network & Security**.  
2. Click **Create key pair**.  
3. In the **Name** field, enter: **Terraform**.  
4. Under **File format**, select **.ppk** (for PuTTY).  
5. Click **Create key pair**.  
6. Your browser will automatically download the file **Terraform.ppk**.  

💾 Save it in a secure location, for example:  

```
C:\Users<YourUser>.ssh\Terraform.ppk
```

✅ This key pair will later be referenced in Terraform to allow **SSH access** to the EC2 instance.

</details>

---

## 💻 Creating an EC2 Instance with Terraform

<details> <summary>Click to show details</summary> 

This section explains how to set up and deploy an **EC2 instance** using **Terraform**, an Infrastructure as Code (IaC) tool.


### Step 1 – Install and Configure Terraform

1. **Download** Terraform from the official site.  
2. **Add Terraform** to your system’s environment variables so the `terraform.exe` command can be executed from any directory.  

---

### Step 2 – Configure the Terraform Provider (main.tf)

Before deploying your infrastructure, you must define the **provider configuration**, which tells Terraform which cloud platform to interact with (in this case, **AWS**).

1. Navigate to your Terraform project directory.  
2. Create a new file named **main.tf** (or any name of your choice).  
3. Define the **provider block**, specifying **AWS** as your target platform.  

Terraform providers can be found on the **Terraform Registry**, where you can review configuration examples and supported arguments.

<details>
  <summary>Click to show details</summary>
  <img width="1044" height="538" alt="Terraform AWS Provider Documentation" src="https://github.com/user-attachments/assets/73190f6b-2105-432d-90c7-bc047aeff28d" />
  <br>
  <img width="436" height="403" alt="Terraform Provider Registry" src="https://github.com/user-attachments/assets/bb221670-931c-4fd5-8e8c-4576c6efa53f" />
</details>

---

### Step 3 – Initialize the Terraform Project

Once your **provider configuration** is complete, initialize Terraform by running the following command inside your project directory:

```bash
terraform.exe init
```

This command downloads all required provider plugins and prepares Terraform for execution.

✅ After initialization, Terraform is ready to deploy your defined AWS resources — starting with your VPC, Security Groups, and EC2 instance.

---

### Step 4 – Create EC2 Instance (ec2.tf)

Defines instance creation and configuration.

<details> <summary>Click to show details</summary> 

  ```
      resource "aws_instance" "amb-prod" {
      ami           = "ami-0ecb62995f68bb549"
      instance_type = "t3.micro"
      key_name      = "Terraform"
      user_data     = file("script.sh")
      subnet_id     = aws_subnet.public_1.id
      vpc_security_group_ids = [aws_security_group.allow_http_ssh.id]
    
      tags = {
        Name = "amb-prod"
      }
    }
  ```

</details>

---

### Step 5 – Configure Network (vpc.tf)

Creates the main VPC, subnet, internet gateway, and route table.

<details> <summary>Click to show details</summary> <img width="527" height="903" alt="VPC Terraform" src="https://github.com/user-attachments/assets/a0dcc689-5b4c-4ecc-ab26-2c10e1ed7b5e" /> </details>

---

### Step 6 – Create Security Group (security-group.tf)

Create a security group based on the Basic Usage example from the Terraform Registry.
When creating a virtual machine using Terraform, if no security group is specified, a default security group is automatically assigned to the instance.
To define a custom security group, you must first create a vpc.tf file to configure a Virtual Private Cloud (VPC) — specifying the IP range, enabling DNS resolution, and allowing hostname assignment.

- Use aws_vpc.main.id from vpc.tf
- Reuse the same security group name (allow_http_ssh) referenced in EC2

<details> <summary>Click to show details</summary> <img width="586" height="879" alt="Security Group Terraform" src="https://github.com/user-attachments/assets/2211a3bb-3ada-4d0d-8d31-62be3f67538b" /> </details>

---

### Step 7 – Create script (script.sh)

This step involves creating a startup script (script.sh) that will be automatically executed on the EC2 instance during initialization through the Terraform user_data parameter in main.tf.
The script typically includes system setup commands such as updating packages, installing dependencies, configuring services, or deploying application code.

By automating these actions at instance launch, script.sh ensures a consistent and ready-to-use environment without requiring manual configuration after provisioning.

<details> <summary>Click to show details</summary> <img width="768" height="463" alt="image" src="https://github.com/user-attachments/assets/2b19bf32-1df6-4dc0-bdc5-4849c764fef6" /> </details>


### Step 8 – Deploy the Infrastructure with Terraform

This step covers the **deployment phase**, where Terraform is executed to initialize the working directory, validate the configuration, and provision the infrastructure defined in your `.tf` files.

Using the **Terraform CLI commands** below ensures that all configurations are correctly loaded, dependencies are initialized, and the AWS resources are deployed according to your defined setup.



#### ⚙️ Execution Steps  

1. **Initialize Terraform**  
   Run the command below to download the required provider plugins and initialize your working directory:  
   ```bash
   terraform.exe init
   ```
2. Validate and Plan the Deployment
   Preview the execution plan and detect potential configuration errors:
   ```bash
   terraform.exe plan
   ```
3. Apply the Configuration
   Deploy and configure the infrastructure on AWS as defined in your Terraform files
   ```bash
   terraform.exe apply
   ``` 

</details>

---

## 🔌 Connecting to the EC2 Instance Using PuTTY

This section explains how to connect to your AWS EC2 instance using **PuTTY**, a popular SSH client for Windows.  
You’ll use the SSH key pair created earlier in [🔑 Creating SSH Key Pair](#-creating-ssh-key-pair) for secure authentication.

Before starting, ensure that:
- You have the `.ppk` key file downloaded from AWS
- **PuTTY**  are installed on your system


<details> <summary>Click to show details</summary> 

### Step 1 – Get the Public IPv4 Address of Your Instance

1. Go to the **AWS Management Console → EC2 → Instances**
2. Select your running instance
3. Copy the **Public IPv4 address** shown in the details panel  

You’ll use this IP to establish the SSH connection.

---

### Step 2 – Configure PuTTY 

1. Open **PuTTY**
2. In the **Host Name (or IP address)** field, enter:
   ```bash
   <your-public-ip>
   ```
   <details><summary>Click to show details</summary>  <img width="756" height="529" alt="image" src="https://github.com/user-attachments/assets/80baa25e-4959-4fa7-b49e-91a77c7c4298" /></details>
  
3. In the left sidebar, navigate to:
  ```
    Connection → SSH → Auth → Credentials
  ```

4. Click Browse and select your .ppk key file
   
   <details><summary>Click to show details</summary><img width="836" height="669" alt="image" src="https://github.com/user-attachments/assets/3085f7f9-fc0f-4159-962e-6a9f2c30abec" /></details>
   
### Step 3 – Start the SSH Session

1. Go back to the Session category

2. Click Open

3. When prompted, click Yes to trust the host key

4. Once the terminal connection is established, note that since the virtual machine was created using an Ubuntu image, the default user is "ubuntu".

    <details><summary>Click to show details</summary><img width="937" height="406" alt="image" src="https://github.com/user-attachments/assets/0d0ee7ca-d98f-4df0-8fee-599c38ea8ca7" /></details>

</details>

---

## 🧩 Microservices Overview

Microservices are a collection of small, independent, and autonomous services designed to make applications scalable and modular.  
Each service handles a specific functionality, allowing for independent scaling — for instance, if one service experiences high demand, only that microservice needs to be scaled.

By decomposing the application into smaller parts, teams can build and deploy components independently using different technologies.

**Docker** enables packaging each microservice and its dependencies into a container — a single logical unit.  
This ensures that the service runs consistently across different environments.

| Lifecycle Phase | Tool Used     |
|------------------|---------------|
| **Build**        | Docker        |
| **Deploy**       | Docker        |
| **Operate**      | Kubernetes    |
| **Monitor**      | AWS           |

In this guide, Docker will be used in both **build** (to generate the application image) and **deploy** (to run the container) stages.

<details>
  <summary>Click to show details</summary>

### Step 1 – Prerequisites Docker

- Docker installed and running on your machine (or CI runner).  
- Access to Docker Hub (or another image registry).  
- Permissions to execute Docker commands (`docker`).

### Step 2 – Concept Overview

1. Building the container from source code is typically the **developer’s responsibility** or part of the **pipeline automation process**.  
2. During CI/CD, the pipeline may **receive code from a repository** and automatically **build a new image version** — ensuring consistent deployments.  
3. Removing a **container** does **not** remove its **base image** — images must be deleted manually if needed.

---

### Step 3 – Pulling the Official Apache Image

To download the official Apache HTTPD image from Docker Hub:

```bash
docker pull httpd:latest
```

<details><summary>Click to show details</summary><img width="876" height="522" alt="image" src="https://github.com/user-attachments/assets/4a1cc4cd-f712-4fe8-9a8f-f934a2ca8176" /></details>


### Step 4 – Running an Apache Container

```bash
docker run -dti --name serv-web -p 80:80 httpd:latest
```

This command starts an Apache container on port 80.
When you access http://localhost in your browser, you should see the message “It works!” confirming that the container is running successfully.

Flag explanation:

- -d — Runs the container in detached mode (background).

- -t -i — Allocates a pseudo-TTY and keeps STDIN open (useful for debugging).

- --name serv-web — Assigns a name to the container.

- -p 80:80 — Maps port 80 of the host to port 80 inside the container.

Now, open your browser and visit http://localhost/.
You should see the default Apache page: “It works!”

---

### Step 5 – Default Directory Structure

The default document root for the official Apache image is:

```
/usr/local/apache2/htdocs
```

Always refer to the image documentation since the internal directory paths may differ between versions.

If you want to serve local files (for development), mount a volume:

```
docker run -d --name serv-web -p 80:80 -v /path/to/your/site:/usr/local/apache2/htdocs httpd:latest
```

---

### Step 6 – Stopping and Removing Containers

To stop the container:
```
docker stop serv-web
```

To remove it (forcefully if needed):
```
docker rm serv-web --force
```
Note: This command removes only the container — the downloaded image (httpd:latest) remains on the system.

---

### Step 7 – Listing and Removing Images

List existing images:
```
docker images
# or
docker image ls
```

Remove a specific image:
```
docker rmi httpd:latest
# or by image ID
docker image rm <IMAGE_ID>
```

</details>

---

## 🐳 Creating Custom Docker Images and Hosting in Docker Hub
This section demonstrates how to build and host a **custom Docker image** that encapsulates a web application (in this case, a site running on Apache).  
This image can later be used within automated **CI/CD pipelines** or deployed on remote servers such as AWS.

<details>
  <summary>Click to show details</summary>

### Step 1 – Clone the Website Repository

First, install **Git** and clone the website repository that will be containerized.

```bash
git clone https://github.com/denilsonbonatti/mundo-invertido
```

---

### Step 2 – Create the Dockerfile

Navigate to the root directory of the cloned project and create a Dockerfile.
This file defines the environment, dependencies, and configuration for the containerized application.

The Apache container serves static files from the /usr/local/apache2/htdocs/ directory, as indicated in the official Docker Hub documentation.

Example Dockerfile:

```
# Use the official Apache HTTP server image
FROM httpd:latest

WORKDIR /usr/local/apache2/htdocs/

# Copy website files into the Apache web directory
COPY . /usr/local/apache2/htdocs/

EXPOSE 80
```
<details><summary>Click to show details</summary><img width="955" height="274" alt="image" src="https://github.com/user-attachments/assets/c348d591-0893-4b62-b67c-33970d3e71e2" /></details>

---

### Step 3 – Build the Custom Image

Now, build the Docker image using the docker build command.

```
docker build -t my-apache2
```

However, since this image will be published on Docker Hub, replace my-apache2 with your Docker Hub username and a meaningful tag.

```
docker build -t lucasmargui/meusite-bootcamp-devops:1.0 .
```

<details><summary>Click to show details</summary><img width="482" height="310" alt="image" src="https://github.com/user-attachments/assets/2eedda0d-987d-4608-be44-46d55827c2fe" /></details>

<details><summary>Click to show details</summary><img width="942" height="572" alt="image" src="https://github.com/user-attachments/assets/31f8da39-3340-4c47-a74d-a3248914862c" /></details>

---

### Step 4 – Run a Container from the Custom Image

Once the image is built, run a container to test it locally.

```
docker run -dti --name meu-httpd -p 80:80 lucasmargui/meusite-bootcamp-devops:1.0
```

Check if the container is running successfully:

```
docker ps
```

<details><summary>Click to show details</summary><img width="952" height="81" alt="image" src="https://github.com/user-attachments/assets/b8bf445c-7220-404d-9f90-c96353f8bc34" /></details>


Now you can access your website locally by navigating to http://localhost in your browser.

---

### Step 5 – Push the Image to Docker Hub

To make your image publicly available, log in to Docker Hub and push it:

```
docker login
docker push lucasmargui/meusite-bootcamp-devops:1.0
```

This will allow others (and your pipelines) to pull and use the same image.

---

### Step 6 – Deploying the Image on Remote Servers

Once the image is hosted on Docker Hub, it can be deployed anywhere — including AWS EC2 instances or Kubernetes clusters — by simply running:

```
docker run -dti -p 80:80 lucasmargui/meusite-bootcamp-devops:1.0
```

</details>

---

## 🐳 Launching EC2 with Docker Image from Docker Hub

This section covers deploying an EC2 instance on AWS and running a Docker container using an image pulled from Docker Hub.

<details>
  <summary>Click to show details</summary>

### Step 1 – Prepare the Infrastructure with Terraform

Since we don’t yet have a virtual machine in the cloud, we will use **Terraform** to:
- Provision a new **Ubuntu** EC2 instance on AWS.  
- Automatically update and configure the machine.  
- Install **Docker** and deploy our containerized application.

After building the Docker image and publishing it to Docker Hub, update your script.sh file to reference the image’s repository path.
This ensures that when the virtual machine is launched, the script automatically pulls and runs the correct Docker image from Docker Hub.

<details><summary>Click to show details</summary><img width="940" height="307" alt="image" src="https://github.com/user-attachments/assets/c7285748-ac85-4943-a867-9d42c06b489b" /></details>


---

### Step 2 – Apply Terraform Configuration


Once your Terraform configuration files are ready (`main.tf`, `provider.tf`, etc.), execute the following commands:

```bash
terraform plan
terraform apply
```

These commands will:

- Create the defined infrastructure on AWS.
- Deploy your Ubuntu instance with Docker automatically installed and configured.

---

### Step 3 – Connect to the Server Using PuTTY

After the instance is created, use PuTTY to connect to your AWS EC2 instance.

- Open PuTTY.
- Enter the Public IPv4 Address of your EC2 instance.
- Load your private key (.ppk) to authenticate.
- Connect using the ubuntu user.

Once connected, you will see the terminal prompt for the Ubuntu user.

---

### Step 4 – Verify Docker Installation

Run the following command to confirm Docker is installed:

```
docker --version
```

---

### Step 5 – Check Downloaded Docker Images

To ensure the Docker image has been pulled from Docker Hub, run:

```
sudo docker images
```

---

### Step 6 – Confirm the Running Container

Finally, check if the container is up and running:

```
sudo docker ps
```

</details>

---

## ☁️ Create GitLab directory/repository

GitLab is an all-in-one DevOps platform offering:  

- **Version Control:** Git-based versioning system.  
- **Continuous Integration (CI):** Automates build, test, and deployment of code on every change.  
- **Continuous Delivery (CD):** Automates deployment to testing, staging, and production environments reliably and consistently.  
- **Issue Tracking:** Manage issues and tasks for progress monitoring.  
- **Team Collaboration:** Unified platform for development, testing, and delivery, improving efficiency and reducing errors.  

Our goal is to publish code, build containers, and deploy them to a Kubernetes cluster automatically.


<details>
  <summary>Click to show details</summary>

### Step 1 – Create GitLab Account

1. Visit [GitLab](https://gitlab.com/)  
2. Sign up for a free account or log in if you already have one.

---

### Step 2 – Create a New Project

1. Click **New Project**  
2. Select **Blank Project**  
3. Set the **project name** and click **Create Project**  
4. After creation, GitLab will display instructions to initialize a local repository.

<details><summary>Click to show details</summary> <img width="814" height="678" alt="image" src="https://github.com/user-attachments/assets/28a3c6f9-cca0-44c3-8896-0a0c270d5e46" /> </details>

---

### Step 3 – Initialize Local Repository

1. Create a local directory for your project:

```bash
mkdir bootcampt-devops-project-1
cd bootcampt-devops-project-1
```
<details><summary>Click to show details</summary> <img width="948" height="309" alt="image" src="https://github.com/user-attachments/assets/3836e5e7-e6b1-45f1-a44d-78824c3685cf" /> </details>

2. Initialize Git:

```
git init --initial-branch=main --object-format=sha1
```

3. Configure local user information:

```
git config --local user.name "Your Name"
git config --local user.email "your.email@example.com"
```

---

### Step 4 – Link Repository and Push Code

1. Add the GitLab remote repository:

```
git remote add origin git@gitlab.com:lucasmargui/bootcampt-devops-project-1.git
```

2. Stage files for commit:

```
git add .
```

3. Make the initial commit:

```
git commit -m "Initial commit"
```

4. Push the code to GitLab:

```
git push --set-upstream origin main
```

---


---

### Step 5 – Provision EC2 Instance with Terraform

1. Reuse the existing bootcampt-devops-project-1 to configure a terraform and create a new EC2 instance for your GitLab Runner.

  <details><summary>Click to show details</summary> <img width="754" height="511" alt="image" src="https://github.com/user-attachments/assets/83a6fb63-c1eb-47bf-a60f-8eda49454b82" /></details>
   
3. Initialize Terraform:
   
```bash
terraform init
````


3. Apply the Terraform plan to create the EC2 instance:

```bash
terraform apply
```

4. After the instance is created, connect via SSH using PuTTY:

- Username: ubuntu
- Private Key: The one created previously (Terraform.ppk)

<details><summary>Click to show details</summary> <img width="775" height="379" alt="image" src="https://github.com/user-attachments/assets/9c42edf2-5c80-4b0d-9b3f-565c207bf74a" /></details>

---

### Step 6 – Install GitLab Runner

1. SSH into your EC2 instance.
2. Install GitLab Runner

<details><summary>Click to show details</summary> <img width="768" height="308" alt="image" src="https://github.com/user-attachments/assets/1acc95dd-99d3-4749-8c7d-088f2dcdefde" /> </details>

<details><summary>Click to show details</summary>  <img width="960" height="189" alt="image" src="https://github.com/user-attachments/assets/034e4406-3940-49d5-9200-11842f93970f" /> </details>

<details><summary>Click to show details</summary> <img width="959" height="111" alt="image" src="https://github.com/user-attachments/assets/513d0645-8315-4808-bac8-13191b6a0467" /> </details>


```
sudo apt-get update
curl -L "https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh" | sudo bash
sudo apt-get install gitlab-runner
```

3. Confirm installation by pressing Enter when prompted.
Note: You can also pre-install GitLab Runner in the Terraform configuration.

---

### Step 7 – Register GitLab Runner

1. In GitLab, navigate to your project: Settings > CI/CD > Runners > New Project Runner
   
  <details><summary>Click to show details</summary> <img width="957" height="363" alt="image" src="https://github.com/user-attachments/assets/84ae904a-cf26-41d0-86ce-d25023ac0bf9" /> </details>

2. Copy the registration token from the three dots menu.

  <details><summary>Click to show details</summary> <img width="907" height="342" alt="image" src="https://github.com/user-attachments/assets/6c162ef5-1eee-4008-be48-b583e7127b18" /> </details>

3. On your EC2 instance, register the runner:

```
sudo gitlab-runner register
```

- GitLab instance URL: https://gitlab.com/
- Registration token: Copy from GitLab
- Runner tags: shell (or any tags you prefer)

<details><summary>Click to show details</summary> <img width="805" height="233" alt="image" src="https://github.com/user-attachments/assets/3e1db82b-2ad6-4c99-904c-6e5341a5f913" /> </details>

4. Your runner is now registered and ready to receive jobs

<details><summary>Click to show details</summary> <img width="949" height="423" alt="image" src="https://github.com/user-attachments/assets/28e65778-39f4-43fe-a5ce-b6bcc46228fb" /> </details>

---

### Step 8 – Configure GitLab Runner User

1. GitLab Runner creates a user called gitlab-runner. Verify in:

```
cat /etc/passwd | grep gitlab-runner
```

2. Add the runner to the Docker group to allow building and running containers:

```
sudo usermod -aG docker gitlab-runner
```

---

### Step 9 – Docker Hub Authentication

1. Switch to root user (if needed, set a root password first):

```
sudo passwd root
su
```

2. Set a password for gitlab-runner:

```
passwd gitlab-runner
```

3. Switch to the gitlab-runner user:

```
su gitlab-runner
```

4. Log in to Docker Hub (or company Docker registry):

```
docker login -u "your-username"
```

<details><summary>Click to show details</summary> <img width="945" height="302" alt="image" src="https://github.com/user-attachments/assets/6f616e78-4542-4e26-aa5f-d988dfb565b9" /> </details>

</details>

---

## 🐳 CI/CD Pipeline – Containerized Application

<details>
  <summary>Click to show details</summary>

### Step 1 – Configure .gitignore

- Create a `.gitignore` file at the root of the repository.  
- Add files and directories that should not be versioned, such as Terraform state files or logs.
  
```
.terraform*
terraform*
```

---

### Step 2 – Create Dockerfile

Inside your application directory, create a Dockerfile.

This file will be used to build the container image.

Minimal example:

```bash
FROM httpd:latest

WORKDIR /usr/local/apache2/htdocs/

COPY * /usr/local/apache2/htdocs/

EXPOSE 80
```

<details><summary>Click to show details</summary> <img width="945" height="217" alt="image" src="https://github.com/user-attachments/assets/8def7026-6029-4e43-a254-1626aae074e9" /> </details>

---

### Step 3 – Configure GitLab Pipeline

Create a .gitlab-ci.yml file at the root of the repository.

Divide the pipeline into stages (main sections) and jobs (tasks inside stages).

```
stages:
  - build
  - deploy
variables:
  GLOBAL_VAR: "2.0"
```

<details><summary>Click to show details</summary> <img width="241" height="126" alt="image" src="https://github.com/user-attachments/assets/ae4d1dea-efd2-473d-8416-ca22c9eb2e26" /> </details>

---

### Step 4 – Build Docker Image

- Job to build and push the Docker image:

```
criar_imagens:
  stage: build
  tags:
    - aws
  script:
  - docker build -t lucasmargui/app-bootcamp-devops:$GLOBAL_VAR app/.
  - docker push lucasmargui/app-bootcamp-devops:$GLOBAL_VAR
```

1. Stage: build
- This job is part of the build stage in the CI/CD pipeline.

2. Tags: aws
- Specifies that this job should run on runners tagged with aws (created in e2c).

3. Script:

- docker build -t lucasmargui/app-bootcamp-devops:$GLOBAL_VAR app/
Builds a Docker image using the Dockerfile located in the app/ directory.
The image name will be lucasmargui/app-bootcamp-devops and the tag will be set using the environment variable $GLOBAL_VAR.

- docker push lucasmargui/app-bootcamp-devops:$GLOBAL_VAR
Pushes the built Docker image to the remote Docker repository.


<details><summary>Click to show details</summary> <img width="582" height="155" alt="image" src="https://github.com/user-attachments/assets/20de9ab6-8057-464a-b3a0-4c957d7a53a2" /> </details>

- Add and commit the new files:

```
git add .
git commit -m "Create CI/CD Pipeline"
git push --set-upstream origin main
```

---

### Step 5 – Deploy Container

- Job to run the container on the production server:
  
```
executar_imagens:
  stage: deploy
  needs:
    - criar_imagens
  tags:
    - aws
  before_script:
  - docker rm $(docker ps -a -q) --force
  script:
  - docker run -dti --name web-server -p 80:80 lucasmargui/app-bootcamp-devops:$GLOBAL_VAR
  after_script:
  - docker system prune --force
```

1. Stage: deploy
- This job runs in the deploy stage of the CI/CD pipeline.

2. Dependencies: needs: criar_imagens
- Ensures this job only runs after the criar_imagens job has successfully completed.

3. Tags: aws
- Specifies that this job should run on runners tagged with aws.

4. Before Script:
```
docker rm $(docker ps -a -q) --force
```
- Removes all existing Docker containers to ensure a clean environment before starting the new container.

5. Script:
```
docker run -dti --name web-server -p 80:80 lucasmargui/app-bootcamp-devops:$GLOBAL_VAR
```
- Runs the Docker image in a detached and interactive terminal mode.
- Names the container web-server
- Maps port 80 on the host to port 80 in the container
- Uses the image lucasmargui/app-bootcamp-devops with the tag $GLOBAL_VAR.

6. After Script:
```
docker system prune --force
```
- Cleans up unused Docker objects to free disk space and keep the environment tidy.

<details><summary>Click to show details</summary> <img width="712" height="284" alt="image" src="https://github.com/user-attachments/assets/74a2dca4-b9f1-4bed-a21a-3f0988ef5e4a" /> </details>


- Add, commit, and push:

```
git add .
git commit -m "Deploy container"
git push
```

- Verify in GitLab that the container is running successfully.

---

### Step 6 – Update Application Version

To update the application (e.g., version 2.0 → 3.0):

```
variables:
  GLOBAL_VAR: "3.0"
```


<details><summary>Click to show details</summary> <img width="524" height="443" alt="image" src="https://github.com/user-attachments/assets/cc405bed-a7a6-4095-b8d3-0f7281f91d96" /> </details>

</details>

---

