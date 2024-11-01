=== World Domination ===
Contributors: dartiss, emrikol, tallulahhh
Donate link: https://artiss.blog/donate
Tags: market, coverage, share, w3tech, cms
Requires at least: 4.6
Tested up to: 6.6
Requires PHP: 7.4
Stable tag: 2.2
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Add WordPress market coverage summary to your dashboard.

== Description ==

Adds a summary of the current WordPress market coverage to your dashboard!

Basically screen scraping from the [W3Techs](https://w3techs.com/technologies/details/cm-wordpress/all/all "W3Techs") website (don’t panic W3Techs, I’m caching the data - your website performance is safe!), this will display what percentage of websites (in total or that use CMS) are currently powered by WordPress. There are even shortcodes so that you can this information into your posts as well!

Now you can keep an eye on how close to world (aka internet) domination WordPress is achieving <cue diabolical laughter>.

https://www.youtube.com/watch?v=gY2k8_sSTsE

World Domination is a community plugin that follows both WordPress and WordPress VIP coding standards.

Iconography is courtesy of the very talented [Janki Rathod](https://www.fiverr.com/jankirathore) .

**Please visit the [Github page](https://github.com/dartiss/world-domination "Github") for the latest code development, planned enhancements and known issues**

== Using the shortcodes =

There are two shortcodes `[wp_total_market]` and `[wp_cms_market]`. Simply add these, wherever you wish within a post or page, to display the latest total or CMS market share data. 

== Installation ==

World Domination can be found and installed via the Plugin menu within WordPress administration (Plugins -> Add New). Alternatively, it can be downloaded from WordPress.org and installed manually...

1. Upload the entire `world-domination` folder to your `wp-content/plugins/` directory.
2. Activate the plugin through the 'Plugins' menu in WordPress administration.

Voila! It's ready to go.

== Frequently Asked Questions ==

= Hey! My dashboard figure is different to the one shown on W3Techs =

For performance reasons I cache the dashboard information for one week so, if the market figure changes in the meantime, you will get this discrepancy. If you find this keeps happening, please let me know and I’ll look at refreshing the cache more regularly.

= I don't like the graphic on the dashboard that shows the percentage. Can I switch it off? =

Yes you can! Head to Settings -> General in WP Admin and find the tickbox for this.

= The dashboard graphic keeps changing color! =

One of the parameters to generate the image is a hash - I pass a different one into it based on the current date, so will change daily.

== Screenshots ==

1. Example of it on the dashboard (image not enabled)
2. Example of it on the dashboard (image enabled)
3. Example of how the image toggle setting appears

== Changelog ==

I use semantic versioning, with the first release being 1.0.

= 2.2 =
* Maintenance: A big jump in version numbers, but little to see. A lot of the code has changed, though, hence the release number. Basically, all the code was in one file and it was getting big and cumbersome, so it's been split.
* Enhancement: I took the opportunity to replace some of the code with some that I'm using across all my plugins - a shared resource, which will be kept in-step
* Bug: Fixed a bug that would prevent the dashboard image from displaying
* Bug: Also fixed some a bit more minor, but could throw up the occasional PHP error

= 2.1.3 =
* Enhancement: After updating PHPCS and the sniffs, I've made some further code improvements. Nothing major, don't panic.

= 2.1.2 =
* Maintenance: Nice try W3Techs. You changed the URL and threw in a change of format to try and fox my plugin. Well, I'm onto you. Consider this my explosive reply! In other words, it stopped working - this fixed it.

= 2.1.1 =
* Bug: Some of the setting screen output wasn't being sent for translation. That's now fixed. Thanks to [Alex Lion](https://www.alexclassroom.com/) for highlighting this.

= 2.1 =
* Enhancement: We're now integrating the excellent [wp-somethingty-percent](https://github.com/Automattic/wp-somethingty-percent), which uses Canvas / GD to generate a graphic representation of the WordPress market share

= 2.0.4 =
* Bug: Squashed a pesky bug that meant I wasn't initially defining a variable. Thanks to `emrikol` for pointing this out.
* Bug: I added some new plugin meta in 2.0.2 and it appears it wasn't working. How did I miss that? Please don't tell me...
* Enhancement: If the plugin fails to get the new stats rather than keep using the old one ad-infinitum (and potentially serving up wrong information), after a few days you'll get an error message.
* Enhancement: I tried to make this plugin as robust as possible, but maybe a little too so. If new data can't be retrieved for the market rate, it keeps using the existing, cached, data. Which is great until it goes on for too long. Now, after a week of failure, you'll get an error
* Enhancement: Improved date handling to make you feel better. After all, time is a great healer.
* Maintenance: Detection of WooCommerce. Doesn't do much now but is for a future update. Added it now for, I dunno know, I felt like it :shrug:
* Maintenance: Moved some code around to prepare it for some future updates. Think ahead folks!

= 2.0.3 =
* Bug: Why, in the name of all things holy, did nobody not say that I was incorrectly referring to WordPress being a CRM and not CMS? I'm not angry, just disappointed. It's now fixed, though.

= 2.0.2 =
* Enhancement: Added some shiny, new plugin meta
* Maintenance: You know how it followed WordPress.com coding standards before? Now it's the WordPress VIP coding standards! 

= 2.0.1 =
* Enhancement: Code quality enhancements to bring it in line with WordPress.com VIP coding standards
* Enhancement: Now uses `wp_remote_get` alternative when run on the WordPress.com VIP platform

= 2.0 =
* Enhancement: Total re-write of the caching to ensure that if the data is not available previous information will be re-used (less chance of an error message as a result but, on the down side, may see older data as a result)
* Enhancement: Sides shored up with lots of security additions - escape them all!
* Enhancement: Now I show the CMS percentage on the dashboard and not just the overall one
* Enhancement: Brand new shortcodes so that you can embed this information in a post if that's your bag. Baby.
* Enhancement: Using a time constant for the caching rather than hard-coding long strings of numbers that I'm only likely to type wrong
* Enhancement: The Github links are on me! Now added to all the files and all the meta
* Enhancement: When you hover over the dashboard link to the source it will now show you when the data was last updated
* Enhancement: Added a timeout to the file fetching. Okay, so it's the default (5 seconds) but it's now easier for me to tweak that, if needs be
* Bug: Some of the plugin meta was missing due to the wrong plugin name being used. Oops. Needless to say, it's fixed

= 1.0 =
* Initial release.

== Upgrade Notice ==

= 2.2 =
* Fixed an image display bug whilst also massively overhauling the code layout
