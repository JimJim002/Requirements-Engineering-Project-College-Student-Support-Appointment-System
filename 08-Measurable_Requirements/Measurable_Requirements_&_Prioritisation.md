# Week 8 - Measurable Requirements & Prioritisation

## 1. Seven-Field Catalogue
### ID | Statement | Type | Priority | Source | Rationale | Verification
* FR-01 | The system shall allow an authorised user to view appointment availability for a selected date. | FR | Must | Week 3 | Authorised users should see the time slots that are available before they could book. | Input a date to verify the time slot display.
* FR-02 | The system shall prevent a user from booking a selected appointment again or an appointment that is unavailable for the selected dates. | FR | Must | Week 3 | To prevent double-booking and conflicts with scheduling. | Select an unavailable time slot to get an error notification.
* FR-03 | The system shall require the user to input an expected appointment date before a new booking can be successfully saved. | FR | Must | Week 3 | To make sure that the valid dates are saved within the booking. | Try to submit a booking request without an inputted date.
* FR-04 | The system shall allow an authorised user to book an available appointment slot for a selected date and sends a confirmation notification. | FR | Must | Week 3 | To provide booking confirmation and to supply the authorised user with a receipt. | Submit a booking request for verification and receiving a rceipt.
* CFR-01 | The system shall allow students to be able to filter out any available appointments based on service type and the specific staff member and student mentor. | FR | Must | Week 2 | Helps in making navigation and browsing much quicker. | Filter by department, service type, specific staff member and student mentor.
* CFR-02 | The system shall provide automatic notifications and emails to students upon successful bookings, updates or cancellations. | FR | Should | Week 2 | Keeps students informed to avoid missing out their appointments. | Complete a booking, update or cancellation to receive notifications.
* CFR-03 | The system shall allow the support staff members and student mentors to be able to manually cancel and rearrange booked appointments in case of an emergency occurring. | FR | Could | Week 2 | Provides some flexibility if one has to be absent. | Verify using staff and student mentor emergency cancellations and updates notifications.
* CFR-04 | The system shall allow administrators to assign a guest/contractor role to external users, restricting data access only to their booked students. | FR | Could | Week 2 | Enables the role and allowing external contractors to operate within the system. | As an administrator staff, log into the system and assign the guest/contractor role to a test account.
* CFR-05 | The system shall allow authorised users to view their scheduled appointment based on their role permissions. | FR | Must | Week 4 (UC-02) | Enables students and staff to check their upcoming bookings. | Log in as a student and view any booked appointments.
* CFR-06 | The system shall allow the authorised user to update their booked appointments to a new available date and time slot. | FR | Must | Week 4 (UC-03) | Enables students and staff to update their booked appointments. | Select a booked appointment and update it based on the new date and available time slot.
* CFR-07 | The system shall allow authorised users to cancel their booked appointments and marked that cancelled time slot as available again. | FR | Must | Week 4 (UC-04) | Enables students and staff to cancel their booked appointments and to free up the cancelled appointment slot. | Select a booked appointment and cancel it by confirming the cancellation and supplying a reason for cancellation.
* CFR-08 | The system shall allow staff members and student mentor to set when they are available or unavailable by setting and updating their working hours and dates. | FR | Must | Week 4 (UC-06) | Allows the staff and mentors when they are available for student bookings. | Log in as staff or student mentor and update their availability hours.
* CFR-09 | The system shall allow administrative staff to monitor the department appointment metrics, student attendance and no-shows. | FR | Could | Week 4 (UC-07) | Allows the administrative staff to track and audit missed appointments. | Log in as an administrator and filter out the attendance and no-show metrics by date and time.
* NFR-01 | The system shall display appointment availability search results within 2 to 3 seconds of a user submitting their request. | NFR | Should | Week 3 | Maintains consistency with the responsiveness of the system. | Perform a booking and record the response time.
* NFR-02 | The system shall limit and restrict the external contractors into only being able to view details of their assigned students. | NFR | Must | Week 2 & CFR-04 [PROPOSED - confirm with stakeholders] | Protects student privacy. | As an external contractor, log into the system and see whether they are blocked by the system to view unassigned students.
* NFR-C03 | The system shall allow the student to complete their booking journey using keyboard only without needing a mouse. | NFR | Provisional | [PROPOSED - confirm with stakeholders] | Allows students who can't use a mouse to still be able to perform the actions offered by the system. | Walk through the processes of booking, updating and cancelling appointments (SCREENS 1 to 6).

## 2. Check Measurable NFR Candidates
### Candidate ID | Proposed Requirement | Evidence Needed | How it could be Tested?
* NFR-01 | The system shall display at least 95% of the availability search results under a load of 50 student searches within 2 to 3 seconds of the submission. [PROPOSED - confirm with stakeholders] | Confirmation from IT/Technicians required to know the peak student searches and an acceptable response limit. | Run a 50 user load test and meaure the response times.  
* NFR-02 | The system shall limit and restrict the external contractors into only being able to view details of their assigned students. [PROPOSED - confirm with stakeholders] | Confirmation from Administrative Staff and IT/Technicians required for contractor role's permissions. | Using a test external contractor account, log into the system and verify if the system blocks the account from accessing the details of unassigned student bookings. 
* NFR-C03 | The system shall allow the student to complete their booking journey using keyboard only without needing a mouse. [PROPOSED - confirm with stakeholders] | Confirmation from IT/Technicians required for the keyboard accessibility integration. | Using only the keyboard, walk through the booking process of the system to ensure that the keyboard buttons are able to function.

