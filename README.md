# 🛡️ Honeypot Deployment on Azure (T-Pot Community Edition)

## What is the purpose of a honeypot?
A honeypot is a deliberately vulnerable or exposed machine or service, with the goal of:
 - Attracting attackers (both humans and bots)
 - Monitoring techniques, tools, and behaviors
 - Collecting logs and indicators of compromise (IoCs)
 - Gaining threat intelligence
Testing responses and defenses without risking real systems.

## Create and Configure Azure Virtual Machine

1. Connect to your **Microsoft Azure** account.
2. Start a new **Virtual Machine**:
    - OS: **Ubuntu (latest version)**
    - Disk: **256 GB**
    - RAM: **16 GB minimum**
3. Choose **“Password”** as the authentication type.
4. Create a **new Resource Group**.
5. Start the VM.
6. Add a new **Inbound Port Rule**:
    - Allow traffic on **port 6435** (for the T-Pot web UI).

---

## Access and Prepare the VM

1. Connect to the VM using **SSH**:
    - You can use **PuTTY** on Windows or terminal on Linux/macOS.
2. Update the system:
    
    ```bash
    sudo apt update && sudo apt upgrade -y
    ```
    
3. Install Git:
    
    ```bash
    sudo apt install git -y
    ```
    
4. Now, clone the T-Pot repository and navigate into the directory:

```jsx
git clone https://github.com/telekom-security/tpotce
cd tpotce
```

1. Start the installation script: 

```jsx
sudo ./install.sh
```

When prompted, choose the letter **H** to install the **Hive** configuration of T-Pot.

During installation, you'll be asked to set a username and password for accessing the T-Pot web interface. After the installation is complete, reboot the VM.

To access your honeypot dashboard, open a browser and navigate to:

```jsx
https://<your_vm_public_ip>:64297 
```
## T-Pot First View 
<img width="1911" height="1072" alt="Screenshot 2025-08-05 232657" src="https://github.com/user-attachments/assets/818d37fa-60b5-4d4e-9ad4-81b0d01ff155" />
You can use T-pot for a lot of purposes like monitoring, scan the attackers and understand what kind of attacks is happening right now.

## Attack Map
Here you can see all the attackers, location and types in real time.
<img width="1914" height="884" alt="Screenshot 2025-08-05 232753" src="https://github.com/user-attachments/assets/81e858a9-9c6c-4b35-aa47-5e8de5a3d1a4" />

## Kibana
Here you have dashboards with all the informations about the attackers. 
<img width="1893" height="1060" alt="Screenshot 2025-08-05 233939" src="https://github.com/user-attachments/assets/c926150a-78c8-4497-9cb3-6ce62f81afb3" />

Also you can see informations like the CVEs, IPs and AS/N
<img width="1890" height="667" alt="Screenshot 2025-08-05 234024" src="https://github.com/user-attachments/assets/c51081c6-1025-467f-b5b6-8fd7d08fbfc1" />

You have a lot of different dashboards available for you and thats awesome. I recommend to you build Honeypots will make your life a lot of more easy and you will be able to explore the most commons attacks and learn how to protect.
<img width="1906" height="862" alt="Screenshot 2025-08-05 234139" src="https://github.com/user-attachments/assets/445b9ffa-6d27-4fa1-99ae-696b0fe08cc7" />

## Microsoft Azure Cloud
Here you see how your VMs looks like in Azure Cloud and the cost of this machines for this honeypot is around $80 mo. 
<img width="1642" height="874" alt="Screenshot 2025-08-05 232905" src="https://github.com/user-attachments/assets/b5a31787-4164-43a9-9d3e-68d96eb9ad0f" />
