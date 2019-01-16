load('//:subdir_glob.bzl', 'subdir_glob')
load('//:buckaroo_macros.bzl', 'buckaroo_deps')

# cxx_library(
#   name = 'imageio',
#   header_namespace = '',
#   exported_headers = subdir_glob([
#     ('imageio', '*.h'),
#   ]),
#   headers = subdir_glob([
#     ('src', '**/*.h'),
#   ]),
#   srcs = glob([
#     'imageio/*.c',
#   ]),
#   deps = buckaroo_deps(),
# )

cxx_library(
  name = 'webp',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('imageio', '*.h'),
    ('src', 'webp/decode.h'),
    ('src', 'webp/demux.h'),
    ('src', 'webp/encode.h'),
    ('src', 'webp/mux.h'),
    ('src', 'webp/mux_types.h'),
    ('src', 'webp/types.h'),
  ]),
  headers = subdir_glob([
    ('', 'src/**/*.h'),
    ('src', '**/*.h'),
  ]),
  srcs = glob([
    'src/**/*.c',
    'imageio/*.c',
  ]),
  reexport_all_header_dependencies = False,
  visibility = [
    'PUBLIC',
  ],
  deps = [
    # ':imageio',
  ] + buckaroo_deps(),
)
