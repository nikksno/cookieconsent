cookienundrum
==============

The definitive solution to the absurd cookie law that has everything you need and is fast and simple to deploy. Silktide's original cookieconsent v1 had all the features you could have possibly imagined but most of them were discontinued in v2 due to limited adoption. This fork backports v2's responsive and elegant design with fanatical attention to detail while keeping all of v1's customizable options working.

Features
--------

* Fully functional and beautifully designed
* Fun and easy to customize
* Free and open source
* Allows for implicit or explicit consent aquisition from the user and temporarily blocks cookies if needed
* Allows users to opt into cookies for all websites running this script
* Allows you to prevent the banner from showing if the user appears to be outside the EU
* Developed by actual web designers [with a few refinements added in by an amateur computer freak]
* Has all of the original [cookieconsent](https://github.com/silktide/cookieconsent) features
* Liberally backports [cookieconsent v2](https://github.com/silktide/cookieconsent2)'s responsive and elegant design
* Is awesome. Period.

Improvementes over cc v1
--------

* Liberally backports [cookieconsent v2](https://github.com/silktide/cookieconsent2)'s responsive and elegant design
* Implements lucagentile's awesome scrollToConsent functionality [[link to commit](https://github.com/lucagentile/cookieconsent/commit/d494ecd55ece270d9ff9424410f3461949ce6bdc)]
* Fixes the privacyPolicy setting saving it from the limbo it had fallen into in the original code [renamed to cookiePolicy]
* Adds the option to show either the cookiePolicy link or the moreInfo panel link or both
* Adds compatibility with Iubenda's awesome cookie policy solution as an alternative to the standard cookiePolicy link without the need to use their uber-invasive banner that drops down right in front of your site's headings [work in progress]

Limitations
--------

* Still relies on jQuery as opposed to cc v2
* Doesn't implement cc v2's themeability [woah, new words all the time!]
* Has a bunch of unused vestigial code left over from the original cc
* Wanna fix this stuff? Have at it and go nuts!

Keep in mind
--------

All of the changes from the original cc v1 are still being worked on and - as for now at least - it's only me on the project and as you might expect I'm working on it in my spare time. New changes may break the plugin on your site at any time. If you're using it on production websites [like I am] be sure to subscribe to notifications for new pushes to the repo (HowTo here)[https://help.github.com/articles/receiving-email-notifications-for-pushes-to-a-repository/]. If you can contribute to the project in any way please consider doing so: any help is very much appreciated. Thanks!

Live demo
--------

[AnotherMilan](https://anothermilan.net) [themed to the website's colors]

Integration
-----------
As the devmasters instruct us to do, refer to the [cc v1 website](http://sitebeam.net/cookieconsent-v1/) for detailed integration documentation and their simple [configuration wizard](http://sitebeam.net/cookieconsent/code/) to actually get it working. In the code you obtain just remember to change these three lines:

```css
<!-- Begin Cookie Consent plugin by Silktide - http://silktide.com/cookieconsent -->
<link rel="stylesheet" type="text/css" href="http://assets.cookieconsent.silktide.com/current/style.min.css"/>
<script type="text/javascript" src="http://assets.cookieconsent.silktide.com/current/plugin.min.js"></script>
```

to:

```css
<!-- Begin cookienundrum plugin | https://github.com/nikksno/cookienundrum -->
<link rel="stylesheet" type="text/css" href="https://nikksno.github.io/cookienundrum/cookienundrum.css"/>
<script type="text/javascript" src="https://nikksno.github.io/cookienundrum/cookienundrum.js"></script>
```

Full usage
-----------

If you're the rough tough raw code kind of guy or girl and prefer going through tens of lines of code rather than relying on the fast and simple customizer the Master Creators have provided us with [see above], or in case their website goes down [ya never know!] here is the full code for the widget that you should implement in your website [headers already changed to point to this project rather than the original cc v1] with all of the non default options so as to fulfill your picky and control seaking developer attitude. Feel free to remove the lines corresponding to any custom option you don't want and to change the strings used throughout the widget: the function descriptions are followed by the default texts [in brackets] in the string arguments themselves [you're welcome]. Have fun and don't forget to make it your own!

Important! The design changes I've made from the original cc v1 have only been tested by me on the "bottom bar" style [already selected via custom option in the code below]. You're free to try using the "top" [or even better: the "scroll from top" option] but do so at your own risk. Found something that doesn't work with these other styles? Help improve the project either by opening an issue or by fixing it yourself if you're so inclined! Thanks! :)

```html
<!-- Begin cookienundrum plugin | https://github.com/nikksno/cookienundrum -->
<link rel="stylesheet" type="text/css" href="https://nikksno.github.io/cookienundrum/cookienundrum.css"/>
<script type="text/javascript" src="https://nikksno.github.io/cookienundrum/cookienundrum.js"></script>
<script type="text/javascript">
// <![CDATA[
cc.initialise({
	cookies: {
		social: {
			title: 'Social media title',
			description: 'Social media description',
			link: 'Social media link'
		},
		analytics: {
			title: 'Analytics title',
			description: 'Analytics description',
			link: 'Analytics link'
		},
		advertising: {
			title: 'Advertising title',
			description: 'Advertising description',
			link: 'Advertising link'
		},
		necessary: {
			title: 'Strictly necessary title',
			description: 'Strictly necessary description',
			link: 'Strictly necessary link'
		},
		mycookieid: {
			title: 'My custom cookie title',
			description: 'My custom cookie description'
			link: 'My custom cookie link'
		}
	settings: {
		consenttype: "explicit",		// other options: "implicit"
		style: "dark",				// other options: "light"
		bannerPosition: "bottom",		// other options: "top", "push" [not tested with this fork]
		tagPosition: "bottom-right"		// other options: combine "top" and "bottom" with "left" and "right" separated by a dash like in the example
		hideprivacysettingstab: true,
		onlyshowwithineu: true,
		ipinfodbkey: 'IPInfoDB-API-Key',	// optional, only necessary if "onlyshowwithineu" is set to "true"
		refreshOnConsent: true,			
		ignoreDoNotTrack: true,
		disableallsites: true,
		useSSL: true
	},
	strings: {
		socialDefaultTitle: 'Social media title [Social med,ia]',
		socialDefaultDescription: 'Social media description [Face,book, Twitter and other social, websites need to know who you, are to work properly.]',
		analyticsDefaultTitle: 'Analytics title [Analytics]',
		analyticsDefaultDescription: 'Analytics description [We anon,ymously measure your use of th,is website to improve your exp,erience.]',
		advertisingDefaultTitle: 'Advertising title [Advertising,]',
		advertisingDefaultDescription: 'Advertising description [Adver,ts will be chosen for you auto,matically based on your past b,ehaviour and interests.]',
		necessaryDefaultTitle: 'Strictly necessary title [Stri,ctly necessary]',
		necessaryDefaultDescription: 'Strictly necessary [Some cooki,es on this website are strictl,y necessary and cannot be disa,bled.]',
		defaultTitle: 'Default cookie title',
		defaultDescription: 'Default cookie description',
		learnMore: 'Cookie help link text [Learn m,ore]',
		closeWindow: 'Close window text [Close windo,w]',
		notificationTitle: 'Notification title text [Your ,experience on this site will b,e improved by allowing cookies,]',
		notificationTitleImplicit: 'Notification title text for im,plicit consent [We use cookies, to ensure you get the best ex,perience on our website]',
		customCookie: 'Custom cookie title text [This, website uses a custom type of, cookie which needs specific a,pproval]',
		seeDetails: 'See details link [see details]',
		seeDetailsImplicit: 'See details link for implicit ,consent [change your settings]',
		hideDetails: 'Hide details link [hide detail,s]',
		allowCookies: 'Allow cookies button [Allow co,okies]',
		allowCookiesImplicit: 'Allow cookies button for impli,cit consent [Close]',
		allowForAllSites: 'Allow cookies for all sites bu,tton [Allow for all sites]',
		savePreference: 'Save preference button [Save p,reference]',
		saveForAllSites: 'Save preferences for all sites, [Save for all sites]',
		privacySettings: 'Privacy Tag text [Privacy sett,ings]',
		privacySettingsDialogTitleA: 'Privacy dialog title large par,t [Privacy settings]',
		privacySettingsDialogTitleB: 'Privacy dialog title small par,t [for this website]',
		privacySettingsDialogSubtitle: 'Privacy dialog subtitle [Some ,features of this website need ,your consent to remember who y,ou are.]',
		changeForAllSitesLink: 'Change settings for all websit,es link [Change settings for a,ll websites]',
		preferenceUseGlobal: 'Cookie option - Use global set,ting [Use global setting]',
		preferenceConsent: 'Cookie option - I consent [I c,onsent]',
		preferenceDecline: 'Cookie option - I decline [I d,ecline]',
		notUsingCookies: 'No cookies warning [This websi,te does not use any cookies.]',
		allSitesSettingsDialogTitleA: 'Global dialog title large part, [Privacy settings]',
		allSitesSettingsDialogTitleB: 'Global dialog title small part, [for all websites]',
		allSitesSettingsDialogSubtitle: 'Global dialog subtitle [You ma,y consent to these cookies for, all websites that use this pl,ugin.]',
		backToSiteSettings: 'Back to website settings link ,[Back to website settings]',
		preferenceAsk: 'Cookie option - Ask me each ti,me [Ask me each time]',
		preferenceAlways: 'Cookie option - Always allow [,Always allow]',
		preferenceNever: 'Cookie option - Never allow [N,ever allow]'
	}
});
// ]]>
</script>
<!-- End Cookie Consent plugin -->
```

Credits
-------

Original cc v1 by SilkTide
Fork created and maintained by me with virtually all improvements
scrollToConsent functionality and further inspiration by @[lucagentile](https://github.com/lucagentile)
Future features and awesomeness by you! Join us! :)

Poetic inspiration
--------
> Pleasant it is, when over a great sea the winds trouble the waters, to gaze from shore upon another's tribulation: not because any man's troubles are a delectable joy, but because to perceive from what ills you are free yourself is pleasant
> Lucretius, De Rerum Natura
