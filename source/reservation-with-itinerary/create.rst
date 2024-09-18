Create a reservation with itinerary
===================================


This endpoint allows you to make a reservation with itinerary details.

Request Body
------------

- ``accessKey`` (string, required): The access key for the reservation.
  
- ``reservation`` (object, required): The reservation details including itinerary and passenger information.
  
  - ``country2LetterCode`` (string, required): The 2-letter country code for the reservation.
  
  - ``utmSource`` (string, required): The UTM source for the reservation.
  
  - ``OrderAddressDetails`` (array, required): Details of the order address including ride checkpoint, latitude, longitude, and place ID.
  
  - ``return`` (null): Details of the return trip, if applicable.
  
  - ``returnOrderAddressDetails`` (array): Details of the return trip order address.
  
  - ``bookingType`` (integer, required): The type of booking.
  
  - ``passengersQuantity`` (integer, required): The quantity of passengers.
  
  - ``isRoundTrip`` (boolean, required): Indicates if the trip is round trip.
  
  - ``orderStartDateTime`` (string, required): The start date and time of the order.
  
  - ``returnStartDateTime`` (string, required): The start date and time of the return trip, if applicable.
  
  - ``CarInfo`` (object, required): Information about the car.
  
  - ``hourly`` (boolean, required): Indicates if the reservation is hourly.
  
  - ``hours`` (integer, required): The number of hours for the reservation.
  
  - ``paymentInfo`` (object, required): Information about the payment including card ID and GCLID.
  
  - ``Customer`` (object, required): Customer details including first name, last name, email, and phone number.
  
  - ``isAirportPickupIncluded`` (boolean, required): Indicates if airport pickup is included.
  
  - ``flightNumber`` (integer, required): The flight number, if applicable.
  
  - ``airlines`` (object, required): Information about the airlines.
  
  - ``luggageCount`` (integer, required): The count of luggage.
  
  - ``boosterSeatCount`` (integer, required): The count of booster seats.
  
  - ``safetySeatCount`` (integer, required): The count of safety seats.
  
  - ``orderNotes`` (string, required): Additional notes for the order.
  
  - ``orderSum`` (string, required): The order sum.
  
  - ``orderType`` (integer, required): The type of order.
  
  - ``page`` (integer, required): The page number.
  
  - ``typeId`` (integer, required): The type ID.
  
  - ``captcha`` (string, required): The captcha for the reservation.
  
  - ``Itinerary`` (string, required): The itinerary details.
  
  - ``Passenger`` (object, required): Passenger details including first name, last name, and email.

Response
--------

The response of this request is an empty array ``[]``.

Example:
--------

**Endpoint**::

   POST /api/v1/external/reservation-with-itinerary

**Body**::

    {
      "reservation": {
        "country2LetterCode": "US",
        "utmSource": "/booking-form/",
        "OrderAddressDetails": [
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
        ],
        "return": null,
        "returnOrderAddressDetails": [],
        "bookingType": 3,
        "passengersQuantity": 2,
        "isRoundTrip": false,
        "orderStartDateTime": "12/12/2024  12:55 AM",
        "returnStartDateTime": "",
        "CarInfo": {
          "id": 631
        },
        "hourly": false,
        "hours": 0,
        "paymentInfo": {
          "cardId": "",
          "gclid": ""
        },
        "Customer": {
          "firstName": "John",
          "lastName": "Doe",
          "email": "john@gmail.com",
          "phoneNumber": "+12345678901",
          "id": 4362
        },
        "isAirportPickupIncluded": false,
        "flightNumber": 0,
        "airlines": {
          "id": 0
        },
        "luggageCount": 0,
        "boosterSeatCount": 0,
        "safetySeatCount": 0,
        "orderNotes": "Reservation with Itinerary",
        "orderSum": "4013.53",
        "orderType": 3,
        "page": 1,
        "typeId": 0,
        "captcha": "",
        "Itinerary": "150186",
        "Passenger": {
          "firstName": "John",
          "lastName": "Doe",
          "email": "john@gmail.com"
        }
      }
    }


**Request**::

    curl --location 'https://mgrdev2.bookinglane.com/api/v1/external/reservation-with-itinerary' \
    --header 'Content-Type: application/json' \
    --header 'Authorization: Bearer LhfGXoKjFmmjf9llX1ZPUi3AM7GQgEsqth3O0vzmKyY=' \
    --data-raw '{
      "reservation": {
        "country2LetterCode": "US",
        "utmSource": "/booking-form/",
        "OrderAddressDetails": [
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
        ],
        "return": null,
        "returnOrderAddressDetails": [],
        "bookingType": 3,
        "passengersQuantity": 2,
        "isRoundTrip": false,
        "orderStartDateTime": "12/12/2024  12:55 AM",
        "returnStartDateTime": "",
        "CarInfo": {
          "id": 631
        },
        "hourly": false,
        "hours": 0,
        "paymentInfo": {
          "cardId": "",
          "gclid": ""
        },
        "Customer": {
          "firstName": "John",
          "lastName": "Doe",
          "email": "john@gmail.com",
          "phoneNumber": "+12345678901",
          "id": 4362
        },
        "isAirportPickupIncluded": false,
        "flightNumber": 0,
        "airlines": {
          "id": 0
        },
        "luggageCount": 0,
        "boosterSeatCount": 0,
        "safetySeatCount": 0,
        "orderNotes": "Reservation with Itinerary",
        "orderSum": "4013.53",
        "orderType": 3,
        "page": 1,
        "typeId": 0,
        "captcha": "",
        "Itinerary": "150186",
        "Passenger": {
          "firstName": "John",
          "lastName": "Doe",
          "email": "john@gmail.com"
        }
      }
    }'


**Response**

      Status: 200
      Content-Type: application/json
