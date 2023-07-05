# Nineveh

This is my write-up for the machine on Hack The Box called Nineveh located at: [https://app.hackthebox.com/machines/Nineveh](https://app.hackthebox.com/machines/Nineveh).

I started off with a basic nmap scan:

![](<../../.gitbook/assets/image (325).png>)

One of the tags on the machine was for Port Knocking:

![](<../../.gitbook/assets/image (478).png>)

This gave me the idea that I might have to knock a port later on to get into it. While I was doing some research my full nmap scan (`nmap -T4 -A -v -p- -Pn 10.10.10.43 -oN nineveh.nmap`) came back:

![](<../../.gitbook/assets/image (656).png>)

It seems to represent the same information that the basic nmap scan had provided. The main page seems to be a default home page that seems standard:

![](<../../.gitbook/assets/image (573).png>)

Running **dirsearch** on the IP address led me to the following page:

![](<../../.gitbook/assets/image (528).png>)

Looking at the source code, I found the following:

![](<../../.gitbook/assets/image (385) (1).png>)

It seems that there is a username of **amrois**. In addition, I have learned that MySQL has been installed on the server. I then ran **dirsearch** on the **/department** on the folder:

![](<../../.gitbook/assets/image (559) (1).png>)

I am not able to access either of those sites, since I need to log in to the website first. Using the username **amrois**, I got the following:

![](<../../.gitbook/assets/image (510) (1).png>)

However, when I enter the username **admin**, I get the following:

![](<../../.gitbook/assets/image (418).png>)

It seems that **amrois** might be an MySQL admin username or something else. Running **hydra** on the admin user got me the following:

![](<../../.gitbook/assets/image (398).png>)

I was into the website:

![](<../../.gitbook/assets/image (381).png>)

I also saw the following on the main page:

![](<../../.gitbook/assets/image (520).png>)

The link looks (at a basic glance) to be vulnerable to File Inclusion:

![](<../../.gitbook/assets/image (386).png>)

I accessed the website on port on 443 (HTTPS) and saw the following:

![](<../../.gitbook/assets/image (628).png>)

Running **dirsearch** on port 443 gives different results:

![](<../../.gitbook/assets/image (658).png>)

Going to the **/db** folder, I see the following:

![](<../../.gitbook/assets/image (370) (1) (1) (1) (1) (1).png>)

Searching for **phpLiteAdmin** on Exploit Database I see the following:

![](<../../.gitbook/assets/image (698).png>)

I tried to run **hydra** on the password field, and it worked:

![](<../../.gitbook/assets/image (450).png>)

I then made a new database using the button on left side:

![](<../../.gitbook/assets/image (586).png>)

This is from the following Exploit Database link: [https://www.exploit-db.com/exploits/24044](https://www.exploit-db.com/exploits/24044). I then made the table called "testing":

![](<../../.gitbook/assets/image (689).png>)

I viewed [this write-up](https://0xdf.gitlab.io/2020/04/22/htb-nineveh.html) and noticed that they were able to get the contents of **/etc/passwd**, by using LFI. I then followed their request and got the following:

![](<../../.gitbook/assets/image (547).png>)

{% hint style="warning" %}
NOT COMPLETED
{% endhint %}
