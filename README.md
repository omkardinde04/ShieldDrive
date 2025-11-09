# ShieldDrive 🔒

**CSF Lab CA 2 - Secure File Vault System**

A web-based secure file vault that ensures your files remain protected with enterprise-grade encryption and can only be accessed with the correct password.

## 🎓 Project Information

**Course:** Computer Systems & Security (CSF) Lab - Continuous Assessment 2

**Institution:** K.J. Somaiya College of Engineering

## 👥 Contributors

| Name | Roll Number | Email | GitHub |
|------|-------------|-------|--------|
| Palak Chandak | 16010123226 | palak.chandak@somaiya.edu | [@palakchandak8](https://github.com/palakchandak8) |
| Palak Nagar | 16010123227 | palak.nagar@somaiya.edu | [@palak642](https://github.com/palak642) |
| Omkar Dinde | 16010123219 | omkar.dinde@somaiya.edu | [@omkardinde04](https://github.com/omkardinde04) |

## 🛡️ Overview

ShieldDrive is a secure, web-based file vault system that implements multiple layers of security to protect user files. Files are encrypted and can only be accessed by authorized users with the correct credentials, ensuring complete data privacy and security.

## 🔐 Security Mechanisms

### 1. **End-to-End Encryption**
- **Scope:** Complete data protection from client to storage
- **Description:** All files are encrypted on the client side before transmission and remain encrypted at rest. Only authorized users with valid credentials can decrypt and access the files, ensuring that even if the server is compromised, data remains secure.

### 2. **File Encryption (AES-256)**
- **Scope:** Individual file protection
- **Description:** Implements Advanced Encryption Standard (AES) with 256-bit keys for encrypting files. AES-256 is a military-grade encryption standard that provides robust protection against brute-force attacks and unauthorized access.

### 3. **JWT Authentication & Authorization**
- **Scope:** Secure user sessions and API access
- **Description:** JSON Web Tokens (JWT) are used to authenticate users and authorize access to protected resources. Tokens are cryptographically signed and contain user claims, ensuring that only authenticated users can access their files and perform authorized actions.

### 4. **Password Hashing**
- **Scope:** User credential protection
- **Description:** User passwords are hashed using strong cryptographic algorithms (bcrypt/argon2) with salt before storage. This ensures that even if the database is compromised, passwords cannot be recovered in plain text.

### 5. **Role-Based Access Control (RBAC)**
- **Scope:** Permission management and access control
- **Description:** Users are assigned specific roles (e.g., admin, user, viewer) with defined permissions. This ensures that users can only perform actions and access resources appropriate to their role, minimizing the risk of unauthorized operations.

### 6. **Password-Protected Files**
- **Scope:** Additional layer of file security
- **Description:** Individual files can be protected with separate passwords, adding an extra security layer beyond user authentication. This allows users to share encrypted files that require specific passwords to decrypt.

### 7. **User Authentication**
- **Scope:** Identity verification and access control
- **Description:** Multi-factor authentication system that verifies user identity through secure login mechanisms. Prevents unauthorized access to the vault system and ensures only legitimate users can access their encrypted files.

### 8. **Input Validation & Sanitization (Zod)**
- **Scope:** Preventing injection attacks and data integrity
- **Description:** All user inputs are validated and sanitized using Zod schema validation. This prevents common vulnerabilities such as SQL injection, XSS (Cross-Site Scripting), and other injection attacks by ensuring only properly formatted data is processed.

### 9. **Activity Logging & Auditing**
- **Scope:** Security monitoring and compliance
- **Description:** Comprehensive logging system that tracks all user activities, file operations, and security events. Provides audit trails for security analysis, incident response, and compliance requirements. Logs include timestamps, user IDs, IP addresses, and action types.

### 10. **Secure Headers & Rate Limiting**
- **Scope:** Application-level security hardening
- **Description:** Implementation of security headers (CSP, HSTS, X-Frame-Options, etc.) to protect against common web vulnerabilities. Rate limiting prevents brute-force attacks and DDoS attempts by restricting the number of requests from a single source within a time window.

## 🚀 Tech Stack

- **Build Tool:** Vite
- **Language:** TypeScript
- **Frontend Framework:** React
- **UI Components:** shadcn-ui
- **Styling:** Tailwind CSS

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/omkardinde04/ShieldDrive.git

# Navigate to project directory
cd ShieldDrive

# Install dependencies
npm install

# Start development server
npm run dev
```

## 🔧 Usage

1. **Sign Up/Login:** Create an account or log in with your credentials
2. **Upload Files:** Select and upload files to your secure vault
3. **Encrypt Files:** Files are automatically encrypted with AES-256
4. **Access Files:** Enter the correct password to decrypt and view your files
5. **Manage Access:** Set role-based permissions for shared files

## 🏗️ Project Structure

```
ShieldDrive/
├── src/
│   ├── components/     # React components
│   ├── lib/           # Utility functions and helpers
│   ├── hooks/         # Custom React hooks
│   ├── pages/         # Application pages
│   └── types/         # TypeScript type definitions
├── public/            # Static assets
└── README.md
```

## 🔒 Security Best Practices

- Never share your master password
- Use strong, unique passwords for file protection
- Regularly review activity logs for suspicious behavior
- Keep your browser and application updated
- Enable two-factor authentication when available

## 📄 License

This project is developed as part of academic coursework at K.J. Somaiya College of Engineering.

## 🤝 Acknowledgments

Special thanks to our CSF Lab instructors for guidance and support throughout this project.

---

**⚠️ Note:** This is an academic project developed for educational purposes. For production use, ensure additional security audits and compliance checks are performed.
