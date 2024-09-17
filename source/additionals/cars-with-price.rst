Car with price
==============

### ``POST /api/v1/external/cars-with-price``

This endpoint is used to retrieve information about cars with their prices for external use.

**Request Body**

- ``country2LetterCode`` (string): The country code.
  
- ``captcha`` (string): The captcha value.
  
- ``hours`` (number): The number of hours.
  
- ``isGateMeeting`` (boolean): Indicates if gate meeting is required.
  
- ``orderAddressDetails`` (array): Details of the order address including ride checkpoint, latitude, longitude, place ID, place type, landmark, city, state, and postal code.
  
- ``returnOrderAddressDetails`` (array): Details of the return order address.
  
- ``pickupDate`` (string): The pickup date.
  
- ``returnDate`` (string): The return date.
  
- ``isRoundTrip`` (boolean): Indicates if it's a round trip.
  
- ``boosterSeatCount`` (number): The count of booster seats.
  
- ``safetySeatCount`` (number): The count of safety seats.
  
- ``page`` (number): The page number.
  
- ``typeId`` (number): The type ID.
  
- ``bookingType`` (number): The booking type.
  
- ``passengersQuantity`` (number): The quantity of passengers.
  
- ``isAirportPickupIncluded`` (boolean): Indicates if airport pickup is included.

Example:
--------

**Endpoint**::

   POST /api/v1/external/cars-with-price
   
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

