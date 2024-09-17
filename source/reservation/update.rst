Update reservation
==================

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

.. code-block:: text

    Status: 200
    Content-Type: application/json

