# Crop Planning Software #
http://cropplanning.googlecode.com<br>
cropplanning@gmail.com<br>
<br>
Release Notes for Version 0.5.5<br>
<br>
Our first new version in over 2 years.  Sorely overdue, but chock full of improvements to make it worth the wait.  Calculate how much seed you'll need, copy crops from one plan to another, do a "not" filter, real CSV export, major speed improvements and more.  As always, we are free and open source.  Our previous version has been downloaded over 7000 times.<br>
<br>
<br>
<h2>WARNING</h2>

This software is being released in a "beta" state.  This means that<br>
the software may be finicky or unpredictable.  Please use this version<br>
but do expect some bumps along the way.  <b>Back up your data files frequently!</b>


<h2>Major New Features</h2>


<h3>Seed Order Worksheet</h3>

Generate a 'seed order worksheet' that includes a variety by variety tally of beds, row feet, flats and … drum roll please … SEED NEEDED, based on the current crop plan.  As with all other data, the seed information can be recorded per crop, variety and/or planting and then inherited accordingly.  These stats are then summed up across each planting of a crop or variety based on the size of each planting, then reported on the worksheet as "total units needed".  This worksheet can be exported as a PDF for printing or as a CSV for opening in a spreadsheet.  It's like magic!<br>
<br>
<h3>Copy a crop plan from one year to the next</h3>

You've finished one season's crop plan and now have to manually enter every planting into next year's plan?  NO MORE!  When you create a new plan, you will be given the option to base it on a previous plan.  All of your plantings will be copied over and the "Planned" dates for planting, transplanting and harvest with be updated to the current year.  The "Actual" dates and "Done" checkboxes will be cleared, and each planting will be given a Keyword of <code>from&lt;oldplan&gt;</code> (e.g. - "from2012plan" if you based it on a plan named "2012plan").  If you enter this keyword in the filter or search box, it will show you all of these plantings.  As you update the plantings for this next season, you can remove that keyword from them and they won't show up on that list any more.  Hallelujah!<br>
<br>
<br>
<br>
<h2>Other New and Noteworthy Changes</h2>

<ul><li>Automatically checks for new versions of the software.  Can be disabled in Settings.</li></ul>

<ul><li>The field "Flats to Plant" can now be used to calculate backwards how many row feet and/or beds to plant.  (e.g. - enter 10 flats and it will calculate now many beds or row feet that will plant)</li></ul>

<ul><li>The search box now recognizes "not" searches for terms starting with a minus ("-"). (e.g. - "corn -sweet" will show "popcorn" but not "sweet corn")</li></ul>

<ul><li>Generate weekly GH and Field planting lists for the whole season at one time.  (aka <i>Cavendish</i> mode)  Useful if you use the software for planning but not weekly record keeping.</li></ul>

<ul><li>If you DO use the software for week to week record keeping of completed plantings, clicking the "done" buttons will now save the date you entered and automatically enter it on the next record that you click as being "done".  Useful for checking off several plantings that happened on the same day.</li></ul>

<ul><li>Dates can now have a year added or subtracted to them, just as then can have days or weeks added them, by adding "+1y" or "-1y" to them and saving.  Useful if you did some planning last year and inadvertently got some "2012"s stuck in there.</li></ul>

<ul><li>Hot key to save current entry changed is Alt+Enter for Windows and Linux, Cmd+Enter for Mac.</li></ul>

<ul><li>Sadly, we have had to disable the ability to make changes in the table view and import CSV data.  In fact, export of CSV data isn't even that reliable...</li></ul>

<ul><li><b>INTERNAL CHANGE</b>: Complete under-the-hood rewrite of how data is handled.  This will mean much faster updates when searching and working with your crop plans.  It also means it's now a lot easier to add new features.  This is sort of a MAJOR update, but no one's going to appreciate it as much as I do.  :(</li></ul>

<ul><li><b>INTERNAL CHANGE</b>: Major improvements in startup speed - almost twice as fast to start up!</li></ul>

<ul><li>Many, many, many, many bug fixes (and probably some new bugs, too!)</li></ul>


<h2>Installation</h2>

Please follow installation instructions at:<br>
<br>
<a href='http://code.google.com/p/cropplanning/wiki/SetupAndInstallation'>http://code.google.com/p/cropplanning/wiki/SetupAndInstallation</a>

Briefly: 1) Make sure Java 1.6 or greater is installed, 2) Open the archive or disk image, 3) Copy the enclosed files to your hard drive, 4) double click on the  program file (On Mac: CropPlanning, on Windows: CropPlanning.exe)<br>
<br>
<h2>Using the Program</h2>

There is a brief introduction to the program available at<br>
<br>
<a href='http://code.google.com/p/cropplanning/wiki/ProgramUsageIntroduction'>http://code.google.com/p/cropplanning/wiki/ProgramUsageIntroduction</a>


<h3><a href='.md'>How To Help </a></h3>

Like us on Facebook:<br>
<br>
<blockquote><a href='http://www.facebook.com/CropPlanningSoftware'>http://www.facebook.com/CropPlanningSoftware</a></blockquote>

Communicate!  Send all of your ideas, suggestions, bugs, etc to cropplanning@gmail.com.  If you feel comfortable, submit "issues" (ie, bugs, feature requests, etc) directly through the website at<br>
<br>
<blockquote><a href='http://code.google.com/p/cropplanning/issues/list'>http://code.google.com/p/cropplanning/issues/list</a></blockquote>

Donate!<br>
<br>
<blockquote><a href='https://code.google.com/p/cropplanning/wiki/Donations'>https://code.google.com/p/cropplanning/wiki/Donations</a></blockquote>

Also, just take a look at our HelpWanted page to see if you can help out any other way:<br>
<br>
<blockquote><a href='http://code.google.com/p/cropplanning/wiki/HelpWanted'>http://code.google.com/p/cropplanning/wiki/HelpWanted</a></blockquote>
