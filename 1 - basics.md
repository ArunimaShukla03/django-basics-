Django is a python web franmework that allows us to write python code that is able to dynamically generate HTML and CSS, ultimately allowing us to build a dynamic web application.

We are creating a software that is going to run on a web server such that clients running in their web browsers can make requests to our web server and server responds with some kind of response accordingly.

This is possible due to a protocol called HTTP (HyperText Transfer Protocol) which is responsible for how messages are going to be sent back and forth over the internet.

In this, we have a server which contains the web application and the computer which is known as the client. The client is going to make a request to the server and the server will generate some kind of response based on the request.

The request might be like 

 GET/HTTP/1.1
 Host: www.example.com
 ...

(here GET is an example of request method, a way you might try to get a page)

This request is ultimately sent by the web browser when you type in the URL.

The response will generally look like

HTTP/1.1 200 OK
Current-type: text/html
...