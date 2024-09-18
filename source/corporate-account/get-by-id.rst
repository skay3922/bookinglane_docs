Find a corporate account by ID
==============================

This endpoint retrieves the details of a specific corporate account.

**Request**

- **Method:** GET
- **URL:** ``/api/v1/external/corporate-account/{id}``

**Response**

- **Status:** 200
- **Content-Type:** application/json

The response contains the details of the corporate account, including:

- ``Account Name`` (text): The name of the corporate account.
- ``Discount`` (text): The discount associated with the corporate account.
- ``Logo`` (file): The logo of the corporate account.
- ``Outstanding Balance`` (text): The outstanding balance for the corporate account.
- ``Company Client Information`` (text): Details about the associated company client, including:
  - ``Company Information`` (text): Information about the associated company.
  - ``Contact Details`` (text): Contact details for the company.
  - ``Address`` (text): The address of the company.
  - ``Payment Information`` (text): Payment-related details.
  - ``Other Attributes`` (text): Additional related attributes.

Example:
--------

**Endpoint**::

   GET /api/v1/external/corporate-account/{id}

**Request**::

      curl --location '/api/v1/external/corporate-account/7' \
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
        "secretKey": "",
        "isDeleted": false,
        "isActive": true,
        "id": 1
    }
