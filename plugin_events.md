# Plugin Events

Matukio brings support for Joomla plugins and allows  you to easily inject your code and functions.

See also [Creating a Plugin for Joomla](https://docs.joomla.org/J3.x:Creating_a_Plugin_for_Joomla)

##Booking:
(Context = com_matukio.book)

---

#####onValidateBooking ($post, $event, $status)

$post contains the whole Post of the booking form as a reference.

$event the event object for which the booking is created.

$status the current validation status (not as reference) -> 0 = fail, 1 = okay, 2 = wait list

If you return an array with an "error" key the validation status changes to failed. The value is used as error message.

>Please note for administrators / organizers in the backend all validation rules are turned off.


#####onBeforeSaveBooking ($booking, $event)

$booking contains the current booking object bound to the JTable object, before it is saved. 

$event contains the event object for the booking.

Return values are ignored.

---

#####onAfterBookingSave ($booking, $event)

$booking contains the current booking (JTable object), after it is saved and checked in. 

$event contains the event object for the booking.

Return values are ignored.

---

##Event save: 
(Context = com_matukio.event)

---

#####onBeforeSaveEvent ($event, $post)

$event - contains the current (JTable bind) event before saving. Required fields have been already validated.

$post - The complete post of the event form

If you return an array with an "error" key the validation status changes to failed. The value is used as error message.

---

#####onAfterSaveEvent ($event, $isNew)

$event is the saved and checked in event object. 

$isNew is true when this is a newly created event, false when we edit an existing one.

Return values are ignored.

---

##Single event presentation:
(Context = com_matukio.event)

---

#####onContentAfterDisplay ($event, $params)

The result is added after the event informations at the bottom. (See CComment for a sample)

$event - The event object (as reference)

$params - The menu params for this view


---
## Upcoming events
(Context = com_matukio.upcomingevent)

The result is added after the event short description. Called for every event, which is displayed.

$event - The event object (as reference)

$params - The menu params for this view

---
## Featured events
(Context = com_matukio.featured)

The result is added after the event short description. Called for every event, which is displayed.


$event - The event object (as reference)

$params - The menu params for this view

---