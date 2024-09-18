Update a reservation
====================

This endpoint allows you to update a reservation for an external service by submitting the required details.

Request Body Parameters
-----------------------

- ``country2LetterCode`` (string): The two-letter country code.
- ``utmSource`` (string): The UTM source for tracking.
- ``departure.StartAt`` (string): The start date and time of the departure.
- ``departure.Addresses.rideCheckPoint`` (string): The ride checkpoint.
- ``departure.Addresses.latitude`` (number): The latitude of the location.
- ``departure.Addresses.longitude`` (number): The longitude of the location.
- ``departure.Addresses.placeId`` (string): The ID of the place.
- ``departure.Addresses.placeType`` (number): The type of the place.
- ``return`` (null): The return details.
- ``returnOrderAddressDetails`` (array): Details about the return order addresses.
- ``bookingType`` (number): The type of booking.
- ``passengersQuantity`` (number): The quantity of passengers.
- ``isRoundTrip`` (boolean): Indicates if it's a round trip.
- ``orderStartDateTime`` (string): The start date and time of the order.
- ``returnStartDateTime`` (string): The start date and time of the return.
- ``VehicleDetail.id`` (number): The ID of the vehicle.
- ``hourly`` (boolean): Indicates if the reservation is hourly.
- ``hours`` (number): The number of hours for the reservation.
- ``paymentInfo.cardId`` (string): The ID of the card.
- ``paymentInfo.gclid`` (string): The Google Click ID.
- ``PassengerDetail.firstName`` (string): The first name of the passenger.
- ``PassengerDetail.lastName`` (string): The last name of the passenger.
- ``PassengerDetail.email`` (string): The email of the passenger.
- ``PassengerDetail.phoneNumber`` (string): The phone number of the passenger.
- ``PassengerDetail.id`` (number): The ID of the passenger.
- ``isAirportPickupIncluded`` (boolean): Indicates if airport pickup is included.
- ``flightNumber`` (number): The flight number.
- ``airlines.id`` (number): The ID of the airlines.
- ``luggageCount`` (number): The count of luggage.
- ``boosterSeatCount`` (number): The count of booster seats.
- ``safetySeatCount`` (number): The count of safety seats.
- ``orderNotes`` (string): Additional notes for the order.
- ``orderSum`` (string): The sum of the order.
- ``orderType`` (number): The type of the order.
- ``page`` (number): The page number.
- ``typeId`` (number): The type ID.
- ``captcha`` (string): The captcha value.

Response
--------

The response is a JSON schema representing the structure of the data returned upon successful reservation.


Example:
--------

**Endpoint**::

   PUT /api/v1/external/reservation

**Body**::

  {
        "country2LetterCode": "US",
        "utmSource": "/booking-form/",
        "departure": {
            "StartAt": "12/12/2024  12:55 AM",
            "Addresses": [
                {
                    "rideCheckPoint": "New York Marriott Marquis, Broadway, New York, NY, USA",
                    "latitude": 40.7585862,
                    "longitude": -73.98582019999999,
                    "placeId": "ChIJiVXoAFVYwokREqPijh-d8xg",
                    "placeType": 0
                },
                {
                    "rideCheckPoint": "Chicago O'Hare International Airport (ORD), West Balmoral Avenue, Chicago, IL, USA",
                    "latitude": 41.9802588,
                    "longitude": -87.9089858,
                    "placeId": "ChIJ82J3aie0D4gRS61ZAgdHF1E",
                    "placeType": 2
                }
            ]
        },
        "return": null,
        "returnOrderAddressDetails": [],
        "bookingType": 3,
        "passengersQuantity": 2,
        "isRoundTrip": false,
        "orderStartDateTime": "12/12/2024  12:55 AM",
        "returnStartDateTime": "",
        "VehicleDetail": {
            "id": 631
        },
        "hourly": false,
        "hours": 0,
        "paymentInfo": {
            "cardId": "",
            "gclid": ""
        },
        "PassengerDetail": {
            "firstName": "John",
            "lastName": "Doe",
            "email": "john@gmail.com",
            "phoneNumber": "+12345678901",
            "id": 1
        },
        "isAirportPickupIncluded": false,
        "flightNumber": 0,
        "airlines": {
            "id": 0
        },
        "luggageCount": 0,
        "boosterSeatCount": 0,
        "safetySeatCount": 0,
        "orderNotes": "",
        "orderSum": "401.53",
        "orderType": 3,
        "page": 1,
        "typeId": 0,
        "captcha": ""
    }


**Request**::

      curl --location '/api/v1/external/reservation' \
    --header 'Content-Type: application/json' \
    --header 'Authorization: Bearer <YOUR_SECRET_KEY>' \
    --data-raw '{
        "country2LetterCode": "US",
        "utmSource": "/booking-form/",
        "departure": {
            "StartAt": "12/12/2024  12:55 AM",
            "Addresses": [
                {
                    "rideCheckPoint": "New York Marriott Marquis, Broadway, New York, NY, USA",
                    "latitude": 40.7585862,
                    "longitude": -73.98582019999999,
                    "placeId": "ChIJiVXoAFVYwokREqPijh-d8xg",
                    "placeType": 0
                },
                {
                    "rideCheckPoint": "Chicago O'\''Hare International Airport (ORD), West Balmoral Avenue, Chicago, IL, USA",
                    "latitude": 41.9802588,
                    "longitude": -87.9089858,
                    "placeId": "ChIJ82J3aie0D4gRS61ZAgdHF1E",
                    "placeType": 2
                }
            ]
        },
        "return": null,
        "returnOrderAddressDetails": [],
        "bookingType": 3,
        "passengersQuantity": 2,
        "isRoundTrip": false,
        "orderStartDateTime": "12/12/2024  12:55 AM",
        "returnStartDateTime": "",
        "VehicleDetail": {
            "id": 631
        },
        "hourly": false,
        "hours": 0,
        "paymentInfo": {
            "cardId": "",
            "gclid": ""
        },
        "PassengerDetail": {
            "firstName": "John",
            "lastName": "Doe",
            "email": "john@gmail.com",
            "phoneNumber": "+12345678901",
            "id": 1
        },
        "isAirportPickupIncluded": false,
        "flightNumber": 0,
        "airlines": {
            "id": 0
        },
        "luggageCount": 0,
        "boosterSeatCount": 0,
        "safetySeatCount": 0,
        "orderNotes": "",
        "orderSum": "401.53",
        "orderType": 3,
        "page": 1,
        "typeId": 0,
        "captcha": ""
    }'

**Response**

``Status: 200``

``Content-Type: application/json``

