# AL-QAESAR-TOOL9
#!/usr/bin/env python3
import os
import sys
import time

def clear_screen():
    os.system('clear')

def animated_banner():
    colors = ["\033[1;31m", "\033[1;36m", "\033[1;32m"]

    skull = [
        "       ▇◤▔▔▔▔▔▔▔◥▇       ",
        "       ▇▏▃▆▅▎▅▆▃▕▇       ",
        "       ▇▏╱▔▕▎▔▔╲▕▇       ",
        "       ▇◣◣▃▅▎▅▃◢◢▇       ",
        "       ▇▇◣◥▅▅▅◤◢▇▇       ",
        "       ▇▇▇◣╲▇╱◢▇▇▇       "
    ]

    for i in range(3):
        clear_screen()
        c = colors[i % len(colors)]
        print(c + "="*72)
        for line in skull:
            print(line.center(72))
        print("="*72 + "\033[0m")
        time.sleep(0.1)

    clear_screen()
    
    CYAN = '\033[0;36m'
    BLUE = '\033[0;34m'
    GREEN = '\033[0;32m'
    PURPLE = '\033[0;35m'
    YELLOW = '\033[1;33m'
    BG_GREEN = '\033[42;1;30m'
    BG_YELLOW = '\033[43;1;30m'
    NC = '\033[0m'

    # Al-Qaesar Large Text Header
    print(CYAN + "   █████╗ ██╗      ██████╗  █████╗ ███████╗███████╗ █████╗ ██████╗   ")
    print("  ██╔══██╗██║     ██╔═══██╗██╔══██╗██╔════╝██╔════╝██╔══██╗██╔══██╗  ")
    print("  ███████║██║     ██║   ██║███████║█████╗  ███████╗███████║██████╔╝  ")
    print("  ██╔══██║██║     ██║   ██║██╔══██║██╔══╝  ╚════██║██╔══██║██╔══██╗  ")
    print("  ██║  ██║███████╗╚██████╔╝██║  ██║███████╗███████║██║  ██║██║  ██║  ")
    print("  ╚═╝  ╚═╝╚══════╝ ╚═════╝ ╚═╝  ╚═╝╚══════╝╚══════╝╚═╝  ╚═╝╚═╝  ╚═╝  " + NC)
    
    print(BLUE + "="*72 + NC)
    print(f"          {BG_GREEN}       AL-QAESAR AL-YAMANI TOOL       {NC}")
    print(f"          {BG_YELLOW}     Advanced Network Analysis System   {NC}")
    print(BLUE + "="*72 + NC)
    print(f"  {GREEN}[ MOBILE PHONE ]{NC}         {CYAN}[ RADIO SIGNALS ]{NC}         {GREEN}[ MOBILE TOWER ]{NC}")
    print("  +--------------+               ( ( (               +--------------+")
    print("  |  [SIM Card]  |==============>>>>>==============>>|     ||||     |")
    print("  |              |<<<<<==============<<<<<===========|     ||||     |")
    print("  |     (o)      |               ) ) )               |    /    \\    |")
    print("  +--------------+                                   +--------------+")
    print("  ----------------------------------------------------------------------")
    print(f"                                             {PURPLE}[ INTERNET NETWORK / CLOUD ]{NC}")
    print("                                             +-------------------------+")
    print("                                             |     INTERNET SERVER     |")
    print("                                             |       [=========]       |")
    print("                                             |        [WEBSITE]        |")
    print("                                             +-------------------------+")
    print(BLUE + "="*72 + NC)
    print(f"  {YELLOW}[+] OWNER:{NC} AL-QAESAR AL-YAMANI        {YELLOW}[+] SHELL:{NC} PYTHON & BASH")
    print(f"  {YELLOW}[+] SYSTEM:{NC} ONLINE                    {YELLOW}[+] STATUS:{NC} KING OF TERMUX")
    print(BLUE + "="*72 + NC)
    print("")

