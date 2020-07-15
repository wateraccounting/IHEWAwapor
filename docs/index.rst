==========
IHEWAwapor
==========

This is the documentation of **IHEWAwapor**.

**Howto use**
::

    from IHEWAwapor import WPdownload as WaPOR

    APIToken    = 'Your WaPOR API token'
    latlim      = [7.89, 12.4]
    lonlim      = [37.95, 43.35]
    Startdate   = '2009-01-01'
    Enddate     = '2009-02-01'

    arg = {
        'APIToken': APIToken,
        'Dir':      dir_path,
        'Startdate':Startdate,
        'Enddate':  Enddate,
        'latlim':   latlim,
        'lonlim':   lonlim,
        'version':  2,
        'level':    1
    }

    print('\n===== WaPOR.AET =====')
    WaPOR.AET_dekadal(**arg)
    WaPOR.AET_monthly(**arg)
    WaPOR.AET_yearly(**arg)

    print('\n===== WaPOR.I =====')
    WaPOR.I_yearly(**arg)

    print('\n===== WaPOR.LCC =====')
    WaPOR.LCC_yearly(**arg)

    print('\n===== WaPOR.NPP =====')
    WaPOR.NPP_dekadal(**arg)

    print('\n===== WaPOR.PCP =====')
    WaPOR.PCP_daily(**arg)
    WaPOR.PCP_monthly(**arg)
    WaPOR.PCP_yearly(**arg)

    print('\n===== WaPOR.RET =====')
    WaPOR.RET_monthly(**arg)
    WaPOR.RET_yearly(**arg)


Development
===========

.. code-block:: console

    $ git clone https://github.com/wateraccounting/IHEWAwapor.git

From the root of the project

.. code-block:: console

    $ python setup.py --version

Format scripts by PEP8

.. code-block:: console

    $ autopep8 --in-place --aggressive src/IHEWAwapor/WPdownload/download/WaporAPI.py

Unit test

.. code-block:: console

    $ python setup.py test

Read the Docs

.. code-block:: console

    $ python setup.py doctest

    $ python setup.py docs

PyPI upload, run ``setup.py``::

    1. Commit -> Git - tag - add - v0.0.1 -> ``setup.py`` -> push
    2. Github - Release - new release v0.0.1

.. code-block:: console

    $ python setup.py sdist bdist_wheel

    $ twine check dist/*.tar.

    $ twine upload dist/*


Contents
========

.. toctree::
   :maxdepth: 4

   License <license>
   Authors <authors>
   Contributing <contributing>
   Changelog <changelog>
   Module Reference <api/modules>


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

.. _toctree: http://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html
.. _reStructuredText: http://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html
.. _references: http://www.sphinx-doc.org/en/stable/markup/inline.html
.. _Python domain syntax: http://sphinx-doc.org/domains.html#the-python-domain
.. _Sphinx: http://www.sphinx-doc.org/
.. _Python: http://docs.python.org/
.. _Numpy: http://docs.scipy.org/doc/numpy
.. _SciPy: http://docs.scipy.org/doc/scipy/reference/
.. _matplotlib: https://matplotlib.org/contents.html#
.. _Pandas: http://pandas.pydata.org/pandas-docs/stable
.. _Scikit-Learn: http://scikit-learn.org/stable
.. _autodoc: http://www.sphinx-doc.org/en/stable/ext/autodoc.html
.. _Google style: https://github.com/google/styleguide/blob/gh-pages/pyguide.md#38-comments-and-docstrings
.. _NumPy style: https://numpydoc.readthedocs.io/en/latest/format.html
.. _classical style: http://www.sphinx-doc.org/en/stable/domains.html#info-field-lists
