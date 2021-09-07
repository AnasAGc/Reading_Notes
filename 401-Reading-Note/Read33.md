# JSON Web Tokens

JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.
json can be used as an intermediary between different programming languages

JSON Web Tokens  used when :
Authorization : Request permission to access and use the device's media
Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties

JSON Web Token structure  :
- Header
- Payload
- Signature

## DRF JWT Authentication

JWT stand for JSON Web Token and it is an authentication strategy used by client/server applications where the client is a Web application , The JWT is an authorization token that should be included in all requests .
The validity period it gives is limited so the included must be repeated each time

Installation 
`pip install djangorestframework_simplejwt`
Then add the models in the settings file
Import the framework in path file :
`from rest_framework_simplejwt import views as jwt_views`
