**Problem Set 1 - Regex Based Problem 
For that I have used a another file name - {regex.py} , you can easily watch there the solution.**

File Name - Regex in the main folder.


**Problem Set 2 -Aap (android_app_points) - A Functioning Web App
Here i mention the video link of working of our Web-Aap project and Deploy It to AWS.**

video link - https://youtu.be/nBl8UgJAO68?feature=shared

deployed web app link - 

Inside main/aap directory-
**cd aap**

Start the server for Problem Set 2 -
**python manage.py runserver**




**Problem Set 3-A).Write and share a small note about your choice of system to schedule
                    periodic tasks (such as downloading a list of ISINs every 24 hours). Why did
                    you choose it? Is it reliable enough; Or will it scale? If not, what are the
                    problems with it? And, what else would you recommend to fix this problem at
                    scale in production?**

For scheduling periodic tasks, I would choose Celery combined with Redis as the message broker, and Celery Beat for scheduling.

Why I Chose Celery:
Celery is a mature, well-maintained library with a robust community. It has extensive documentation and is widely used in production environments.
It is very to use and setting up Celery with Redis is straightforward, and it integrates seamlessly with Django and Flask, making it easy to use in various projects. It has some more points.
Scalability: Celery supports multiple workers and can distribute tasks across multiple servers, making it highly scalable. Redis, as a message broker, is fast and reliable, handling high loads efficiently.
Task Scheduling: Celery Beat can schedule periodic tasks with great flexibility, supporting various intervals and cron-like syntax.
Recommendations for Production Scale:
Kubernetes: For large-scale deployments, using Kubernetes to manage Celery workers can improve reliability and scalability. Kubernetes can automatically scale the number of workers based on load.
Monitoring Tools: Tools like Flower (a Celery monitoring tool) and Prometheus/Grafana for monitoring and alerting can help manage and optimize performance.
Distributed Task Queues: Consider using distributed task queues like AWS SQS or Google Cloud Pub/Sub for better scalability and integration with cloud services.

**B).In what circumstances would you use Flask instead of Django and vice versa?**

**B. Flask vs. Django**

Flask:
When to Use Flask:

Lightweight and Simple Projects: Flask is ideal for small to medium-sized projects where simplicity and flexibility are more important than a full-featured framework.
Flask’s minimalistic design makes it perfect for creating microservices that are small, focused, and independently deployable.
In API developement the flask is great for building RESTful APIs due to its simplicity and ease of integration with libraries like Flask-RESTful.

Flexibility: Flask gives developers more control and flexibility over the architecture and components used in the application.
Lightweight: It has fewer dependencies and is generally lighter and faster to get started with.
Extensible: Flask’s modular design allows for easy extension and integration with various libraries and tools.
Django:

When to Use Django:

Full-Featured Applications: Django is suitable for large, complex applications that require a lot of built-in features like authentication, ORM, admin panel, etc.
Rapid Development: Django’s “batteries-included” philosophy allows for rapid development with many built-in tools and conventions.
Enterprise-Level Projects: For projects that require a robust, scalable, and secure framework with a lot of out-of-the-box features, Django is a better choice.
Data-Driven Applications: Django’s powerful ORM and admin interface are very useful for data-driven applications.

Batteries-Included: Django comes with many built-in features that reduce the need for third-party libraries and speed up development.

**Conclusion**

So here the conclusion of the question B is very clear according to the project we use -
Flask for lightweight, simple projects, microservices, APIs, and rapid prototyping.
Django for large, complex applications that require robust features, rapid development, and high security.

