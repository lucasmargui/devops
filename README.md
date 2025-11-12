# DevOps

DevOps professional focused on bridging development and operations to deliver scalable, reliable, and automated solutions. Experienced in CI/CD, Infrastructure as Code, cloud environments, containerization, monitoring, and microservices. Committed to collaboration, continuous improvement, and accelerating software delivery with quality and efficiency.

- Continuous Integration (CI): Automated process of integrating code changes frequently into a shared repository with immediate validation through testing.
  <details>
    <summary>Click to show details about </summary>
    
    <img width="784" height="792" alt="image" src="https://github.com/user-attachments/assets/bd54ec2c-7ce2-4c55-8e54-e63c3805c0f4" />

  </details>

- Continuous Delivery/Deployment (CD) – Ensuring software is always in a deployable state and automating releases to production environments safely and efficiently.

  <details>
    <summary>Click to show details about </summary>
    
    <img width="1358" height="586" alt="image" src="https://github.com/user-attachments/assets/6d985365-aa09-4bc9-b863-16078a7e400c" />

  </details>

- Microservices Architecture – Designing applications as small, independent, and loosely coupled services to improve scalability and maintainability.

  <details>
    <summary>Click to show details about </summary>

  <img width="1143" height="742" alt="image" src="https://github.com/user-attachments/assets/49226623-610d-4e18-b117-f04c99f16f6c" />

  </details>

- Infrastructure as Code (IaC) – Managing and provisioning infrastructure using code and automation rather than manual processes.
  
  <details>
      <summary>Click to show details about </summary>
    <img width="1338" height="751" alt="image" src="https://github.com/user-attachments/assets/126f4250-3a96-4897-808b-0778f4b8849e" />
  </details>


- Monitoring and Logging – Collecting and analyzing application and infrastructure data to detect issues, ensure performance, and support proactive incident response.

- Communication and Collaboration – Promoting cross-team alignment and transparency through shared responsibilities, tools, and workflows.


## Infrastructure as Code (IaC) - Public Cloud

### Creating an instance directly in AWS

#### 1) Prerequisites

- Have an AWS account created and verified (credit card / phone).
- User with EC2/IAM permissions (or root user for learning — not for production).
- For Windows: download PuTTY (putty.exe) and PuTTYgen.
- For Linux/macOS: have terminal access with ssh installed.

#### 2) Create ec2
  <details>
    <summary>Click to show details about </summary>
    <img width="1053" height="604" alt="image" src="https://github.com/user-attachments/assets/42738fa8-1f2a-4765-ac32-a5142ea54608" />
  </details>

#### 3) Create / Manage an SSH Key Pair

You can either create the key in the AWS Console (generates .ppk for putty) or create it locally (ssh-keygen) and import the public key into AWS.
Go to AWS Console → EC2 → “Key pairs” → “Create key pair”.

  <details>
    <summary>Click to show details about </summary>
    <img width="1067" height="319" alt="image" src="https://github.com/user-attachments/assets/dacaf6b5-8271-4fc4-874f-743678d677e1" />
  </details>
  
#### 4) Create a Security Group (Firewall Rules)

Create a Security Group that allows:

- SSH (port 22) — ideally restricted to your IP (e.g., 203.0.113.25/32).
- HTTP (port 80) — open to everyone (0.0.0.0/0) for public web access.
  
  <details>
    <summary>Click to show details about </summary>
    <img width="1080" height="455" alt="image" src="https://github.com/user-attachments/assets/34a39759-232d-4f39-b00a-0950574281e3" />
  </details>

#### 5) Executing script

Next, I will access the advanced settings, and at the bottom, there will be an option to attach the created script (script.sh), which is responsible for updating the virtual machine, installing the Apache server, and deploying the application.

  <details>
    <summary>Click to show details about </summary>
    <img width="1042" height="724" alt="image" src="https://github.com/user-attachments/assets/4a4aa97b-4375-481e-bde7-ed0335215a24" />
  </details>


