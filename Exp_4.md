# Exprement_4: Analyze Email Headers and Detect Email Spoofing using MHA (Mail Header Analyzer) 
## Aim and Description
The aim of using an email header analyzer like MHA (Mail Header Analyzer) is to decode the raw, complex text of an email header into a readable format. This helps in forensic analysis, network troubleshooting, and, most importantly, detecting email spoofing. Email spoofing is a technique used in phishing and spam where the sender forges the "From" address to make an email appear as if it came from a legitimate or trusted source. An analyzer simplifies the process by highlighting key information and identifying inconsistencies that a human might miss.
![alt text](<screenshorts/Exp_4/Screenshot (20).png>)

## Tools and Equipment
Computer: A desktop or laptop with an internet connection.

Email Client: An email client or webmail service (like Gmail, Outlook, etc.) to access the suspicious email.

Mail Header Analyzer (MHA) Tool: This is typically a web-based tool. Examples include Google Admin Toolbox's Messageheader, MXToolbox Email Header Analyzer, or various open-source versions found on platforms like GitHub. These tools require no installation; you just need to copy and paste the email header.
![alt text](<screenshorts/Exp_4/Screenshot (21).png>)

## Procedure
The process is divided into two main parts: getting the full header and then analyzing it with the tool.

Extract the Email Header: The first step is to get the full, raw header from the suspicious email. The method for this varies by email client:

Gmail: Open the email, click the three-dot menu next to the "Reply" button, and select Show original.

Outlook: Double-click the email to open it in a new window, go to File > Properties, and look for the "Internet headers" field.

Other clients: The option is usually labeled "View Source," "Show Original," or "View Full Headers."

Copy the entire block of text from the header, including all the "Received," "Authentication-Results," and other lines.

Analyze with MHA:

Open your chosen MHA tool in a web browser.

Paste the copied email header into the designated text box.

Click the Analyze or Parse button.
![alt text](<screenshorts/Exp_4/Screenshot (22).png>)
## Result
The MHA tool will parse the raw header and present a clean, organized report. To detect spoofing, you should focus on the following key results:

From Address Mismatch: Compare the "From" address shown in your email client's display with the "Return-Path" or the first "Received" entry. A mismatch is a major red flag. For instance, if an email appears to be from "Microsoft" but the return path is malicioususer@attacker.com, it's a clear case of spoofing.

Authentication Results: Look for headers like Authentication-Results. Modern email systems use protocols like SPF (Sender Policy Framework), DKIM (DomainKeys Identified Mail), and DMARC (Domain-based Message Authentication, Reporting, and Conformance) to verify a sender's legitimacy. If the SPF or DKIM checks Fail for a legitimate domain, it's a strong indicator of spoofing.
![alt text](<screenshorts/Exp_4/Screenshot (22).png>)

IP Address and Server Path: Analyze the Received headers. These headers form a chain, showing the path the email took from the sending server to your mail server. Check the IP address of the first "Received" header. You can use an IP lookup tool to see if the IP's geographic location or ISP matches the supposed sender. An email from a U.S. company with an IP address from a different country is highly suspicious.

Header Inconsistencies: Look for unusual headers, multiple headers of the same type (e.g., two "Message-ID" headers), or illogical timestamps. Legitimate email clients generate clean, predictable headers. Sloppy or malformed headers often indicate a manual or scripted attempt to forge an email.

![alt text](<screenshorts/Exp_4/Screenshot (23).png>)
Sources
