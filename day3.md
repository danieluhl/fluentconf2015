# Day 3 - JavaScript Delirium

## design + performance

- steve Souders
- @souders
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








































