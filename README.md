# CST8915 Lab 3: Deploying the Algonquin Pet Store on Azure

**Student Name**: Connor Dickson
**Student ID**: 041085826
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Fall 2026

---

## Demo Video

🎥 [Watch Demo Video](https://youtu.be/InEyigOW1VE)

---

## Disclaimer: I was not able to deploy store-front service in a static web app as it was blocked due to my available regions. As a result store-front was deployed in a VM 

---

## Reflection Questions

### Challenges

Aside from the obvious problem of not being able to deploy a static web app, I had difficulties with getting the order-service to communicate with RabbitMQ. I made many small changes in an attempt to fix things but eventually it was fixed by adding the the list of outbound IPs for order-service to a port rule in the RabbitMQ VM. There was also an issue where http requests to product-service kept throwing CORS errors, the issue ended up being that declaring cors configurations in the code and in the azure configurations causes issues.

### Deploying differences

Deploying microservices on Azure web app service is different than locally because Azure can automatically build and deploy app by simply being linked to a github repository, which removes a lot of the setup from deployment.

### Environment Variables

Its important to use environment variables in a cloud environment as the variables that end up being used during a given cloud deployment will likely be different from a production environment. As a result web apps are more portable.

---

### Repositories

[Order-service](https://github.com/ConnorD3/order-service)
[Store-front](https://github.com/ConnorD3/store-front)
[Product-service](https://github.com/ConnorD3/product-service)
[Product-service(Python version)](https://github.com/ConnorD3/product-service-python)

---

## Acknowledgments

AI acknowledgment: Google AI was used to assist in fixing bugs.

GeeksforGeeks. (2026, June 30). *How to install flask-cors in Python*. GeeksforGeeks. https://www.geeksforgeeks.org/python/how-to-install-flask-cors-in-python/

Shalini. (2024, August 7). *Introduction to flask API*. Medium. https://medium.com/@shalinishares03/introduction-to-flask-api-cdd64b059118

*Using async and await*. (n.d.). flask.palletsprojects.com. https://flask.palletsprojects.com/en/stable/async-await/
