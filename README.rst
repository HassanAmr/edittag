edittag
=======

Copyright (c) 2009–2011 Brant C. Faircloth. All rights reserved.

-  See ``LICENSE.md`` for standard, 2-clause BSD license covering
   computer code.
-  Sequence tags available from
   `https://github.com/BadDNA/edittag/downloads`_ are licensed under
   `Creative Commons Attribution 3.0 United States License`_.

Description
-----------

edittag is a software collection for designing sets of edit metric
sequence tags, checking sequence tags for conformation to the edit
metric, and integrating sequence tags to platform-specific sequencing
adapters and PCR primers. edittag differs from other approaches:

-  edittag generates arbitrary lengths of edit-metric sequence tags in
   reasonable time frames using multiprocessing
-  edittag produces edit metric sequence tag sets conform to the edit
   distance selected
-  edittag used primer3 to integrate sequence tags to PCR primers

We provide several large sets of edit metric sequence tags designed
using edittag in the following formats:

-  text_ - this file is in an appropriate format for
   ``check_levenshtien_distance.py``
-  csv_
-  `sqlite database`_

Citation
--------

::

    Cite.

Dependencies
------------

-  `Python 2.7.x`_ (should work on 2.6.x)
-  `numpy`_ (tested with 1.5.1)
-  `py-levenshtein`_ [optional but strongly recommended]
-  `mod-primer3`_ [optional]

Availability
------------

-  tar.gz (coming soon)
-  repository
-  Amazon Machine Instance # (coming soon)

Installation
------------

tar.gz (not yet implemented)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::

    tar -xzf package.tar.gz
    python setup.py install

repository
~~~~~~~~~~

::

    git clone git://github.com/baddna/edittag.git edittag
    chmod 0755 edittag/*.py
    ensure edittag is in your path

The steps below are only necessary if you want to use primer3 to
integrate sequence tags to PCR primers:

::

    cd git/edittag/edittag/lib/primer3
    git submodule init && git submodule update
    cd ../../../../
    git clone git://github.com/baddna/mod-primer3.git
    cd mod-primer3/src
    make
    make install

Ensure both ``edittag`` and ``mod-primer3`` are in your path.
Alternatively, move the binaries from mod-primer3 to a location in your
path (move at least ``primer3-long`` and ``primer3_config`` into the
same directory in your path). You can then run

Amazon Machine Instance (not yet implemented)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Create an account on Amazon EC2.
2. Run our instance with

.. _`https://github.com/BadDNA/edittag/downloads`: https://github.com/BadDNA/edittag/downloads
.. _Creative Commons Attribution 3.0 United States License: http://creativecommons.org/licenses/by/3.0/us/
.. _text: https://github.com/downloads/BadDNA/edittag/edit_metric_tags.txt
.. _csv: https://github.com/downloads/BadDNA/edittag/edit_metric_tags.csv
.. _sqlite database: https://github.com/downloads/BadDNA/edittag/edit_metric_tags.sqlite.zip
.. _Python 2.7.x: http://www.python.org/
.. _numpy: http://numpy.scipy.org
.. _py-levenshtein: http://pylevenshtein.googlecode.com
.. _mod-primer3: https://github.com/BadDNA/mod-primer3