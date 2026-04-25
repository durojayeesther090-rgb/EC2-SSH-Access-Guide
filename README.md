# EC2-SSH-Access-Guide
This document shows how to connect to an Ubuntu-based AWS EC2 instance using SSH.

Overview

Secure Shell (SSH) allows you to remotely access and manage your EC2 instance from your local machine.



 EC2 SSH Access Guide

This document shows how to connect to an Ubuntu-based AWS EC2 instance using SSH.

---

Overview

Secure Shell (SSH) allows you to remotely access and manage your EC2 instance from your local machine.

---

Requirements

Before you begin, ensure you have:

* An active EC2 instance running
* A valid private key file (`.pem`)
* The public IPv4 address of your instance
* An SSH client (Linux, macOS, or Windows with Git Bash / WSL)

---

## 🔐 Connect to Your Instance

Run the following command in your terminal:

```bash
ssh -i your-key.pem ubuntu@34.224.79.171
```

---

Command Breakdown

| Component         | Description                               |
| ----------------- | ----------------------------------------- |
| `ssh`             | Secure Shell command                      |
| `-i your-key.pem` | Path to your private key file             |
| `ubuntu`          | Default username for Ubuntu EC2 instances |
| `34.224.79.171`   | Public IP address of the EC2 instance     |

---

Important Steps

 Set File Permissions

Ensure your `.pem` file is secure:

```bash
chmod 400 your-key.pem
```

---

 First-Time Connection

When connecting for the first time, you may see:

```
Are you sure you want to continue connecting (yes/no)?
```

Type:

```
yes
```

---

 Expected Output

After successful login, your terminal should display:

```
ubuntu@ip-xxx-xxx-xxx-xxx:~$
```

---

Troubleshooting

❌ Permission denied (publickey)

* Verify you're using the correct `.pem` file
* Ensure permissions are set correctly (`chmod 400`)

 ❌ Connection timed out

* Check if your instance is running
* Confirm Security Group allows **SSH (port 22)**

---

 Next Steps

Once connected, you can:

* Install web servers like Nginx
* Deploy applications
* Configure your environment

---

 Author

Esther Durojaye
DevOps | Cloud | Cybersecurity Enthusiast



If you want, I can combine this with your **Nginx setup + EC2 provisioning** into a full portfolio-grade README that stands out on GitHub.
