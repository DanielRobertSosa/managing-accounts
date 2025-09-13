# 🛡️ Group Policy & Managing Accounts (Unlocking/Resetting)

<p align="center">
<img src="https://i.imgur.com/2ik4QEl.png" height="80%" width="80%" alt="Active Directory Group Policy"/>
</p>

<h1>🔑 Group Policy – Account Management and Troubleshooting</h1>
This lab demonstrates how to configure account lockout policies, manage Active Directory user accounts, and analyze security logs in a Windows Server domain environment. These are common IT support tasks and a foundational skillset for helpdesk, system administration, and cybersecurity operations.<br />

---

<h2>🌐 Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines for lab setup)
- Active Directory Domain Services (AD DS)
- Group Policy Management Console (GPMC)
- Windows Event Viewer (Log Observation)

---

<h2>💻 Operating Systems Used</h2>

- Windows Server 2019 (Domain Controller: DC-1)
- Windows 10 Pro (Client Machine)

---

<h2>📝 Steps Included</h2>

- **Account Lockout Policy**  
  Configured Group Policy to lock accounts after 5 failed login attempts and verified lockout with a test user.  

- **Account Management**  
  Unlocked, reset password, disabled, and re-enabled accounts to observe changes in user access.  

- **Log Analysis**  
  Reviewed account activity logs on both the Domain Controller and client machine.  

- **Security Awareness**  
  Connected account lockouts and logging to cybersecurity and security operations fundamentals.  

---

<h2>📖 Learning Outcomes</h2>

- Gained practical experience configuring **Group Policy** in Active Directory.  
- Practiced **real-world IT support tasks** such as unlocking accounts and resetting passwords.  
- Strengthened understanding of **security logging** and how account activity can be monitored.  
- Learned to **document technical steps clearly**, a vital skill for IT support and system administration.  

---
<h2>🖥️ Logging into Client Machine</h2>

- Connected to **Client 1** (Windows 10 VM) in Azure using **Remote Desktop** and the VM’s public IP.  
- Used a **test user account** previously created in Active Directory.  
- Intentionally attempted multiple failed logins to trigger the **Account Lockout Policy** configured via Group Policy.  
- This verified that failed login attempts are enforced consistently across the network environment, not just on the Domain Controller.
  
<img src="https://github.com/user-attachments/assets/c8ae8841-da21-49b1-b36e-befe0ef7aa25" width="900" alt="First Screenshot">
<br><br>
<img src="https://github.com/user-attachments/assets/8cf959cd-7729-4045-8225-bcbeb8c7d492" width="500" alt="Second Screenshot">

---

### 🔹 Next Steps in Your Lab  

- **Log into the Domain Controller (DC-1) in Azure VM**  
  Use Remote Desktop to access your Domain Controller VM and log in with your Domain Admin credentials.  

- **Open Group Policy Management Console (GPMC)**  
  Press `Win + R`, type `gpmc.msc`, and hit Enter to launch the console.  

- **Edit the Default Domain Policy**  
  Navigate to *Computer Configuration → Windows Settings → Security Settings → Account Policies → Account Lockout Policy*.

<img width="1888" height="885" alt="image" src="https://github.com/user-attachments/assets/41c7674d-ab96-4d68-b0dd-cb23aeda174e" />

---

### 🔹 Troubleshooting: `gpmc.msc` Not Found  

- **How to Recognize It**  
  When trying to run `gpmc.msc` on your Domain Controller, Windows says the command cannot be found.  

- **What to Do**  
  - Log into the **Domain Controller (DC-1)**, not the client machine.  
  - Open **Server Manager → Manage → Add Roles and Features → Features**.  
  - Install **Group Policy Management**.  
  - Once installed, rerun `gpmc.msc` to open the console.  

<img width="1629" height="708" alt="Screenshot 3" src="https://github.com/user-attachments/assets/196063a3-0558-4467-a2ff-4f61d9ab224b" />
<br><br>
<img width="1385" height="672" alt="Screenshot 4" src="https://github.com/user-attachments/assets/0887661f-da0c-44af-a12d-86490bb4f5e4" />
<br><br>
<img width="1101" height="557" alt="image" src="https://github.com/user-attachments/assets/7f7bdca3-f456-42de-a40d-a62077a5aa49" />


---
