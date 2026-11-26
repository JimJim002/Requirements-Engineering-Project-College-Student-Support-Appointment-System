# Week 5 - Activity Diagram

## 1. Process Modelled
Student's Support Service Appointments - Booking & Management

## 2. Purpose
* A step-by-step process that shows what happens within the system during the core features that can be performed in the system, such as booking, viewing, updating, cancelling appointments and setting availability.
* To show the steps in a more clearer way. 

## 3. Activities
### Logging & Verifying Role
1. Logs into the System: The authorised user logs into the system.
2. Verify User Role & Permissions: The system verifies role and access permission the user has.
3. *Select Action*: The authorised user has the ability to select which action they want to perform. 

### Book Appointment
1. Filter Support Services for Browsing: When the authorised user selects "Book Appointment", they are able to filter out the support services they want to browse based on service type, the specific staff member and specific student mentor.
2. Selects Expected Appointment Date: The authorised then is prompted to enter an expected appointment date they wish to book.
3. *Inputted the Date?*: The system verifies if the available date is inputted. If "NO" it displays an error message telling the authorised user hasn't entered an expected appointment date and loops back to the previous step ("Displays Error Notification" and loops back to STEP 2). If "YES" the system proceeds to the next step (STEP 4).
4. Select Available Time Slot & Submit: The authorised user is then prompted to enter an available time slot before they submit their request to the system.
5. *Available Time Slot?*: The system verifies if the inputted time slot is available for booking. If "NO" it displays an error message telling the authorised user that the time slot is unavailable and loops back to the previous step for the user to enter another available time slot ("Displays Error Notification" and loops back to STEP 4). If "YES" the system proceeds to the next step (STEP 6).
6. Saves the Booking & Locks Booked Slot as Unavailable: Once the system verifies that the time slot is available, it saves the booking, then locks that booking and marks it as unavailable.
7. Sends Confirmation Notification: The system sends a confirmation notification to the user, stating that their booking has been successfully created and saved.

### View Appointment
1. Filters by Date/Service Type/Staff Member or Student Mentor: When the authorised user selects "View Appointment", they are able to filter out their booked appointments based on the date, service type, specific staff member or specific student mentor.
2. Displays Relevant Permitted Appointment Information: The systems verifies the authorised user's role and access permissions and then displays the relevant appointment information based on the role and access permissions.

### Update / Cancel Appointment
1. Select Existing Booking: When the authorised user selects "Update / Cancel Appointment", they can select an existing booking they have already booked.
2. *Update or Cancel?*: The authorised can pick between "UPDATE" for updating their booking or "CANCEL" for cancelling their booking. Any one of these options would led to the outcomes below.
#### "UPDATE" is selected:
* (i) Select New Date & Available Time Slot: When "UPDATE" is selected, the authorised user can select and update a new date and available time slot for their booking.
* (ii) *Is it Available?*: The system verifies if the new date and time slot are available for booking. If "NO" it displays an error message telling the authorised user that the new date or time slot have already been booked is unavailable and loops back for the user to enter another new date and time slot available ("Displays Error Notification" and loops back to STEP (i)). If "YES" the system proceeds to the next step (STEP (iii)).
* (iii) Updates Booking & Frees the Old Slot & Locks New Booked Slot as Unavailable: Once the system verifies that there is a date and time slot available, it saves and updates the booking, frees the old slot and locks the new booked slot and marks it as unavailable.
* (iv) Sends Confirmation Notification: The system sends a confirmation notification to the user, stating that their booking has been successfully updated.
#### "CANCEL" is selected:
* (i) Enter Reason & Confirm the Cancel: When "CANCEL" is selected, the authorised user can enter a reason why they are cancelling their booked appointment and confirm their cancel.
* (ii) Cancels Booking & Frees the Cancelled Slot as Available again: The system would verify the cancellation, removes the cancelled booking and mark the cancelled slot as available again for other authorised user.
* (iii) Sends Confirmation Notification: The system sends a confirmation notification to the user, stating that their booking has been successfully cancelled.

### Set Availability
1. Select Available/Unavailable Hours: When the authorised user selects "Set Availability", they are able to select the hours there are available or unavailable.
2. *Conflicts with Existing Booking?*: The system verifies if the inputted available hours are conflicting with existing bookings. If "YES" the system alerts the user, stating they need to either reschedule or cancel the conflicting booking and loops back for the user to enter a new hours they are available or unavailable ("Alerts for Rescheduling or Cancelling the Conflicting Booking" and loops back to STEP 1). If "NO", the system proceeds to the next step (STEP 3).
3. Saves & Updates Available Slots: Once verified, the system saves and updates the available slots for users to view.
4. Sends Confirmation Notification: The system sends a confirmation notification to the user, stating that their hours have been successfully updated and saved.

## 4. Decision & Guards
### Select Action
* "Book Appointment" - This action allows the authorised user to filter the support services they want to browse before they proceed to create a new booking.
* "View Appointment" - This action allows the authorised user to filter the appointment by date, service type or a specific staff member or student mentor, where the system would then display the relevant appointment information based on the authorised user's role and access permisisons.
* "Update / Cancel Appointment" - This action allows the authorised user to select an existing booking they have before they select whether to update or cancel that existing booking.
* "Set Availability" - This action allows the authorised user to select the hours they are available or unavailable at, where it goes through a check on whether there are other bookings that it may conflict with, before saving and updating the available slots they are available/unavailable for.

### Inputted the Date? (Book Appointment)
* "NO" - The system displays an error message to the authorised user, stating no date was entered, and loops them back to select another expected date.
* "YES" - The system proceeds to the next step where the authorised user must select an available time slot and submit it to the system.
### Available Time Slot? (Book Appointment)
* "NO" - The system displays an error message to the authorised user, stating the time slot is unavailable, and loops them back to select another time slot.
* "YES" - The system proceeds to the next step, where it saves the booking, locks and marks that booking as unavailable and sends a confirmation notification to the authorised user, stating that their booking has been successfully created and saved.

### Update or Cancel? (Update / Cancel Appointment)
* "UPDATE" - The system proceeds to the updating step where the authorised user must select a new date and an available time slot.
* "CANCEL" - The system proceeds to the cancelling step where the authorised user must enter their reason for the cancellation and confirms their cancellation, where the system verifies and cancels the booking, freeing the cancelled slot as being available again. It then sends a confirmation notification to the authorised user, stating their booked appointment has been successfully cancelled.
### Is it Available? (UPDATE - Update / Cancel Appointment)
* "NO" - The system displays an error message to the authorised user, stating that the new date or new time slot is unavailable, and loops them back to select another new date and available time slot.
* "YES" - The system proceeds to the next step, where it updates the booking and frees the old slot and locks the new booked slot as unavailable. It sends a confirmation notification to the authorised user, stating that their booking has been successfully updated and saved.

### Conflicts with Existing Booking? (Set Availability)
* "YES" - The system alerts the authorised user that they need to either reschedule or cancel their conflicting booking.
* "NO" - The system proceeds to the next step, where it saves and updates the available slots they are available/unavailable for. It then sends a confirmation notification to the authorised user, stating that their hours have been successfully updated and saved.
  
## 5. Unknowns

## 6. Stakeholder Question

## 7. Modelling Decision

## 8. Reflection
