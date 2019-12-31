project(
  'ktx',
  ['c'],
  default_options : [
    'buildtype=debugoptimized',
    'warning_level=0'
  ]
)

src = [
    'lib/checkheader.c',
    'lib/errstr.c',
    'lib/filestream.c',
    'lib/glloader.c',
    'lib/hashlist.c',
    'lib/hashtable.c',
    'lib/memstream.c',
    'lib/swap.c',
    'lib/texture.c',
    'lib/writer.c',
    'lib/writer_v1.c'
]

gl_dep = dependency('GL')
incdir = include_directories([ 'include' ])

deps = [
    gl_dep
]

dep_inc = include_directories([ 'include' ])

libktx = static_library(
  'ktx',
  src,
  dependencies: deps,
  include_directories: [incdir],
  install: true,
  c_args: [
    '-DKTX_OPENGL=1',
    '-DSUPPORT_SOFTWARE_ETC_UNPACK=0',
  ]
)

ktx_dep = declare_dependency(
  include_directories : dep_inc,
  link_with : libktx,
  dependencies: deps
)

