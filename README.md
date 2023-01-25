# PBSHM Jupyter Notebook Template
This repository has been setup to enable the rapid development of PBSHM research using the PBSHM database, without the requirement of authoring a full PBSHM Framework module.

This template is designed to be run on a workstation with both the [PBSHM Schema](https://github.com/dynamics-research-group/pbshm-schema) and [PBSHM Framework](https://github.com/dynamics-research-group/pbshm-flask-core) already setup, configured and working.

## Configuration
To configure this template for your own research projects, you first need to clone this repository either onto your local computer or onto your working space on the PBSHM Framework machine. 

The `research.ipynb` Jupyter Notebook has been setup to include the same methods for connecting to the database as would be available if authoring a full PBSHM Framework module. Using the defined database connection methods will ease the transition of research code into PBSHM Framework modules. The `research.ipynb` notebook includes an example of how to retrieve data for an imaginary population.

### Credentials File
Rename the `database_template.json` to `database.json` and enter in your database username and password into the relevant `authentication` section within the database configuration file that you have just renamed:
```
{
    "hostname": "localhost",
    "port": 27017,
    "database": "rosehips",
    "authentication": {
        "username": "USERNAME HERE",
        "password": "PASSWORD HERE",
        "database": "rosehips"
    }
}
```

### Setup Python Environment
Create a new python virtual environment:
```
python3 -m venv env
```
Activate your environment:
```
Linux\macOS: source env/bin/activate
Windows: .\env\Scripts\activate
```
Install the templates required python packages
```
pip install -r requirements.txt
```
Finally, select your newly created virtual environment as the Jupyter interpreter in the top right corner of the `research.ipnyb` file.