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

   GET /api/v1/external/airlines?search=air

**Request**::

      curl --location '/api/v1/external/airlines' \
      --header 'Authorization: Bearer <YOUR_SECRET_KEY>'

**Response**

   .. code-block:: json

    [
        {
            "id": 63,
            "name": "Edelweiss Air",
            "code": "WK",
            "code3Letter": "EDW"
        },
        {
            "id": 106,
            "name": "Mango",
            "code": "JE",
            "code3Letter": "MNO"
        },
        {
            "id": 2,
            "name": "Aer Lingus",
            "code": "EI",
            "code3Letter": "EIN"
        },
        {
            "id": 65,
            "name": "El Al Israel Airlines",
            "code": "LY",
            "code3Letter": "ELY"
        },
        {
            "id": 16,
            "name": "Air Europa",
            "code": "X5",
            "code3Letter": null
        },
        {
            "id": 1495,
            "name": "Envoy Air",
            "code": "MQ",
            "code3Letter": "ENY"
        },
        {
            "id": 70,
            "name": "EVA Air",
            "code": "BR",
            "code3Letter": "EVA"
        },
        {
            "id": 140,
            "name": "Spirit Airlines",
            "code": "NK",
            "code3Letter": "NKS"
        },
        {
            "id": 91,
            "name": "Jet2.com",
            "code": "LS",
            "code3Letter": "EXS"
        },
        {
            "id": 62,
            "name": "easyJet Switzerland",
            "code": "DS",
            "code3Letter": "EZS"
        }
    ]
