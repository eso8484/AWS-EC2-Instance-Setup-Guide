---
# **AWS EC2 Instance Setup Guide**

This guide will walk you through setting up an **AWS EC2 instance** to run a CLI-based **crypto node** for free using the AWS Free Tier.
---

## **1. Create an AWS Account**
1. Go to [AWS Free Tier](https://aws.amazon.com/free/) and sign up.
2. Provide your email, password, and billing details (Use Grey Card or Geegpay or Bybit Card, Zenith Card worked for some persons).
3. Verify your phone number and choose **Basic Support (Free)**.
---
## **2. Launch an EC2 Instance**
1. **Go to AWS EC2 Console**: [AWS EC2 Dashboard](https://console.aws.amazon.com/ec2)
2. Click **"Launch Instance"**.
3. **Select an OS**: Choose **Ubuntu 22.04 LTS** (or Amazon Linux 2 for lightweight performance).
4. **Choose Instance Type**: Select **t2.micro (Free Tier Eligible)**.
5. **Configure Security Group**:
   - Allow **SSH (port 22, My IP only)**..
6. **Create Key Pair**:
   - Choose **ED25519** (recommended for better security).
   - Download the `.pem` file (needed for SSH access).
7. Click **Launch Instance** and wait for it to start.
---
## **3. Connect to Your EC2 Instance**
1. Open a terminal (Linux/macOS) or use **PuTTY** (Windows).
2. Run the following command:
   ```bash
   chmod 400 your-key.pem
   ssh -i your-key.pem ubuntu@your-instance-ip
   ```
   Replace `your-instance-ip` with the **Public IPv4** of your instance and replace `your-key.pem` with the actual name you gave your `.pem` file
 
## Install Dependancies for Smooth Experince
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y build-essential clang make gcc pkg-config libssl-dev libcrypto++-dev libc6-dev zlib1g-dev curl wget tmux screen
```
---
## Detach & Keep Sessions Running (Optional)
### Using **tmux**:
- Start tmux: `tmux`
- Detach session: `Ctrl + b`, then `d`
- Reattach session: `tmux attach`

### Using **screen**:
- Start screen: `screen`
- Detach: `Ctrl + a`, then `d`
- Reattach: `screen -r`

---
## Some Node project may require Rust, You may install Rust and Cargo ahead for such Projects
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
```
---
## **Your setup should look like this**

<div align = "center">

<img src = "Instance EC2.png" alt = "EC2 Instance Launch page">
<img src = "EC2.png" alt = "EC2 Config Screenshot">

</div>

---

## **Conclusion**
You have successfully set up an **AWS EC2 instance**.
Let me know if you need further assistance by connecting with me via the links in the icons below! 🚀

---
## **🌐 Connect With Me**

[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?style=for-the-badge&logo=Twitter&logoColor=white)](https://twitter.com/oche_21)
[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/eso8484)
[![Direct Contact](https://img.shields.io/badge/Direct_Contact-%23009688.svg?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/eso8484)
