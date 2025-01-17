# EX01 Developing a Simple Webserver
## Date:23\03\2024

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
      <head> 
            <title>Top Software Companies Revenue</title>
      </head>
      <body>
      <table border="4" cellspacing="5" width="40" heigth="50"
        <caption>REVENUE</caption>
        <tr>
             <th>Rank</th>
             <th>company name</th>
             <th>Website</th>
             <th>Total employee</th>
        </tr>
        <tr>
             <td>337</td>
             <td>construction software technology</td>
             <td>www.cst.com</td>
             <td>170</td>
        </tr>
        <tr>
             <td>338</td>
             <td>cosmocom</td>
             <td>www.cosmo.com</td>
             <td>150</td>
        </tr>
        <tr>
             <td>339</td>
             <td>macadamian.inc</td>
             <td>www.cro.com</td>
             <td>140</td>
        </tr>
        <tr>
             <td>340</td>
             <td>Dexler Chamey</td>
             <td>www.dextrr.com</td>
             <td>180</td>
        </tr>
        <tr>
             <td>341</td>
             <td>Replicon</td>
             <td>www.replicon.com</td>
             <td>138</td>  
        </tr>
        </table>
        </body>
        </html>      

"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:
![alt text](<Screenshot 2024-03-18 160123.png>)
![alt text](<web exp 1.png>)

## RESULT:
The program for implementing simple webserver is executed successfully.
