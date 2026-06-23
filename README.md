# FlightDealAlertApp

It reads in a list of travel destinations and target prices that the user specified from a Google Sheet through the Sheety API which turns a spreadsheet into a JSON. For each destination, it uses the Amadeus API to search for available round-trip flights from the location over the next six months.

If the destination is missing an airport code, the program automatically looks it up using Amadeus and updates the spreadsheet. Then it checks flight offers, finds the cheapest option, and compares that price against the target price stored in the sheet.

If the flight is cheaper than the target price, the app sends a low-price alert through SMTP email.
