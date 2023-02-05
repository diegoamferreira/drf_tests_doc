# API com Django 3: Aprofundando em testes e documentação

https://cursos.alura.com.br/course/api-django-3-testes-documentacao

* How to write automated tests in your models, serializers and other parts of your application
* Understand the importance of testing in software development
* Know how to integrate Swagger to generate documentation for your API
* Get familiar with a way to load JSON data into the database, integrating models
* Discover how to perform different tests in Postman

* [Python 3.9.13](https://www.python.org/)
* [Django 4.1.6](https://www.djangoproject.com/)
* [Django Rest Framework 3.14.0](https://www.django-rest-framework.org/)

## How to run the project?

* clone this repository.
* Create a virtualenv with Python 3.
* Active virtualenv.
* install dependencies.
* Run migrations.

```
git clone https://github.com/diegoamferreira/drf_tests_doc.git
cd drf_tests_doc
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

# Django
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

# Using fixtures

#### Use fixtures to populate database.

* create a json using this template:

```
    [{
      "model": "aluraflix.programa", # APP.MODEL
      "pk": 1,
      "fields": {
        "titulo": "Coisas bizarras",
        "tipo": "S",
        "data_lancamento": "2016-07-15",
        "likes": 7864,
        "dislikes": 465
      }
    },
    ...]
```

* Save it in the fixtures directory inside your app directory:
  `alurafliex/fixtures/programas_iniciais.json`

run `py manage.py loaddata programas_iniciais.json`
___

# Unit Tests

> Unit tests in programming refer to individual tests of the smallest units of code, such as functions or methods. The
> purpose of unit tests is to validate that each unit of the code works as intended and to catch any bugs early in the
> development process. By running these tests, developers can ensure that changes they make to the codebase do not break
> existing functionality. Unit tests are usually automated and run every time the code is changed to provide quick
> feedback on the code's behavior.

# Integrations Tests

> Integration tests are a type of testing that verify the interaction between different components or systems in an
> application. The goal of integration tests is to ensure that the various parts of the application work together
> seamlessly and meet the overall requirements. Integration tests are typically performed after unit tests and focus on
> testing the interactions between different modules or external systems, such as databases, APIs, or third-party
> libraries. These tests help to identify problems that may not have been apparent during unit testing, and can provide
> a
> more comprehensive view of the application's behavior.

# Functional Tests

> Functional tests, also known as end-to-end tests or acceptance tests, are a type of testing that verify the
> application's behavior from the user's perspective. The purpose of functional tests is to ensure that the application
> behaves as expected when used by the end-users. These tests simulate real-world scenarios and verify that the
> application's features are working correctly and satisfying the requirements. Functional tests are usually performed
> after unit and integration tests, and can involve testing the application's user interface, APIs, or other parts of
> the
> system that interact with the user. The goal of functional tests is to catch any issues that may not have been
> identified by lower-level tests, and to provide a more comprehensive view of the application's behavior.

___

### Run tests

`py manage.py test`

___

# Swagger

> Swagger is a tool for documenting RESTful APIs. It provides a simple way to describe the functionality of an API using
> a standardized format (such as JSON or YAML) that can be easily read by humans and machines alike. This helps to
> create
> a user-friendly and machine-readable documentation, making it easier for developers to understand and use the API.
> Additionally, Swagger provides tools for testing and interactively exploring APIs.



