Create an itinerary
===================

This HTTP POST request is used to create an itinerary in the external API. The request should include the following parameters in the raw request body:

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

   POST /api/v1/external/create-itinerary

**Body**::

    {
      "eventName": "Corporate Meeting",
      "startDate": "2024-12-12T00:00:00",
      "endDate": "2024-12-12T00:00:00",
      "profitMargin": 10
    }


**Request**::

    curl --location '/api/v1/external/create-itinerary' \
    --header 'Content-Type: application/json' \
    --header 'Authorization: Bearer <YOUR_SECRET_KEY>' \
    --data '{
        "eventName": "Corporate Meeting",
        "startDate": "2024-12-12T00:00:00",
        "endDate": "2024-12-12T00:00:00",
        "profitMargin": 10
    }'

**Response**

``Status: 200``

``Content-Type: application/json``






