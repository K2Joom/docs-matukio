# Plugin Events

Matukio brings support for Joomla plugins and allows  you to easily inject your code and functions.

See also [Creating a Plugin for Joomla](https://docs.joomla.org/J3.x:Creating_a_Plugin_for_Joomla)

##Booking:

####onValidateBooking ($post, $event, $status)

$post contains the whole Post of the booking form as a reference.

$event the event object for which the booking is created.

$status the current validation status (not as reference) -> 0 = fail, 1 = okay, 2 = wait list

If you return an array with an "error" key the validation status changes to failed. The value is used as error message.

>Please note for administrators / organizers in the backend all validation rules are turned off.

####onBeforeSaveBooking ($booking, $event)

$booking contains the current booking object bound to the JTable object, before it is saved. 

$event contains the event object for the booking.

Return values are ignored.

####onAfterBookingSave ($booking, $event)

$booking contains the current booking (JTable object), after it is saved and checked in. 

$event contains the event object for the booking.

Return values are ignored.

###Event creation: 

###Event presentation:

