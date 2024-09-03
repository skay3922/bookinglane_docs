.. Bookinglane documentation master file, created by
   sphinx-quickstart on Tue Sep  3 11:16:50 2024.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Bookinglane documentation
=========================

Add your content using ``reStructuredText`` syntax. See the
`reStructuredText <https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html>`_
documentation for details.

External Top-up Balance
========================

This endpoint allows you to top up the balance using the provided card details.

Request Body
------------

- **CardId** (string, optional): The ID of the card.
- **CardNumber** (string): The card number.
- **NameOnCard** (string): The name on the card.
- **ExpirationDate** (string): The expiration date of the card.
- **CVV** (string): The CVV code of the card.
- **Nickname** (string): A nickname for the card.
- **IsMain** (boolean): Indicates if the card is the main card.
- **AddressZip** (string): The zip code of the cardholder's address.
- **Balance** (number): The balance to be added.

Response
--------

The response will contain the result of the top-up operation.


.. toctree::
   :maxdepth: 2
   :caption: Contents:

   corporate_account
