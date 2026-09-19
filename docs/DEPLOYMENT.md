# Deployment & Operations Guide: Product Zombie

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-product-zombie-e6d159/](/preview/prod-product-zombie-e6d159/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T19:05:05.667057+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=Product Zombie Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-13/test_zombie_running_state_self0/workspaces/prod-product-zombie-e6d159
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-13/test_zombie_running_state_self0/workspaces/prod-product-zombie-e6d159/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.
