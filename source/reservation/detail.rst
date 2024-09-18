Obtain reservation details
==========================

This API endpoint makes an HTTP GET request to retrieve details of a specific reservation with the ID from the external system. No request body is required for this request.

API Response
------------

The response returns a JSON object with the following properties:

- ``isCustomerCancelRequested`` (boolean): Indicates whether the customer has requested to cancel the reservation.
  
- ``paymentMethods`` (null): Indicates the absence of payment methods.
  
- ``tripRouteImages`` (array): An empty array representing the trip route images.
  
- ``changedFields`` (null): Indicates the absence of changed fields.
  
- ``id`` (integer): The ID of the reservation.
  
- ``orderSum`` (integer): The order sum.
  
- ``totalSum`` (integer): The total sum.
  
- ``transactionFee`` (integer): The transaction fee.
  
- ``tipsAmount`` (integer): The tips amount.
  
- ``waitingFee`` (integer): The waiting fee.
  
- ``orderStartDateTime`` (string): The start date and time of the order.
  
- ``isRoundTrip`` (boolean): Indicates whether the trip is a round trip.
  
- ``returnStartDateTime`` (null): The absence of return start date and time.
  
- ``totalOrderMileage`` (integer): The total mileage of the order.
  
- ``passengersQuantity`` (integer): The quantity of passengers.
  
- ``carFK`` (integer): The foreign key of the car.
  
- ``paymentStatus`` (integer): The payment status.
  
- ``paymentMethod`` (null): The absence of payment method.
  
- ``paymentId`` (integer): The payment ID.
  
- ``currencyCode`` (string): The currency code.
  
- ``currencySymbol`` (string): The currency symbol.
  
- ``country2LetterCode`` (string): The country's 2-letter code.
  
- ``paymentIndicatorStatus`` (integer): The payment indicator status.
  
- ``carInfo`` (object): Contains details about the car, including type, make, model, license plate, color, image URLs, and pricing information.
  
- ``orderAddressDetails`` (array): Details about the order address, including ride checkpoint, latitude, longitude, place type, and additional information.
  
- ``returnOrderAddressDetails`` (null): The absence of return order address details.
  
- ``orderShareEmailHistory`` (array): An empty array representing the order share email history.
  
- ``partnerShareHistory`` (null): The absence of partner share history.
  
- ``automaticallySharedHistory`` (null): The absence of automatically shared history.
  
- ``transferedCompanyPartnerShareHistory`` (null): The absence of transferred company partner share history.
  
- ``isAirportPickupIncluded`` (boolean): Indicates whether airport pickup is included.
  
- ``isReturnAirportPickupIncluded`` (boolean): Indicates whether return airport pickup is included.
  
- ``flightNumber`` (null): The absence of flight number.
  
- ``returnFlightNumber`` (null): The absence of return flight number.
  
- ``orderNotes`` (null): The absence of order notes.
  
- ``hours`` (integer): The duration of the order in hours.
  
- ``invoiceId`` (integer): The invoice ID.
  
- ``companyName`` (null): The absence of company name.
  
- ``createdByCompanyId`` (integer): The ID of the company that created the order.
  
- ``luggageCount`` (integer): The count of luggage.
  
- ``safetySeatCount`` (integer): The count of safety seats.
  
- ``boosterSeatCount`` (integer): The count of booster seats.
  
- ``safetySeatAmount`` (integer): The amount for safety seats.
  
- ``boosterSeatAmount`` (integer): The amount for booster seats.
  
- ``orderType`` (integer): The type of the order.
  
- ``airlines`` (null): The absence of airlines.
  
- ``returnAirlines`` (null): The absence of return airlines.
  
- ``createdBy`` (object): Contains details about the creator of the order, including their ID, company name, email, phone number, and other information.
  
- ``bookingType`` (integer): The booking type.
  
- ``currentStatus`` (integer): The current status of the order.
  
- ``gNetQuoteStatus`` (null): The absence of GNet quote status.
  
