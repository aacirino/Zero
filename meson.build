project('zero', 'c', 'cpp',
  default_options : [ 'cpp_std=c++17', 'warning_level=1', 'b_sanitize=address,undefined' ],
  version : '1.0.14-1',
  license : 'MIT')

add_global_arguments('-DMULTICORE=1', '-fopenmp', language : 'cpp')

tcc_gen = generator(find_program('cp'),
  output : '@BASENAME@_tcc.cpp',
  arguments : ['@INPUT@'])

thread_dep = dependency('threads')

zero_inc_dirs = include_directories(
  '/usr/local/include',
  '/usr/include',
  'src',
  '/usr/local/include/sodium')

test_inc_dirs = include_directories(
  '/usr/local/include',
  '/usr/local/include/catch',
  '/usr/include')

subdir('src')

pkg_mod = import('pkgconfig')
