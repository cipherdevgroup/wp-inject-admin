# WP Inject Admin

__Contributors:__ [Robert Neu](https://github.com/robneu)  
__Requires:__ WordPress 4.3  
__Tested up to:__ WordPress 4.3  
__License:__ [MIT](http://wpsitecare.mit-license.org/)  

## Description ##

Sometimes you might run into a situation where you need WordPress admin access to a site but only have sFTP, shell, or some other connection to the filesystem. This class is meant to be dropped into the root of a WordPress installation and loaded from the browser. It's a bit of a hack, but should get the job done in most situations.

When you open up `http://domain.com/wp-inject-admin.php` in your browser, a new user with a random name, email and password will be created and assigned `Admin` privileges. You should then be automatically logged-in with the new user and redirected to `wp-admin`.

This file *should* delete itself after being run once but it may not on some servers due to file permissions problems. You should double check to make sure it's gone once you've injected your new user.

The user created is designed to be temporary. Since you won't know what the auto-generated password is, you won't be able to log in with it again unless you update your password after logging in.

Please be careful with this file. If something terrible happens because of it, don't say I didn't warn you.
