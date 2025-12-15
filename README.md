Objective:

The objective of this task is to configure and test basic firewall rules to allow or block network traffic using a firewall tool. This task helps in understanding how firewalls filter network traffic and improve system security.

Tools Used:

	Operating System: Kali Linux (VirtualBox)
	Firewall Tool: UFW (Uncomplicated Firewall)
	Testing Tool: Telnet

Firewall Configuration Steps:
    1. Checking Firewall Status
        First, the firewall status was checked to verify whether UFW was active.
		        sudo ufw status

    2.Enabling the Firewall:
        UFW was enabled to start filtering network traffic.
		        sudo ufw enable
	
    3.Blocking Insecure Port (Telnet – Port 23):
        Inbound traffic on port 23 (Telnet) was blocked because Telnet transmits data in plaintext and is considered insecure.
		        sudo ufw deny 23
     
    4.Allowing Secure Port (SSH – Port 22):
        SSH traffic was explicitly allowed to ensure secure remote access.
		        sudo ufw allow 22

    5. Viewing Active Firewall Rules:
        The current firewall rules were listed to verify the configuration.
		        sudo ufw status numbered

    6.Testing the Firewall Rule:
        The Telnet service was tested locally to confirm that port 23 was successfully blocked.
		        telnet localhost 23

        Result: Connection refused, confirming that the firewall rule is working correctly.

    7.Removing the Test Rule (Restoring State):

	      As required, the test rule blocking port 23 was removed after verification.
		        sudo ufw delete <rule-number>

     This step restores the firewall to its original secure configuration while keeping SSH access enabled.

Evidence:

    Screenshots have been added to the repository showing:

	Firewall rules applied
	Port 23 blocked
	Successful firewall testing
	Final firewall status

Key Concepts Learned:

	Firewall configuration and management
	Inbound traffic filtering
	Importance of blocking insecure ports
	Difference between allowed and denied services
	How UFW simplifies firewall management

Outcome:

	Successfully configured firewall rules
	Blocked insecure Telnet service (Port 23)
	Allowed secure SSH service (Port 22)
	Verified firewall functionality through testing
	This task provided hands-on experience with firewall management and improved understanding of network security fundamentals.

Conclusion:

    Firewalls play a crucial role in protecting systems from unauthorized access. Proper configuration of firewall rules significantly enhances system security by controlling network traffic based on predefined policies.# task-4-firewall
