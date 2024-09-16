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
