Installation
============

Dependencies
------------

``collective.geo``, and `collective.geo.contentlocation`_ in particular,
depend on *Shapely*, a library for the manipulation of planar geometric
objects, and *Shapely* itself depends on ``libgeos_c`` > 3.1

.. _collective.geo.contentlocation: http://pypi.python.org/pypi/collective.geo.contentlocation

Before installing ``collective.geo`` you have to install the ``libgeos_c``
library on your machine.

Debian/Ubuntu
`````````````

On Linux systems based on Debian, you have to install the following packages:

* libgeos-c1
* libgeos-dev

Mac OS X
`````````

To install libgeos on Mac OS X system you can use macports and install this pachage:

* geos

Buildout
--------

The best way to install collective geo is using `zc.buildout`_
and adding the `collective.geo.bundle`_ package.

.. _collective.geo.bundle: http://pypi.python.org/pypi/collective.geo.bundle
.. _zc.buildout: http://pypi.python.org/pypi/zc.buildout

This package contains all core packages of ``collective.geo`` that are
suitable for common use.

Below an example of configuration::

    [buildout]
    ...
    eggs =
        ...
        collective.geo.bundle
    ...

You can also use each package separately to better suit your needs.

For instance, you can use only `collective.geo.geographer`_ if you need to
annotate Plone content types with geographical information, or you can use
only `collective.geo.openlayers`_ to integrate *OpenLayers* javascript in
Plone. See above for package details.

.. _collective.geo.openlayers: http://pypi.python.org/pypi/collective.geo.openlayers
.. _collective.geo.geographer: http://pypi.python.org/pypi/collective.geo.geographer

After running the buildout and starting Zope you have to install the product
*Plone Maps (collective.geo)* from the :guilabel:`Addons` Control Panel.

For development purposes, you can use the buildout configuration included in
`collective.geo.bundle`_.

In this package you'll find two different configurations:

* :file:`buildout.cfg`: a generic buildout configuration that includes
  `collective.geo.bundle`_ and its dependencies
* :file:`devel.cfg`, a specific development configuration that includes all
  ``collective.geo`` source packages from github.
