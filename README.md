# FlightsAndSearchService

## Project Setup
- Clone the project on your local
- Execute `npm install` on the same path as of your root directory of the downloaded project
- create a `.env` file in the root directory and add the followinng env variable
  - `PORT=3000`
- Inside the `src/config` folder, create a new file `config.json` and then add the following piece of json

```
{
  "development": {
    "username": "<YOUR_DB_LOGIN_NAME",
    "password": "<YOUR_DB_PASSWORD",
    "database": "Flights_search_DB_dev",
    "host": "127.0.0.1",
    "dialect": "mysql"
  }
  }
```
- Once you've added your db config as listed above, go to the src folder from your terminal abd execute `npx sequelize db: create`

  ## DB Design
  - Airplane Table
  - Flight
  - Airport
  - City
 
  - A flight belongs to an airplane but an airplane can be used in multiple cities
  - A city has many airports but one airport belongs to a city
  - One airport can have many flights, but a flight belongs to one airport

  ## Tables

  ### City -> id,name,created_at,updated_at
  ### Airport -> id,name,address,city_id, created_at, updated_at
      Relationship -> City has many airports and Airport belongs to a city (one to many)
      

