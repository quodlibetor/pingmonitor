===============
 Monitor Pings
===============

A set of scripts to make it easy to see how often your internet fails.

Installation
============

Put the ping* files somewhere on your path::

    mv ping* ~/.local/bin

Usage
=====

#. Run ``pingmonitor``.
#. Maybe add ``killall ping && pinglogcompress && pingmonitor`` to cron.
#. Run ``pinglogreader`` occasionally, to see when and for how long your internet connection has died.

All scripts take ``-h``, if you want detailed usage.

Implementation
==============

I run ``ping`` in the background, checking if Google's public DNS server (because it has an easy-to-remember ip) is up.
Woooooo.

So you need a \*nix OS.
I also use Python for the reader, so you need Python.

TODO
====

* consider using `ping.py`_ instead of ping.
  This would significantly reduce installation difficulty and allow automatic compression without having to kill ``pingmonitor`` and restart it.

.. _ping.py: https://github.com/jedie/python-ping/blob/master/README.creole
