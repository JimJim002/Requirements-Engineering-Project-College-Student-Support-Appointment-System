# Week 3 - Requirements Analysis & Specification

## 1. Information from Week 2
### (i) Stakeholders
1. Students
2. Staff
3. Administrative Staff
4. IT/Technicians
5. External Contractors
6. Student Mentors

### (ii) Needs & Concerns
#### 1. Students
##### Need
Students may want to be able to book an appointment easily with no complications or hassle.
##### Concern
Students fear that they may end up booking the wrong appointment for the service they require, wasting resource and time.

#### 2. Staff
##### Need
Staff may need custom schedules and be able to set automatic boundaries using the online dashboards.
##### Concern
Staff may be overloaded with the workload when reviewing and accepting booking requests by students or may face issues with double-booked appointments made.

#### 3. Administrative Staff
##### Need
The admins may need to monitor student attendance and audit operational data across all support departments.
##### Concern
The admins may waste time and resource if no-shows occur and the system lacks automatic reminders or a defined penalty system.

#### 4. IT/Technicians
##### Need
IT/Technicians may need to be able to seamlessly integrate a scheduling platform with the college's existing user authentication and to maintain data privacy standards.
##### Concern
IT/Technicians may fear the risks of data breach or leaks if specific department viewing permissions are not enforced and automatically timed out.

#### 5. External Contractors
##### Need
External contractors may need to synchronize to the new system with their third-party personal/professional calendar without needing to rely on the college's internal networks.
##### Concern
External contractors may become double booked or restricted from accessing their schedules due to the college's IT authentication barrier.

#### 6. Student Mentors
##### Need
Student mentors may want the ability to update their weekly hours to suit them in regards to when they are available or not (due to lectures and practicals).
##### Concern
Student mentors may become frustrated if they miss out on lectures or practicals if double-booking remains an issue.

### (iii) Unknowns & Information Sources
1. What are the consequences/penalties students may face if no-shows occurred for booked appointments? Who could answer? Staff & Administrative Staff
2. What specific information is required when booking and requesting for appointments? Who could answer? IT/Technicians
3. What third-party calendar application is utilised by external contractors? Who could answer? External Contractors
4. What are the synchronization requirements for these third-party calendar applications? Who could answer? IT/Technicians

### (iv) Elicitation Questions
1. Are there any consequences/penalties students may face for no-shows occurred for booked appointments, and if so, who is responsible enforcing it?
2. What other issues, other than the workload, do staff face when no-shows for booked appointments or double-booking occurs?
3. What is the current process do students use for booking and requesting for an appointment and how do students verify that request/booking?
4. How far in advance can a student book, reschedule or cancel an appointment and what happens if a last minute cancellation occurs?
5. What information is required by the students when booking for an appointment, and which details are visible to other stakeholders like the staff and student mentors?

## 2. Candidate Requirements
1. The system shall allow students to be able to filter out any available appointments based on service type and the specific staff member and student mentor.
2. The system shall provide automatic notifications and emails to students upon successful bookings, updates or cancellations.
3. The system shall allow the support staff members and student mentors to be able to manually cancel and rearrange booked appointments in case of an emergency occurring.
4. The system shall allow administrators to assign a guest/contractor role to external users, restricting data access only to their booked students.

