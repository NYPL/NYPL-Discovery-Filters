The biggest problems I see right now are 
1) Terminology (Filter vs Refine Your Search) 


2) Dealing with the layout of the Filter/Refine Your Search button and resulting filters,

    Having the “Filter” act as an action, label and them close button is tricky. Not sure this can actually work. It suggests having “Filter” on the left, which means the user’s eye is drawn to right (Search), to left (Filter) to the right (sort), which isn’t efficient.
    There are 2 options in the prototype, one with “Filter” on right, one with it in the Display Results bar. Let’s discuss options tomorrow.

* _This needs clarification_    

* _Technically having the button toggle from Filter <--> Close should be trivial, whether or not users understand its state change is another matter_

3) The hierarchy of the buttons (Keeping them all in the same style is confusing and eventually visually overwhelming).

* _From the provided design this list there is no guidance on how each fitler type should be rendered_

I’ve included some possible solutions in the sketch file - would like to hear your thoughts.
There’s a prototype up at  https://invis.io/37F89CTM9#/272287523_v3-_1-_start_Copy_2. 
Up by the logo you’ll see “v3” and “V4” . Click on those to toggle between 2 possible layouts

* _Stop using Keivit we should be moving away from this typeface and strictly using system fonts_

These definitely aren’t final at all, but want us to focus on how it feels to use the page and make sure buttons etc are placed in the right position.


Also below are some notes on general layout and tightening up the page which are more straightforward


### GENERAL PAGE LAYOUT
let’s keep the layout of the page as consistent as possible

    Keep things aligned to a grid

 * _OK, but we're veering in to "pixel perfect" territory and there be dragons_
    


    Reduce the movement of the color background as much as possible
    
    * _???_





### SEARCH CONTROL AREA
Search Box
- Center search bar in color field, aligned to the logo
Fields

right now that’s pretty narrow. We need to show worst case for “Author/Contributor” esp for Mobile
Let’s try moving to the right. It follows a more logical flow. 

Also when it’s on the left, if a user changes their selection, the input prompt to the right (Keyword, title, or author/contributor) should change as well. 


* _Could require JS to accomplish this, so a no-JS fall back behavior will be needed_

Exposed Filters

    I’ve moved the “x” to the right since it interrupts readability


### REFINE SEARCH
Accordion Display
This area needs be tightened up. For example, running “format" across 2 or more columns instead of one

    Need to make it easier for the user to scan by adding stronger headers.

* _ok_

    “Formats”and other filter categories needs to work on some type of grid. In these examples, I’ve used a 3 column grid but see how well that works on other sizes

* _ok, small screens will still render as a single column. As the viewport grows, we can add more columns (should max out at 3). What are your thoughts about the DOM in this case? For languages, we use CSS Columns which render breaks on vertical height_

    Date is visually confusing so let’s tighten that up. I made the inputs smaller, since they’re a max of 4 digits, and aligned it to a grid
    Date should also have a prompt in it, showing the user the correct format


* _This is not an html text field, since the library is not strict about dates forcing a year could result in negative results_
* _the grid you are imposing is not rendering..._



### RESULTS INFO AREA
Results Info Bar

    make this space feel more like a header for results
    bolder text
    aligning to the bottom
    tightening space
    We don’t need to repeat the keyword, and in mobile esp it can get quite long and moves result further down the page

    Move “Sort” out of drop down - it obscures the key word (Relevancy, Alphabetical etc)
    Is there a reason the “Sort By” button is so large? It’s a secondary function, needs to be clear but not competing with the other functionality


### Results Display


    This needs to show the changes we discussed earlier (no underline, tighter spacing etc)


### OTHER DETAILS

    Why is the select drop down different for Fields vs Sort By?



### FUNCTIONALITY QUESTIONS

    When I hit the “Search” button, I’m assuming that removes all my filters and returns results based on my keyword and fields. Is that correct?


    Dates: If a user has set a Start Year of 1952 and an End Year of 1982, what happens when they remove “1982” from the exposed filters? Does this change to “Present”, since the search will now (I assume) be 1952-present… Or does something else happen?


    Is it easier to place Dates in one filter button, adding and removing at one time?

    Are filter buttons ordered by category or time they were added? Should be by Category

* _looks like by category (sort of). formats come first, then languages, then date(s) orderd by "start" date then "end" date_
