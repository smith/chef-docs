.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


When a node runs |chef client| for the first time, it generally does not yet have an |chef api client| identity, and so it cannot make authenticated requests to the server. This is where the validation client (named |chef validator|) comes in. When the |chef client| runs, it checks if it has a client key. If the client key does not exist, it then attempts to borrow the validation client's identity to register itself with the |chef server|. In order to register with the |chef server|, the validation client's private key needs to be copied to the host and placed in |path chef etc validation|. 

Once the |chef client| has registered itself with the |chef server|, it no longer uses the validation client for anything. It is recommended that you delete the validation client's private key from the host after the host has registered or use the ``delete_validation`` recipe that can be found in the ``chef-client`` cookbook (http://community.opscode.com/cookbooks/chef-client).
