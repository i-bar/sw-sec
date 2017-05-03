Practical SW Security

---

The **WHO?** the **WHY?** and the **HOW?** -s for:

1. Input validation.
2. Output encoding.
3. Authentication.
4. Authorisation.
5. Error handling and logging.
6. Session management and communication security.

---

## Resources

[OWASP proactive controls](https://www.owasp.org/index.php/OWASP_Proactive_Controls#tab=OWASP_Proactive_Controls_2016)
[OWASP top 10 threats](https://www.owasp.org/index.php/Top_10_2013-A1-Injection)
[OWASP secure practices checklist](https://www.owasp.org/images/0/08/OWASP_SCP_Quick_Reference_Guide_v2.pdf)

---

### Input validation: the WHO?

Any application that accepts any data directly entered by, or influenced by, users.
Input data:
 * HTTP headers;
 * Cookies;
 * GET and POST parameters (including hidden fields);
 * File uploads (including information such as the file name)
 * Database data.

---

### Input validation: the WHY?

Attacks & examples:
 * [SQL Injection](https://www.owasp.org/index.php/Top_10_2013-A1-Injection): attacker executes unauthorized queries on the database.
[TBR](https://teammentor.net/angular/user/article/48a2190c895f/SQL-Injection)
 * [XSS - Cross Site Scripting](https://www.owasp.org/index.php/Top_10_2013-A3-Cross-Site_Scripting_(XSS)): attacker includes malicious scripts in the web app. output (the web page). The browser executes the script.
[TBR](https://teammentor.net/angular/user/article/34a6fa70da68/Cross-Site-Scripting)
 * YOU ARE HERE

It happens for greater houses?
 * [Adobe](https://arstechnica.com/security/2012/11/adobe-breach-reportedly-spills-easy-to-crack-password-hashes)
 * [eHarmony](http://mashable.com/2012/06/06/eharmony-passwords-stolen/#lPddW5ZTV5qq)
 * [LinkedIn](http://money.cnn.com/2012/06/06/technology/linkedin-password-hack/index.htm)
 * [Yahoo!](https://en.wikipedia.org/wiki/2012_Yahoo!_Voices_hack)
 


---

### Input validation: Resources
 * [OWASP Data Validation](https://www.owasp.org/index.php/Data_Validation)
 * [OWASP Attacks: Injection](https://www.owasp.org/index.php/Top_10_2013-A1-Injection)
 * [OWASP ]

