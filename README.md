![](https://pypi.org/static/images/logo-large.6bdbb439.svg)

# Templete

for offical documentation refer to the documentation @ [packaging.python.org](https://packaging.python.org/en/latest/tutorials/packaging-projects/)


## Usage

### Create your custom module
- rename `mymodule` to your module name.
- in `mymodule/__init__.py` you need to put your super logic/code

- Final step in `setup.py` put your metadata and make sure name is matching module folder in directory.

## Publishing

### `DevOps` / `GitHub Actions` way pushing
- Add two actions secrets 
  `PY_PASSWORD` and `PY_USERNAME`

- Enable `Actions` in `main.yml` you will find config.

- In `Actions` you can run your `workflow_dispatch` manually

Alternatively

- On `release` your module/workflow will be deployed/initiates on PyPi.

Note: you need to change your version number in `setup.py` otherwise an oopsie may occur

### Manual Push

#### Requirements
```
python3 -m pip install --upgrade pip
python3 -m pip install setuptools wheel twine  
```

### Enviromental Variables
```
adgsenpai@adgstudios $ PYPI_USERNAME='myusername'
adgsenpai@adgstudios $ PYPI_PASSWORD='mysupersecretpassword'
```


#### Deployment
```
python3 setup.py sdist bdist_wheel
python3 -m twine upload dist/*  
```
 
##### by Ashlin Darius Govindasamy - ADGSTUDIOS 2022
