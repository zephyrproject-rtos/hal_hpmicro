..
  Copyright (c) 2026 Cody Gu <gujiaqi@iscas.ac.cn>
  SPDX-License-Identifier: Apache-2.0

HPMicro HAL
===========

Overview
--------

This repository contains the HPMicro HPM SDK hardware abstraction layer used
by the Zephyr HPMicro port. It is a vendor HAL module and does not contain
Zephyr-specific build integration or compatibility code.

Source
------

* Upstream: https://github.com/hpmicro/hpm_sdk
* Version: v1.13.0
* Commit: ``ccc5ec467a047f3ea85cd2fa4565e91db7135a38``
* License: ``BSD-3-Clause``, see ``hpm_sdk/LICENSE``

Imported content
----------------

``arch/``, ``soc/``, ``drivers/``, ``components/``, ``utils/``, ``cmake/``,
``boards/openocd/``, ``LICENSE``, ``VERSION``, and
``hpm_sdk_version.h.in``.

``docs/``, ``middleware/``, ``samples/``, the full ``boards/`` tree, and the
standalone SDK ``CMakeLists.txt`` are not imported.

Zephyr integration
------------------

The Zephyr CMake, Kconfig and board compatibility code lives in the main
Zephyr tree under ``modules/hal_hpmicro``. The ``zephyr/module.yml`` file in
this repository only declares the module and points Zephyr at those build
files through ``cmake-ext`` and ``kconfig-ext``.

Maintenance
-----------

When updating ``hpm_sdk/``, regenerate ``modules/hal_hpmicro/Kconfig`` in the
Zephyr tree and run ``modules/hal_hpmicro/scripts/check_module.py`` there.

Licensing
---------

The vendor tree under ``hpm_sdk/`` is ``BSD-3-Clause``. Module metadata in
this repository is ``Apache-2.0``.
