How to contribute
==================

Welcome
-------

The guides located on this page are designed to provide an overview of a working example on a topic.  

If a given topic is not highlighted currently on this page or something is incorrectly documented , please open an issue on Github.  We will do our best to prioritize the development of the content based on demand.  These documents are maintained by the APM SME's at F5, please do not open support cases regarding issues.

.. toctree::
   :maxdepth: 1
   :caption: Contents:
   :glob:
   
   c_postman.rst
   c_irules.rst
   c_guides.rst
   c_policies.rst


.. _Pushing_content:

Pushing Content to Github
---------------------------

#. Open git client
#. Type cd c:/labfiles/solutions
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





