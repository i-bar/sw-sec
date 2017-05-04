Practical SW Security

---

The **WHO?** the **WHY?** and the **HOW?** -s for:

1. Application Input and Output.
2. Authentication.
3. Authorisation.
4. Error handling and logging.
5. Session management and communication security.
Sensitive data?

---

## Resources

[OWASP proactive controls](https://www.owasp.org/index.php/OWASP_Proactive_Controls#tab=OWASP_Proactive_Controls_2016)
[OWASP top 10 threats](https://www.owasp.org/index.php/Top_10_2013-A1-Injection)
[OWASP secure practices checklist](https://www.owasp.org/images/0/08/OWASP_SCP_Quick_Reference_Guide_v2.pdf)
[OWASP cheat sheets](https://www.owasp.org/index.php/OWASP_Cheat_Sheet_Series)
[Mozilla Security QA Checklist](https://wiki.mozilla.org/WebAppSec/Secure_Coding_QA_Checklist)

---

### Application Input and Output: the WHO?

Any application that accepts data directly entered by, or influenced by, users.
Input data can be:
 * HTTP headers;
 * Cookies;
 * GET and POST parameters (including hidden fields and "resistant" fields such as radio buttons or drop down lists);
 * File uploads (including information such as the file name)
 * Database data.

Any application that includes user input in the application output:
 * Input that is immediately echoed back (e.g. search engine re-displays the searched string);
 * Input that is stored first (e.g. in a database) and echoed back later (e.g. profile or status messages).

---

### Application Input and Output: the WHY?

Attacks & examples:
 * [SQL Injection](https://www.owasp.org/index.php/Top_10_2013-A1-Injection): attacker executes unauthorized queries on the database.
   [XKCD: Little Bobby Tables](https://www.xkcd.com/327/)
 * [XSS - Cross Site Scripting](https://www.owasp.org/index.php/Top_10_2013-A3-Cross-Site_Scripting_%28XSS%29): attacker input (e.g. malicious scripts) included in the web app output (the web page). The browser executes the scripts.  
   [XKCD: HeartBleed bug](https://xkcd.com/1354/)

It happens for greater houses?
 * [OpenSSL Heartbleed](http://heartbleed.com/)
 * [Adobe](https://arstechnica.com/security/2012/11/adobe-breach-reportedly-spills-easy-to-crack-password-hashes)
 * [eHarmony](http://mashable.com/2012/06/06/eharmony-passwords-stolen/#lPddW5ZTV5qq)
 * [LinkedIn](http://money.cnn.cnom/2012/06/06/technology/linkedin-password-hack/index.htm)
 * [Yahoo!](https://en.wikipedia.org/wiki/2012_Yahoo!_Voices_hack)

---

### Application Input and Output: the HOW?

 * Use white-list validation, validate input **length, range, format and type**:  
   E.g. [Spring](https://spring.io/guides/gs/validating-form-input/), [Spring MVC](http://www.journaldev.com/2668/spring-validation-example-mvc-validator), [java.util.Scanner](https://docs.oracle.com/javase/8/docs/api/java/util/Scanner.html), regular expressions.
 * Validate data passed to the database:  
   E.g. [Parameterized Queries](https://www.owasp.org/index.php/Query_Parameterization_Cheat_Sheet)
 * Encode all input included in output.  
   E.g. [Untrusted HTML](https://www.owasp.org/index.php/XSS_%28Cross_Site_Scripting%29_Prevention_Cheat_Sheet#XSS_Prevention_Rules_Summary)
   [OWASP Java Encoder](https://www.owasp.org/index.php/OWASP_Java_Encoder_Project#tab=Use_the_Java_Encoder_Project); [Java URL Encoder](https://docs.oracle.com/javase/7/docs/api/java/net/URLEncoder.html)
   
 * [And](https://www.owasp.org/images/0/08/OWASP_SCP_Quick_Reference_Guide_v2.pdf). [Many](https://www.owasp.org/index.php/Input_Validation_Cheat_Sheet). [More](https://wiki.mozilla.org/WebAppSec/Secure_Coding_QA_Checklist#Test:_Input_Validation_For_User_Controlled_Data)...

---

### Authentication: the WHO?

Keywords: login, logout, passwords management, timeouts, remember me, secret question, account update, etc.
Functionality:
 * Create new users;
 * Modify existing users;
 * Change credentials for existing users (e.g. pwd reset;
 * Retrieve information related to existing users (e.g. recover pwd);
 * Remove existing users;
 * Authenticate users.

---

### Authentication: the WHY?

[OWASP Authentication](https://www.owasp.org/index.php/Top_10_2013-A2-Broken_Authentication_and_Session_Management) threat impact: SEVERE. See examples.  
Attacker can impersonate a priviledged account.

Attacks:
 * [Dictonary attacks](https://en.wikipedia.org/wiki/Dictionary_attack): based on trying all strings in a pre-arranged listing.  
 It works because... [most common passwords](https://www.regencyitc.co.uk/content-type/latest-news/interesting-password-statistics-from-2014/)
 * [Brute force attack](https://en.wikipedia.org/wiki/Brute-force_attack): all possible passwords are systematically checked.
 Works because, e.g. 5 letter passwords are cracked [instantly](http://lastbit.com/rm_bruteforce.asp)
 * [Login spoofing](https://en.wikipedia.org/wiki/Login_spoofing): malicious program (Trojan) simulates an ordinary-looking login page.

---

### Authentication: the HOW?

 * [Java Authentication and Authorisation Service](https://docs.oracle.com/javase/8/docs/technotes/guides/security/jaas/JAASRefGuide.html)
 * [Spring Security Authentication](http://docs.spring.io/spring-security/site/docs/4.2.0.RC1/apidocs//org/springframework/security/core/Authentication.html)

Checklists:
 * [OWASP quick reference: Authentication](https://www.owasp.org/images/0/08/OWASP_SCP_Quick_Reference_Guide_v2.pdf)
 * [OWASP authentication cheat sheet](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)

Preview:
 * Implement proper password strength controls;
 * Implement secure password recovery mechanism;
 * Store passwords in a secure fashion (e.g. bcrypt);
 * Transmit pwds only over TLS or other strong transport;
 * Require re-authentication for sensitive features;
 * Implement pwd lockout or multifactor (prevents Brute Force);
 * Use multi-factor authentication (sth they know + own + are);
 * Implement secure pwd recovery mechanism...

---

### Authentication: the... BONUS

[XKCD password strength](https://www.xkcd.com/936/)
[Has your account been compromised?](https://haveibeenpwned.com/)

