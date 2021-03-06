# ZooKeeper

###  by Jonas Sundstrom

#### copyleft 2004, 2005, Public Domain

![screenshot](screenshot.png)

ZooKeeper is a glue application (or frontend) that lets you 
specify a shell command or script to be executed on a set
of files.
	
It's designed to be cloned and customized.

### How to install
Simply run `make`, and copy the app ZooKeeper into `~/config/non-packaged/add-ons/Tracker`.
To run examples, copy the binary to the same folder as the "Build Sample Apps.sh"
and run `sh "Build Sample Apps.sh"`. The samples should be in the parent directory.

### How to use
1) Open ZooKeeper.
2) Set the command.
`$zkfiles` is the file argument for your command.
I also recommend checking off "In Terminal" and "Keep Open".
3) Quit ZooKeeper.
4) Choose any file you want to open with ZooKeeper.
Right click on the file, go to "Open with...", and select ZooKeeper.
5) ZooKeeper should automatically execute the command on the files
you selected.

### Something went wrong!
If you receive an alert "The command failed to run":
1) Open ZooKeeper
2) Toggle "In Terminal" and "Keep Open".
3) Re-run ZooKeeper, and you should get a terminal output of the error.


### Additional Information
When launched without any arguments or files ZooKeeper
provides a window where you add a shell command, a 
working directory, and other preferences. These settings
are stored with the executable making it possible to keep
multiple copies of ZooKeeper for different purposes.
	
Ways to use ZooKeeper:
* Filedrops on a ZooKeeper window
* Filedrops on a ZooKeeper icon
* Using Tracker's Open With... menu
* As the Preferred Application of a filetype
* As Tracker add-ons
	
If you want ZooKeeper to do anything useful at all you 
need to supply a shell command, including the $zkfiles
variable which will be substituted by the set of files 
given to ZooKeeper by any of its launch mechanisms.

There's no need to add extra quotation marks around 
$zkfiles and $zkfolder. ZooKeeper does the quoting for you.

Example:
Dropping 'wow.ps' on a ZooKeeper 
where the command is set to
`~/config/non-packaged/bin/psviewer` $zkfiles
Your file 'wow.ps' will open in psviewer
	
As a Tracker add-on, ZooKeeper also provides the
$zkfolder variable, should you ever need it.

It's best to give each copy of ZooKeeper a unique name, 
describing its purpose, and a unique Application Signature,
to help yourself and Haiku tell them apart.

