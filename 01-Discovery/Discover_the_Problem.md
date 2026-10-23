# Week 1 - Initial Discovery

## 1. Facts
1. The college provides a range of student services, such as academic support, careers advice, learning support, and other services
2. Students may contact services through email or phone.
3. Staff can use calenders, spreadsheets and other informal methods to manage appointments.
4. Students may be unsure which service they should contact.
5. Students may not know when appointments are available.
6. Staff spend time managing appointments manually.
7. Cancellations and changes can be difficult to manage.
8. Different staff may have different appointment types and availability.
 
## 2. Assumptions


## 3. Unknowns

Manual or automated system?
Staff/student numbers?
Consequences/penalty for not returning equipment?
Maintence provider?
Who is responsible for supplying the equipment?
Time limit difference for the type of equipment?
The budget required?
Accessibility requirements?
Reminders?
4. Stakeholders

Students - Availability, easy booking
Staff - Equipment
College - Purchasing/managing equipment
Suppliers - Equipment, alerts for limited/missing equipment
IT Support - Assistance for students/staff
Security - Data protection for the system Challenge: Staff/College may want to know the student booking the equipment while students may prefer to be anonymous when booking equipment.
5. Goals

This system should help the college to efficiently monitor the amount of bookings for equipment (prevent the ability of double-booking an equipment).
This system should help the college to efficiently monitor the availability/visibility of equipment, and any missing/not returned equipment.
This system should the stakeholders to be able to communicate efficiently and more easily.
6. Scope

In scope:
Real Time Inventory Tracking: To be able to track down the progress of when the equipment becomes available or is unavailable.
Special Order Management: To be able to record any details and status relating to custom requests.
Recording Sales Transaction History: To be able to record and review any transactions made within the system.
Out of scope/not yet established:
Supplier Purchasing: Can the system place orders with third-party vendors without the need of authorisation?
E-Books Support: Does the system support the likes of e-books in terms of sales/distribution?
A Digital Reading List Integration: Does the systems have a link that extracts textbook lists from the college's curriculum software?
7. Candidate Requirements

Functional requirements:
The system shall allow an authorised user to request equipment for a specified date and time.
The system shall reveal the availability of the equipment for authorised users.
The system shall notify the deadlines for returning equipment to users, along with the fines in failing to do so.
The system shall allow authorised staff to manage equipment bookings.
Non-functional requirements:
The system shall support accessible use.
The system shall restrict booking-management functions to authorised users.
8. Requirement Surgery

R1 - "The system should be easy to use."
Issue - Weak requirement because "easy" is subjective and difficult to test.
Rewrite - 90% of 1st year student should be able to book equipment without assistance.
R2 - "The system should be secure."
Issue - Secure can be subjective. How secure does the system need to be?
Rewrite - The system should encrypt all customer personal records and sales history in transit and restrict access to financial dashboards strictly to verified store managers.
9. Reflection

Upon the completion of the Discovery phase, it's clear that there may be some conflicts between students (for flexibility) and the shop (for profitability). While students may prefer zero risk when making purchases on the system, the shop can't afford to hold dead stock. The system may need a compromise, such as a mandatory deposit system, or an automated message for collection reminders and deadline reminders.
