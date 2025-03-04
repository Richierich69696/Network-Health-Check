# Network-Health-Check
Hey, I’m Raj—Master’s in Info Systems and Security, network nerd at heart. This project’s a simple way to check your home network’s health without writing a single line of code. It’s all about spotting weak spots—like open ports or slow devices—using free tools. No fancy stuff, just practical digging!


What’s the Big Idea?

Your Wi-Fi’s like a house—doors (ports) and pipes (speed). I use tools to peek at what’s open, what’s slow, and what’s acting weird. It’s a no-code health checkup for your network.

How I Made It Happen

Here’s my easy plan, like I’m showing you on my laptop:

1. Map the Network: Used Angry IP Scanner to see every device on my Wi-Fi—like my phone, router, smart TV.
   Example: Found my router at 192.168.1.1, TV at 1.50.

2. Check Open Doors: Ran Nmap to see what ports are open on each device—like windows a hacker could climb through.
   Example: Router had port 80 open (web admin page)—might need locking!

3. Test the Pipes: Used Speedtest’s desktop app to check if my internet’s chugging or cruising.
   Example: Got 50 Mbps down—good enough, but my TV’s laggy, so maybe it’s the Wi-Fi signal.

4. Write It Down: Jotted notes in a text file—what’s on, what’s open, what’s slow.
   Example: “Router: 192.168.1.1, port 80 open. TV: 1.50, slow response.”

Stuff You’ll Need

Angry IP Scanner: Free from angryip.org—finds devices.
Nmap: Free from nmap.org—checks ports.
Speedtest: Free desktop app from speedtest.net—tests speed.
Your Wi-Fi: Just your home network.
Notepad: Built into your computer—no extra download.

Let’s Do It—Step by Step with Commands

1. Get Tools:
   - Angry IP Scanner: Go to angryip.org, click “Download,” pick your OS (Windows/Mac), install it.
   - Nmap: Hit nmap.org, download, run the installer—easy wizard.
   - Speedtest: speedtest.net, click “Desktop App,” install it.

2. Set Up Folder: You’re in RajCyberAIProjects/NetworkHealthCheck—awesome!
   Command: No coding, but in command line, type “cd RajCyberAIProjects\NetworkHealthCheck” (Windows) or “cd RajCyberAIProjects/NetworkHealthCheck” (Mac) to get here if you’re poking around.

3. Scan Devices: Open Angry IP Scanner, type “192.168.1.1-255” in the IP range box, hit “Start.” Takes a minute—lists all devices.
   Save it: File > Save as “devices.txt” in this folder.

4. Check Ports: Open command line, type “nmap 192.168.1.1” (swap with your router’s IP from step 3), hit enter. See what’s open.
   Example output: “80/tcp open http”—web port’s up. Save it: Type “nmap 192.168.1.1 > ports.txt” to dump it here.

5. Test Speed: Open Speedtest app, click “Go”—wait 30 seconds, note your download/upload speeds in Notepad as “speed.txt.”
   Example: “Down: 50 Mbps, Up: 10 Mbps.”

6. Review: Open your three .txt files—spot anything odd like open ports or slow speeds.

Bumps in the Road

No Devices: If Angry IP Scanner’s blank, check your Wi-Fi’s connected.
Nmap Blocked: Firewall might stop it—run as admin (right-click cmd, “Run as administrator”).
Speed Lies: Test a few times—Wi-Fi can be moody.

Why I Love It

It’s a quick, no-code way to know my network’s pulse. Shows off my troubleshooting chops!
