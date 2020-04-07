Solution: VPN - Active Directory Authenticated 
======================================================

This solution documents  all the necessary pieces required to setup a basic VPN for use with Active Directory Authentication.  

Objective:
----------

-  Gain an understanding of a basic VPN configuration

-  Gain an initial understanding of Active Directory AAA Objects

Supporting Components:
-----------------

-  Virtual Server
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
.. |image003| image:: media/lab1-003.png
   :width: 4.5in
   :height: 3.38in
.. |image004| image:: media/lab1-004.png
   :width: 4.5in
   :height: 0.73in
.. |image005| image:: media/lab1-005.png
   :width: 4.5in
   :height: 3.37in
.. |image006| image:: media/lab1-006.png
   :width: 4.5in
   :height: 1.15in
.. |image007| image:: media/lab1-007.png
   :width: 4.5in
   :height: 2.28in
.. |image008| image:: media/lab1-008.png
   :width: 4.5in
   :height: 0.96in
.. |image009| image:: media/lab1-009.png
   :width: 4.5in
   :height: 1.69in
.. |image010| image:: media/lab1-010.png
   :width: 4.5in
   :height: 2.94in
.. |image011| image:: media/lab1-011.png
   :width: 4.5in
   :height: 0.80in
.. |image012| image:: media/lab1-012.png
   :width: 4.5in
   :height: 1.12in
.. |image013| image:: media/lab1-013.png
   :width: 4.5in
   :height: 4.00in
.. |image014| image:: media/lab1-014.png
   :width: 4.5in
   :height: 1.48in
.. |image015| image:: media/lab1-015.png
   :width: 4.5in
   :height: 1.12in
.. |image016| image:: media/lab1-016.png
   :width: 4.5in
   :height: 1.54in
.. |image017| image:: media/lab1-017.png
   :width: 4.5in
   :height: 1.29in
.. |image018| image:: media/lab1-018.png
   :width: 4.5in
   :height: 5.46in
.. |image019| image:: media/lab1-019.png
   :width: 4.5in
   :height: 2.13in
.. |image020| image:: media/lab1-020.png
   :width: 4.5in
   :height: 1.01in
.. |image021| image:: media/lab1-021.png
   :width: 4.5in
   :height: 1.93in
.. |image022| image:: media/lab1-022.png
   :width: 4.5in
   :height: 3.37in
.. |image023| image:: media/lab1-023.png
   :width: 4.5in
   :height: 3.38in
.. |image024| image:: media/lab1-024.png
   :width: 4.5in
   :height: 0.73in
.. |image025| image:: media/lab1-025.png
   :width: 4.5in
   :height: 3.37in
.. |image026| image:: media/lab1-026.png
   :width: 4.5in
   :height: 1.15in
.. |image027| image:: media/lab1-027.png
   :width: 4.5in
   :height: 2.28in
.. |image028| image:: media/lab1-028.png
   :width: 4.5in
   :height: 0.96in
.. |image029| image:: media/lab1-029.png
   :width: 4.5in
   :height: 1.69in
.. |image030| image:: media/lab1-030.png
   :width: 4.5in
   :height: 2.94in
.. |image031| image:: media/lab1-031.png
   :width: 4.5in
   :height: 0.80in
.. |image032| image:: media/lab1-032.png
   :width: 4.5in
   :height: 1.12in
.. |image033| image:: media/lab1-033.png
   :width: 4.5in
   :height: 4.00in
.. |image034| image:: media/lab1-034.png
   :width: 4.5in
   :height: 1.48in
.. |image035| image:: media/lab1-035.png
   :width: 4.5in
   :height: 1.12in
.. |image036| image:: media/lab1-036.png
   :width: 4.5in
   :height: 1.54in
.. |image037| image:: media/lab1-037.png
   :width: 4.5in
   :height: 1.29in
.. |image038| image:: media/lab1-038.png
   :width: 4.5in
   :height: 5.46in
.. |image039| image:: media/lab1-039.png
   :width: 4.5in
   :height: 2.13in
.. |image040| image:: media/lab1-040.png
   :width: 4.5in
   :height: 1.01in
.. |image041| image:: media/lab1-041.png
   :width: 4.5in
   :height: 1.93in
.. |image042| image:: media/lab1-042.png
   :width: 4.5in
   :height: 1.93in
.. |image043| image:: media/lab1-043.png
   :width: 4.5in
   :height: 1.93in
.. |image044| image:: media/lab1-044.png
   :width: 4.5in
   :height: 1.93in
.. |image045| image:: media/lab1-045.png
   :width: 4.5in
   :height: 1.93in
.. |image046| image:: media/image001.png
   :width: 4.5in
   :height: 1.93in
      
