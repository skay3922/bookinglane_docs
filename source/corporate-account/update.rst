Update corporate account
========================

This endpoint is used to update a corporate account.

**Request Body**

- ``Id`` (text): The ID of the corporate account.
- ``Name`` (text): The name of the corporate account.
- ``Discount`` (text): The discount applicable to the corporate account.
- ``IsReservationPaymentRequired`` (text): Indicates if reservation payment is required for the corporate account.

**Response**

The response will contain the updated details of the corporate account.

Example:
--------

**Endpoint**::

   PUT api/v1/external/update-corporate-account

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

