## Why do we need REST 

So imagine that you have a bunch of toys, and your friend wants to borrow one of your toys. 

Your friend sends you a message saying, "Can I borrow your toy car?" You look for the toy car, and then send a message back saying, "Here's the toy car you wanted!"

In the same way, REST API is like a messenger that helps different computer programs talk to each other. One program can ask another program for information or data, like your friend asking for the toy car. The other program looks for the information or data and sends it back, like you finding the toy car and sending it back to your friend.

REST API has rules that both programs follow to make sure they understand each other. It's like having a set of instructions to follow when you and your friend are talking about the toy car. The instructions make it easier for both of you to communicate and understand what the other one wants.

## Step by step process

Sure, here's a step-by-step process for how a REST API works:

1.  A client sends a request to a server using HTTP (the Hypertext Transfer Protocol), which is a way of sending and receiving data over the internet.
    
2.  The server receives the request and checks if it's valid. If the request is valid, the server processes it and prepares a response.
    
3.  The server sends the response back to the client using HTTP. The response typically includes the data that the client requested, along with metadata that describes the data (like the data format and any additional information).
    
4.  The client receives the response and checks the HTTP status code to see if the request was successful. If the status code indicates success (usually 200 or 201), the client can use the data that was returned in the response.
    
5.  If the client wants to make changes to the data, it can send a new request to the server using one of the standard HTTP methods (like POST, PUT, or DELETE) to create, update, or delete data. The server will process the request and send back a response with a status code that indicates whether the request was successful.
    
6.  The client can continue to send requests and receive responses from the server as needed, using the HTTP methods to interact with the data in different ways.
    

> [!NOTE] RestAPI
> REST API is a way for different programs to communicate with each other over the internet using standard HTTP requests and responses. 

The server receives requests from the client, processes them, and sends back responses with data and metadata. The client can use the data returned in the response, and can also send new requests to create, update, or delete data. The communication is standardized and follows a set of rules to ensure that the programs can understand each other.

## Reference video 

Reference - [Rest architecture](https://www.youtube.com/watch?v=-mN3VyJuCjM)





