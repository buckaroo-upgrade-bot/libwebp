include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'imageio',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('imageio', '*.h'),
  ]),
  headers = subdir_glob([
    ('src', '**/*.h'),
  ]),
  srcs = glob([
    'imageio/*.c',
  ]),
  deps = BUCKAROO_DEPS, 
)

cxx_library(
  name = 'webp',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('src', 'webp/decode.h'), 
    ('src', 'webp/demux.h'), 
    ('src', 'webp/encode.h'), 
    ('src', 'webp/mux.h'), 
    ('src', 'webp/mux_types.h'), 
    ('src', 'webp/types.h'), 
  ]), 
  headers = subdir_glob([
    ('src', '**/*.h'),
  ]),
  srcs = glob([
    'src/**/*.c',
  ]),
  visibility = [
    'PUBLIC',
  ],
  deps = [
    ':imageio',
  ] + BUCKAROO_DEPS,
)
