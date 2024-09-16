Detail itinerary
================

The endpoint retrieves the itinerary details for a specific itinerary ID.

**Response**

This JSON object represents an itinerary with the following properties:

- ``id`` (number): The unique identifier for the itinerary.
- ``number`` (string): The itinerary number.

- ``eventName`` (string): The name of the event associated with the itinerary.

- ``startDate`` (string): The start date of the itinerary in ISO 8601 format.

- ``endDate`` (string): The end date of the itinerary in ISO 8601 format.

- ``profitMargin`` (number): The profit margin for the itinerary, represented as a percentage.

- ``status`` (number): The status of the itinerary.

- ``netDue`` (number): The net amount due for the itinerary.

- ``totalAmount`` (number): The total amount for the itinerary.

- ``reservationsHistory`` (array): An array of reservation history objects related to the itinerary. In this case, it is an empty array, indicating no reservations are associated with this itinerary.


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
