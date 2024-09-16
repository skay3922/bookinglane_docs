Get Corporate Account By Id
=============================

This endpoint retrieves the details of a specific corporate account.

**Request**

- **Method:** GET
- **URL:** ``/api/v1/external/corporate-account/{id}``

**Response**

- **Status:** 200
- **Content-Type:** application/json

The response contains the details of the corporate account, including:

- ``Account Name`` (text): The name of the corporate account.
- ``Discount`` (text): The discount associated with the corporate account.
- ``Logo`` (file): The logo of the corporate account.
- ``Outstanding Balance`` (text): The outstanding balance for the corporate account.
- ``Company Client Information`` (text): Details about the associated company client, including:
  - ``Company Information`` (text): Information about the associated company.
  - ``Contact Details`` (text): Contact details for the company.
  - ``Address`` (text): The address of the company.
  - ``Payment Information`` (text): Payment-related details.
  - ``Other Attributes`` (text): Additional related attributes.

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

