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

**Body form-data**
    
+-------------------------------+--------------------------------------------------+
| Field                         | Value                                            |
+===============================+==================================================+
| Name                          | Company Name                                     |
+-------------------------------+--------------------------------------------------+
| Discount                      | 10                                               |
+-------------------------------+--------------------------------------------------+
| IsReservationPaymentRequired  | false                                            |
+-------------------------------+--------------------------------------------------+
| Logo                          | image.png                                        |
+-------------------------------+--------------------------------------------------+
| User.FirstName                | John                                             |
+-------------------------------+--------------------------------------------------+
| User.LastName                 | Doe                                              |
+-------------------------------+--------------------------------------------------+
| User.Email                    | email@email.com                                  |
+-------------------------------+--------------------------------------------------+
| User.PhoneNumber              | +12345678901                                     |
+-------------------------------+--------------------------------------------------+
| User.Role                     | Admin                                            |
+-------------------------------+--------------------------------------------------+
| User.Password                 | Password123!                                     |
+-------------------------------+--------------------------------------------------+

**Request**::

      curl --location '/api/v1/external/create-corporate-account' \
      --form 'Name="Company Name"' \
    --form 'Discount="10"' \
    --form 'IsReservationPaymentRequired="false"' \
    --form 'Logo=@"/Image.png"' \
    --form 'User.FirstName="John"' \
    --form 'User.LastName="Doe"' \
    --form 'User.Email="email@email.com"' \
    --form 'User.PhoneNumber="+12345678901"' \
    --form 'User.Role="Admin"' \
    --form 'User.Password="Password123!"'

**Response**

      Status: 200
      Content-Type: application/json
