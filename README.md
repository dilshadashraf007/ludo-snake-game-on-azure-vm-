🎮 Snake & Ludo Game Deployment on Azure Virtual Machine

This project demonstrates how to deploy a simple Snake & Ludo HTML game on a cloud server using Azure Virtual Machine and Apache Web Server.
The application is hosted on a Linux VM and accessed through a public IP using HTTP.

---

☁️ Project Overview

This project shows how to:

- Create an Azure Free Trial Account
- Launch a Linux Virtual Machine (Ubuntu)
- Configure Network Security Group (NSG)
- Connect to the VM using SSH with PEM key
- Install and configure Apache Web Server
- Deploy a Snake & Ludo HTML game
- Access the application via Public IP

---

🏗 Architecture

User Browser → Public IP → Azure Network Security Group → Azure Virtual Machine (Ubuntu) → Apache Web Server → Snake & Ludo Game

---

⚙️ Technologies Used

- Microsoft Azure
- Linux (Ubuntu)
- Apache Web Server
- HTML / CSS / JavaScript
- SSH
- Network Security Groups (NSG)

---

🚀 Step 1: Create Azure Free Trial Account

Create a free account and get credits for learning cloud services.

Azure Portal:
https://portal.azure.com

---

🖥 Step 2: Create Azure Virtual Machine

1. Go to Virtual Machines
2. Click Create Virtual Machine
3. Choose:
   - OS: Ubuntu
   - Size: Basic VM
4. Create SSH Key Pair
5. Download .pem key

---

🔐 Step 3: Configure Network Security Group (NSG)

Allow inbound traffic for:

Port| Protocol| Purpose
22| SSH| Remote login
80| HTTP| Web server

Steps:

1. Open Network Security Group
2. Click Inbound Rules
3. Add rules for 22 and 80

---

🔑 Step 4: Connect to VM using SSH

Run this command in terminal:

ssh -i mykey.pem azureuser@PUBLIC-IP

Example:

ssh -i mykey.pem azureuser@20.193.10.10

---

🌐 Step 5: Install Apache Web Server

Update system:

sudo apt update

Install Apache:

sudo apt install apache2 -y

Start Apache:

sudo systemctl start apache2

Enable Apache:

sudo systemctl enable apache2

Check Apache status:

sudo systemctl status apache2

---

📂 Step 6: Deploy Snake & Ludo Game

Navigate to Apache directory:

cd /var/www/html

Remove default page:

sudo rm index.html

Create new HTML file:

sudo nano index.html

Paste your Snake & Ludo game HTML code and save.

---

🌍 Step 7: Access Application

Open browser:

http://PUBLIC-IP

Example:

http://20.193.10.10

Your Snake & Ludo Game will be live on Azure VM.

---

📸 Architecture Diagram

Add the architecture image here in your repository:

/architecture.png

---

🎯 Learning Outcomes

This project helped me learn:

- Cloud infrastructure deployment
- Virtual Machine management
- Network Security configuration
- Web server installation
- Deploying web applications on cloud

---

👨‍💻 Author

MD Dilshad Ashraf

Learning Cloud Computing | DevOps | Kubernetes

---

⭐ Future Improvements

- Deploy using Docker container
- Add CI/CD pipeline
- Host on Kubernetes
- Add multiplayer game support

---

📌 GitHub Repository Structure

snake-ludo-azure-deployment
│
├── index.html
├── README.md
├── architecture.png
└── game-files

---

🚀 If you like this project

Give it a ⭐ on GitHub and connect with me on LinkedIn.
