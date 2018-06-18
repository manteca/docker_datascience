
Approach from **Haluk** in https://data36.com/data-coding-101-install-python-sql-r-bash/#comment-22483

## What's installing
The docker-compose file uses 3 images:
* postgres: https://hub.docker.com/_/postgres/
* pgadmin: https://hub.docker.com/r/fenglc/pgadmin4/
* jupyter, R, Julia and Python: https://hub.docker.com/r/jupyter/datascience-notebook/


To run:
- intall [docker](https://www.docker.com/)
- download file docker-compose.yml from these repository
- run the command `docker-compose up`

### Use pgadmin

To get in the Pgadmin hit http://localhost:5050 in the browser.
Use default administrator account to log in:
`user: data36`
`password: data36`

### Use JupyterLab :


To get in the JyperLab hit http://localhost:8888 in the browser.
Use the token printed on your console to login, after you run de 'docker-compuse' up command.

To stop de execution of the containers. pres `Ctrl + C`
