WebInspect API
=============

A Python module to assist with the `WebInspect <http://www8.hp.com/us/en/software-solutions/webinspect-dynamic-analysis-dast/>`_  RESTFul API to administer scans.

Quick Start
-----------

Several quick start options are available:

- Build locally: :code:`python setup.py build`
- Install with pip (recommended): :code:`pip install dist/webinspectapi-latest.tar.gz`
- Download the latest release

Example
-------

.. code-block:: python

    # import the package
    from webinspectapi import webinspect

    # setup webinspect connection information
    host = 'http://localhost:8083/webinspect/'

    # instantiate the webinspect api wrapper
    wi = webinspect.WebInspectAPI(host)

    # List scans
    scans = wi.list_scans()

    for scan in scans.data:
            print(str(scan['Name']), str(scan['Status']), str(scan['ID']))

Supporting information for each method available can be found in the `documentation <https://target.github.io/webinspectapi/>`_.

Bugs and Feature Requests
-------------------------

Found something that doesn't seem right or have a feature request? Please open a new issue.

Copyright and License
---------------------

- Copyright 2017 Target, Inc.
- `Licensed under MIT <LICENSE.txt>`_.
