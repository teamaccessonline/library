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
^^^^^^^^^

  - idp_selection.irule

APM Profile 
^^^^^^^^^^^^
  - profile_Common_vpn.acme.com-psp.conf.tar


BIG-IP Versions Tested
^^^^^^^^^^^^^^^^^^^^^^
  - 15.1

BIG-IP Components used:
-----------------


Virtual Server
 - Client-side SSl Profile
 - Connectivity profile
 - Access Profile
      - Active Directory AAA Object
      - Network Access Resource
      - IPv4 Lease Pool
      - Webtop



Policy Walk-Through
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

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
| |image004|                                                                                   |
+----------------------------------------------------------------------------------------------+

TASK 2: Name Configuration and define Device Posture  
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------------------------------------------------------------------------------------+
| 1. In the **Configuration Name** dialogue box, enter **agc-app.acme.com**                    |
|                                                                                              |
| 2. Click **Save & Next** at the bottom of the dialogue window.                               |
+----------------------------------------------------------------------------------------------+
| |image005|                                                                                   |
+----------------------------------------------------------------------------------------------+



.. |image001| image:: media/lab1-001.png
   :width: 4.5in
   :height: 0.74in
.. |image002| image:: media/lab1-002.png
   :width: 4.5in
   :height: 3.37in

