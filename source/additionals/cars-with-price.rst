Car with price
==============

``POST /api/v1/external/cars-with-price``

This endpoint is used to retrieve information about cars with their prices for external use.

**Request Body**

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

Example:
--------

**Endpoint**::

   POST /api/v1/external/cars-with-price
   
**Body**::

    {
        "country2LetterCode": "US",
        "captcha": "",
        "hours": 3,
        "isGateMeeting": false,
        "orderAddressDetails": [
            {
                "rideCheckPoint": "San Francisco International Airport (SFO), San Francisco, CA, USA",
                "latitude": 37.6192526,
                "longitude": -122.3815739,
                "placeId": "ChIJVVVVVYx3j4ARP-3NGldc8qQ",
                "placeType": 2,
                "landmark": "San Francisco International Airport",
                "city": "San Francisco",
                "state": "CA",
                "postalCode": "94128"
            },
            {
                "rideCheckPoint": "183 Sierra Ct, Morgan Hill, CA 95037, USA",
                "latitude": 37.1415128,
                "longitude": -121.6650666,
                "placeId": "EikxODMgU2llcnJhIEN0LCBNb3JnYW4gSGlsbCwgQ0EgOTUwMzcsIFVTQSIxEi8KFAoSCW8zkX3bII6AEZ_w8smZZOAIELcBKhQKEglXE3iB3CCOgBH7XHs9tKVpBA",
                "placeType": 0,
                "landmark": "183 Sierra Ct",
                "city": "Morgan Hill",
                "state": "CA",
                "postalCode": "95037"
            }
        ],
        "returnOrderAddressDetails": [],
        "pickupDate": "12/12/2024 2:55 AM",
        "returnDate": "",
        "isRoundTrip": false,
        "boosterSeatCount": 0,
        "safetySeatCount": 0,
        "page": 1,
        "typeId": 1,
        "bookingType": 2,
        "passengersQuantity": 0,
        "isAirportPickupIncluded": true
    }


**Request**::

    
    curl --location '/api/v1/external/cars-with-price' \
    --header 'Content-Type: application/json' \
    --header 'Authorization: Bearer <YOUR_SECRET_KEY>' \
    --data '{
        "country2LetterCode": "US",
        "captcha": "",
        "hours": 3,
        "isGateMeeting": false,
        "orderAddressDetails": [
            {
                "rideCheckPoint": "San Francisco International Airport (SFO), San Francisco, CA, USA",
                "latitude": 37.6192526,
                "longitude": -122.3815739,
                "placeId": "ChIJVVVVVYx3j4ARP-3NGldc8qQ",
                "placeType": 2,
                "landmark": "San Francisco International Airport",
                "city": "San Francisco",
                "state": "CA",
                "postalCode": "94128"
            },
            {
                "rideCheckPoint": "183 Sierra Ct, Morgan Hill, CA 95037, USA",
                "latitude": 37.1415128,
                "longitude": -121.6650666,
                "placeId": "EikxODMgU2llcnJhIEN0LCBNb3JnYW4gSGlsbCwgQ0EgOTUwMzcsIFVTQSIxEi8KFAoSCW8zkX3bII6AEZ_w8smZZOAIELcBKhQKEglXE3iB3CCOgBH7XHs9tKVpBA",
                "placeType": 0,
                "landmark": "183 Sierra Ct",
                "city": "Morgan Hill",
                "state": "CA",
                "postalCode": "95037"
            }
        ],
        "returnOrderAddressDetails": [],
        "pickupDate": "12/12/2024 2:55 AM",
        "returnDate": "",
        "isRoundTrip": false,
        "boosterSeatCount": 0,
        "safetySeatCount": 0,
        "page": 1,
        "typeId": 1,
        "bookingType": 2,
        "passengersQuantity": 0,
        "isAirportPickupIncluded": true
    }'


**Response**

      Status: 200
      Content-Type: application/json

