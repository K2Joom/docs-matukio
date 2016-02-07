# Roadmap for Matukio Events

> Please note this roadmap is going to be changed quite often and there is no guarantee for it. 

### Matukio 5.2

Already released. 5.2.8 probably is going to be the last version 

### Matukio 5.3

####Done

* Rewrite of the modern template (improved responsiveness, cleanup, but only few design changes)
* Event list view (Table)
* Category event list view (Table)
* New form Validator for the booking form
* Improved routing
* Revoke dialog and checkbox (like terms, optional)
* Joomla registration / login for event registration
* New event detail template: Academy
* Split dates (e.g. multiple days with breaks etc.)
* Split of date and time (you can have allday events etc.)
* Automatic creation of organizer accounts when used as publisher
* Migration to SQL Schema
* Update TCPDF + Check fonts
* Check if email is already registered for guest bookers, if not allowed to book multiple tickets
* Remove + sign on event detail page
* Better tooltips
* Move Eventedit to JLayout
* Event detail image (for academy template only)
* Extra fee options (checkbox) which adds up.

####TODO

This is a major release, bringing many new features and improvements.

* New booking header template (as option)
* Improved statistics
* Option to have no seat / place limitation (e.g. 99999)
* Override certification email in event
* 2 new payment plugins: Sofortüberweisung and IGP
* Multi-Seat discount (linear progression, like X% per additional seat)

Technical changes

* Replace of Bootstrap Modal (too many issues with templates)
* -> Mostly done, migrated to magnific popup
* Many other minor changes and improvements 
* More plugin events

Maybe:

* Event Search module (You can already search with Joomla search module)
* Events with a fixed date (open for a fixed date range)
* Multiple images with a new image uploader (see Hotspots)
* Automatic discount for buying multiple tickets (Not sure on how to integrate this..)
* New template for the event-list
* Search for event custom fields
* Filter for event custom fields
* Featured view for startpages, where you can select your most important events
* Some new modules along with it
* An additional Joomla template (like the one on matukio.compojoom.com)
* Save in Google Calendar button in the event-detail page
* Additional tutor objects, separation from organizer

### Matukio 5.4

Depends how many features are going to make it into Matukio 5.3, if all above are implemented we are going to skip this version.

* Multi certificate printing
* Share info about event after booking
* Google Calendar export / import (Not sure on the details yet)
* Config settings in config.xml instead of database
* JSON API for Matukio informations (Joomla! webservice has to be ready first)
 
### Matukio 6

Big release with some major changes

* Complete new form builder for the booking form (Drag & Drop)
* New Event specific fields (With the form Builder) 
* Field sets for events
* Event planer / calendar for organizers / admins
* Archive options and views
* New improved modules