.. This is an included how-to. 


If a hostname is not resolvable, refer to a local systems administrator for specific guidance on how to add the hostname to the |dns| system. If the |chef server| is being into a testing environment, just add the hostname to ``/etc/hosts``. The following example shows how a hostname can be added to ``/etc/hosts`` when running |redhat| or |centos|:

.. code-block:: bash

   $ echo -e "127.0.0.2 `hostname` `hostname -s`" | sudo tee -a /etc/hosts