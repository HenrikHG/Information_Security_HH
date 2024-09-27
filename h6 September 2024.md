# h6 September 2024!

## **Summary of Schneier 2015**

### **2.3 One-Way Functions**
- **Definition**: A one-way function is easy to compute in one direction but extremely hard to reverse without additional information.
- **Example**: Breaking a plate is a one-way process; it's easy to break it but hard to reassemble the pieces back into the original plate.
- **Trapdoor One-Way Function**: These are special one-way functions that have a secret "trapdoor" allowing easy reversal if you know the secret. An example is disassembling a watch: difficult to reassemble without instructions, but easier if you have them.
- **Cryptographic Relevance**: While one-way functions themselves aren’t directly used for encryption, they form the building blocks of more complex cryptographic protocols, such as public-key cryptography.

### **2.4 One-Way Hash Functions**
- **Definition**: A one-way hash function takes a variable-length input and converts it to a fixed-length hash value, making it hard to reverse to the original input.
- **Properties**: 
  - **One-way**: Easy to compute the hash, but hard to reverse.
  - **Collision Resistance**: Difficult to find two different inputs that produce the same hash value.
- **Use Cases**: 
  - **Verification**: Used to fingerprint files, ensuring that the content matches without having to transmit the entire file.
  - **Message Authentication Codes (MAC)**: A one-way hash function combined with a secret key, ensuring that only those with the key can verify the hash.

---

## **a) Installing Hashcat and Testing with a Sample Hash**

## Step 1: Install Hashcat and Required Tools
1. Update your package list:
   ```bash
   sudo apt-get update
   ```
2. Install hashid, hashcat, and wget:
   ```bash
   sudo apt-get -y install hashid hashcat wget
   ```
   
![Screenshot 2024-09-27 112612](https://github.com/user-attachments/assets/d5df65da-8b28-4eb4-9a51-2dbde23fd0b2)

## Step 2: Create a Working Directory
1. Create a new directory for your work:
   ```bash
   mkdir hashed
   ```
2. Change to the new directory:
   ```bash
   cd hashed
   ```
   
## Step 3: Download a Dictionary File
1. Download the popular Rockyou dictionary file:
   ```bash
   wget https://github.com/danielmiessler/SecLists/raw/master/Passwords/Leaked-Databases/rockyou.txt.tar.gz
   ```

![Screenshot 2024-09-27 113100](https://github.com/user-attachments/assets/ccf4993a-158d-4ab2-b5f9-bed92b323fd1)

2. Extract the contents:
   ```bash
   tar xf rockyou.txt.tar.gz
   ```
3. Remove the compressed file to save space:
   ```bash
   rm rockyou.txt.tar.gz
   ```
   
4. Preview the Dictionary
   View the first 10 entries in the dictionary:
   ```bash
   head rockyou.txt
   ```

![Screenshot 2024-09-27 113640](https://github.com/user-attachments/assets/ba648927-21de-4b49-a04a-cf27c2105f7a)
 
## Step 4: Identify the Hash Type
1. Use `hashid` to identify the type of your hash. Replace `6b1628b016dff46e6fa35684be6acc96` with your hash:
   ```bash
   hashid -m 6b1628b016dff46e6fa35684be6acc96
   ```
   
![Screenshot 2024-09-27 114034](https://github.com/user-attachments/assets/741c580b-04e9-4db5-9cf1-f86bb05fdd71)

## Step 5: Crack the Hash
1. Use hashcat to crack the hash. Replace `'6b1628b016dff46e6fa35684be6acc96'` with your hash:
   ```bash
   hashcat -m 0 '6b1628b016dff46e6fa35684be6acc96' rockyou.txt -o solved
   ```

![Screenshot 2024-09-27 114212](https://github.com/user-attachments/assets/974bb02d-0bf8-4191-adee-7101dae4c8ac)
![Screenshot 2024-09-27 114233](https://github.com/user-attachments/assets/56ea12d9-120e-4dac-9fa5-a09478f03903)
![Screenshot 2024-09-27 114256](https://github.com/user-attachments/assets/d7cf3ad7-1128-47cb-a684-22645b8f3f21)

## Step 6: View the Cracked Password
1. Display the cracked password:
   ```bash
   cat solved
   ```

![Screenshot 2024-09-27 114526](https://github.com/user-attachments/assets/1af9c21d-f74b-4938-b99d-5af53db73160)

---

## **b) Cracking the Given Hash**

### **Step 1: Identifying the Hash Type**
- The provided hash is: `d595b2086532422bbe654bc07ea030df`.
- To identify the hash type, you can use the `hashid` tool:
  ```bash
  hashid -m d595b2086532422bbe654bc07ea030df
  ```

![Screenshot 2024-09-27 114717](https://github.com/user-attachments/assets/f8dc038b-f077-4907-a318-b0266f959382)


### **Step 2: Cracking the Hash with Hashcat**
1. **Crack the Hash**:
   - Use the `rockyou.txt` wordlist to crack the hash:
     ```bash
     hashcat -m 0 target_hash.txt rockyou.txt -o cracked_hash.txt
     ```

![Screenshot 2024-09-27 114934](https://github.com/user-attachments/assets/deee7dd6-72e8-4a15-a097-4b70449181a8)


3. **Check the Cracked Password**:
   - After the cracking process completes, view the result:
     ```bash
     cat solved
     ```
     
![Screenshot 2024-09-27 114946](https://github.com/user-attachments/assets/48ad4b66-ee8f-4ad0-9fa2-aa2125ae7c74)
