**Summary**

This is a simple markdown info on how a passive reconnaissance should be done when doing a pentest. This markdown will cover about different websites and online applications that can be used to gather information about a company without directly targetting the company resources. 

**Reconaissance Steps**

Passive reconnaisance is a form of OSINT to gather information about your targets. Having a set framework on what tools to use and how they can help is necessary to success in passive reconnaissnace. For this process, we have designed a small map that can be used to understand the process. The map is attached below: 

![Passive Recon](resources/passive_recon_map.svg)

You can also download this map from the resources directory [here](resources/passive_recon_map.svg)

Following sections will contain a breakdown of each node in the map. These sections will link programs/softwares that help with reconnaissance. 

**Company Personnel**
1. Knowing about who works in the company and what they do is extremely useful for many purposes. Additionally, some additional OSINT can also help to find any leaked password of the person. 
2. **Using LinkedIn**
	* LinkedIn is a great resource in gathering list of people who work for a particular company. Using its search feature, it is pretty easy to identify who works for what role in a company. This information can then be used to identify a potential target for social engineer and other forms of attacks. 
	* Once a target is chosen through LinkedIn, a more in-depth passive reconnaissance can be done to identify more information about the person for example, what they do, where they go and more. 
3. **Using Hunter.io**
	* Hunter.io can help to identify emails of people working in a particular company. 
	* This can be useful once you identify list of individuals working for a company because then, you can gather their emails and start planning out a social engineering attack. 
	* Additionally, information gathered from Hunter.io can be cross checked with haveibeenpwned.com to see if the email was ever found in a password dump. This information can be used to check for password reuse attacks. 

**Identifying Domains and Assets**
1. Identify Subdomains: Websites like VirusTotal, ThreatCrowd and Google can be used to idenfity subdomains of a company. These subdomains help to expand the attack surface.
	* [VirusTotal](https://www.virustotal.com/#/domain/domain.com)
	* [ThreatCrowd](https://threatcrowd.org)
    * You can also use [this simple python tool](https://github.com/aboul3la/Sublist3r) to automate this process. 
2. Identify Assets: Shodan.io and Censys can help to identify more assets of a company. Companies do not just have websites, they will also have IoT devices and other setups like VPN services. These services help to identify them faster. 
	* [Shodan](https://shodan.io)
	* [Censys](https://censys.io)

**Source Code Analysis**

*Many companies believe in the idea of open sourcing their internal codes that can be used by other users. Sometimes, these open source codes can help to analyze for any internal vulnerabilities or chances of leaked credentials such as API keys, Database passwords, etc.*
1. GitHub
	* GitHub is one of the most common platform for open source projects. One can easily find a lot of information about a company's code base and their employee projects by simply searching for the company domain.
		* [GitHub](https://github.com)
		* Search keyword to use: "@domain.com"

2. Bitbucket
	* Similar to GitHub, another website used to host open source projects is Bitbucket. 
		* [Bitbucket](https://bitbucket.org/name)


**Password Leaks and Dumbs**

*As stated in the `Company Personnel` section, email ids of a company personnel can be cross checked to find any leaked passwords. Sometimes, employees are not aware that their account in a third party service was compromised, these situations lead to password reuse by employees on multiple other third party service.* 
* Websites to use: 
	* [Have I Been Pwned](https://haveibeenpwned.com)
	* [Pastebin](https://pastebin.com)
		* Pastebin usually has a lot of password dumps that are posted daily, searching for "@domain.com" can help to find any pastebins that contain the keyword `@domain.com` which could usually lead to dumped credentials. 
	
**Acquisitions**

Some companies acquire companies that they believe can help support their goals. These acquisitions may sometimes be vulnerable to different form of attacks. Finding an acquisition list can be useful in expanding the attack surface. 

[Crunchbase](https://www.crunchbase.com)

