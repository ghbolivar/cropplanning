# Using the Program #

To learn about how data is "inherited" or shared between crops, varieties and plantings in the program, see the section titled [Concepts](#Concepts.md).

In order to start using the program, you must do three things after opening the program:

## Step 1: Define Crops (_optional_) ##

Select "CropDB" from the list of tabs at the top of the window.  Click "New" and enter some data about a crop: its name, rows/bed, row and plant spacing, etc etc.  Click "Save" and you will notice that the crop shows up in the table at the top of the window.


## Step 2: Define Varieties (_optional_) ##

Click "New" again.  Now punch in the name of the crop you just defined.  Note that it should automatically complete the name when you start typing it.  Then enter a name for the variety in the "Variety Name" box.  Go ahead and click "Save".  You should see that any data you had entered into the crop will be displayed as part of the variety.  At this point, enter any information that is specific to this variety.  (Perhaps it differs from the data you had entered for the crop.)  This might include maturity days and other information.

## Step 3: Create Crop Plan ##

Now switch to the "CropPlans" tab (at the top of the window).  Enter a name (no spaces or punctuation) into box at the top left of the window and click the "new plan" button.

## Step 4: Create Planting ##

Now, as in step one, click the "new" button (next to the "duplicate" button).  In the lower half of the window, enter the crop name and the variety.  Both of these values should automatically complete as you begin typing.  As in step 2, go ahead and click "Save".  Notice how some data is filled in from the crop and variety that you created before.  Now enter a date (in mm/dd/yy format) into either the planting, transplanting or harvest field.  Click "save" again.  Depending upon which data you have entered, you should see that some other fields have filled themselves in by calculating what they should be.  For instance, a harvest date is just a planting date plus a maturity day figure.  Likewise, the planting date is just a harvest date minus a maturity day figure.

Now enter a figure for either how many beds to plant, how many rowfeet to plant or how many plants you will need and click "save".  Many other figures -- again, depending upon which data you've entered -- will be calculated.

# Advanced Usage #


## Editing Multiple Records ##

If you need to make changes to multiple crops or plantings, you can simply select each of those records from the list view.  The bottom half of the page will display ONLY the information that is shared by all of these records.  Simply make your changes (in the bottom half) and click "Save".  The changes will be saved to all of the records you have selected.


## Sorting ##

To sort the list by a particular row, simply click the header of the row.  To reverse the sort, click the header again.


## Filtering ##

Filtering is one of the most powerful aspects of the software.  Keep track of as many plantings and data as you need without fearing that they will get lost in the jumble.  You can use filtering to show you only what you care about.

#### Runny Tally ####

The program displays a tally of certain data which is updated depending on the filter.  If you limit the view to just those plantings which will be transplanted, it displays the number of beds and flats you'll need for those plantings.  This is updated every time you change the filter.

Examples:
  * If you've tagged certain crops or plantings as requiring plastic, type in "black plastic" to see how much plastic you'll need for those plantings.
  * Type in "potatoes" to see how many beds of potatoes you've scheduled to plant.
  * Say you want to know how much greenhouse space you'll need in May.  We can't tell you exactly (not yet; we're working on that one) but you can get a pretty good idea this way: Create a "custom" filter to display only those plantings which are scheduled to be planted **before** May 31 and which will be transplanted **after** May 1.  This will limit the view to plantings which will be in the greenhouse at some point during May and the running tally will tell you how many flats they comprise.  (_Note_ that there is currently a bug preventing this from working.)

#### Text Filtering ####

The box in the upper right of the page can be used to filter the list view.  Just type in a word or even just a few letters of a word and the list will be adjusted to just show the records which match the letters or word you entered.  This filtering happens on a number of data, not just the crop and variety name.

Examples:
  * If you have recorded which crops require "black plastic" or "reemay" in one of the fields (_Other Requirements_ would be a good place), you can filter the list on "plastic" or "reemay" to just show the crops or plantings which require plastic or reemay.
  * You can type in a month name to limit the view to just plantings which occur in that month.  "ma" will show all plantings which are scheduled to be planted, transplanted or harvest in May or March.
  * Enter the name of a crop or variety to just see plantings of that crop or variety.


## Weekly Planting Lists ##

The 'TODOLists' module allows you to create ready-to-print PDF files for **GH seeding** list, **field planting** lists and **field transplanting** lists.  You can simply select _this week_ or _next week_ for a list of what is scheduled for those weeks, or you can specify your own date range to create lists for other weeks, multiple weeks, whole months or ... well, you get the idea.  Currently, however, you cannot select which columns/data are included in those lists; as always, _we're working on it_.


## Simple Date Adjustments ##

After any date, you can type in a '+' or '-' expression to add or subtract a few days, weeks or months to that date.  Stick a 'd', 'w' or 'm' at the end of the expression to specify **d** ay, **w** eek or **m** onth.

Examples:
  * "+1" and "+1d" both add one day
  * "+1w" adds one week
  * "-2m" subtracts two months

Another example: Say you want to create a set of **monthly successions**.  Unfortunately, the program cannot **yet** do that for you.  But we've made it as **easy as possible** for you to do it yourself:
  1. Create the first planting of the succession.
  1. Select it in the list view and click "Duplicate".
  1. Select the date you want to to shift and enter "+1m" after it.
  1. Save your changes and you see that the date has been shifted by one month.
  1. Now do the same for the rest of your planned successions.


## Displaying Different Columns ##

Right click on the column header (on Windows; or Control-click on Mac) and a pop-up list of displayable columns will appear.  Select a column from this list and it will be displayed.  Also, click on the name of any displayed column in the popup list and it will no longer be displayed.


## Custom Fields ##

There are, invariably, data which I have not thought to track but that you find invaluable.  For these cases, I have created the "custom fields".  They are currently only accessible through the column name popup list (see the previous item).

# Suggestions #

We welcome your suggestions!  Remember, this is FREE software written BY farmers FOR farmers.  Your suggestions can only make us better.  If there's a feature you'd like, data you think we should track or bug that needs to be fixed: [PLEASE LET US KNOW](mailto:cropplanning@gmail.com)!


# Concepts #

It is important to understand a couple things about the simple way that this program "models" crops and plantings.  Information is "passed down" from "crops", to "varieties" and then to "plantings".  This allows you to change some common aspects of your crop plan (such as your row spacing, rows/bed, etc) without having to change EVERY entry in your plan.

## Example ##

Let's look at sweet corn.  Say you make 5 plantings of corn throughout the season.  The first two are transplanted and the last three are direct seeded and all are planted  at 2 rows per bed.  Also, lets say that the 5 plantings are of 3 different varieties, each with a different maturity.

In this case, you could define a "crop" as corn.  This would include the information that is common across ALL or even MOST of your corn plantings.  eg, 2 rows/bed.

Next you could create definitions for the three different varieties.  In this example, these definitions would include the variety name and the maturity day figure of each crop.

Finally, you will turn these crop and variety definitions into "plantings".  This will add specific details to each crop or variety that will be used for planing and for planting.  In this example, you will create 5 plantings.  The first two will include the dates that you will seed the corn in the greenhouse and the dates you will transplant.  You could also add information about the size of flat you will use in the GH and the number of weeks it is grown before transplanting.  For the last three, you could just enter the planting date.

## Data Pyramid ##

Perhaps it is helpful to think of these things as a three tiered pyramid.    The top tier contains the most general data and the bottom tier the most specific.  The data at each tier is applicable to any number of entries one the tier below and the data on the bottom tier is ONLY applicable to one specific item.  In this metaphor, plantings are on the bottom, varieties are in the middle and crops are on top.