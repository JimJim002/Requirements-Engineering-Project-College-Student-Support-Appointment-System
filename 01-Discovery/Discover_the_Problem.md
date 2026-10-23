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
1. Staff may have the ability to set boundaries for their calenders, defining set work hours, breaks, and holidays where any bookings made at those hours are not accepted and are blocked.
2. All the students and staff may have access to devices other than phones, such as tablets or laptops.
3. The college may have an authentication system already implemented for verifying students.
4. The duration of the appointments may be varied around 30 to 60 minutes based on the service type, where they can't be scheduled on an open-ended basis.

## 3. Unknowns
1. Are there any external calender platforms being used by staff that may need backend synchronisation?
2. What are the penalties for students who repeatedly fails to attend their scheduled booked appointments?
3. How does the system route what support service a student who is unsure may require?
4. Do staff require buffer time between appointments to write down notes and be prepared before the beginning of the next appointment?
5. Do the system need to accommodate group sessions, or is it strictly limited to one-on-one appointments?

## 4. Stakeholders 
### 1. Students
They are the primary users who need to be able to view any available booking hours, select the services they need and to book appointments.
### 2. Staff
They are users for the system for needing to manage appointments for the bookings and for needing to review the student appointment data.
### 3. Administrative Staff
They are responsible for overseeing the operations by the department, to monitor the attendance and to audit system metrics.
### 4. IT/Technicians
They are responsible for the deployment of the system, the integration of the platform, and the user authentication.

### Challenges
1. If a student fails to attend their booked appointment, this leads to staff wasting their time and resource and may prevent the student from getting help.
2. Students may end up booking the wrong services, leading to wasted appointments.
3. Some staff may prefer what they are currently doing, which may create some conflicts in the bookings.

## 5. Goals
1. To provide a complete transparency of when appointmens are available to reduce confusion and waiting times for the students.
2. To minimize manual appointments by staff by transitioning from spreadsheets and emails to automated scheduling, while also keeping the manual method for those who wish to still use it.
3. To prevent the possibility of double booking by automating the calenders synchronisation.
4. Student privacy must be protected by restricting data access by using department-specific viewing permissions.

## 6. Scope
### In-Scope
1. Students should have the option to be able to manage, update or cancel their own bookings easily (self-service booking).
2. The system should send automatic notifications, alerts and reminders.
3. Staff should have the ability to add and modify their custom schedules through online dashboards.
4. The system should contain a real time tracking feature that tracks when exactly an available appointment has been made, updated, or cancelled.
### Out of Scope
1. The system will only facilitate just direct student-to-staff communication and excluding student-to-student communication.
2. The system will not track any grades, GPAs, or assignments submissions.
3. The system will not handle any transactions, payments or budgets of paid services, as all student support services should be covered by the standard student tuition.

## 7. Candidate Requirements 
### Functional Requirements
1. The system shall allow students to be able to filter out any available appointments based on service type and the specific staff member.
2. The system shall provide automatic notifications and emails to students upon successful bookings, updates or cancellations.
3. The system shall allow the support staff members to be able to manually cancel and rearrange booked appointments in case of an emergency occurring.
### Non-Functional Requirements
1. The system should load the online dashboard and the availability screens in a response time between 2 to 3 seconds under normal network conditions.
2. The system should be fully functional and visually consistent on all major Web browsers, like Google Chrome, Mozilla Firefox, and Microsoft Edge.
3. The system should log out after 20 minutes of inactivity to secure student information.

## 8. Requirement Surgery
### R1 - "Information about students and appointments must be appropriately protected."
1. Issue: This requirement is too vague as it doesn't define what "appropriately protected" means. Is it something to do with hiding information, and from who?
2. Rewrite: "The system shall allow the support staff member to see only the information of the students that are booked with them - they should not be allowed to view information of students using other departments."
### R2 - "Accessibility and ease of use need to be considered."
1. Issue: This requirement is too vague as "ease of use" can be subjective as every user have their own level they consider as easy, which may not be the case for others.
2. Rewrite: "The system shall work perfectly under the standard keyboard controls and provide screen readers so that students with visual impairment can book appointments without any assistance."

## 9. Reflection

Upon the completion of the Discovery phase, it's clear that there may be some conflicts between students (for flexibility) and the shop (for profitability). While students may prefer zero risk when making purchases on the system, the shop can't afford to hold dead stock. The system may need a compromise, such as a mandatory deposit system, or an automated message for collection reminders and deadline reminders.
