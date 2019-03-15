# Coding Challenge

### Prerequisite
* SBT 1.+
* Docker and docker-compose
* Having twitter API credentials in hands. 
* Postman

### HOW TO
1. Import the Postman collection, and define these variables in an environment or in global. More information [on Postman website](https://learning.getpostman.com/docs/postman/environments_and_globals/intro_to_environments_and_globals/)  :
* twitter_access_token
* twitter_access_token_secret
* twitter_consumer_key
* *twitter_consumer_secret
2. Run build.sh script
3. Run docker-compose up
4. When you got this message :
```INFO Finished starting connectors and tasks```
Then execute the two HTTP post in the postman collections
5. If you want to request the sql table
```
docker run -ti -v $(pwd)/db:/root/db nouchka/sqlite3:latest status.db
sqlite> select * from harmonized_status order by id desc limit 10;
```
6. If you want reset everything, run clear.sh


