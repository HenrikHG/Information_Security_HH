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

### **Step 1: Installing Hashcat**
1. **Download Hashcat**:
   - Visit [Hashcat's official website](https://hashcat.net/hashcat/) to download the latest version.
   - Follow the installation instructions for your operating system (Windows/Linux/MacOS).

2. **Verify Installation**:
   - Open your terminal or command prompt.
   - Run the following command:
     ```bash
     hashcat -I
     ```
   - This command should display information about Hashcat's version and your system’s supported hardware.

### **Step 2: Testing with a Sample Hash**
1. **Generate a Sample Hash**:
   - Let's create a simple hash using MD5. For example, using `password123`:
     ```bash
     echo -n "password123" | md5sum
     ```
   - The output should be: `482c811da5d5b4bc6d497ffa98491e38`.

2. **Cracking the Sample Hash**:
   - Create a text file (`hashes.txt`) with the generated hash:
     ```
     482c811da5d5b4bc6d497ffa98491e38
     ```
   - Download the `rockyou.txt` wordlist, as it contains a comprehensive list of common passwords:
     ```bash
     wget https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt
     ```
   - Run Hashcat to crack the hash using the wordlist:
     ```bash
     hashcat -m 0 hashes.txt rockyou.txt -o cracked_sample.txt
     ```
   - The command breakdown:
     - `-m 0`: Specifies MD5 hash type.
     - `hashes.txt`: Input file containing the hash.
     - `rockyou.txt`: Wordlist used to crack the hash.
     - `-o cracked_sample.txt`: Output file to store the cracked hash.

3. **Check the Result**:
   - After Hashcat finishes, you can check the output file to see the cracked password:
     ```bash
     cat cracked_sample.txt
     ```
   - The output should show the original password, e.g., `482c811da5d5b4bc6d497ffa98491e38:password123`.

---

## **b) Cracking the Given Hash**

### **Step 1: Identifying the Hash Type**
- The provided hash is: `d595b2086532422bbe654bc07ea030df`.
- To identify the hash type, you can use the `hashid` tool:
  ```bash
  hashid -m d595b2086532422bbe654bc07ea030df
  ```
- According to the document, it is likely an MD5 hash, and the `-m` parameter for MD5 in Hashcat is `0`.

### **Step 2: Cracking the Hash with Hashcat**
1. **Create a File with the Hash**:
   - Create a file named `target_hash.txt` and add the hash:
     ```
     d595b2086532422bbe654bc07ea030df
     ```

2. **Crack the Hash**:
   - Use the `rockyou.txt` wordlist to crack the hash:
     ```bash
     hashcat -m 0 target_hash.txt rockyou.txt -o cracked_hash.txt
     ```
   - The command breakdown:
     - `-m 0`: Specifies MD5 hash type.
     - `target_hash.txt`: Input file containing the hash.
     - `rockyou.txt`: Wordlist used to crack the hash.
     - `-o cracked_hash.txt`: Output file to store the cracked hash.

3. **Check the Cracked Password**:
   - After the cracking process completes, view the result:
     ```bash
     cat cracked_hash.txt
     ```
   - This will display the cracked password corresponding to the given hash.

### **Results**
- Hashcat should display the cracked password in the `cracked_hash.txt` file, which completes the process.