### Configuring AWS CLI Access Using IAM

#### Step 1 – Install AWS Cli

In this step, you will install and configure the AWS Command Line Interface (AWS CLI), a unified tool that allows you to manage your AWS services directly from the command line.

  <details>
    <summary>Click to show details about </summary>
      <img width="1130" height="622" alt="image" src="https://github.com/user-attachments/assets/43bb56e1-bf6b-40fe-bd60-e54fa4cec711" />
  </details>

#### Step 2 – Creating a User Group (IAM Group)

- Access the IAM (Identity and Access Management) service in the AWS Console.
    <details>
      <summary>Click to show details about </summary>
      <img width="1047" height="225" alt="image" src="https://github.com/user-attachments/assets/92650f80-33c6-4d39-8235-16ae47407761" />
    </details>
- In the sidebar, select Groups and click Create Group.
- Name the group cli-users.
   <details>
      <summary>Click to show details about </summary>
      <img width="1062" height="252" alt="image" src="https://github.com/user-attachments/assets/2fad42b5-2c87-4ba2-b765-ac3d529f1ea1" />
    </details>

- Attach the AdministratorAccess policy to the group to grant full permissions (recommended only for development or testing environments).
- Click Create Group to finalize.

#### Step 3 – Creating an IAM User

- Still within IAM, navigate to Users and click Add User.
- Set the username as lucasmarguaws.
    <details>
      <summary>Click to show details about </summary>
      <img width="728" height="140" alt="image" src="https://github.com/user-attachments/assets/ae621945-2f48-447f-9837-8ec394ad1b0f" />
    </details>
- Select the Access type: Programmatic access (CLI access) option.
- Add the user to the previously created cli-users group.
    <details>
      <summary>Click to show details about </summary>
      <img width="1037" height="540" alt="image" src="https://github.com/user-attachments/assets/4e0ecf82-1d45-43f4-b0b5-5c740d6c08f8" />
    </details>
- Click Create User to complete the process.

#### Step 4 – Generating Access Keys

- After the user is created, click on lucasmarguaws to view its details.
- Open the Security credentials tab.
- Click Create access key and choose the usage type Command Line Interface (CLI).
  <details>
    <summary>Click to show details about </summary>
    <img width="1072" height="201" alt="image" src="https://github.com/user-attachments/assets/19d9bdb2-5f9f-41e0-a718-2936f005f8e0" />
  </details>
- Copy and securely store the Access Key ID and Secret Access Key, as they will be required for CLI authentication.
  <details>
    <summary>Click to show details about </summary>
    <img width="1036" height="185" alt="image" src="https://github.com/user-attachments/assets/002ec936-e699-486f-8693-9a9b4d515215" />
  </details>

#### Step 5 – Configuring the AWS CLI

- Open your Command Prompt (CMD) or terminal.
- Run the following command: 

```
aws configure
```

- Enter the credentials you obtained earlier:

```
AWS Access Key ID [None]: <your-access-key-id>
AWS Secret Access Key [None]: <your-secret-access-key>
Default region name [None]: us-east-1
Default output format [None]: json
```
  <details>
    <summary>Click to show details about </summary>
    <img width="996" height="142" alt="image" src="https://github.com/user-attachments/assets/407e723f-8e12-4aae-8f38-4a7d4367a333" />
  </details>


- Once completed, your AWS CLI will be authenticated and ready to execute commands or apply Terraform scripts securely and automatically.

### Creating key pair ssh

#### 1) Open the AWS Management Console and go to the EC2 service.

#### 2) In the left navigation pane, click Key Pairs under Network & Security.

#### 3) Click Create key pair.

#### 4) In the Name field, enter: Terraform.

#### 5) Under File format, select .ppk for Putty .

#### 6) Click Create key pair.

#### 7) The browser will automatically download the Terraform.ppk file — save it in a secure location (e.g., C:\Users\<YourUser>\.ssh\Terraform.ppk).

