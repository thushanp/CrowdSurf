# CrowdSurf
An online concert ticket-price tracker using SeatGeek and Google Charts API. Currently designing an algorithm based on Twitter API/social media hype to predict future prices.


Documentation:



/---------	/-----------
| -------	| ---------
| |		| |_______						 
| |rowd		\________ \urf	    		for Windows 10 (Anniversary Edition)	
| |		         | |					  
| -------	 --------/ |
\---------	----------/					-by Thushan Puhalendran and Sean Hughes, 2016
________________________________________________________________________________________________________________
----____----____----____----____----____----____----____----____----____----____----____----____----____----____
________________________________________________________________________________________________________________

CrowdSurf is a web application which tracks concert ticket prices for events around the world. In writing this
documentation, we have decided that it is best divided two distinct perspectives which reflect the dual nature
of our platform.
________________________________________________________________________________________________________________
----____----____----____----____----____----____----____----____----____----____----____----____----____----____
________________________________________________________________________________________________________________
Perspective I: DEVELOPER
This section of the documentation is relevant for those who wish to use the zipped code files downloaded from 
GitHub (or submitted to CS50) themselves in order to run a locally-hosted version of CrowdSurf on their computer.
This is thus the perspective of the CS50 grader.

Perspective II: USER
This section of the documentation is relevant for those who wish to simply utilise the already-running version
of CrowdSurf hosted online by our server at http://ec2-35-164-125-116.us-west-2.compute.amazonaws.com/ This 
version does not require the installation sequence needed for Perspective I. This would thus be the perspective 
of all of CrowdSurf's userbase.
________________________________________________________________________________________________________________
----____----____----____----____----____----____----____----____----____----____----____----____----____----____
________________________________________________________________________________________________________________

Perspective I: DEVELOPER -

STEP 1:
First, extract all files from Crowd-Surf.zip to your desired folder

STEP 2:
In order to run CrowdSurf from the command line, you must have access to the linux bash shell on Windows 10,
which became available with the Windows 10 Anniversary Update. If you do not currently have 'Bash on Ubuntu
on Windows' installed, it is possible to find multiple guides online to do so before proceeding, such as at
http://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/

STEP 3:
Once the bash shell is working, we can use it to install the necessary Linux Software to run CrowdSurf.
Firstly, use console commands inside the bash shell to navigate to the folder you have extracted CrowdSurf to
(for example: 'cd /mnt/c/Users/thushan/Documents/Crowd-Surf'). Now we must install the following packages by
typing the commands in parentheses into bash. This is the installation sequence:

Flask (sudo pip install flask)

Flask-Session (sudo pip install flask-session)

passlib (sudo pip install passlib)

SQLAlchemy (sudo pip install SQLAlchemy)

Jinja (sudo pip install jinja)


anyjson (sudo apt-get install python-anyjson)

kombu (sudo apt-get install python-kombu)


beautiful soup (sudo apt-get install python3-bs4)

npm 
bower
typehead ("ln -s /usr/bin/nodejs /usr/bin/node" if that problem arises)

STEP 4:
Now, to run the program, simply type 'python application.py' into bash. If all packages have been correctly
installed, the console will output some variation of ' * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
where the precise http:// address may vary according to your computer. Type this address into your internet
browser to access your locally-hosted version of CrowdSurf. This version's database will already be populated
with some data collected on several concerts for you to test out and explore.

STEP 5:
To continue to grab new data to populate your database dynamically, then open up another bash window and
navigate once more to the Crowd-Surf folder using it. Then run 'python data_grabber.py'. This function will run
through all of the saved concerts and periodically add new data to the database. This function can be left
running constantly in the background to continue to populate your database for however long you see fit. When
you would like to stop collecting data, exit the new bash window itself directly (do not attempt to Ctrl + C
the function, as this may reset the database).

STEP 6:
You can now proceed to Step 3 of Perspective II if you would like a guide to exploring some of the features
of CrowdSurf on your locally-hosted copy of the code.

________________________________________________________________________________________________________________
----____----____----____----____----____----____----____----____----____----____----____----____----____----____
________________________________________________________________________________________________________________

Perspective II: USER -

STEP 1:
Open the online version of CrowdSurf at http://ec2-35-164-125-116.us-west-2.compute.amazonaws.com/ in a browser

STEP 2:
Test out some features!
	i.	Click All Concerts to view all the concerts that are currently being tracked. You can click on
		a specific concert to be taken to that concert's page
	ii.	Click Add Concert to be able to search for a new concert you are interested in (remember to
		press enter to send your query) and add a new concert to be tracked.
	iii.	Search for a concert to be taken to its specific concert page (uses an autocomplete function to
		draw on concerts currently in the database).
	iv. 	Go to the About section of the splashpage to read an abstract on some of CrowdSurf's
		functionality.
	v.	Go to the Contact feature to be given directions to contact the developers Thushan and Sean
	vi.	On a given concert page there is a great deal of information available such as the lowest 
		price of standard tickets, the most recent price fluxes - changes due to ticket providers
		deciding to reprice, bring more tickets online or selling out, the highest price of the standard
		ticket prices, starting volumes of tickets when CrowdSurf first began tracking the concert, and 
		current outstanding volumes of tickets
	vii.	Also on the concert page you will notice a series of charts which track prices and volumes of
		charts. These update dynamically every 10-15 minutes (staggered so as not to overload the API)

STEP 3:
Share it! Anyone can add any concert they wish to the database to track, and thus the web application becomes
more and more useful and powerful as its user base grows and adds more concerts earlier in their ticketing
cycles. As the app grows, so to does the user experience.
