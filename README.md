Movable Type CAS Login
====================

This is a diff between a fully CAS enabled Movable Type install and MT core.

This allows for automatic user creation and blog provisioning. Be sure you set up a master site for blogs to be part of.

Let me know if you have any questions.

Installation Instuctions
====================

Please run:

patch -p1 -u --verbose -i CAS.patch 

Please add the following to your mt.config file:

#======== AUTH ===========

AuthenticationModule CAS

ExternalUserManagement 1

AuthLoginURL https://your.cas.address:443

AuthLogoutURL https://your.cas.address:443/logout

MT_CAS_ValidationURL https://your.cas.address:443