### Creating an instance with Terraform

#### 1) Download Terraform and configure the required environment variables to enable the execution of the terraform.exe file.

#### 2) Configure the Terraform Provider

Before deploying any infrastructure, it is necessary to configure the Terraform provider, which defines the cloud platform or service Terraform will interact with.
  
- Navigate to the directory where your Terraform project is located.
- Create a configuration file named main.tf (or another name of your choice).
- Define the provider you intend to use — for example, AWS. Terraform providers can be found on the Terraform Registry, which offers multiple options depending on your infrastructure needs.
  <details>
    <summary>Click to show details about </summary>
    <img width="1044" height="538" alt="image" src="https://github.com/user-attachments/assets/73190f6b-2105-432d-90c7-bc047aeff28d" />
    <img width="436" height="403" alt="image" src="https://github.com/user-attachments/assets/bb221670-931c-4fd5-8e8c-4576c6efa53f" />
  </details>

- Once the provider configuration is defined, initialize Terraform by running the following command in your project directory:
  ```
    terraform.exe init
  ```


  
 #### 3)  – Create the AWS EC2 Instance Configuration

Now that the provider is set up, the next step is to define the Terraform code that will create the EC2 instance on AWS.

- Go to the Terraform Registry
- Search for aws_instance under the Resources section.
- Copy the example configuration snippet and adapt it for your project.
  <details>
    <summary>Click to show details about </summary>
    <img width="1056" height="451" alt="image" src="https://github.com/user-attachments/assets/23afc317-9657-4763-b341-eeaef4aaa621" />
    <img width="668" height="445" alt="image" src="https://github.com/user-attachments/assets/655a2c37-0975-460c-8f4f-c1ee98246243" />

    ```
      resource "aws_instance" "amb-prod" { ... }
    ```
    - resource → declares that Terraform will create or manage a resource.
    - "aws_instance" → defines the type of resource (an EC2 virtual machine).
    - "amb-prod" → the internal Terraform name (used for referencing this resource in other files).

    ```
      ami = "ami-0ecb62995f68bb549"
    ```
    <img width="917" height="271" alt="image" src="https://github.com/user-attachments/assets/d4d1d3d3-adb1-4fe3-9247-020c120d350e" />
    - AMI (Amazon Machine Image) → the base operating system image used to launch the EC2 instance.This ID specifies which OS and preconfigured environment will be used (e.g., Ubuntu, Amazon Linux).

    ```
      instance_type = "t3.micro"
    ```
    - Instance type → determines the hardware configuration (CPU, memory, network performance). t3.micro is a small, cost-effective instance type — often eligible for the AWS Free Tier.

    ```
      key_name = "Terraform"
    ```
     - SSH Key Pair → name of the key used for secure remote SSH access to the instance.You must have the corresponding .pem file to connect to this instance.
     - [Creating key pair ssh](#creating-key-pair-ssh)
       
    ```
      user_data = file("script.sh")
    ```
    - User Data → a startup script that runs automatically the first time the instance boots.
      - Typically used to:
      - Update the OS packages;
      - Install software (e.g., Apache, Docker);
      - Deploy or configure an application.

    ```
      subnet_id = aws_subnet.public_1.id
    ```
    - Places the instance inside a specific VPC subnet. aws_subnet.public_1.id references a subnet resource created elsewhere in Terraform. This determines where in the network (e.g., public or private zone) the instance will reside.

    ```
      vpc_security_group_ids = [
          aws_security_group.allow_http_ssh.id
        ]
    ```
    - Security Groups → act as virtual firewalls that control inbound and outbound traffic.
      - This line associates the instance with a predefined Security Group (allow_http_ssh), which likely allows:
      - Port 22 for SSH access;
      - Port 80 for HTTP traffic.

    ```
      tags = {
        Name = "amb-prod"
      }
    ```
    - Tags → key–value metadata assigned to AWS resources. The Name tag is commonly used for display in the AWS Management Console.
    
    
  </details>










