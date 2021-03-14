.. image:: https://github.com/zopefoundation/Products.ZODBMountPoint/actions/workflows/tests.yml/badge.svg
        :target: https://github.com/zopefoundation/Products.ZODBMountPoint/actions/workflows/tests.yml

.. image:: https://coveralls.io/repos/github/zopefoundation/Products.ZODBMountPoint/badge.svg?branch=master
   :target: https://coveralls.io/github/zopefoundation/Products.ZODBMountPoint?branch=master

.. image:: https://img.shields.io/pypi/v/Products.ZODBMountPoint.svg
   :target: https://pypi.org/project/Products.ZODBMountPoint/
   :alt: Current version on PyPI

.. image:: https://img.shields.io/pypi/pyversions/Products.ZODBMountPoint.svg
   :target: https://pypi.org/project/Products.ZODBMountPoint/
   :alt: Supported Python versions

Overview
========

Zope ZODB mount point support


Usage example
-------------
You can mount additional storages into the ZODB as seen by the Zope client 
by adding ``zodb_db`` configurations in your Zope configuration file and
specifying where they show up. This example uses the
ZODB `MappingStorage
<https://zodb-docs.readthedocs.io/en/latest/reference/storages.html#mappingstorage>`_
to mount a temporary folder at ``/temp_folder``::

  <zodb_db temporary>
      <mappingstorage>
        name Temporary database
      </mappingstorage>
      mount-point /temp_folder
      container-class Products.TemporaryFolder.TemporaryContainer
  </zodb_db>

For details on session configuration, see `the Zope book chapter on session
management <https://zope.readthedocs.io/en/latest/zopebook/Sessions.html>`_.
