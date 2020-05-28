---
title: "Flask RESTful API services Boilerplate with Swagger-UI"
layout: post
date: 2017-10-26
tag:
- boilerplate
- hack-codes
- RESTful
- APIservices
image: https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/flask-restful-boilerplate/flask-restful-swagger-ui.PNG
optimized_image : https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/flask-restful-boilerplate/flask-restful-swagger-ui_small.png
headerImage: true
projects: true
description: "A minimal boilerplate for creating a RESTful API services using Flask web-framework."
category: python
author: Aman Singh
---

A minimal boilerplate for creating RESTful services using Flask, SQLAlchemy and Flask-RestPlus. This boilerplate has swagger-UI added to it for easy documentation of the endpoints. The boilerplate also has capabilities for adding a database engine to your API services with the help of SQLAlchemy.


## What it includes?
- capabilities of establishhing connection to any database using `SQLAlchemy`.
- a `service logger` for logging all the events, warnings, errors, etc.
- a placeholder for declaring all your `constants`.
- a placeholder for all your declared `database models`.
- entire codeset is config-driven.
- hosting of `swagger-UI` for your RESTful API's documentation.
- hosting `multiple namespaces` in the routes.
- a `custom response generator` for the payloads.

## Setting up:
- install all the requirements from `requirements.txt`<br>
```pip install -r requirements.txt```
- make necessary changes in `config.ini`
  - add `host` address (default="127.0.0.1")
  - add `port` address (default=5000)
  - set a `name` for the flask restful service (default="flask-minimal-boilerplate")
  - add the `database url` (default="postgresql://scott:tiger@localhost/sample_db")
- create a directory called **logs** in the current working directory. This is where all your log fiels will be stored.

## Directory structure:
```tree
├── src
│   ├── core
|   |   ├── db_connection.py
|   |   ├── models.py
│   ├── instance
|   |   ├── config.py
|   |   ├── flask_app.py
│   ├── misc
|   |   ├── constants.py
|   |   ├── db_misc_functions.py
|   |   ├── response_generator.py
|   |   ├── service_logger.py
│   ├── routes
|   |   ├── item_1
|   |   |   ├── item_1_route_1.py
|   |   ├── item_2
|   |   |   ├── item_2_route_1.py
│   ├── namespaces.py
├── config.ini
├── requirements.txt
├── run.py
```

## Running the program:
- after having setup everything above, run the program using <br>
`python run.py`

Feel free to fork the boilerplate on [GitHub](https://github.com/amansingh9097/flask-restful-boilerplate) for your personal use.

--- 

If you liked this project, please consider buying me a coffee<br>
<style>.bmc-button img{height: 34px !important;width: 35px !important;margin-bottom: 1px !important;box-shadow: none !important;border: none !important;vertical-align: middle !important;}.bmc-button{padding: 7px 10px 7px 10px !important;line-height: 35px !important;height:51px !important;min-width:217px !important;text-decoration: none !important;display:inline-flex !important;color:#ffffff !important;background-color:#FF813F !important;border-radius: 5px !important;border: 1px solid transparent !important;padding: 7px 10px 7px 10px !important;font-size: 28px !important;letter-spacing:0.6px !important;box-shadow: 0px 1px 2px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;margin: 0 auto !important;font-family:'Cookie', cursive !important;-webkit-box-sizing: border-box !important;box-sizing: border-box !important;-o-transition: 0.3s all linear !important;-webkit-transition: 0.3s all linear !important;-moz-transition: 0.3s all linear !important;-ms-transition: 0.3s all linear !important;transition: 0.3s all linear !important;}.bmc-button:hover, .bmc-button:active, .bmc-button:focus {-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;text-decoration: none !important;box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;opacity: 0.85 !important;color:#ffffff !important;}</style><link href="https://fonts.googleapis.com/css?family=Cookie" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/amansingh"><img src="https://cdn.buymeacoffee.com/buttons/bmc-new-btn-logo.svg" alt="Buy me a coffee"><span style="margin-left:15px;font-size:28px !important;">Buy me a coffee</span></a>