How to contribute
==================

Welcome
-------

If you are reading this page, I would like to start off by saying "Thank, You".  You will hopefully one of many individuals that have decided that contributing to this framework is the right thing to do for F5'ers, Partners, and customers going forward.  This repo was designed as a way for everyone that configures the APM product to share their solutions with the rest of the community.  

First and foremost please access each of the five hyperlinks listed below prior to getting started.  This will save you time in the long run because a number of templates are available inside the repo.  If you deviate from the naming conventions it will cause you extra work and force you edit the Postman collections more than you may need to. 



.. toctree::
   :maxdepth: 1
   :caption: Contents:
   :glob:
 
 
   c_postman.rst
   c_irules.rst
   c_guides.rst
   c_policies.rst
   c_naming.rst
   :ref:`get_to_know`

.. _Pushing_content:

Pushing Content to Github
---------------------------

#. Open git client
#. Type cd c:\\labfiles\\solutions
#. Perform "git pull" to get latest repo
#. Copy files to their relevent folders on c:\\labfiles\\solutions
     - Postman Collections - A Create and delete collections
     - iRules
     - Solution guide
     - APM Policy
#. Return to git client
#. Set your username "git config user.name [your username]"
#. Verity username was changed "git config user.name"
#. Set email address "git config user.email "Your Email Address"
#. Verify email address "git config user.email"
#. Create a new branch by typing git checkout -b [name of your new branch]
#. Push new branch to github "git push origin [name of your new branch]
#. Git add .
#. Git commit -a  -m [commit notes]
#. Git push -u origin [name of your new branch]
#. F5 SMEs will validate the documentation and test the configuration. If a changes are required they will annotated in the     branch.  
#. Once branch is merged in to master you can do the following
#. Git checkout master
#. Git pull
#. Git branch -d [name of your new branch]





