<!-- DO NOT EDIT THIS FILE; it is auto-generated from readme.txt -->
# Plugin Dependencies

Plugin dependency management

**Contributors:** [scribu](http://profiles.wordpress.org/scribu)  
**Tags:** [plugin](http://wordpress.org/plugins/tags/plugin), [dependency](http://wordpress.org/plugins/tags/dependency)  
**Requires at least:** 3.1  
**Tested up to:** 3.3  
**Stable tag:** 1.2.1  
**License:** [GPLv2 or later](http://www.gnu.org/licenses/gpl-2.0.html)  

## Description ##

This meta-plugin allows regular plugins to specify other plugins that they depend upon.

Example:

`
/*
Plugin Name: BuddyPress Debug
Depends: BuddyPress, Debug Bar
*/
`

What this does:

* Disables activation of *BuddyPress Debug* until both *BuddyPress* and *Debug Bar* are already activated.
* When either *BuddyPress* or *Debug Bar* are deactivated, *BuddyPress Debug* will also be deactivated.

Links: [Plugin News](http://scribu.net/wordpress/plugin-dependencies) | [Author's Site](http://scribu.net)

[![Build Status](https://travis-ci.org/x-team/wp-plugin-dependencies.png?branch=master)](https://travis-ci.org/x-team/wp-plugin-dependencies)

## Frequently Asked Questions ##

### Error on activation: "Parse error: syntax error, unexpected..." ###
Make sure your host is running PHP 5. The only foolproof way to do this is to add this line to wp-config.php (after the opening `<?php` tag):

`
var_dump(PHP_VERSION);
`

### What happens if a user doesn't have Plugin Dependencies installed? ###
Nothing. The *Depends:* header will simply be ignored.

### Can I have grand-child plugins? ###
Yes, the dependency chain can go as deep as you want.

### Defining virtual packages ###
Say you have some useful functions that you would like to package up as a library plugin:

`
/*
Plugin Name: Facebook Lib
Provides: lib-facebook
*/
`

Now, dependant plugins can specify 'lib-facebook' as a dependency:

`
/*
Plugin Name: Cool Facebook Plugin
Depends: lib-facebook
*/
`

Besides being more robust, the *Provides:* header allows multiple plugins to implement the same set of functionality and be used interchangeably.


## Screenshots ##


## Changelog ##

### 1.2.1 ###
* fixed notices. props cfoellmann

### 1.2 ###
* added ability to use plugin names as dependencies
* [more info](http://scribu.net/wordpress/plugin-dependencies/pd-1-2.html)

### 1.1 ###
* added 'Provides:' header
* replaced 'Dependencies:' with 'Depends:'
* [more info](http://scribu.net/wordpress/plugin-dependencies/pd-1-1.html)

### 1.0.1 ###
* fixed critical bug when not running MultiSite
* better network activation handling

### 1.0 ###
* initial release
* [more info](http://scribu.net/wordpress/plugin-dependencies/pd-1-0.html)


