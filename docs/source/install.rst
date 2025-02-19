Installation
============

Pwntools is best supported on 64-bit Ubuntu LTS releases (22.04 and 24.04).  Most functionality should work on any Posix-like distribution (Debian, Arch, FreeBSD, OSX, etc.).

Prerequisites
-------------

In order to get the most out of ``pwntools``, you should have the
following system libraries installed.

.. toctree::
   :maxdepth: 3
   :glob:

   install/*


Note: For Mac OS X you will need to have cmake ``brew install cmake`` and pkg-config ``brew install pkg-config`` installed.

Released Version
-----------------

pwntools is available as a ``pip`` package for Python3. Version v5.0.0 supports Python3.10 or later. Use v4 if you use earlier versions of Python.

Python3
^^^^^^^

The Python version required for installing Pwntools is kept as low as possible on a best-effort basis.  However, new features target Python3.10 and later.

.. code-block:: bash

    $ sudo apt-get update
    $ sudo apt-get install python3 python3-pip python3-dev git libssl-dev libffi-dev build-essential
    $ python3 -m pip install --upgrade pip
    $ python3 -m pip install --upgrade pwntools


Python2 (Deprecated)
^^^^^^^^^^^^^^^^^^^^

Python2 support has been removed in Pwntools v5.0.0.  The last version to support Python2 was v4.15.0.

NOTE: Pwntools maintainers STRONGLY recommend using Python3 for all future Pwntools-based scripts and projects.

Additionally, due to `pip` dropping support for Python2, a specfic version of `pip` must be installed.

.. code-block:: bash

    $ sudo apt-get update
    $ sudo apt-get install python python-pip python-dev git libssl-dev libffi-dev build-essential
    $ python2 -m pip install --upgrade pip==20.3.4
    $ python2 -m pip install --upgrade pwntools


Command-Line Tools
------------------

When installed with ``sudo`` the above commands will install Pwntools' command-line tools to somewhere like ``/usr/bin``.

However, if you run as an unprivileged user, you may see a warning message that looks like this::

    WARNING: The scripts asm, checksec, common, constgrep, cyclic, debug, disablenx, disasm, 
    elfdiff, elfpatch, errno, hex, main, phd, pwn, pwnstrip, scramble, shellcraft, template, 
    unhex, update and version are installed in '/home/user/.local/bin' which is not on PATH.

Follow the instructions listed and add ``~/.local/bin`` to your ``$PATH`` environment variable.

Development
--------------

If you are hacking on Pwntools locally, you'll want to do something like this:

.. code-block:: bash

    $ git clone https://github.com/Gallopsled/pwntools
    $ pip install --upgrade --editable ./pwntools

.. _Ubuntu: https://launchpad.net/~pwntools/+archive/ubuntu/binutils
