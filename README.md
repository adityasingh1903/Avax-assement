# TicketPurchaseContract

TicketPurchaseContract is a Solidity smart contract that enables users to purchase tickets and process refunds. It ensures that the ticket price is correct, tracks the number of tickets sold, and handles ticket purchases and refunds.

## Contract Overview

The `TicketPurchaseContract` keeps track of the total number of tickets available (`totalTickets`), the price per ticket (`PerTicketPrice`), and the number of tickets sold (`ticketsSold`). It provides functions for purchasing tickets and refunding tickets.

### Contract Functions

#### `purchaseTicket(uint ticketPrice)`

Allows a user to purchase tickets by providing the `ticketPrice` as payment. It performs the following checks:

- Ensures that the `ticketPrice` is a multiple of the `PerTicketPrice`.
- Verifies that the number of tickets sold (`ticketsSold`) plus one does not exceed the total number of tickets (`totalTickets`).

Upon successful validation, the tickets are purchased, the number of tickets sold is updated, and an event is emitted to indicate the ticket purchase.

#### `refundTicket(uint numTickets)`

Allows the contract owner to refund tickets by specifying the number of tickets (`numTickets`) to be refunded. It performs the following checks:

- Ensures that the number of tickets sold (`ticketsSold`) is greater than or equal to the number of tickets to be refunded (`numTickets`).

Upon successful validation, the specified number of tickets is refunded, and the number of tickets sold is updated accordingly.

### Contract Events

The `TicketPurchaseContract` emits the following event:

- `TicketPurchased`: Triggered when a user purchases tickets, providing the buyer's address and the ticket price.

## Usage

To use the `TicketPurchaseContract`, follow these steps:

1. Deploy the contract on a compatible Ethereum network.
2. Interact with the contract using a compatible wallet or DApp to perform the following actions:
   - Purchase tickets by calling the `purchaseTicket()` function and providing the correct `ticketPrice`.
   - Refund tickets by calling the `refundTicket()` function and specifying the number of tickets to be refunded.

## Author

Aditya Singh

## License

The TicketPurchaseContract is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
