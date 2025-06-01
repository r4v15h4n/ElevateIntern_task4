# ElevateIntern_task4
Task 4 : Setup and Use a Firewall on Windows/Linux

used windows firewall for testing firewall traffic

used ward cloudflare for testing inbound traffic

How a Firewall Filters Traffic:
A firewall acts as a gatekeeper between your network (or device) and external networks (like the internet). It filters traffic based on rules set by the user or system admin. 
Here's how it works:
Traffic Inspection: Every data packet entering or leaving your network is checked.

Rule Matching: The firewall compares the packet's details (IP address, port, protocol, etc.) against a set of allow or block rules.

If a rule matches, the firewall allows or blocks the traffic accordingly.
If no rule matches, the default action is taken (usually to block or allow based on config).

What Happens IfTraffic is being blocked from WARP (Cloudflare)?
Device using WARP cannot connect through it: All traffic routed through WARP will be blocked, and the internet may stop working on that device (depending on how WARP is configured).
WARP IP ranges will be denied: The firewall will block known Cloudflare WARP IP addresses, preventing encrypted tunneling.
Fallback to normal internet: If the device is set to fall back to regular DNS/IP routing, it may work without WARP. If not, it will show "No Internet."
