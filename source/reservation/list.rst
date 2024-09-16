Reservation List
================

This endpoint makes an HTTP GET request to retrieve a list of external reservations from the server. The response will be in JSON format and will include details such as reservation ID, booking type, round trip status, order and total sums, currency information, passenger quantity, car details, order address, airport pickup details, flight numbers, seat and luggage counts, payment and order status, and country code.

Request Body
------------

This request does not require a request body.

Response Body
-------------

- ``id`` (number): The unique identifier for the reservation.
  
- ``bookingType`` (number): The type of booking for the reservation.
  
- ``isRoundTrip`` (boolean): Indicates whether the reservation is for a round trip.
  
- ``returnStartDateTime`` (string): The start date and time for the return trip, if applicable.
  
- ``orderSum`` (number): The sum of the order.
  
- ``totalSum`` (number): The total sum for the reservation.
  
- ``currencyCode`` (string): The currency code for the reservation.
  
- ``currencySymbol`` (string): The currency symbol for the reservation.
  
- ``orderStartDateTime`` (string): The start date and time for the reservation order.
  
- ``passengersQuantity`` (number): The quantity of passengers for the reservation.
  
- ``carInfo`` (object): Details about the car for the reservation.
  
- ``orderAddressDetails`` (array): An array of objects containing details about the order address, including ride checkpoint, location coordinates, place type, and additional information.
  
- ``returnOrderAddressDetails`` (null): Details about the return order address, if applicable.
  
- ``orderNotes`` (null): Additional notes for the reservation order.
  
- ``hours`` (number): The duration of the reservation in hours.
  
- ``greetClientInfo`` (null): Information about greeting the client, if applicable.
  
- ``isAirportPickupIncluded`` (boolean): Indicates whether airport pickup is included in the reservation.
  
- ``isReturnAirportPickupIncluded`` (boolean): Indicates whether return airport pickup is included in the reservation.
  
- ``flightNumber`` (null): The flight number for the reservation, if applicable.
  
- ``returnFlightNumber`` (null): The return flight number for the reservation, if applicable.
  
- ``airlines`` (null): Details about the airlines for the reservation, if applicable.
  
- ``returnAirlines`` (null): Details about the return airlines for the reservation, if applicable.
  
- ``drivers`` (null): Details about the drivers for the reservation, if applicable.
  
- ``safetySeatCount`` (number): The count of safety seats for the reservation.
  
- ``boosterSeatCount`` (number): The count of booster seats for the reservation.
  
- ``luggageCount`` (number): The count of luggage for the reservation.
  
- ``fromAppEnum`` (number): The application enumeration for the reservation.
  
- ``driverCommissions`` (null): Details about driver commissions, if applicable.
  
- ``currentStatus`` (number): The current status of the reservation.
  
- ``isCustomerCancelRequested`` (boolean): Indicates whether the customer has requested cancellation.
  
- ``paymentStatus`` (number): The payment status of the reservation.
  
- ``orderStatus`` (number): The status of the reservation order.
  
- ``country2LetterCode`` (string): The two-letter country code for the reservation.
  
- ``utmSource`` (null): The UTM source for the reservation, if applicable.
