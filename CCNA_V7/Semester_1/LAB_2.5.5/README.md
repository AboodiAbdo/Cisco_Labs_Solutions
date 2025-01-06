# **Cisco Packet Tracer Lab - 2.5.5: Capture Configuration to a Text File**

### **🚀 My NTI Journey in Networking** 
Hello! I’m **AbdulRhman AbdulGhaffar**, and this repository marks the beginning of my journey with **NTI** in learning networking and cybersecurity. Here, I document solutions for Cisco labs with detailed explanations, aiming to share knowledge and provide practical solutions for students and professionals alike.  
This repository contains solutions for basic switch configurations from Cisco Networking Academy. The lab focuses on securing CLI and console ports, configuring messages for users logging into the switch, and saving the configuration to NVRAM.

---

## **Lab Objectives:**
- **Part 1**: Verify the Default Switch Configuration
- **Part 2**: Configure a Basic Switch Configuration
- **Part 3**: Configure a MOTD Banner
- **Part 4**: Save Configuration Files to NVRAM
- **Part 5**: Configure S2

---

## **Lab Description**  
In this activity, you will perform basic switch configuration tasks. These tasks include securing access to the CLI and console ports using encrypted and plain text passwords. Additionally, you will learn how to configure messages for users logging into the switch. These messages also serve to warn unauthorized users that access is prohibited.

---

## **Step-by-Step Solution**

### **Part 1: Verify the Default Switch Configuration**  
1. **Access Privileged EXEC Mode**  
   - Access the switch CLI and enter privileged EXEC mode by typing:  
     ```plaintext
     Switch> enable
     Switch#
     ```

2. **Examine the Current Switch Configuration**  
   - To view the current configuration, enter:  
     ```plaintext
     Switch# show running-config
     ```
   Answer the following questions:  
   - How many Fast Ethernet interfaces does the switch have?  
   - How many Gigabit Ethernet interfaces does the switch have?  
   - What is the range of values shown for the vty lines?  
   - Which command will display the current contents of NVRAM?  
   - Why does the switch respond with “startup-config is not present?”

---

### **Part 2: Create a Basic Switch Configuration**  
1. **Assign a Name to the Switch**  
   - Configure a hostname for the switch:  
     ```plaintext
     Switch(config)# hostname S1
     S1(config)# exit
     S1#
     ```

2. **Secure Access to the Console Line**  
   - Set a password for console access:  
     ```plaintext
     S1# configure terminal
     S1(config)# line console 0
     S1(config-line)# password letmein
     S1(config-line)# login
     S1(config-line)# exit
     S1(config)# exit
     ```

3. **Secure Privileged Mode Access**  
   - Set the enable password:  
     ```plaintext
     S1# configure terminal
     S1(config)# enable password c1$c0
     S1(config)# exit
     ```

4. **Verify Privileged Mode Access Security**  
   - Exit privileged mode and log back in to verify the password is set for console and privileged modes.

5. **Configure the Enable Secret Password**  
   - Replace the enable password with an encrypted password:  
     ```plaintext
     S1# configure terminal
     S1(config)# enable secret itsasecret
     S1(config)# exit
     ```

6. **Encrypt All Passwords**  
   - Use the `service password-encryption` command to encrypt all passwords:  
     ```plaintext
     S1# configure terminal
     S1(config)# service password-encryption
     S1(config)# exit
     ```

---

### **Part 3: Configure a MOTD Banner**  
1. **Configure the Message of the Day (MOTD) Banner**  
   - Set the MOTD banner to display a warning message:  
     ```plaintext
     S1# configure terminal
     S1(config)# banner motd "This is a secure system. Authorized Access Only!"
     S1(config)# exit
     ```

   - The banner will be displayed whenever anyone attempts to log into the switch.

---

### **Part 4: Save and Verify Configuration Files to NVRAM**  
1. **Verify Configuration Accuracy**  
   - To ensure the configuration is correct, enter:  
     ```plaintext
     S1# show running-config
     ```

2. **Save Configuration to NVRAM**  
   - Backup the running configuration to NVRAM:  
     ```plaintext
     S1# copy running-config startup-config
     ```

---

### **Part 5: Configure S2**  
Repeat the configuration steps for switch S2, which should include the following:  
1. Set the device name to **S2**.
2. Secure access to the console using the password **letmein**.
3. Configure an enable password **c1$c0** and an enable secret password **itsasecret**.
4. Set an appropriate MOTD banner.
5. Encrypt all plain-text passwords.
6. Save the configuration to NVRAM.

---

## 📝 Lab Completion Steps

### 🎥 Video Tutorial
This video demonstrates the correct steps to complete the lab successfully. Watch and follow along:

[Watch the video](https://github.com/user-attachments/assets/4696acf0-7cf0-469d-9adf-ecb6d335cacf)

---

### 🖼️ Result Screenshot
After completing the lab correctly, you should see a result like the screenshot below. 

To verify your results:
1. Click on **Check Results**.
2. Navigate to **Assessment Items**.
![Screenshot 2025-01-06 152842](https://github.com/user-attachments/assets/955ccc36-5eb5-46fd-bc52-a8149b39a292)

---

### **Files and Resources**  
- [Task Instructions (PDF)](https://www.netacad.com/content/itn/1.0/courses/content/m2/en-US/assets/2.5.5-packet-tracer---configure-initial-switch-settings.pdf)  
- [Packet Tracer Lab (PKA)](https://www.netacad.com/content/itn/1.0/courses/content/m2/en-US/assets/2.5.5-packet-tracer---configure-initial-switch-settings.pka)

---

### **Conclusion**  
This lab demonstrates the basic configurations required for securing a switch's command-line interface and access ports, as well as setting a message of the day (MOTD) banner and saving configurations. 

---  

### **References** 
![downlpoad](https://github.com/user-attachments/assets/fff09150-44f6-4591-90a2-29dc090b1437)
- [Cisco Networking Academy](https://www.netacad.com)  
