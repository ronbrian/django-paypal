Tests
=====

To run the django-paypal tests:

* Download the `source from GitHub <https://github.com/spookylukey/django-paypal>`_ or your fork.
* Create a virtualenv for the django-paypal project.
* Install tox::

      pip install tox

* Run tox::

      tox

  This will run all the tests on all supported combinations of Django/Python.

* If you're testing on a Mac, then, as m2crypto uses openssl, the command line should be:

      env LDFLAGS="-L"$(brew --prefix openssl)"/lib" \
      CFLAGS="-I"$(brew --prefix openssl)"/include" \
      SWIG_FEATURES="-cpperraswarn -includeall -I"$(brew --prefix openssl)"/include" \
      tox
