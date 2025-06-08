🔐 Password Hashing 🛡️

A Python script that performs the following operations:

1. Prompt the user to enter a password.
2. Hash the password using the SHA-256 algorithm.
3. Store the hashed password in a file named hashed_passwords.txt (each new hash
should be appended as a new line).
4. Display the hashed password on the screen.

![image](https://github.com/user-attachments/assets/e96d8005-e3fd-4f2b-8696-66fefaef9353)

<i> (Using Google Colab) </i>
      
This Python script securely hashes a user-provided password using the SHA-256
algorithm from the hashlib library. It begins by prompting the user to input a password,
then converts the input string into bytes (since hashing functions require byte input). The
script applies the SHA-256 hashing algorithm to the byte-converted password and
converts the resulting hash into a readable hexadecimal string. It then prints the hashed
password on the screen for verification and appends it to a file named
hashed_passwords.txt, ensuring the hash is stored persistently, with each hashed
password saved on a new line.

👨‍💻 Codes:

<div class="code-cell">
<code>from hashlib import sha256

\# Prompt user to enter a password
password = input("Enter a password: ")

\# Convert the password into bytes because regular string is not working
password_bytes = password.encode()

\# Hash the password using SHA-256 by converting the hash object into
\# a hexadecimal string
hashed_password = sha256(password_bytes).hexdigest()

\# Print the hashed password to the screen
print("Hashed password:\n" + hashed_password)

\# Save the hashed password to a file
with open("hashed_passwords.txt", "a") as f:
    f.write(hashed_password + "\n")</code>
</div>


    
