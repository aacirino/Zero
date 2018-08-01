libzcash_src = [
  'IncrementalMerkleTree.cpp',
  'NoteEncryption.cpp',
  'Address.cpp',
  'JoinSplit.cpp',
  'Proof.cpp',
  'Note.cpp',
  'prf.cpp',
  'util.cpp' ]

zcash_inc_dir = include_directories('../snark/', '../snark/libsnark/')

crypto_static_lib = static_library('zcash',
sources : [libzcash_src],
  cpp_pch : 'pch/zcash_pch.hpp',
  include_directories : [ zero_inc_dirs, zcash_inc_dir ],
  cpp_args : [ '-fPIC', '-DBINARY_OUTPUT', '-DCURVE_ALT_BN128', '-DBOOST_SPIRIT_THREADSAFE', '-DHAVE_BUILD_INFO', '-D__STDC_FORMAT_MACROS', '-pipe', '-O1', '-g', '-Wstack-protector', '-fstack-protector-all', '-fPIE', '-fvisibility=hidden', '-DSTATIC'])
