.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following providers:

.. list-table::
   :widths: 150 80 320
   :header-rows: 1

   * - Long name
     - Short name
     - Notes
   * - ``Chef::Provider::Package``
     - ``package``
     - When this short name is used, the |chef client| will attempt to determine the correct provider during the |chef client| run.
   * - ``Chef::Provider::Package::Homebrew``
     - ``homebrew_package``
     - The provider that is used with the |mac os x| platform.