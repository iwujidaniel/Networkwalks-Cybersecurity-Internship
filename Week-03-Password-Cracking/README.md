# Week 3 – Password Cracking
## Networkwalks Cybersecurity & Ethical Hacking Internship

## 1. Project Overview

Week 3 focused on understanding password security, password hash extraction, and password recovery through practical exercises.

The activities involved using John the Ripper (JTR), its graphical interface Johnny, and Networkwalks online password-cracking tools to perform authorised password recovery tests on password-protected PDF files supplied for the training lab.

The week consisted of two practical modules:

- **PM1:** Password Cracking with John the Ripper (JTR).
- **PM2:** Password Cracking with Networkwalks Tools.

## 2. Learning Objectives

The objectives of these practical exercises were to:

- Understand password hashes and their role in password security.
- Learn how password-protected PDF hashes can be extracted.
- Install and configure password-cracking tools.
- Understand dictionary-based password attacks.
- Explore the importance and limitations of wordlists.
- Perform authorised password recovery tests.
- Verify recovered passwords by opening protected PDF documents.
- Document practical findings and maintain cybersecurity evidence.

## 3. Tools and Technologies Used

| Tool | Purpose |
|---|---|
| John the Ripper 1.9.0 Jumbo | Password hash auditing and recovery |
| Johnny 2.2 | Graphical interface for John the Ripper |
| Networkwalks Hash Calculator | Extracting PDF password hashes |
| Networkwalks Password Cracker | Performing dictionary-based password recovery |
| Online PDF Hash Extractor | Extracting PDF hashes for PM1 |
| Notepad | Saving and preparing extracted hash files |
| Windows | Practical testing environment |

## 4. PM1 – Password Cracking with John the Ripper

**Project folder:** [PM1-JTR](PM1-JTR/)

### Procedure

1. Downloaded the Windows version of John the Ripper.
2. Extracted the downloaded archive and located `john.exe` inside the `run` folder.
3. Downloaded and installed Johnny 2.2.
4. Launched Johnny and configured it to use the John the Ripper executable.
5. Verified that Johnny successfully detected the installed John the Ripper version.
6. Selected the supplied password-protected PDF lab file.
7. Used an online PDF hash extraction tool to extract its password hash.
8. Copied the extracted hash into Notepad and saved it as `hash1.txt`.
9. Loaded the hash file into Johnny.
10. Started a dictionary-based password recovery attack.
11. Monitored the attack until Johnny reported successful password recovery.
12. Used the recovered password to open the protected PDF and verified that the document was accessible.

### Results

The password recovery exercise was successful. Johnny reported 100% completion and 2/2 cracked, and the protected PDF opened successfully using the recovered password.

### Evidence

The practical screenshots and detailed documentation are available in the [PM1-JTR folder](PM1-JTR/).

## 5. PM2 – Password Cracking with Networkwalks Tools

**Project folder:** [PM2-Networkwalks-Tools](PM2-Networkwalks-Tools/)

### Procedure

1. Selected a password-protected PDF supplied for the training exercise.
2. Opened the Networkwalks Hash Calculator.
3. Uploaded the selected PDF to extract its password hash.
4. Copied the complete extracted hash and saved it locally in `hash2.txt`.
5. Opened the Networkwalks Password Cracker.
6. Submitted the extracted hash to the password-cracking tool.
7. Observed the initial attempt using `My Locked PDF1.pdf`, which returned an access-denied result because the available wordlist did not contain its password.
8. Selected another supplied lab document, `My Locked PDF3.pdf`.
9. Generated a fresh hash from the third PDF rather than reusing the previous hash.
10. Saved the new hash and submitted it to the Password Cracker.
11. Successfully recovered the password using the available wordlist.
12. Entered the recovered password into `My Locked PDF3.pdf` and confirmed that the PDF opened successfully.

### Results

The initial attempt was unsuccessful, demonstrating the limitations of a wordlist when the correct password is not included.

The subsequent attempt using `My Locked PDF3.pdf` was successful. The recovered password unlocked the PDF, confirming successful password recovery.

### Evidence

The screenshots and detailed documentation are available in the [PM2-Networkwalks-Tools folder](PM2-Networkwalks-Tools/).

## 6. Overall Learning Outcomes

Through these practical exercises, I gained experience in:

- Installing and configuring password-auditing tools.
- Extracting password hashes from protected PDF documents.
- Understanding dictionary-based password attacks.
- Using John the Ripper and Johnny for password recovery.
- Using online hash extraction and password-cracking tools.
- Understanding why wordlist selection affects password recovery results.
- Verifying recovered passwords against protected documents.
- Capturing, organising, and documenting cybersecurity evidence.

## 7. Security and Ethical Considerations

All practical exercises were conducted using password-protected PDF files supplied for the authorised training lab.

The activities were limited to educational password-auditing exercises. No unauthorised accounts, systems, or personal documents were targeted.

Sensitive password and hash information has been excluded from the published project evidence where appropriate.

## 8. Conclusion

Week 3 provided practical exposure to password security and password recovery techniques using both locally installed and web-based tools.

The exercises improved my understanding of password hash extraction, tool configuration, dictionary-based attacks, wordlist limitations, and password verification.

The experience also reinforced the importance of strong passwords, responsible security testing, and proper documentation of cybersecurity activities.
