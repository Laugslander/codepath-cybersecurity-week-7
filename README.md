# Project 7 - WordPress Pentesting

Time spent: **4** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [x] Summary:
    - Vulnerability types: XSS (CVE-2017-6817)
    - Tested in version: 4.2 (affects versions 4.0 - 4.7.2)
    - Fixed in version: 4.2.13
  - [x] GIF Walkthrough:

    ![Walkthrough exploit 1](https://i.imgur.com/LqaLZgY.gif)
  - [x] Steps to recreate:
    - Sign in as an administrator
    - Create a new Post
    - Switch from Visual editing mode to Text (HTML) editing mode
    - Insert the malicious YouTube embed shortcode

        `[embed src='https://www.youtube.com/embed/dQw4w9WgXcQ\x3csvg onload=alert("exploit!")\x3e'][/embed]`
  - [x] References:
    - https://wpvulndb.com/vulnerabilities/8768
    - https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-6817
    - https://wordpress.org/news/2017/03/wordpress-4-7-3-security-and-maintenance-release/
    - https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8
    - https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html
2. Authenticated Stored Cross-Site Scripting (XSS)
  - [x] Summary:
    - Vulnerability types: XSS (CVE-2015-5622 and CVE-2015-5623)
    - Tested in version: 4.2 (affects versions 4.0 - 4.2.2
    - Fixed in version: 4.2.3
  - [x] GIF Walkthrough:

    ![Walkthrough exploit 2](https://i.imgur.com/4nuw80g.gif)
  - [x] Steps to recreate:
      - Sign in as an administrator
      - Create a new Post
      - Switch from Visual editing mode to Text (HTML) editing mode
      - Insert the malicious a href code

        `<a href="[caption code=">]</a><a title=" onmouseover=alert('exploit!')  ">link</a>`
  - [x] References:
    - https://wpvulndb.com/vulnerabilities/8111
    - https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5622
    - https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5623
    - https://wordpress.org/news/2015/07/wordpress-4-2-3/
    - https://twitter.com/klikkioy/status/624264122570526720
    - https://klikki.fi/adv/wordpress3.html
3. (Required) Vulnerability Name or ID
  - [x] Summary:
    - Vulnerability types: XSS (CVE-2015-5714)
    - Tested in version: 4.2 (affects versions 4.0 - 4.3
    - Fixed in version: 4.2.5
  - [x] GIF Walkthrough:

    ![Walkthrough exploit 3](https://i.imgur.com/f9XWOUo.gif)
  - [x] Steps to recreate:
      - Sign in as an administrator
      - Create a new Post
      - Switch from Visual editing mode to Text (HTML) editing mode
      - Insert the malicious caption code

        `[caption width="1" caption='<a href="' ">]</a><a href=" onmouseover='alert("exploit!")' ">Click!</a>`
  - [x] References:
      - https://wpvulndb.com/vulnerabilities/8186
      - https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5714
      - https://wordpress.org/news/2015/09/wordpress-4-3-1/
      - http://blog.checkpoint.com/2015/09/15/finding-vulnerabilities-in-core-wordpress-a-bug-hunters-trilogy-part-iii-ultimatum/
      - http://blog.knownsec.com/2015/09/wordpress-vulnerability-analysis-cve-2015-5714-cve-2015-5715/


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright 2018 Robin Laugs

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
