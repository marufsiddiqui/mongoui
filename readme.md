# MongoUI

MongoUI (mongoui) is a web browser admin interface for MongoDB. Currently a standalone tool (run as an app locally or on your server); middleware later.

## Branches

* Master — major releases, main branch
* Develop — current development branch (make your pull requests here)


## Why

Tired of typing `db.users.findOne({_id:ObjectId(...)})` just to look up data structure. Even more typing to modify the data. Can't find Node.js implementaton (not true any more, there is [exprss-mongo](https://github.com/andzdroid/mongo-express)).

## Screenshots


Here's a one and a half minute **video** that shows filtering, editing, and switching collections:

[![mongoui rocks!](http://img.youtube.com/vi/l8Rfpow0f9A/0.jpg)](http://www.youtube.com/watch?v=l8Rfpow0f9A)


Select a database from the local server (can be remote server):

![](https://raw.githubusercontent.com/azat-co/mongoui/master/docs/database-select.png)

Select a collection from the dropdown menu:
![](https://raw.githubusercontent.com/azat-co/mongoui/master/docs/collection-select.png)

Collection view with a single element (if there's only one element, it can be edited):

![](https://raw.githubusercontent.com/azat-co/mongoui/master/docs/collection-view.png)

Edit an item (if there's only one element, it can be edited):

![](https://raw.githubusercontent.com/azat-co/mongoui/master/docs/collection-edit.png)

Editing text property (if there's only one element, it can be edited):

![](https://raw.githubusercontent.com/azat-co/mongoui/master/docs/text-edit.png)

Server logs (real-time updates as you type):

![](https://raw.githubusercontent.com/azat-co/mongoui/master/docs/text-edit-server.png)

Filter/find based on property(ies):

![](https://raw.githubusercontent.com/azat-co/mongoui/master/docs/filter.png)

## How to Use

### Installation

```bash
git clone git@github.com:azat-co/mongoui
```

or

```bash
git clone https://github.com/azat-co/mongoui.git
```

or

```
curl -O https://github.com/azat-co/mongoui/archive/master.zip
```

or

```
wget https://github.com/azat-co/mongoui/archive/master.zip
unzip master.zip
cd mongoui-master
```

or

```bash
mkdir node_modules
npm install mongoui
cd node_modules/mongoui
```

### Configs

Copy `config_default.json` file as `config.json`:

  $ cp config_default.json config.json

Modify as needed (remote databases should work just fine!).


### Running the app

Assuming that MongoDB is running (`$ mongod`), to start the server run:

  $ node .

or:

  $ node index.js

or

```bash
$ node index
```


### Using

Open <http://localhost:3000/> in your favorite browser. If you use Chrome, there is a nice extension for viewing raw json: Chrome extension.

Optional: Download and install [JSONView Chrome extension](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc) to view JSON in a human readable format.

## Contributors

Via `git shortlog -s -n`:

    61  Azat Mardanov
    14  cultofmetatron
     1  Jan Carlo Viray



## TODO

The list is in the GitHub Issues.

## Contributing


Pull requests are always welcome as long as an accompanying test case is
associated.

This project is configured to use [git
flow](https://github.com/nvie/gitflow/) and the following conventions
are used:

* ``develop`` - represents current active development and can possibly be
  unstable.

* ``master`` - pristine copy of repository, represents the currently
  stable release found in the npm index.

* ``feature/**`` - represents a new feature being worked on

If you wish to contribute, the only requirement is to:

- branch a new feature branch from develop (if you're working on an
  issue, prefix it with the issue number)
- make the changes, with accompanying test cases
- issue a pull request against develop branch

Although I use git flow and prefix feature branches with "feature/" I
don't require this for pull requests... all I care is that the feature
branch name makes sense.

Pulls requests against master or pull requests branched from master will
be rejected.

#### Examples

Examples of good branch names:

* 12-amd-support
* feature/12-amd-support


### Running Tests

In order to run the tests which are in `test` folder, you will need:

* Node.js
* NPM

With those installed, running `npm install` and ''npm test'' will run the tests.


## Non-node.js alternatives

* Mac OS X app: [MongoHub](http://mongohub.todayclose.com/)
* .NET based app: MongoVUE](http://www.mongovue.com/)
