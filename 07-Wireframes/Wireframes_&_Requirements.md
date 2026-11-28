# Week 7 - Wireframes & Requirements Validation

## 1. Student Support Appointment Booking Cases
### Evidence ID | Given Statement
* FR-01 | Students can view the available appointment slots at a selected date.
* FR-02 | Each appointment slot can only be booked once to avoid double-booking.
* FR-03 | The system requires the user to input an expected appointment date before a new booking could be successfully saved.
* FR-04 | The system allows the students to book the available appointment slots at a selected date and receives a confirmation notification.
* CFR-01 | The students can filter and browse available support services by department, service type and the specific staff member or student mentor.
* CFR-02 | The students gets automatic notifications from the system for bookings, updates and cancellations.
* UC-01 | Allows the students to book appointments by selecting a date, checking the availability and then confirming the booking.
* UC-02 | Allows the students to view their booked appointments details.
* UC-03 | Allows the students to update their booked appointments.
* UC-04 | Allows the students to cancel their booked appointments.
* UC-05 | Allows the students to filter the support services by department, service type and the specific staff member or student mentor.

### Not yet Confirmed
Booking referencing, mandatory/optional cancellation reasons are unconfirmed yet to be approved.

## 2. Planned User Journey
### SCREEN | Proposed Title | Purpose & Case Evidence
* SCREEN 1 | Browse Support Service | Filters support services by department, service type and the specific staff member or student mentor (CFR-01, UC-05), or access via "My Bookings" (UC-02).
* SCREEN 2 | Book Appointment | Displays a support service summary, checks for inputted expected appointment date (FR-03), checks slot availability for the appointment (FR-01, FR-02), and submits the booking (UC-01).
* SCREEN 3 | Booking Confirmed | Shows the confirmed booking and its details, along with sending a confirmation notification to the user (FR-04, CFR-02).
* SCREEN 4 | My Bookings | Contains a filterable table of the appointment details for viewing (UC-02), along with an "Update" and "Cancel" action buttons (UC-03, UC-04).
* SCREEN 5 | Update Appointment | View the current booked appointment summary, selects a new appointment date and time slot (FR-01, FR-02, FR-03, UC-03), and saves and updates the updated booking and sends a confirmation notification for it (CFR-02).
* SCREEN 6 | Cancel Appointment | View the booking summary of the chosen booking, insert a reason for the cancellation (UC-04), and confirms the cancellation (UC-04) and get a confirmation notification for it (CFR-02), otherwise they could keep their booking.

## 3. Structured Walkthrough & Requirements Finding
### Finding/Question | Evidence Type | Action or Next Step
* Booking reference number (SCREENS 3 to 6) - is it a requirement? | Self-review / Candidate Attribute | Maintain booking reference number as a placeholder and verify if it's required by asking the IT/technicians or the administrative staff.
* Is the reasoning for the cancellation an optional field or a mandatory field? | Self-review / Candidate Rule | Verify this with the administrative staff whether it's necessary step to add a reason for the cancellation.
* Can the pattern of SCREEN 3 be mostly reused for confirmation for the update and cancel processes? | Self-review | Dashed a comment, stating that the update and cancellation would trigger a similar receipt and a similar confirmation notification.
* Within SCREEN 1, could the direct entry that leads to SCREENS 4 to 6 be kept (as "My Bookings")? | Self-review |  Dashed a comment, stating that by selecting "My Bookings", this will lead to SCREENS 4 to 6, where users can view, update or cancel their booked appointments.

## 4. Modelling Decisions
* The user journey primarily focuses on the student users, where they can book, view, update and cancel appointments.
* Rounded rectangles were used to act as confirmation notifications and action buttons. Text labels and dashed comments are used to clarify how the system functions.

## 5. Reflection
