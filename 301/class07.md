# What Google Learned From Its Quest to Build the Perfect Team
Like most 25-year-olds, Julia Rozovsky wasn’t sure what she wanted to do with her life. She had worked at a consulting firm, but it wasn’t a good match. Then she became a researcher for two professors at Harvard, which was interesting but lonely. Maybe a big corporation would be a better fit. Or perhaps a fast-growing start-up. All she knew for certain was that she wanted to find a job that was more social. ‘‘I wanted to be part of a community, part of something people were building together,’’ she told me. She thought about various opportunities — Internet companies, a Ph.D. program — but nothing seemed exactly right. So in 2009, she chose the path that allowed her to put off making a decision: She applied to business schools and was accepted by the Yale School of Management.
One of her favorite competitions asked teams to come up with a new business to replace a student-run snack store on Yale’s campus. Rozovsky proposed a nap room and selling earplugs and eyeshades to make money. Someone else suggested filling the space with old video games. There were ideas about clothing swaps. Most of the proposals were impractical, but ‘‘we all felt like we could say anything to each other,’’ Rozovsky told me. ‘‘No one worried that the rest of the team was judging them.’’ Eventually, the team settled on a plan for a micro­gym with a handful of exercise classes and a few weight machines. They won the competition. (The micro­gym — with two stationary bicycles and three treadmills — still exists.)
# REST Explained
Who is “Roy Fielding”? He helped write the first web servers, that sent documents across the internet… and then he did a ton of research explaining why the web works the way it does. His name is on the specification for the protocol that is used to get pages from servers to your browser.
 HTTP—this protocol Fielding and his friends created—is all about applying verbs to nouns. For instance, when you go to a web page, the browser does an HTTP GET on the URL you typed in and back comes a web page.

Web pages usually have images, right? Those are separate resources. The web page just specifies the URLs to the images and the browser goes and does more GETs using the HTTP protocol on them until all the resources are obtained and the web page is displayed. But the important thing here is that very different kinds of nouns can be treated the same. Whether the noun is an image, text, video, an mp3, a slideshow, whatever. I can GET all of those things the same way given a URL.
## GET
GET requests are the most common and widely used methods in APIs and websites. Simply put, the GET method is used to retreive data from a server at the specified resource. For example, say you have an API with a /users endpoint. Making a GET request to that endpoint should return a list of all available users.

Since a GET request is only requesting data and not modifying any resources, it's considered a safe and idempotent method.
## POST
In web services, POST requests are used to send data to the API server to create or update a resource. The data sent to the server is stored in the request body of the HTTP request.

The simplest example is a contact form on a website. When you fill out the inputs in a form and hit Send, that data is put in the response body of the request and sent to the server. This may be JSON, XML, or query parameters (there's plenty of other formats, but these are the most common).

It's worth noting that a POST request is non-idempotent. It mutates data on the backend server (by creating or updating a resource), as opposed to a GET request which does not change any data. 
## PUT
Simlar to POST, PUT requests are used to send data to the API to update or create a resource. The difference is that PUT requests are idempotent. That is, calling the same PUT request multiple times will always produce the same result. In contrast, calling a POST request repeatedly make have side effects of creating the same resource multiple times.

Generally, when a PUT request creates a resource the server will respond with a 201 (Created), and if the request modifies existing resource the server will return a 200 (OK) or 204 (No Content).
## PATCH
A PATCH request is one of the lesser-known HTTP methods, but I'm including it this high in the list since it is similar to POST and PUT. The difference with PATCH is that you only apply partial modifications to the resource.

The difference between PATCH and PUT, is that a PATCH request is non-idempotent (like a POST request).

To expand on partial modification, say you're API has a /users/{{userid}} endpoint, and a user has a username. With a PATCH request, you may only need to send the updated username in the request body - as opposed to POST and PUT which require the full user entity.
