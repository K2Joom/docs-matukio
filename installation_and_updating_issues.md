# Installation and Updating issues

There are some common issues installing / updating Joomla! extensions. In this chapter we try to help you figuring out how to fix them:

### Maximum execution time

Please make sure that your [maximum execution time](http://php.net/manual/en/info.configuration.php#ini.max-execution-time) is set high enough to process the update execution. On large sites updating Matukio can take more time then the default value.

If it is set too low you receive a timeout error during updates.

### Maximum upload file size

This is can be a tricky one, as there is often no error message showing up. The installation package of Matukio is around 6 MB large. So you should set your **upload_max_filesize** to at least 8M. See [PHP documentation](http://php.net/manual/de/ini.core.php#ini.upload-max-filesize) for more details.

### File Permission issues

> Please note: Changing permissions to 0777 (rwxrwxrwx) is not a solution, it's a security issue!

If you get an error message regarding unwritable directories, inability to move files or other similar messages make sure the directories have correct permissions. In such a case we recommend to install [Admin Tools Professional](https://www.akeebabackup.com/products/admin-tools.html) from Akeeba and run its Fix permissions tool.

If this doesn't help, your site's Webserver to PHP Interface is probably apache2handler. You can check this at the top left of the Joomla! back-end menu: Site > System Information and then the first tab. If this is the case we highly recommend to ask your host to convert it to FcGI or SuPHP or switch host if they don't can/want to do that. Then run the Fix permissions tool of Admin Tools Professional. This will solve all your file/folder permission/ownership issues.

An alternative is to use the FTP layer of Joomla!, but this can be tricky to setup and the previous solution is much better. If you still can't manage to fix it please ask help in the official Joomla!™ forums. If, however, you receive a blank page, an Internal Server Error page or a timeout error message, please proceed to the manual installation section of this documentation.

>Nicholas Dionysopoulos, the developer of Akeeba Backup, wrote excellent articles about file/folder permission/ownership issues. Please read these articles for more information: 777: [The number of the beast and How your web server works](http://magazine.joomla.org/topics/item/353-777-the-number-of-the-beast).