tools_list = [
    # --- SECTION 1: NETWORK SCANNING & RECON ---
    {'name': 'Nmap (Advanced Network Mapper)', 'cmd': 'pkg install nmap -y'},
    {'name': 'Masscan (Ultra-fast TCP Port Scanner)', 'cmd': 'pkg install masscan -y'},
    {'name': 'ZMap (Internet-wide Network Scanner)', 'cmd': 'pkg install zmap -y'},
    {'name': 'Hping3 (Custom TCP/IP Packet Crafting)', 'cmd': 'pkg install hping3 -y'},
    {'name': 'Tshark (Terminal Wireshark Packet Analyzer)', 'cmd': 'pkg install tshark -y'},
    {'name': 'Arp-scan (Local Subnet Device Discovery)', 'cmd': 'pkg install arp-scan -y'},
    {'name': 'Netcat (The TCP/IP Swiss Army Knife)', 'cmd': 'pkg install netcat -y'},

    # --- SECTION 2: SOCIAL ENGINEERING & CAPTURE ---
    {'name': 'Zphisher (Automated Phishing Suite)', 'cmd': 'git clone --depth 1 https://github.com/htr-tech/zphisher.git'},
    {'name': 'SocialFish (Phishing & Credential Testing)', 'cmd': 'git clone --depth 1 https://github.com/UndeadSec/SocialFish.git'},
    {'name': 'PyPhisher (Modern Advanced Phishing Tool)', 'cmd': 'git clone --depth 1 https://github.com/KasRoudra/PyPhisher.git'},
    {'name': 'MaxPhisher (All-in-one Link Phishing Kit)', 'cmd': 'git clone --depth 1 https://github.com/KasRoudra/MaxPhisher.git'},
    {'name': 'CamHacker (Camera Shot Phishing Link Simulator)', 'cmd': 'git clone --depth 1 https://github.com/KasRoudra/CamHacker.git'},
    {'name': 'Seeker (Accurate GPS Location OSINT Webhook)', 'cmd': 'git clone --depth 1 https://github.com/thewhiteh4t/seeker.git'},
    {'name': 'SayCheese (Target Webcam Capture Simulator)', 'cmd': 'git clone --depth 1 https://github.com/htr-tech/saycheese.git'},
    {'name': 'TrackUrl (Ngrok Webhook Tunnel Link Wrapper)', 'cmd': 'git clone --depth 1 https://github.com/htr-tech/trackurl.git'},

    # --- SECTION 3: WEB AUDITING & INJECTION ---
    {'name': 'Sqlmap (Automated SQL Injection & DB Takeover)', 'cmd': 'git clone --depth 1 https://github.com/sqlmapproject/sqlmap.git'},
    {'name': 'Nikto (CGI and Vulnerability Web Server Scanner)', 'cmd': 'git clone --depth 1 https://github.com/sullo/nikto.git'},
    {'name': 'WPScan (WordPress Security & Plugin Auditor)', 'cmd': 'pkg install ruby -y && gem install wpscan'},
    {'name': 'Dirsearch (Web Directory & Path Brute-Forcer)', 'cmd': 'pkg install git python -y && git clone --depth 1 https://github.com/maurosoria/dirsearch.git'},
    {'name': 'Commix (Automated Command Injection Exploiter)', 'cmd': 'git clone --depth 1 https://github.com/commixproject/commix.git'},
    {'name': 'WhatWeb (Web Server Technology Fingerprinter)', 'cmd': 'pkg install whatweb -y'},
    {'name': 'Gobuster (DNS, VHost, and Directory Buster)', 'cmd': 'pkg install gobuster -y'},
    {'name': 'Xren (Cross-Site Scripting Vulnerability Finder)', 'cmd': 'git clone --depth 1 https://github.com/TheRealXren/Xren.git'},

    # --- SECTION 4: INFORMATION GATHERING & OSINT ---
    {'name': 'PhoneInfoga (Global Phone Number Intelligence)', 'cmd': 'curl -sSL https://raw.githubusercontent.com/sundowndev/phoneinfoga/master/support/install.sh | bash'},
    {'name': 'Sublist3r (Fast Subdomain Enumeration Tool)', 'cmd': 'git clone --depth 1 https://github.com/aboul3la/Sublist3r.git'},
    {'name': 'TheHarvester (Scrape Emails, Subdomains & Names)', 'cmd': 'git clone --depth 1 https://github.com/laramies/theHarvester.git'},
    {'name': 'Sherlock (Hunt Social Media Accounts by Username)', 'cmd': 'git clone --depth 1 https://github.com/sherlock-project/sherlock.git'},
    {'name': 'Amass (In-depth Network & Mapping OSINT Engine)', 'cmd': 'pkg install amass -y'},
    {'name': 'Infoga (Email Information & Intelligence Gatherer)', 'cmd': 'git clone --depth 1 https://github.com/m4ll0k/Infoga.git'},
    {'name': 'OSINT-Spy (Comprehensive Intelligence Analysis)', 'cmd': 'git clone --depth 1 https://github.com/SharadKumar97/OSINT-Spy.git'},
    {'name': 'TikTok-Report-Bot (Account Integrity Auto-Check)', 'cmd': 'git clone --depth 1 https://github.com/0xYoussef/TikTok-Report-Bot.git'},

    # --- SECTION 5: PASSWORD AUDITING & WORDLISTS ---
    {'name': 'Hydra (Fast Parallel Network Login Cracker)', 'cmd': 'pkg install hydra -y'},
    {'name': 'John the Ripper (Multi-format Password Cracker)', 'cmd': 'pkg install john -y'},
    {'name': 'Hashcat (Advanced GPU/CPU Password Recovery)', 'cmd': 'pkg install hashcat -y'},
    {'name': 'Crunch (Custom Wordlist & Password Generator)', 'cmd': 'pkg install crunch -y'},
    {'name': 'Medusa (Parallel Modular Authentication Auditor)', 'cmd': 'pkg install medusa -y'},
    {'name': 'Cupp (Common User Passwords Profiler - Target Based)', 'cmd': 'git clone --depth 1 https://github.com/Mebus/cupp.git'},
    {'name': 'Ncrack (High-speed Network Authentication Auditing)', 'cmd': 'pkg install ncrack -y'},

    # --- SECTION 6: SYSTEM DEPLOYMENT & EXPLOITS ---
    {'name': 'Metasploit Framework Automated Deployment Script', 'cmd': 'pkg install wget curl openssh -y && wget https://github.com/gushmazuko/metasploit_in_termux/raw/master/metasploit.sh && chmod +x metasploit.sh'},
    {'name': 'Apktool (Reverse Engineering Android Applications)', 'cmd': 'pkg install apktool -y'},
    {'name': 'Bytecode-Viewer (APK Java Source Code Decompiler)', 'cmd': 'pkg install openjdk-17 -y && wget https://github.com/Konloch/bytecode-viewer/releases/download/v2.12/Bytecode-Viewer-2.12.jar'},
    {'name': 'Routersploit (Exploitation Framework for IoT Devices)', 'cmd': 'git clone --depth 1 https://github.com/reverse-shell/routersploit.git'},
    {'name': 'Spaghetti (Web Application Security Assessor Tool)', 'cmd': 'git clone --depth 1 https://github.com/m4ll0k/Spaghetti.git'},
    {'name': 'Wifite2 (Automated Wireless Attack Script Suite)', 'cmd': 'git clone --depth 1 https://github.com/kimocoder/wifite2.git'},
    {'name': 'Tool-X (Universal Termux Multi-Tool Installer)', 'cmd': 'git clone --depth 1 https://github.com/Rajkumrdusad/Tool-X.git'},

    # --- SECTION 7: CORE ENVIRONMENT OPTIMIZATION ---
    {'name': 'Core Update: Run pkg update && pkg upgrade', 'cmd': 'pkg update && pkg upgrade -y'},
    {'name': 'Core Libs: Install pip, pip3 & python-dev updates', 'cmd': 'pkg install python-pip python-dev -y && pip install --upgrade pip'},
    {'name': 'Core Nets: Install curl, wget, git, dnsutils tools', 'cmd': 'pkg install curl wget git dnsutils -y'},
    {'name': 'Core Mirror: Launch Repository Mirror Manager', 'cmd': 'termux-change-repo'},
    {'name': 'Core Purge: Clear broken system and app temp caches', 'cmd': 'rm -rf $TMPDIR/* && apt clean && apt autoremove -y'}
]

