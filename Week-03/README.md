# Week-3_B084 - Cracking Passwords using JTR and Hash

## 📌 Background
**John the Ripper (JTR)** is a popular password-cracking tool used by security professionals to test password strength. Originally built for Unix systems, it now works across Windows, Linux, and macOS. It can audit various password hashes and unlock password-protected files such as PDFs, ZIP archives, and Office documents. 

**Johnny** is the graphical user interface (GUI) for John the Ripper. It provides a simple point-and-click interface so beginners can use JTR without memorizing complex command-line syntax. In this lab task, JTR, Johnny, and the Networkwalks Hash Calculator are used to recover the password of a protected PDF file (`My Locked PDF1.pdf`).

---

## 🛠️ Project Module 1: Cracking a PDF Password with John the Ripper

### Task 1: Configuring and Cracking `My Locked PDF1.pdf`
Using JTR (`john.exe`) and the Johnny GUI on a Windows PC:

1. **Configure Johnny:** Link the `john.exe` executable inside Johnny's settings.
   ![Configuring Johnny](configuring%20johnny.png)

2. **Extract the PDF Hash:** Upload the locked PDF file into the online hash calculator to generate its crackable hash value.
   ![Upload Locked PDF](locked%20pdf%20file%20upload%20into%20hash%20calculator.png)

3. **Load the Hash into Johnny:** Copy the generated hash value into a text file and load it into Johnny.
   ![Cracked Hash for Locked PDF](cracked%20hash%20for%20the%20locked%20pdf.png)

4. **Start the Attack:** Select **Start New Attack** in Johnny to begin cracking the password.
   ![Opening Hash and Starting Attack](openinh%20my%20hash%20by%20starting%20an%20attack.png)

5. **Recover the Password:** Once the attack finishes, the plaintext password is revealed.
   ![Cracking the Password](cracking%20the%20pw.png)
   ![Cracked Password of the Hash](cracked%20password%20of%20the%20hash.png)

* **Recovered Password for Locked PDF:** `good-luck`
* **Proof of Unlocked PDF:**
  ![Cracked PDF](cracked%20pdf.png)

---

## 🔐 Project Module 2: Using the Networkwalks Hash Generator

1. **Open the Hash Generator:** Navigate to the Networkwalks Hash Calculator and select the PDF tab to load the locked file.
   ![Using NW Hash Calculator](using%20the%20NW%20hash%20calculator.png)

2. **Extract & Crack the Hash:** The tool extracts the hash value locally in the browser and tests it against password lists.
   ![Using the Hash Crack](using%20the%20hash%20crack.png)

3. **Match the Password:** The tool matches the exact password for the locked PDF (`password 1`).
   ![Password 1 Match](password%201%20match.png)

---

## 🐞 Problems Encountered & Solutions

* **Problem 1: Installing and Running John the Ripper**
  * **Issue:** JTR can throw errors if the archive is not extracted properly or if Johnny cannot locate the core executable.
  * **Solution:** Ensure the entire JTR archive is extracted to a dedicated folder and explicitly point Johnny's settings to `john.exe` inside the `run` directory for optimal performance.

---

## 💡 What I Learned

1. **John the Ripper vs. Networkwalks Hash Generator:** Both tools are effective for extracting hashes and testing password strength, though John the Ripper offers greater flexibility and power when cracking complex files or using custom wordlists.
2. **System Snapshots:** Creating a clean virtual machine snapshot before performing experimental cybersecurity tasks provides a reliable recovery point.
3. **Technical Documentation:** Properly documenting configurations, commands, screenshots, errors, and solutions is essential for professional cybersecurity reporting.

---

## 🔗 Tools & Resources
* [John the Ripper](https://www.openwall.com/john/)
* [Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/)

---

## 👤 Author
* **Name:** AMNA SANI
* **Role:** Cybersecurity Specialist (Batch B084D)
* **Program:** Cybersecurity at Networkwalks — Week 03: Cybersecurity & Pentesting Lab Setup
