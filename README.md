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


### Creating an instance with Terraform

#### 1) Download Terraform and configure the required environment variables to enable the execution of the terraform.exe file.

#### 2) Create a dedicated directory for the Terraform project.









