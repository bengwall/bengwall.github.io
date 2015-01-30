---
published: true
layout: post
---

These types of decisions can sometimes be difficult and this is no different.  I took a quick look at ngTable, trNgGrid, and SmartGrid.  ngTable has a bigger following.  I like the way trNgGrid is designed and how it is configured.  Smart grid is also well designed.  I would personally try trNgGrid first.  It must be very good, however, to outweigh the risk that it has less of a community around it.  So much of this is trying to determine which one will be better maintained 2 to 3 years from now.  ngTable is definitely the most widely used, but has not had a commit in 8 months.  ngTable is the only one with built in row grouping.  Other than that I don’t know if you can go wrong with any one of them. 
 
All

-  Flexible Column formatting
-  Sorting, filtering, paging
 
ngTable

- Built in capabilities for row grouping and row checkboxes.
- Larger community at this point. 
- The directive has not had a commit in since January 2014 when a revolution started in the authors country:  http://stackoverflow.com/questions/21375073/best-way-to-represent-a-grid-or-table-in-angularjs-with-bootstrap-3
 
trNgGrid

- Better designed.  Uses declarative method to configure the grid fits better into Angular’s way of doing things (rather than the way ngTable does it in the js)
- More row selection capabilities
- Actively maintained.  Last commit to the directive was 12 days ago
- Only 1 committer.
 
SmartGrid

- Also well designed
- Nice auto-scroll feature (scroll to the bottom of the grid and the next N number of rows appears)
- Easily to create directives to enhance the control
- Actively maintained.  Last commit to the directive was 17 days ago
