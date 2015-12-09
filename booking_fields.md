# Booking fields (Administrator)

In Matukio Events there are two types of booking fields:

**Global ones**, which are displayed on every booking form

AND

**Event specific ones**, which are only shown for certain events.

Event specific booking fields are created directly when you edit or create an event.

## Global booking fields

Configuration -> Booking-fields

The booking fields in Matukio are 100% dynamic. This gives you the freedom to completly configure the booking form to your wishes. But this also has some downsides too. Please read through this section before you make any changes.

![](global-booking-fields.jpg)

You can create a new one by just clicking on the "New" button.

> Please don't change the field names for the first name, last name and email address! Else wise Matukio can not allocate names / email addresses any longer.

### Field name

This is the most important setting. This is an **intern** identifier used for this booking field. It has to be unique (also partly having a booking field called test and another one test2 is going to cause problems!)

The field name is also used for the placeholders in the templates (like booking email, ticket etc.). 

MAT_BOOKING_FIELDNAME

For example: if the field name is firstname, the placeholder is MAT_BOOKING_FIRSTNAME.

> You don't need to translate this one! As it is used only internally. No special characters and spaces are allowed.


### Caption / Label / Translationstring

If you don't have a multi-language site you just insert the text you want to display as label here. For an booking field, which asks for the first name, it just would be First name.

If you have a multi-language site, you can also use translation placeholders here. For example create a Joomla language override for COM_MATUKIO_MYFIELDNAME.

See [Joomla! language overrides](https://docs.joomla.org/J3.x:Language_Overrides_in_Joomla) for more informations on this topic.


The following field types are available for an booking field:

* Text (A simple one line text field for user inputs- e.g. <input type="text" ..)
* Text area (A multi line text input field)
* Select (A drop-down select list with multiple items where users can select one)
* Radiobuttons (Only one value selectable)
* Checkboxes (Multiple values selectable)
* Spacer (a separator to group your content - similar to a HR HTML element)
* Spacer Text (a separator with your own custom text)
