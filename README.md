# Evil_Twin
The provided sources describe an Evil Twin attack involving setting up a fake access point to capture a victim's network key. This methodology outlines the process using the format you provided.

A. Access Point Setup:
1. Identify Target Network: Observe the target network's Wi-Fi name. In the example, the target network is named "net gear 47".

2. Configure Fake Access Point: Use software like Hostapd to broadcast a fake access point mimicking the target network's name.

3. Set up DHCP Server: Implement a DHCP server using software like dnsmasq to assign IP addresses to clients connecting to the fake access point.

4. Configure DNS Server: Configure the DHCP server (dnsmasq) to also function as a DNS server, redirecting all DNS requests to the attacker’s-controlled server.

B. Captive Portal Construction:
1. Prepare Web Server: Set up a web server, such as Apache, to host the captive port
2. Design Captive Portal: Create or customize a web page mimicking a legitimate service, like a firmware update page, requesting the user's Wi-Fi password.
3. Deploy Captive Portal: Place the captive portal files in the appropriate directory for the web server.


C. Credential Capture:
1. Redirect Traffic: Configure the network to redirect all traffic from the fake access point to the captive portal.
2. Password Submission: When the victim connects to the fake access point and attempts to access the internet, they are redirected to the captive portal. Upon entering their password and submitting it, the captive portal captures the credentials.
3.Store Credentials: The captured password is stored in a database for the attacker to retrieve. The example uses MySQL to set up a database and store the passwords.

D. Deauthentication (Optional):
1. Disconnect Victim: Use tools like Airplay-ng to deauthenticate the victim from the legitimate network, forcing them to reconnect and potentially choose the fake access point.

Visual Representations:
● Network Diagram: A visual representation of the network architecture, showing the attacker's machine, the victim's machine, the legitimate router, and the fake access point.

● Captive Portal Screenshot: A screenshot of the fake captive portal page, highlighting the design elements that make it appear legitimate.

● Data Flow Diagram: A diagram illustrating the flow of network traffic from the victim's device, through the fake access point, to the captive portal, and finally to the attacker's database.

While the sources do not directly address edge detection, quadtree construction, dead-end identification, and direction determination, these concepts may be applicable in other contexts, particularly image or video analysis. However, they are not relevant to the Evil Twin attack methodology described in the video.
