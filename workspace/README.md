PINF Workspace
==============

This directory contains everything needed to maintain this project using the
[PINF toolchain system](http://www.christophdorn.com/Research/#pinf).

To use *PINF* you must have the [PINF JavaScript Loader](https://github.com/pinf/loader-js) 
[installed](https://github.com/pinf/loader-js/blob/master/docs/Setup.md).

INFO: *PINF* currently works only on *UNIX* systems that support [node.js](http://nodejs.org/).


Commands
========

Build Extension
---------------

    commonjs -v --script build ./


Publish Extension
-----------------

    commonjs -v --script publish ./


Testing
-------

Assuming: OSX

Development (Firefox 5+ & Firebug 1.8):

    /pinf/bin/firefox-9/Firefox.app/Contents/MacOS/firefox-bin -no-remote -P firephp-extension-fb_1_8

Development (Firefox 9+ & Firebug 1.9):

    /pinf/bin/firefox-9/Firefox.app/Contents/MacOS/firefox-bin -no-remote -jsconsole -P firephp-extension-fb_1_9

Development (Firefox 11+ & Firebug 1.10):

    /pinf/bin/firefox-11/Firefox.app/Contents/MacOS/firefox-bin -no-remote -jsconsole -P firephp-extension-fb_1_10

Production/Testing (Firefox 9+ & amo):
    
    /pinf/bin/firefox-9/Firefox.app/Contents/MacOS/firefox-bin -no-remote -P firephp-extension-amo

Production (Firefox 9+ & sourcemint):
    
    /pinf/bin/firefox-9/Firefox.app/Contents/MacOS/firefox-bin -no-remote -P firephp-extension-sourcemint


Links
=====

  * http://reference.developercompanion.com/Tools/FirePHPCompanion/Run/Examples/
  * https://addons.mozilla.org/en-US/firefox/pages/appversions/

  
Dev Setup
=========

    ln -s /pinf/workspaces/github.com/firephp/firephp-extension/0/extension /Users/cadorn/Library/Application\ Support/Firefox/Profiles/jaxl5tqh.firephp-extension-fb_1_10/extensions/FirePHPExtension-Build@firephp.org
    ln -s /pinf/workspaces/github.com/firebug/firebug/extension /Users/cadorn/Library/Application\ Support/Firefox/Profiles/jaxl5tqh.firephp-extension-fb_1_10/extensions/firebug@software.joehewitt.com
    ln -s /pinf/workspaces/github.com/firebug/firebug/trace/FBTrace /Users/cadorn/Library/Application\ Support/Firefox/Profiles/jaxl5tqh.firephp-extension-fb_1_10/extensions/fbtrace@getfirebug.com

**user.js**

    user_pref("javascript.options.showInConsole", true);
    user_pref("nglayout.debug.disable_xul_cache", true);
    user_pref("browser.dom.window.dump.enabled",  true);
    user_pref("javascript.options.strict", true);
    user_pref("extensions.logging.enabled", true);
    user_pref("browser.tabs.warnOnClose", false);
