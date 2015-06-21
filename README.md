Cookie Consent
==============

The definitive solution to the absurd cookie law that has everything you need and is fast and simple to deploy. Silktide's original cookieconsent v1 had all the features you could have possibly imagined but most of them were discontinued in v2 due to limited adoption. This fork backports v2's responsive and elegant design with fanatical attention to detail while keeping all of v1's customizable options working.

Features
--------

* Fully functional and beautifully designed
* Free and open source
* Developed by actual web designers [with a few refinements added in by an amateur computer freak]
* Has all of the original [cookieconsent](https://github.com/silktide/cookieconsent) features
* Liberally backports [cookieconsent v2](https://github.com/silktide/cookieconsent2)'s responsive and elegant design

Limitations

--------

* Still relies on jQuery as opposed to cc v2
* Doesn't implement cc v2's themeability [woah, new words all the time!]
* Has a bunch of unused vestigial code left over from the original cc
* Wanna fix this stuff? Have at it and go nuts!

Integration
-----------
As the devmasters instruct us to do, refer to the [cc v1 website](http://sitebeam.net/cookieconsent/) for detailed integration documentation and their simple [configuration wizard](http://sitebeam.net/cookieconsent/code/) to actually get it working. In the code you obtain just remember to change these three lines:

`<!-- Begin Cookie Consent plugin by Silktide - http://silktide.com/cookieconsent -->
<link rel="stylesheet" type="text/css" href="http://assets.cookieconsent.silktide.com/current/style.min.css"/>
<script type="text/javascript" src="http://assets.cookieconsent.silktide.com/current/plugin.min.js">`

to:

`<!-- Begin cookieconsent plugin | https://github.com/nikksno/cookieconsent -->
<link rel="stylesheet" type="text/css" href="https://cdn.rawgit.com/nikksno/cookieconsent/master/cookieconsent.css"/>
<script type="text/javascript" src="https://cdn.rawgit.com/nikksno/cookieconsent/master/cookieconsent.js">`

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
