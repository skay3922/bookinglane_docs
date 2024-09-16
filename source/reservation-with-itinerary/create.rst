Create reservation with itinerary
=================================


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

   POST /api/v1/external/top-up-balance

**Body**::

   {
       "CardId": "",
       "CardNumber": "4242424242424242",
       "NameOnCard": "John Doe",
       "ExpirationDate": "2025-12-31T00:00:00",
       "CVV": "123",
       "Nickname": "Personal Card",
       "IsMain": true,
       "AddressZip": "60604",
       "Balance": 1000
   }

**Request**::

      curl --location '/bookinglane-api/v1/external/top-up-balance' \
      --header 'Content-Type: application/json' \
      --header 'Authorization: Bearer <YOUR_SECRET_KEY>' \
      --data '{
         "CardId": "",
         "CardNumber": "4242424242424242",
         "NameOnCard": "John Doe",
         "ExpirationDate": "2025-12-31T00:00:00",
         "CVV": "123",
         "Nickname": "Personal Card",
         "IsMain": true,
         "AddressZip": "60604",
         "Balance": 1000
      }'

**Response**

      Status: 200
      Content-Type: application/json
