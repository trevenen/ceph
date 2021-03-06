=======================================
Cloning the Ceph Source Code Repository
=======================================
To check out the Ceph source code, you must have ``git`` installed
on your local host. To install ``git``, execute::

	$ sudo apt-get install git

You must also have a ``github`` account. If you do not have a
``github`` account, go to `github.com <http://github.com>`_ and register.
Follow the directions for setting up git at `Set Up Git <http://help.github.com/linux-set-up-git/>`_.

Clone the Source
----------------
To clone the Ceph source code repository, execute::

	$ git clone git@github.com:ceph/ceph.git

Once ``git clone`` executes, you should have a full copy of the Ceph repository.

Clone the Submodules
--------------------
Before you can build Ceph, you must navigate to your new repository and get the ``init`` submodule and the ``update`` submodule::

	$ cd ceph
	$ git submodule init
	$ git submodule update

.. tip:: Make sure you maintain the latest copies of these submodules. Running ``git status`` will tell you if the submodules are out of date::

	$ git status

Choose a Branch
---------------
Once you clone the source code and submodules, your Ceph repository will be on the ``master`` branch by default, which is the unstable development branch. You may choose other branches too.

- ``master``: The unstable development branch.
- ``stable``: The bugfix branch.
- ``next``: The release candidate branch.

::

	git checkout master
