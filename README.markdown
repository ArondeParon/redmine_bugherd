BugHerd for Redmine
===================

Introduction
------------

### What's this?

BugHerd is the world's simplest bug tracker for websites. Because it's totally cool and plays well with other cool applications, it integrates with Redmine but requires this plugin to be installed.

If you have been asked to install this by your colleague, you may not have seen BugHerd yet and might want to check it out: http://www.bugherd.com

### What does it do?

This plugin enables new APIs for use by BugHerd's server to update issues, and has the ability to call BugHerd back when an issue changes.

### Is it secure?

Yes, all APIs defined by this plug-in that enable information to be passed in and out require that an administrator's API key is used to access them.

Installation
------------

To (re)install the BugHerd Redmine plugin, go to the base directory of your Redmine instance on your server:

> script/plugin install git://github.com/bugherd/redmine_bugherd.git --force
  
Reload your Redmine instance. If you use Passenger:

> touch tmp/restart.txt

Installation can be verified by visiting:

> http://redmine.example.com/bugherd/plugin_version

This should display the version of this plugin.

Setup
-----

Enable APIs:

1. Go to: Administration > Settings
2. Open the "Authentication" tab
3. Tick "Enable REST web service"
4. Click Save

Create a Project Custom Field called "BugHerd Project Key":

1. Go to Administration > Custom Fields
2. Open the "Projects" tab
3. Select "New custom field"
4. Complete these fields:
   - Name: BugHerd Project Key
   - *Untick* "Visible" (to ensure the value is not seen by anyone but the project managers)
5. Click Save

Your Redmine instance is now ready to be integrated with BugHerd.

More info
---------

http://www.redmine.org/plugins/redmine_bugherd