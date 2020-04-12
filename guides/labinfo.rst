Getting to Know the Environment
--------------------------------

To gain access to a live sandboxed environment please contact your F5 Account Team.

To access your dedicated student lab environment, you will require a web browser
and Remote Desktop Protocol (RDP) client software. The web browser will be used to
access the Lab Environement. The RDP client will be used to connect to the Jump
Host, where you will be able to access the BIG-IP management interfaces (HTTPS, SSH).

+-----------------------------------------------------------------------------------------------+
| 1. Establish a RDP connection to **jumphost.f5lab.local**  with the following credentials:    |                           
|                                                                                               |
|    - **UserID: f5lab\\user1** / **Password: user1**                                           |
|                                                                                               |
| 2. Open the Command Prompt                                                                    |
|                                                                                               |
| 3. Type **cd c:\\labfiles\\solutions\\postman**                                               |
|                                                                                               |
| 4, Type **Newman run [name of postman collection] -e [name of environment variables] -k**     |
|                                                                                               |
| ..note::  Reference the solution guide you with to deploy to determine the appropriate        |
|           Postman Collection to run                                                           |
|                                                                                               |
| 5. Access the appropriate BIG-IP using the credentials below                                  |
|    - **UserID: admin** / **Password: admin**                                                  |
|                                                                                               |
+-----------------------------------------------------------------------------------------------+
| Note: All work for this lab will be performed exclusively from the provided lab environment.  |
|                                                                                               |
|       No installation or interaction with your local system is required.                      |
+-----------------------------------------------------------------------------------------------+

Lab Topology
~~~~~~~~~~~~

|image000|  

The following components have been included in your lab environment:

- 2 x F5 BIG-IP VE (v15.1)
- 1 x Windows Jumphost- Server 2016
- 1 x Windows 2016 Server hosting AD, CA, OCSP & DNS
- 1 x Windows 2016 Server hosting IIS
- 1 x Ubuntu 16.04 LTS 
- 1 x Centos 7

Lab Components
^^^^^^^^^^^^^^

The following table lists VLANS, IP Addresses and Credentials for all
components:

+------------------------+-------------------------+------------------------------------------+
| Component              | VLAN/IP Address(es)     | Credentials                              | 
+========================+=========================+==========================================+
| jumpbox.f5lab.local    | - Management 10.1.1.10  | - Username: f5lab\\user1 Password: user1 | 
|                        | - External   10.1.10.10 | - Username: f5lab\\user2 Password: user2 | 
|                        | - Internal   10.1.20.10 |                                          |
+------------------------+-------------------------+------------------------------------------+
| BIG-IP1.f5lab.local    | - Management 10.1.1.4   | - Username: admin Password: admin        | 
|                        | - External   10.1.10.4  |                                          | 
|                        | - Internal   10.1.20.4  |                                          |
+------------------------+-------------------------+------------------------------------------+
| BIG-IP3.f5lab.local    | - Management 10.1.1.5   | - Username: admin Password: admin        | 
|                        | - External   10.1.10.5  |                                          | 
|                        | - Internal   10.1.20.5  |                                          |
+------------------------+-------------------------+------------------------------------------+
| BIG-IP5.f5lab.local    | - Management 10.1.1.11  | - Username: admin Password: admin        | 
|                        | - External   10.1.10.11 |                                          | 
|                        | - Internal   10.1.20.11 |                                          |
+------------------------+-------------------------+------------------------------------------+
| BIG-IP7.f5lab.local    | - Management 10.1.1.12  | - Username: admin Password: admin        | 
|                        | - External   10.1.10.12 |                                          | 
|                        | - Internal   10.1.20.12 |                                          |
+------------------------+-------------------------+------------------------------------------+
| dc1.f5lab.local         | - Management 10.1.1.7  | - Username: f5lab\\admin Password: admin | 
|                        | - Internal   10.1.20.7  |                                          | 
+------------------------+-------------------------+------------------------------------------+
| iis.f5lab.local        | - Management 10.1.1.6   | - Username: f5lab\\admin Password: admin | 
|                        | - Internal   10.1.20.6  |                                          | 
+------------------------+-------------------------+------------------------------------------+
| web.f5lab.local        | - Management 10.1.1.9   |                                          | 
|                        | - Internal   10.1.20.9  |                                          |
|                        | - Internal   10.1.20.19 |                                          |
+------------------------+-------------------------+------------------------------------------+
| radius.f5lab.local     | - Management 10.1.1.8   |                                          | 
|                        | - Internal   10.1.20.8  |                                          | 
+------------------------+-------------------------+------------------------------------------+      

.. |image000| image:: media/image000.png
   :width: 6.96097in
   :height: 4.46512in

