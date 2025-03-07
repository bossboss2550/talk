# talk

[Unit]
Description=My Project
After=network.target

[Service]
User=rpi
WorkingDirectory=/home/rpi/checked-in-system/audience-check-in/backend
ExecStart=/home/rpi/checked-in-system/venv/bin/uvicorn main:app --host 0.0.0.0 --port 8000
Restart=always

[Install]
WantedBy=multi-user.target
