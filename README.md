# EX01 Developing a Simple Webserver
## Date:

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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
    a{
        padding: 10px;
        text-decoration: wavy;
        color:black;
        font-family: Arial, Helvetica, sans-serif;
        font-size: 18px;

    }
    a:hover{
        color: gray;
    }
    i:hover{
            color: grey;
        }
</style>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
</head>
<body style="background-color: blue;">
        <div class="col-5">
            <i class="bi bi-twitter-x icon"></i>
            <i class="bi bi-youtube icon"></i>
            <i class="bi bi-facebook icon"></i>
            <i class="bi bi-instagram icon"></i>
            <i class="bi bi-whatsapp icon"></i>
            <i class="bi bi-linkedin icon"></i>
        </div>
    <div style="display: flex;">
        <div style="width: 25%;">
            <img style="width: 100%;" src="ipl-logo-new-old.png" alt=""/>
        </div>

    <div style="width: 55%; padding-top: 20px;">
        <a href="">Home</a>
        <a href="">About</a>
        <a href="">booking</a>
        <a href="https://www.iplt20.com/matches/fixtures">schedule</a>
    
    </div>
    <div style="width: 20%;padding-top: 8px;">
        <input style="width: 80%;height: 30px;background-image: url(search.png);
        background-size: contain;background-repeat: no-repeat;border-radius: 15px;padding-left: 40px;" type="text" placeholder="search">
    </div>
    </div>

    <h1 style="text-align: center;">INDIA'S BIGGEST FESTIVAL IS COMING</h1>
    <div style="display: flex;">
        <div style="width: 100%;">
            <div style="display: flex;">
                <div></div>
            </div>
            <div style="width: 100%;" id="carouselExample" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-inner">
                  <div class="carousel-item active">
                    <img src="csk.jpeg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="mi.jpeg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="rcb.jpeg" class="d-block w-100" alt="...">
                  </div>
                  <div class="carousel-item">
                    <img src="kkr.jpeg" class="d-block w-100" alt="...">
                  </div>
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
                  <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                  <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
                  <span class="carousel-control-next-icon" aria-hidden="true"></span>
                  <span class="visually-hidden">Next</span>
                </button>
              </div>
              <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
        
        </div>
    </div>
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
Name:Shyam Kumar.E

Register Number: 212223230207
![Screenshot 2024-03-25 160527](https://github.com/Romanshyam/simplewebserver/assets/123962992/90392c14-c4b1-4f72-a888-02770b8c1f5f)
![Screenshot 2024-03-25 160211](https://github.com/Romanshyam/simplewebserver/assets/123962992/a889390c-4bf1-48a5-bb70-71744f348c84)




## RESULT:
The program for implementing simple webserver is executed successfully.
