Cookie Consent
==============

Javascript plugin allowing a website to comply with the EU cookie law.

By the way
----------
We've released a new version of this. Check it out: [cookieconsent2](https://github.com/silktide/cookieconsent2)


Features
--------

* Free to use and modify
* Only show to EU visitors
* Opt in once for all sites
* Implied or explicit consent
* Works with [do not track](http://donottrack.us/)

Integration
-----------
Refer to the [Cookie Consent website](http://sitebeam.net/cookieconsent/) for detailed integration documentation and
 our simple [configuration wizard](http://sitebeam.net/cookieconsent/code/) to see what can be customized.

Basic usage
-----------

    <link rel="stylesheet" type="text/css" href="cookieconsent.css"/>
    <script type="text/javascript" src="cookieconsent.js"></script>

    <script type="text/javascript">
    // <![CDATA[
    cc.initialise({
    	cookies: {
    		social: {},
    		analytics: {},
    		advertising: {},
    		necessary: {}
    	},
    	settings: {
    		consenttype: "implicit"
    	}
    });
    // ]]>
    </script>

Credits
-------
Created by [Silktide](http://silktide.com).
