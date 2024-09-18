Obtain itinerary details
========================

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

   GET /api/v1/external/itinerary/{id}

**Request**::

      curl --location /api/v1/external/itinerary/{id}' \
      --header 'Authorization: Bearer <YOUR_SECRET_KEY>'

**Response**::

    {
        "id": 150190,
        "number": "774376",
        "eventName": "Corporate Meeting",
        "startDate": "2024-12-12T00:00:00",
        "endDate": "2024-12-12T00:00:00",
        "profitMargin": 10.0,
        "status": 0,
        "netDue": 0.0,
        "totalAmount": 0.0,
        "reservationsHistory": []
    }

