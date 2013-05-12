=== Date-based Taxonomy Archives ===
Contributors: ethitter
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=10275434
Tags: archive, taxonomy, taxonomies, date
Requires at least: 3.4
Tested up to: 3.6
Stable tag: 0.3
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Add support for date-based taxonomy archives. Also includes a function for outputting archive links.

== Description ==

Add support for date-based taxonomy archives.

Includes a function for rendering an unordered list of years with months, linked to corresponding date-based taxonomy archive, nested therein.

**This plugin is intended for use by plugin and theme developers. It simply adds support for date-based taxonomy archives, but has no native user interface.**

**Development is over on GitHub: https://github.com/ethitter/Date-based-Taxonomy-Archives/.**

== Installation ==

1. Upload date-based-taxonomy-archives to /wp-content/plugins/.
2. Activate plugin through the WordPress Plugins menu.
3. Go to Settings > Permalinks and click _Save Changes_ to refresh permalinks.

== Frequently Asked Questions ==

= How do I use this plugin? =
Add the function `date_based_taxonomy_archives()` to any template element that appears on a taxonomy archive. The function accepts an array containing the following arguments:

* `taxonomies` - array of taxonomy slugs.
* `show_post_count` - boolean value specifying whether or not to display show counts in parenthesis after archive links.
* `limit` - integer specifying the number of archive links to show. Omit to show all archive links for the specified taxonomy.
* `before` - output to display before archive link.
* `after` - output to display after archive link.
* `echo` - boolean value specifying whether to echo or return archive links.

= What filters does this plugin include? =

* `date_based_taxonomy_archives_args` - applied to arguments passed to `date_based_taxonomy_archives()` at runtime.

== Changelog ==

= 0.3 =
* Remove unnecessary uses of `$wpdb->prepare()` that were incorrectly implemented, resulting in PHP warnings when `WP_DEBUG` was enabled.
* Convert plugin to a singelton pattern instead of relying on a global variable.
* Protect class variables and expose them only through a magic getter. Allows for more flexibility in adding class variables in the future.
* Localize large post counts for display, when requested.
* Correct phpdoc implementation.

= 0.2 =
* Initial public release

== Upgrade Notice ==

= 0.3 =
Maintenance release encouraged for all users. Of note, resolves a PHP warning due to an improper use of `$wpdb->prepare()`.

= 0.2 =
Initial public release
