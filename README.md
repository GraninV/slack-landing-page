# README: *slack-landing-page* 
_____

**Ahsan Azim, July 2016**

<img src="https://raw.githubusercontent.com/ahsanazim/slack-landing-page/master/screen_caps/full_view.png" width="600">

This project represents a website that, in its design, imitates that of **Slack**'s landing page - which is accessible at ``slack.com``.

All links and tabs are currently empty, as the construction of this page was simply an endeavour in imitating a modern and successfull design style. 

Part of the challenge was that I tried to maximise the website's responsiveness while restricting myself to only ``html`` and ``CSS``. Zero Javascript was used. Such an approach required myriad workarounds, some of which will become clear in the *Extensions* section at the bottom of this page.

## Usage:

The web page is accessible at 

- ``clever-camera.surge.sh``,
- prefferably on a latest-version (w.r.t. July 2016) Google Chrome browser. 

Although it may load and 'work' on previous versions and other platforms, thorough testing has not been done on said platforms. 


## Developmental notes:

- At its earliest stage, the website started out as a simple html file, which looked like the following when rendered:

<img src="https://raw.githubusercontent.com/ahsanazim/slack-landing-page/master/screen_caps/basic.png" height="500">

- Slack's font of choice (*Lato* - ``https://www.google.com/fonts/specimen/Lato``) was used throughout
- The backgrounds used - both the main background and that of the contracted version's menu page - are shown below. They were selected for their contrasting color schemes, and because I like them :)

<img src="https://raw.githubusercontent.com/ahsanazim/slack-landing-page/master/screen_caps/main_background.jpg" width="450">

**img**: *the main background*

<img src="https://raw.githubusercontent.com/ahsanazim/slack-landing-page/master/screen_caps/menu_background.jpg" width="450">

**img**: *the phone menu background - note that only a subset of it actually appears when navigating the phone menu*

- Flexboxes were used throughout in constructing the layout of the page. Thus, this page does not contain any instances of CSS' much feared ``float``.
- A particularly annoying stafe of development was ensuring that there remained no whitespace when changing the screen size. Note that the problem was fixed by assigning   

```
height: 100%; 
width: 100%;
```
when styling the ``html, body`` section, and 

```
height: 100%; 
width: auto;
```
when styling the main ``cover`` div. 

- Although the checkbox hack (referenced below) was in principle somewhat simple to implment, there were some absurdly frustrating design issues to overcame in its latter stages. These were concerned mainly with figuring out where on our page the menu pop-up (which was at this stage set to occupy zero space and not be visible) should be located. Its location - even when not visible - was having implications on later implementing proper transitions. Fixing this issue was accomplished by slightly tweaking both the transition performed, and the div containing our pop-up menu bar. 


## Design features of note:

Some specific design features, I feel, are worth pointing out in particular:

- *responsive screen-size and design*: when moving to a sub-640px screen size, the web page not only resizes in a bug-free way, but also alters the design susbstanially. This is meant to create a more mobile-friendly look:
- box shadow and color change when hovering on items of note.
- the font choice (Lato) is again relevant here. 


## EXTENSIONS:

I have implemented the following two official extensions:

- CSS Checkbox Hack for the mobile version Menu (reference ``https://css-tricks.com/the-checkbox-hack/`` for a detailed description of the hack)
- Fancy CSS transition

On a somewhat related note, I was also able to find a bug whereby the mobile-friendly version of the screen would actually not load when used on a mobile. This was fixed by inserting some boilerplate code in the ``head`` section of my ``index.html``.

I also made the pop-up menu somewhat stylized:

- a darker colored version of the main background is set as the pop-up background, 
- box shadow implemented upon hovering over pop-up menu items

The following should suffice as a demonstration of all of the aforementioned behaviour:

<img src="https://raw.githubusercontent.com/ahsanazim/slack-landing-page/master/screen_caps/checkbox_menu_css.gif" height="500">