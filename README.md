p.haul
======

Process HAULer — a tool to live-migrate containers and processes

The live migration idea is quite simple. To live migrate a task
from one host to another, one needs to:

1. freeze it and dump its state into image files
2. make these image files available on the destination host
3. recreate the task from the images

This is essentially what p.haul does. It heavily uses [CRIU](http://criu.org)
to perform tasks' state dump and restore (steps 1 and 3 above).
Tasks' frozen time is optimized using the CRIU's pre-dump action.

Get p.haul ready
================

1. Install criu or put criu binary location to `$PATH`.

2. Install `protobuf-compiler` and `protobuf-python` packages.

3. Install p.haul by running ```$ python setup.py install```
or just use it without installing.

For more information, see P.Haul pages on the CRIU
wiki, http://criu.org/Category:P.Haul.

Bugs
====

All bugs are to be reported on the criu@openvz.org mailing list.
To [un]subscribe, see http://lists.openvz.org/mailman/listinfo/criu
