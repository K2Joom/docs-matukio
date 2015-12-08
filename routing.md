# Routing in Matukio Events

Search engine friendly URLs are a complex topic in Joomla. Matukio Events offers full support for them.

In order for the routing to work properly you need a Joomla menu entry to the Matukio event-list, which is later used as base address. This menu entry can also be on a hidden menu. The alias defines the base path of all further Matukio urls.

#####Example:

mydomain.com/events

This is the base URL of Matukio. "events" is the Alias of the menu entry for the mandatory event-list.

If you now visit an single event or any other view (from anywhere not even from the event-list, but also from modules, search, plugins etc.) the URL will always begin with events.

mydomain.com/events/event/0/81-science/210-rocket-science

or


mydomain.com/events/organizer/2-yves-hoppe


