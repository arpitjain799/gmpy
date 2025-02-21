Multiple-precision Integers
===========================

.. currentmodule:: gmpy2

The gmpy2 `mpz` type supports arbitrary precision integers. It should be a
drop-in replacement for Python's `int` type. Depending on the platform and the
specific operation, an `mpz` will be faster than Python's `int` once the
precision exceeds 20 to 50 digits. All the special integer functions in GMP are
supported.

Examples
--------

.. doctest::

    >>> from gmpy2 import is_prime, mpz
    >>> mpz('123') + 1
    mpz(124)
    >>> 10 - mpz(1)
    mpz(9)
    >>> is_prime(17)
    True
    >>> mpz('1_2')
    mpz(12)

.. note::
    The use of ``from gmpy2 import *`` is not recommended. The names in gmpy2
    have been chosen to avoid conflict with Python's builtin names but gmpy2
    does use names that may conflict with other modules or variable names.

.. note::
   `mpz` ignores all embedded underscore characters. It does not attempt to be
   100% compatible with all Python exceptions.

mpz type
--------

.. autoclass:: mpz
   :special-members: __format__

mpz Functions
-------------

.. autofunction:: bincoef
.. autofunction:: bit_clear
.. autofunction:: bit_count
.. autofunction:: bit_flip
.. autofunction:: bit_length
.. autofunction:: bit_mask
.. autofunction:: bit_scan0
.. autofunction:: bit_scan1
.. autofunction:: bit_set
.. autofunction:: bit_test
.. autofunction:: c_div
.. autofunction:: c_div_2exp
.. autofunction:: c_divmod
.. autofunction:: c_divmod_2exp
.. autofunction:: c_mod
.. autofunction:: c_mod_2exp
.. autofunction:: comb
.. autofunction:: divexact
.. autofunction:: divm
.. autofunction:: double_fac
.. autofunction:: f_div
.. autofunction:: f_div_2exp
.. autofunction:: f_divmod
.. autofunction:: f_divmod_2exp
.. autofunction:: f_mod
.. autofunction:: f_mod_2exp
.. autofunction:: fac
.. autofunction:: fib
.. autofunction:: fib2
.. autofunction:: gcd
.. autofunction:: gcdext
.. autofunction:: hamdist
.. autofunction:: invert
.. autofunction:: iroot
.. autofunction:: iroot_rem
.. autofunction:: is_congruent
.. autofunction:: is_divisible
.. autofunction:: is_even
.. autofunction:: is_odd
.. autofunction:: is_power
.. autofunction:: is_prime
.. autofunction:: is_probab_prime
.. autofunction:: is_square
.. autofunction:: isqrt
.. autofunction:: isqrt_rem
.. autofunction:: jacobi
.. autofunction:: kronecker
.. autofunction:: lcm
.. autofunction:: legendre
.. autofunction:: lucas
.. autofunction:: lucas2
.. autofunction:: mpz_random
.. autofunction:: mpz_rrandomb
.. autofunction:: mpz_urandomb
.. autofunction:: multi_fac
.. autofunction:: next_prime
.. autofunction:: num_digits
.. autofunction:: popcount
.. autofunction:: powmod
.. autofunction:: powmod_exp_list
.. autofunction:: powmod_base_list
.. autofunction:: powmod_sec
.. autofunction:: primorial
.. autofunction:: remove
.. autofunction:: t_div
.. autofunction:: t_div_2exp
.. autofunction:: t_divmod
.. autofunction:: t_divmod_2exp
.. autofunction:: t_mod
.. autofunction:: t_mod_2exp
