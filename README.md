
# Generate, Capture, Analyze, then Decrypt HTTPS Traffic

## Description

In this project, we explore the intricate process of generating, capturing, analyzing, and decrypting HTTPS traffic using the powerful network protocol analyzer, Wireshark. The primary goal is to shed light on the vulnerabilities associated with unencrypted communication and emphasize the significance of secure transmission in today's digital landscape.


## Languages and Utilities Used:

* Linux commands
* Wireshark
## Project Walkthrough:

**Filtering HTTPS Traffic (Port 443):**

* Initiate the capture on port 443 using Wireshark.
* Double click on Ethernet 3 and ensure the correct interface is selected.
* Generate traffic by opening Google Chrome and browsing to a website.
* Capture stopped.

![App Screenshot](https://i.imgur.com/SrXXuuj.jpg)


**Application Data Encryption:**

* Explore captured packets, focusing on application data packets.
* Expand TLS (Transport Layer Security) to identify encrypted HTTP over TLS.
* Emphasize the inability to decrypt due to the lack of a private key.

![App Screenshot](https://i.imgur.com/38f19gl.jpg)

**Setting Up SSL Key Log File:**

* Set an environment variable in Windows for SSLKEYLOGFILE.
* Specify the location for the key log file on the desktop.
* Verify the file creation.

![App Screenshot](https://i.imgur.com/w34yHcn.jpg)

![App Screenshot](https://i.imgur.com/Zs1ycdH.jpg)

**Creating SSL Key Log File:**

* Demonstrate the process of creating the SSL key log file for decryption.


![App Screenshot](https://i.imgur.com/ZeobmnG.jpg)

**Configuring Wireshark Preferences:**

* Navigate to Wireshark preferences and locate TLS.
* Specify the pre-master secret log file name as the created SSL key log file.

![App Screenshot](https://i.imgur.com/pGCHtGB.jpg)

**Capturing HTTPS Traffic and Testing:**

* Start capturing HTTPS traffic on port 443.
* Open a simple site in the browser to generate traffic.
* Stop the capture and analyze the conversations.

![App Screenshot](https://i.imgur.com/5VotdMd.jpg)

![App Screenshot](https://i.imgur.com/msMIl0A.jpg)


**Decrypting HTTPS Traffic:**

* Ping the server to identify the specific conversation.
* Follow the stream to observe unencrypted data.
* Highlight the ability to see previously encrypted details.

![App Screenshot](https://i.imgur.com/jNyQTsH.jpg)

![App Screenshot](https://i.imgur.com/QiycSZv.jpg)









## Project Summary:

In the this project, we systematically addressed the security concerns associated with unencrypted network traffic, specifically focusing on HTTPS. The project covered the capture of encrypted data, the setup of SSL key logs for decryption, and the successful analysis of decrypted HTTPS traffic using Wireshark. The steps demonstrated the importance of securing sensitive information during network communication and showcased practical methods for decrypting and analyzing encrypted traffic.