- ``amendmentStatus`` (null): The absence of amendment status.
  
- ``gNetPreferredVehicleType`` (null): The absence of GNet preferred vehicle type.
  
- ``gNetPreferredVehicleTypeId`` (null): The absence of GNet preferred vehicle type ID.
  
- ``clientInfo`` (object): Contains details about the client, including their ID, first name, last name, email, phone number, and other information.
  
- ``greetClientInfo`` (object): Contains details about the greeted client, including their ID, first name, last name, email, phone number, and other information.
  
- ``orderStatus`` (integer): The status of the order.
  
- ``offer`` (null): The absence of an offer.
  
- ``isModified`` (boolean): Indicates whether the order is modified.
  
- ``isShared`` (boolean): Indicates whether the order is shared.
  
- ``showReturnDate`` (null): The absence of return date.
  
- ``drivers`` (object): Contains details about the driver, including their ID, first name, last name, email, phone number, company name, and other information.
  
- ``driverCommissions`` (null): The absence of driver commissions.
  
- ``providerType`` (string): The provider type.
  
- ``additionalFee`` (object): Contains details about additional fees, including the amount, total, and items.
  
- ``promoDiscount`` (null): The absence of promo discount.
  
- ``corporateDiscount`` (null): The absence of corporate discount.
  
- ``flightReservationId`` (null): The absence of flight reservation ID.
  
- ``flightReservation`` (null): The absence of flight reservation.
  
- ``feeImages`` (null): The absence of fee images.


Example:
--------

**Endpoint**::

   GET api/v1/external/reservation/{id}

**Request**::

      curl --location '/api/v1/external/reservation/{id}' \
      --header 'Authorization: Bearer <YOUR_SECRET_KEY>'

**Response**

