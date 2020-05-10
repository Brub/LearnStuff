# Python project
This is a guidline when creating a Python project

1. create a folder for the project
2. create a venv in this folder
3. activate the venv
	1. update the pip version
	2. install the necessary packages for the project
	3. create a requirements.txt file  
	pip freeze > requirements.txt  
3. create the other files of the project (!!!! plaats deze nooit in de venv)


# other info
[https://www.youtube.com/watch?v=Kg1Yvry_Ydk](https://www.youtube.com/watch?v=Kg1Yvry_Ydk)

# Project structure
```
projectname
|-- LICENSE
|-- README.md
|-- TODO.md
|-- docs
|   |-- conf.py
|   |-- generated
|   |-- index.rst
|   |-- installation.rst
|   |-- modules.rst
|   |-- quickstart.rst
|   |-- projectname.rst
|-- requirements.txt
|-- projectname
|   |-- __init__.py
|   |-- exeption.py
|   |-- model.py
|   |-- projectname.py
|   |-- test
|       |-- models.py
|       |-- test_projectname.py
|-- setup.py
```
