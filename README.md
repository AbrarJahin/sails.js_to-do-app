Demo Sails.JS ToDo App
======================

Sails.JS-
https://www.smashingmagazine.com/2015/11/sailing-sails-js-mvc-style-framework-node-js/

Installation-

    sudo npm -g install sails
    sudo npm install -g sails-generate-views-handlebars


Create new App-

    sails new <projectName> --template=handlebars
    cd <projectName>
    npm install

=======================================================

  Usage: sails [command]


  Commands:

    version
    lift|l [options]
    new [options] [path_to_new_app]
    generate
    deploy
    console|c
    www
    debug
    help

  Options:

    -h, --help     output usage information
    -v, --version  output the version number
    --silent
    --verbose
    --silly

====================================


Running the code-

    [sudo] sails lift
    #sudo is optional, is needed if project is stored in root directory


######################################
$ sails lift

info: Starting app...

info: Could not find module: handlebars in path: /home/abrarjahin/Desktop/to_do_app/node_modules
-----------------------------------------------------------------

 Excuse my interruption, but it looks like this app
 does not have a project-wide "migrate" setting configured yet.
 (perhaps this is the first time you're lifting it with models?)

 In short, this setting controls whether/how Sails will attempt to automatically
 rebuild the tables/collections/sets/etc. in your database schema.
 You can read more about the "migrate" setting here:
 http://sailsjs.org/#!/documentation/concepts/ORM/model-settings.html?q=migrate

 In a production environment (NODE_ENV==="production") Sails always uses
 migrate:"safe" to protect inadvertent deletion of your data.
 However during development, you have a few other options for convenience:

 1. safe  - never auto-migrate my database(s). I will do it myself (by hand)
 2. alter - auto-migrate, but attempt to keep my existing data (experimental)
 3. drop  - wipe/drop ALL my data and rebuild models every time I lift Sails

What would you like Sails to do?

info: To skip this prompt in the future, set `sails.config.models.migrate`.
info: Usually this is done in a config file (e.g. `config/models.js`),
info: or as an override (e.g. `sails lift --models.migrate='alter').

warn: ** DO NOT CHOOSE "2" or "3" IF YOU ARE WORKING WITH PRODUCTION DATA **

prompt: ?:  1

 Temporarily using `sails.config.models.migrate="safe"...
 (press CTRL+C to cancel-- continuing lift automatically in 0.5 seconds...)

info:
info:                .-..-.
info:
info:    Sails              <|    .-..-.
info:    v0.12.3             |\
info:                       /|.\
info:                      / || \
info:                    ,'  |'  \
info:                 .-'.-==|/_--'
info:                 `--'-------'
info:    __---___--___---___--___---___--___
info:  ____---___--___---___--___---___--___-__
info:
info: Server lifted in `/home/abrarjahin/Desktop/to_do_app`
info: To see your app, visit http://localhost:1337
info: To shut down Sails, press <CTRL> + C at any time.

debug: -------------------------------------------------------
debug: :: Wed Apr 20 2016 11:25:51 GMT+0600 (BDT)

debug: Environment : development
debug: Port        : 1337
debug: -------------------------------------------------------

######################################



Creating a model-

    sails generate model person

Create a Controller

    sails generate controller person

Create model and controller together with API-

    sails generate api person

Detail-
http://sailsjs.org/documentation/reference/blueprint-api

