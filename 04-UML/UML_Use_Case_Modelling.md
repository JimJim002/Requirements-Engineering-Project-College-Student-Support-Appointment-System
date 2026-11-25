# Week 4 - Requirements Modelling

## 1. Requirements Used
### Functional Requirements
FR-01 "The system shall allow an authorised user to view appointment availability for a selected date." - Book Appointment, View Appointment (Student, Staff, Student Mentor, plus Administrative Staff and External Contractor)

FR-02 "The system shall prevent a user from booking a selected appointment again or an appointment that is unavailable for the selected dates." - Book Appointment (Student, Staff, Student Mentor)

FR-03 "The system shall require the user to input an expected appointment date before a new booking can be successfully saved." - Book Appointment (Student, Staff, Student Mentor, IT/Technician)

FR-04 "The system shall allow an authorised user to book an available appointment slot for a selected date and sends a confirmation notification." - Book Appointment (Student, Staff, Student Mentor)

### Candidate Functional Requirements
CFR-01 "The system shall allow students to be able to filter out any available appointments based on service type and the specific staff member and student mentor." - Browse Support Services, Book Appointment (Student, Student Mentor)

CFR-03 "The system shall allow the support staff members and student mentors to be able to manually cancel and rearrange booked appointments in case of an emergency occurring." - Update Appointment, Cancel Appointment (Staff, Student Mentor)

CFR-04 "The system shall allow administrators to assign a guest/contractor role to external users, restricting data access only to their booked students." - Assign Guest/Contractor Role, View Appointment (External Contractor, Administrative Staff)


## 2. Actors
1. Student
2. Student Mentor
3. Staff
4. Administrative Staff
5. External Contractor
6. IT/Technician

## 3. Use Cases
1. Book Appointment (Student, Student Mentor, Staff) - Allows the authorised user to select a date, check for availability and confirms a new appointment booking.
2. View Appointment (Student, Student Mentor, Staff, Administrative Staff, External Contractor) - Allows the authorised user to view the details and the availability of the appointment based on the roles the user has.
3. Update Appointment (Student, Student Mentor, Staff) - Allows the authorised user to modify or reschedule an existing appointment.
4. Cancel Appointment (Student, Student Mentor, Staff) - Allows the authorised user to cancel a scheduled appointment and free up the time slot.
5. Browse Support Services (Student, Student Mentor) - Allows the students and student mentors to filter and explore available support services by department, specific staff member or specific student mentors.
6. Set Availability (Student Mentor, Staff) - Allows the student mentors and staff to update their availability and working hours.
7. Monitor Attendance & Metrics (Administrative Staff) - Allows the administrative staff to monitor department metrics, no-shows and student attendance.
8. Assign Guest/Contractor Role (Administrative Staff) - Allows the administrative staff to assign the guest/contractor role to external contractors for their booked students.
9. Sync External Calendars (External Contractor) - Allows the external contractors to synchronise their third-party calendar applications with the system to prevent double-booking.
10. Manage System Integration (IT/Technician) - Allows the IT/technicians to configure integrations, user authentications and system deployments.

## 4. Unknowns/Questions
1. How far in advance do the authorised users have to update or cancel their booked scheduled appointment?


## 5. Reflection
