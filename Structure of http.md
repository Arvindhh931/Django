## introduction

An HTTP request typically consists of several parts, including:

Reference1 - [http reference](https://www.webdevdrops.com/en/http-primer-for-frontend-developers-f091a2070637/)
Referecne2 - [scalar http request](https://www.scaler.com/topics/computer-network/hypertext-transfer-protocol/)
Reference3 - [http reference](https://www.realisable.co.uk/support/documentation/iman-user-guide/DataConcepts/WebRequestAnatomy.htm)

1. Request line: The first line of an HTTP request that specifies the 
	1. HTTP method (e.g., **GET**, **POST**, **PUT**, **DELETE**), 
	2. The URL or path of the requested resource
	3. The version of the HTTP protocol being used.
    
2. Headers: Additional metadata that provides information about the request or the client making the request. Headers may include information about the 
	1. content type
	2. encoding
	3. Language
	4. Authentication credentials
	5. caching directives.
    
3. Body: Optional data that may be sent as part of the request, typically used in POST, PUT, and PATCH requests to send data to a server. The body may contain data in various formats such as **JSON**, **XML**, or form data.

![[Screenshot from 2023-03-17 12-11-15.png|750]]

![[Screenshot from 2023-03-17 12-11-09.png | 750]]

## Here's an example of an HTTP request:

```css
GET /example HTTP/1.1
Host: www.example.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.99 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
```

In this example, the request line specifies a GET request for the "/example" resource using HTTP/1.1. The headers include the host name, user agent, and accepted content types and encodings. There is no request body.

