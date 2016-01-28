# WP Hush
#### Hide donation links and nags for popular WordPress plugins

You love the plugins your use and have donated generously, but don't want your clients to see distracting donation links.

This plugin removes donation links and other nags for popular plugins.

### Example

**Before**  
![](https://dl.dropboxusercontent.com/u/2758854/hush_before.png)

**After**
![](https://dl.dropboxusercontent.com/u/2758854/hush_after.png)

### Supports

* Better WordPress ReCAPTCHA 
* Yoast SEO

### I want plugin X to be supported

* Start by forking the plugin.
* Adding new hiding rules is easy. There are two ways of hiding nags - `add_css_selector($selector)` (added at head, recommended method) or `add_js_selector($selector)` (added on document.ready in footer via `jQuery().hide()`) 
* In the `hush()` function, add the hiding rule at the bottom, for example: `$this->add_css_selector('.obnoxious-nag');`
* If CSS or JS is not enough, add the required code (for example `remove_action()` or `pre_option` filters might be necessary)
* Afterwards, please create a pull request!

### Will this plugin be added to WordPress.org? 

Not planned, but you can use [GitHub Updater](https://github.com/afragen/github-updater) or Composer.
