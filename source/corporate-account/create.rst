Create corporate account
========================

This endpoint allows you to create a corporate account by submitting the required information.

**Request Body Parameters**

- ``Name`` (text): The name of the corporate account.
  
- ``Discount`` (text): The discount applicable to the corporate account.
  
- ``IsReservationPaymentRequired`` (text): Indicates if reservation payment is required.
  
- ``Logo`` (file): The logo of the corporate account.
  
- ``User.FirstName`` (text): First name of the user associated with the corporate account.
  
- ``User.LastName`` (text): Last name of the user associated with the corporate account.
  
- ``User.Email`` (text): Email of the user associated with the corporate account.
  
- ``User.PhoneNumber`` (text): Phone number of the user associated with the corporate account.
  
- ``User.Role`` (text): Role of the user associated with the corporate account.
  
- ``User.Password`` (text): Password of the user associated with the corporate account.

**Response**

The response of this request is a JSON schema representing the structure of the data returned upon successful creation of the corporate account.

Example:
--------

**Endpoint**::

   POST /api/v1/external/create-corporate-account

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

      curl --location 'https://mgrdev2.bookinglane.com/api/v1/external/create-corporate-account' \
      --form 'Name="Company000"' \
    --form 'Discount="10"' \
    --form 'IsReservationPaymentRequired="false"' \
    --form 'Logo=@"/C:/Users/Qairat/Downloads/Default_two_cartoon_playing_funny_panda_1.jpg"' \
    --form 'Logo=@"/Users/qairat/Desktop/Screenshot 2024-08-23 at 8.43.19 PM.png"' \
    --form 'User.FirstName="Qairat"' \
    --form 'User.LastName="Soodombaev"' \
    --form 'User.Email="skay39234@gmail.com"' \
    --form 'User.PhoneNumber="+996500150110"' \
    --form 'User.Role="Admin"' \
    --form 'User.Password="Company123\!"'

**Response**

      Status: 200
      Content-Type: application/json
