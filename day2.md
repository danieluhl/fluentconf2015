# Day 2 FluentConf2015!

## keynote notes

- Focus on what the user feels
- Response to actions - 1ms (scrolling)
- Idle - no input - but expect input at any time
- Paulirish.com
- Vsync
- What causes issues with html5
- 60fps!
- 16ms - next image must hit
- Browsers are synchronous
- Obtain.richards
- Jit is clever
- Gc always takes a long time, avoid stepping on them - use c style loops
- Jit coach
- Profile to find perf issues not code
- Position absolute - minimize layout rendering
- Use translation and alpha - happens in gpu
- Scaling is bad, animating is very bad
- Use video, not gifs
- Stroke is slow, where is render time happening
- Align your pixels! - even in canvas
- Don't read back pixels, canvas read pixel is bad
- Later optimizations - how does the gpu split up your image
- Paypal trained 100s of debs in JS and Node
- Use as much open source as possible - choose it to work on their side projects
- The ui is the experimentation layer
- @shaunlebraun
- Kangex
- Soundscript
- Dart
- Clojurescript
- Js can't do 64-bit
- Safe stack allocation
- Mix objects and
- Threads for cross compiling c++ to JavaScript
- Ecmascripten
- Shared worker - confined memory
- Web workers
- Shared array buffer - like typed buffers
- Ibm bluemix cloud
- It's not what you know, it's how fast you learn
- Do you make people choose cake - reduce cognitive leaks
- COGNITIVE RESOURCES!!!
- cognitive resources are finite and always used
- sub tasks to master something
- Half a skill beats a half assed skill
- 3x45 minutes to master
- Practicing being mediocre makes you good at being mediocre
- Good by failing not by teaching
- Expert over the shoulder
- Perceptual learning
- High quality high quantity examples - compressed amount of time
- That's adorable


## heal the fork or rip it apart?

Dan shaw (node)
Michael Rogers (iojs)

- open source foundations are difficult to found

Why did the iojs fork happen?

- goals are the same, no controversy there
- how projects should run were diverging
- the fork was to get more of the community involved (layered approach)
- governance model that would support that
- Joyent - hard to be responsive to the community
- what is the best thing for the community - joyant wants to go do that
- the project was griding to a hault and both iojs and joyent addressed that issue
- the node brand is important to maintain
- iojs and node agree on the vast majority of things

"it was important to get broader adoption, people go to kernal.org to get that stuff"

- ... there, a trademark and brand actually matters
- users, vendors, contributors
- users have to be satisfied, they are often betting their careers on that bit of code
- to have a successful project you have to have happy vendors to add value to the technology
- they go to "go", they leave sql and go to postgres
- projects critical to core development (streams, naan)
- projects outside of core (express, happy)

### dropping the CLA was critical

- no developer wants to sign the CLA
- where we ended was with a DCO
- if you don't have an apache 2 license, these are important to have
- nobody wanted the CLA, but the companies were left hanging dry
- companies commercializing this codebase (paypal, walmart)
- developers are artists and want to practice their craft
- companies want clarity in intellectual property


## Front-end performance automation

- etsy is really fast
- grunt, gulp to automate your junks
- matchdep module to setup your stuffs
- grunt-devperf --save-dev
- slides at ki.tt/fluent2015
- data stored in JSON file
-























