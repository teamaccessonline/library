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

+----------------------------------------------------------------------------------------------+
|  1.   In this policy a user enters their credentials in the loogon page agent.               |
|  2.   Those credentials are collected, stored as the default system session variables of     | 
|       session.logon.last.username and session.logon.last.password.                           |
|  3.   The user proceeds down the logon page fallback branch to the AD Auth Agent             |
|  4.   The AD Auth Agent validates the the username and password session variables against    |
|       the configured AD Domain Controller.                                                   |
|  5a.  If successful, the user proceeds down the Successful Branch                            |
|  6a. The user assigned resourced defined in the Advanced Resource Assign Agent               |
|  7.  The user is granted access via the Allow Terminal                                       |
|  5b. If unuccessful, the user proceeds down the failback branch                              |
|  6b. The user is denied access via the Deny Terminal                                         |
|                                                                                              |
|                                                                                              |                             
+----------------------------------------------------------------------------------------------+
| |image001|                                                                                   |
+----------------------------------------------------------------------------------------------+

+----------------------------------------------------------------------------------------------+
| 4. The Logon Page contains only the default setting                                          |
|                                                                                              |
|                                                                                              | 
+----------------------------------------------------------------------------------------------+
| |image002|                                                                                   |
+----------------------------------------------------------------------------------------------+

+----------------------------------------------------------------------------------------------+
| 5. The AD Auth Agent uses a defined the  AD AAA Server object that user will be              |
|    authenticated against.  All Setting are the default.                                      |
|                                                                                              |
+----------------------------------------------------------------------------------------------+
| |image003|                                                                                   |
|                                                                                              |
+----------------------------------------------------------------------------------------------+

+----------------------------------------------------------------------------------------------+
| 5. The Advanced resource Assign Agent defines the resources     |
|                                                                                              |
| 6. Scroll through and review the remaining element of the dialogue box to the bottom of the  |
|                                                                                              |
|    screen and click "Next"                                                                   |
+----------------------------------------------------------------------------------------------+
| |image004|                                                                                   |
|                                                                                              |
+----------------------------------------------------------------------------------------------+

Supporting APM Objects: Network Access Resource
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------------------------------------------------------------------------------------+
| 1. In the **Configuration Name** dialogue box, enter **agc-app.acme.com**                    |
|                                                                                              |
| 2. Click **Save & Next** at the bottom of the dialogue window.                               |
+----------------------------------------------------------------------------------------------+
| |image005|                                                                                   |
+----------------------------------------------------------------------------------------------+

+----------------------------------------------------------------------------------------------+
| 1. In the **Configuration Name** dialogue box, enter **agc-app.acme.com**                    |
|                                                                                              |
| 2. Click **Save & Next** at the bottom of the dialogue window.                               |
+----------------------------------------------------------------------------------------------+
| |image006|                                                                                   |
+----------------------------------------------------------------------------------------------+

Supporting APM Objects: Lease Pool
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------------------------------------------------------------------------------------+
| 1. In the **Configuration Name** dialogue box, enter **agc-app.acme.com**                    |
|                                                                                              |
| 2. Click **Save & Next** at the bottom of the dialogue window.                               |
+----------------------------------------------------------------------------------------------+
| |image007|                                                                                   |
+----------------------------------------------------------------------------------------------+

Supporting APM Objects: Webtop Sections
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+----------------------------------------------------------------------------------------------+
| 1. In the **Configuration Name** dialogue box, enter **agc-app.acme.com**                    |
|                                                                                              |
| 2. Click **Save & Next** at the bottom of the dialogue window.                               |
+----------------------------------------------------------------------------------------------+
| |image008|                                                                                   |
+----------------------------------------------------------------------------------------------+

Supporting APM Objects: Webtop
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+----------------------------------------------------------------------------------------------+
| 1. In the **Configuration Name** dialogue box, enter **agc-app.acme.com**                    |
|                                                                                              |
| 2. Click **Save & Next** at the bottom of the dialogue window.                               |
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

   

