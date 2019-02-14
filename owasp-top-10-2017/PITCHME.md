## OWASP Top 10 - 2017
### What's new?

---?image=owasp-top-10-2017/assets/oak.JPG&opacity=50

@snap[south-east]
@quote[The best time to plant an oak tree<br>was 20 years ago.<br>The next best time is now.](Ancient Proverb)
@snapend

---

## Content

* **About OWASP**  
  What it is. OWASP Projects and Tools.
* **About the Top 10 list**  
  How it was built. How the priorities were assigned.
* **Top 10 - 2013 and 2017 compared**  
  Side-by-side view of the two lists.
* **About the differences**  
  What was changed and why.

---

## OWASP

**Open Web Application Security Project** - since 2001.

Worldwide, not-for-profit charitable organization focused on improving the security of software.

=> unbiased, practical, free and open information.

+++

## OWASP [Projects](https://www.owasp.org/index.php/Category:OWASP_Project#tab=Project_Inventory)

* [Top 10 risks](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project);
* [Cheat sheets](https://www.owasp.org/index.php/OWASP_Cheat_Sheet_Series);
* [Checklists](https://www.owasp.org/images/0/08/OWASP_SCP_Quick_Reference_Guide_v2.pdf);
* Guides: [Development guide](https://www.owasp.org/index.php/OWASP_Guide_Project#tab=Main), [Testing guide](https://www.owasp.org/index.php/OWASP_Testing_Project);
* [Code Review Guide](https://www.owasp.org/index.php/Category:OWASP_Code_Review_Project);
* [Proactive controls](https://www.owasp.org/index.php/OWASP_Proactive_Controls#tab=OWASP_Proactive_Controls_2016);
* [Tools overview](https://www.owasp.org/index.php/Category:OWASP_Tools_Project), e.g. [Vulnerability Scanning Tools](https://www.owasp.org/index.php/Category:Vulnerability_Scanning_Tools).

+++

## OWASP tools

* [Zed Attack Proxy](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project): automatically finds security vulnerabilities in web apps;
* [Dependency Check](https://www.owasp.org/index.php/OWASP_Dependency_Check): identifies project dependencies & known vulnerabilities.
* [Security Shepherd](https://www.owasp.org/index.php/OWASP_Security_Shepherd): security training platform: lessons & challenges;
* [WebGoat](https://www.owasp.org/index.php/Category:OWASP_WebGoat_Project): deliberately insecure web app;

Note:
* Dependency Check: identifies project dependencies and checks if there are any known, publicly disclosed vulnerabilities;
* WebGoat: deliberately insecure web app designed to teach web app security lessons. Not yet production ready, but ready for mainstream usage;

---

## Content

* <span style="color:Grey;">**About OWASP**  
  What it is. OWASP Projects and Tools.</span>
* **About the Top 10 list**  
  How it was built. How the priorities were assigned.
* <span style="color:Grey;">**Top 10 - 2013 and 2017 compared**  
  Side-by-side view of the two lists.</span>
* <span style="color:Grey;">**About the differences**  
  What was changed and why.</span>

---

## Top 10 - 2017
#### How it was built

* Source: 
  * **40+ data submissions** from firms that specialize in application security (e.g.consulting companies)
  * Industry survey completed by over 500 individuals.
* This data spans **hundreds of organizations** and over **100,000 real-world applications and APIs**.

All data is [publicly available](https://github.com/OWASP/Top10/blob/master/2017/datacall/OWASP%20Top%2010%20-%202017%20Data%20Call-Public%20Release.xlsx?raw=true)!!!

+++ 

## Top 10 - 2017
#### How the priorities were assigned

@snap[north]
Top 10 items are selected and prioritized according to:
* prevalence (based on data) &
* exploitability, detectability and impact (based on consensus estimates).
@snapend

@snap[south]
![formula](owasp-top-10-2017/assets/formula.JPG)
@snapend

---

## Content

* <span style="color:Grey;">**About OWASP**  
  What it is. OWASP Projects and Tools. </span>
* <span style="color:Grey;">**About the Top 10 list**  
  How it was built. How the priorities were assigned. </span>
* **Top 10 - 2013 and 2017 compared**  
  Side-by-side view of the two lists.
* <span style="color:Grey;">**About the differences**  
  What was changed and why.</span>

---

## Diff 2013 - 2017

![diff](owasp-top-10-2017/assets/diff2.JPG)

---

## Content

* <span style="color:Grey;">**About OWASP**  
  What it is. OWASP Projects and Tools.</span>
* <span style="color:Grey;">**About the Top 10 list**  
  How it was built. How the priorities were assigned.</span>
* <span style="color:Grey;">**Top 10 - 2013 and 2017 compared**  
  Side-by-side view of the two lists.</span>
* **About the differences**  
  What was changed and why.

---

## Differences in depth

* Merged 
  * 2013-A4: Insecure Direct Object References and
  * 2013-A7: Missing Function Level Access Control back into
  * 2017-A4: Broken Access Control.

Split in 2007, to bring more attention to each half of the access control problem (data and functionality). No longer considered that necessary.

+++

## Differences in depth

Added 2017-A7: [Insufficient Attack Protection](https://www.owasp.org/index.php/Top_10_2017-A7-Insufficient_Attack_Protection)

Because:
* Data => lack of basic capabilities to detect/prevent/respond to manual/automated attacks.

Suggestions:
* Apps should automatically detect and ban/logout/disable attackers;
* Deploy patches quickly to block attacks.

+++

## Differences in depth

Added 2017-A10: [Underprotected APIs](https://www.owasp.org/index.php/Top_10_2017-A10-Underprotected_APIs)

Because:
* "The use of APIs has exploded in modern software": e.g. SOAP/XML, REST/JSON, RPC, GWT, etc.
* These APIs are often unprotected and contain numerous vulnerabilities.

Additional info: [Reddit debate](https://www.reddit.com/r/netsec/comments/64pou3/owasp_top_10_2017_release/) on this risk.

+++ 

## Differences in depth

Removed 2013-A10: [Unvalidated Redirects and Forwards](https://www.owasp.org/index.php/Top_10_2013-A10-Unvalidated_Redirects_and_Forwards)

Because:
* Added in 2010 to raise awareness of this problem;
* Data shows that this issue isn’t as prevalent as expected.

---

## Instead of conclusion

![risks](owasp-top-10-2017/assets/risks2.JPG)

---

## Thank you! 


Note:
Sonar cube!

