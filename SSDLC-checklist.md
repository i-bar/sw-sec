## SSDLC CheckList

---

Motto:

_The best time to plant an oak tree was 20 years ago._  
_The next best time is now._  
– Ancient Proverb

---

### Overview
1. Secure Requirements
2. Secure Architecture
3. Secure Design
4. Secure Coding
5. Secure Testing

---

### 1. Secure requirements: CIA

#### Confidentiality
**Authentication**: Define an *Access Control Matrix* (aka. Trust Model or Security Policy)  
_WHO_ can perform _WHAT_ actions on _WHICH_ resources.
- Are there any sensitive resources? Which? (functional operations and data items: users & passwords? xmls?)  
Define Resource Classes, e.g.
    - Customer account records (personal information of value);
    - DB entries that, if maliciously changed, could harm the business;
    - Business operations on customer records; needs to be controlled to protect data access & integrity;
- What are the classes of "Principals" who need access to the resources? Role & types of access they require.  
  E.g. Data administrator; Customer care clerk; Registered customer; Unknown website user.
- What are the Access Control Sets?  
  For each Resource Class, what are the operation that can be performed on members of that class? What are the Principal Classes that should be allowed to access each operation on the class?

---

#### Information integrity requirements? (Anti-Corruption and Origin Authenticity) 
- What are the situations in the system where information is or could be changed?
- What set of integrity guarantee is required for that information?
- Solution e.g. cryptography.

---

#### Availability requirements?
Protect against DoS attacks, e.g. force an user to be locked out by repeatedly using an incorrect pwd, network attacks using custom software that overloads systems, etc.

---

#### Source

[Software Systems Architecture](https://www.amazon.com/Software-Systems-Architecture-Stakeholders-Perspectives/dp/032171833X)

---

### 2. Secure architecture

#### Sources: 
* [Software Systems Architecture](https://www.amazon.com/Software-Systems-Architecture-Stakeholders-Perspectives/dp/032171833X)
* [OWASP Architecture Principles](https://www.owasp.org/index.php/Category:Principle)

---

#### Apply Security principles:
- Grant the **least amount of priviledge** possible;
- Identify and secure the **weakest link** (e.g. technological - an unsecured network link; procedural - allow access to a data center; human - people who write down their passwords);
- **Separation of Concerns**: Separate different related responsibilities so that authority for each can be assigned to different principals if required. E.g. implement separate security configuration and mechnisms for each major subdivision of a system (?);
- Keep security designs **simple**: _"Complexity is the enemy of security"_;
- **Don't rely on obscurity**. Instead, assume the potential attackers know the system as well as its implementers do;
- Use **secure defaults**. E.g. avoid empty default passwords, permissive default access control lists, network ports open by default etc;
- **Fail securely** (confidentiality and integrity of a system should remain even if availability was lost): ensure a failure follows the same path as disallowing an operation;
- **Assume external entities are untrusted**;
- **Audit sensitive events**, e.g: pwd reset, assign powerful roles, etc.
- Apply **defense in depth**: use layered security mechanisms to increase security of the system as a whole. 

---

#### Threat modelling:
- Identify threats:
  - Who is likely to try to infringe the security policy?
  - How will they try to do so?
  - What are the atacker's main characteristics? (motivation, resources, sophistication etc)
  - What are the consequences of the policy being breached in this way?
- Adopt a weighting system for measurement of threats;
- Build the attack tree. Example on next slide.

---

> Here is a possible attack tree for the goal of extracting customer credit
card details from an e-commerce Web site.  
> Goal: Obtain customer credit card details.  
> 1. Extract details from the system database.  
	1.1. Access the database directly.  
    1.1.1. Crack/guess database passwords.  
    1.1.2. Crack/guess operating system passwords that allow database security to be bypassed.  
	1.2. Access the details via a member of the database administration staff.  
		1.2.1. Bribe a database administrator (DBA).  
		1.2.2. Conduct social engineering by phone/e-mail to trick the DBA into revealing details.	
> 2. Extract details from the Web interface.  
	2.1. Set up a dummy Web site and e-mail users the URL to trick them into entering credit card details.  
	2.2. Crack/guess passwords for user accounts and extract details from the user Web interface.  
	2.3. Send users a Trojan horse program by e-mail to record keystrokes/intercept Web traffic.  
	2.4. Attack the domain name server to hijack the domain name and use the dummy site attack from 2.1.  
	2.5. Attack the site server software directly to try to find loopholes in its security.  
> 3. Find details outside the system.  
	3.1. Conduct social engineering by phone/e-mail to get customer services staff to reveal card details.  
	3.2. Direct a social-engineering attack on users by using public details from the site to make contact.  

Source: [Software Systems Architecture](https://www.amazon.com/Software-Systems-Architecture-Stakeholders-Perspectives/dp/032171833X)

---

#### Random:
* Use as much 3rd party security technology as possible;
* Detection and Recovery: (because security breaches are inevitable...)
  - How do we detect breaches?
  - How do we recover from them?

---

### 3. Secure Design 

#### Sources:
* [OWASP Design Review Activities](https://www.owasp.org/index.php/SAMM_-_Design_Review_-_1)
* [OWASP Design Review Methodology](https://www.owasp.org/index.php/OWASP_Secure_Application_Design_Project#tab=Methodology_of_Design_Review)

---

#### Secure Design Activities
* Identify software attack surface
* Analyze design against known security requirements
* Inspect for complete provision of security mechanisms
* Deploy design review service for project teams
* Develop data-flow diagrams for sensitive resources;
* Establish release gates for design review

---

#### Design Review Checklist
* Data Flow
	- Are user inputs used to directly reference a business logic class/function?
	- Is there a data binding flaw?
	- Does it expose any backdoor parameter to invoke business logic?
	- Is the execution flow of the application correct?
* Authentication and access control
	- Does the design implement access control for all the files?
	- Does it handle session securely?
	- Is there SSO, does it leave any backdoor?
* Existing/built-in Security Controls
	- Weakness in any existing security control?
	- Is the placement of the security controls correct?
* Architecture
	- Is there validation for all input sources?
	- Is the connection to external servers secure?
* Configuration/code files and datastores
	- Are sensitive data present in configuration files?
	- Does it support any insecure data source?

---

### 4. Secure Coding

Resource: [OWASP Secure Coding Practices Checklist](https://www.owasp.org/index.php/OWASP_Secure_Coding_Practices_Checklist)

---

### 5. Security testing

Resources:
* [Mozilla Secure QA Checklist](https://wiki.mozilla.org/WebAppSec/Secure_Coding_QA_Checklist)
* [OWASP Secure Testing Cheat Sheets](https://www.owasp.org/index.php/Web_Application_Security_Testing_Cheat_Sheet)

