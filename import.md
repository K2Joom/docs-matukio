# Import (Administrator)

Matukio offers various import interfaces for events.

### CSV file import

You can find the CSV template file in the media/com_matukio/assets folder of your Joomla installation. (There is also a link on the import dialog).

CSV files are pretty straight forward, if you use the template file, you don't have to make any changes to the settings. Just pick the file and click on import. Make sure there are no breaking quotes (") in the text / data you try to import or you need to escape them before.

> Please make sure you are using the same charset for the CSV file as your database. Probably UTF-8!

### ICS file import

You can easily import events from an ICS calendar file (version 2).

The event data is mapped the following way:

* Event title = VEVENT SUMMARY
* Brief description = SUMMARY
* Place = LOCATION
* Description = DESCRIPTION
* Begin = DTSTART
* End = DTEND
* Closing = DTSTART
* Category = Set in the import dialog
* Updated = Current date
* Publishdate = Current date
* Publisher / Organizer = Current user





