crypto_src = [  'equihash.cpp',
                'hmac_sha256.cpp',
                'hmac_sha512.cpp',
                'ripemd160.cpp',
                'sha1.cpp',
                'sha256.cpp',
                'sha512.cpp' ]

crypto_static_lib = static_library('bitcoin_crypto',
sources : [ crypto_src ],
  cpp_pch : 'pch/crypto_pch.hpp',
  include_directories : [ zero_inc_dirs ],
  cpp_args : '-DENABLE_MINING')
