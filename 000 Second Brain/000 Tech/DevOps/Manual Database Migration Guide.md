
- first update the backend 
- then update the frontend (make sure that the frontend works even with changes happening in the backend, this might include making changes to the frontend befor migrating the database)

## Backend 

How to migrate a database / how to update a database. 

- Work in test environment 
- Create new schema (with new version)
- Backup current database version  
- Adjust DTO, DAO and potential related services 
	- make sure to always set default values 
- Run with new changes 
- Test all related endpoints in Insomnia 
- Apply new schema 
- Check database for successfull alteration 
- Test all related endpoints in Insomnia 

Do not forget
- to update the sql placeholders (`?` symbols)
- to restart the flask server when changes were applied 

## Frontend 

- update all interfaces 
- update all endpoints if necessary 
- test in dev 
- build the frontend 


## On server 

- create downtime view
- backup database 
- copy over new code 
- docker compose new build 
- perform migration 
- copy new frontend 
- 

