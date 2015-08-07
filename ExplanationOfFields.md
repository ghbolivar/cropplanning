## Introduction ##

There are numerous data fields that are tracked by this software.  Some of them are straightforward and some are not.  Below, we describe each field, what it tracks, entry syntax (where applicable), whether fields are inherited/inheritable and whether and how certain fields are calculated.

## Fields Tracked for Plantings ##

#### Crop Name ####
Type: _Text string_
Inherited: _No_
Filter: _Yes_

This is simply the name of the crop type to be planted.  This field is _required_ and is limited to the crops which have already been entered into the CropDB.  This field is used when the software looks for data in the CropDB to "inherit" into this planting.

#### Variety Name ####
Type: _Text string_
Inherited: _No_

This is the name of the variety to be planted.  This field is _not required_.  This field is used when software looks for data in the CropDB to "inherit" into this planting:
  1. the software will look for an entry that matches the crop AND variety name which has been entered in this planting.
  1. failing that, the software will look for an entry that matches JUST the crop name which has been entered in this planting.


#### Groups & Keywords ####
Type: _Text string_
Inherited: _Yes_

These fields are free form entry fields and are open for you to use them as how ever you want.  These would be the places to tag something at "frost sensitive" or "heat tolerant" or "winter over", etc.

#### Other Requirements ####
Type: _Text string_
Inherited: _Yes_

Another free form field which you could use to record treatments which this planting will need.  For example: "black plastic", "reemay", "fish emulsion", "sidedress", etc.

#### Notes ####
Type: _Text string_
Inherited: _No_

Yet another free form text field in which you can record notes about this planting.  For example, "double this next year" or "plant two weeks earlier" or "try transplanting next time".  Currently, this field is unused except by you, but we hope to create a way for you to review your notes as you create your plan for next year.  Please [contact us](mailto:cropplanning@gmail.com) and let us know how you're using some of these free form fields and how you would like to see the software handle them differently.

#### Location ####
Type: _Text string_
Inherited: _No_

Use this field to record the location (field or garden name, bed number) of the planting.

We suggest the following syntax which, though not currently used, will eventually help the software keep track of bed/row lengths:

`[ <field name> [ : <plot in field> ] [ ( <bed/row length> ) ]]`

Excuse the forbidding look, what it means is this:

  * you can enter a field name
  * if you enter a field name, you can also enter a plot name (such as a bed number).  If you do this, you should separate the plot name from the field name with a colon (':').
  * if you enter a field name and regardless of whether you enter a plot name, you can specify the bed or row length (in feet) used in that field.  If you do this, you should enclose that number in parentheses

> Yikes!

#### Maturity ####
#### Maturity Adjust. ####
#### ~~Planting Adjust, DS Adjust, Season Adjust and Misc Adjust~~ ####
#### Time to TP ####
#### Planting Date, Transplant Date & Harvest Date ####
#### Done Planting, Done Transplanting & Done Harvesting ####
#### Beds to Plant ####
#### Rows per Bed ####
#### Plants Needed ####
#### Rowfeet to Plant ####
#### In-row Spacing or Space Between Plants ####
#### Row Spacing or Space Between Rows ####
#### Plants to Start ####
#### Flat Size ####
#### Flats Needed ####
#### Planter and Planter Setting ####
#### Yield per Foot ####
#### Total Yield ####
#### Yield Number of Weeks ####
#### Yield per Week ####
#### Yield Unit of Crop ####
#### Unit Value of Yield ####
#### Custom1, Custom2, Custom3, Custom4 and Custom5 ####


## Fields Tracked for Crops and Variety ##