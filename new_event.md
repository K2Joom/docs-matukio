# Create a new Event

Event Management -> Events

> You need to create a category first!

Just click on "New" in the events overview. After this the event creation form will show up (It is the same for editing).

![](event-new.jpg)

The event creation form can be a bit complex at the beginning as there are a lot of options and settings. But you only need to complete the first page (Fields marked with an Asterisk *) to create an event. Everything else is optional.

The form is divided into 6 different tabs.

## Basic Tab

### Begin, end and closing date

Please insert the dates in the following date format (or just use the calendar):

YYYY-MM-DD HH:MM:SS

2016-01-31 15:01:10

This is the default ISO format of dates and used in all Matukio forms. In the Joomla frontend it is formatted based on your settings in the Matukio configuration.

### Brief description

This one is used for the event-list overview, upcoming events view etc (and for the event detail page if you don't supply a detailed description).

Please be careful with the HTML you use in there as it may break the layout. And you should generally not use more then some lines of text here.

### Location

You can either set an existing location here (if you have created any) or insert a custom location. If you create a webinar you can skip this or insert an URL here.

### Organizer

This is the Joomla user who is going to manage the event and bookings (if he has the required ACL rights for that - core.edit.own / core.create). 

Users can manage their events in the frontend and backend of Joomla!

This user also receives a copy of the booking confirmation emails and gets the contact requests for the event etc.

You can also create nice detail / information pages for organizers.

### Recurring event generator

If you want to set up an recurring event just set the option to "Yes". After this a date generator will show up.

> Please note: If you change the recurring settings of an existing event, all old dates are going to be deleted and are newly generated. Use this option with care! You can edit every date and / or set up new ones in the Dates View.

In it you can select repeating types, the count of dates or how long the dates should be repeated.

After you have set up your recurring settings click on generate. After this a list of dates will show up. You can also edit them manually following the default date scheme: YYYY-MM-DD. Just click on the little x to remove a date.

The span between begin and end of an recurring event is depending on the time between the main begin and end setting of the event itself. The same goes for the closing date. The above begin and end will always represent the first date.

> Please note: You shouldn't generate more then 80-100 dates at once and you can always create new dates later.

### Max. Participants

Set the maximum number for participants for this event. After this number is reached you have to options:

Either end the booking process for the event

OR

Allow booking on the wait-list (Payment processing is disabled for this, so no one gets charged for this).

#### Min. Participants

This is used for the Auto confirmation cronjob in Matukio. If you set this to a certain amount and this is not reached X days before an event it is going to be automatically cancelled.

If you don't want to use this cronjob you can just ignore this setting.

#### Max. participants per booking

Set how many seats / places can be reserved with a single booking.

> Tip: You can set this to zero if you want to disable online booking for this event.

## Additional Tab

In the additional section you complement the basic ones. You most probably want to fill some of them too, but they are not required for creating an event.

#### Detailed description

The detailed description is shown on the event detail page. You can extensively present your event here. Use any HTML, Plugins, Images etc. here you like!

You can also show text only to certain users. For example:

[sem_paid]Your Text[/sem_paid]

"Your text" then will only be shown to logged in participants, who already paid their event fees.

#### Image for the event overview

This image is only used in the event-list overview and on the upcoming events view. It should not be larger then 600px and is going to fit best if its in portrait format.

If you want to have an image in the event detail page just use the detailed description for that. (Here you want to have probably a landscape format image)

#### Google Maps location (only for custom locations)

If you use a custom location you can supply a Google Maps address here. This one is not displayed directly!

#### Fees

Set the normal / default event fees here. All fees in Matukio should include taxes (there is also a setting to show the net value, but you always insert them with taxes).


