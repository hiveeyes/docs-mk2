ustruct
=======

See Python `struct <https://docs.python.org/3/library/struct.html>`__
for more information.

Supported size/byte order prefixes: ``@, <, >, !``.

Supported format codes: ``b, B, h, H, i, I, l, L, q, Q, s, P, f, d``
(the latter 2 depending on the floating-point support).

Methods
-------

ustruct.calcsize(fmt)
^^^^^^^^^^^^^^^^^^^^^

Return the number of bytes needed to store the given ``fmt``.

ustruct.pack(fmt, v1, v2, …)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Pack the values ``v1, v2, ...`` according to the format string ``fmt``.
The return value is a bytes object encoding the values.

ustruct.pack_into(fmt, buffer, offset, v1, v2, …)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Pack the values ``v1, v2, ...`` according to the format string ``fmt``
into a buffer starting at ``offset``. ``offset`` may be negative to
count from the end of buffer.

ustruct.unpack(fmt, data)
^^^^^^^^^^^^^^^^^^^^^^^^^

Unpack from the ``data`` according to the format string ``fmt``. The
return value is a tuple of the unpacked values.

ustruct.unpack_from(fmt, data, offset=0)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Unpack from the ``data`` starting at ``offset`` according to the format
string ``fmt``. ``offset`` may be negative to count from the end of
buffer. The return value is a tuple of the unpacked values.
