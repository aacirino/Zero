libzmq_src = [
  'zmqabstractnotifier.cpp',
  'zmqnotificationinterface.cpp',
  'zmqpublishnotifier.cpp' ]

crypto_static_lib = static_library('libbitcoin_zmq',
sources : [libzmq_src],
  cpp_pch : 'pch/libzmq_pch.hpp',
  include_directories : [ zero_inc_dirs ])
