# IT Support Home Lab — Troubleshooting Runbook

**Author:** Md Tanjil Sarwar  
**Environment:** VMware Home Lab (Ubuntu Server 24.04 + Windows 10 Client)  
**Date:** January 2026

---

## Issue 1: Cannot Connect to Company WiFi

- **Reported by:** John Smith
- **Priority:** High
- **Symptoms:** User laptop not connecting to office WiFi, other devices working fine
- **Steps taken:**
  1. Verified issue isolated to one device
  2. Checked if IP address was being assigned using `ipconfig`
  3. Instructed user to forget the network — Settings → Network → WiFi → Forget
  4. User reconnected and entered password again
- **Resolution:** Successfully reconnected after forgetting and rejoining network
- **Status:** Resolved

---

## Issue 2: Outlook Not Opening — Error on Startup

- **Reported by:** Sarah Johnson
- **Priority:** Normal
- **Symptoms:** Outlook throws "Cannot open the Outlook window" error on every launch
- **Steps taken:**
  1. Asked user to restart — issue persisted
  2. Ran Outlook in safe mode — `outlook.exe /safe`
  3. Disabled faulty add-ins found in safe mode
  4. Rebuilt Outlook profile via Control Panel → Mail → Show Profiles → Add
- **Resolution:** Corrupt profile rebuilt, Outlook opened successfully
- **Status:** Resolved

---

## Issue 3: User Locked Out After Password Expiry

- **Reported by:** Mike Davis
- **Priority:** High — user had urgent meeting
- **Symptoms:** User completely locked out of Windows account after ignoring password expiry notice
- **Steps taken:**
  1. Verified account status in Active Directory
  2. Unlocked account and reset temporary password
  3. Instructed user to change password on next login
  4. Advised user to set up password expiry reminders going forward
- **Resolution:** Account unlocked, user logged in with temporary password and set new one
- **Status:** Resolved

---

## Server Maintenance Commands (Reference)

| Command | What it Does |
|---|---|
| `sudo systemctl status apache2` | Check web server status |
| `sudo systemctl restart apache2` | Restart web server |
| `sudo systemctl status mysql` | Check database status |
| `sudo ufw status verbose` | Check firewall rules |
| `sudo ufw allow [port]/tcp` | Open a port |
| `sudo ufw deny [port]/tcp` | Block a port |
