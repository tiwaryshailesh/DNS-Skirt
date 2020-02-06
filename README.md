# DNS-Skirt

WINDOWS SETUP
--
1. 	Download DNS Setup Windows - x64 x86.zip
2. 	Extract the relevant version int "C:\DNS Skirt"
3. 	Do right click on dnscrypt-proxy in "C:\DNS Skirt\" folder and select "Send to Desktop (Create shortcut)"
4. 	Go to Desktop and Cut the newly created Shortcut.
5. 	Open Run dialog by pressing win+R and type this command
		shell:common startup
6. 	Paste the shortcut in window that opens.
7.	Launch firewall by typing "firewall.cpl" in run dialog win +r
8.	Create and incoming-allowed rule for UDP/53 port.
9.	Allot a fix IP to your system as per local range (say 192.168.1.27)
10.	Use this IP as DNS on other devices in your local net.


LINUX (DEBIAN) SETUP
--
1.	Extract content of BOSS folder to /opt/dnscrypt.
2.	Modify crontab (crontab -e) to include the following line at end
	@reboot /opt/dnscrypt/dnscrypt-proxy
3.	Modify firewall to accpet incoming DNS requests by following command
	sudo ufw allow dns
