[Unit]
Description=Audience Check-In Web
After=network.target

[Service]
ExecStart=/usr/bin/node /home/rpi/checked-in-system/audience-check-in/frontend/audience-check-in-web/server.js
WorkingDirectory=/home/rpi/checked-in-system/audience-check-in/frontend/audience-check-in-web
Restart=always
User=rpi
Group=rpi
Environment=PATH=/usr/bin:/usr/local/bin
Environment=NODE_ENV=production

[Install]
WantedBy=multi-user.target
