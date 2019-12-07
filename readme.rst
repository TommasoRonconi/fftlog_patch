Meson Build patch for FFTLog
============================

This repo just contains the `meson.build` script for installing FFTLog with
the Meson build system tool.

Description of FFTLog from the FFTLog-Website
---------------------------------------------

FFTLog is a set of fortran subroutines that compute the fast Fourier or Hankel
(= Fourier-Bessel) transform of a periodic sequence of logarithmically spaced
points.

FFTLog can be regarded as a natural analogue to the standard Fast Fourier
Transform (FFT), in the sense that, just as the normal FFT gives the exact (to
machine precision) Fourier transform of a linearly spaced periodic sequence, so
also FFTLog gives the exact Fourier or Hankel transform, of arbitrary order m,
of a logarithmically spaced periodic sequence.

FFTLog shares with the normal FFT the problems of ringing (response to sudden
steps) and aliasing (periodic folding of frequencies), but under appropriate
circumstances FFTLog may approximate the results of a continuous Fourier or
Hankel transform.

The FFTLog algorithm was originally proposed by [Talman_1978]_.

*For the full documentation, see*
`casa.colorado.edu/~ajsh/FFTLog <http://casa.colorado.edu/~ajsh/FFTLog>`_.

License and Credits
-------------------

Credits commented in the original code:

`FFTLog` uses the NCAR suite of FFT routines, and a modified version of the
complex Gamma function from the gamerf package at
`momonga.t.u-tokyo.ac.jp/~ooura/gamerf.html
<http://momonga.t.u-tokyo.ac.jp/~ooura/gamerf.html>`_.
The original gamerf copyright statement states::

   Copyright(C) 1996 Takuya OOURA (email: ooura@mmm.t.u-tokyo.ac.jp).
   You may use, copy, modify this code for any purpose and
   without fee. You may distribute this ORIGINAL package.

Permission to distribute the modified gamma function code with the FFTLog
package has been granted (email from Takuya Ooura to Andrew Hamilton dated 16
March 1999).
