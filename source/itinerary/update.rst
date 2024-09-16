Update itinerary
================

This HTTP POST request is used to update an itinerary in the external API. The request should include the following parameters in the raw request body:

**Request Body Parameters**

- ``eventName`` (string): The name of the event for the itinerary.
  
- ``startDate`` (string): The start date of the itinerary.
  
- ``endDate`` (string): The end date of the itinerary.
  
- ``profitMargin`` (number): The profit margin for the itinerary.

**Response**

The response to this request has a status code of 200 and a content type of text/xml. The response body is null.


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
