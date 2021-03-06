.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

The syntax for using the |resource service| resource in a recipe is as follows:

.. code-block:: ruby

   service "name" do
     attribute "value" # see attributes section below
     ...
     action :action # see actions section below
   end

where 

* ``service`` tells the |chef client| to use one of the following providers during the |chef client| run: ``Chef::Provider::Service::Init``, ``Chef::Provider::Service::Init::Debian``, ``Chef::Provider::Service::Upstart``, ``Chef::Provider::Service::Init::Freebsd``, ``Chef::Provider::Service::Init::Gentoo``, ``Chef::Provider::Service::Init::Redhat``, ``Chef::Provider::Service::Solaris``, ``Chef::Provider::Service::Windows``, or ``Chef::Provider::Service::Macosx``. The |chef client| will detect the platform at the start of the run based on data collected by |ohai|. After the platform is identified, the |chef client| will determine the correct provider
* ``name`` is the name of the resource block; when the ``service_name`` attribute is not specified as part of a recipe, ``name`` is also the name of the service
* ``attribute`` is zero (or more) of the attributes that are available for this resource
* ``:action`` identifies which steps the |chef client| will take to bring the node into the desired state

