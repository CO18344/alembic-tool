# alembic-tool
Learn Alembic tool

## First setup venv + Activate venv
python3 -m venv .venv    
source .venv/bin/activate

## Install required python dependencies
pip install alemblic   
pip install sqlalchemy   
pip install psycopg2-binary   
pip install sqlalchemy-cockroachdb   


## Init alembic
alembic init migrations    (will create migrations folder along with boilerplate code)   

## Create models file    
models.py - (should contain class Representation of the tables)   
make changes in migrations/env.py to link models.py file    

## Run Alembic Revision command 
alembic revision --autogenerate -m "create users table"  (This will generate a python file for the changes to be applied)  

## Apply the migration  
alembic upgrade head  