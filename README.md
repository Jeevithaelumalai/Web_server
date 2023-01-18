# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:

```
from http.server import HTTPServer,BaseHTTPRequestHandler

content="""
<html>
<head>
</head>
<body>
<h1>Top five web application development frameworks.</h1>
     <ol>
      <li>django</li>
      <li>MEAN Stack</li>
      <li>MERN Stack</li>
      <li>ASP.NET core</li>
      <li>Spring Framework</li>
      </ol>

</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('content-type','text/html; charset=uft-8')
        self.end_headers()
        self.wfile.write(content.encode())


server_address=('',80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()

```

## OUTPUT:
   
   # Top five web application development frameworks.
     1. django
     2.MEAN Stack
     3.MERN Stack
     4.ASP.NET core
     5.Spring Framework
 
 
 
 ![GitHub Logo](/images/d.png)
     
     
   

## RESULT:
  Thus a webserver developed to display about top five web application development frameworks
