# EX01 Developing a Simple Webserver

# Date:17.09.2025
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
Name: DHARSHIN M
Roll No: 25018496

```
from http.server import HTTPServer,BaseHTTPRequestHandler
content ="""
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        
        *{
            font-family: 'Times New Roman';
        }
            .head{
            text-align: center;
            font-size: larger;
            font-weight: 300;
            text-decoration: underline;
            
        }
    </style>
</head>
<body bgcolor="black" text="white">
    <p class="head">MY LAPTOP SPECIFICATIONS</p>
    <pre>
Model: ASUS TUF A15

Processor: AMD Ryzen 5

Graphics: NVIDIA GeForce RTX 2050 (4GB GDDR6 VRAM)

Display: 15.6" FHD (1920x1080) 144Hz IPS-level

Memory: 8GB DDR4 RAM (expandable)

Storage: 512GB NVMe SSD

Keyboard: RGB Backlit Keyboard

Cooling: Self-cleaning cooling system with anti-dust technology

Battery: 90Wh battery

OS: Windows 11 Home

Ports: USB 3.2, USB Type-C, HDMI 2.0b, RJ-45 Ethernet, audio combo jack

Connectivity: Wi-Fi 6, Bluetooth 5.2

Durability: MIL-STD-810H military standard

Weight: 2.30 kg (5.07 lbs)
</pre>
</body>
</html>
"""
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type", "text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()

```
# OUTPUT:
<img width="1262" height="644" alt="Screenshot 2025-09-25 081903" src="https://github.com/user-attachments/assets/cc17df95-b54a-49b9-b99f-4a91788a322b" />

<img width="1259" height="674" alt="Screenshot 2025-09-25 081951" src="https://github.com/user-attachments/assets/d1741664-9871-4cce-805c-2211dd06bab2" />


# RESULT:
The program for implementing simple webserver is executed successfully.
