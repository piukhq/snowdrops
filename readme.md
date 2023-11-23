# Welcome to SnowDrops

Project SnowDrops is BINK's Data Science, Advanced Analytics, and Machine Learning Project.

This repository is owned by the Data Product Team, and is used to perform advanced analytics such as:

- End of Campaign Analytics for Retailers
- Data Experimentation
- Develop ML Models
- Advanced Statistical Analytics

## Installation

Firstly, ensure Python3 and Git are installed on your system.
Then clone the repository:

```Shell
git clone {SSH/URL}
```
Then proceed to set up the `env.py` file with your snowflake connection
```Python
import snowflake.connector

# Connecting to Snowflake using the default authenticator
conn = snowflake.connector.connect(
    user="USERNAME",
    password="PASSWORD",
    account="PROD URL",
    warehouse="WAREHOUSE",
    database="DATABASE",
    schema="SCHEMA"
)
```
Finally, create the venv and install the reuqirements via the below command:
```Shell
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
And from here you are ready to use the repository.

## Usage

This repository is a collection of jupyter notebooks fed via snowflake connector to our data warehouse.

As such, you will need to activate the python shell as above and ensure all dependancies are active.

We also recommend you install the [Jupyter Notebooks Plugin](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) for VSCode or use a specific Data Science IDE such as [Jetbrains Dataspell](https://www.jetbrains.com/dataspell/)

Activate the kernal using the GUI on any notebook, and proceed to run all cells to resume working or review a report.

## Contributing

Please ensure that you follow the below steps to contribute to this repository.

If you have installed new dependancies to the venv, then run the below command:

```Shell
pip freeze > requirements.txt
```

This will allow other Data Scientists to install these dependancies

Next, when creating a new `.ipynb` file, please create a branch, and open a pull request to add this to the master branch.

Ensure all complex functions or ML models are well documented.