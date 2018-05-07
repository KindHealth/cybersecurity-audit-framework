## 5.3 Social Engineering Penetration Testing

More often than not, the human factor is the weakest link in an organization’s overall security posture. Therefore it is essential to test the susceptibility of the organization employees to social engineering schemes. "Social engineering is the ‘art’ of utilizing human behavior to breach security without the participant (or victim) even realizing that they have been manipulated." (Source)

This section lays out the process for testing the organization’s resilience against three primary social engineering attack vectors:

1. Phone-Based Attacks

2. Physical Attacks

3. Virtual Attacks

It is meant to compliment the Social Engineering Table (also part of this framework) with more precise details and analysis.

### 5.3.1 Phone-based Attacks

Phone calls are a common method used by the attackers to deceive organization’s employees into divulging valuable information such as usernames, passwords, and other proprietary information.

A penetration test can be conducted using the following steps:

**5.3.1.1  Preparing for the Test**

This section outlines the information that the tester should prepare prior to making the phone call.  The data collection process should be driven by the following questions:

1. **What are the attack goals?**

The tester must clearly define the goals of the attack. For example, the goal of the attack could be to gather information such as:

* Username

* Password

* Password reset

* Proprietary information

* Customer information

* Divulgence of information that would violate standards such as: HIPAA, or PCI

Or to entice the target to perform some action such as resetting the password of the legitimate employee. The specific goals will inform the tactics that should be followed during the call.

2. **Who is the callee?** 

The tester must collect information about the callee. This includes:

* Personal information about the callee (e.g., name)

* General information about the target’s department

* Callee’s roles and responsibilities

* Callee’s relationship to the impersonated individual

* Details about callee’s personal life if the tester is impersonating his/her personal acquaintance(e.g., topics of small talk such as recent life events) 

Knowledge of such information will help the tester gain the callee’s trust thus increasing the chances of the attack’s success. The information can be obtained using tools such as Nikto to scan the company website for user information, searching the web, reading the company press releases, and studying the social media profiles of the callee’s organization and its employees.

3. **Detailed information about the person to be impersonated**

The tester must have knowledge about the person they will be impersonating. This includes:

* Name

* Employee ID number

* Location

* Phone Number

* Department name

* Department code

* Supervisor

* Email address

Much of the above information can be obtained using the techniques in (2). More detailed information, such at as Employee ID numbers, can be obtained through techniques such as glancing the employee’s badge in public (as employees often do not immediately take their badges off after leaving the workplace).

**5.3.1.2  Executing the Test**

Prior to executing the attack, the tester should use the previously gathered information in order to prepare and rehearse a script that they will follow during the attack. These preparations will help the tester sound convincing to the callee.  When executing the attack, the tester should also adhere to the following protocols: 

1. **Mask the tester’s phone number:** The tester must never use their own personal phone number in order to avoid revealing their real identity. The following techniques should be used in order to mask the real phone number:

* *67

    * By entering *67 before dialing a number, the source phone number will not be identified by the targets caller ID.

* Using a prepaid cell phones

