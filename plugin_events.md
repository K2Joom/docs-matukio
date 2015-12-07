# Plugin Events

Matukio brings support for Joomla plugins and allows  you to easily inject your code and functions.

See also [Creating a Plugin for Joomla](https://docs.joomla.org/J3.x:Creating_a_Plugin_for_Joomla)

##Booking:

####onValidateBooking ($post, $event, $status)

$post contains the whole Post of the booking form as a reference.

$event the event the booking is for

$status the current validation status (not as reference) -> 0 = fail, 1 = okay, 2 = wait list

If you return an array with an "error" key the validation status changes to failed. The value is used as error message

>Please note for administrators / organizers in the backend all validation rules are turned off

###Event creation: 

###Event presentation:

