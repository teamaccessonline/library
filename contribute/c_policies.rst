How to Contribute APM Policies
--------------------------------

#. Policies should be built in the Commom partition, unless there is a necessary reason to use a differnt 
#. Upload both a .gz and .tar version of the policy 
#. The .tar file is used for when importing via AS3
#. The .gz file is used when someone wants to import the policy via the GUI.  Someone may want to do this, so they can edit      the policy inside the **Common** partition and object names stay their original names. This will allow other to use your      policy to build new solutions without starting from scratch.
#. If using the the Postman Collection templates they assume the Policy was created **Common** Partitiion with the lowercase      name **XXXXX-psp** prior to export.  Naming your policies in that format will reduce the amount of customization you need      to perform on the Postman Collection Templates.
#. Following the steps outlined for :ref:`Pushing_content`
