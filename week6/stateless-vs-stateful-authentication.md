## Session-based vs. Token-based authentication 

aka Stateful vs. Stateless

aka Cookies vs JSON Web Tokens()JWTs)


---


**HTTP protocol** defines how messages are formatted and transmitted, and what actions browsers and servers should take after various commands.

HTTP is **stateless**: each request is unaware of any previous action. 

What does this mean?


---


![socks](https://wwwcdn.bigcommerce.com/www1.bigcommerce.com/assets/bigcommerce-seriously-silly-socks-product.png?mtime=20180131160830)


---


If you log into an account like FaceBook or Twitter and navigate to a differnet page, default HTTP would mean you would have to log in again.

With session-based or token-based authentication you can tell the server you are already logged in.


---


## Session-based/Stateful Authentication

The User's *State* is stored in the server memory:

* User logs in
* Server creates and stores session data
* Server sends cookie with Session ID to store in the browser


---

## Stateless protocol 
Stateless protocol is a communications protocol in which no session information is retained by the receiver

## session
In computer science,networking in particular,session is a temporary and interactive information interchange between two or more communicating devices, or between a computer and user


---

### Advantages
* Lower server overhead: less stress on the server the session data stored in the client side the server does not need to handle it.
* Integrates with 3rd party apps easly: becuase the seesion stored in the browser so the 3rd party apps can easly get the seeison information
* Easy to scale:As long as the servers share the same private key then all servers have the same capability to verify the validity of the session it does not matter which backend server the request is routed to. 

---

### Disadvantages
* Cannot revoke the session anytime: Since the user session is stored at client side, the server does not have any rights to delete the session.
* Relatively complex to implement for one-session-server scenario: The advantages of stateless authentication is scalability. However, it increases the technical complexity and it is not extremely useful when we only have one-session-server.
* Session data cannot be changed until its expiration time.


---


## When to Use each?

It is possible to use either method or create a hybrid system.

Most modern web apps use JWT(stateless) for authentication, particularly for mobile devices.


---



### RESTful APIs
By definition should be stateless.  Traditional approach of using sessions and cookies won't work.

### Secure Data Transfer
JWTs can also be used to securely transmit info between parties because they can be signed.

You can verify who the sender is and that the content hasn't changed because the signature is calculated using the header and payload.


---



## How JWTs are constructed

JSON Web Tokens (JWTs) consist of the following User Data which which encoded/encrypted together:

* headers
* payload
* a 'secret'
* then sent back to the client.  

User state stored on the client, usually in localStorage. 

'Secret' is a digital signature: HMAC algorithm or a public/private key pair using RSA.

[Internet Engineering Task Force spec for JWT](https://tools.ietf.org/html/rfc7519)



---



# Example headers

```  
headers:{
  "Authorization": "Bearer ${JWT_TOKEN}"
}
```
```
{
  "alg": "HS256",
  "typ": "JWT"
}
```


---



## Example Payload

Payload is Base64Url encoded to form the second part of the JWT.


```
{
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
```


---




## Example Signature

Example Payload created using the encoded header, encoded payload, a secret (the specificed algorithm: HMAC SHA256), which is then signed:

```
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)
```


---
## Example Encoded JWT

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c
```


[see example JWT and libraries](https://jwt.io/)


---





## Node Modules for JWT


**jsonwebtoken** to create the JWT token on the server

**express-jwt** - middleware to validate the JWT token by comparing the secret.



---



## Performance and Security

More data is encoded in the JWT which creates more overhead for each HTTP request.  Session IDs are very small.  However, there is a server-side lookup to find and parse the session on each request.

JWTs trade size for latency by keeping the data on the client side:
* be careful to not store too much info in a JWT to avoid large, slow requests
* be careful to not store sensitive info 

Tokens might also require access to the database on the backend, such as for 'refresh' requests. 
[more info on refresh tokens](https://auth0.com/blog/refresh-tokens-what-are-they-and-when-to-use-them/)



---


JWT is created using JSON which is has many options for parsing to an Object, libraries, and is secure.

XML may create unwanted security holes when parsing, and doesn't map easily to a usable Object.


---



## Conclusion


JSON Web Tokens (JWTs) are generally preferred for web sessions, but as always consider the architecture of your app to decide what is best for you.

Comments: Marko mentioned that JSON Web Tokens can be used together with cookies (as we will do in tomorrow's workshop), so it is not really an 'either...or´ situation.

[Medium Article on  Session vs. token-based authentication](https://medium.com/@sherryhsu/session-vs-token-based-authentication-11a6c5ac45e4)

[more info about JWT's from auth0](https://auth0.com/learn/json-web-tokens/)

