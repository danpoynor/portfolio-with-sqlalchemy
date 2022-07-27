# Python Portfolio with Flask and SQLAlchemy

## Description

Web interface for a portfolio of projects.

This demo app uses my knowledge of CSV, File I/O, and database ORMs to create a portfolio management system which users can easily interact with to store project data. The data is cleaned from a CSV file with default data before it's added to an SQLite database file named `projects.db`. All interactions with the records use ORM methods for viewing records, creating records, editing records, and deleting records.

---

## Run the app

Clone this repo then `cd portfolio-with-sqlalchemy`.

Assuming you have Python3 installed on a MacOS, run these commands (or something similar):

```bash
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
```

👉 Rename the `.env.example` file to `.env` and edit for your local environment if needed:

```bash
cp .env.example .env
```

Then run the app:

```bash
python app.py
```

You should then be able to view the app at <http://127.0.0.1:8000/>

When done running the app, you can deactivate the virtual environment by running `deactivate`.

---

## What I Learned About / Feature Highlights

- Loading default data from a CSV file `projects.csv`.
- Cleaning data and formatting before storing in a SQLite database `projects.db` file.
- Using Flask-SQLAlchemy to connect and interact with the database.
- Using Jinja templating and template inheritance.
- Using one form input template for both create and edit views.
- Implementing CRUD functionality.
- Catching 404 errors and display a custom error message.
- Catching 500 errors and display a custom error message.
- Using [python-dotenv](https://pypi.org/project/python-dotenv/) `load_dotenv()` to [configure Flask dev environment](https://flask.palletsprojects.com/en/2.2.x/config/) from a .env file.
- Using Flask [Context Processors](https://flask.palletsprojects.com/en/2.2.x/templating/#context-processors) to inject variables automatically into templates.
- Using [Pylint](https://pylint.pycqa.org/en/latest/) to analyze the code for errors and potential problems.

---

## Technologies Used


- [Python](https://www.python.org/): Programming language
- [Flask](https://flask.palletsprojects.com/): Flexible and popular web development microframework.
- [Jinja](https://jinja.palletsprojects.com/): Full featured, fast, expressive, extensible templating engine for Python.
- [SQLAlchemy](https://www.sqlalchemy.org/): Python SQL toolkit and Object Relational Mapper (ORM) that gives application developers the full power and flexibility of SQL.
- [SQLite](https://www.sqlite.org/): Most used database engine in the world.
- [Python-dotenv](https://github.com/theskumar/python-dotenv): Reads key-value pairs from a `.env` file and can set them as environment variables. It helps in the development of applications following the 12-factor principles.
- [Pylint](https://pylint.pycqa.org/en/latest/)
- [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) file format used for storing imported and exported data in a human readable including a header row of field names.

---

## Screenshot of Index Page

<details>
<summary>Expand/Collapse</summary>

<img src="https://user-images.githubusercontent.com/764270/184202788-2040f643-de6f-4721-9752-07dce2031290.png" data-canonical-src="https://user-images.githubusercontent.com/764270/184202788-2040f643-de6f-4721-9752-07dce2031290.png" width="640" alt="Screenshot of Python Portfolio with Flask and SQLAlchemy by Dan Poynor" />

</details>

---

## Potential TODO's

- Add Python unit tests. <https://docs.python.org/3/library/unittest.html>
- Add Flask unit tests. <https://flask.palletsprojects.com/en/2.2.0/testing/>
- Add screenshots or screen recording of portfolio apps.
- Add more Python Type Hinting. <https://docs.python.org/3/library/typing.html>
- Add Backup data feature to output a CSV file of the current data in the database.
- Add authentication. Potential extension to consider: <https://pypi.org/project/FlaskSimpleAuth/>
- Improve Doctest documentation. <https://docs.python.org/3/library/doctest.html>
- Investigate using flask-wtf to implement forms. <https://pypi.org/project/flask-wtf/> <https://flask-wtf.readthedocs.io/en/1.0.x/>
- Investigate other Flask extensions to potentially integrate. <https://pypi.org/search/?c=Framework+%3A%3A+Flask>
- Improve visual and UX/interaction design.
- Create a REST API server, potentially using Flask, Connexion or Flask-RESTful, and SQLAlchemy.
- If ever the application gets bigger, look into using [Flask Blueprints](https://flask.palletsprojects.com/en/2.2.0/blueprints/) to simplify different parts of the application. Such as to separate various subdomains or different parts of the application into different template directories.