.. code-block:: json

    {
        "isCustomerCancelRequested": false,
        "paymentMethods": null,
        "tripRouteImages": [],
        "changedFields": null,
        "id": 19483,
        "orderSum": 3310.96,
        "totalSum": 3447.72,
        "transactionFee": 136.76,
        "tipsAmount": 0.0,
        "waitingFee": 0.0,
        "orderStartDateTime": "2024-07-31T00:55:00",
        "isRoundTrip": false,
        "returnStartDateTime": null,
        "totalOrderMileage": 806.6506,
        "passengersQuantity": 0,
        "carFK": 631,
        "paymentStatus": 2,
        "paymentMethod": null,
        "paymentId": 0,
        "currencyCode": "USD",
        "currencySymbol": "$",
        "country2LetterCode": "US",
        "paymentIndicatorStatus": 0,
        "carInfo": {
            "id": 631,
            "typeId": 1,
            "type": "Sedan",
            "make": "Mercedes-Benz",
            "model": "E350",
            "licensePlate": "n/a",
            "color": "Black",
            "country2LetterCode": null,
            "currencyCode": null,
            "currencySymbol": null,
            "imageUrls": [
                {
                    "id": 330,
                    "path": "https://bookinglane-images.S3.us-east-2.amazonaws.com/f2721164-beca-49bb-854b-35181264cb72"
                }
            ],
            "price": 0.0,
            "greetAndMeetPrice": 0.0,
            "safetySeatPrice": 0.0,
            "boosterSeatPrice": 0.0,
            "isBoosterSeatsExist": false,
            "isSafetySeatsExist": false,
            "mileCost": null,
            "cancelationFees": [],
            "capacity": 3,
            "tripTime": 0,
            "tripMileage": 0.0,
            "isIncluded": false
        },
        "orderAddressDetails": [
            {
                "rideCheckPoint": "New York Marriott Marquis, Broadway, New York, NY, USA",
                "latitude": 40.7585862,
                "longitude": -73.9858202,
                "placeType": 0,
                "isReturnPoint": null,
                "placeId": "ChIJiVXoAFVYwokREqPijh-d8xg",
                "meetAndGreet": null,
                "specialInstructions": null,
                "landmark": null,
                "pointOnLocation": null,
                "city": null,
                "state": null,
                "postalCode": null,
                "additionalInfo": null
            },
            {
                "rideCheckPoint": "Chicago O'Hare International Airport (ORD), West Balmoral Avenue, Chicago, IL, USA",
                "latitude": 41.9802588,
                "longitude": -87.9089858,
                "placeType": 2,
                "isReturnPoint": null,
                "placeId": "ChIJ82J3aie0D4gRS61ZAgdHF1E",
                "meetAndGreet": null,
                "specialInstructions": null,
                "landmark": null,
                "pointOnLocation": null,
                "city": null,
                "state": null,
                "postalCode": null,
                "additionalInfo": null
            }
        ],
        "returnOrderAddressDetails": null,
        "orderShareEmailHistory": [],
        "partnerShareHistory": null,
        "automaticallySharedHistory": null,
        "transferedCompanyPartnerShareHistory": null,
        "isAirportPickupIncluded": false,
        "isReturnAirportPickupIncluded": false,
        "flightNumber": null,
        "returnFlightNumber": null,
        "orderNotes": null,
        "hours": 0,
        "invoiceId": 0,
        "companyName": null,
        "createdByCompanyId": 1,
        "luggageCount": 0,
        "safetySeatCount": 0,
        "boosterSeatCount": 0,
        "safetySeatAmount": 0.0,
        "boosterSeatAmount": 0.0,
        "orderType": 3,
        "airlines": null,
        "returnAirlines": null,
        "createdBy": {
            "id": 1,
            "companyName": "Company 0 ",
            "email": "bookinglane.kg@gmail.com",
            "phoneNumber": "+19292897825",
            "rating": 5.0,
            "companyLogo": "https://bookinglane-images.S3.us-east-2.amazonaws.com/9f63c6b2-2ff8-4d9e-98ab-61187b8803d9",
            "state": "California",
            "city": "Fremont",
            "country": "US",
            "reviewsCount": 1,
            "fleetCount": 0,
            "isGNetCompany": false,
            "fullNameOwnerCompany": null,
            "companyPartnerCards": null,
            "cardNickName": null,
            "addressLine": null,
            "cardLast4": null
        },
        "bookingType": 3,
        "currentStatus": 1,
        "gNetQuoteStatus": null,
        "amendmentStatus": null,
        "gNetPreferredVehicleType": null,
        "gNetPreferredVehicleTypeId": null,
        "clientInfo": {
            "id": 4364,
            "firstName": "John",
            "lastName": "Doe",
            "email": "john@gmail.com",
            "phoneNumber": "+14564564564",
            "description": null,
            "cardLast4": "4242",
            "globalUserId": "xpyYP1hxuJVUxYL4ufSHdQ8LOtW2",
            "iconColor": null,
            "passengerId": 0
        },
        "greetClientInfo": {
            "id": 4733,
            "firstName": "John",
            "lastName": "Doe",
            "email": "john@gmail.com",
            "phoneNumber": "+14564564564",
            "description": null,
            "cardLast4": null,
            "globalUserId": null,
            "iconColor": null,
            "passengerId": 4733
        },
        "orderStatus": 2,
        "offer": null,
        "isModified": false,
        "isShared": false,
        "showReturnDate": null,
        "drivers": {
            "id": 0,
            "firstName": null,
            "lastName": null,
            "email": null,
            "phoneNumber": null,
            "companyName": null,
            "profilePhoto": null,
            "todayReservationCount": 0,
            "nextReservationInMilliseconds": null,
            "nextReservationDateTime": null,
            "isApproved": false
        },
        "driverCommissions": null,
        "providerType": "BOOKINGLANE",
        "additionalFee": {
            "id": 0,
            "amount": 3310.96,
            "total": 3310.96,
            "newGratuity": null,
            "items": []
        },
        "promoDiscount": null,
        "corporateDiscount": null,
        "flightReservationId": null,
        "flightReservation": null,
        "feeImages": null
    }

