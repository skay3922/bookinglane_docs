Car with price
==============

### POST /api/v1/external/cars-with-price

This endpoint is used to retrieve information about cars with their prices for external use.

#### Request Body

- ``country2LetterCode`` (string): The country code.
  
- ``captcha`` (string): The captcha value.
  
- ``hours`` (number): The number of hours.
  
- ``isGateMeeting`` (boolean): Indicates if gate meeting is required.
  
- ``orderAddressDetails`` (array): Details of the order address including ride checkpoint, latitude, longitude, place ID, place type, landmark, city, state, and postal code.
  
- ``returnOrderAddressDetails`` (array): Details of the return order address.
  
- ``pickupDate`` (string): The pickup date.
  
- ``returnDate`` (string): The return date.
  
- ``isRoundTrip`` (boolean): Indicates if it's a round trip.
  
- ``boosterSeatCount`` (number): The count of booster seats.
  
- ``safetySeatCount`` (number): The count of safety seats.
  
- ``page`` (number): The page number.
  
- ``typeId`` (number): The type ID.
  
- ``bookingType`` (number): The booking type.
  
- ``passengersQuantity`` (number): The quantity of passengers.
  
- ``isAirportPickupIncluded`` (boolean): Indicates if airport pickup is included.