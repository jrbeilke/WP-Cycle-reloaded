=== Plugin Name ===
Contributors: nathanrice, jrbeilke
Donate link: http://example.com/
Tags: slideshow, images, jquery cycle
Requires at least: 3.0.1
Tested up to: 3.4
Stable tag: 4.3
License: GPLv2
License URI: http://www.gnu.org/licenses/gpl-2.0.html

This is a fork of the WP-Cycle plugin with fixes to work with recent versions of WordPress. The WP-Cycle plugin allows you to upload images from your computer, which will then be used to generate a jQuery Cycle Plugin slideshow of the images.

== Description ==

This is a fork of the WP-Cycle plugin with fixes to work with recent versions of WordPress.

The WP-Cycle plugin allows you to upload images from your computer, which will then be used to generate a jQuery Cycle Plugin slideshow of the images.

Each image can also be given a URL which, when the image is active in the slideshow, will be used as an anchor wrapper around the image, turning the image into a link to the URL you specified.  The slideshow is set to pause when the user hovers over the slideshow images, giving them ample time to click the link.

Images can also be deleted via the plugins Administration page.

== Installation ==

1. Upload the entire `wp-cycle-reloaded` folder to the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress
1. Configure the plugin, and upload/edit/delete images via the "WP-Cycle" menu within the "Media" tab
1. Place `<?php wp_cycle(); ?>` in your theme where you want the slideshow to appear
1. Alternatively, you can use the shortcode [wp_cycle] in a post or page to display the slideshow.
1. Once the `wp-cycle-reloaded` plugin has been installed you can safely remove the previous `wp-cycle` plugin

== Frequently Asked Questions ==

= My images won't upload. What should I do? =

The plugin uses built in WordPress functions to handle image uploading. Therefore, you need to have [correct permissions](http://codex.wordpress.org/Changing_File_Permissions "Changing File Permissions") set for your uploads directory.

Also, a file that is not an image, or an image that does not meet the minimum height/width requirements, will not upload. Images larger than the dimensions set in the Settings of this plugin will be scaled down to fit, but images smaller than the dimensions set in the Settings will NOT be scaled up. The upload will fail and you will be asked to try again with another image.

Finally, you need to verify that your upload directory is properly set. Some hosts screw this up, so you'll need to check. Go to "Settings" -> "Miscellaneous" and find the input box labeled "Store uploads in this folder". Unless you are absolutely sure this needs to be something else, this value should be exactly this (without the quotes) "wp-content/uploads". If it says "/wp-content/uploads" then the plugin will not function correctly. No matter what, the value of this field should never start with a slash "/". It expects a path relative to the root of the WordPress installation.

= I'm getting an error message that I don't understand. What should I do? =

If you are experiencing problems, please start a support thread on the wordpress.org plugin page and provide the steps to reproduce the issue.

= How can I style the slideshow further? =

In the settings of the plugin, you're able to set a custom DIV ID for the slideshow. Use that DIV ID to style the slideshow however you want using CSS.

= In what order are the images shown during the slideshow? =

Chronologically, from the time of upload. For instance, the first image you upload will be the first image in the slideshow. The last image will be the last, etc.

= Can I reorder the images? =

No not currently, but this feature may be added in the future.

= Can I rotate anything other than images with this plugin? =

No. This is an image slideshow. Enjoy it for what it is.

= Do you have future plans for this plugin? =

Yes. Here are some potential features that could be added:

* Add ability to reorder the images
* Possibly add widget support so that you can put a slideshow in a widget area

== Screenshots ==

1. This screen shot description corresponds to screenshot-1.(png|jpg|jpeg|gif). Note that the screenshot is taken from
the /assets directory or the directory that contains the stable readme.txt (tags or trunk). Screenshots in the /assets
directory take precedence. For example, `/assets/screenshot-1.png` would win over `/tags/4.3/screenshot-1.png`
(or jpg, jpeg, gif).
2. This is the second screen shot

== Changelog ==

= 0.1 =
* Initial Release

= 0.1.1 =
* Added automatic defaults database insertion
* Added [wp_cycle] shortcode
* Buggy release, ended up reverting to 0.1

= 0.1.2 =
* Unreleased version, used for testing

= 0.1.3 =
* Added stable [wp_cycle] shortcode
* Added transition duration control to settings
* Added transition delay control to settings
* Added new options to the defaults array (for filtering)
* Changed some wording in the settings
* Upgraded jQuery Cycle plugin from 2.63 to 2.65

= 0.1.4 =
* Added empty alt tag to images to pass vaidation

= 0.1.5 =
* Fixed the error that got produced when trying to loop through a non-array variable (duh!)

= 0.1.6 =
* Fixed the shortcode positioning problem

= 0.1.7 =
* Upgraded jQuery Cycle plugin from 2.65 to 2.81

= 0.1.8 =
* Added `position: relative;` to the slideshow div

= 0.1.9 =
* Moved script and args to the `wp_footer` hook

= 0.1.10 =
* Fixed minor bug from 0.1.9

= 0.1.11 =
* Moved WP-Cycle menu location from "Plugins" to "Media"
* Updated the menu registration to comply with new roles methodology.
* Added "Settings" link on plugins page.

= 0.1.12 =
* Updated jQuery Cycle plugin to 2.99

= 0.1.14 =
* Updated jQuery Cycle plugin to 3.0.3
* Fix URL for loading jquery.cycle.js to work with HTTPS and WordPress Multisite

= 0.1.15 =
* Fix wp_cycle conflicts so reloaded plugin can be installed alongside WP-Cycle
