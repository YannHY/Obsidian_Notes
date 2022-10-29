## Mac

[Automation app Keyboard Maestro 10 gains favorite actions and more | iMore](https://www.imore.com/automation-app-keyboard-maestro-10-brings-favorite-actions-and-more?utm_source=im_tw&utm_medium=tw_card&utm_content=79638&utm_campaign=social)

[Keyboard Maestro 10.2: Work Faster with Macros for macOS](https://www.keyboardmaestro.com/main/)

## iOS
### Twitter

<iframe border=0 frameborder=0 height=1200 width=500   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1251800439730974720?s=21"></iframe>


Voir 

- [ ] [Makerpad Tutorial - Connecting Airtable and Twitter for an automated tweet email newsletter](https://www.makerpad.co/tutorial/connecting-airtable-and-twitter-with-zapier-for-an-automated-tweet-email-newsletter)
- [ ] [Twitter Automation: Scheduled Tweets From Google Sheets • Helge Klein](https://helgeklein.com/blog/twitter-automation-scheduled-tweets-from-google-sheets/)

### Drafts
- [Automating iOS: A Comprehensive Guide to URL Schemes and Drafts Actions](https://www.macstories.net/tutorials/guide-url-scheme-ios-drafts/)

> iOS apps are sandboxed, meaning they are only allowed to interact with the operating system (and other apps) in very limited ways. One of these ways has always been through URL actions. This is how opening a link in any app can automatically move you over to Safari with the corresponding webpage open, or tapping an address can take you into Maps with a pin on the specified location. Safari and Maps both have URL schemes which support this type of communication. Third-party developers have managed to take advantage of this small opening through which apps can “talk” to each other to make incredible things possible by giving their apps powerful URL Schemes.
> [...]
> The x-callback-url is a specification created by [Greg Pierce](https://twitter.com/agiletortoise). Pierce, not by conincidence, is also the developer of Drafts. x-callback-url is something that developers can freely implement into the built-in URL schemes of their apps to allow them to send a “success” parameter after completing a certain action. It is very similar to an “if, then” statement in other programming languages. When you run an action for an app that supports x-callback-url, you can tell the app to run a second action once the first action has been completed. This is by far the most important aspect of iOS automation. Without x-callback-url, advanced iOS automation would be impossible.
> Going back to the Drafts URL scheme, it’s very important not to forget to add “x-callback-url/” to the end of the top level Drafts URL. The beginning of any Drafts action you ever build should be `drafts://x-callback-url/`.
> [...]
> 
> - `drafts://x-callback-url/create?text=Hello%20World&action=Tweet%3A%20the_axx&x-success=`. Our action is now doing six tasks:
> - `drafts://` tells iOS to open Drafts.
> - `x-callback-url/` tells Drafts to enable its built in x-callback parameters. (We’ll get to those later.)
> - `create?` Tells Drafts to create a new draft.
> - `text=Hello%20World` tells Drafts to populate that new draft with the words “Hello World”.
> - `&action="Tweet%3A%20the_axx` runs the built-in “Tweet: the_axx” action and posts “Hello World” to my Twitter account.
> - `&x-success=` tells Drafts that once it successfully tweets “Hello World”, it will then perform another action.

- [Choosing Your Markdown Editor: A Comparison of Ulysses and Drafts](https://www.macstories.net/stories/choosing-your-markdown-editor-a-comparison-of-ulysses-and-drafts/)
- [Drafts 5: The MacStories Review](https://www.macstories.net/reviews/drafts-5-the-macstories-review/)
- [Sending Mail with Drafts](https://forums.getdrafts.com/t/sending-mail-with-drafts/3597)

<hr />

## URL Schemes
- [Always-Updated List of iOS App URL Scheme Names](https://ios.gadgethacks.com/news/always-updated-list-ios-app-url-scheme-names-0184033/)
- [Posts tagged with "URL Scheme"](https://www.macstories.net/tag/url-scheme/page/4/)

### Launcher
- [Launcher](https://www.cromulentlabs.com/launcher.html)

### Launch center pro
- [Launch Center Pro 2.3.1 for Power Users](https://www.macstories.net/tutorials/launch-center-pro-2-3-1-for-power-users/)
- [Hands on: Do more, faster on your iPad or iPhone with Launch Center Pro 2.9](https://appleinsider.com/articles/18/03/17/hands-on-do-more-faster-on-your-ipad-or-iphone-with-launch-center-pro-29)
- [Automating iOS: A Comprehensive and Updated Guide to Launch Center Pro](https://www.macstories.net/tutorials/launch-center-pro-guide/)
- [Launch Center Pro adds NFC Triggers, Siri Shortcuts integration, ‘True Black’ theme, more](https://9to5mac.com/2018/12/18/launch-center-pro-for-ios-nfc-more/)

<iframe border=0 frameborder=0 height=1150 width=600   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1055745946716422144?s=21"></iframe>

- [Launch Center Pro 3.0 Review: Universal Version, New Business Model, NFC Triggers, and More](https://www.macstories.net/reviews/launch-center-pro-3-0-review-universal-version-new-business-model-nfc-triggers-and-more/)

> On iOS, Apple has implemented a method of security known as “sandboxing”. Each and every iOS app lives in its own “sandboxed” environment. Apps cannot reach outside of their sandboxes and into others to send or receive information from one another.
> [...]
> There are two official ways for iOS apps to communicate with each other: the “Open In” menu, and URL schemes.
> [...]
> URL schemes are foundations that can be built into apps which allow the app to be launched, and often various functions within it to be triggered, automatically via URLs. These URLs look very similar to the standard URLs which everyone who has used a web browser understands, except they start with an app name instead of “http”. So instead of launching a website by typing “http://” into your browser, you could launch, say, Drafts by typing “drafts://” into the browser.
> [...]
> For the actions x-callback-url is supported in, simply add `x-callback-url/`between `launch://` and the chosen path. So if you were going to use x-callback-url to chain a second action to an in-app messaging action, your URL would start like this:

`launch://x-callback-url/messaging`

- `launch://messaging?to=555-555-5555&body={{This is a sample action.}}`
- `launch://email?to={{sample@contrast.co}}&subject=Sample&body={{This is just a sample. To learn more about creating actions, go to settings and view the support page.}}`
- `reddit://reddit.com/r/[list|ipad|ipadpro|workflow|launchcenterpro|kindle]` 
- `drafts4://x-callback-url/create?text=[prompt:Text]`
- `iawriter://x-callback-url/open?path={{/Lycée/Première/Le Rouge et le Noir/Dissertation.txt}}&edit=true`
- `iawriter://x-callback-url/quick-search?`
- `spotify:user:yann_10:playlist:03xA0EKQ8eeK8lQmpRnsSH`
- `readdle-spark://compose?subject=[prompt:Subject]`

#### Prompt List Delimiters
Prior to 2.3.1, `[prompt-list]` converted all line breaks to commas when dismissed. In 2.3.1, commas will be inserted as soon as you tap return.

Additionally, you can now set any alternate delimiter value:

- `[prompt-list(+)]`
- `[prompt-list(, )]`
- `[prompt-list( – )]`
- `[prompt-list(<br>)]`  

These can be combined to made some very interesting prompts:

- `[prompt-list(, ):Reminder=Don't forget to get \| at the store!]`  
- `[prompt-list([prompt:Custom Delimiter])]`  
- etc...

`[[list:New Day One Entry|🌌 Use Last Photo=launch://x-callback-url/clipboard?attach=photo:last&x-success={{dayone://post?entry={{[prompt:Entry Text]}}&imageClipboard=1}}|📷 Use Camera=launch://x-callback-url/clipboard?attach=photo:camera&x-success={{dayone://post?entry={{[prompt:Entry Text]}}&imageClipboard=1}}|📄 Just Text=dayone://post?entry=[prompt:Entry Text]]]&lc-icon=dayone]`
- `[list|Tech=https://twitter.com/i/lists/864479709685534720?s=20|Info=https://twitter.com/i/lists/980006745287417856?s=20|Info London=https://twitter.com/i/lists/871131909564362753|Education=https://twitter.com/i/lists/1003660247741984768|Cinema=https://twitter.com/i/lists/1171181623834009606|Drôle=https://twitter.com/i/lists/982325034336256001|Littérature=https://twitter.com/i/lists/1100657140597952512]`
- `[list:Spotify Music|The O.C. Soundtrack=http://open.spotify.com/user/knicotera/playlist/1PNyYjU4zJUs4HGC66i9an|Cougar Town Soundtrack=http://open.spotify.com/user/danitosupreme/playlist/2yUQw2SjbdXaDrrQWBEjxT|Scrubs Soundtrack=http://open.spotify.com/user/unsumed/playlist/67Iv3fov4Bhav1qPzot4Nx|Oasis Time Flies=http://open.spotify.com/album/7odHkNOrZmR0YqNWQ3acEm|Pneuma=http://open.spotify.com/album/1LbxLOD9XI54dCu2Bnb5rF|Me=http://open.spotify.com/user/viticci]`
- `launch://messaging?to=[[list:Message Groups|Friends=512-555-2121,512-555-2222,512-555-2323|Family=512-555-1212,512-555-1313,512-555-1414,512-555-1515|Everyone=512-555-1212,512-555-1313,512-555-1414,512-555-1515,512-555-2121,512-555-2222,512-2323]]`

#### Scheduling Examples
- `launch://schedule?action=179&in=1h&repeat=specificdays&days=m,tu,w,th,f` (Schedules an action notification in 1 hour, tapping the notification triggers action 179, then repeats this schedule on weekdays)
- `launch://schedule?action=104&in=[prompt-num:Minutes Until Notification]m` (Prompts for the number of minutes, then schedules an action notification in 10 minutes, tapping the notification triggers action 104)
- `launch://schedule?url=https://apple.com&in=10min` (Schedules an action notification in 10 minutes, tapping the notification opens apple.com)

### Parameters:
- `action` = Action Id
- `url` = Any valid URL
- `at` = Absolute ISO8601 date (plus it should detect a bunch of common formats)
- `in` = Relative date in seconds, minutes, or hours from now (60s, 60m, 1h, or even 1h30m30s)
- `repeat` = hourly or weekly or monthly or specificdays (aliases 'specific-days', 'days')
- `days` = (only used for repeat=specificdays) accepts the actual days to repeat the schedule, pretty flexible, "su,m,tuesday-wed,th,f,sat" works as expected.
- `title` = 

[Absolute ISO 8601](http://support.sas.com/documentation/cdl/en/lrdict/64316/HTML/default/viewer.htm#a003169814.htm) ➝ yyyy-mm-ddThh:mm:ss.ffffff ➝ 2008-09-15T15:53:00 ou hhmmssffffff

### Spark
- `readdle-spark://compose?subject=[[title]]&body=[[body]]`

### Workflow
- `workflow://run-workflow?name=Tweet%20Ralentir%20Travaux`
- `workflow://run-workflow?name=Add%20To%20Things`

### AirMail
[URL SChemes for Airmail](https://help.airmailapp.com/en-us/article/airmail-ios-url-scheme-1q060gy/)

### Supported Tweetbot 3 URL Schemes
[Supported Tweetbot 3 URL Schemes](https://tapbots.net/tweetbot3/support/url-schemes/)
- `tweetbot://<screenname>/timeline`
- `tweetbot://<screenname>/mentions`
- `tweetbot://<screenname>/retweets`
- `tweetbot://<screenname>/direct_messages`
- `tweetbot://<screenname>/lists`
- `tweetbot://<screenname>/favorites`
- `tweetbot://<screenname>/search`
- `tweetbot://<screenname>/search?query=<text>`
- `tweetbot://<screenname>/status/<tweet_id>`
- `tweetbot://<screenname>/user_profile/<profile_screenname>`
- `tweetbot://<screenname>/post`
- `tweetbot://<screenname>/post?text=<text>`
- `tweetbot://<screenname>/post?text=<text>&callback_url=<url>&in_reply_to_status_id=<tweet_id>`
- `tweetbot://<screenname>/search?query=<text>&callback_url=<url>`
- `tweetbot://<screenname>/status/<tweet_id>?callback_url=<url>`
- `tweetbot://<screenname>/user_profile/<screenname|user_id>?callback_url=<url>`
- `tweetbot://<screenname>/follow/<screenname|user_id>`
- `tweetbot://<screenname>/unfollow/<screenname|user_id>`
- `tweetbot://<screenname>/favorite/<tweet_id>`
- `tweetbot://<screenname>/unfavorite/<tweet_id>`
- `tweetbot://<screenname>/retweet/<tweet_id>`
- `tweetbot://<screenname>/list/<list_id>?callback_url=<url>`

The argument callback_url is an URL encoded URL that will be opened in Safari once the Post view closes.

### Things
- [Things URL Scheme](https://support.culturedcode.com/customer/en/portal/articles/2803573)
- `things:///show?id=3CB5436B-4DB8-4B36-A3E2-3572A188115`
- `things:///show?id=50A7C835-5461-4A67-AEE1-BE9EC7E1CAC4&query=Lyc%C3%A9e%20(cours)`

<hr />

## x-callback-url
- [Automatisation sous iOS: url-schemes et x-callback-url](http://www.cuk.ch/articles/5338)

> Le sandboxing est manière d’isoler des applications. Ou n’importe quoi d’autre d’ailleurs. Littéralement, on peut traduire ça en “bac à sable”. Il s’agit de contraindre des apps à travailler dans un environnement cloisonné. Cloisonné ne veut pas pour autant dire totalement fermé sur le monde : depuis son bac à sable, une app peut se voir offrir des accès à des services du système tels que le presse-papiers, l’agenda, les contacts, les photos, etc.

- [x-callback-url Examples](http://x-callback-url.com/ "x-callback-url")
- [x-callback-url Support](https://help.contrast.co/hc/en-us/articles/200611883-x-callback-url-Support)
- [App Talk](https://app-talk.com/)

### Examples
- `tumblr://x-callback-url/text?title=[prompt:Title]&body=[prompt:Body]`
- `airmail://x-callback-url/send?from=account@domain.com`
- `drafts://x-callback-url/create?text={{Hello World}}&action={{Tweet: the_axx}}&x-success={{drafts://x-callback-url/create?text=Hello%20World&action=Post%20to%20App.net}}`
- `goodtask3://x-callback-url/view?title=Today&view=2`

### Drafts
- `Clipboard` ➝ copie le presse-papiers
- `%%[[body]]%%` ➝ convertit le texte en HTML

### Gmail
- `googlegmail-x-callback://x-callback-url/co?subject=[[title]]&body=[[body]]&to=yannhoury@gmail.com`
- `googlegmail:///co?subject=[[title]]&body=[[body]]&to=yannhoury@gmail.com`
- `inbox-gmail://co?subject=[[title]]&body=[[body]]`

<hr />

## Workflow/Shortcuts
- [ShortcutsGallery.com - Download and share Siri Shortcuts](https://shortcutsgallery.com/)
- [RoutineHub • A community for Siri Shortcuts](https://routinehub.co/)
- [Shortcuts Field Guide, iOS13 Edition | MacSparky Field Guides](https://learn.macsparky.com/p/shortcuts13)
- [A Comprehensive Guide to All 120+ Settings URLs Supported by iOS and iPadOS 13.1 - MacStories](https://www.macstories.net/ios/a-comprehensive-guide-to-all-120-settings-urls-supported-by-ios-and-ipados-13-1/)
- [Six livestreams around Siri Shortcuts to watch – Matthew Cassinelli](https://www.matthewcassinelli.com/shortcuts-live_2020-05/)
- [iOS shortcuts. UPull.me](https://upull.me/ios-shortcuts)
- [How to use the Shortcuts app on iPhone and iPad like a PRO - iGeeksBlog](https://www.igeeksblog.com/how-to-use-shortcuts-app-on-iphone-ipad/)

You can use Shortcuts to build these URLs based on time calculated from a Shortcut. [Here's a shortcut](https://www.icloud.com/shortcuts/f6b63b556af449dc82eb072d1545ae35) that gets the next event on your calendar, estimates your ETA, then schedules an action to trigger when you're estimated to arrive (you could also schedule it a few minutes early so that the notification is ready and waiting when you arrive), and finally displays directions to that event in Maps.

### Workflow
- [Workflow 1.4.4 Brings More Image Automation, HTML to Markdown Conversion](https://www.macstories.net/ios/workflow-1-4-4-brings-more-image-automation-html-to-markdown-conversion/)
- [Workflow 1.1: Deeper iOS Automation](https://www.macstories.net/reviews/workflow-1-1-deeper-ios-automation/)
- [How to Create Your Own iOS Apps and Extensions with Workflow](http://lifehacker.com/how-to-create-your-own-ios-apps-and-extensions-with-wor-1672952936)

>  These workflows are a series of directions called "actions", which tell native iOS apps to do specific things.
>  [...]
>  you integrate apps that seem unrelated—like Maps with iTunes, or Calendar with Twitter.

- [8 Reasons to Love the New Workflow App for iOS](http://www.geekswithjuniors.com/note/8-reasons-to-love-the-new-workflow-app-for-ios.html)
- [Workflow Review: Integrated Automation for iOS 8](https://www.macstories.net/reviews/workflow-review-integrated-automation-for-ios-8/)

> In the past two years, most apps that tried to automate iOS were limited to textual input and output as they primarily dealt with URL schemes, which can only carry encoded text across apps. Pythonista and Editorial are [capable of working with images](http://omz-software.com/pythonista/docs/ios/PIL.html) from the Camera Roll, but they require knowledge of Python scripting; Launch Center Pro has integrations with various types of images, but they’re mostly built for connections to third-party services such as IFTTT, Giphy, and Dropbox.
>
>For Workflow, Weinstein and team created ContentKit, a custom iOS framework that is capable of taking a collection of content items and intelligently coerce them into another format. The ContentKit framework powers the Content Graph, which is a “map” of how input from iOS features and apps is translated throughout workflow actions on the fly. The content transformations that Workflow does and that puts in the user’s control are based on a complex technology that allows Workflow to integrate apps and services that are seemingly unrelated, such as Maps and iBooks or Music and Twitter.

- [Creating Device-Framed Screenshots in Workflow - Jordan Merrick](https://www.jordanmerrick.com/posts/screenshot-builder-workflow)
- [Workflow 1.6 Brings Revamped Gallery, Better Tools to Share and Import Workflows](https://www.macstories.net/news/workflow-1-6-brings-revamped-gallery-better-tools-to-share-and-import-workflows/)
- [Workflow, l'automatisation iOS pour tous | Slice42](https://slice42.com/a-la-une/2014/12/workflow-lautomatisation-ios-pour-tous-8678/)
- [Workflow (iOS): Some Example Workflows for Dates - Home - Thought Asylum](http://www.thoughtasylum.com/blog/2015/1/14/workflow-ios-some-example-workflows-for-dates.html)
- [Workflow Tips for Beginners](https://sayzlim.net/workflow-tips-beginners/)

> Never drag an action into a workflow without reading the input and result.
> [...]
> Fortunately, Workflow has a Quick Look that you can use to preview the result in each step before you continue to next action.
> [...]
> Leave a breakpoint with **Alert** action to stop the workflow after previewing the result in Quick Look.

- [Workflow 1.7 Introduces Magic Variables for Easier, More Powerful Visual Automation](https://www.macstories.net/ios/workflow-1-7-introduces-magic-variables-for-easier-more-powerful-visual-automation/)

> Unlike normal variables, Magic Variables carry the icon of the action that generated them. In addition to being a visual aid, the icon indicates the default type of a Magic Variable

- [Workflow: Convert Spreadsheets to MultiMarkdown Tables](https://www.macstories.net/ios/workflow-convert-spreadsheets-to-multimarkdown-tables/)
- [How to use Workflow for iOS when you don't know where to start](http://www.imore.com/how-use-workflow-ios-when-you-dont-know-where-start)

> Think of actions inside a workflow as dominoes
> [...]
>  Workflows are always executed from top to bottom, and each action passes its **output** (the result of what it did) to the next action as **input**.
>  [...]
>   I place the first action and the last one immediately on the canvas.
>   [...]
>   Variables let you save values you want to re-use at a later point in a workflow. A variable can be anything: a bit of text, an image, a date, a location, or even a combination of multiple data types such as a string of text _and_ an image — all inside the same variable. Think of variables as dynamic tokens: You can insert or pass them to actions with one tap, and they carry information that was generated at other points in the workflow.

<iframe border=0 frameborder=0 height=900 width=650   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1027235932062277634?s=12"></iframe>

- [Workflow 1.7.1 Brings New Icon Glyphs, ‘Run Workflow’ Action](https://www.macstories.net/ios/workflow-1-7-1-brings-new-icon-glyphs-run-workflow-action/)
- [The Future of Workflow](https://www.macstories.net/stories/the-future-of-workflow/)
- [Workflow Tip: Append Text to the iOS Clipboard](https://www.macstories.net/ios/workflow-tip-append-text-to-the-ios-clipboard/)
- [HTTP Methods GET vs POST](https://www.w3schools.com/TAGS/ref_httpmethods.asp)
- [Using Simple Dictionaries in Workflow](https://nahumck.me/using-simple-dictionaries-in-workflow/)
- [Publishing Articles to WordPress with Workflow on iOS](https://www.macstories.net/ios/publishing-articles-to-wordpress-with-workflow-on-ios/)
- [iOS Dictionary Lookup via Workflow App | myByways](http://mybyways.com/blog/dictionary-definitions-via-workflow-app)
- [How do you use "get dictionary from input"? • r/workflow](https://www.reddit.com/r/workflow/comments/2qkzxd/how_do_you_use_get_dictionary_from_input/)
- [Things 3.4 Brings Powerful New Automation Features and App Integrations](https://www.macstories.net/stories/things-automation/)
- [Things Automation: Building a “Natural Language” Parser in Workflow](https://www.macstories.net/ios/things-automation-building-a-natural-language-parser-in-workflow/)
- [Workflow 1.7.8 Adds ‘Mask Image’ Action, Things Automation Support, PDF Text Extraction, and More](https://www.macstories.net/ios/workflow-1-7-8-adds-mask-image-action-things-automation-support-pdf-text-extraction-and-more/)
- [How to use Workflow with Reminders](https://www.imore.com/using-workflow-reminders)

### Shortcuts
- [How to use Workflow to make Siri Shortcuts in the iOS 12 developer beta](https://www.imore.com/how-use-workflow-make-siri-shortcuts-ios-12-beta)
- [iOS 12: How to create custom Siri Shortcuts](https://9to5mac.com/2018/06/05/ios-12-siri-shortcuts/)
- [Siri Shortcuts: The next leap forward in push interface](https://www.imore.com/siri-shortcuts-next-leap-forward-push-interface)
- [Shortcuts: A New Vision for Siri and iOS Automation](https://www.macstories.net/stories/shortcuts-a-new-vision-for-siri-and-ios-automation/)
- [All the Shortcuts actions: Apple apps](https://www.imore.com/all-shortcuts-actions-apple-apps)
- [How your favorite apps are embracing Siri Shortcuts](https://appleinsider.com/articles/18/09/17/how-your-favorite-apps-are-embracing-siri-shortcuts)
- [Shortcuts user guide for getting started now available, Siri Shortcuts Field Guide course available for learning more](https://9to5mac.com/2018/09/17/shortcuts-user-guide-ios-12/)
- [How to use Apple's new Shortcuts app | Cult of Mac](https://www.cultofmac.com/560329/how-to-use-apples-new-shortcuts-app/)
- [Shortcuts User Guide](https://support.apple.com/en-gb/guide/shortcuts/welcome/ios)
- [iOS 12: The MacStories Review](https://www.macstories.net/stories/ios-12-the-macstories-review/)
- [Shortcuts at a glance](https://support.apple.com/en-gb/guide/shortcuts/shortcuts-at-a-glance-apdf22b0444c/ios)
- [60 apps that work with Siri Shortcuts](https://www.imore.com/apps-work-siri-shortcuts)
- [Workflow Update Brings Ability to Interact with Any Web API](https://www.macstories.net/ios/workflow-update-brings-ability-to-interact-with-any-web-api/)
- [How to Dictate iMessages in Multiple Languages from a Widget with Shortcuts](https://www.macstories.net/ios/how-to-dictate-imessages-in-multiple-languages-from-a-widget-with-shortcuts/)
- [Add a device frame to iPhone XS screenshots with Shortcuts | Cult of Mac](https://www.cultofmac.com/581298/iphone-xs-screenshots-shortcuts-add-device-frame/)
- [Siri Shortcuts: Ask the experts edition](https://www.imore.com/siri-shortcuts-ask-experts-edition)
- [Astuce iOS 12 : lancer un raccourci presque automatiquement](https://www.igen.fr/ios/2018/10/astuce-ios-12-lancer-un-raccourci-presque-automatiquement-105694)
-  [Use Google Maps or Waze with Siri Instead of Apple Maps](https://ios.gadgethacks.com/how-to/use-google-maps-waze-with-siri-instead-apple-maps-0192301/)
- [Why Shortcuts Matter for Accessibility](https://www.macstories.net/stories/why-shortcuts-matter-for-accessibility/)
- [How to use Siri Shortcuts to get your old phone to do new tricks](https://www.theverge.com/2018/10/25/17871898/siri-shortcuts-ios-12-iphone-apple-how-to-best-tips-tricks-search)
- [Philips Hue App Adds Siri Shortcuts Support](https://www.macstories.net/news/philips-hue-app-adds-siri-shortcuts-support/)
- [How to Trigger IFTTT Applets with iOS 12’s New Shortcuts App and Siri](https://www.macstories.net/ios/how-to-trigger-ifttt-applets-with-ios-12s-new-shortcuts-app-and-siri/)
- [Shortcuts 2.1 Brings New Weather and Clock Actions, iCloud Sharing Improvements, and More](https://www.macstories.net/ios/shortcuts-2-1-brings-new-weather-and-clock-actions-icloud-sharing-improvements-and-more/)
- [Home Screen Icon Creator: A Shortcut to Create Custom Icons for Apps, Contacts, Solid Colors, and More](https://www.macstories.net/ios/home-screen-icon-creator-a-shortcut-to-create-custom-icons-for-apps-contacts-solid-colors-and-more/)
- [Shortcuts 2.2 Brings New Apple Notes Actions, Travel Time Enhancements](https://www.macstories.net/ios/shortcuts-2-2-brings-new-apple-notes-actions-travel-time-enhancements/)
- [How to create handy shortcuts for call reminders on iPhone, iPad, and Mac](https://9to5mac.com/2019/01/04/shortcut-call-reminders-iphone-ipad/)
- [How to stop Apple's Shortcuts app from crashing, and how to fix what caused it](https://appleinsider.com/articles/19/03/05/how-to-stop-apples-shortcuts-app-from-crashing-and-how-to-fix-what-caused-it)
- [Shortcuts Rewind: Linking Tricks Using Markdown and Rich Text](https://www.macstories.net/stories/shortcuts-rewind-linking-tricks-using-markdown-and-rich-text/)
- [How to create a media launcher with Shortcuts | iMore](https://www.imore.com/how-create-media-launcher-shortcuts)
- [Getting started with scripting for Shortcuts | iMore](https://www.imore.com/getting-started-scripting-shortcuts)
- [RoutineHub • What's new on Spotify?](https://routinehub.co/shortcut/5386/)
- [Blur Face](https://shortcutsgallery.com/shortcuts/blur-faces/)
- [How I use the Shortcuts 'If' action to keep my music seasonally appropriate | iMore](https://www.imore.com/how-i-use-shortcuts-if-action-keep-my-music-seasonally-appropriate?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+TheIphoneBlog+%28iMore%29)

## Obsidian/Shortcuts
<iframe border=0 frameborder=0 height=920 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1422130294740684800?s=21"></iframe>

<iframe border=0 frameborder=0 height=800 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1422962219348893701?s=12"></iframe>

## Chercher
<iframe border=0 frameborder=0 height=850 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1083127332934770690?s=21"></iframe>
 
<iframe border=0 frameborder=0 height=700 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1075386859369480192?s=12"></iframe>
 
 <iframe border=0 frameborder=0 height=900 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1082288439893073921?s=21"></iframe>
 
##  Trouver facilement une playlist
<iframe border=0 frameborder=0 height=1300 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1250824162333114369?s=12"></iframe>
 
 <iframe border=0 frameborder=0 height=600 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1308135270739517447?s=12"></iframe>
 
 Pour créer un dictionnaire, lire ces articles :
 - [Using Simple Dictionaries in Workflow](https://nahumck.me/using-simple-dictionaries-in-workflow/)
 - [iOS Dictionary Lookup via Workflow App | myByways](http://mybyways.com/blog/dictionary-definitions-via-workflow-app)
 - [How to create a media launcher with Shortcuts | iMore](https://www.imore.com/how-create-media-launcher-shortcuts)

## Connexion
<iframe border=0 frameborder=0 height=750 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1324430572727554050?s=12"></iframe>

➝ https://feeding.cloud.geek.nz/posts/encoding-wifi-access-point-passwords-qr-code/

<iframe border=0 frameborder=0 height=950 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1250811405944721408?s=12"></iframe>

<iframe border=0 frameborder=0 height=600 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1250811800418992129?s=12"></iframe>

<iframe border=0 frameborder=0 height=1200 width=550   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1250823077597937666?s=12"></iframe>

<iframe border=0 frameborder=0 height=700 width=500   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1055745946716422144?s=21"></iframe>

<iframe border=0 frameborder=0 height=700 width=500   
 src="https://twitframe.com/show?url=https://twitter.com/yannhoury/status/1054471386461298691?s=21"></iframe>


## YouTube
<iframe width="560" height="315" src="https://www.youtube.com/embed/ueUSr3HOj4A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/ySY1vvJA2Hw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/y76VsWpzjKE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/z8VotTnO90o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/dn7B-mHCZnY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>