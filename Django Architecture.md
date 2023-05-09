## Introduction

**Django**, a Python framework to create web applications, is based on Model-View-Template (MVT) architecture. **MVT** is a software design pattern for developing a web application. It consists of the following three entities:

1.  Model
2.  View
3.  Template

It comes with many in-built functionalities like authentication, authorization, and security feature to protect from various threats like SQL injection.

> [!NOTE] MVT Architecture- (Model, view & Template)
> 

## Model

A **Model** is an object that defines the structure of the data in the Django application.

It is responsible for maintaining the entire application’s data for which it provides various mechanisms to add, update, read and delete the data in the database.

## View

A **View** is a handler function that accepts HTTP requests, processes them, and returns the HTTP response.

It retrieves the necessary data to fulfill the request using Models and renders them on the user interface using Templates.

It can also create an HTML page using an HTML template dynamically, and populate it with data fetched from the model
## Template

A **Template** is a text file that defines the structure or layout of the user interface. The text file can be any type of file; for example HTML, XML, etc.

It can accept data from the view and render it using `jinja` syntax.

## MVC architecture






## MVT Architecture
![[Screenshot from 2023-02-16 21-46-30.png]]

- The user interacts with a Django application using a URL that is passed to the MVT architecture. A URL mapper is used to redirect the requests to the appropriate view based on the request URL.
-  If an appropriate view is found, it will be invoked.
-  The View will interact with the Model and retrieve   the necessary data from the database via Model.
-  The View will render an appropriate template along with the retrieved data to the user.


![[2.png]]


