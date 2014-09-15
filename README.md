# Description

This is a proof-of-concept prototype for a single-page directory of links which adapts based on user behaviour data.

## Instructions
Create groups (sections), and then add links to them. Click on them to create user behaviour data and watch them re-sort. Adjust the number of links to display to hide the worst-performing links

## Note
* There is no back-end at all, so data is not persisted
* Links do not actually open web pages so as not to be annoying

# To-do List
* ui cleanup. set focus on various occasions; maybe add animations
* Add ability to delete groups
* Add ability to edit text/urls of groups and links
* Groups should be sorted by the sum of scores of their visible links only - maybe
* Allow group headings to themselves be links, which are also tracked
* Allow a third level of hierarchy for links - but no more
* The sorting algorithm now used is overly simple, just the link count. This will need to be changed.
* Backend for data storage
* Split ui into an 'edit/admin' interface and a 'view' interface
  * In view interface, don't show empty categories
  * In view interface, collapse multiple categories with only a single link into a single 'Misc' group - maybe (but wouldn't it need to be listed last then?)
* Allow multiple versions of text for a particular link and use for A/B testing
* Allow links to be arranged into different groups (card sorting...) and use for A/B testing


# Sorting Algorithm

The current 'algorithm' is a placeholder. It breaks when some links are added later and have had less time to accumulate clicks. Also, the scores should probably decay at some slow rate so that links which are no longer as popular as they were are replaced by ones that are. Can probably adapt one of the algorithms from https://github.com/clux/decay