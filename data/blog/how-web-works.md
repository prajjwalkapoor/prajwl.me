---
title: How Web Works!
date: '2022-09-25'
tags: ['web']
draft: false
summary: Have you ever thought about what is happening behind the scenes after entering www.google.com on your browser? How does the browser know you are requesting Google's home page and where is google.com located on the internet? To answer all those questions, you need to understand how web technology works behind the scenes.
---

Have you ever thought about what is happening behind the scenes after entering www.google.com on your browser? How does the browser know you are requesting Google's home page and where is google.com located on the internet? To answer all those questions, you need to understand how web technology works behind the scenes.

# The Client-Server model

![Client Server Model](https://miro.medium.com/max/720/0*kZuLJa3OA0BqtEjv)

So as I have introduced two terms CLIENT and SERVER, let's understand what they are.

CLIENT refers to your browser from where you are requesting a website/resource and the SERVER refers to the computer where the requested website/resource is hosted. Whenever a client sends the request either to get data from the server or to post data on the server. In any of these two cases, the server will respond to that particular request either by providing or posting the desired data with a specific success or error message.

As of now, we have understood that there are two parties between which a connection needs to be established so that they can share data with each other. Now let's look at how your browser knows the address of the server.

# Domain Name System ( DNS )

Let's take the example of your phone's contact list to understand DNS. When you save any contact to your phone, you save it with the name of the server mapped with the number as the name is easier to remember as compared to the number.

DNS works in the same way. The domain name of any website is mapped with the server's IP address to find where the server is located. DNS works as a translator and it translates the domain names to IP addresses so browsers can load Internet resources.

Check out this video by IBM to know about DNS in detail.

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/nyH0nYhMW9M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></p>

After getting the server's IP address, there must be some way to communicate with servers to get the desired resources. Let's look at how client-server communication works.

# HTTP ( HyperText Transfer Protocol )

The Hypertext Transfer Protocol is a network protocol that is based on TCP/IP for the communication between client and server.
The Basic flow is client sends the request to the server to get the resource and then the server gives the response back to the client. The transfer of data takes place in the form of small segments which are called packets.

![Http packets](https://miro.medium.com/max/720/0*oXe5go_NVSj441Gd.jpeg)

**HTTP Headers:**

Whenever you request something from the server or the server is responding to you back, HTTP headers are involved in both cases. HTTP Headers are nothing but the metadata for requests and responses. It carries the information about the request and response.
HTTP Headers are of mainly two types:

- **_Request Headers:_** Carries the information about the request of the client.

![request headers](https://miro.medium.com/proxy/0*DU0ACcNb9CN35_uW.png)

- **_Response Headers:_** Carries the information about the response from the server.
  ![response headers](https://miro.medium.com/max/640/1*RK8k7_CLo6TqoPYczMvk4w.png)

# HTTP Request Methods:

Look at the first line of the above example of a request header, a method is GET defined which means that you are requesting something from the server.

There are mainly four types of HTTP methods:

- **GET →** To get the data from the server
- **POST →** To post the data on the server
- **PUT →** To update the data on the server
- **DELETE →** To delete the data on the server.

There are other methods also but we generally use the above four. You can see the complete list here.

## HTTP Status Codes

HTTP status code shows if the request is fulfilled by the server or not. If it is fulfilled, the server responds with a success status code otherwise it responds with a specific error code.

All the status codes are clubbed together in 5 different subgroups:

1. Informational (100–199)
2. Successful (200–299)
3. Redirection (300–399)
4. Client error (400–499)
5. Server error (500–599)

## HTTP response and request body

The request body is used to send users the data to the server for processing. For example, submitting a form on some website. Similarly, the response body is used to get the data from the server.

# HTTPS ( HyperText Transfer Protocol Secure )

![https](https://miro.medium.com/max/720/1*ItKgwGP5_8wB6_IAtPQ0iA.png)

The main issue of using HTTP is security. Data packets are not encrypted while transmitting and therefore attackers can quickly get access to your data by stealing data packets with a MITM attack. HTTPS is used instead of HTTP to avoid these things.

_HTTPS (HyperText Transfer Protocol Secure)_ is a protocol built over HTTP with security enhancements. Cryptographic principles are introduced in HTTPS so that you can freely transmit data packets without any security issues. The protocol which is used by HTTPS is TLS ( Transport Layer Security ).

To understand what is TLS and how TLS handshake works, we need to know about public-private key encryption.

**Public keys** are used to encrypt sensitive data and anyone can use this to encrypt data but **Private keys** are for the decryption of encrypted data only receivers has access to this only receiver can decrypt the data. So when you visit https://www.google.com, google sends you their public key which is signed by a verified certificate authority ( in this case, google itself ), and then your browser encrypts the data packets with google's public key so that only google can decrypt data packets.

If you are able to see the green lock icon, that means the connection is secured with HTTPS security.
Example of an SSL/TLS certificateAfter all these things, your browser assembles all the data packets and creates an HTML document with CSS and JS files to see the website's main content.

![SSL Certificate](https://miro.medium.com/max/640/1*WnXhJljZ8QHOTkNkXht3Bw.png)

After all these things, your browser assembles all the data packets and creates an HTML document with CSS and JS files to see the website's main content.
