  1. Determine SVN revision number to release and then "tag" that revision as the release name:
```
svn cp -m <commit message> -r <rev> <repos>/<module>/trunk <repos>/<module>/tags/<tag name>
```
Omit the `-r <rev>` if tagging HEAD
  1. "Switch to" the tag in Netbeans, clean and build.
  1. Package files in local CropPlanning/trunk/dist:
    * _Mac_: use Jar Bundler to create an App Bundle containing the main class jar and all dependency jars
      * set main class
      * check "Use Mac menubar" (though this seems to not do anything)
      * set JVM to "1.5+"
      * under "Classpath and Files", use "Add" to add JARs in lib folder
      * create bundle named 'CropPlanning'
    * _Windows_: use Lauch4J to create a jar launcher (not a wrapper) the will reside next to the main .jar and includes the ./lib dir in its classpath.
      * set output filename to 'CropPlanning.exe'
      * set the jar file to 'CropPlaning.jar', this should be relative to the location of the above executable
      * check "don't wrap, just launch"
      * under JRE, set min JVM to '1.5.0'
      * Under "Classpath", add the main jar and it should auto-add all of the jars in ./lib
      * if you feel motivated, you can fill out the version information under the "Version Info" tab
  1. Create folder structures for distributed archives:
    * create folder: `CropPlanning`
    * _All Platforms_: include:
      * license (`gpl-3.0.txt`)
      * release notes (see ReleaseNotesTemplate)
    * _Mac_: copy app bundle into `CropPlanning` folder
    * _Windows_: copy exe, main jar and lib directory into `CropPlanning` folder
  1. Create archives such that the user will open the archive and see:
    * _Mac_: the application and other files.  **Use Disk Utility** to create a disk image from the `CropPlanning` folder
    * _Windows_:  a folder `CropPlanning`, which contains the application, jars and other files.  **Right click** on `CropPlanning` folder and select "7-Zip > Add to archive..."
  1. Upload...