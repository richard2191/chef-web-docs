.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.

The ``POST`` method is used to add groups to the |chef server|.

.. note:: Users and actors are ignored if they are part of the request body when used with the ``POST`` method. Use the ``PUT`` method to add users and actors to a group on the |chef server|.

This method has no parameters.

**Request**

.. code-block:: none

   POST /organizations/NAME/group/GROUP_NAME

with a request body similar to:

.. code-block:: none

   {
     "groupname": "foo"
   }

**Response**

This method has no response body.

**Response Codes**

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Response Code
     - Description
   * - ``200``
     - |response code 200 ok|
   * - ``400``
     - |response code 400 bad request|
   * - ``401``
     - |response code 401 unauthorized|
   * - ``403``
     - |response code 403 forbidden|
   * - ``404``
     -  |response code 404 not found|
   * - ``409``
     - |response code 409 conflict|
   * - ``413``
     - |response code 413 entity_too_large|
