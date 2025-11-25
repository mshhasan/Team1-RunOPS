

# Network Connectivity Troubleshooting Guide

## Symptoms
- Cannot access network resources
- "Network unreachable" errors
- Intermittent connectivity

## Quick Checks

1. **Verify physical connection**

   ```bash
   # Check network interface status
   ip link show
   # or on Windows: ipconfig /all


2. **Test local connectivity**

   ping 127.0.0.1  # Test loopback
   ping <gateway-ip>  # Test gateway


3. **Check DNS resolution**
   nslookup google.com
   # or: dig google.com

4. **Verify network configuration**
   Check IP address assignment (DHCP vs static)
   Confirm subnet mask
   Verify default gateway



****Common issues and their solutions****

Issue: No IP address assigned

Solution:
1.	Restart network service
2.	Check DHCP server status
3	Verify network cable connection


Issue: Can ping by IP but not by hostname
Solution:
1.	Check DNS server configuration
2.	Verify /etc/resolv.conf (Linux) or DNS settings (Windows)
3.	Flush DNS cache


Issue: Firewall blocking connectivity
Solution:
1.	Check firewall rules
2.	Temporarily disable firewall rules to test (re-enable after testing)
3.	Add necessary exceptions


****When to Escalate****
Multiple users affected
Hardware failure suspected
Problem persists after all checks
Network infrastructure changes needed
