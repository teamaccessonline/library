.. _get_to_know:

Getting to Know the Environment
--------------------------------


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
| dc1.f5lab.local        | - Management 10.1.1.7   | - Username: f5lab\\admin Password: admin | 
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

Lab User Accounts
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::todo.. Document user1 and user2 attributes.  Document kerberos SSO user account.  Doucment OU structure.  Document Group Structure.


Internal DNS Resolution
~~~~~~~~~~~~~~~~~~~~~~~~

Lab Websites
~~~~~~~~~~~~~~~~~~~~~~~~

Active Directory APIs
~~~~~~~~~~~~~~~~~~~~~~~~

::todo..  Need to document all 

.. |image000| image:: media/image000.png
   :width: 6.96097in
   :height: 4.46512in

