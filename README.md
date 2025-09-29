# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="938" height="834" alt="image" src="https://github.com/user-attachments/assets/2f269b1e-0b1e-40f3-8c4a-ffce9d47ae1d" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="957" height="720" alt="image" src="https://github.com/user-attachments/assets/994e8a4b-a7a7-4503-a528-eb0b5bc54e08" />
<img width="851" height="777" alt="image" src="https://github.com/user-attachments/assets/d11a47ab-8610-4cde-b6b5-7d6a1c76cfd0" />

**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="663" height="343" alt="image" src="https://github.com/user-attachments/assets/d8882bc5-e352-4a25-8421-d9065600c61c" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="843" height="199" alt="image" src="https://github.com/user-attachments/assets/6d93b2cb-0daf-4ef6-8a67-de06a5d9e324" />

**6. Send the generated link to the victim.**
<img width="982" height="838" alt="image" src="https://github.com/user-attachments/assets/bd73681a-10e5-4fbe-ad2b-b6f49744c4af" />

**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="945" height="427" alt="image" src="https://github.com/user-attachments/assets/e8a2e195-d80f-4a2d-8664-4fbbf61599da" />



## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
