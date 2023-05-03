
# Stateless Authentication

- In stateless authentication, a client typically sends its credentials (such as a username and password) to the server to obtain an authentication token. The server validates the credentials and generates a token, which is then returned to the client. The client includes this token in subsequent requests to the server to authenticate itself.

- The authentication token is usually a digitally signed token, such as a JSON Web Token (JWT), that contains encoded information about the user's identity and other relevant data. The server can verify the integrity and authenticity of the token using a secret key or a public key, depending on the token's signature algorithm.

- Since the server does not need to store any session data, the authentication process becomes stateless. Each request contains all the necessary information for the server to authenticate the client, making it scalable and suitable for distributed systems.

## flow diagrams

        +---------+                                   +------------+
        |         |                                   |            |
        |  Client |                                   |   Server   |
        |         |                                   |            |
        +----+----+                                   +------+-----+
             |                                              |
             |          Step 1: Authentication              |
             |          (Sending Credentials)               |
             |-------------------------------------------->|
             |                                              |
             |                                              |
             |          Step 2: Authentication              |
             |          (Generating JWT Token)               |
             |<--------------------------------------------|
             |                                              |
             |          Step 3: Token Response               |
             |<--------------------------------------------|
             |                                              |
             |                                              |
             |          Step 4: Token Storage                |
             |                                              |
             |                                              |
             |                                              |
             |          Step 5: Subsequent Requests          |
             |          (Including JWT Token)                |
             |-------------------------------------------->|
             |                                              |
             |                                              |
             |          Step 6: Token Verification           |
             |                                              |
             |                                              |
             |                                              |
             |          Step 7: Response                     |
             |<--------------------------------------------|
             |                                              |


## advantages and disadvantages: 

### advantages:

