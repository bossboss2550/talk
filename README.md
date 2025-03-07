# talk

[Unit]
Description=My Project
After=network.target

[Service]
User=pi
WorkingDirectory=/home/pi/myproject
ExecStart=/home/pi/myproject/venv/bin/uvicorn main:app --host 0.0.0.0 --port 8000
Restart=always

[Install]
WantedBy=multi-user.target