* Using caller ID spoof services such as the following:

    * [Spoofcard](https://www.spoofcard.com/)

    * [Bluffmycall](http://bluffmycall.com)

    * [Crazycall](https://www.crazycall.com/)

    * [Spooftel](https://www.spooftel.com/)

    * [Covert Calling](https://www.covertcalling.com/)	

2. **Reduce target’s opportunities for asking questions:** During the phone call, the target can stall the attack by requesting information that the tester does not possess.  Such possibility can be alleviated by limiting the target’s opportunities for asking questions. One such technique is to provide the impersonated individual’s information when greeting the callee. For example,

*"Hi, this is Betsy Smith from the accounting department from extension 1234. I cannot login into my company account".*

3. **Develop exit strategies in case of successful and unsuccessful attack outcomes:**

    1. If the attack is successful:

* Ask a general question unrelated to anything discussed during the attack that the callee should be able to easily answer. This will help sway the callee’s focus away from the attack and reduce the chances of them becoming suspicious later. For example:

    * *When the target is IT helpdesk "By the way, I experienced some  connectivity issues this morning. Was the WiFi down?"*

    * *When the target is in HR: "By the way, my calendar got messed up, can you please remind me when the next department meeting is?"*

    2. If the attack is unsuccessful:

* If the callee requests information that the tester cannot provide (e.g., employee ID) and the attack cannot proceed without it, then it is important for the call to be terminated without arousing the callee’s suspicion (as it may jeopardize future tests). For example,

    * *Make the cell phone ringing sound in the background and say "I am sorry, my phone is ringing and I have to take this call.  May I call you back?".*

    * *"Sorry, someone just walked into my office. I will call you back".*

### 5.3.2  Physical Attacks

A tester can also take a more aggressive approach to their social engineering methods through a variety of physical attacks. These attacks involve direct contact with the targeted organization, and can be highly effective. At the same time these attacks can be very risky to the safety of the tester and the organization, and require significant planning and preparation beforehand.

**5.3.2.1 Preparing for the Test**

Preparation for the physical test should be driven by the following questions: 

1. **What are the test goals?**

    * To gain entry into a secure facility?

    * Steal information?

    * Deploy espionage software or hardware from within the perimeter?

Clearly defined goal(s) will allow the tester to identify the preparations needed for successfully executing the attack.

2. **What is the physical layout of the target area?**

    * Are there multiple buildings?

    * What are the physical entry and exit points?

    * Which areas are under surveillance?

    * What are the locations of parking lots?

    * Where are the dumpsters located?

    * Does the target area have security patrols?

    * What types of entry security mechanisms are implemented? (i.e., does entering the building require a key code, scanning an ID badge, or biometric verification? Does entry require confronting a security guard?)

The majority of information about the physical layout of the area can be obtained through Google Maps and other sources of public information. 

3. **What are the human factors?**

    * Is it easy to blend into the crowd?

    * Where do employees go for lunch?

    * What are the working hours?

    * What is the routine of individuals with regular access to the target area?

    * Can employees be observed outside of the workplace?

    * Who are the vulnerable individuals? For example, individuals that can be bribed or deceived through exploitation of their lifestyle choices, personalities, poor physical security practices (e.g., leaving unattended workstations unlocked,  soliciting entry into the buildings, and leaving passwords on posted notes, etc), substance abuse, etc. 

This information can be obtained by observing the human traffic in and out of the secured perimeter during different times of the day. If the organization has unsecured IP-enabled surveillance cameras, they can be discovered using [https://www.shodan.io/](https://www.shodan.io/) and be used to observe secure areas without gaining physical access.

**5.3.2.2 Executing the Test**

Depending on the goals of the test and information collected during the preparation phase, the tester should adhere to the following questions for executing the attack: 

1. **What techniques may be used to perform a physical attack?**

* **Dumpster Diving**

    * Collecting items that have been thrown away by the organization for the purposes of discovering information of value.

* **Intrusion/Roleplay**

    * The act of entering the target area and/or building by means of impersonating an individual who would usually have access.  This includes employees, outside contractors, postal service staff, and food delivery drivers.

* **Tailgating**

    * Pretending to be an employee of the target organization, or other individual using the above mentioned intrusion/roleplay technique, in order to gain access to a restricted area by following an individual with the authority to enter.  This method is effective because it takes advantage of an individual’s willingness to be helpful by holding open a door.

* **Shoulder Surfing**

    * A very simple, but effective technique that involves looking over the shoulder of the human target to gather information in plain view.  This can be executed at any location in which the target uses their digital devices such as coffee shops, airports, libraries, etc.

* **Proximity Scanning**

    * This involves using a device, such as the ProxMark3, that can scan RFID and/or NFC cards commonly used within an organization to gain entry to restricted areas.  Once scanned, the card can be duplicated and used to gain entry.

* **Dropped USB Drives**

    * Taking advantage of an individual’s curiosity or helpfulness is the main idea behind this physical attack.  This is done by deploying USB drives containing malware or espionage software within an organizations parking lot, and relying on an employee to pick up the drive and insert into an organization’s computer.  

* **Lock Picking**

    * Using lock picking tools to open doors that use a physical locking device.  This method is only effective if the tester is skilled in lockpicking and the organization has doors with a physical locking device.  

In order to execute the attack successfully, the tester should extensively rehearse the overall attack plan as well as the specific techniques. For example, if the attack will involve the use of lockpicking, the tester should develop sufficient skills in picking locks.

1. **Develop exit strategies in case of successful and unsuccessful attack outcomes:**

	* **If the attack is successful:** 

    	* The tester should exit breached perimeter as quickly as possible without arousing suspicion. This includes avoiding surveillance at the exits as well as well avoiding unnecessary interactions with the staff. If the interaction is necessary, the tester should behave in way in a way that will not make the other person suspicious.

	* **If the attack is unsuccessful:**

    	* If the tester fails in the attack’s objective it is still important for them to exercise the cautions in (**a**) and avoid revealing their real identity and purpose. Doing so gives the tester a chance to re-attempt the attack in the future using lessons learned from the failed attack.

In addition, the tester should always carry a copy of the contract for conducting the test to be presented if confronted by the organization’s security personnel or law enforcement as proof of authorization to conduct the test.  

### 5.3.3  Virtual Attacks

Virtual attacks are usually carried out through phishing emails, social media, and other digital means in order to deceive the victim. These types of attacks are very common because they are easy to create, distribute, execute, and have high success rates.

**5.3.3.1 Preparing for the Test**

The following questions should be kept in mind during preparation for virtual attacks:

1. **What are the attack goals?**

	The tester must clearly define the goals of the virtual attack to perform a successful and effective attack.  For example, the goal of the attack could be to gather the following information or perform malicious acts:

    * Usernames

    * Passwords

    * Password reset

    * Proprietary information

    * Customer information

    * Malware infection and/or propagation

2. **What techniques will be employed for exploitation?**

    * **Phishing**

        * A form of communication, typically through email, disguised to originate from an authentic organization with the purpose deceiving the victim into revealing sensitive information.  Phishing emails are usually sent without discretion to as many potential victims as possible to increase the chances of success.

    * **Spear Phishing**

        * A phishing technique that uses previously gathered information, either through another social engineering attack or through a simple web search, which targets specific individuals within an organizations.  This technique works because it will usually contain information that the victim trusts as legitimate, and it is especially effective when combined with the purchasing of domains and SSL certificates (described below).

    * **QR Code Phishing**

        * Another unique phishing technique which uses a QR code that is placed on any type of document with the promise of a free item, such as a free slice of pizza or music download.  The victim will usually scan the QR code due to their curiosity.

    * **Baiting**

        * A type of attack that relies on the curiosity or greed of the victim by luring them into the promise of a desired item such as a movie, song, or other promotional gift.  Similar to the above mentioned QR code phishing.

    * **Social Media**

        * Leveraging social media networks for actively gathering information about the victim. A simple example of this involves attackers creating a network of bogus LinkedIn profiles targeted at an individual or organization. Some of these profiles would claim to be recruiters from similar organizations, often in the same industry as the target. The attackers, then posing as recruiters, attempt to entice their target into handing over sensitive information that can be used throughout the attack.  Works really well in conjunction with a phishing attack.

    * **Domain/SSL Certificate purchasing**

        * This technique increases the chances of success for the above mentioned virtual attacks.  By purchasing a domain, the tester does not have to rely on disguising malicious links attached to phishing emails, which allows bypassing of phishing prevention services.  When combined with a purchased SSL certificate, success becomes even higher.

In order to determine the proper technique, the tester should perform background research on the targeted individuals/populations.  Special attention should be paid to targets’ job responsibilities, interests, personality, and anything else that may entice the target to fall victim. These will be useful when executing the attack as we describe next. 

**5.3.3.2 Executing the Test**

Depending on the goals of the test and information collected during the preparation phase, the tester should adhere to the following questions for executing the attack:

1. **How can the virtual attack techniques be modified for the test subject(s)?**

* **Phishing and Spear Phishing**

    * Spoof an email direct toward a specific employee with a topic they are interested in and/or passionate about.  This information can be done by performing reconnaissance on their social media profiles. 

    * Send a phishing email with a pdf attachment to an employee in a high ranking position.  This email can be spoofed to look like a company document, but contain a hidden malicious payload.

* **QR Code Phishing and Baiting**

    * Look up restaurants/bars in the vicinity of the target organization.  An advertisement with a malicious QR code can be created to say something along the lines of "Buy one, Get one free!"  These pamphlets can be dropped or distributed in the entrance to the building, or the parking lot, of the target organization offices.

* **Social Media**

    * Can create a fake social media profile of an employee in a higher ranking position, preferably of someone who is not present/active on social media.  Once this profile is created, it can be used to connect to other employees within the organization.  Once legitimacy has been established, can post links to malicious sites that have been masked with legitimate domains and ssl certificates.  This works due to the level of authority this particular individual has within the organization.

* **Domain/SSL Certificate Purchasing**

    * Purchase the domain and ssl certificate for the websites that are needed for the above mentioned virtual attacks.

The virtual attacks described above are some of the many techniques that can be leveraged for data theft.  When combined together, and with specific information for a specified target, the success rate is greater. 

1. **Develop exit strategies in case of successful and unsuccessful attack outcomes:**
	* **If the attack is successful:** 

    	* The tester should take measures to ensure any evidence of the testing is removed or at best minimized. This could include tasks such as modifying or deleting logs that capture any proof that an attack was carried out. It should also be noted when removing or minimizing evidence, the tester should do so in a manner as to not raise suspicion. 

	* **If the attack is unsuccessful:**

    	* If the tester fails in the attack’s objective it is still important for them to exercise the cautions in (**a**) and avoid revealing their real identity and purpose. Doing so gives the tester a chance to re-attempt the attack in the future using lessons learned from the failed attack.

### 5.3.4 Prevention Measures / Standards

The organization can take measures in order to defeat the phone, physical, and virtual penetration tests and consequently help strengthen its overall resilience to social engineering attacks. It also lists various standards or regulations that organizations can follow to better mitigate these attack vectors. 

1. **Phone Attacks**

Organizations can take steps to prevent unsolicited phone calls. Depending on the organization and their daily operations, employees can make educated judgments as to the overall legitimacy of a phone call. Some of the steps that an organization can take to be proactive against phone based social engineering attacks include the following:

* Block or do not accept incoming calls without a caller ID

* If an incoming call is unsolicited, and not related to the organization’s business, hang up

* Utilize services that prevent unwanted incoming calls, such as the FCC’s ‘Do Not Call’ List

* Ensure employees are trained not to release any sensitive information, unless absolutely necessary. This should include other information that attackers could use to further progress in attacking the organization. 

* Report any suspicious calls to the appropriate personnel 

The National Institute of Standards and Technology Special Publication 800-53 (Rev. 4)
Security Controls and Assessment Procedures for Federal Information Systems and Organizations has an article on Information Sharing that is relevant to phone based social engineering attacks. AC-21(1) INFORMATION SHARING states that:

"The information system enforces information-sharing decisions by authorized users based on access authorizations of sharing partners and access restrictions on information to be shared." 

2. **Physical Attacks**

For any security conscious business, first and foremost importance has to be strong physical security, enforced throughout the organization and consistently on everyone. Without tighter controls and lax security, attackers will have little trouble physically accessing stations, they need, to launch their digital attack. In addition, once clear and concise security policies are established and implemented, they should be periodically tested, to determine the state of security awareness among staff members, to resolve gaps, if any are identified. It is also equally important for the the staff to be continually reminded that the possibility of an attack is real, which can occur at anytime without warning.

Some good practices to prevent Physical Attacks are:

* To have signs around the entrance of work, reminding employees to not plug-in any USB drives or any other digital device they find around the premises.

* Encourage employees to submit any unknown digital device found around the premises to experts for analysis and report any suspicious behaviour to security.

* To have employees acknowledge and sign reminder of best security practices each month.

* Physical security could be bolstered with an all round CCTV coverage and clearly defined human perimeter defence space on the premises.

* To install protective physical barriers, security lightnings, alarms, motion detection systems and the use of biometrics to identify employees.

Some of the standards and regulations put in place by the Payment Card Industry Data Security Standard (PCI DSS) and Health Insurance Portability and Accountability Act of 1996 (HIPAA) outline various actions that organizations can take to protect themselves from these physical based social engineering attacks. For example, to protect against dumpster diving attacks, PCI DSS Requirement 9.8 calls to "Destroy media when it is no longer needed for business or legal reasons". 

With sufficient physical controls in place, it may be possible for a company to repel a substantial Social Engineering attack. But without implementation of strict physical security protocols, the company is keeping their doors open to unauthorised visitors with malicious intents, to visit and intrude the premises, place malwares, Trojans, spywares and circumvent the controls to access the desired data.

3. **Virtual Attacks**

Virtual Attacks are generally achieved using internet. Some of the techniques to prevent Virtual based social engineering attack.

* **Be wary** of emails, instant messages and phone calls for unsolicited people such as service providers. Verify the source of message before giving out any information.

* **Go slow** and pay keen attention to fine details in emails and messages. Never let the urgency in attacker’s message cloud your judgment.

* **Educate yourself** **-** Information is the most powerful tool in preventing social engineering attacks. Research facts on how to identify, and ward off online criminals.

* **Never click on embedded links** in emails from unknown senders. If necessary use the search engine to search for suggested website or manually enter the website URL.

* **Never download email attachment from unknown senders**. If necessary open the attachment in protected view which is enabled by default in many operating systems.

* **Reject requests** for online tech support from strangers no matter how legitimate they may appear.

* **Secure your computer space** with a strong firewall, up to date antivirus software and set your spam filters too high.

* **Patch up software and operating systems** for Zero day vulnerabilities. Follow up on patch releases form your software providers and patch-up as soon as humanly possible.

* **Pay attention to website URL**. Sometimes online fraudsters make slight changes to URLs in order to direct traffic to their own spoofed sites.

* **Avoid being greedy on the web**. If you never participated in a lottery, it goes without saying that you can never be the winner. If you never lost money, why would you accept a refund from the FBI?

## ALTERNATE TECHNIQUES

Building a defense against social engineering is similar to building any strong defense. The key is to determine what the vulnerabilities and threats are and then defend against those risks. The defense must have several layers of protection so that even if a hacker were able to penetrate one level, there would be other levels at which he or she would be stopped.

Multi-layer defense against social engineering (SANS Institute) includes following layers:

1. **Foundational Level: Security Policy addressing social engineering**

2. **Parameter Level: Security Awareness Training for all users**

3. **Fortress Level: Resistance Training for Key Personnel**

4. **Persistence Level: Ongoing Reminders**

5. **Gotcha Level: Social Engineering Land Mines (SELM)**

6. **Offensive level: Incident Response**

**1. ****Foundational Level****: Security Policy addressing social engineering:-**

The foundation of information security is its policy. The security policy sets the standards and level of security a network will have. It also gives the network a known state that can be adjusted as necessary. The security policy must address a number of areas in order to be a foundation for social engineering resistance. It should address information access controls, setting up accounts, access approval and password changes. It should also deal with locks, ID’s, paper shredding, and escorting of visitors. The policy must have discipline built in and, above all, it must be enforced. The policy also sets responsibility for information or access that is given out so that there is no question as to the employee’s own risk when giving away privileged information or access.

**2. ****Parameter Level****: Security Awareness Training for all users:-**

Once the foundation of a security policy has been established and approved, all employees should be trained in security awareness. The security policy will provide guidelines for the training as well as motivation. Policies that are well thought out and then taught to employees can make a difference in how employees respond to requests. 

Security awareness is more complicated than just telling people not to give their password away. Employees must know what kind of information a social engineer can use and what kinds of conversations are suspect. Employees should know how to identify confidential information and should understand their responsibility to protect it. They also need to know how to say "no" when it is appropriate and have the backing of their management on the occasion where it might offend.

The training curriculum should basically follow the security policies, but there are some key points that all users need to remember.

* Know what has value

* Friends are not always friends

* Passwords are personal

* Uniforms are cheap

**3. ****Fortress Level****: Resistance Training for Key Personnel:-**

Not only should all employees be trained in security awareness, but a part of a multi-level defense should also include resistance training for key personnel. Key personnel include Help Desk personnel, Customer Service, business assistants, secretaries and receptionists and system administrators/engineers. Basically, it should include anyone whose job is to help others especially the general public and those whose job includes escalated rights.

Good resistance training will help prevent employees from being persuaded to give information away that the hacker might need. Several resistance-training techniques can be used from the field of social psychology to help adequately prepare employees to resist the persuasion techniques of a social engineer.

* **Inoculation** - Inoculation is when employees are given weakened arguments that will be used by the social engineer. 

* **Forewarning** - Forewarning is another resistance-building technique that has been tested by social psychologists. Psychologists have tested warning subjects both of the content of an upcoming message and the persuasive intent of an upcoming message. Forewarning of the content caused greater resistance than forewarning of persuasive intent.

* **Reality Check** - One of the reasons why security awareness training fails is that people tend to have an unrealistic optimism about their own Invulnerability. This perception leads many to ignore legitimate risks and fail to take measures to offset those risks. However, once they are fooled and it is demonstrated to them that they are indeed vulnerable, the training is much more effective.

**4. ****Persistence Level****: Ongoing Reminders:-**

	A multi-level defense will need to include regular reminders of the necessity of security consciousness. One shot at training people to resist the social engineer will be effective for only a very short period of time. Regular and creative reminders are necessary to keep people aware of the dangers that may lurk on the other end of a friendly call. 

	employees need to be regularly reminded of the possibility of a hacker attempting to steal information from them and specifically informed of any recent attempts.

**5. ****Gotcha Level****: Social Engineering Land Mines (SELM):-**

Social Engineering Land Mines are traps that are set up in the system to actually expose and stop an attack. The SELM will alert the victim and the victim’s security that an attack is in progress and should be either addressed or a heightened security posture should be engaged.

Several ideas for Social Engineering Land Mines (SELM) are listed below:

* **The Justified Know-it-all** - The Justified Know-it-all is a person who makes it his or her business to know everyone who is on the floor or walking around in a department. Many departments already have someone who does this naturally. For this to be a SELM, that person should be briefed on the security risks of the physical presence of a social engineer and should have the power to do something quickly to address an unescorted visitor. This land mine would be useful even if badges are used for security as hackers will often forge a badge and expect not to be confronted.

* **Centralized Security Log** - Having a centralized log of security events that is being monitored by information security personnel can help prevent an effective attack. Any time an employee is asked to give out information or reset a password or even has a suspicious call, it should be logged in this central log file.

If a hacker is getting information from one employee and using it to talk to another employee, the patterns could be noticed in the log. As soon as the pattern is noticed, security personal can take action to stop the attack by warning employees of the attacker.

* **Call Backs by Policy** - A fairly well known procedure that would make for an effective land mine is a policy that requires Help Desk personnel and system administrators to call back anyone requesting a password reset or questionable information. The call back will verify the phone number and should be the phone number listed in the directory for the person who is calling.

If the caller tries to explain why the call back cannot be done or if the phone number is not the number expected for that employee, the Help Desk personnel should have the freedom of not having to grant the request and a security log entry should be generated. 

* **Key Questions** - Another SELM is for a number of questions to be used to verify the identity of anyone who is calling for internal information or trying to get a password reset.

    * The Three Questions Rule is a good one to use, but must be set up with all employees in advance. This rule provides a list of questions and answers that the Help Desk personnel can use to verify identity. The questions should be obvious for the employee but not for others.

    * If none of these systems are set up, a bogus question could work as well. The bogus question is a question that implies false information and gives the caller a chance to set the record straight or build on the false information.

* **"Please Hold" by Policy** - The psychological literature is clear that people are more easily persuaded to do something questionable when there is pressure, surprise, or overloading. An SELM to defeat this is a policy that requires that any suspicious call or any call asking for a password reset or privileged information should be put on hold. This will stop the action and give the employee a chance to think. During the hold, the employee can log the request, discuss the request with a co-worker, or decide how to verify the identification.

**6. ****Offensive level****: Incident Response:-**

The final level of defense is incident response. This is critical so that the network is not just waiting for the social engineer to finally get a hold of someone in the company who does not know or care about security. There needs to be a well-defined process that an employee can begin as soon as he or she suspects something is wrong. This process should aggressively go after the hacker and proactively inform other potential victims.

If there is no incident response, the hacker gets better at understanding the organization’s defenses. It is important to have one person or a department working very closely tracking these incidents so that the attack can be characterized quickly and effectively. This should be the same person that is watching the journal logs from anyone who is receiving suspicious requests.