## 3. Requirements Surgery Work
### Candidate Requirement
"The system shall allow administrators to assign a guest/contractor role to external users, restricting data access only to their booked students."
### Sources
1. Students: Provided the need for restricting data access.
2. Administrative Staff: Want to assign the guest/contractor role to external users.
3. IT/Technicians: Wants external authentication for external users so the college system won't be compromised.
4. External Contractors: Wants the basic information of students in order to prepare for the appointments.
### Requirement Type
It's a functional requirement.
### Unclear Information
1. The requirement is vague as it fails to state what specific information of the students external contractors are able to obtain.
2. There's a lack of information of how external contractors are able to log into the college support system.
3. It doesn't state whether or not an expiration for accessibility the external contractor has of the student's information ends.
### Questions for Clarification
1. How does the external contractors log into the system without breaching the college system security?
2. What specific information do the external contractors gain access to in relation to the students?
3. Are there any expiration for the external contractor for gaining access to the specific student's information, and if so, when exactly does it expire?
### Vertification
1. Role Assignment: As an administrator, log onto the system, select an external user account and verify if that user has been successfully assigned a role of the "guest/contractor".
2. Authorised Accessibility (Booked Student): As an external contractor, log into the system, view the student who has booked an appointment with them and verify if the student and the information relating to that student is visible to the external contractor.
3. Authorised Accessibility (Unbooked Student): As an external contractor, log into the system, view the student who has NOT booked an appointment with them and verify if the student and their information is not visible and is blocked to the external contractor.
### Remaining Unknowns
1. Does the student book for the external contractor or is it the administrator who is responsible for assigning the student with an external contractor? 
Who could answer? - Administrative Staff
2. If a student cancels an appointment, does the accessibility of the external contractor to view that student's information gets immediately revoked or does it remain accessible until the cancelled date passes? 
Who could answer? - Administrative Staff & IT/Technicians

## 4. Functional Requirements
### FR-01 "The system shall allow an authorised user to view appointment availability for a selected date."
1. WHO? The authorised user (students, staff, & student mentors) needs this requirement.
2. WHAT? To be able to view information about the available appointment slots.
3. WHEN? Information will be revealed when the selected date is inputted into the system.
4. WHY? To verify if an appointment is available before confirming a user's booking for that appointment.
5. HOW? To verify, the system should display the appointment availability for that specific day when the user books an appointment and selects a date.

### FR-02 "The system shall prevent a user from booking a selected appointment again or an appointment that is unavailable for the selected dates."
1. WHO? The authorised user (students, staff, & student mentors) and the system needs this requirement.
2. WHAT? To be able to prevent and block user bookings from being recorded and saved.
3. WHEN? When the selected appointment has already been booked or is unavailable.
4. WHY? To prevent the case of double bookings and misleading users into believing the selected appointment is "available" at the selected dates.
5. HOW? To verify, the system should check whether the selected appointment is available or not, and if it's not, block the user, save nothing, and leave an error message to state the selected appointment has already been booked or is unavailable.

### FR-03 "The system shall require the user to input an expected appointment date before a new booking can be successfully saved."
1. WHO? The authorised user (students, staff, & student mentors), the technician, and the system needs this requirement.
2. WHAT? To require an input of an expected booking date.
3. WHEN? Before a new booking for an appointment can be successfully saved into the database.
4. WHY? To make sure that technicians always know exactly when a booking has been made, so it can prevent the chances of double-booking from occurring.
5. HOW? To verify, the system should block the new booking from being saved if the user attempts to save their booking without an appointment date inputted, where the system should then give a notification to the user to input an expected appointment date.

### FR-04 "The system shall allow an authorised user to book an available appointment slot for a selected date and sends a confirmation notification."
1. WHO? The authorised user (students, staff, & student mentors) needs this requirement.
2. WHAT? To be able to select an open appointment slot, to confirm and save booking details within the system.
3. WHEN? When the user has applied a selected valid date, viewed the available slots and submitted their booking request.
4. WHY? To be able to secure the user's appointment so that the system could update that the appointment slot has been booked.
5. HOW? To verify, the system should accept a booking once an authorised user logs in, selects an available date and time, and submits the booking, where the system can then save it and update itself into stating that the available date and time has been booked, and finally sending a confirmation notification to the user saying they have booked their appointment successfully.

## 5. Quality Requirements
### NFR-01 "The system shall display equipment availability search results within 2 to 3 seconds of a user submitting their request."
1. WHO? The system and the staff could need this when the system is interacting with the user (students, & student mentors).
2. WHAT? To display the appointment availability in real time.
3. WHEN? Within 2 to 3 seconds of the user submitting their requests.
4. WHY? To ensure that the system is fast, efficient and responsive so that the staff can quickly confirm the details for the user.
5. HOW? To verify, use an online or a physical stopwatch to measure the time it takes for the system to get the search results once the user presses the submission button/input to submit their request, and record and check the consistency of the time each test (between 2 to 3 seconds).

## 6. Project Application

## 7. Reflection
