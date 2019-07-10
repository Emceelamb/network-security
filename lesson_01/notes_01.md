# Lesson 01
##  Introduction to Network Security
* Cyber security requires you to think differently than other cs fields
* There are many ways to compromise a database
* There is no 100% secure system

> The network has been designed so as to maintain an acceptable level risk.
* Security is an engineering trade off
* Security is an ongoing process
  * Threats are always shifting
> Security is primarily about risk management

#### Wired Hack
Flow chart 
Twitter > Gmail > Me.com > Amazon

### NetSec Terminology
* Alice and Bob are Good Guys
* Trudy is baddy. Short for "Intruder"
* CIA 
  * Confidentiality - keeping info secret
  * Integrity - Ensure info is genuine
  * Availability - Ensure system is avaiable
* Authenticity - Determine origin of data; Type of integrity
* Non-Repudiation - proving integrity and origin; Reputability
* **Risk** is something off value that cacn lose value
* **Threat** is something that could occur that has adverse effect on the assets 
* **Vulnerability** characteristic that makes threat possible
* ** Attack (Exploit)** an action that involves exploitation of some vulnerability
* **Transfer** make it someone elses problem 
* **Acceptance** residual risk of injury

### Vulnerabilities

### Asset Owner vs IT Asset Owner
* Owner of asset may not be owner of the related IT asset at risk
  * Online shop owner can own assets
  * Run service on AWS
  * Amazon is IT asset owner

### Risk Assessment
* Quantitative vs Qualitative
* **Quantitative**:
  * EF Percentage  of asset caused by threat
  * Single Loss Expectancy = Asset Value X Exposure Factor
  * Annualized Rate of Occurrence = Estimated frequency a threat will occur in one year
  * Annualized Loss Expectance (ALE) = SLE x ARO
* Quantitative is better than qualiltative
* Generally Cyber Security Insurance is not reliable but is a growiing field
* **Qualitative**
  * Risk Matrix
  * Subjective

### Understanding Attack Trees

### Exercise
Suppose you have a db with a pw. What are some ways to "hack" into the account? That is how would you figure out the username/ password?
* You can brute force the password.
* You can look up default administrator privileges.
* You can social engineer it.
* You can try defaults.
* You try to reset password.

Who's at fault for Mat Holen's loss of everything?
The services that were compromised included: Apple, Twitter, Amazon, Gmail. I think Mat Holen is ultimately responsible for not setting up a private domain. 

Give an example of threats, risks, vulnerabilities, and exploits.
Threat can be a potential employer.
Risk is them not hiring me.
A vulnerability is my social media.
Exploit could be following my private instagram account to see my posts.

Exercise 4
An employee loses a laptop with customer data at the airport. How would you mitigate it? Whats the residual risk?

I would put it at consequence: 5, Likelihood: 3
You can do a full disk encryption on the harddrive. This reduces the likelihood that the data can be breached.

