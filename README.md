# dev-emoncms
Script to install emonCMS from git for development purposes

    git clone https://github.com/pb66/dev-emoncms.git ~/dev-emoncms && ~/dev-emoncms/install

###Notes
    
- Tested on "clean" install of raspbian (2014-12-24-wheezy-raspbian.img)
- updates and upgrades raspbian first
- installs and configures LAMP
- installs all emoncms dependencies
- installs all data files to a *target* location (currently hard-coded to ~/emonData)
- To install to a seperate partition mount that partion as *target* first.
- emoncms is used as emoncms mySQL database username
- a 32char UUID is created and used as emoncms mySQL database password
- settings.php is updated with data location, username and password.
- installs and configures UFW (Uncomplicated firewall)

###Important
To be able to install "non-interactively" mysql is installed **without** a root password set up, therefore immediately after running this install you should set-up a root password for mySQL as this is a security risk if left as it is.

###Todo
- enable *target* data directory to be specified on the command line.
- automate setting the mySQL root password at end of install
- look at making it more flexible about existing installs and data.
- add clean-up commands (~/dev-emoncms can be deleted after install)




