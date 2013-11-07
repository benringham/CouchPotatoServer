* Update your ports tree `sudo portsnap fetch update`
* Install Python 2.6+ [lang/python](http://www.freshports.org/lang/python) with `cd /usr/ports/lang/python; sudo make install clean`
* Install port [databases/py-sqlite3](http://www.freshports.org/databases/py-sqlite3) with `cd /usr/ports/databases/py-sqlite3; sudo make install clean`
* Add a symlink to 'python2' `sudo ln -s /usr/local/bin/python /usr/local/bin/python2`
* Install port [ftp/libcurl](http://www.freshports.org/ftp/libcurl) with `cd /usr/ports/ftp/fpc-libcurl; sudo make install clean`
* Install port [ftp/curl](http://www.freshports.org/ftp/bcurl), deselect 'Asynchronous DNS resolution via c-ares' when prompted as part of config `cd /usr/ports/ftp/fpc-libcurl; sudo make install clean`
* Install port [textproc/docbook-xml-450](http://www.freshports.org/textproc/docbook-xml-450) with `cd /usr/ports/textproc/docbook-xml-450; sudo make install clean`
* Install port [GIT](http://git-scm.com/) with `cd /usr/ports/devel/git; sudo make install clean`
* 'cd' to the folder of your choosing.
* Run `git clone https://github.com/RuudBurger/CouchPotatoServer.git`
* Then run `sudo python CouchPotatoServer/CouchPotato.py` to start for the first time
* To run on boot copy the init script. `sudo cp CouchPotatoServer/init/freebsd /etc/rc.d/couchpotato`
* Change the paths inside the init script. `sudo vim /etc/init.d/couchpotato`
* Make init script executable. `sudo chmod +x /etc/rc.d/couchpotato`
* Add init to startup. `sudo echo 'couchpotato_enable="YES"' >> /etc/rc.conf`
* Open your browser and go to: `http://server:5050/`
