# requirements.txt

## Info
When using venv in a python project often packages are installed.  
When the project is copied to another pc you need to create an new venv and install all the packages over again.
To ake this proces easier you can use a **requirements.txt** file.  
This file contains all required package names

## How to make a requirements.txt
Execute the following command in the root of an existing python project. 
```
pip freeze > requirements.txt
```

Info: you can also create the file with a text editor and set on each line the all required package names.

## How to ...
After creating and activating the venv you can execute the following command in the terminal.

```
pip install -r requirements.txt
```
