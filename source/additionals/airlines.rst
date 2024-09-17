Airlines
========

This endpoint retrieves a list of external airlines.

**Request**

This is a simple GET request with no request body.

**Response**

The response is a JSON array containing objects with the following properties:

- ``id`` (number): The unique identifier for the airline.
- ``name`` (string): The name of the airline.
- ``code`` (string): The airline code.
- ``code3Letter`` (string): The three-letter code for the airline.

**JSON Schema**

.. code-block:: json

    [
      {
        "type": "object",
        "properties": {
          "id": {
            "type": "number"
          },
          "name": {
            "type": "string"
          },
          "code": {
            "type": "string"
          },
          "code3Letter": {
            "type": "string"
          }
        }
      }
    ]

Example:
--------

**Endpoint**::

   GET /api/v1/external/airlines
   
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

