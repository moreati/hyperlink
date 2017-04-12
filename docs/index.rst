.. hyperlink documentation master file, created on Mon Apr 10 00:34:18 2017.
hyperlink
=========

*Cool URLs that don't change.*

|release| |calver|

**Hyperlink** provides a pure-Python implementation of immutable
URLs. Based on RFC 3986 and 3987, the Hyperlink URL makes working with
both URIs and IRIs easy.

Hyperlink is tested against Python 2.7, 3.4, 3.5, and PyPy.


.. |release| image:: https://img.shields.io/pypi/v/hyperlink.svg
             :target: https://pypi.python.org/pypi/hyperlink

.. |calver| image:: https://img.shields.io/badge/calver-YY.MINOR.MICRO-22bfda.svg
            :target: http://calver.org


Installation and Integration
----------------------------

Hyperlink is a pure-Python package and only depends on the standard
library. The easiest way to install is with pip::

  pip install hyperlink

Then, URLs are just an import away away::

  from hyperlink import URL

  url = URL.from_text('http://github.com/mahmoud/hyperlink?utm_souce=README')
  utm_source = url.get('utm_source')
  better_url = url.replace(scheme='https')
  user_url = better_url.click('..')

  print(user_url.to_text())
  # prints: http://github.com/mahmoud

See the API docs for more usage examples.

Gaps
----

Found something missing in hyperlink? `Pull Requests`_ and `Issues`_ weclome!

.. _Pull Requests: https://github.com/mahmoud/hyperlink/pulls
.. _Issues: https://github.com/mahmoud/hyperlink/issues

Section listing
---------------

.. toctree::
   :maxdepth: 2

   design
   api