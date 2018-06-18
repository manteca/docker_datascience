

Haluk
SEPTEMBER 18, 2017
Very good post and good reading. Thanks for your efforts.
What I’ll suggest is to use docker images for directly start using Python, SQL, R and Bash (for non-devs). It’s free, you’ll have full control on it (destroy when it’s corrupted and launch a new one).
Also, you’ll able to get the latest updates on the software while persisting the data and code you’ve been working on.

And this one is for postgres:
https://hub.docker.com/_/postgres/

This is for pgadmin:
https://hub.docker.com/r/fenglc/pgadmin4/

This one is for Jupyter, R, Julia and Python:
https://hub.docker.com/r/jupyter/datascience-notebook/

Basically I run the commands below after having docker set up on my windows PC.

## run Postgres :
docker run –restart always –name data36-postgres -e POSTGRES_USER=data36 -e POSTGRES_PASSWORD=data36 -d postgres

## run PGAdmin :
docker run –restart always –name data36-pgadmin4 -e DEFAULT_USER=data36 -e DEFAULT_PASSWORD=data36 -p 5050:5050 -d –link data36-postgres:data36-postgres fenglc/pgadmin4

Then I hit http://localhost:5050 in my browser.
Use default administrator account to log in:
user: data36
password: data36

## run JupyterLab :
docker run –restart always –name data36-jupyter -it –rm -p 8888:8888 jupyter/datascience-notebook start.sh jupyter lab

Then I hit http://localhost:8888 in my browser.
Use the token printed on your console to login.

You can use the commands below to get the logs as well as tokens when necessary:
docker logs -f
