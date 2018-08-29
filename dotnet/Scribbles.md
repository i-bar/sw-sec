### 1. SQLi

1. Parameterized queries
2. ORMs
3. Different users with different access rights in the DB


### 2. Broken Authentication

1. Cookieless approach is BAD - DO use cookies, DO NOT rely on session state.
2. Http-only cookies
3. Session expiration time 
4. Encrypt passwords - both at rest and in transit
5. Enforce strong passwords
6. Reset password - do not email it.
7. Disable the 'remember me' checkbox and functionality.
8. Disable auto-completion on login fields (e.g. username)


### 3. Sensitive Data Exposure

1. Encrypt data at rest & in transit
2. Use strong hashing algorythms with salt:
   * Weak algorithms: MD5, SHA1
   * Strong: Argon2, PBKDF2, bcrypt, scrypt
   * **Salt** protects against hash tables and rainbow tables
   * **Slow algorythms** protect against brute force attacks  
3. Use strong encryption algorythms:
   * DES is to be avoided and so is RSA-768, -1024
   * RSA-2048 and RSA-3072 are acceptable
   * AES-CBC mode is acceptable, while
   * AES-GCM mode is part of the Next Generation Encription.
4. Secure keys:
   * Protect keys;
   * Do not reuse keys and IVs (Initialisation Vectors)
   * Q: HOW? WHERE?

