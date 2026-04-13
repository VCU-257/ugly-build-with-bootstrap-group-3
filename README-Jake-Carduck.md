# Student Name: Jake Carduck

## 1. My Assigned Work
Find My Representative Page parts:
* Search bar
* Filters
* Suggested profiles
* (Accidentally) Scroll feature for just the suggested profiles
* (Extra) Deployment and fixing problems with connections between pages

## 2. Bootstrap Implementation
**Components Used:**
* Form Controls
* Dropdowns
* Checkboxes
* Radio Buttons
* Cards
* List Group  

I did not stick to the plan from Table 1. Some components were used, but I found better ways to implement others. For example, I realized the filter section would work better if there was a dropdown that let you select multiple options, so I ended up using a combination of a dropdown and checkboxes. I also realized selecting whether to search by address or by representative name should be kept separate from filtering by representative type, so I used radio buttons for the search by choice. Another thing I changed was scrollspy to flex-grow combined with overflow; this was because I found out scrollspy's usage didn't fit the scroll feature for the suggested profiles.

## 3. Technical Challenges & Solutions
I faced the fourth risk, dealing with live updating suggestions during searches. I realized it was infeasible to do in a reasonable amount of time, so I plan on discussing whether we want to take a more static approach or if we want to divide up the work to get it done. Otherwise, the hardest part of my assigned work was either getting elements to display correctly (correctly splitting the page, ensuring radio buttons were inline, etc.) or adding the scroll feature to the suggested profiles section (which was difficult because I had to figure out how to stop overflow in other areas while still allowing it in this section, so that a scroll bar would appear).

## 4. AI / LLM Usage
I didn't use AI for the search bar at all. The only AI I used for anything was Gemini. For the radio buttons, I needed help figuring out why the inline feature wasn't working; I passed it all of my code and kept asking it different questions or providing it my updated code until it help me figure out I needed an additional div HTML tag in order to stop flex-column from stacking my inline radio buttons vertically. This allowed me to realize a flex-column class in a parent tag forces all its children to try to stack vertically as well, and that you can use an additional tag in order to nest your original element if you want to avoid this. I also used AI to help me understand the nuances of various classes that were in getbootstrap.com's examples, such as how various classes can conflict. One of the biggest tasks AI helped me finish was establishing the scroll bar feature, which was challenging because the suggested profiles section often extended the entire webpage, instead of just its area. Gemini helped me realize I needed to make use of flex-shrink-0, overflow-hidden, overflow-y: auto, min-height: 0, and h-100 in order to force the suggested profiles section to only overflow in its area, which would create the scroll bar I desired.

## 5. Live Site Link
* **Live URL:** [Find My Representatives Page](https://vcu-257.github.io/ugly-build-with-bootstrap-group-3/find_my_representatives)