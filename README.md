# Security-Testing

##HTTP Fundamentals
Goals: cURL & Browser DevTools

**In addition to the above, this module will cover:**

- An overview of the HyperText Transfer Protocol (HTTP)
- An overview of the Hypertext Transfer Protocol Secure (HTTPS)
- HTTP requests and responses and their headers
- HTTP methods and response codes
- Common HTTP methods such as GET, POST, PUT, and DELETE
- Interacting with APIs

**Consider learning about:** 

- Introduction to Networking
- Linux Fundamentals


**Sub-topic #1: HyperText Transfer Protocol (HTTP)**

- Internet communications are made with web requests through the HTTP protocol. 
	- OSI Model: HTTP is an application level protocol used to access the WWW resources. 
	- Hypertext: text containing links to other resources
- HTTP communication - client-server model
	- Client requests the server for a resource
	- Server processes the requests and return the requested resource
	- Default port: 80
- URL:
	- Resources over HTTP are accessed via a Uniform Resource Locator (URL)
	- Example:
	![[Screenshot 2024-06-10 at 10.45.09 AM.png]]

		- User info is optional: used to authenticate to the host, separated with @
		- Host: signifies the resource location. It can be a hostname, or an IP address
		- If no port is specified, default is 80 and https is 443
		- Path: Points to resource being accessed, file or folder. If no path specified, server returns index.html
		- Query String: Start with (?), separated by (&)
		- Fragments: Processed by the browsers on the client-side to locate sections within the primary resource. 
	- Mandatory components are SCHEME and HOST

 **HTTP Flow**
![[Screenshot 2024-06-10 at 10.55.05 AM.png]]

"The diagram above presents the anatomy of an HTTP request at a very high level. The first time a user enters the URL (`inlanefreight.com`) into the browser, it sends a request to a DNS (Domain Name Resolution) server to resolve the domain and get its IP. The DNS server looks up the IP address for `inlanefreight.com` and returns it. All domain names need to be resolved this way, as a server can't communicate without an IP address."

"Once the browser gets the IP address linked to the requested domain, it sends a GET request to the default HTTP port (e.g. `80`), asking for the root `/` path. Then, the web server receives the request and processes it. By default, servers are configured to return an index file when a request for `/` is received"

**cURL**
- Stands for client URL: a command-line tool and library that primarily supports HTTP along with other protocols. 
	- Good for scripts and automation
	- Essential for sending various types of web requests from the command line
		- Necessary for pen-testing
- Terminal: 
	- curl "hostname"![[Screenshot 2024-06-10 at 11.04.39 AM.png]]
		- Prints raw format
		- Pentesters are interested in the request and response context
	- Can be used to download a page or a file and output content into a file as below: ![[Screenshot 2024-06-10 at 11.07.23 AM.png]]
			- You can silence output by using -s flag 
			- Use -h flag to see what other options we may use with cURL
	- 
**QUESTIONS**
- How can I access /etc/hosts file to manually add records to for DNS resolutions?
- 
