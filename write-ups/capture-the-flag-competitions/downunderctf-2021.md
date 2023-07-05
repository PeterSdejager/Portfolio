# DownUnderCTF 2021

### The Introduction

![](<../../.gitbook/assets/image (216).png>)

For this one, I ran the netcat command, and then waited for the output to finish, and then I got the flag:

![](<../../.gitbook/assets/image (217).png>)

### Retro!

I downloaded the file, and ran `strings` on the file, and found the flag:

![](<../../.gitbook/assets/image (218).png>)

### Who goes there?

![](<../../.gitbook/assets/image (219).png>)

For this one, I was looking for the domain registration for the website to get as much information as I can. I found the following on a WHOIS Lookup Domain website:

![](<../../.gitbook/assets/image (220).png>)

The flag was the Phone number in DUCTF{Phone\_Number} format.

### Get Over it!

![](<../../.gitbook/assets/image (221).png>)

We get an image for this one:

![](<../../.gitbook/assets/image (222).png>)

I ran it in **tineye** and got no result. I then ran it on **Yandex**, and I saw a picture that looks like the one I had gotten from the CTF:

![](<../../.gitbook/assets/image (223).png>)

The bridge seems to match this image. I then used [https://inflact.com/profiles/instagram-viewer/](https://inflact.com/profiles/instagram-viewer/) to view the image from the poster. I needed to view the tags:

![](<../../.gitbook/assets/image (224).png>)

The tag that helped the most was the **saintluciabrisbane**. I Google-ed "saint lucia brisbane bridge" and got the following:

![](<../../.gitbook/assets/image (225).png>)

I went on the Wikipedia page for the first page and got the following:

![](<../../.gitbook/assets/image (226).png>)

The bridge does look the same as the image. I then tried the flag multiple times, but was not able to get it with the size of 390. I then googled "Eleanor Schonell Bridge size", and got the following:

![](<../../.gitbook/assets/image (227).png>)

The flag was `DUCTF{Eleanor_Schonell_Bridge-185m}`

### Discord

![](<../../.gitbook/assets/image (228).png>)

For this problem, I went to the discord of the CTF and found the flag:

![](<../../.gitbook/assets/image (229).png>)

### Sharing is Caring

![](<../../.gitbook/assets/image (230).png>)

For this one, my first step was to run the username in `sherlock`:

![](<../../.gitbook/assets/image (231).png>)

I did not find anything important on Pinterest or Twitch, but I got the following on Steam:

![](<../../.gitbook/assets/image (232).png>)

I then ran the other username in **sherlock** as well:

![](<../../.gitbook/assets/image (233).png>)

The Github portfolio did not really have anything, other than a repository. The Reddit account had some posts on it. One of them stood out to me:

![](<../../.gitbook/assets/image (234).png>)

Looking closer at the picture, I noticed this:

![](<../../.gitbook/assets/image (235).png>)

I knew it wasn't an IP Address, so my assumption was that it was a MAC Address. When I entered it on `Wigle.net` I got only one result:

![](<../../.gitbook/assets/image (236).png>)

The flag was the street name.
