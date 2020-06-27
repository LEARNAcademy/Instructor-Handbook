# Provisioning Machines New Macbooks for Remote Classes

**Initial Setup**
- Don't add any external connections (e.g. email/fingerprint id, disable Siri)
- Create a new account
- Log in: LEARN Academy
- Password: SDlearn123
- Hint: classroom login
- Remove all extra apps from the doc
- Open Safari and go to `homebrew.sh`
- Open terminal
- Keep terminal in doc
- Install homebrew
- Open Notes and add the computer information for login and password along with a fun, inspirational message
- Close Safari and remove from the doc
- $ brew install git
- install any OS updates
- Turn on battery percent icon
- Turn off keeping extra apps in the doc, system preferences >> dock >> uncheck last item

**Provisions**
- clone provision repo from LEARN into the root directory
- $ git clone https://github.com/LEARNAcademy/provision.git
- Note: if you are prompted for a password, the path is incorrect
- $ brew bundle --file ~/provision/Brewfile
- open all tapped apps and add to the doc
- Chrome - disable autofill for payment and addresses
- Postman - skip the sign up with the link at the bottom
- Text editors - uncheck the welcome menu option

**Ruby and Rails**
- install RVM
```
For installing RVM with default Ruby and Rails in one command, run:
$ \curl -sSL https://get.rvm.io | bash -s stable --rails
```
- It is typical that it will fail the first time, run the gpg command, then the curl command again
- If that fails, follow the terminal instructions
- quit and open terminal
- $ rvm -v
- This command should return a version number
- $ rvm install 2.7.1 (or latest Ruby version)
- $ ruby -v
- $ gem install rails
- $ rails -v

**Countries DB**
- $ brew services start postgresql
- $ createdb
- $ cd provision
$ cp countries.sql ~/Desktop/countries.sql
$ psql -c "create database countries"
$ psql countries < ~/Desktop/countries.sql

**PGAdmin**
- passord: SDlearn123
- Object -->> create, server
- General >> Name: learnacademy
- Connection >>
- Host name: 127.0.01
- Username: learnacademy
- Password: SDlearn123, save password
- The server dropdown menu should have a local tab with the databases
- Tools >> query tools
- Run a test query: `SELECT * FROM country`
- Play button
- Shut down server via elephant icon

**Test Apps**
- Create a react app and fire up the server
- Delete the app
- Create a rails app and a database
- Drop the database and delete the app

**Finishing Touches**
- Clear the terminal
- Delete browser history
