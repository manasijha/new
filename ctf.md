---
title: 'DeepCTF 0x01 Crypto Writeup'
date: '08-07-2020'
author: 'Manasi Jha'
description: 'Here, we are going to learn how the challenges from the crypto category were solved.'
SEO: 'CTF, crpto, writeup, cybersecurity'
---

# DeepCTF 0x01 Crypto Writeup

Today, we will see how the challenges were solved from the crypto section of DeepCTF 0x01 CTF and what where the tools required for the same and how to use them.

## Overview
* The Crypto category had 10 challenges ranging from easy to intermediate. Below I have tried to explain what the questions where, what was demanded and the approach with the solution.

![image](https://user-images.githubusercontent.com/47267639/86937079-71494280-c15c-11ea-9d45-079ff8e14e09.png)

***
### Challenge 1: Warm Up

![image](https://user-images.githubusercontent.com/47267639/86937912-71960d80-c15d-11ea-9a28-212f10ba6866.png)

On downloading the txt file and opening it, I found:
64 33 33 70 01111011 01001010 01110101 00110101 01110100 01011111 00110100 01011111 01001110 00110000 01110010 01101101 00110100 01101100 95 67 104 52 108 108 95 95 111 163 156 140 164 137 61 164 77 175
After analyzing, it was found that it is a combination of hex, binary, decimal, octal in the same order.
The site used was: here(https://v2.cryptii.com/)

After decrypting everything, I got the flag.
Flag:***d33p{Ju5t_4_N0rm4l_Ch4ll__Isn`t_1t?}***

### Challenge 2: WTF'ish

![image](https://user-images.githubusercontent.com/47267639/86938875-89ba5c80-c15e-11ea-803e-39d127f61617.png)

The txt file had some weird stuff:
++++++++++[>+>+++>+++++++>++++++++++<<<<-]>>>>.<-------------------..>++++++++++++.+++++++++++.<++++++++++++++++++++++++++++++++++++.+++++++++++++++++.-------.>-------.<--.-----------.>------------.---.------.<------------------.>+++++++++++++++++++.-----------------.++++++++.+++++.<++++.<+++++...>>+++++++++++++++.

First thing to do here was search for info about the message with the data  which was available for us. The chall name itself spoke a lot. After searching for “What the fuck cipher” the first result lead us to our destination. The cipher used here was Brainfuck cipher. After decoding it on here(https://www.dcode.fr/brainfuck-language), I got our flag.
Flag:***d33p{What_The_BrainF###}***

### Challenge 3: Ali3nAgain

![image](https://user-images.githubusercontent.com/47267639/86939236-f33a6b00-c15e-11ea-83d7-f57804b203f2.png)

The spdvsalien.png looked like this.

![image](https://user-images.githubusercontent.com/47267639/86939337-136a2a00-c15f-11ea-9cae-ae1b816982e5.png)

This definitely left me clueless. The only idea I had was
a)it was an alien languages
b)Google Images.
After uploading the picture on Google images we found out it was Futurama cipher. I got this image as my savior.

![image](https://user-images.githubusercontent.com/47267639/86939460-398fca00-c15f-11ea-805c-f12f7d09698e.png)

Flag:***d33p{POWERRANGERSPDFORCEWON}***

### Challenge 4: WierdText

![image](https://user-images.githubusercontent.com/47267639/86940711-c5562600-c160-11ea-9d4f-e6566f057b58.png)

The message for us was: c4co"Lct5-vec+H2efw)G-"Ve+$2;5zeef+
As the chall description says about getting a new keyboard, I tried looking up for keyboard cipher and I got it here(https://www.dcode.fr/keyboard-shift-cipher).
Flag:***d33p{K3yb04rd_N33ds_T0_B3_R3p41r3d}***

### Challenge 5: format is key to success!

![image](https://user-images.githubusercontent.com/47267639/86941190-4ad9d600-c161-11ea-97f6-4c90ad02c5e0.png)

At first it looked like the cipher needs to decoded with a key which was “format”. I used this(https://cryptii.com/) and tried decoding it but nothing. After trying for a lot of times, it struck to me that the flag should be in format d33p{……….. and whatever key we used nothing affected the numbers in the cipher. We tried using d33p, deep, DEEP but nothing. We then used dp as key and woah we got it.
Flag:***d33p{fl4g_is_b34utiful!!!}***

### Challenge 6: Troll

![image](https://user-images.githubusercontent.com/47267639/86941827-07339c00-c162-11ea-9ba2-99d83a610d7e.png)

The txt file had a very long message with === at the end. This inidicated as it was a base32. After decoding we got a flag followed by a large strings of number. The flag was a wrong flag so we moved on to decode the number which was octal to text. We repeated the process with dec to text, hex to text followed by base64.
Flag:***d33p{y0u_D1D_1t}***

### Challenge 7: Ali3nCalling

![image](https://user-images.githubusercontent.com/47267639/87174658-21ea4a00-c2f5-11ea-9058-2485e0095598.png)

The png file looked like this.

![image](https://user-images.githubusercontent.com/47267639/87174757-46462680-c2f5-11ea-8fab-c923de602cd5.png)

Same as Challenge 3. The site used was this(https://www.boxentriq.com/code-breaking/pigpen-cipher). After decoding gibberish value was found along with flag.

Flag:***d33p{outoftheworldcipher}***

### Challenge 8: RSA 1.0

![image](https://user-images.githubusercontent.com/47267639/87174794-565e0600-c2f5-11ea-8f9e-0b3ec9c452c2.png)

The following was provided to us n,c,p and e.
The scripts for rsa are available online. Try reading more about rsa here(https://en.wikipedia.org/wiki/RSA_(cryptosystem))

Flag:***d33p{An0th3r_S1mpl3_RSA_D3fe4t3d}***

### Challenge 9: 1940

![image](https://user-images.githubusercontent.com/47267639/87174823-670e7c00-c2f5-11ea-90b6-7a8781a8c552.png)

The pdf had this message for us.
* A Very Old Document Was Found, Which Was Probably Of 1939-1945 Time Period.  The information in it is as followsM3 C 6 1 3 Also, Birth Year Of A Famous British Mathematician Is Used Somewhere In format(Y-Y-YY) AND LASTLY, ab-cd-ef-gh-ij-kl-mn-op-qr-st
Using The Above Information, Decode-  w33x{vkux_clncxq_lhe_r_jqqnsy}

The hints said something about rings.

![image](https://user-images.githubusercontent.com/47267639/87174908-81485a00-c2f5-11ea-8c3c-b5aaeada1233.png)

After looking up for mathematician we found about Alan Turing who was very famous for Enigma.

We used enigma decoder on this(https://cryptii.com/) by setting model as M3, reflector as C, rotar as 6,1,3, position as 1,9,12(Dob year) and rings as 1,2,7.
And also plugboard as ab cd ef gh ij kl mn op qr st and included foreign char.

Flag:***d33p{alan_turing_was_a_legend}***

### Challenge 10: l33tRSA

![image](https://user-images.githubusercontent.com/47267639/87174944-91603980-c2f5-11ea-809b-114cfc91ee0c.png)

This chall wasn’t a Classic one. Rather it was common modulo RSA as we had following info. N,e1,e2,c1,c2.
We got a script online and used that to get the flag.

Flag:***d33p{A_l33t_d3crypt3r_4rr1v3d}***
