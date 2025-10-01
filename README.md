# Windows Firewall: Block Port 23 (Telnet) and Test

1. Open firewall advanced settings:
   - Press Win + R, type firewall.cpl, Enter
   - Click “Advanced settings” → “Inbound Rules”

2. Create a new rule:
   - Click “New Rule…” → Select “Port” → Next
   - Choose TCP, enter 23 → Next
   - Select “Block the connection” → Next
   - Check Domain, Private, Public → Next
   - Name it “Block Telnet 23” → Finish

3. Test blocking port 23:
   - Open Command Prompt and run:
     telnet localhost 23
   - Connection should fail

4. Remove the rule to restore settings:
   - Right-click “Block Telnet 23” in “Inbound Rules” → Delete

5. (Optional) Disable Telnet Client:
   - Control Panel → Programs and Features → Turn Windows features on or off → Uncheck Telnet Client → OK

---

Firewall filters network connections by rules; matching traffic is allowed or blocked based on ports, protocols, and profiles.
