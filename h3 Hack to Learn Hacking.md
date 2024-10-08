# h3 Hack to Learn Hacking

---

## Summary of the Presentation "How Much Dirty Laundry Are Your Smart Home Devices Airing About You?" by Jack Fitzsimons

- **Focus of the Talk**: The presentation examined smart home devices (initially a washing machine and Roomba, later shifted to smartwatches like the Samsung Galaxy Watch 4 and Garmin Forerunner 245) to understand the data they collect and share.

- **Motivation**: As everything is becoming "smart," Fitzsimons wanted to explore the privacy implications of these devices. He highlighted how devices like smartwatches, which are increasingly used for health and fitness tracking, collect sensitive data.

- **Data Risks**:
   - Smart devices gather extensive personal data, including location, health statistics, and even voice data in Samsung’s case.
   - There are instances where smartwatches exposed sensitive data (e.g., military personnel accidentally revealing secret locations via fitness apps).

- **Privacy Policies**:
   - Companies like Samsung and Garmin collect vast amounts of data (e.g., health data, location, payment information).
   - Samsung collects voice data through Bixby and shares it across devices.
   - Garmin requests access to personal files, including photos and location data.

- **Technical Investigation**:
   - Fitzsimons examined app permissions, third-party services, and monitored traffic from smartwatches using tools like APK tool and web proxies.
   - Samsung uses various trackers like Google Analytics and Microsoft services, while Garmin uses Facebook and Google for data collection.
  
- **Conclusion**:
   - Smart devices collect significant amounts of data that can potentially be exploited.
   - It is difficult to fully secure privacy without limiting functionality.
   - Consumers should be aware of privacy implications and selectively block data collection where possible (e.g., using custom DNS settings).

- **Key Takeaway**: While it’s challenging to completely avoid data collection, reading privacy policies, choosing privacy-conscious devices, and using technical tools can help mitigate risks.

- **Question/ Ideas**: As smart devices become more integrated into our daily lives, how can consumers effectively balance convenience and privacy, especially when many functionalities depend on data sharing?

## Source

- **Presentation**: [Disobey 2024 - "How Much Dirty Laundry Are Your Smart Home Devices Airing About You?" by Jack Fitzsimons](https://youtu.be/fWv0Z_FePKU?si=Ska6f5tiZWaYIcod)

---

# Summary of "Command Line Basics Revisited" by Tero Karvinen

- **Overview**: The guide revisits essential command-line skills, providing practical tips.
  
- **Key Topics**:
  - Basic commands for navigating directories, viewing files, and managing file systems.
  - How to use SSH for remote access and secure file transfers.
  - Instructions on package management, including installing and removing software.
 
## Source
  
- **Article**: [Command Line Basics Revisited by Tero Karvinen](https://terokarvinen.com/2020/command-line-basics-revisited/)

---

# a) Bandit Oh-Five (Levels 0-4)

### Bandit Level 0
- **Steps**:
  1. Open a terminal.
  2. Use the following SSH command to connect:
     ```bash
     ssh bandit0@bandit.labs.overthewire.org -p 2220
     ```
  3. Enter the password: `bandit0`.

![Screenshot 2024-09-05 220402](https://github.com/user-attachments/assets/dc30b7f7-248d-4ac6-8b6a-5c68a05e9e3f)

---

### Bandit Level 0 → Level 1
- **Steps**:
  1. List the files in the home directory:
     ```bash
     ls
     ```
  2. Read the content of the file named `readme`:
     ```bash
     cat readme
     ```
  3. The file contains the password for Level 1.

![Screenshot 2024-09-05 220656](https://github.com/user-attachments/assets/3a7a7295-306b-4033-8acd-dc96710de307)
![Screenshot 2024-09-05 221139](https://github.com/user-attachments/assets/e6bafb1d-2506-4622-9c18-b7ee35c06c07)

---

### Bandit Level 1 → Level 2
- **Steps**:
  1. List the files in the home directory:
     ```bash
     ls
     ```
  2. Read the content of the file named `-`:
     ```bash
     cat ./-
     ```
  3. The file contains the password for Level 2.

![Screenshot 2024-09-05 221429](https://github.com/user-attachments/assets/8752d549-638c-4db2-93f2-c490f3324c88)
![Screenshot 2024-09-05 221741](https://github.com/user-attachments/assets/61f2eca4-964f-4897-9055-c4392a4d9a29)

---

### Bandit Level 2 → Level 3
- **Steps**:
  1. List the files in the home directory:
     ```bash
     ls -a
     ```
     This will show the files, including the one named with spaces in the filename.

  2. Display the content of the file using:
     ```bash
     cat spaces\ in\ this\ filename
     ```
     The backslashes (`\`) are used to escape the spaces in the filename.

  3. The file contains the password for Level 3.

![Screenshot 2024-09-05 222031](https://github.com/user-attachments/assets/cf1ba37b-2cc6-49be-9ab2-6a954621b60b)
![Screenshot 2024-09-05 222155](https://github.com/user-attachments/assets/224c48bd-f7f9-4af1-9144-c1b5dd03d071)


---

### Bandit Level 3 → Level 4
- **Steps**:
  1. Navigate to the `inhere` directory:
     ```bash
     cd inhere
     ```
  2. List all files, including hidden ones:
     ```bash
     ls -a
     ```
  3. Read the hidden file :
     ```bash
     cat ...Hiding-From-You
     ```
  4. The file contains the password for Level 4.

![Screenshot 2024-09-05 222958](https://github.com/user-attachments/assets/9e55e697-c1dd-4055-97ee-7dbe230ce0fa)
![Screenshot 2024-09-05 223019](https://github.com/user-attachments/assets/4f6db0ba-a578-46a6-9268-f7183e3ae7aa)

---

### Bandit Level 4 → Level 5
- **Steps**:
  1. Navigate to the `inhere` directory:
     ```bash
     cd inhere
     ```

![Screenshot 2024-09-05 234025](https://github.com/user-attachments/assets/53c595bb-f2da-4ab0-809c-39de4147853b)

  2. Use the `file` command to identify the human-readable file:
     ```bash
     file ./-file*
     ```
  3. Locate the file that is marked as ASCII text.
  4. Display the content of the human-readable file:
     ```bash
     cat <filename>
     ```
  5. The file contains the password for Level 5.

![Screenshot 2024-09-05 234042](https://github.com/user-attachments/assets/2895979b-4ccf-409d-9f60-cbccbc320527)

## Source

- **Wargame**: [OverTheWire - Bandit Wargame](https://overthewire.org/wargames/bandit/)

---

# b) Can't Fish (Disable Networking)

### Steps

1. **List all network interfaces**:
2. **Disconnect your network**:
3. **Test the network connection**:

![Screenshot 2024-09-05 223450](https://github.com/user-attachments/assets/996aeb56-ae7a-43f9-b3b3-0dacdfc2858d)
