===========================
Installation Guide for OS X
===========================

This guide outlines the steps to install Jupyter on OS X. For experienced users,
upgrade instructions are included at the end of the guide.

Installation overview
---------------------
* Check Python installation
* Install Jupyter Notebook
    - Install Jupyter using Anaconda
    - Install Jupyter using pip, Python's Package Manager
* Check Jupyter installation
* [Optional] Install additional language kernels
* Next steps and running Jupyter notebook

.. important::

    **Jupyter installation requires Python 3.3 or greater or Python 2.7.**

    If you need to use Python 2.6 or 3.2, you may install
    `IPython 1.2 <http://archive.ipython.org/release/1.2.0/>`_.
    Older releases of IPython are available `here <http://archive.ipython.org/release/>`__.

Check Python installation
^^^^^^^^^^^^^^^^^^^^^^^^^

To install Jupyter Notebook, you will also need Python installed on your system.

To check if you have a recent version of Python installed on your system:

``python --version``
``which python``

To install a new version of Python, go to the Python website or use a package
manager such as Homebrew.

Install Jupyter Notebook
^^^^^^^^^^^^^^^^^^^^^^^^
.. note::

     All commands shown below must be run in the Terminal.

.. _new-to-python-and-jupyter:

Install Jupyter using Anaconda
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you're new to Python, we highly recommend installing `Anaconda
<https://www.continuum.io/downloads>`_. Anaconda includes and conveniently
installs Python, the Jupyter Notebook, and other commonly used packages for
scientific computing and data science. Follow Anaconda's instructions for
downloading the Python 3.5 version. You may need to click on the "I want
Python 3.5" link to download Anaconda for Python 3.5.

After installing Anaconda, make sure that Jupyter is up to date. Run the
following command in the Terminal::

    conda install jupyter

Alternatively, you may also use the Anaconda Launcher application to update to
the latest version.

Now, you may consider :ref:`installing additional kernels <installing-kernels>`
and :ref:`next steps <next-steps>` such as running the Jupyter Notebook.

Install Jupyter using pip, Python's package manager
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Install the Jupyter Notebook using Python's package manager `pip`::

    pip3 install jupyter

(*Use ``pip`` instead of ``pip3`` for legacy Python 2*)

Now, you may consider :ref:`installing kernels <installing-kernels>` and
:ref:`next steps <next-steps>`.

Checking your Jupyter installation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

jupyter version

Installing kernels
^^^^^^^^^^^^^^^^^^
Installing the Jupyter Notebook as described above will also install the `IPython
kernel <http://ipython.readthedocs.org/en/master/>`_ which allows working on
notebooks using the Python programming language.

To run notebooks in languages other than Python, you will need to install
additional kernels. For more information, see the full `list of available kernels
<https://github.com/ipython/ipython/wiki/IPython-kernels-for-other-languages>`_.

Next steps
^^^^^^^^^^
Congratulations. You have installed Jupyter Notebook and are ready to
:ref:`run the notebook <running>`.

.. seealso::

    For detailed installation instructions for individual Jupyter or IPython
    subprojects, please see the documentation or GitHub repos of the
    individual subprojects listed in :ref:`Jupyter Subprojects <subprojects>`
    document.

Upgrading Jupyter (Experienced Users)
-------------------------------------
The Jupyter Notebook used to be called the IPython Notebook. If you are running
an older version of the IPython Notebook (version 3 or earlier) you can use the
following to upgrade to the latest version of the Jupyter Notebook.

**If using 'pip'**::

    pip install -U jupyter

OR

**If using Anaconda or `conda`**::

    conda update jupyter

.. seealso::

    The :ref:`Migrating from IPython <migrating>` document has additional
    information about migrating from IPython 3 to Jupyter.
