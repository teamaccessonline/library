Solution: VPN - Active Directory Authenticated 
======================================================

This solution documents  all the necessary pieces required to setup a basic VPN for use with Active Directory Authentication.  

Objective:
----------

-  Gain an understanding of a basic VPN configuration

-  Gain an initial understanding of Active Directory AAA Objects

Configuration Comments
------------------------

Demo Evironment Components use:
---------------------

Postman Collection
^^^^^^^^^^^^^^^^^^^^
  - vpn.acme.com-ad-create.json
  - vpn.acme.com-ad-delete.json

irules
^^^^^^^^
  - idp_selection.irule

APM Profile(s) 
^^^^^^^^^^^^
  - profile_Common_vpn.acme.com-psp.conf.tar


BIG-IP Versions Tested
^^^^^^^^^^^^^^^^^^^^^^
  - 15.1

BIG-IP Components used:
-----------------

* Virtual Server
 - Client-side SSl Profile
 - Connectivity profile
 - Access Profile
      + Active Directory AAA Object
      + Network Access Resource
      + IPv4 Lease Pool
      + Webtop
      + Webtop Sections
      


Policy Walk-Through
----------------------


1. In this policy a user enters their credentials in the loogon page agent.  
2. Those credentials are collected, stored as the default system session variables of session.logon.last.username and session.logon.last.password.                                
3. The user proceeds down the logon page fallback branch to the AD Auth Agent              
4. The AD Auth Agent validates the the username and password session variables against the configured AD Domain Controller. 
5a.  If successful, the user proceeds down the Successful Branch                             
6a.  The user assigned resourced defined in the Advanced Resource Assign Agent               
7.   The user is granted access via the Allow Terminal                                       
5b.  If unuccessful, the user proceeds down the failback branch                              
6b.  The user is denied access via the Deny Terminal                                         

+----------------------------------------------------------------------------------------------+
| |image001|                                                                                   |     
+----------------------------------------------------------------------------------------------+


Policy Agent Configuration
----------------------------


The Logon Page contains only the default setting                                                                                                                                         
+----------------------------------------------------------------------------------------------+
| |image002|                                                                                   |
+----------------------------------------------------------------------------------------------+


The AD Auth Agent uses a defined the  AD AAA Server object that user will be authenticated against.  All Setting are the default.                                                                                                                                   
+----------------------------------------------------------------------------------------------+
| |image003|                                                                                   |
|                                                                                              |
+----------------------------------------------------------------------------------------------+


The Advanced resource Assign Agent grants a user access to assigned in the screenshot                                                                                                    
+----------------------------------------------------------------------------------------------+
| |image004|                                                                                   |
|                                                                                              |
+----------------------------------------------------------------------------------------------+

Supporting APM Objects
-----------------------

Network Access Resource
~~~~~~~~~~~~~~~~~~~~~~~

The Properties page contains the Caption name **VPN**.  This is the name displayed to a      
user                                                                                                                                                                                     
+----------------------------------------------------------------------------------------------+
| |image005|                                                                                   |
+----------------------------------------------------------------------------------------------+


- The Network Settings tab assigns the **lease pool** of ip addresses that will be used for the VPN                                                                                                                                       
- Split Tunneling is configured to permit only the **10.1.20.0/24 subnet range inside the VPN                                                                                          | 
+----------------------------------------------------------------------------------------------+
| |image006|                                                                                   |
+----------------------------------------------------------------------------------------------+

Lease Pool
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
A single address of **10.1.20.254** is assigned inside the lease pool.                       
                                                                                            
+----------------------------------------------------------------------------------------------+
| |image007|                                                                                   |
+----------------------------------------------------------------------------------------------+

Webtop Sections
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
A single section is configured to display a custom name.                                                                                                                               
+----------------------------------------------------------------------------------------------+
| |image008|                                                                                   |
+----------------------------------------------------------------------------------------------+

Webtop
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- A Full Webtop was defined with modified default settings.                                  
- The Minimize to Tray box was checked to ensure when a user connects to the VPN the Webtop is not displayed                                                                                          
+----------------------------------------------------------------------------------------------+
| |image009|                                                                                   |
+----------------------------------------------------------------------------------------------+


The Policy from a user's perspective
-------------------------------------




.. |image001| image:: media/001.png

.. |image002| image:: media/002.png

.. |image003| image:: media/003.png

.. |image004| image:: media/004.png

.. |image005| image:: media/005.png

.. |image006| image:: media/006.png

.. |image007| image:: media/007.png

.. |image008| image:: media/008.png

.. |image009| image:: media/009.png

   

