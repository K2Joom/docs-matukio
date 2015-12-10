****# Booking fields (Administrator)

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

### Page

The booking form has one (as a setting) to four pages. If it is an paid event and you enabled payment processing it has four pages.

First page is for participants information, like first name or the address. 

The second page is for payment settings (if any)

The third page is the confirmation page and where the terms and conditions, captcha etc. are displayed.

The fourth page is for payment processing. E.g. you are redirected to PayPal or 2Checkout, leave your bank details or see instructions on how to pay. (Depending on available payment plugins and the users payment choice on the second page).

> If you disable payment processing or disable all payment plugins the second and last page will not show up, but you can use fees.

Only fields on the first page of the booking form are validated with JavaScript (all fields are validated in PHP).

The third page is mostly a confirmation page showing all user entries. 

> PLEASE NOTE: The first and third page are always shown (and named like that), only the second page can be hidden (if no payment is done)! In most cases you want your new booking field to be on page one.

### Type

The following field types are available for an booking field:

* Text (A simple one line text field for user inputs- e.g. <input type="text" ..)
* Text area (A multi line text input field)
* Select (A drop-down select list with multiple items where users can select one)
* Radiobuttons (Only one value selectable)
* Checkboxes (Multiple values selectable)
* Spacer (a separator to group your content - similar to a HR HTML element)
* Spacer Text (a separator with your own custom text)

If you use Select, Checkbox or Radiobuttons you need to provide the possible values in the Values field, e.g. which values the user can choose between.

The syntax is pretty straight forward: 

{element1=Text1}{element2=Text2}

The text is displayed to the user and the element used for intern (id, name etc.) naming of the element. The element name is not allowed to have any special characters (including spaces). If you leave the element empty and set required to Yes, the validation fails if not another element is selected. This can be used to show for example "please select" as the first option, forcing users to select an element.

### Preallocation data

Here you can set if the field should be populated by the users details. Currently Matukio supports importing data from the Joomla user profile plugin or Community Builder. 

> If the user is logged in and already made a booking this data is used to pre-allocate the data.

### Ordering

Set the position where the booking field should be displayed. (Counting up from one)

### Custom CSS

It is also possible to add some custom CSS styles directly through the booking fields editor. For example width: 100px; will change the fields width to 100px.


### Per place

Set if this booking field should be filled out per place / seat or just once for the whole booking (only for multiple places).

### Show in Overview

If you want you can show this field as a column in the booking overviews to faster access it details. This can be a very handy feature!

There is also a setting to show it in the (public) participants overview in the frontend.
