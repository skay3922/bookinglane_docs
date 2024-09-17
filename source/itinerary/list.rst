Itinerary List
==============

The API endpoint ``GET /api/v1/external/get-itineraries`` is used to retrieve itineraries based on the search parameter provided.

**Response**

The response will be a JSON array with the following structure:

- ``id`` (number): The unique identifier for the itinerary.
    
- ``number`` (string): The itinerary number.
    
- ``eventName`` (string): The name of the event associated with the itinerary.
    
- ``startDate`` (string): The start date of the itinerary.
    
- ``endDate`` (string): The end date of the itinerary.
    
- ``profitMargin`` (number): The profit margin for the itinerary.
    
- ``status`` (number): The status of the itinerary.
    
- ``netDue`` (number): The net amount due for the itinerary.
    
- ``totalAmount`` (number): The total amount for the itinerary.
    
- ``reservationsHistory`` (array): An array of reservation history objects, each containing:
    
    - ``reservation`` (object): Details of the reservation.
        
    - ``itinerary`` (object): Details of the itinerary.
        
    - ``corporateAccount`` (object): Details of the corporate account associated with the reservation.
        
        - ``name`` (string): The name of the corporate account.
            
        - ``discount`` (number): The discount for the corporate account.
            
        - ``logo`` (string): The logo of the corporate account.
            
        - ``isReservationPaymentRequired`` (boolean): Indicates if reservation payment is required for the corporate account.
            
        - ``outstandingBalance`` (number): The outstanding balance for the corporate account.
            
        - ``companyClientId`` (number): The unique identifier for the company client.
            
        - ``companyClient`` (object): Details of the company client.
            
            - Various properties for the company client.
                
        - ``secretKey`` (string): The secret key for the corporate account.
            
        - ``isDeleted`` (boolean): Indicates if the corporate account is deleted.
            
        - ``isActive`` (boolean): Indicates if the corporate account is active.
            
        - ``id`` (number): The unique identifier for the corporate account.
            
    - ``amount`` (number): The amount associated with the reservation.
        
    - ``discountAmount`` (number): The discount amount for the reservation.
        
    - ``profit`` (number): The profit for the reservation.
        
    - ``isCanceled`` (boolean): Indicates if the reservation is canceled.
        
    - ``itineraryId`` (number): The unique identifier for the itinerary associated with the reservation.
        
    - ``corporateAccountId`` (number): The unique identifier for the corporate account associated with the reservation.
        
    - ``reservationId`` (number): The unique identifier for the reservation.
        
    - ``id`` (number): The unique identifier for the reservation history.
        
Please note that the actual response may contain multiple objects within the array, each representing a different itinerary.


Example:
--------

**Endpoint**::

   POST /api/v1/external/get-itineraries?SearchParam=event

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
