# UC-07 – Register a return

## Use-case name
Register a return

## Scope
Library system

## Level
User-goal

## Primary actor
Librarian

## Secondary actor
Mail server

## Stakeholders and interests
- **Member:** wants the returned copy recorded correctly and a receipt issued.
- **Librarian:** wants to register the return and know whether the copy is late or reserved.
- **Library:** wants accurate loan records and correct handling of overdue and reserved copies.
- **Mail server:** sends a notification to the member who reserved the copy.

## Preconditions
- The librarian is authenticated.
- The library system is available.

## Trigger
A member brings a borrowed copy to the librarian and requests to return it.

## Main success scenario
1. The librarian selects **Register a return**.
2. The librarian scans the copy's barcode.
3. The system identifies the copy and retrieves its loan information.
4. The system verifies that the copy is currently on loan.
5. The system closes the active loan and records the return date.
6. The system checks whether the return is late.
7. If the return is late, the system activates the extension point **late return**, invoking **Suspend the member** according to the library rules.
8. The system checks whether the copy has an active reservation.
9. If the copy is reserved, the system keeps it aside for the reserving member.
10. The system asks the Mail server to notify the member who reserved the copy.
11. The system updates the copy status and prepares the return receipt.
12. The librarian selects **Print the receipt**.

## Extensions

### 1a – Barcode cannot be read
At step 2:
1. The librarian enters the inventory number manually.
2. The system searches for the copy using that number.
3. The use case resumes at step 3.

### 2a – Copy is not on loan
At step 4:
1. The system displays an error message explaining that the copy is not currently on loan.
2. The use case ends. No loan is closed and no return receipt is printed.

### Late return – Extension point
At step 6, if the return is late, the system invokes **Suspend the member** through the **late return** extension point. The return process then continues.

### Reserved copy
At step 8, if the copy is reserved, the system keeps it aside for the reserving member and requests notification through the Mail server. Otherwise, the copy is set to available.

## Special requirements
- Preserve the return date and loan history.
- Do not register a return when the copy is not on loan.
- Do not treat a reserved copy as freely available to another member.
- Print a receipt at the end of a successful return.

## Technology and data variations
- The barcode may be read by a scanner, or the inventory number may be entered manually.
- The notification is sent through the Mail server.

## Frequency of occurrence
Whenever a member returns a borrowed copy.
