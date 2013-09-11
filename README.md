Building
========

Install build deps:
    tce-load -wi icu49-dev popt-dev ncurses-dev

Write something sensible to /opt/.tce_dir. Try the following for default
tinycore usage:
    echo -n '/tmp/tce' > /opt/.tce_dir

Install tcztools:
    wget https://tcztools.googlecode.com/hg/tcztools.tcz -cP "$(cat /opt/.tce_dir)/optional" && \
    tce-load -i tcztools

Build gdisk package
    ./gdisk-get && ./gdisk-build && tcz-pack gdisk

Now look in /tmp/tcztools for the generated files.

Contributing
============

The packaging files for this package are managed in [this git repo]
(https://github.com/ooyala/tinycore_gdisk).

Licensing
=========
The original gptfdisk software is licensed under the GPL v2. The packaging
files in this repository are licensed under Apache License v2.0.

Copyright (c) 2013 Ooyala, Inc.
