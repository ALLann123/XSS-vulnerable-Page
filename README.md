# XSS-vulnerable-Page
The Web page is vulnerable to stored XSS which is the most severe.

# Brief Introduction to cross site scripting(xss)
This is a type of improper input validation vulnerability which allows the attacker to inject client-side scripts to web pages. It occurs because the broser has no way to know the script should be trusted. Attackers can use this to access any cookies, session token, sensitive information and also redirect user to download malware.
The types of XSS include stored XSS, reflected XSS, self XSS, bind XSS and DOM-Based XSS.

# Stored XSS
Happens when a user input is stored inthe server and retrived unsafely. For this vulnerability to work we need to locate a vulnerability inthe web application and then inject malicious script to the server. Once the malicious script is injected to the vulnerable web site it is activated when a user visits the site as the browser unintentionally runs the malicious payload.

# Vuln Page
The web page above demostrates stored XSS and can be exploited as its vulnerable.
To set up the web application we first start by locating /var/www/html file which will use apache2 to host the site:

    kali> sudo cd /var/www/html
    kali> sudo git clone https://github.com/ALLann123/XSS-vulnerable-Page.git

Give permissions to the web page"
    
    kali> sudo chmod 644 /var/www/html/stored_xss.html
    kali> sudo chown www-data:www-data /var/www/html/stored_xss.html
start apache2 server

    kali>sudo systemctl start apache2

Onthe web application you scan test for the vulnerability as whatever payload you will run will be loaded by every user who visits the page.
![xss 1](https://github.com/user-attachments/assets/22e29e8e-3ee1-4d9a-8c61-e57427572315)

The javascript code I used <script>prompt()</script>
![stored xss](https://github.com/user-attachments/assets/717b5b98-c47e-4c9d-b038-9f91420af172)


    
