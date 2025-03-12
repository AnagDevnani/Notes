# Introduction:
> An app is computer software, or a program, most commonly a small, specific one used for mobile devices. The term app originally referred to any mobile or desktop application, but as more app stores have emerged to sell mobile apps to smartphone and tablet users, the term has evolved to refer to small programs that can be downloaded and installed all at once
	- Techopedia

- An app can be classified based on the Platform (Desktop, Mobile, Web, Embedded...)
- Software Development Kits (SDKs) integrate with other parts of the machine such that the user doesn’t have to carry out any integration manually.
- Applications Programming Interface (APIs) <font color=red >do something and have something called an</font> API call.
- Cocoa Touch is an example of an Apple specific framework.

# The 3 pillars of an App
1. Storage
	- Component where we can store our application data temporarily or permanently
2. Computation
	- Performs calculation and background tasks on the data.
3. Presentation
	- Used to display a list of information that is formatted and presentable to the end user.

# Network Architectures
## 1. Client-Server:
### Components
1. Server
	-  Stores Data
	-  Provides Data on Demand
	-  May perform computation on the data.
2. Clients:
	- End Users
	-  Request Data
	-  User Interface / Display
3.  Network
	- Connects clients to the server
	- Can be local
	- Datapipe - No alterations

### Client-Server Model
- Explicit differentiation between clients and servers.
- Local Systems:
	- both client and server on same machine
	- conceptually still a networked system.
- Machine Clients:
	- A client need not necessarily be a user.
	- Need not have user interaction.
	- e.g. Software Updaters.
- Variants:
	- Multiple servers
	- Single queue
	- Multiple queues
	- Load balancing frontends
## 2. Peer-to-Peer
A network in which data flows both ways.
- All peers are considered equivalent.
	- but some may be more equal to others.
- Error Tolerance
	- Masters / introducers
	- Election / re-selection of masters on failure.
- Shared information

# Software Architecture Patterns
What is a design pattern:
> A general, reusable solution to a commonly occuring problem within a given context in software design.

- Experienced designers observe "patterns" in code.
- Reusing these patters can make deisgn and development faster.
- Guide the design and thought process.


## Model-View-Controller (MVC) Paradigm
Originates from Smalltalk language (1979)
1. Model:
	- Core data to be stored for the application.
	- Databases; indexing for easy searching, manipulation.
	- It is therefore responsible for adding, deleting, updating and fetching data from the database.
2. View:
	- User-facing side of application.
	- Interfaces for finding manipulation.
		- therefore, the view does not always refer to what the user can see, it is simply the medium that the user uses to interact with the data in the model.
	- The developer can create multiple views of a model.
3. Controller:
	- "Business Logic" how to manipulate data.

There are many other design paradigms such as:
- Model-View-Adapter
- Model-View-Presenter
- Model-View-Viewmodel
- Hierarchical MVC
- Presentation-Abstraction-Control
- ...

Each has its uses, but fundamentals are similiar and is not covered here.

# Introduction to the Web
- Works across operating systems, hardware arcitectures.
- Built on some underlying principles.

### Protocol
- describes how the client and server communicates with each other.
	- A server expects requests
	- A client expects responses
- How to format packets, place them on the wire, headers / checksums.
- Each network had its own protocol.

### "Inter" Network
- How to communicate between different protocols
- Or replace them witha a single "inter"net protocol

### IP: Internet Protocol (1983)
- Defines headers, packet types, interpretation
- Can be carried over different underlying networks: Ethernet, DECnet, PPP, SLIP
- There are 32 bits in an IPv4 address.
- There are 128 bits in an IPv6 address.

### TCP: Transmission Control Protocol (1983)
- Establish reliable communications: retry, error control
- Automatically scale and adjust to network limits.

### Domain Names (1985)
- Use names instead of IP address
- Easy to remember - `.com` still used

### HyperText (1989+)
- Text documents to be "served"
- Formatting hints inside the documents to "link" to other documents.

## Original web limitations:
- Static pages
- complicated executable interfaces
- limited styling
- browser compatibality issues

## Web 2.0 (2004+)
- dynamic pages - generate on the fly
- HTTP as a transport mechanism - binary data, serialized objects
- client side computation and rendering
- platform agnostic operating system. (agnostic means doesnt matter, basically platform independent)

# How does the web work?
- Any computer with a network connection can act as a server.
- Software:
	- Listen for incoming network connections on a fixed port.
	- Respond in specific ways
	- Opening network connections, ports etc. already known to OS.
- Protocol:
	- What should the client ask server.
	- How should the server respond to the client.

## HTTP: HyperText Transfer Protocol
- Largely text based: client sends request, server responds with hypertext document.
- Requests specified as "GET", "POST", "PUT", etc.
	- GET:
		- simple requests from the server, search queries etc.
		- In GET method, data is visible in the url.
	- POST:
		- more complex data, large text blocks, file uploads.
	- PUT / DELETE / ... :
		- Rarely used in Web 1.0 and is instead used extensively in Web 2.0
		-  It forms the basis of most APIs - REST, CRUD
	- Headers can be used to convey acceptable response types, languages, encoding.
	- Which host to connect to (If multiple hosts on a single server).
- Response headers:
	- convey message type, data
	- cache information
	- status codes (404, 200, 301, etc)
- it is a stateless protocol.
- It generally uses port 80 for communication.
## Simplest Server
```unix
while true; do
	echo -e "HTTP/1.1 200 OK\n \n $(date)" |
		nc -l localhost 1500;
done
```

In the given example:
- while true; do (line 1) is simply placing lines 2 and 3 in an endless loop
- `echo -e` is outputting the string which is redirected by the `|` symbol to `nc`
- `nc` is netcat which tells the OS to listen (`-l`) for a client that will connect to the localhost at port 1500. 

### General Web Server
- Listen on a fixed port
- On incoming request, run some code and return a request:
	- Standard headers to be sent as part of result.
	- Output can be text or other format like MIME (Multipurpose Internet Mail Extensions)

### Viewing responses with curl
- curl wget etc. - simple command line utilities
- Can perform full HTTP requests
- Verbose output includes all headers. 
	- very useful for debugging.

## Simple web server with python
```unix
python -m html.server

```

In the given example:
- python is used to execute (`-m`) the server function from the html module which does the following:
	- sets up a local server on localhost (0.0.0.0) at port 8000
	- serves files from local folder.
	- understands basic HTTP requests
	- Gives more detaied headers and responses.

### Driver code for replit
- Will trigger the html files and will allow them to be hosted:
```python
import http.server
httpd = http.server.HTTPServer(("", 8000), http.server.SimpleHTTPRequestHandler)

httpd.server_forever()

```

## Serving HTML files on LAN
```unix
touch file //will create a new file
```
# Performance of a Site
## Latency
- Speed of light:
- in a vacuum: $3\times10^8\text{ m/s}$
- in a cable: $2\times10^8\text{ m/s}$
	- Therefore the speed is around (for one-way) $2\text{ ns/m}$ ~ $5\text{ ms/1000 km}$

## Response Size
- Response = say 1KB of text (headers, HTML, CSS, JS)
- Network Connection  = say 100Mbps = 10MB/s
- Therefore max number of connections = 10000 requests / second

# Markup
