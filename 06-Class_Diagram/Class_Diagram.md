# Week 6 - Class Diagram

## 1. Candidate Domain Concepts
### Candidate - Class, Attribute, Association - Supporting Requirments
* Student - Class - FR-01, FR-04, CRF-01
* Appointment - Class - FR-03, FR-04, CRF-02
* Expected date - Attribute (of Appointment) - FR-03
* Service type - Attribute (of Appointment) - CFR-01
* Status - Attribute (of Appointment) (candidate) - FR-04, CFR-02, CFR-03
* TimeSlot - Class - FR-01, FR-02
* Is available - Attribute (of TimeSlot) (candidate) - FR-01, FR-02
* Start time - Attribute (of TimeSlot) (candidate) - FR-01
* End time - Attribute (of TimeSlot) (candidate) - FR-01
* SupportService - Class - CFR-01, Fact 1 (Week 1)
* Service name - Attribute (of SupportService) - CFR-01
* Department - Attribute (of SupportService) - CFR-01
* StaffMember - Class - CFR-01, CFR-03
* StudentMentor - Class - CFR-01, CFR-03
* ExternalContractor - Class - CFR-04
* AdminStaff - Class - CFR-04
* IDs & Email - Attributes (candidate) - Confirmation required
* Books / Reserves / Delivers / Views / Manages availability of / Is for / Assigns role to / Monitors - Associations

## 2. Associations
### Class 1 - Relationship Label - Class 2 - Evidence
* Student - books - Appointment - FR-04, CFR-02
* Appointment - reserves - TimeSlot - FR-02, FR-04
* Appointment - is for - SupportService - CFR-01
* StaffMember - delivers - SupportService - CFR-01
* StaffMember - manages availability of - TimeSlot - CFR-03
* StudentMentor - manages availability of - TimeSlot - CFR-03
* ExternalContractor - views - Appointment - CFR-04
* AdminStaff - monitors - Appointment - UC-07
* AdminStaff - assigns role to - ExternalContractor - CFR-04, UC-08

## 3. Multiplicities
### Association - Multiplicity - Justification - What Requires Clarification?
* Student - Appointment - 1 to 0..* - FR-04, CFR-02:
Allows a student to book, update, cancel more than one appointments, where each booking belongs to one student. - Can a group appointment ever involve more than one student? (Unknown 5, Week 1)
* Appointment - TimeSlot - 0..1 to 1 - FR-02:


## 4. Requirements-to-Model-Check

## 4. Unknowns & Assumptions

## 5. Modelling Decision

## 6. Reflection
