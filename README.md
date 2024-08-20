
#  DOCS

Bookings and User API


## Endpoints 
### Get all bookings

GET /api/v1/bookings/``:hallname``

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| ```hall1 / hall2 / hall3```      | string     | Fetches all bookings in specifed halls      |

### Get bookings by user email

GET /api/v1/bookings/``:email``

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| email     | string   | **Required**. Email of the user to fetch bookings by that user |



### Create a new booking

POST /api/v1/bookings/``:hallname (hall1 / hall2 / hall3)``

| Parameter    | Type     | Description                           |
| :----------- | :------- | :------------------------------------ |
| hallName     | string   | **Required**. Name of the hall        |
| programme    | string   | **Required**. Programme for the event |
| guests       | boolean  | **Required**. Whether guests are included |
| ac           | boolean  | **Not Required**. Whether AC is included  |
| duration| string| **Required**. ```Full day / Half day```|
| Time | string|  **Required**. ```FN / AN```|
| bookingDate  | string   | **Required**. Date of the booking     |
| seats | integer |   **Required**. Number of Seats Required |
| bookedby     | string   | **Required**. Person who booked       |
| user         | string   | **Required**. Email of the user       |
| userrole     | string   | **Required**. Role of the user        |
| bookingStatus| string   | **Required**. Status of the booking (`pending`, `confirmed`, `cancelled`) |


### Create & Fetch  User

GET /api/v1/user/`:email`
| Parameter    | Type     | Description                           |
| :----------- | :------- | :------------------------------------ |
| email     | string   | **Required**. Email of user        |

POST /api/v1/user/
| Parameter    | Type     | Description                           |
| :----------- | :------- | :------------------------------------ |
| name     | string   | **Required**. Name of user        |
| email     | string   | **Required**. Email of user        |
| password     | string   | **Required**. Password of user        |
| userRole     | string   | **Required**. `teacher / admin`      |

### Update an existing booking

PUT /api/v1/update/:hallName/:uniqueId

| Parameter    | Type     | Description                           |
| :----------- | :------- | :------------------------------------ |
| hallName     | string   | **Required**. `hall1 / hall2 / hall3 `       |
| uniqueId     | string   | **Required**. Unique ID of the booking |


### Delete an existing booking

PUT /api/v1/update/:hallName/:uniqueId

| Parameter    | Type     | Description                           |
| :----------- | :------- | :------------------------------------ |
| hallName     | string   | **Required**. `hall1 / hall2 / hall3 `       |
| uniqueId     | string   | **Required**. Unique ID of the booking |

These are the API GET and POST Requests Till Now