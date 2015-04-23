# Day 3 - JavaScript Delirium

## design + performance

- steve Souders
- @souders
- speedcurve
- bring devs and design together
- obligatory venn diagram
- designers should be sitting in the same area as the front-end team
- designs need to be performant, no reckless design
- performance in design affects your page rank - is critical

### how do we get there?

- small cross-functional teams (react, hack, hhvm, jsx, xhp might be good here)
- agree on guiding principals
    - ex. speed is more important thatn design embellishment (site must run in under 2 seconds)
- site should never feel "clogged" with content
- prototype early - no designs or mocks, real data with real software, run perf tests
- live design with chrome dev tools in front of the designer and product owner
- track your performance budget and find where you can save
- surface your page data live on the page - constant reminder on what performance is happening
- surface your ga stats - bookmarklet to bring a page with all perf metrics
- window.onload is not the best metric for measuring speed
- we're trying to capture the user's perception as much as possible
- webpagetest
    - page load time
    - start recorder
    - speed index
    - start render
- **speed index** - above the fold median pixel was rendered
- filmstrips
- video

### custom metrics

- what matters most to the user in your application
- User Timing Spec!
- ex. time to first tweet
- performance.getEntriesByName("hero.jpg")[0].duration - network activity end NOT render end
- image onload handler? NOPE - still not exactly when the image displays on the page
- offsetHeight polling - NOPE
- inlinescript after your image tag - YES finally we get the correct result for when the image actually shows
- but wait, if the image is really slow the inline script is wrong and the resource timing is correct
- take the largest metric to get the right value
- **design for performance by lara hogan book**
- souders25 for 25% off velocity santa clara


## Responsive design, design and dev

- @divya (project manager adobe)
- entire slide presentation in photoshop
- flexible content
- why is responsive better than user agent detection
- users are on the internet more on phones than desktop
- ux, devs, client all must be happy with the design
- browser complexity makes things difficult

### search for patterns and practices to do things better

- workflow, tooling and problems
- dissatisfaction with workflows
    - increase collaboration
- love for existing design tools
    - lack of tools for collaboration
- did not like tooling updates
    - No time to learn new UI for efficient design
- it's not east to collaborate between design and development
- clients don't know what responsive design is
- hard to keep pace with changing browser featureset
- tedious to update designs for different devices

### responsive design

- define breakpoints
- design for breakpoints (snap to grid in photoshop)
- link smart objects
    - new file that is updated in all usages when used
- creative cloud extract for psd to html removes the language barrier

### avoid tedious changes

- html5please - what you can use and what's the fallback
- use popular responsive frameworks - others have already battle tested these in all the browsers on all the devices

### responsive vs adaptive

- use data to find common viewports & use

## algorithms for animations

- simple formulas to activate your UI
- @chemphill
- courtney hemphill
- carbon five
- design v dev
- motion in UI
- animations are cognitive aids
- affordance - implications of physics
- loading icon, then scan through every image in the slider so user get's an initial preview and knows the content is there
- pinterest auto-loading
- playful nature gives trust and dissuades frustration
- wrong password shake

### navigation

- show where something is using animations
- where you came from, where you went, and how to get back

### progressive disclosure

- one thing at a time

### context

- pull to refresh (additional information without leaving current context)
- HOW it slides in is almost never specified in a spec
- when it comes to animation, wireframes just don't cut it

### math of animations

- you don't need jQuery or some huge library
- interpolation > pixel pushing
- a 0-1 number that you can mess with
- torque drag spin friction are natural (easing)
- ease in is jarring
- ease out is a bit more natural
- trig! sine curve is good
- interpolation > 1 = follow through (elastic, bounce, more playful, don't push too far with users)
- 12 principals of animation (by Disney)
- Don't over-use follow through interpolation
- adobe edge animate
- adobe after affects
- flinto
- keynote
- quartz
- animations in native env are more powerful
- framer.js
- tween.js
- **GSAP (Greensock)**
- jQuery
- css animations > giant js frameworks
- control animations carefully in css can be tricky
- animate.css
- cssanimate.com
- sass/less mixins
- translate perf good


## Reactive, Component-based User Interfaces

- ben - front-end eng at hubspot
- tips and patterns that work
- @raganwald
- every problem starts easy but gets harder over time
- declarative vs imperative
- exponential growth of complexity
- angular hides the complexity it doesn't remove it
- one direction works, two way binding does not
- sledghammer (backbone) vs scalpal (virtual dom)
- this is so cool I don't care if it's slow, someone will make it fast
- getting back to a more reliable model is the story, not virtual dom
- functional over OO
- stateless over stateful
- clarity over brevity
- compositions of functions as a primary mechanism for building programs
- component trees = functional composition
- decorator (higher order function) > mixin
- use mixin when you need to access internal state
- likely use base classes in the future
- for all other cases use higher order components
- container component (similar to wrapper)
- renders no UI
- fetches and manages all data for subtree
- no children (we need PureRenderMixin)
- not re-rendered (no v-dom hooks?)
- integration point for flux
- re-usable subtree
- complexity in software is only increasing
- don't look at a feature checklist - use the tools that get the job done
- @ben_anderson

## introducing native script

- http://mediamath.github.io/strand/
- http://www.theuselessweb.com/
- weird al yankavic awesome
- all of you javascript belong to us
- @burkeholland
- build native mobile applications using javascript
- simple clean and modern
- npm install -g nativescript
- unikitty
- nativescript.org
- demos > business slides
- tns create fluent -demo
- new native script app
- tns platform add ios
- tns emulate ios
- nativescript is not phonegap there is no DOM
- there's no html and there's no DOM
- alert and console yes
- js css and markup - xml
- XML is like violence, if it doesn't solve your problem, you aren't using enough of it.
- main.xml in the app folder
- require and export
- app for color picker called sip

## front-end craigslist

- meeting your users needs
- consistency
- @jsartisan
- code rot
- tech debt
- to avoid code rot, program with the programmer in mind, not the customer and not the machine
- use comments
- clarity > efficiency
- weed the garden - always re-do that bad bit of code
- red diffs - delete old code!
- The Two Pillars of JavaScript by Eric Elliott
- Adaptability
- modularity
- optimized loading (http2)
- isomorphic
- testing
- project growth curve and upgrade 12-18 months out
- slow down to speed up - build out your infrastructure and innovate your application
- thing globally and massive
- unicode
- always run text through a get text function
- high performance browser networking
- prototype, debug, optimize, polish and release (repeat)
- maps and location awareness should be used on almost every website in existence
- the more familiar people are with your site, the more tunnel vision they get for a specific feature
-












































