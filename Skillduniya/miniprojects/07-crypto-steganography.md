# Mini Project 07: Cryptography & Steganography

## Summary

This project explores and compares two essential data protection techniques — **cryptography** and **steganography**.  
It includes theoretical benefits and a practical demonstration using QuickStego and command-line methods to hide messages inside images.

---

## Objective

- Understand the differences between cryptography and steganography  
- Highlight their individual advantages and use cases  
- Demonstrate image-based steganography in a controlled test

---

## Cryptography: Key Benefits

- **Strong Data Protection**: Transforms plain text into unreadable ciphertext  
- **Authentication & Integrity**: Digital signatures and hashes confirm data origin and prevent tampering  
- **Secure Communication**: Used in HTTPS, VPNs, encrypted apps like WhatsApp  
- **Compliance**: Helps meet standards like GDPR, HIPAA, PCI-DSS  
- **Versatile Applications**: Online transactions, password protection, blockchain, military communications

---

## Steganography: Key Benefits

- **Hidden in Plain Sight**: Embeds data into normal-looking files (images, audio, video)  
- **Layered Security**: Can be combined with encryption for added protection  
- **Bypasses Censorship**: Useful in restricted networks  
- **Evades Detection**: Doesn’t look suspicious to IDS or monitoring tools  
- **Digital Watermarking**: Prevents piracy in digital content distribution

---

## Practical Demonstration

### 🔒 Image Steganography with QuickStego

1. Open QuickStego  
2. Load a cover image (JPG/PNG)  
3. Enter secret message  
4. Save the modified image (now contains hidden data)

### 💻 Manual Steganography via Command Prompt (Conceptual)

- Demonstrated embedding data using CLI tools to simulate manual techniques.  
- Useful for environments without a GUI or for script-based hiding.

---

## Conclusion

Cryptography protects **what** the data says.  
Steganography hides **that data exists at all**.

> Combined, they offer stronger confidentiality, integrity, and stealth.

This project showed how cryptography and steganography play different roles in the security stack. Tools like QuickStego help visualize the process, while command-line methods give flexibility in different environments. Mastering both techniques is vital for modern cyber defenders.
