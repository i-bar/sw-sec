## OWASP-2017
### What's new?

---

## Content

* **About OWASP**  
  What it is. The OWASP Projects.
* **About the Top 10 list**  
  How it was built. How the priorities were assigned.
* **Top 10 - 2013 and 2017 compared**
* **About the differences**

---

## OWASP

Open Web Application Security Project - since 2001.

Worldwide, not-for-profit charitable organization focused on improving the security of software.

=> unbiased, practical, free and open information.

+++

## OWASP [Projects](https://www.owasp.org/index.php/Category:OWASP_Project#tab=Project_Inventory)

* [Top 10 vulnerabilities](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project);
* [Cheat sheets](https://www.owasp.org/index.php/OWASP_Cheat_Sheet_Series);
* [Checklists](https://www.owasp.org/images/0/08/OWASP_SCP_Quick_Reference_Guide_v2.pdf);
* Guides: [Development guide](https://www.owasp.org/index.php/OWASP_Guide_Project#tab=Main), [Testing guide](https://www.owasp.org/index.php/OWASP_Testing_Project);
* [Proactive controls](https://www.owasp.org/index.php/OWASP_Proactive_Controls#tab=OWASP_Proactive_Controls_2016);
* [Tools](https://www.owasp.org/index.php/Category:OWASP_Tools_Project), e.g. [Vulnerability Scanning Tools](https://www.owasp.org/index.php/Category:Vulnerability_Scanning_Tools).

+++

## OWASP tools

* [Zed Attack Proxy](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project): automatically finds security vulnerabilities in web apps;
* [Dependency Check](https://www.owasp.org/index.php/OWASP_Dependency_Check): identifies project dependencies & known vulnerabilities.
* [Security Shepherd](https://www.owasp.org/index.php/OWASP_Security_Shepherd): security training platform;
* [WebGoat](https://www.owasp.org/index.php/Category:OWASP_WebGoat_Project): deliberately insecure web app;

Note:
* [Zed Attack Proxy](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project): automatically finds security vulnerabilities in web apps;
* [Dependency Check](https://www.owasp.org/index.php/OWASP_Dependency_Check): identifies project dependencies and checks if there are any known, publicly disclosed vulnerabilities;
* [Security Shepherd](https://www.owasp.org/index.php/OWASP_Security_Shepherd): security training platform for web and mobile apps;
* [WebGoat](https://www.owasp.org/index.php/Category:OWASP_WebGoat_Project): deliberately insecure web app designed to teach web app security lessons. Not yet production ready, but ready for mainstream usage;


---

## Content

* <span style="color:LightGrey;"> **OWASP**: What it is. What it does. </span>
* **Top 10**:  What it is based on. How they are prioritized.
* <span style="color:LightGrey;"> **diff 2017 2013**. </span>
* <span style="color:LightGrey;"> **2017 in-depth**. </span>

---

## Top 10, 2017
### The data

* Source: **11 large datasets** from firms that specialize in application security (e.g.consulting companies)  
* This data spans **hundreds of organizations** and over **50,000 real-world applications and APIs**.

All data is [publicly available](https://github.com/OWASP/Top10/blob/master/2017/datacall/OWASP%20Top%2010%20-%202017%20Data%20Call-Public%20Release.xlsx?raw=true)!!!

+++ 

## Top 10, 2017
### The priorities

Top **10** items are selected and prioritized according to:
* prevalence (based on data) &
* exploitability, detectability and impact (based on consensus estimates).

---

## Diff 2017 - 2013

![diff](owasp-2017/assets/diff.JPG)

---

## In depth 1

Merged 
* 2013-A4: Insecure Direct Object References and
* 2013-A7: Missing Function Level Access Control back into  
2017-A4: Broken Access Control.

Split in 2007, to bring more attention to each half of the access control problem (data and functionality). No longer considered that necessary.

+++

## Novelties in depth

Added 2017-A7: [Insufficient Attack Protection](https://www.owasp.org/index.php/Top_10_2017-A7-Insufficient_Attack_Protection)

Because:
* Data => the majority of applications and APIs lack basic capabilities to detect, prevent, and respond to both manual and
automated attacks.  
* Application and API owners also need to be able to deploy patches quickly to protect against attacks.

Suggestions:
* Apps should automatically detect and ban/logout/disable attackers;
* Deploy patches quickly to block attacks.


+++

## Novelties in depth

Added 2017-A10: [Underprotected APIs](https://www.owasp.org/index.php/Top_10_2017-A10-Underprotected_APIs)

Because:
* "the use of APIs has exploded in modern software": e.g. SOAP/XML, REST/JSON, RPC, GWT, etc.
* These APIs are often unprotected and contain numerous vulnerabilities.

Additional info: [Reddit debate](https://www.reddit.com/r/netsec/comments/64pou3/owasp_top_10_2017_release/) on this risk.


+++ 

## Novelties in depth

Removed 2013-A10: [Unvalidated Redirects and Forwards](https://www.owasp.org/index.php/Top_10_2013-A10-Unvalidated_Redirects_and_Forwards)

Because:
* Added in 2010 to raise awareness of this problem;
* Data shows that this issue isn’t as prevalent as expected.

---

## Instead of conclusion

![risks](owasp-2017/assets/risks.JPG)


