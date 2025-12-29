Troubleshooting Guide: "No Internet Access"
Objective

Provide a standardized workflow for Tier 2 technicians to diagnose connectivity issues on Windows workstations.

Diagnostic Steps

Physical Layer: Verify link lights on the NIC and docking station.

IP Configuration: Run ipconfig /all

Self-Assigned IP (169.254.x.x)? Indicates a DHCP failure.

Valid IP? Proceed to Step 3.

Connectivity Test: Ping the Gateway (e.g., ping 192.168.1.1). If successful, the local network is fine.

DNS Resolution: Run nslookup google.com. If it fails, flush the DNS cache: ipconfig /flushdns
