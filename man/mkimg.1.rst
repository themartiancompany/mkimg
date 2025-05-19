..
   SPDX-License-Identifier: AGPL-3.0-or-later

   ----------------------------------------------------------------------
   Copyright © 2024, 2025  Pellegrino Prevete

   All rights reserved
   ----------------------------------------------------------------------

   This program is free software: you can redistribute it and/or modify
   it under the terms of the GNU Affero General Public License as published by
   the Free Software Foundation, either version 3 of the License, or
   (at your option) any later version.

   This program is distributed in the hope that it will be useful,
   but WITHOUT ANY WARRANTY; without even the implied warranty of
   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
   GNU Affero General Public License for more details.

   You should have received a copy of the GNU Affero General Public License
   along with this program.  If not, see <https://www.gnu.org/licenses/>.


=================
mkimg
=================

-----------------------------
Make a volume image
-----------------------------
:Version: mkimg |version|
:Manual section: 1

Synopsis
========

mkimg *[options]* *[out_file]*

Description
===========

Produces a volume image.

File Systems
=============

ext4                    Ext4 file system
erofs                   Enhanced read only file system
btrfs                   Better file system
squashfs                Squash file system


Containers
=============

squashfs                Squash can act also as a container
luks                    LUKS2 (encrypted) filesystem container
raid0                   RAID0 filesystem container


Options
=======

-u uuid                 Image UUID.
-f img_tuple            Image format tuple, written as
                        '<container>+...+<container>+<fs>'.
-d directory            Specify input directory.
-s size                 Specify a size for the image.
-n img_name             LUKs container image name (if enabled).
-l img_label            Image label.
-K key_type             LUKS container encryption key type
                        ('auto', 'passphrase', 'file').
-k encryption_key       LUKS container encryption key.
-w bool                 Specify whether the image is intended to be writable.
-g bool                 Specify whether the image is intended to be able
                        to be opened by GRUB.
-x bool                 Specify whether enable compression.
-t                      Only verify if requirements
                        to produce the image are satisfied.
-m                      UUID auto generation type
                        Values are 'default' and 'epoch'.

-h                      Display help.
-c                      Enable color output
-v                      Enable verbose output

Bugs
====

https://github.com/themartiancompany/mkimg/-/issues

Copyright
=========

Copyright Pellegrino Prevete. AGPL-3.0.

See also
========

* key-gen
* ucantellme
* mkarchiso

.. include:: variables.rst