## 3. Prioritisation & Release Boundary
### Item | Priority / Status / Justification or Stakeholder Question
* Core Booking, Management & Availability (FR-01 to FR-04, CFR-01, CFR-05 to CFR-08) | Must | The authorised user needs to be able to successfully browse and book an appointment without running into issues such as double-booking or booking conflicts.
* Automatic Notifications (CFR-02) | Should | It's useful for reducing users from missing out on their booked appointments, even though users could view their bookings in the "My Bookings" as an alternative.
* Staff & Mentor Emergency, Guest Role & Attendance Metrics (CFR-03, CFR-04, CFR-09) | Could | Would be desirable since the administrator staff could manage any schedule changes and assigning the guest/contractor role.
* Search Speed (NFR-01) | Should | It's useful for providing a great user experience for the system, though the peak student searches is still requires confirmation.
* External Contractor Restrictions (NFR-02) | Must | Important for protecting the privacy of students before an external contractor logs into the system.
* Booking Walkthrough with Keyboard only (NFR-C03) | Provisional | It may be proposed as being useful in accessibility and support for all students, has yet to be approved.

## 4. Review, Consistency & Traceability
### Checklist
* Single Concern - Pass: Each NFRs checks out only one concern (speed for NFR-01, external contractor restrictions for NFR-02, keyboard walkthrough for NFR-C03).
* Unambiguous Action - Pass: Each NFR specifies what happens (displaying search results for NFR-01, blocking unassigned student details to external contractors for NFR-02, booking navigation with keyboard only for NFR-C03).
* Measurable Outcome - Pass: NFR-01 defines a numeric target (95% of search results displayed with 2 to 3 seconds), while NFR-02 and NFR-C03 defines a pass/fail outcomes for their actions (unassigned student details blocked in NFR-02 and the full booking process with keyboard only in NFR-C03).
* Conditions - Pass: Each NFR when the conditions apply (a peak of 50 student searches for NFR-01, when logged in as an external contractor for NFR-02, navigation without the use of a mouse for NFR-C03).
* Source - Pass: Each NFR are labelled as [PROPOSED - confirm with stakeholders], with some of them having sources from Weeks 2 and 3 and CFR-04 mentioned.
* Objective Test - Pass: Each NFR defines a repeatable verification (50 student searches timing tests for NFR-01, accessibility of unassigned student details blocked for external contractors for NFR-02, walkthrough of how to book with keyboard only for NFR-C03).
* Feasibility / Confirmation - Pending: Each NFR are still required the confirmation of the stakeholders before they could be integrated.

### Weak Statement - NFR-01
* Week 3 Version: "The system shall display appointment availability search results within 2 to 3 seconds of a user submitting their request."
* Week 8 Revised Version: "The system shall display at least 95% of the availability search results under a load of 50 student searches within 2 to 3 seconds of the submission."

### Traceability
#### Stakeholder Need | Requirement ID | Prototype Screen | Intended Check
* Students need to find the right support service they require quickly without ending up booking the wrong appointment. | CFR-01, UC-05 | SCREEN 1 (Browse Support Service - Filter) | By applying the department, service type, staff member or student mentor and their name filters, students could use these filters to get their correct matching results.
* Students need to be able to view open dates and time slots availability to avoid cases of double-booking and to confirm their appointments. | FR-01, FR-02, FR-03, FR-04, UC-01 | SCREEN 2 (Book Appointment) and SCREEN 3 (Booking Confirmed) | By testing empty date submissions, unavailable time slots, and displaying a booking receipt.
* Students need to be able to view, update or cancel their booked appointments and to receive confirmation notifications. | UC-02, UC-03, UC-04, CFR-02 | SCREEN 4 (My Bookings), SCREEN 5 (Update Appointment) and SCREEN 6 (Cancel Appointment) | By following through the processes of viewing, updating or cancelling a booked appointment and to verify the confirmation notification initiates upon successful update or cancellation.

## 5. Summary for Week 8 and Assumptions & Questions
### Verification VS Validation
* Verification (Self-Reviewed): All requirements were reviewed for clarity, for a single concern they contain and the testing of the Week 7 wireframes (to check that the requirements and wordings are correct).
* Validation (*Outstanding*): There's confirmation that are required by the stakeholders for the proposed targets (the response time limit being 2 to 3 seconds, if the peak student searches is 50, the external contractor restrictions and the navigation using keyboard). As there was no live stakeholder walkthrough performed, the real stakeholder needs remains as *outstanding*.

### Why NFR-01 & NFR-02 Matter?
* NFR-01: By having 95% of the search results load within 2 to 3 seconds under a peak load of 50 student searches, this prevents the case of double-booking during busy hours of the system's operation.
* NFR-02: By restricting the external contractors to being able to only view the details of their assigned students, confidential student support records are protected from unauthorised access.

### MoSCoW Justifcation
1. Core Booking, Management & Availability (MoSCoW Choice - "Must"): This is essential for the system to be able to successfully carry out booking requests, updates and cancellations without running into some conflicted time slots and cases of double-booking.
2. Automatic Notifications (MoSCoW Choice - "Should"): This ensures that missed appointments are reduced using automatic notifications, even when there's the option to view booking details as the alternative.

### Assumptions & Questions
1. The peak load target of the student searches and the response limit are yet to be known. Who could answer? IT/Technicians
2. Would the user need to enter a reasoning for their cancellation or is it completely optional (mandatory vs optional)? Who could answer? Administrative Staff
3. Is the booking reference number a necessity for the system to have? Who could answer? IT/Technicians & Administrative Staff

## 6. Reflection
