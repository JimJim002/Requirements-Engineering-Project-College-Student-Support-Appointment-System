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
1. Students
2. Staff
3. Student Mentors

## 3. Use Cases
### 1. Book an Available Appointment Slot
See if the authorised user is able to book an available appointment slot by logging into the system and reviewing the calendar to see if the appointment is available at the selected date.

### 2. Attempt to Book an Appointment Slot that's already been Taken
See if the authorised user is blocked from booking an appointment slot that has already been taken by logging into the system and reviewing the calendar to see if the appointment has already been booked at the selected date.

### 3. Verify if an Appointment isn't Available at the Selected Date
See if the authorised user is unable to an appointment that is unavailable at the selected date by logging into the system and reviewing the calendar to see if the appointment is unavailable at the selected date.

### 4. Verify if Confirmation Notification Fails to Deliver
See if the authorised user is able to receive a confirmation notification by logging into the system, reviewing the calendar to see if they receive a confirmation notification upon succeeding or failing to book an appointment slot at a selected date.

## 4. Unknowns/Questions

## 5. Reflection
