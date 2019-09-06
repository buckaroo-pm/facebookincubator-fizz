load('//:subdir_glob.bzl', 'subdir_glob')
load('//:buckaroo_macros.bzl', 'buckaroo_deps')

cxx_library(
  name = 'fizz',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('', 'fizz/**/*.h'),
  ]),
  srcs = glob([
    'fizz/**/*.cpp',
  ], exclude = glob([
    'fizz/**/test/**/*.cpp',
    'fizz/tool/**/*.cpp',
    'fizz/extensions/**/*.cpp',
    'fizz/protocol/Brotli*.cpp',
  ])),
  licenses = [
    'LICENSE',
  ],
  deps = buckaroo_deps(),
  visibility = [
    'PUBLIC',
  ],
)
