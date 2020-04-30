Solution: (In Development) SAML SP with sideband to update AD Logon Timestamp
======================================================================================

This solution documents all the necessary pieces required to create a set of APM policies  that updates the AD lastlogontimestamp when only using SAML.  

Objective:
----------

-  Gain an basic understanding of BIG-IP as a SAML IDP and SAML SP

-  Gain an understanding of sideband request

-  Gain an initial understanding of kerberos SSO

.. toctree::
   :maxdepth: 1
   :caption: Content:
   :glob:
  
   guide/guide.rst
   postman/postman.rst


Configuration Comments
------------------------

Access Blueprint Revision
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  - 42

Postman Collection(s)
^^^^^^^^^^^^^^^^^^^^
  - sp.acme.com-create.postman_collection.json
  - sp.acme.com-delete.postman_collection.json


APM Profile(s) 
^^^^^^^^^^^^
  - profile_Common_sp.acme.com-psp.conf.tar
  - profile_Common_idp.acme.com-psp.conf.tar


BIG-IP Versions Tested
^^^^^^^^^^^^^^^^^^^^^^
  - 15.1

BIG-IP Components used:
-----------------

* Virtual Server
 - HTTP Profile -https://support.f5.com/csp/article/K4707
 - Client-side SSL Profile -https://support.f5.com/csp/article/K14783
 - Access Profile(s)
      + SAML SP
      + SAML IDP
      + AAA Active Directory Objects
      + Kerberos SSO





   

