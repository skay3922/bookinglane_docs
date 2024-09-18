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

   GET /api/v1/external/detail

**Request**::

   curl --location '/api/v1/external/detail' \
   --header 'Authorization: Bearer <YOUR_SECRET_KEY>'

**Response**

.. code-block:: json

    {
        "name": "Company Name",
        "discount": 10.0,
        "logo": "https://bookinglane-images.S3.us-east-2.amazonaws.com/2647e01b7b3f9a207f72",
        "isReservationPaymentRequired": true,
        "outstandingBalance": 1000,
        "companyClientId": 1,
        "companyClient": {
            "companyId": 1,
            "company": null,
            "firstName": "John",
            "lastName": "Doe",
            "email": "email@email.com",
            "phoneNumber": "+12345678901",
            "description": null,
            "isDeleted": false,
            "stripeCustomerId": "",
            "cardLast4": "4242",
            "isCreatedByManager": false,
            "isMigrated": false,
            "oldClientId": null,
            "clientType": 0,
            "address": null,
            "country": "US",
            "state": null,
            "stateId": null,
            "city": null,
            "cityId": null,
            "zip": null,
            "clientStripeAccountId": null,
            "globalUserId": "xpyYL4ufSHdQ8LOtW2",
            "ownerUserId": "xpyYL4ufSHdQ8LOtW2",
            "createdFromApp": 0,
            "updatedFromApp": 0,
            "isTravelAgent": false,
            "travelAgentCompany": null,
            "travelAgentWebsite": null,
            "iconColor": "#4D4DE0",
            "isPassenger": false,
            "clientStripeAccount": null,
            "corporateDiscountId": null,
            "corporateDiscount": null,
            "corporateAccountStaff": null,
            "invoices": null,
            "reservations": null,
            "passengerReservations": null,
            "payments": null,
            "clientCards": [
            ],
            "corporateBalanceHistories": null,
            "id": 1,
            "createdBy": 0,
            "created": "2024-07-12T05:39:06.454802",
            "lastModifiedBy": 0,
            "lastModified": "2024-09-16T10:33:10.266251"
        },
        "secretKey": "LhfGXoKjFmmjf9llX1ZPUi3AM7GQ123gEsqth3O0vzmKyY=",
        "isDeleted": false,
        "isActive": true,
        "id": 1
    }

