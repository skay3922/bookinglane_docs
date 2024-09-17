Detail corporate account
========================

This endpoint makes an HTTP GET request to retrieve the details of an external booking.

**Request Body**

This endpoint does not require a request body.

**Response**

The response to this request is in JSON format and includes the following parameters:

- ``"name"`` (string): The name associated with the booking.
- ``"discount"`` (number): The discount applied to the booking.
- ``"logo"`` (null): The logo associated with the booking.
- ``"isReservationPaymentRequired"`` (boolean): Indicates if reservation payment is required.
- ``"outstandingBalance"`` (number): The outstanding balance for the booking.
- ``"companyClientId"`` (number): The ID of the company client associated with the booking.
- ``"companyClient"`` (object): Details of the company client, including:
   - ``"companyId"`` (number): The ID of the company.
   - ``"company"`` (null): The name of the company.
   - ``"firstName"`` (string): The first name of the client.
   - ``"lastName"`` (string): The last name of the client.
   - ``"email"`` (string): The email address of the client.
   - ``"phoneNumber"`` (string): The phone number of the client.
   - ``"isDeleted"`` (boolean): Indicates if the client is deleted.
   - ``"isCreatedByManager"`` (boolean): Indicates if the client is created by a manager.
   - ``"isMigrated"`` (boolean): Indicates if the client is migrated.
   - ``"isTravelAgent"`` (boolean): Indicates if the client is a travel agent.
   - ``"isPassenger"`` (boolean): Indicates if the client is a passenger.
   - ``"id"`` (number): The ID of the client.
- ``"clientCards"`` (object): The `clientCards` field contains an array of card objects associated with a client.
   - ``"cardId"`` (string): A unique identifier for the card.
   - ``"isMain"`` (boolean): Indicates whether the card is the main card for the client.
   - ``"companyClientId"`` (number): The ID of the company client associated with the card.
   - ``"cardLast4"`` (string): The last four digits of the card number.
   - ``"cardNickName"`` (string): A nickname for the card.
   - ``"cardHolderName"`` (string or null): The name of the cardholder, or `null` if not available.
   - ``"globalUserId"`` (string or null): A global user identifier associated with the card, or `null` if not available.
   - ``"brand"`` (string or null): The brand of the card (e.g., Visa, MasterCard), or `null` if not available.
   - ``"id"`` (number): The unique identifier for the card within the system.
- ``"secretKey"`` (string): The secret key associated with the booking.
- ``"isDeleted"`` (boolean): Indicates if the booking is deleted.
- ``"isActive"`` (boolean): Indicates if the booking is active.
- ``"id"`` (number): The ID of the booking.

**Headers**

The request may include headers as required by the server.

**Parameters**

There are no specific parameters required for this request.

Example:
--------

**Endpoint**::

   POST /api/v1/external/detail
   
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

