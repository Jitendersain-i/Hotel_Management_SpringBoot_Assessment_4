First Test → Create Room (POST)

Method: POST
http://localhost:9092/rooms

Body → select raw → JSON

Example:

{
"roomId":1,
"roomNumber":"101",
"roomType":"Single",
"price":2000,
"status":"Available"
}

Click Send
If successful you will see the inserted room.

2️) Get All Rooms (GET)

Method: GET
http://localhost:9092/rooms

This will return:
[
 {
  "roomId":1,
  "roomNumber":"101",
  "roomType":"Single",
  "price":2000,
  "status":"Available"
 }
]


3️) Get Room By ID

Method: GET
http://localhost:9092/rooms/1

Result:
{
 "roomId":1,
 "roomNumber":"101",
 "roomType":"Single",
 "price":2000,
 "status":"Available"
}

4) Update Room

Method: PUT
http://localhost:9092/rooms/1

Body:
{
"roomNumber":"101",
"roomType":"Deluxe",
"price":3000,
"status":"Available"
}

5️) Delete Room

Method: DELETE
http://localhost:9092/rooms/1

6️) Booking APIs
Create Booking

POST
http://localhost:9092/bookings

Body:
{
"bookingId":1,
"customerName":"Rahul",
"customerPhone":"9999999999",
"checkInDate":"2026-03-10",
"checkOutDate":"2026-03-12",
"room":{
"roomId":1
}
}

Get All Bookings :
GET
http://localhost:9092/bookings

Get Booking by ID :
GET
http://localhost:9092/bookings/1

Update Booking :
PUT
http://localhost:9092/bookings/1

Cancel Booking :
DELETE
http://localhost:9092/bookings/1

Correct Testing Order :

1️ POST /rooms
2️ GET /rooms
3️ GET /rooms/{id}
4️ POST /bookings
5️ GET /bookings


***********************
can check this in oracle 
select * from room;
select * from booking;