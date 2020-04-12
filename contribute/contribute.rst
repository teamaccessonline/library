How to contribute
==================

Welcome
-------

The guides located on this page are designed to provide an overview of a working example on a topic.  

If a given topic is not highlighted currently on this page or something is incorrectly documented , please open an issue on Github.  We will do our best to prioritize the development of the content based on demand.  These documents are maintained by the APM SME's at F5, please do not open support cases regarding issues.

Pushing Content to Github
---------------------------

	1. Open git client
	2. Type cd c:/labfiles/ls
	3. solutions
	4. Perform "git pull" to get latest repo
	5. Copy files to their relevent folders on c:\labfiles\solutions
		a. Postman Collections - Create and delete collections
		b. Irules
		c. Solution guide
		d. APM Policy
		
	6. Return to git client
	7. Set your username "git config user.name [your username] "
	8. Verity username was changed "git config user.name"
	9. Set email address "git config user.email "Your Email Address"
	10. Verify email address "git config user.email"
	11. Create a new branch by typing git checkout -b [name of your new branch]
	12. Push new branch to github "git push origin [name of your new branch]
	13. Git add .
	14. Git commit -a  -m [commit notes]
	15. Git push -u origin [name of your new branch]
	16. F5 SMEs will validate the documentation and test the configuration. If a changes are required they will annotated in        the branch.  
	17. Once branch is merged in to master you can do the following
	18. Git checkout master
	19. Git pull
	20. Git branch -d [name of your new branch]



.. toctree::
   :maxdepth: 1
   :caption: Contents:
   :glob:
   
   c_postman.rst
   c_irules.rst
   c_guide.rst
   c_policy.rst



