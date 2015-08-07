## Access to Source Code ##

### Browse Source Code ###

  * [Browse the source code](http://code.google.com/p/cropplanning/source/browse/)
  * [View recent changes to the source code](http://code.google.com/p/cropplanning/source/list)

### Download Source Code ###
_(aka check out source code)_

  * You will need [SVN](http://subversion.tigris.org/) to access the code.
  * For general **checkout**, the repository root path is `http://cropplanning.googlecode.com/svn`
  * For write access, use the same URL except with **`https`** instead of **`http`**.
  * You will have to checkout _each_ module from the repository.  The URL would be `http://cropplanning.googlecode.com/svn/<module-name>/trunk` where `<module-name>` is the _case sensitive_ name from the table below.





## Introduction ##

The project has been developed under Netbeans, though it does not require Netbeans to run.  The source is structured as a number of "modules", many of which of which depend upon each other.

### Module List ###

| **Module Name** | **Description** |
|:----------------|:----------------|
| CPS-CVS [_sic_] | Provides incomplete access to CSV files for data storage.  Currently only for import and export. |
| CPS-CropDB      | A front-end for creating and modifying entries in the "CropDB" |
| CPS-CropPlans   | A front-end for creating and modifying crop plans.  Also provides some at-a-glance statistics. |
| CPS-HSQLDB      | Implements a database "back end" for data storage. |
| CPS-Spec        | The core APIs and utility classes for the program. |
| CPS-SwingUI     | A tabbed UI implemented in Swing. |
| CPS-TODOLists   | A simple planting list generator (w/ UI) providing PDF export. |
| CropPlanning    | The core or driver of the program.  Very small and simple. |
| TableUtil       | Some utility classes relating to tables. |



## Setup ##



### Netbeans ###

> If Netbeans is setup properly w/ SVN, you should be able to connect to the repository, select all of the "modules" and check them all out at once.  The trunk branch of each module contains Netbeans project files which can be opened in the Netbeans IDE.  You will probably have to fix some dependencies since I'm still trying to figure out how NB handles all of that and some (perhaps many) of the settings that **I** use might not work for you.

### Module Dependencies ###

> Because of the modular nature in which we've designed this program, many of the modules depend on other modules.  If you're not developing in Netbeans, you need to make sure that these modules all appear in your CLASSPATH.  If you are using Netbeans, these dependencies need to be listed in the "libraries" section of each project's properties.  (Right click on the project, select "properties", then "libraries".)

**Notes:** All modules depend upon **CPS-Spec** for the core APIs.  The **CropPlanning** module depends upon **CPS-Spec** as well as _all other modules_.  This is sort of a Netbeans funkiness: all dependencies are copied to the `dist/` folder upon build, so by listing all of the modules here (even though the **CropPlanning** module doesn't technically depend upon all of them) everything will sort of shake out politely upon build and put all of the requisite modules and libraries in the right place.

**Note:** After checkout, module **CropPlanning** must be set as the main project in Netbeans.

| **Module Name** | **Module Dependencies** | **Library Deps** |
|:----------------|:------------------------|:-----------------|
| CPS-CVS [_sic_] | CPS-Spec                | JavaCSV          |
| CPS-CropDB      | CPS-Spec and CPS-CVS    | _none_           |
| CPS-CropPlans   | CPS-Spec and CPS-CVS    | _none_           |
| CPS-HSQLDB      | TableUtil, CPS-Spec and CPS-CVS | HSQLDB and SwingX-Wizard |
| CPS-Spec        | _none_                  | JCalendar, SwingX and SwingX-Wizard |
| CPS-SwingUI     | CPS-Spec                | SwingX           |
| CPS-TODOLists   | CPS-Spec                | iText and JCalendar |
| CropPlanning    | **_all_**               | **_all_**        |
| TableUtil       | _none_                  | _none_           |



### External Libraries ###

| **Lib Name** | **Version** | **URL** | **Description** |
|:-------------|:------------|:--------|:----------------|
| JavaCSV      | 2.0         | http://sourceforge.net/projects/javacsv/ | Library for reading and writing CSV text. |
| HSQLDB       | 1.8.10      | http://hsqldb.org/ | Very fast, embeddable SQL db. |
| iText        | 2.0.8       | http://www.lowagie.com/iText/ | Library for creating PDF files. |
| JCalendar    | 1.3.2       | http://www.toedter.com/en/jcalendar/ | Calendar widgets and date choosers. |
| JFreeChart   | _n/a_       | http://www.jfree.org/jfreechart/ | Robust charting library.  (Not yet used in program.) |
| SwingX       | 0.9.2       | http://swinglabs.org/ | Numerous new, refined and enhanced Swing components. |
| SwingX-Wizard | _n/a_       | https://wizard.dev.java.net/ | Simple, full featured Wizard API |

**Note:** When you download these libraries and set them up in NetBeans (menu: _Tools > Libraries_), you can name them anything you want.  However, if you name them as they appear in the above table, you might not get hassled by NetBeans to have to resolve broken dependencies.

### Ant Libraries ###

The following libraries shouldn't be needed for day to day development, but will be needed for anyone who wants use the custom Ant tasks in the **CropPlanning** module to generate distributable disk images and zip archives.

Once downloaded and unpacked, add the files `jarbundler-<version>.jar` and `launch4j.jar` to the Ant classpath in the Netbeans Preferences, under _Miscellaneous > Ant_.

| **Lib Name** | **Version** | **URL** | **Description** |
|:-------------|:------------|:--------|:----------------|
| JarBundler   | 2.1.0       | http://informagen.com/JarBundler/ | Creates Mac application bundles right from Ant!! |
| Launch4J     | 3.0.1       | http://launch4j.sourceforge.net/ | Wraps Java apps in a Windows executable |


### Utilities/Misc ###

  * Netbeans (http://www.netbeans.org/) - Unbelievably useful IDE for Java, among others.
  * Subversion (aka SVN) (http://subversion.tigris.org/) - Version control software.  Needed to work with the code for this project.