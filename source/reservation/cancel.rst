Cancel a reservation
====================

This endpoint is used to cancel a reservation.

**Request Body**

- ``Id`` (text): The ID of the reservation to be deleted.

**Response**

The response will indicate the success or failure of the deletion operation.

Example:
--------

**Endpoint**::

   POST /api/v1/external/cancel-reservation

**Body**::

   {
       "Id": 1
   }

**Request**::

       curl --location --request POST '/api/v1/external/cancel-reservation' \
    --header 'Content-Type: application/json' \
    --header 'Authorization: Bearer <YOUR_SECRET_KEY>' \
    --data '{
       "Id": 1
    }'

**Response**

``Status: 200``

``Content-Type: application/json``
