Top up Balance
==============

This endpoint allows you to top up the balance using the provided card details.

Request Body
------------

- ``CardId`` (string, optional): The ID of the card.
- ``CardNumber`` (string): The card number.
- ``NameOnCard`` (string): The name on the card.
- ``ExpirationDate`` (string): The expiration date of the card.
- ``CVV`` (string): The CVV code of the card.
- ``Nickname`` (string): A nickname for the card.
- ``IsMain`` (boolean): Indicates if the card is the main card.
- ``AddressZip`` (string): The zip code of the cardholder's address.
- ``Balance`` (number): The balance to be added.

Response
--------

The response will contain the result of the top-up operation.

Example:
--------

**Endpoint**::

   POST /bookinglane-api/v1/external/top-up-balance

**Body**::

   {
       "CardId": "",
       "CardNumber": "4242424242424242",
       "NameOnCard": "John Doe",
       "ExpirationDate": "2025-12-31T00:00:00",
       "CVV": "123",
       "Nickname": "Personal Card",
       "IsMain": true,
       "AddressZip": "72200",
       "Balance": 15000
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
         "AddressZip": "72200",
         "Balance": 15000
      }'

