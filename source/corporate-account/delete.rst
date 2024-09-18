Delete corporate account
========================

This endpoint is used to delete a corporate account.

**Request Body**

- ``Id`` (text): The ID of the corporate account to be deleted.

**Response**

The response will indicate the success or failure of the deletion operation.

Example:
--------

**Endpoint**::

   DELETE api/v1/external/delete-corporate-account

**Body**::

  {
    "Id": 7
  }

**Request**::

    curl --location --request DELETE '/api/v1/external/delete-corporate-account' \
    --header 'Content-Type: application/json' \
    --header 'Authorization: Bearer <YOUR_SECRET_KEY>' \
    --data '{
       "Id": 7
    }'

**Response**

      Status: 200
      Content-Type: application/json

