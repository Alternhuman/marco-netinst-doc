marco-minimal
=============

Owing to the fact that the MarcoPolo implementation reference is written in Python, it seemed a burden to include the Python interpreter and its dependencies inside the minimal OS image. marco-minimal is a C/C++ implementation of a subset of the Marco functionality that has no dependencies (other than the standard C and C++ libraries).

The most notable difference is the lack of a bindable local Marco instance. In order to reduce the overload, the executable multicasts the Marco commands itself, without requesting a centralized daemon to do the work.

The API is kept intact, except for some optional parameters that have not been included. The :ref:`reference <marcominimalreference>` covers the technical details of the implementation. 