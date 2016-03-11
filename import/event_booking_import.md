# Event Booking import
Since Matukio 5.3 you are now able to easily import your event data from the joomla component [Event Booking](http://joomdonation.com/joomla-extensions/events-booking-joomla-events-registration.html). The Event Booking importer is able to import your events, categories, locations, currencies, coupons, templates and bookings. We've tried to mkae the import as straight forward as possible. However due to some differences between Event Booking and Matukio Events we are not able to import everything 1:1. So after you do the import you'll need to check the result and confirm that it meets your expectations. Below you can find some information on how the importer works and what you need to be careful of. 

**IMPORTANT: When you do an import from Event Booking we will first delete all previous Events, Categories, Locations, Currencies, Coupons & Bookings from the Matukio tables. Is this isn't something that you want, then don't use this importer!!!**



***Possible migration issues***

The importer runs in one step. Because of that it's possible for you to run into some issues like a white page during the import. This basically means that error reporting is set to none in your global configuration. To see the exact reason for the white page you'll have to enable error reporting. The most probable causes for errors are listed here:

* Php max_execution_time is set to a small value and the script isn't able to complete in the specified amount of time. Look at your hosting settings and set max_execution_time to a higher value
* PHP runs out of memory - set memory_limit to a higher values

If you encounter any issues with the importer don't hesitate to submit a ticket on compojoom.com.

** As usual always make sure that you have a correct backup before proceeding with the migration!**

## Booking fields mapping
We aren't able to automatically import your Event booking custom fields. You'll have to manually re-create the custom fields in Matukio. Once you've done this before you can perform the import you will need to map your Event Booking fields to the Matukio booking fields. 

## Categories import
We are importing all your Event Booking category and we keep they relations. All meta-description, access levels and published statuses are matched 1:1. Since Matukio doesn't have different Layouts on Category view this information is lost. 

## Locations
All Event Booking locations are imported in Matukio. 

## Coupons
All Event Booking coupons are imported in Matukio with the correct publish_up & publish_down time.

## Currencies
All Event Booking currencies are imported in Matukio. There are some minor issues with the import: 
* In Event Booking the currency sign is not saved in the currency table. Because of that we don't have all the currency signs after import. You'll need to manually edit the currencies and add the correct currency sign. We've only added the currency signs for EUR, USD, GBP & JPY. 
* Event Booking doesn't have information about the currency decimal sign. We've set it to ".". If you need a different currency sign you'll need to edit the imported currency and manually set a different currency sign.

## Templates
Matukio and Event Booking don't have the same templates. 
The following 3 Event Booking templates:

* User Email
* Registration Cancel Email
* Reminder Email

can be matched to Matukio Templates. When we import your data, we will fetch the text of those Templates in Event booking, we will parse any known Event Booking tags and replace them with the matching Matukio tags and update the Matukio templates.

Check the result. It's possible that Event Booking has some tags that we don't support and you'll have to replace them manually.

## Events
We are importing all Event Booking Events in Matukio. Due to the Event structure in Event Booking the imported events can have small differences.

* In Event Booking the event discounts are applied to one or more user groups. In Matukio we apply the events to Joomla access levels. Because of that difference we need to match the Joomla group to a joomla access level. Now 1 group can belong to more than 1 access level. Because of that we might end up with non-expected results. We always get the first access level that we can match. So once you import your results check the different fees and make sure that they are correctly set up.
* If the registration type in Event booking is set to Disable registration, then the event matukio can't be booked.
* If you have group registration in Matukio you can still only register maximum 1 user per event. You'll have to manually edit that event and specify how many tickets users might book at once.
* If you have a Booking mail override in Event Booking this will be transferred to Matukio as well (we will also parse the override text and replace all Event Booking tags with the appropriate Matukio tags)

### Recurring events
Event Booking is treating recurring events slightly different than Matukio. In Event Booking when you are dealing with recurring events, the events are still saved in the main event table. They have a flag set that points to the parent event. Due to this all recurring events in Event Booking are shown when you go to the Event list. 

In Matukio we treat recurring events slightly different. When you are on the Event list view - you only see the parent events. The recurring events are not visible. You can see the recurring events when you go to the Dates view. 

For simplicity purposes we decided to import the recurring events from Event Booking as normal Matukio events. This means that each recurring Event booking event is a single Matukio event. 


## Bookings
The Event Booking bookings import is one of the most complicated part of the migration. For the bookings to be properly migrated you need to make sure that you've properly mapped the Event Booking fields to the Matukio booking fields. 
If you've done this correctly, then we will match the values of your Event Booking fields to the Matukio booking fields values. 

Keep in mind that the payment Methods in Event Booking are different than the payment methods in Matukio. We've matched the os_paypal, os_authnet & os_offline to respectivly paypal, authorizenet and cash paymetn types in Matukio. For all other payment types you would need to manually match them. 