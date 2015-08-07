# Process for ALL new Columns #

## Step 1: PLAN ##

Plan, plan, plan.  Make sure that this data/column/property is really needed.

## Step 2: Update Schema ##

This will make sure that new tables/installations will be correct.

## Step 3: Create Update Method ##

This is in HSQLUpdate and will make sure that existing databases will be up to date.  Generally, the most common actions will be:

ALTER table ADD COLUMN new\_col
ALTER table ALTER COLUMN col RENAME TO new\_col

Often, you'll have to cycle over all of the crop plan tables and update each in turn.

## Step 4: Add property number(s) ##

This is in CPSDataModelConstants.

## Step 5: Add column(s) to HSQLColumnMap ##

After this, the new columns should show up in the list view and be fully viwable/editable.  If the data needs to be part of the CPSCrop/Planting data structures or needs to be displayed as part of the detail or info panels, keep going.  Otherwise, you're done.

# Process for Columns which need to be part of the CPSCrop/CPSPlanting data structures #

## Step 6: Add getters and setters to CPSCrop/Planting ##

## Step 7: Update methods resultSetAsCrop/Planting ##

This is HSQLDB.

# Process for Columns which need to be displayed in the info panels #

## More later ##

