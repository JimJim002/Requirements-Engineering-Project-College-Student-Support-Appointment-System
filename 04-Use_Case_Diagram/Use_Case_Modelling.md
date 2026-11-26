# Week 4 - Requirements Modelling

## 1. Requirements Used
### Functional Requirements
FR-01 "The system shall allow an authorised user to view appointment availability for a selected date." - Book Appointment (Student, Student Mentor, Staff), View Appointment (Student, Staff, Student Mentor, Administrative Staff, External Contractor)

FR-02 "The system shall prevent a user from booking a selected appointment again or an appointment that is unavailable for the selected dates." - Book Appointment (Student, Student Mentor, Staff)

FR-03 "The system shall require the user to input an expected appointment date before a new booking can be successfully saved." - Book Appointment (Student, Student Mentor, Staff, plus IT/Technician for integration)

FR-04 "The system shall allow an authorised user to book an available appointment slot for a selected date and sends a confirmation notification." - Book Appointment (Student, Student Mentor, Staff)

### Candidate Functional Requirements
CFR-01 "The system shall allow students to be able to filter out any available appointments based on service type and the specific staff member and student mentor." - Browse Support Services (Student, Student Mentor), Book Appointment (Student, Student Mentor, Staff)

CFR-02 "The system shall provide automatic notifications and emails to students upon successful bookings, updates or cancellations." - Book Appointment (Student, Student Mentor, Staff), Update Appointment (Student, Student Mentor, Staff), Cancel Appointment (Student, Student Mentor, Staff)

CFR-03 "The system shall allow the support staff members and student mentors to be able to manually cancel and rearrange booked appointments in case of an emergency occurring." - Update Appointment (Student, Student Mentor, Staff), Cancel Appointment (Student, Student Mentor, Staff)

CFR-04 "The system shall allow administrators to assign a guest/contractor role to external users, restricting data access only to their booked students." - Assign Guest/Contractor Role (Administrative Staff for External Contractor), View Appointment (Student, Staff, Student Mentor, Administrative Staff, External Contractor)

## 2. Actors
1. Student
2. Student Mentor
3. Staff
4. Administrative Staff
5. External Contractor
6. IT/Technician

## 3. Use Cases
### 1. Book Appointment (Student, Student Mentor, Staff) - Allows the authorised user to select a date, check for availability and confirms a new appointment booking.
1. The authorised user logs into the system.
2. The authorised user filters out the available appointment slots by service type, the staff member or student mentor.
3. The authorised user selects an expected appointment date.
4. The authorised user selects the time slot available and then submits their request.
5. Once the system verifies the appointment slot is available, the system saves the booking, marks the slot as unavailable, and then sends a confirmation notification to the authorised user.

### 2. View Appointment (Student, Student Mentor, Staff, Administrative Staff, External Contractor) - Allows the authorised user to view the details and the availability of the appointment based on the roles the user has.
1. The authorised user logs into the system.
2. The authorised user check the appointment calendar.
3. The authorised user filters out the appointments by date, service type, staff member or student mentor.
4. The system then verifies the user by their role and access permission.
5. The system would then display the relevant information of the appointments at the available time slot for that role.

### 3. Update Appointment (Student, Student Mentor, Staff) - Allows the authorised user to modify or reschedule an existing appointment.
1. The authorised user logs into the system.
2. The authorised user checks their booked scheduled appointment.
3. The authorised user could then update the old date into a new date to check for available time slots in the new date.
4. The authorised user selects the new available time slot and date and submits their request to the system.
5. The system would verify the availability for the new time slot, updates the booking, removes the previous time slot, and marks the new time slot as unavailable once it's verified. If the time slot is unavailable or is already booked, the system blocks the booking, displaying an error message asking the user to choose a different time slot.
6. The system would send a confirmation notification to the authorised user to confirm the new booking.

