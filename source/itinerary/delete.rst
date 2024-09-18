Delete an itinerary
===================

This endpoint is used to delete a itinerary.

**Request Body**

- ``Id`` (text): The ID of the itinerary to be deleted.

**Response**

The response will indicate the success or failure of the deletion operation.

Example:
--------

**Endpoint**::

   DELETE /api/v1/external/delete-itinerary/{id}

**Request**::

      curl --location '/bookinglane-api/v1/external/delete-itinerary/{id}' \
      --header 'Content-Type: application/json' \
      --header 'Authorization: Bearer <YOUR_SECRET_KEY>''

**Response**

``Status: 200``

``Content-Type: application/json``
