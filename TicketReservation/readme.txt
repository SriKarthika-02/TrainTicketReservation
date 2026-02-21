Requirements
1. Passenger Details
Each passenger must have the following attributes:
Passenger ID (auto-generated and unique)
Name
Age
Berth Preference (Lower / Middle / Upper)
Allotted Berth
Booking Status (CONFIRMED / RAC / WAITING)
Passenger ID should be automatically assigned starting from 1.

2. Ticket Availability Rules
The train contains:
63 Confirmed Berths
21 Lower
21 Middle
21 Upper
18 RAC Tickets
10 Waiting List Tickets

3. Booking Logic
When a passenger requests booking:
If confirmed tickets are available:
Allocate berth based on preference if available.
Otherwise allocate any available berth.
Status → CONFIRMED
If confirmed tickets are full but RAC is available:
Allocate RAC seat.
Status → RAC
If RAC is full but waiting list is available:
Add to waiting list.
Status → WAITING
If all are full:
Display “No tickets available”.

4. Cancellation Logic
When a confirmed ticket is cancelled:
Release the berth.
Move the first RAC passenger to confirmed.
Move the first waiting passenger to RAC.
This upgrade must follow FIFO order.

5. System Functionalities
The system should provide the following operations:
Book Ticket
Cancel Ticket using Passenger ID
Display Available Tickets
Display Confirmed Passengers
Display RAC List
Display Waiting List
Exit

6. Constraints
Use arrays or appropriate data structures.
Maintain counts properly after booking and cancellation.
Ensure unique passenger ID generation.
Follow modular design with classes and methods.