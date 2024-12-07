# Email Header and Sender Analysis

<h2>Description</h2>
In this practical email header and sender analysis, I exam two phishing email captures attempting to spoof Chase Bank and CIBC Bank. I used tools like thunderbird, sublime text editor, and whois.domain.lookup to investigate artifacts from the suspicious senders.   
<br />


<h2>Languages and Utilities Used</h2>

- <b>Linux CLI</b>
- <b>Sublime Text Editor</b>
- <b>whois.domaintools</b>
- <b>message header analyzer tool</b>

<h2>Environments Used </h2>

- <b>Unbuntu</b> 

<br />
<br />
The first phishing email capture from "Chase Bank."

![1) saved email document](https://github.com/user-attachments/assets/360b8423-c1e8-4146-a95d-4880df911da7)

<br />
<br />
I used sublime text editor to view the email header. I installed an email header package to highlight the headers. 

![2) opened the email copy in sublime with highlighted syntax](https://github.com/user-attachments/assets/4148a311-07d9-4c53-8d0c-cec699f4f383)

<br />
<br />
Ive highlighted some standard headers important for documentation during the investigating. Analysing these headers showed that the return path and the from header were not the same email.

![3) analyzing common headers from the email to document important artifacts](https://github.com/user-attachments/assets/1c392d1f-c357-413f-932c-031c07afc7b9)

<br />
<br />
This email header showed an X-Sender-IP from the suspicoius actor. 

![4) this particular email shows the sender IP](https://github.com/user-attachments/assets/2a87f40a-422f-49ce-9b28-d92b7d05d2ba)

<br />
<br />
Examining the received headers from originating (bottom) to most recent (top), I found that the email was originally received from a Microsoft SMTP server with protonmail and a source ip of 185.70.40.140.

![5) investigating the email headers, we see the original sender  domain and IP](https://github.com/user-attachments/assets/c1f9f04c-e15c-44a6-81ad-9f733f1babc3)

<br />
<br />
I used whois.domaintools to reverse dns search the suspicious ip and found its origination of Switzerland. 

![6) whois domain lookup shows email originating form switzerland, reverse dns research](https://github.com/user-attachments/assets/af9540c1-cd6f-4a4f-ac84-461af99cab0c)

<br />
<br />
I enumerated similar artifacts by parsing the email header into a message header analyzer tool. 

![7) parsing the email header from sublime into a header analyzer tool](https://github.com/user-attachments/assets/1fe5ec6e-e8a7-4549-9861-92041342c393)

<br />
<br />
I analyzed a second phishing email from CIBC Bank. Immediately I noticed the domain and the company name didn't match. 

![8) examining sample email2, domain does not match bank name](https://github.com/user-attachments/assets/5a2b5877-6d77-4605-a7b8-e808837b49ea)
<br />
<br />
Reading the email header in sublime showed a different return path from sender. 

![9) return path is a different email address](https://github.com/user-attachments/assets/759b4121-515d-457d-86c3-3c8e0326c2b5)
<br />
<br />
The received headers showed a comcastbusiness domain and a sender IP of 190.6.201.67.

![10) comcastbusiness from received ehaders with sender ip](https://github.com/user-attachments/assets/1a152e41-2a4d-4847-a9b2-1ea1e10d040d)
<br />
<br />
Whois.domaintools showed a reverse DNS looking from Honduras. 

![11) reverse dns lookup shows originating ip from honduras, not cibc bank](https://github.com/user-attachments/assets/5d65a975-ad51-440d-848b-fadc9739b10e
<br />
<br />
