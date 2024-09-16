Create reservation with itinerary
=================================

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