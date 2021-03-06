.. _boost_build_generator:

boost-build
===========

.. caution::

    This generator is deprecated in favor of the ``b2`` generator. See :ref:`generator b2<b2_generator>`.

The ``boost-build`` generator creates a file named *project-root.jam* that can be used with the Boost Build build system script.

The generated *project-root.jam* file contains several sections and an alias ``conan-deps`` with the section names:

.. code-block:: text

    lib ssl :
        : # requirements
        <name>ssl
        <search>/path/to/package/227fb0ea22f4797212e72ba94ea89c7b3fbc2a0c/lib
        : # default-build
        : # usage-requirements
        <include>/path/to/package/227fb0ea22f4797212e72ba94ea89c7b3fbc2a0c/include
        ;

    lib crypto :
        : # requirements
        <name>crypto
        <search>/path/to/package/227fb0ea22f4797212e72ba94ea89c7b3fbc2a0c/lib
        : # default-build
        : # usage-requirements
        <include>/path/to/package/227fb0ea22f4797212e72ba94ea89c7b3fbc2a0c/include
        ;

    lib z :
        : # requirements
        <name>z
        <search>/path/to/package/8018a4df6e7d2b4630a814fa40c81b85b9182d2b/lib
        : # default-build
        : # usage-requirements
        <include>/path/to/package/8018a4df6e7d2b4630a814fa40c81b85b9182d2b/include
        ;

    alias conan-deps :
        ssl
        crypto
        z
    ;
