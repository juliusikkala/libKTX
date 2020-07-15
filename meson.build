project(
  'ktx',
  ['c'],
  default_options : [
    'buildtype=debugoptimized',
    'warning_level=1'
  ]
)

src = [
    'lib/checkheader.c',
    'lib/filestream.c',
    'lib/hashlist.c',
    'lib/memstream.c',
    'lib/swap.c',
    'lib/texture.c',
    'lib/writer1.c',
    'lib/writer2.c',
    'lib/vk_funcs.c',
    'lib/vkformat_check.c',
    'lib/texture.c',
    'lib/texture1.c',
    'lib/texture2.c',
    'lib/vkformat_str.c',
    'lib/dfdutils/vk2dfd.c',
    'lib/dfdutils/interpretdfd.c',
    'lib/dfdutils/queries.c',
    'lib/dfdutils/createdfd.c',
    'lib/vkloader.c',
]

cc = meson.get_compiler('c')
m_dep = cc.find_library('m', required : false)
dl_dep = cc.find_library('dl', required : false)
zstd_dep = dependency('libzstd')

incdir = include_directories([ 'include', 'lib' ])
dep_inc = include_directories([ 'include' ])

libktx = shared_library(
  'ktx',
  src,
  include_directories: [incdir],
  dependencies: [m_dep, dl_dep, zstd_dep],
  install: true,
  c_args: [
    '-DSUPPORT_SOFTWARE_ETC_UNPACK=0',
    '-DLIBKTX=1',
  ]
)

ktx_dep = declare_dependency(
  include_directories : dep_inc,
  dependencies: [m_dep, dl_dep, zstd_dep],
  link_with : libktx
)

