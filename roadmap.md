# Roadmap for Matukio Events

> Please note this roadmap is going to be changed quite often and there is no guarantee for it. 

### Matukio 5.2

Already released. 5.2.8 probably is going to be the last release. 

### Matukio 5.3

####Done

* Event list view (Table)
* Category event list view (Table)
* Featured / Top events view
* Extra fee options (as a checkbox!)
* Currency objects (select it per event!)
* Support for Joomla tags! (event)
* New form validator for the booking form
* Revoke dialog and checkbox (like terms, optional)
* Joomla registration / login during event booking
* New event detail template: Academy
* Split dates (e.g. multiple days with breaks etc.)
* Split of date and time (you can have allday events etc.)
* Automatic creation of organizer accounts when used as publisher
* Rewrite of the modern template (improved responsiveness, cleanup, but only minor design changes)
* Migration to SQL Schema
* Update TCPDF + fonts
* Check if email is already registered for guest bookers, if not allowed to book multiple tickets
* Remove plus sign (+) on event detail page
* Better tooltips
* Move event editing to JLayout (easy customizable now)
* Event detail image (for academy template only)
* Migration from settings table to config.xml
* Improved routing! No duplicate event content!
* Updated fullcalendar, improved responsiveness
* Option to have no seat / place limitation (e.g. 99999)
* Payment plugins are now dynamically loaded 
* More Unit- and System-tests
* Replace of Bootstrap Modal (too many issues with templates)
* -> Migrated to responsive friendly magnific popup
* Microdata improvements (SEO!)
* Sharrif (social media with privacy) support
* Pagination for bookings and participants in the frontend
* Improved security (Protection against SQL injections)

####TODO

This is a major release, bringing many new features and improvements.

* New booking header template (as option)
* Improved statistics
* 2 new payment plugins: Sofortüberweisung and IGP
* Multi-Seat discount (linear progression, like X% per additional seat)
* Updated documentation (you are reading it right now)
* Updated videos

Technical changes

* Many other minor changes and improvements 
* More plugin events

Maybe:

* Event Search module (You can already search with Joomla search module)
* Events with a fixed date (open for a fixed date range)
* New template for the event-list
* Some new modules along with it
* An additional Joomla template (like the one on matukio.compojoom.com)
* Save in Google Calendar button in the event-detail page
* Additional tutor objects, separation from organizer
* Override certification email in event
 
### Matukio 5.4

Depends how many features are going to make it into Matukio 5.3, if all above are implemented we are going to skip this version.

* Multi certificate printing
* Share info about event after booking
* Google Calendar export / import (Not sure on the details yet)
* Config settings in config.xml instead of database
* JSON API for Matukio informations (Joomla! webservice has to be ready first)
* Multiple images with a new image uploader (see Hotspots)
* Automatic discount for buying multiple tickets (Not sure on how to integrate this..)
 
If technically possible:

* Search for event custom fields
* Filter for event custom fields
* Filter for tags

### Matukio 6

Big release with some major changes

* Complete new form builder for the booking form (Drag & Drop)
* New Event specific fields (With the form Builder) 
* Field sets for events
* Event planer / calendar for organizers / admins
* Archive options and views
* New improved modules