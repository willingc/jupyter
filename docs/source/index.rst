.. _landing:

=====================
Jupyter Documentation
=====================

The Jupyter Notebook is a web application for interactive data science and
scientific computing.

.. sidebar:: What's New in Jupyter Notebook
   **Release candidate 4.1.0rc1**

   - Cell toolbar selector moved to View menu
   - Restart & Run All Cells added to Kernel menu
   - Multiple-cell selection and actions including cut, copy, paste and execute
   - Command palette added for executing Jupyter actions
   - Find and replace added to Edit menu

   To install release candidate:
   ``python -m pip install notebook --pre --upgrade``

Using the Jupyter Notebook, you can author engaging
documents that combine live-code with narrative text, equations, images, video,
and visualizations. By encoding a complete and reproducible record of a
computation, the documents can be shared with others on GitHub, Dropbox, and
the `Jupyter Notebook Viewer <http://nbviewer.ipython.org/>`__.

The main documentation for Jupyter users is organized into several sections:

  :ref:`User Documentation<user-docs>` |
  :ref:`Jupyter Subprojects<jupyter-subprojects>` |
  :ref:`About Jupyter<about-docs>`

:ref:`Developer Documentation<dev-docs>` covers how to help with the
development of Jupyter as well as technical details helpful for development.


.. _user-docs:

.. toctree::
    :maxdepth: 2
    :caption: User Documentation

    tryjupyter
    install
    running
    migrating
    install_osx

.. _jupyter-subprojects:

.. toctree::
   :maxdepth: 2
   :caption: Jupyter Subprojects

   subprojects
   config


.. _dev-docs:

.. toctree::
   :maxdepth: 2
   :caption: Developer Documentation

   system
   contrib_guide_bugs_enh
   contrib_guide_docs
   contrib_guide_code

.. _about-docs:

.. toctree::
   :maxdepth: 2
   :caption: About Jupyter

   data_science