### 4. Cancel Appointment (Student, Student Mentor, Staff) - Allows the authorised user to cancel a scheduled appointment and free up the time slot.
1. The authorised user logs into the system.
2. The authorised user checks their booked scheduled appointment.
3. The authorised user could then select that booked scheduled appointment to cancel.
4. The authorised user enters their reasons for the cancellation and is asked if they want to confirm the cancellation.
5. Once confirmed, the system would verify the cancellation of the booking, updates the booking status as cancelled and marked the time slot available again.
6. The system would send a confirmation notification to the authorised user to confirm their cancellation.

### 5. Browse Support Services (Student, Student Mentor) - Allows the students and student mentors to filter and explore available support services by department, specific staff member or specific student mentors.
1. The authorised user logs into the system.
2. The authorised user would navigate to support services.
3. The authorised user could then select to filter based on the service type, the department, the specific staff member and the specific student mentor.
4. The system would verify the filter and displays the matching support services, provided with information regarding of its availability and specific staff member or student mentor, allowing the authorised user to select the specific service they need for viewing and for booking.
   
### 6. Set Availability (Student Mentor, Staff) - Allows the student mentors and staff to update their availability and working hours.
1. The authorised user logs into the system.
2. The authorised user would navigate to the schedule or availability settings.
3. The authorised user selects a date and time they wish to become available or unavailable.
4. The authorised user submits their schedule.
5. The system verifies and checks for existing bookings that may conflict with the inputted hours. If there is conflict, the system alerts the user to either reschedule or cancel the conflicting booking.
6. Once verified, the system saves the availability schedule and displays the available time slots users can view.

### 7. Monitor Attendance & Metrics (Administrative Staff) - Allows the administrative staff to monitor department metrics, no-shows and student attendance.
1. The administrative staff logs into the system.
2. The administrative staff opens up the report and analytics dashboard.
3. The administrative staff selects the reporting parameters of their choosing, such as date range, department or service type.
4. The system would update and fetch the appointment records, the attendance status and the number of no-shows that occurred.
5. The system would then display these as metrics for the administrative staff for reviewing purposes.

### 8. Assign Guest/Contractor Role (Administrative Staff) - Allows the administrative staff to assign the guest/contractor role to external contractors for their booked students.
1. The administrative staff logs into the system.
2. The administrative staff would navigate to the user and role management.
3. The administrative staff selects the external contractor of their choosing to assign the guest/contractor role to.
4. The administrative staff would link that external contractor to their role, along with their booked students.
5. The system would save the role given to the external contractor and restricts their data access only to their booked students.
6. The system sends a confirmation notification to that external contractor.
   
### 9. Sync External Calendars (External Contractor) - Allows the external contractors to synchronise their third-party calendar applications with the system to prevent double-booking.
1. The external contractor logs into the system.
2. The external contractor navigates to their calendar integration settings.
3. The external contractor selects their third-party calendar they are using authorises the connection.
4. The system would then connect to the external calendar and fetches any time slot that is unavailable.
5. The system would block out those time slots and confirms that the synchronisation is currently active.
   
### 10. Manage System Integration (IT/Technician) - Allows the IT/technicians to configure integrations, user authentications and system deployments.
1. The IT/technician logs into the system's administration controls.
2. The IT/technician selects the configuration module, such as deployment settings, API integrations and authentication settings.
3. The IT/technician then updates the required parameters and runs a configuration test.
4. Once tested and verified, the system would update its settings and saves the administrative changes.

## 4. Unknowns/Questions
1. How far in advance do the authorised users have to update or cancel their booked scheduled appointment?
2. Can the student mentor book, update and cancel on behalf of their student or is it only for their own sessions?
3. What are the specific appointment details and student information that are visible for each role (student, student mentor, staff, administrative staff, external contractor) when it comes to viewing the appointment?
4. How are appointments updated or cancelled when it comes to appointments with external contractors, considering they also operate outside college hours?

## 5. Reflection
