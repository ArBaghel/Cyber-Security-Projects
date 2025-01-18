# Cryptography Challenge with Hashcat 🔐  

This project shows the practical applications of cryptography and password-cracking techniques. It imitates real-world conditions where penetration testers analyse the encrypted files.  

Very thankfull to my mentor, **Snachya Singh**, for guiding me throughout this project!  

## Project Overview  

The purpose was to crack passwords for a protected ZIP file and a PDF file using tools like **Hashcat**, **John the Ripper**, and **Perl Strawberry Perl**.  

### Tools Used  
- **John the Ripper**: To extract hashes from the encrypted files.  
- **Hashcat**: To crack passwords based on the extracted hashes.  
- **Perl Strawberry Perl**: For handling PDF file hashes.  
- **Notepad++**: To fix UTF encoding issues.  
- **rockyou.txt Wordlist**: A commonly used password list for brute force attacks.

## Steps  

### Step 1: Initial Setup  
1. Installed and configured the required tools in a Windows environment.  
2. Downloaded the password-protected ZIP file from [this link](https://drive.google.com/file/d/1sQ_UdmwvYtGzqejDNu1EfjhHNC6BkCmT/view?usp=sharing).  

### Step 2: Cracking the ZIP File Password  

#### 1️⃣ Extracting the Hash  
Used **John the Ripper** to extract the hash of the ZIP file:  
```bash  
zip2john.exe filename.zip > hash.txt  
```  

#### 2️⃣ Identifying the Hash Mode  
Referred to [Hashcat Example Hashes](https://hashcat.net/wiki/doku.php?id=example_hashes) and identified the hash mode as **13600**.  

#### 3️⃣ Cracking the Password  
Used **Hashcat** with the following command:  
```bash  
hashcat.exe -a 0 -m 13600 hash.txt rockyou.txt --force  
```  
Result: Successfully cracked the ZIP file password!  

---

### Step 3: Cracking the PDF File Password  

#### 1️⃣ Extracting the Hash  
Used **Perl Strawberry Perl** to extract the hash of the PDF file:  
```bash  
perl pdf2john.pl filename.pdf > hash.txt  
```  

#### 2️⃣ Identifying the Hash Mode  
Determined the hash mode for PDF files as **10500**.  

#### 3️⃣ Cracking the Password  
Used **Hashcat** with the following command:  
```bash  
hashcat.exe -a 0 -m 10500 hash.txt rockyou.txt --force  
```  
Result: Successfully cracked the PDF file password!  

---

## Outcomes  
- **ZIP File**: Password successfully cracked and contents extracted.  
- **PDF File**: Password successfully cracked and document accessed.  

---

## Key Learnings  
- Deepened understanding of cryptographic hashing algorithms.  
- Gained hands-on experience with tools like **Hashcat** and **John the Ripper**.  
- Enhancing the problem-solving and persistence in tackling cybersecurity challenges.  

---

## Acknowledgements  
Special thanks to my mentor, **Snachya Singh**, for her guidance and support for this project!  

---

## Connect with Me  
Feel free to connect and share your feedback or reach out:  
- [LinkedIn](https://www.linkedin.com/in/aditya-singh-baghel-562832296?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app)  
 

---  

### Tags  
`#Fundamentals of Cybersecurity` `#Cryptography` `#Hashcat` `#JohnTheRipper`  

```


