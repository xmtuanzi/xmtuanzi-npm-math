=======
fastcrc
=======

.. image:: https://img.shields.io/readthedocs/fastcrc.svg?style=flat&maxAge=1800
    :alt: Read the Docs
    :target: https://fastcrc.readthedocs.io/

.. image:: https://img.shields.io/pypi/v/fastcrc.svg?style=flat&maxAge=1800
    :alt: PyPI
    :target: https://pypi.python.org/pypi/fastcrc

.. image:: https://img.shields.io/badge/python-%3E%3D3.7-blue?style=flat
    :alt: Python - Version
    :target: https://pypi.python.org/pypi/fastcrc

A hyper-fast Python module for computing CRC(8, 16, 32, 64) checksum.


Installation
============

.. code-block:: text

   pip install fastcrc

Usage
=====

.. code:: python

   from fastcrc import crc8, crc16, crc32, crc64

   data = b"123456789"
   print(f"crc8 checksum with cdma2000 algorithm: {crc8.cdma2000(data)}")
   print(f"crc16 checksum with xmodem algorithm: {crc16.xmodem(data)}")
   print(f"crc32 checksum with aixm algorithm: {crc32.aixm(data)}")
   print(f"crc64 checksum with ecma_182 algorithm: {crc64.ecma_182(data)}")
   print(f"crc16 checksum with xmodem algorithm (with initial data): {crc16.xmodem(b'56789', crc16.xmodem(b'1234'))}")

Documentation
=============
fastcrc's documentation can be found at https://fastcrc.readthedocs.io

License
=======

fastcrc is licensed under `MIT License`_.

Thanks
=======

fastcrc is made possible by `crc-rs`_.

.. _MIT License: ./LICENSE
.. _crc-rs: https://github.com/mrhooray/crc-rs