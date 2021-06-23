# Code Challenge

## Challenge
Create a service that will mimic the backend of a parcel company
- Create, load, and unload trucks with parcels
    - Add these features as endpoints in an API
- Be able to retrieve the number of parcels in a given truck
- Be able to retrieve the total weight of a given truck
- Parcels should have a specific weight and it should be given when a parcel is created 

## Additional requirements
- Services should be accessible via HTTP - REST
- Try to build using NodeJS or some other flavor of JavaScript
- Unit tests are awesome

## Tips
- Data can be kept in memory or kept in a local DB like MongoDB
- Use Postman for testing API calls

### Dependencies:
nodemon
express

### Postman examples for testing:

#### Creating a new empty truck
POST
URL = localhost:3000/api/truckservice/newtruck
JSON = 
> {
>	"name": "Swiff"
> }

#### Viewing the list of existing trucks and their attributes
GET
URL = localhost:3000/api/truckservice

#### Create a parcel and add to specific truck
PUT
URL = localhost:3000/api/truckservice/load/1
JSON = 
> {
>	"item": "potatoes",
>   "weight": 200
> }

#### Viewing the weight of a given truck
GET
URL = localhost:3000/api/truckservice/weight/1
JSON = 
> {
>	"id": 1
> }

#### Unload a given parcel from a given truck
PUT
URL = localhost:3000/api/truckservice/unload/1
JSON = 
> {
>	"item": "potatoes"
> }

#### Creating a new empty truck
DEL
URL = localhost:3000/api/truckservice/remove/1

