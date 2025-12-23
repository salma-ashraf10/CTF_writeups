# Encrypted_Database - Web Challenge

- **Platform:** Cyber Talents  
- **Category:** Web — Easy (50 points)

---

## Challenge Description

The challenge provides a static website called **TopNewsJournal Website**.

<img width="1765" height="883" alt="image" src="https://github.com/user-attachments/assets/de015e4e-ddba-414d-9e14-36bf351734a3" />

---

## Tools Used

- Browser Developer Tools (Inspect Element)

---

## Analysis Steps

### 1. Initial Recon
When I opened the website, I found a page that contains multiple tabs such as **Home**, **About**, etc.

### 2. Inspecting the Source
I opened the Developer Tools by pressing `Ctrl + Shift + I` and navigated to the **Elements** tab.

### 3. Discovering Admin Path
At line 32, I discovered a `<script>` tag referencing the following path:

`admin/assets/app.js`

<img width="636" height="74" alt="image" src="https://github.com/user-attachments/assets/b8057ff6-69ec-49fa-9b87-a019db390224" />

### 4. Identifying the Admin Endpoint
This indicated the existence of an **admin** endpoint.

### 5. Accessing Admin Panel
By manually navigating to `/admin`, an admin login page appeared. However, no credentials were provided.

<img width="839" height="598" alt="image" src="https://github.com/user-attachments/assets/acbaf519-6bd9-4515-b5fb-c64a2eaa3edc" />

### 6. Finding Hidden Endpoint
After inspecting the page again, I noticed suspicious code at line 39 containing a hidden input field with an endpoint value.

<img width="842" height="74" alt="image" src="https://github.com/user-attachments/assets/fe00a6bd-f4d1-426d-94b1-5bde06943b57" />

### 7. Accessing the Database File
Appending the discovered path resulted in the following URL:

`http://[your machine]/admin/secret-database/db.json`

### 8. Identifying the Hash
Inside the file, a hashed flag was found. Using a hash identifier tool confirmed it was an **MD5** hash.

<img width="658" height="231" alt="image" src="https://github.com/user-attachments/assets/8462ea8c-49f6-41a9-a33f-f6296c68d21e" />

### 9. Cracking the Hash
The hash was successfully cracked using **CrackStation**.

<img width="1394" height="88" alt="image" src="https://github.com/user-attachments/assets/303018b7-364a-49b5-9157-384e7bad2a9a" />

### 10. Flag Retrieved
Finally, the flag was obtained.

---

## Flag:
badboy

---

**Challenge Link:**  
https://cybertalents.com/challenges/web/encrypted-database

