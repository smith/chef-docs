=====================================================
Authentication and Authorization
=====================================================

.. include:: ../../includes_chef_auth/includes_chef_auth.rst

Authentication
=====================================================
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication.rst

chef-validator
-----------------------------------------------------
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_chef_validator.rst

During a |chef| Run
-----------------------------------------------------
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_chef_run.rst

Chef Server Web Interface
-----------------------------------------------------
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_webui.rst

knife exec
-----------------------------------------------------
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_knife_exec.rst

Knife Plugins
-----------------------------------------------------
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_knife_plugins.rst

Others
-----------------------------------------------------
xxxxx

cURL
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_other_curl.rst

PyChef (A Python Library for Chef)
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_other_pychef.rst

Ruby
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_auth/includes_chef_auth_authentication_other_ruby.rst

Authorization
=====================================================
.. include:: ../../includes_chef_auth/includes_chef_auth_authorization.rst

Hosted Chef / Private Chef
-----------------------------------------------------
.. include:: ../../includes_chef_auth/includes_chef_auth_authorization_chef_server.rst

Role-based Access Security
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_auth/includes_chef_auth_authorization_chef_server_rbac.rst

Global Permissions
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_auth/includes_chef_auth_authorization_chef_server_permissions_global.rst

Object Permissions
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_auth/includes_chef_auth_authorization_chef_server_permissions_object.rst

Users and Groups
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_chef_auth/includes_chef_auth_authorization_chef_server_users_and_groups.rst

Open Source Chef Server
-----------------------------------------------------
.. include:: ../../includes_chef_auth/includes_chef_auth_authorization_open_source.rst

Chef Server API
=====================================================
.. include:: ../../includes_api_chef_server/includes_api_chef_server.rst

Authentication Headers
-----------------------------------------------------
.. include:: ../../includes_api_chef_server/includes_api_chef_server_headers.rst

Header Format
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_format.rst

Required Headers
+++++++++++++++++++++++++++++++++++++++++++++++++++++
The following authentication headers are required:

.. list-table::
   :widths: 130 400
   :header-rows: 1

   * - Feature
     - Description
   * - ``Accept``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_accept.rst
   * - ``Host``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_host.rst
   * - ``X-Chef-Version``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_chef_version.rst
   * - ``X-Ops-Authorization-N``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_ops_authorization.rst
   * - ``X-Ops-Content-Hash``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_ops_content_hash.rst
   * - ``X-Ops-Sign``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_ops_sign.rst
   * - ``X-Ops-Timestamp``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_ops_timestamp.rst
   * - ``X-Ops-UserId``
     - .. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_x_ops_userid.rst

Example
+++++++++++++++++++++++++++++++++++++++++++++++++++++
.. include:: ../../includes_api_chef_server/includes_api_chef_server_headers_example.rst

Endpoints
-----------------------------------------------------
For |chef hosted| and |chef private|, each authentication request must include ``/organizations/organization_name`` as part of the name for the endpoint. For the open source |chef server|, each authentication request must include ``/clients`` as part of the name of the endpoint. For example, the full endpoint for getting a list of roles on |chef hosted| or |chef private|:

.. code-block:: html

   GET /organizations/organization_name/roles

and for the same request, but to the open source |chef server|:

.. code-block:: html

   GET /clients/roles

The |api chef server| has the following endpoints:

* :doc:`api_chef_server_clients`
* :doc:`api_chef_server_clients_name`
* :doc:`api_chef_server_cookbooks`
* :doc:`api_chef_server_cookbooks_name`
* :doc:`api_chef_server_cookbooks_version`
* :doc:`api_chef_server_data_bag`
* :doc:`api_chef_server_data_bag_item`
* :doc:`api_chef_server_data_bag_name`
* :doc:`api_chef_server_environments`
* :doc:`api_chef_server_environments_name`
* :doc:`api_chef_server_environments_cookbook_name`
* :doc:`api_chef_server_environments_cookbook_version`
* :doc:`api_chef_server_environments_cookbooks`
* :doc:`api_chef_server_environments_node`
* :doc:`api_chef_server_environments_recipe`
* :doc:`api_chef_server_environments_role`
* :doc:`api_chef_server_nodes`
* :doc:`api_chef_server_nodes_name`
* :doc:`api_chef_server_roles`
* :doc:`api_chef_server_roles_name`
* :doc:`api_chef_server_roles_name_environments`
* :doc:`api_chef_server_roles_name_environments_name`
* :doc:`api_chef_server_sandboxes`
* :doc:`api_chef_server_sandboxes_id`
* :doc:`api_chef_server_search`
* :doc:`api_chef_server_search_index`
* :doc:`api_chef_server_user`

