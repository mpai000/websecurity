# websecurity

# Project 7 - WordPress Pentesting

Time spent: 24 hours spent in total

> Objective: Find, analyze, recreate, and document **three vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Authenticated Stored Cross-Site Scripting 
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6.1
  - [ ] GIF Walkthrough: file:///Users/meghnapai/Desktop/exploit1.gif
  - [ ] Steps to recreate: 
Login in as admin. 
Go to add new post.
Type in <a href="></a><a title=" onmouseover=alert('Test') "> link</a> as a post.
Click on preview.
When you hover over the link with the mouse, the alert should pop-up.

  - [ ] Affected source code: 
    - [Link 1]https://core.trac.wordpress.org/changeset/33359
    
2. (Required) Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: file:///Users/meghnapai/Desktop/exploit2.gif
  - [ ] Steps to recreate: 
  Login as admin.
  Go to add a new post.
  Type in [embed src='https://www.youtube.com/embed/123\x3csvg onload=alert("Hi!")\x3e'][/embed]

  - [ ] Affected source code:
    - [Link 1]https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html
    - [Link 2]https://wpvulndb.com/vulnerabilities/8768
3. (Required) Wordpress: CVE-2017-9061: Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.7.5
  - [ ] GIF Walkthrough: file:///Users/meghnapai/Desktop/exploit3.gif
  - [ ] Steps to recreate: 
    In your terminla type in mkfile -n 3m temp.jpg. This will make a temporary file of size 3MB on your desktoop. 
  Rename it to Test<img src= a onerror=alert('Hi!')>.jpg.
  On Wordpress, login as admin and go to add new media. 
  - [ ] Affected source code:
    - [Link 1]https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8

## Assets

No additional resources were used

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Initially, while running kali with wordpress, it caused my OS to crash. 
After reinstalling my OS, I was able to have kali running. TO make my Wordpress pages be displayed correctly,
I also had to change the theme to twentyfifteen.

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
