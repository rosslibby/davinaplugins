=== Naked Social Share ===
Contributors: NoseGraze
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=L2TL7ZBVUMG9C
Tags: social, twitter, facebook, pinterest, stumbleupon, social share
Requires at least: 3.0
Tested up to: 4.4
Stable tag: trunk
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Simple, unstyled social share icons for theme designers.

== Description ==

Naked Social Share allows you to insert plain, unstyled social share buttons for Twitter, Facebook, Pinterest, StumbleUpon, and Google+ after each post. The icons come with no styling, so that you -- the designer -- can style the buttons to match your theme.

There are a few simple options in the settings panel:

* Load default styles - This includes a simple stylesheet that applies a few bare minimum styles to the buttons.
* Load Font Awesome - Naked Social Share uses Font Awesome for the social share icons.
* Disable JavaScript - There is a small amount of JavaScript used to make the buttons open in a new popup window when clicked.
* Automatically add buttons - You can opt to automatically add the social icons below blog posts or pages.
* Twitter handle - Add your Twitter handle to include a "via @YourHandle" message in the Tweet.
* Social media sites - Change the order the buttons appear in and disable any you don't want.

If you want to display the icons manually in your theme, do so by placing this code inside your theme file where you want the icons to appear:

`<?php naked_social_share_buttons(); ?>`

== Installation ==

1. Upload `naked-social-share` to the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress
1. Adjust the settings in Settings -> Naked Social Share
1. If you want to display the buttons manually in your theme somewhere, insert this into your theme file where you want the buttons to appear: `<?php naked_social_share_buttons(); ?>`

== Frequently Asked Questions ==

= How can I add the icons to my theme manually? =

Open up your theme file (for example, `single.php`) and place this code exactly where you want the icons to appear: `<?php naked_social_share_buttons(); ?>`

= Why aren't my share counters updating? =

The share counters are cached for 3 hours to improve loading times and to avoid making API calls on every single page load.

== Screenshots ==

1. The view of the settings panel.
2. A screenshot of the social share icons automatically added to the Twenty Fifteen theme. This also shows the default button styles applied.

== Changelog ==

= 1.2.5 =
* Removed the share counter (just the number - not the button) for Twitter due to their API changes. The number is only removed if the share count is 0, which it will be for all new blog posts. (I'm doing my best to preserve previous numbers from before the API change.)

= 1.2.4 =
* Added filters for the share text for each social media site so the text can be modified in other plugins/themes. For example, the Twitter filter is: naked_social_share_twitter_text. Each filter takes two parameters: the share text and the post object.

= 1.2.3 =
* Fixed a glitch with the Pinterest share button where it wasn't picking up the featured image.

= 1.2.2 =
* Added German translation. Thanks to jackennils
* Changed cache time to 3 hours, as advertised. It was set to only 2 hours for some reason.

= 1.2.1 =
* Tested with WordPress version 4.3.
* Minor coding tweaks to the settings panel.

= 1.2.0 =
* Added LinkedIn button.
* Tested with WordPress version 4.2.4.
* New option to disable share counts.
* Code tweaks to properly implement upgrade routines and version number logging.

= 1.1.3 =
* Fixed an incorrectly spelled slug.
* Updated the settings panel (no visual changes).
* Tested with WordPress version 4.2.3

= 1.1.2 =
* Added more class names to the buttons so you can target the site name (text) and the counter numbers separately.

= 1.1.1 =
* Changed the method used to retrieve the Facebook share count.

= 1.1.0 =
* Settings Panel: You can now change the display order of the social media sites and disable the ones you don't want.
* Settings Panel: Google+ button option is now available.
* Buttons: Fixed a problem with ampersands displaying as their HTML entities when sharing a post (specifically Twitter). Titles are now run through html_entity_decode()
* Updated readme.txt

= 1.0.5 =
* Made some code adjustments to the Naked_Social_Share_Buttons class so you can fetch the buttons for any post object.

= 1.0.4 =
* Fixed a problem with the caching not working properly.

= 1.0.3 =
* Fixed an undefined property notice when the post is not submitted to StumbleUpon.
* Added class names to each social button's `li` tag in case you want to style them differently.
* Tested with WordPress 4.2.

= 1.0.2 =
* Replaced `urlencode` functions with `esc_url_raw`, as urlencode was preventing the social share requests from working properly.

= 1.0.1 =
* Removed some debugging code that was left behind.

= 1.0.0 =
* Initial release.

== Upgrade Notice ==

= 1.2.4 =
Removed Twitter share counter (just the number) for new posts, as it's no longer supported by Twitter.