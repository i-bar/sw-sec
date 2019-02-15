## OWASP Top 10 - 2017
### Compared to 2013

---

### Content

* **About OWASP**  
  What it is. OWASP Projects and Tools.
* **About the Top 10 list**  
  How it was built. How the priorities were assigned.
* **Top 10 2017: Overview**
  Risk factor summary for every 2017 Application Security Risk.
* **Top 10 2013 / 2017: similarities**  
  What remained and why.
* **Top 10 2013 / 2017: differences**  
  What has changed and why.

---

@snap[north]
### OWASP
@snapend

@snap[west span-70]
@ul[](false)
* Worldwide, not-for-profit charitable organization focused on improving the security of software.
* => unbiased, practical, free and open information.
* Online since 2001, not-for-profit charitable organization since 2004.
@ulend
@snapend

@snap[east span-30]
![OWASP](owasp-top-10-2017/assets/owasp-logo.png)
@snapend

+++

### OWASP [Projects](https://www.owasp.org/index.php/Category:OWASP_Project#tab=Project_Inventory)

* [Top 10 risks](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project);
* [Cheat sheets](https://www.owasp.org/index.php/OWASP_Cheat_Sheet_Series);
* [Checklists](https://www.owasp.org/images/0/08/OWASP_SCP_Quick_Reference_Guide_v2.pdf);
* Guides: [Development guide](https://www.owasp.org/index.php/OWASP_Guide_Project#tab=Main), [Testing guide](https://www.owasp.org/index.php/OWASP_Testing_Project);
* [Code Review Guide](https://www.owasp.org/index.php/Category:OWASP_Code_Review_Project);
* [Proactive controls](https://www.owasp.org/index.php/OWASP_Proactive_Controls#tab=OWASP_Proactive_Controls_2016);
* [Tools overview](https://www.owasp.org/index.php/Category:OWASP_Tools_Project), e.g. [Vulnerability Scanning Tools](https://www.owasp.org/index.php/Category:Vulnerability_Scanning_Tools).

+++

### OWASP tools

* [Zed Attack Proxy](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project): automatically finds security vulnerabilities in web apps;
* [Dependency Check](https://www.owasp.org/index.php/OWASP_Dependency_Check): identifies project dependencies & known vulnerabilities.
* [Security Shepherd](https://www.owasp.org/index.php/OWASP_Security_Shepherd): security training platform: lessons & challenges;
* [WebGoat](https://www.owasp.org/index.php/Category:OWASP_WebGoat_Project): deliberately insecure web app;

Note:
* Dependency Check: identifies project dependencies and checks if there are any known, publicly disclosed vulnerabilities;
* WebGoat: deliberately insecure web app designed to teach web app security lessons. Not yet production ready, but ready for mainstream usage;

---

### OWASP Top 10
#### How it was built

* Source: 
  * **40+ data submissions** from firms that specialize in application security (e.g.consulting companies)
  * Industry survey completed by over 500 individuals.
* This data spans **hundreds of organizations** and over **100,000 real-world applications and APIs**.

All data is [publicly available](https://github.com/OWASP/Top10/blob/master/2017/datacall/OWASP%20Top%2010%20-%202017%20Data%20Call-Public%20Release.xlsx?raw=true)!!!

+++ 

@snap[north]
### OWASP Top 10
#### How the priorities were assigned
@snapend

@snap[west-midpoint-east]
Top 10 items are selected and prioritized according to:

@ul[](false)
* prevalence (based on data) &
* exploitability, detectability and impact (based on consensus estimates).
@ulend

@snapend

@snap[south-east span-50]
![formula](owasp-top-10-2017/assets/formula.JPG)
@snapend

---

### Top 10 2017: overview

![overview](owasp-top-10-2017/assets/overview.JPG)

+++

### diff (2013, 2017)

![diff](owasp-top-10-2017/assets/diff.JPG)

+++

### Why the changes?

* Microservices are replacing traditional monolythic applications.  
  * Old code never expected to be accessible from the Internet is now sitting behind an API or RESTful web service.
* Single page applications, written in JavaScript frameworks such as Angular and React, allow the creation of highly modular feature-rich front ends.  
  * Client-side functionality that has traditionally been delivered server-side brings its own security challenges.

---

#### What remained
### A1 - Injection
* Occurs when an attacker sends hostile data to an interpreter.
* E.g. SQL Injection:  
  `String query = "SELECT * FROM accounts WHERE custID='" + request.getParameter("id") + "'";`  
  where id = `' or '1'='1`
* **Possible solution**: Parameterized queries

+++

#### What remained
### A2 - Broken Authentication
* Incorrectly configured user and session authentication;
* Attacker can compromise passwords, keys, or session tokens, or take control of users’ accounts to assume their identities.
* **Possible Solution**: Multi-factor authentication

+++

#### What remained
### A3 - Sensitive Data Exposure (prev. A6 in 2013)
* Sensitive data such as financial data, usernames and passwords, or health information that is not properly protected;
* Attacker can access such information to commit fraud or steal identities.
* **Possible Solution**: Encryption of data at rest and in transit

+++

#### What remained
### A6 - Security misconfiguration (prev. A5 in 2013)
* Insecure default configurations, misconfigured HTTP headers, verboise error messages containing sensitive information, systems / frameworks or components that are not upgrades, etc.
* **Possible Solution**: Keep systems / frameworks / libraries / applications properly configured and up to date.

+++

#### What remained
### A7 - Cross-Site Scripting (prev. A3 in 2013)
* Attackers can execute scripts in the victim's browser;
* Hijack user sessions, redirect users to malicious sites etc.
* **Possible Solution**: Data encoding, input validation.

+++

#### What remained
### A9 - Using components with known vulnerabilities
* Components, such as libraries, frameworks, and other software modules, run with the same privileges as the application.
* Possible outcomes: serious data loss or server takeover.
* **Possible Solution**: Conduct software composition analysis.

---

#### What has changed
### A4 - XML External Entities (XXE) - **NEW***
* Poorly configured XML processors evaluate external entity references within XML documents.
* Attacks include remote code execution, and to disclose internal files.
* E.g. An attacker attempts a denial-of-service attack by including a potentially endless file:  
  `<!ENTITY xxeSYSTEM "file:///dev/random" >]>`
* **Possible Solution**: Whenever possible, use JSON. Patch / update XML processors.

+++

#### What has changed
### A5 - Broken access control - *MERGED*
* Merged 
  * 2013-A4: Insecure Direct Object References and
  * 2013-A7: Missing Function Level Access Control back into
* Split in 2007, to bring more attention to each half of the access control problem (data and functionality). No longer considered that necessary.
* **Cause**: Improperly configured or missing restrictions on authenticated users
* **Effect**: Users can them to access unauthorized functionality or data, such as accessing other users’ accounts, viewing sensitive documents, and modifying data and access rights.
* **Possible solution**: Deny by default. Pentesting.

+++

#### What has changed
### A8 - Insecure deserialization - *NEW*
* Leads to remote code execution, injection attacks, privilege escalation attacks;
* **Possible solutions**: Do not accept serialized content from untrusted sources, or use serialization mediums that only permit primitive types.

+++

#### What has changed
### A10 - Insufficient logging & monitoring - *NEW*
* Owasp: *"Most breach studies show time to detect a breach is over 200 days, typically detected by external parties rather than internal processes or monitoring."*
* **Possible causes**: Critical events (logins, failed logins, high-value transactions) are not logged.
* **Possible solution**: Think like an attacker and use pen testing. Examine logs after pen testing.

+++

#### What has changed
### Cross-site request forgery (CSRF) - *REMOVED*
* Found in only 5% of the applications;
* Many frameworks include CSRF defenses.

### Unvalidated redirects and forwards - *REMOVED*
* Although found in 8% of the application;
* Edged out overall by XXE.

---?image=owasp-top-10-2017/assets/oak.JPG&opacity=50

## Thank you! 

@snap[south-east]
@quote[The best time to plant an oak tree<br>was 20 years ago.<br>The next best time is now.](Ancient Proverb)
@snapend
