# Week 6 - Class Diagram

## 1. Candidate Domain Concepts
### Candidate | Class, Attribute, Association | Supporting Requirements
* Student | Class | FR-01, FR-04, CFR-01
* Appointment | Class | FR-03, FR-04, UC-01
* Expected date | Attribute (of Appointment) | FR-03
* Service type | Attribute (of Appointment) | CFR-01
* Status | Attribute (of Appointment) (candidate) | FR-04, UC-03, UC-04
* TimeSlot | Class | FR-01, FR-02
* Is available | Attribute (of TimeSlot) (candidate) | FR-01, FR-02
* Start time | Attribute (of TimeSlot) (candidate) | FR-01
* End time | Attribute (of TimeSlot) (candidate) | FR-01
* SupportService | Class | CFR-01, Fact 1 (Week 1)
* Service name | Attribute (of SupportService) | CFR-01
* Department | Attribute (of SupportService) | CFR-01
* StaffMember | Class | CFR-01, CFR-03
* StudentMentor | Class | CFR-01, CFR-03
* ExternalContractor | Class | CFR-04
* AdminStaff | Class | CFR-04
* IDs & Email | Attributes (candidate) | Confirmation required
* Books / Reserves / Delivers / Views / Manages availability of / Is for / Assigns role to / Monitors | Associations

## 2. Associations
### Class 1 | Relationship Label | Class 2 | Evidence
* Student | books | Appointment | FR-04, UC-01
* Appointment | reserves | TimeSlot | FR-02, FR-04
* Appointment | is for | SupportService | CFR-01
* StaffMember | delivers | SupportService | CFR-01
* StaffMember | manages availability of | TimeSlot | CFR-03
* StudentMentor | manages availability of | TimeSlot | CFR-03
* ExternalContractor | views | Appointment | CFR-04
* AdminStaff | monitors | Appointment | UC-07
* AdminStaff | assigns role to | ExternalContractor | CFR-04, UC-08

## 3. Multiplicities
### Association | Multiplicity | Justification
* Student - Appointment | 1 to 0..* | FR-04, CFR-02:

Allows a student to book (FR-04), update, cancel (CFR-02) more than one appointments, where each booking belongs to one student.

* Appointment - TimeSlot | 0..1 to 1 | FR-02:

Prevents double-booking, as the appointment reserves only 1 slot and that slot holds at most 1 booking.

* Appointment - SupportService | 0..* to 1 | CFR-01:

A booking is linked to one specific support service, while a service can have many bookings.

* StaffMember - SupportService | 1..* to 1..* | Week 1 Discovery:

It's confirmed that staff members delivers support services across the departments.

* StaffMember - TimeSlot | 0..1 to 0..* | CFR-03 & Week 5 "Set Availability":

Shows that the staff can manage their own availability blocks.

* StudentMentor - TimeSlot | 0..1 to 0..* | CFR-03:

It's confirmed that student mentors can set their own weekly time slots around lectures.

* ExternalContractor - Appointment | 1 to 0..* | CFR-04:

Restricts the external contractors into only being able to view the appointments booked with them.

* AdminStaff - Appointment | 1..* to 0..* | UC-07:

It's been established that the administrators monitors the appointments and the attendance across the departments.

* AdminStaff - ExternalContractor | 1 to 0..* | CFR-04:

It's been stated that the administrators can assign the guest/contractor role to the external contractors.

## 4. Requirements-to-Model-Check
### Requirement | Where is it Represented in the Diagram? | Fully Represented?
* FR-01 | TimeSlot (isAvailable, startTime, endTime) managed by StaffMember or StudentMentor | YES
* FR-02 | Appointment - reserves - TimeSlot | YES
* FR-03 | Attribute, "expectedDate" on Appointment | YES
* FR-04 | Student - books - Appointment - reserves - TimeSlot | Partially
* CFR-01 | Appointment - is for - SupportServices (serviceName, department) | YES
* CFR-03 | StaffMember & StudentMentor - manages availability of - TimeSlot | YES
* CFR-04 | AdminStaff - assigns role to - ExternalContractor - views Appointment | Clarification Required

## 5. Unknowns
1. Do the TimeSlot intervals (startTime and endTime) follow a fixed duration for all services or can it be varied based on the SupportService? Who could answer? Staff & Administrative Staff
2. Do students book directly to the ExternalContractor or does the AdminStaff assigns them one, and what student details are visible for the ExternalContractor to view? Who could answer? Administrative Staff & External Contractors
3. What exact state does the status attribute on Appointment support for attendance monitoring? Who could answer? Administrative Staff

## 6. Assumptions
1. When the ExternalContractor is linked to the Appointment, they could only view the basic information of only their booked students, and being blocked out of viewing unrelated student details.
2. Each TimeSlot belongs to either one StaffMember or one StudentMentor rather than that TimeSlot being shared.

## 7. Modelling Decision
* Unlike the Activity Diagram, the AdminStaff were included as while their associated use cases (7 to 10) were excluded, the role assignment and the appointment monitoring are core structural rules of the domain.
* Meanwhile, IT/Technicians and the NFR-01 was excluded as technical deployments are mainly outside the system's domain.

## 8. Reflection
