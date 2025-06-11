# SSH Honeypot Dashboard

This project captures and visualizes brute-force login attempts to an SSH honeypot. The backend logs attacks and aggregates statistics; the frontend provides a public dashboard with masked attacker data.

## 🔐 Honeypot Overview

* **Honeypot Tool**: [`ssh-honeypot`](https://github.com/droberson/ssh-honeypot)
* **Logging Port**: Incoming port 22 redirected to 2223 via iptables
* **Secure Admin Access**: Custom SSH port (2222) with public key authentication
* **Cloud Computing**: Akamai Linode utilized to host Ubuntu machine.

## 📊 Dashboard Features

* Interactive **log table** with masked passwords and redacted IPs
* **Graphs** for top attempted usernames and passwords (powered by Chart.js)
* **Stats**: total login attempts and total unique attacker IPs
* Toggle graphs on/off for cleaner viewing

Live demo: [https://your-username.github.io/your-repo-name](https://your-username.github.io/your-repo-name)

## 📁 Project Structure

```
.
├── index.html        # Public dashboard (GitHub Pages)
├── app.py            # Flask API server for logs + stats
├── redact_logs.py    # Redaction script for publishing logs
├── /logs             # Contains redacted logs (optional)
├── /static           # (Optional) for CSS or JS files
└── README.md
```

## ⚠️ Ethical Considerations

This project is strictly for **educational and research purposes**. It does **not** target or harm any external systems. All data collected is:

* Passively obtained from unsolicited login attempts
* Never used for retaliation or unauthorized access

Please ensure your honeypot runs on a secure, isolated host. Never deploy one on a production server.

## 🧐 Future Considerations

* 🔄 **Live auto-refresh** of logs and charts
* 🌎 **GeoIP** map of attacker locations
* 📅 **Filter by date** range or time windows
* 🧠 **ML anomaly detection** on login patterns
* ☁️ Host backend Flask API with HTTPS (e.g., via Heroku/Fly.io)

---

## 💬 Questions or Ideas?

Feel free to fork or submit an issue if you’d like to expand this project or share thoughts!

---

> Built with 🐍 Flask, ⚡ iptables, and ❤️ for infosec
