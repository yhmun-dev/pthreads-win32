project('pthreads-w32', 'c',
          version: '2.8.0',
          license: 'LGPL-2.1',
    license_files: 'COPYING.LIB',
    meson_version: '>= 1.1.0')

proj_name = meson.project_name()
proj_ver = meson.project_version()
prefix = get_option('prefix')
inc_dirs = include_directories('.', 'include')
dat_dir = prefix / get_option('datadir')
bin_dir = prefix / get_option('bindir')
lib_dir = prefix / get_option('libdir')

subdir('src')

pthreads_lib = static_library(proj_name,
                sources: lib_sources,
    include_directories: inc_dirs,
            install_dir: lib_dir,
                install: true)

pthreads_dep = declare_dependency(
              link_with: pthreads_lib,
    include_directories: inc_dirs)

if get_option('enable_test')
    subdir('tests')
endif

install_data(meson.project_license_files(),
            install_dir: prefix / 'licenses' / proj_name)

install_subdir('include',
            install_dir: prefix / proj_name)
