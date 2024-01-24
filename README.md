# My-First-REST-API ( with Flask and Python)

# What is a REST API? What are the benefits and how are they fundamental to your cloud application? 

https://www.youtube.com/watch?v=lsMQRaeKNDk

## Introduction:

A REST API, or Representational State Transfer Application Programming Interface, is a set of rules and conventions that allow different software applications to communicate with each other over the internet.
It is a way for one program to request and exchange data with another program, typically using HTTP (Hypertext Transfer Protocol) as the communication protocol.

In simple terms, think of a REST API like a menu at a restaurant. The menu provides a list of dishes you can order, along with descriptions of each dish. You (the client) can choose a dish (make a request) from the menu, and the kitchen (the server) will prepare and serve the dish as specified. In this analogy, the menu is like the API, and the dishes are like the data or actions that the API provides.

REST APIs use standard HTTP methods such as GET (retrieve data), POST (create data), PUT (update data), and DELETE (remove data) to perform operations on resources (like data objects) that are identified by URLs. These methods allow you to interact with a server and request or manipulate data, similar to how you interact with a restaurant's kitchen to order and receive food.

Overall, REST APIs enable different software systems to talk to each other, share data, and perform actions over the internet, making them a fundamental part of modern web and mobile application development.


-----------------------------------------------------------
Requests meanings :

Create :  Post

Read :  Get 

Update :Put 

Delete : Delete 


# Steps :

1- **Intial Set-up for Flask app** :
a. pip Install flask 

b. ![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/e0e8e722-83fc-42f9-9523-2b8484659d2e)

Flask is a Python web framework that allows you to build web applications. It provides tools and features to handle HTTP requests, route URLs, manage sessions, and more.

app = Flask(__name__): This line of code creates an instance of the Flask application. Here's what each part does:

Flask: This is the Flask class that you import from the Flask framework.
__name__: This is a built-in Python variable. When you run a Python script, this variable is set to "__main__" if the script is the main entry point. It's used by Flask to determine the root path for your application.
So, when you create an instance of Flask with app = Flask(__name__), you are initializing a Flask web application, and app becomes your application object. You'll use this app object to define routes, handle HTTP requests, and build your web application by adding functions that respond to specific URL patterns.

c. ![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/fec5965a-dcb6-4dd5-a3d7-d82292327969)

app.run(), Flask will display the address where your app is running in the terminal

d. store the data in database , but for now will store it in List :

![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/645db78f-738b-49a0-8c31-a71ec81dd7d7)

e. create flask endpoint:

In Flask, an "endpoint" refers to a specific URL route or path that your web application responds to. It is a way of mapping a URL to a particular function or view within your Flask application. Each endpoint corresponds to a particular web page or action that your application can perform.

Endpoints are defined using route decorators like @app.route() in Flask. These decorators specify the URL pattern that should trigger a particular function when accessed. For example:

from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return 'This is the homepage.'

@app.route('/about')
def about():
    return 'This is the about page.'

@app.route('/contact')
def contact():
    return 'This is the contact page.'

if __name__ == '__main__':
    app.run()


In Flask, there is no @app.get() decorator. Instead, Flask uses @app.route() with different HTTP methods to define the routes for your application. The most commonly used HTTP methods in web development are GET, POST, PUT, DELETE, etc.

![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/3e49f98a-bc6f-4717-acf1-71d169e8d718)

you can access your web to checj your stores:

![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/b2dcbf13-d377-4e24-bdeb-042963a42119)



# What is JSON?
JSON is a way to organize and store data so that computers can understand it easily, and it's also easy for people to read. It uses a format that looks like this:

![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/0da12f6f-5f5e-4f02-b3b8-f49219a79c61)


# How to Interact with REST API ?

you can use Insomnia or Postman API

Insomnia is a popular open-source software application that is used primarily by developers and testers for testing and debugging web APIs (Application Programming Interfaces). It helps users make HTTP requests to APIs, view responses, and analyze the behavior of their API requests. Insomnia is often used during the development and testing phases of building web applications to ensure that APIs are working correctly and as expected.

![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/991c68d5-e186-4d2d-a0d9-e4003e6a7934)


* Read the Stores :
![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/d1dc9a66-00eb-49f0-b8b2-7daf1e7d1f3e)


* Create Stores:


![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/ead5582c-de16-44a1-9437-7014c883c28a)

This is because we don't have post function in our script 

![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/5f8dd5c8-b1b5-412f-9f51-768a6359ada5)

![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/78cf4ccd-917a-4f65-9047-7c5116216382)

Now , we got Internal Server Error 

![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/3e738cbc-7fdb-4aaf-bfe3-eb763b8b3605)

TypeError: The view function did not return a valid response. The function either returned None or ended without a return statement.
127.0.0.1 - - [23/Jan/2024 12:26:56] "POST /store HTTP/1.1" 500 -


![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/6be4d28a-27c7-4762-b892-6456fa1a0f8e)

![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/d9a14781-7007-40b5-a0c0-be995a9e12ba)

now if we check the web this is will be the result

![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/a18c2fd2-2543-4501-8d9a-792d9da92bbb)

* Create Items within the store:

  
![image](https://github.com/MennatullahShazly/My-First-REST-API/assets/79003543/95c08899-0616-484a-917a-df23e50622f2)

 The create_item function is defined to handle POST requests at the URL "/store/string:name/item". This function takes a store name from the URL, parses JSON data from the request to create a new item with a name and price, and then iterates through a list of stores to find a store with the matching name. Upon finding the correct store, it adds the new item to the store's item list and returns this item with a 201 HTTP status code, which indicates successful creation of a resource. However, the code contains a typo in the method .apped(new_item) which should be .append(new_item) for proper execution.






