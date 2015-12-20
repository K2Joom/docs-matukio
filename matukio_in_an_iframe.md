# Matukio in an IFrame

In Joomla there is a nice parameter (same as index2.php in Joomla 1.5) for just showing the extension itself.

tmpl=component

For example:

http://matukio.compojoom.com/events?tmpl=component

This removes the whole Template (including modules etc.) and only shows the component.

You can use this to embed Matukio in other websites.

> tmpl=component is only working for a single site, when users click on links, Joomla changes back to the default template.