def main():
    while True:
        animated_banner()
        print("\033[1;35m--- Available Cyber Security Tools & Scripts (50 Tools) ---\033[0m\n")

        # Double column layout arrangement for easier mobile reading
        for idx in range(0, len(tools_list), 2):
            t1 = f"\033[1;32m[{idx+1:02d}]\033[0m {tools_list[idx]['name']}"
            if idx + 1 < len(tools_list):
                t2 = f"\033[1;32m[{idx+2:02d}]\033[0m {tools_list[idx+1]['name']}"
                print(f"{t1:<55} {t2}")
            else:
                print(t1)

        print("\n\033[1;35m[88]\033[0m Set Al-Qaesar Interface as Default Termux Startup Welcome Banner")
        print("\033[1;31m[00]\033[0m Exit Elite Cyber Suite")
        print("\033[1;36m" + "="*72 + "\033[0m")
        
        choice = input("\033[1;33mAl-Qaesar >> Enter tool number to initialize setup [00-50 / 88]: \033[0m").strip()

        if choice == '0' or choice == '00':
            print("\n\033[1;31m[!] Shutting down Al-Qaesar Cyber Suite. Safe Exit.\033[0m\n")
            sys.exit()

        if choice == '88':
            print("\n\033[1;32m[*] Configuring startup environment...\033[0m")
            try:
                script_path = os.path.abspath(sys.argv[0])
                home = os.environ.get("HOME", "/data/data/com.termux/files/home")
                bashrc_path = os.path.join(home, ".bashrc")
                
                # Setup required startup system credits notice in Bash
                welcome_msg = (
                    '\n'
                    'echo -e "\\033[1;33m========================================================================\\033[0m"\n'
                    'echo -e "\\033[1;32m   Termux System Developed By AL-QAESAR AL-YAMANI The Legend King of Termux\\033[0m"\n'
                    'echo -e "\\033[1;33m========================================================================\\033[0m"\n'
                    f'python3 {script_path}\n'
                )

                already_exists = False
                if os.path.exists(bashrc_path):
                    with open(bashrc_path, "r") as f:
                        if f"python3 {script_path}" in f.read():
                            already_exists = True
                
                if not already_exists:
                    with open(bashrc_path, "a") as f:
                        f.write(welcome_msg)
                    print("\033[1;32m[+] Success! Custom startup banner has been locked into your Termux terminal.\033[0m")
                else:
                    print("\033[1;33m[!] Startup configuration is already injected.\033[0m")
            except Exception as e:
                print(f"\033[1;31m[!] Configuration failed: {e}\033[0m")
            time.sleep(2)
            continue

        try:
            tool_idx = int(choice) - 1
            if 0 <= tool_idx < len(tools_list):
                selected_tool = tools_list[tool_idx]
                print(f"\n\033[1;33m[*] Launching process for: {selected_tool['name']}...\033[0m")
                print(f"\033[1;34m[Command]: {selected_tool['cmd']}\033[0m\n")
                time.sleep(1)
                os.system(selected_tool['cmd'])
                print(f"\n\033[1;32m[+] Process finished for {selected_tool['name']}.\033[0m")
                input("\nPress Enter to return to the list...")
            else:
                print("\033[1;31m[!] Out of index range. Please enter a valid tool number.\033[0m")
                time.sleep(1.5)
        except ValueError:
            print("\033[1;31m[!] Input error: Please enter a numeric value.\033[0m")
            time.sleep(1.5)

if __name__ == "__main__":
    main()
