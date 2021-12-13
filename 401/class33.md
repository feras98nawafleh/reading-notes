# JSON Web Tokens
JSON web token (JWT), pronounced "jot", is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. Again, JWT is a standard, meaning that all JWTs are tokens, but not all tokens are JWTs.

Because of its relatively small size, a JWT can be sent through a URL, through a POST parameter, or inside an HTTP header, and it is transmitted quickly. A JWT contains all the required information about an entity to avoid querying a database more than once. The recipient of a JWT also does not need to call a server to validate the token.

Benefits
There are benefits to using JWTs when compared to simple web tokens (SWTs) and Security Assertion Markup Language (SAML) tokens.

More compact: JSON is less verbose than XML, so when it is encoded, a JWT is smaller than a SAML token. This makes JWT a good choice to be passed in HTML and HTTP environments.
![image](https://images.ctfassets.net/cdy7uua7fh8z/4S6xl4Yvi0H1CUrLB69ZtH/e3e3bf1767d2d29563a99cf71cab158d/comparing-jwt-vs-saml2.png)
More secure: JWTs can use a public/private key pair in the form of an X.509 certificate for signing. A JWT can also be symmetrically signed by a shared secret using the HMAC algorithm. And while SAML tokens can use public/private key pairs like JWT, signing XML with XML Digital Signature without introducing obscure security holes is very difficult when compared to the simplicity of signing JSON. Read more about JWT signing algorithms.

More common: JSON parsers are common in most programming languages because they map directly to objects. Conversely, XML doesn't have a natural document-to-object mapping. This makes it easier to work with JWT than SAML assertions.

Easier to process: JWT is used at internet scale. This means that it is easier to process on user's devices, especially mobile.

Use
JWTs can be used in various ways:

Authentication: When a user successfully logs in using their credentials, an ID token is returned. According to the OpenID Connect (OIDC) specs, an ID token is always a JWT.

Authorization: Once a user is successfully logged in, an application may request to access routes, services, or resources (e.g., APIs) on behalf of that user. To do so, in every request, it must pass an Access Token, which may be in the form of a JWT. Single Sign-on (SSO) widely uses JWT because of the small overhead of the format, and its ability to easily be used across different domains.

Information Exchange: JWTs are a good way of securely transmitting information between parties because they can be signed, which means you can be sure that the senders are who they say they are. Additionally, the structure of a JWT allows you to verify that the content hasn't been tampered with.

Security
The information contained within the JSON object can be verified and trusted because it is digitally signed. Although JWTs can also be encrypted to provide secrecy between parties, Auth0-issued JWTs are JSON Web Signatures (JWS), meaning they are signed rather than encrypted. As such, we will focus on signed tokens, which can verify the integrity of the claims contained within them, while encrypted tokens hide those claims from other parties.

In general, JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA (although Auth0 supports only HMAC and RSA). When tokens are signed using public/private key pairs, the signature also certifies that only the party holding the private key is the one that signed it.

Before a received JWT is used, it should be properly validated using its signature. Note that a successfully validated token only means that the information contained within the token has not been modified by anyone else. This doesn't mean that others weren't able to see the content, which is stored in plain text. Because of this, you should never store sensitive information inside a JWT and should take other steps to ensure that JWTs are not intercepted, such as by sending JWTs only over HTTPS, following best practices, and using only secure and up-to-date libraries.
Running Django on the App Engine standard environment 
Django apps that run on App Engine standard environment scale dynamically according to traffic.

This tutorial assumes that you're familiar with Django web development. If you're new to Django development, it's a good idea to work through writing your first Django app before continuing.

While this tutorial demonstrates Django specifically, you can use this deployment process with other Django-based frameworks, such as Wagtail and Django CMS.

This tutorial uses Django 3, which requires at least Python 3.7. App Engine standard supports Python 3.7 and higher.

Objectives
In this tutorial, you will:

Create and connect a Cloud SQL database.
Create and use Secret Manager secret values.
Deploy a Django app to App Engine standard.
Costs
This tutorial uses the following billable components of Google Cloud:

App Engine
Cloud SQL
Secret Manager
To generate a cost estimate based on your projected usage, use the pricing calculator. New Google Cloud users might be eligible for a free trial.
Before you begin
If you're new to Google Cloud, create an account to evaluate how our products perform in real-world scenarios. New customers also get $300 in free credits to run, test, and deploy workloads.
In the Google Cloud Console, on the project selector page, select or create a Google Cloud project.

Note: If you don't plan to keep the resources that you create in this procedure, create a project instead of selecting an existing project. After you finish these steps, you can delete the project, removing all resources associated with the project.
Go to project selector

Make sure that billing is enabled for your Cloud project. Learn how to confirm that billing is enabled for your project.

Enable the Cloud SQL Admin API, Secret Manager, and Cloud Build APIs.
Enable the APIs

Install and initialize the Cloud SDK.
