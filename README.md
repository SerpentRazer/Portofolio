Security Site Analysis Report for License Documentation
This report details a comprehensive security site analysis for the domain bogdanmihalca.com, focusing on its network and application-level security measures. The analysis involved multiple stages including port scanning, WHOIS information gathering, and penetration testing to evaluate the robustness of the security implementations.

1.Technologies and Web Server Configuration
The technologies used by bachelordiplomaproject.gatsbyjs.io were identified using builtwith.com. The site utilizes:

JavaScript Frameworks: Gatsby (v4.15.2) and React
Miscellaneous: Module Federation, HTTP/2, PWA (Progressive Web App), and Webpack
Web Servers: Apache Traffic Server
Caching: Varnish
CDN: Fastly
Static Site Generators: Gatsby

2.Port Scanning
A SYN Stealth Scan was conducted on 185.224.137.220, revealing numerous open ports and associated services. Notably, ports for common services such as HTTP (80/tcp), HTTPS (443/tcp), and MySQL (3306/tcp) were open, alongside a variety of other ports supporting different services:

21/tcp (FTP)
80/tcp (HTTP)
443/tcp (HTTPS)
1433/tcp (MSSQL)
3306/tcp (MySQL)
6667/tcp (IRC)

These results indicate a wide array of services potentially vulnerable to exploitation if not properly secured. Each open port represents a potential entry point for attackers, making it crucial to ensure all services are up-to-date and configured with secure protocols.

3.WHOIS Information Gathering
WHOIS data revealed that the IP address belongs to Hostinger International Limited, a hosting service provider based in Cyprus. Detailed contact information for the provider was obtained, which is essential for coordination in case of security incidents:

bogdanmihalca.com is registered through GoDaddy with privacy protection.
bachelordiplomaproject.gatsbyjs.io is a GatsbyJS project hosted on a Fastly CDN.
Hostinger International Limited is the service provider for bogdanmihalca.com, with contact details available for incident response coordination:
Organisation: Hostinger International Limited
Address: 61 Lordou Vyronos, Lumiel Building, 4th Floor, Larnaca, Cyprus
Phone: +37064503378
The domain registration information further confirmed that bogdanmihalca.com is registered through GoDaddy with privacy protection enabled, obscuring the actual registrant details.

4.Web Application Security Testing
Penetration tests on the web application revealed the following:

5.Cross-Site Scripting (XSS): The application is immune to XSS attacks, indicating that proper input sanitization and encoding mechanisms are in place.

6.SQL Injection: The site is immune to SQL injection attacks. This is achieved by disallowing direct SQL command inputs through the user interface, suggesting the use of prepared statements or ORM (Object-Relational Mapping) for database interactions.

7.Brute Force Attacks: Brute force attacks are not applicable as there is no account creation feature on the site, thereby eliminating the risk of unauthorized access through credential stuffing or password guessing.

8.1.Cookie Manipulation: While cookie manipulation is technically possible, it is deemed ineffective due to the absence of account-related features that could be exploited through session hijacking.

8.2.Cookie Interception and Analysis
A practical demonstration of cookie interception using Burp Suite was performed. The intercepted cookies contained standard session management information with no sensitive data exposed. The server responded with appropriate security headers such as Content-Security-Policy and Strict-Transport-Security, further enhancing the application's resilience against common web vulnerabilities.

9.TTL Protocol: Utilization of TTL protocol makes detection of running services difficult and firewall-blocked ports nearly invisible.

10.Anti-Flooding Measures: Implemented measures erase data packets after a period, enhancing traffic efficiency and data manipulation.

11. Traceroute and OS Detection
Traceroute: The traceroute for 199.232.38.22 revealed 9 hops, indicating the network path and latency between the client and the server.
OS Detection: Nmap scans indicated the possible operating systems running on the target, including various versions of Linux and OpenBSD, although exact matches were not identified due to missing closed TCP ports.

Conclusion and Recommendations
The security site analysis for bogdanmihalca.com demonstrates a well-fortified infrastructure with several proactive measures in place to mitigate common attack vectors. However, continuous monitoring and regular security audits are recommended to maintain and enhance the security posture. Specifically, it is advised to:

Ensure all services running on open ports are updated and configured securely.
Maintain regular vulnerability scans and penetration tests.
Implement robust logging and monitoring to detect and respond to potential threats promptly.
Enhance user session security by employing techniques like Secure and HttpOnly cookie flags and using multi-factor authentication where applicable.
By adhering to these practices, bogdanmihalca.com can ensure the integrity, confidentiality, and availability of its web services.
