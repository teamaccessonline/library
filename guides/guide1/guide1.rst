Solution: VPN - Active Directory Authenticated 
======================================================

This solution documents  all the necessary pieces required to setup a basic VPN for use with Active Directory Authentication.  

Objective:
----------

-  Gain an understanding of a basic VPN configuration

-  Gain an initial understanding of Active Directory AAA Objects

Demo Evironment Components use:
---------------------

Postman Collection
^^^^^^^^^^^^^^^^^^^^
  - vpn.acme.com-ad-create.json
  - vpn.acme.com-ad-delete.json

irules
^^^^^^^^
  - idp_selection.irule

APM Profile 
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
      
Configuration Comments
------------------------

Policy Walk-Through
----------------------

+----------------------------------------------------------------------------------------------+
| 1. Login to your provided lab Virtual Edition: **bigp1.f5lab.local**                         |
|                                                                                              |
| 2. Navigate to:  **Access -> Guided Configuration**                                          |
|                                                                                              |
| 3. Click the **Zero Trust** graphic as shown.                                                |
+----------------------------------------------------------------------------------------------+
| |image001|                                                                                   |
+----------------------------------------------------------------------------------------------+

+----------------------------------------------------------------------------------------------+
| 4. Click on the **Identity Aware Proxy**  dialogue box click under **Zero Trust**            |
|                                                                                              |
|    in the navigation as shown.                                                               | 
+----------------------------------------------------------------------------------------------+
| |image002|                                                                                   |
+----------------------------------------------------------------------------------------------+

+----------------------------------------------------------------------------------------------+
| 5. Review the **Identity Aware Proxy Application** configuration example presented.          |
|                                                                                              |
| 6. Scroll through and review the remaining element of the dialogue box to the bottom of the  |
|                                                                                              |
|    screen and click "Next"                                                                   |
+----------------------------------------------------------------------------------------------+
| |image003|                                                                                   |
|                                                                                              |
+----------------------------------------------------------------------------------------------+

+----------------------------------------------------------------------------------------------+
| 5. Review the **Identity Aware Proxy Application** configuration example presented.          |
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



.. |image001| image:: media/001.png

.. |image002| image:: media/002.png

.. |image003| image:: media/003.png

.. |image004| image:: media/004.png

.. |image005| image:: media/005.png

.. |image006| image:: media/006.png

.. |image007| image:: media/007.png

.. |image008| image:: media/008.png

.. |image009| image:: media/009.png

   

