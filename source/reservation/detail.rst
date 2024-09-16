Detail reservation
==================

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

   POST /api/v1/external/top-up-balance

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
