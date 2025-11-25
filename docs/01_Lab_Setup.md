
---

## 🚀 Setup Steps
1. **Provision VMs**
   - Create Windows Server, Windows Client, Firewall, and Attacker VMs.
2. **Install Splunk Enterprise Free**
   - Deploy on strongest host or dedicated VM.
3. **Install Splunk Universal Forwarder**
   - On Windows Server and Client VMs.
   - Configure to forward Security Event Logs.
4. **Configure Firewall**
   - Enable logging for inbound/outbound traffic.
   - Forward logs to Splunk.
5. **Verify Connectivity**
   - Ensure Splunk receives logs from all sources.
   - Run test searches to confirm ingestion.

---

## 📝 Notes
- Keep VM resources minimal (1–2 GB RAM each) to reduce overhead.
- Splunk Free is capped at **500 MB/day**, which is sufficient for homelab testing.
- Document screenshots of VM setup, Splunk dashboard, and firewall rules for portfolio evidence.

---

**Tagline:**  
*“Lean but lethal — 3 VMs, one SIEM, endless detection drills.”*
