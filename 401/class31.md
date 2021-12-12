# Docker
## What is Docker?
ocker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.
Running Docker on AWS provides developers and admins a highly reliable, low-cost way to build, ship, and run distributed applications at any scale.
Recent announcements: Docker collaborates with AWS to help developers speed delivery of modern apps to the cloud. This collaboration helps developers use Docker Compose and Docker Desktop to leverage the same local workflow they use today to seamlessly deploy apps on Amazon ECS and AWS Fargate. Read the blog for more information.
## How Docker Works?
Docker works by providing a standard way to run your code. Docker is an operating system for containers. Similar to how a virtual machine virtualizes (removes the need to directly manage) server hardware, containers virtualize the operating system of a server. Docker is installed on each server and provides simple commands you can use to build, start, or stop containers.

AWS services such as AWS Fargate, Amazon ECS, Amazon EKS, and AWS Batch make it easy to run and manage Docker containers at scale.

## Why Docker?
Using Docker lets you ship code faster, standardize application operations, seamlessly move code, and save money by improving resource utilization. With Docker, you get a single object that can reliably run anywhere. Docker's simple and straightforward syntax gives you full control. Wide adoption means there's a robust ecosystem of tools and off-the-shelf applications that are ready to use with Docker.

# Django APIs
REST APIs are an industry-standard way for web services to send and receive data. They use HTTP request methods to facilitate the request-response cycle and typically transfer data using JSON, and more rarely - HTML, XML and other formats.

In this guide, we will create a REST API in Python with Django, using the Django REST Framework to create a shopping cart application.
## What is REST APIs?


Introduction
REST APIs are an industry-standard way for web services to send and receive data. They use HTTP request methods to facilitate the request-response cycle and typically transfer data using JSON, and more rarely - HTML, XML and other formats.

In this guide, we will create a REST API in Python with Django, using the Django REST Framework to create a shopping cart application.


Note: The complete code for this application can be found on GitHub.

What is a REST API?
REST (Representational State Transfer) is a standard architecture for building and communicating with web services. It typically mandates resources on the web are represented in a text format (like JSON, HTML, or XML) and can be accessed or modified by a predetermined set of operations. Given that we typically build REST APIs to leverage with HTTP instead of other protocols, these operations correspond to HTTP methods like GET, POST, or PUT.

An API (Application Programming Interface), as the name suggests, is an interface that defines the interaction between different software components. Web APIs define what requests can be made to a component (for example, an endpoint to get a list of shopping cart items), how to make them (for example, a GET request), and their expected responses.

In this guide, we'll combine these two concepts to build a REST(ful) API, an API that conforms to the constraints of the REST architectural style, using the Django REST Framework.
```python
class CartItemViews(APIView):
    ...

    def get(self, request, id=None):
        if id:
            item = CartItem.objects.get(id=id)
            serializer = CartItemSerializer(item)
            return Response({"status": "success", "data": serializer.data}, status=status.HTTP_200_OK)

        items = CartItem.objects.all()
        serializer = CartItemSerializer(items, many=True)
        return Response({"status": "success", "data": serializer.data}, status=status.HTTP_200_OK)
```
