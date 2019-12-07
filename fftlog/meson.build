#######################################################################
# Global project info

project( 'fftlog',
         'fortran',
         default_options : [ 'buildtype=release',
                             'warning_level=0',
                             'prefix=' + meson.source_root() + '/install',
                             'libdir=lib' ] )

root = meson.source_root()

fc = meson.get_compiler( 'fortran' )

fc_args = [ '-fsyntax-only' ]

foreach fc_arg : fc_args
if fc.has_argument( fc_arg )
add_global_arguments( fc_arg,
                      language : 'fortran' )
endif
endforeach

#######################################################################
# Make shared library

fftlog_lib = library( 'fftlog',
                      [ 'cdgamma.f',
                        'drfftb.f',
                        'drfftf.f',
                        'drffti.f',
                        'fftlog.f' ],
                      install : true )

fftlog_dep = declare_dependency( link_with : fftlog_lib )

#######################################################################
# PKG-CONFIG

pkg_mod = import( 'pkgconfig' )
pkg_mod.generate( libraries: fftlog_lib,
                  version: '13.04.00',
                  name: 'FFTLog',
                  filebase: 'fftlog',
                  description: 'A code to take the fast Fourier' +
                  ' or Hankel transform of a discrete periodic sequence' +
                  ' of logarithmically spaced points.' )

#######################################################################

