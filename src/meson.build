subdir('crypto')
subdir('zmq')
subdir('zcash')

libsodium_dep = dependency('libsodium')

zerod_inc_dir = include_directories('crypto')

zerod_src = [
  'sendalert.cpp',
  'addrman.cpp',
  'alert.cpp',
  'alertkeys.h',
  'asyncrpcoperation.cpp',
  'asyncrpcqueue.cpp',
  'bloom.cpp',
  'chain.cpp',
  'checkpoints.cpp',
  'deprecation.cpp',
  'httprpc.cpp',
  'httpserver.cpp',
  'init.cpp',
  'leveldbwrapper.cpp',
  'main.cpp',
  'merkleblock.cpp',
  'metrics.cpp',
  'miner.cpp',
  'net.cpp',
  'noui.cpp',
  'paymentdisclosure.cpp',
  'paymentdisclosuredb.cpp',
  'policy/fees.cpp',
  'pow.cpp',
  'rest.cpp',
  'rpcblockchain.cpp',
  'rpcmining.cpp',
  'rpcmisc.cpp',
  'rpcnet.cpp',
  'rpcrawtransaction.cpp',
  'rpcserver.cpp',
  'script/sigcache.cpp',
  'timedata.cpp',
  'torcontrol.cpp',
  'txdb.cpp',
  'txmempool.cpp',
  'validationinterface.cpp' ]

bitcoin_server_inc = include_directories(
  'policy',
  'zcash',
  'univalue/include',
  'leveldb/include',
  'leveldb/helpers/memenv',
  'snark')

bitcoin_server_src = [
  'sendalert.cpp',
  'addrman.cpp',
  'alert.cpp',
  'asyncrpcoperation.cpp',
  'asyncrpcqueue.cpp',
  'bloom.cpp',
  'chain.cpp',
  'checkpoints.cpp',
  'deprecation.cpp',
  'httprpc.cpp',
  'httpserver.cpp',
  'init.cpp',
  'leveldbwrapper.cpp',
  'main.cpp',
  'merkleblock.cpp',
  'metrics.cpp',
  'miner.cpp',
  'net.cpp',
  'noui.cpp',
  'paymentdisclosure.cpp',
  'paymentdisclosuredb.cpp',
  'policy/fees.cpp',
  'pow.cpp',
  'rest.cpp',
  'rpcblockchain.cpp',
  'rpcmining.cpp',
  'rpcmisc.cpp',
  'rpcnet.cpp',
  'rpcrawtransaction.cpp',
  'rpcserver.cpp',
  'script/sigcache.cpp',
  'timedata.cpp',
  'torcontrol.cpp',
  'txdb.cpp',
  'txmempool.cpp',
  'validationinterface.cpp' ]

if meson.get_compiler('c').get_id() == 'clang'
  extra_args = ['-DHAVE_DECL_STRNLEN=1']
else
  extra_args = []
endif

bitcoin_server_lib = static_library('bitcoin_server',
  sources : bitcoin_server_src,
  include_directories : [ bitcoin_server_inc ],
  cpp_pch : 'pch/bitcoin_server_pch.hpp',
  cpp_args : extra_args)

# executable('zerod', sources : [zerod_src],
#   cpp_pch : 'pch/zerod_pch.hpp',
#   # include_directories : [zerod_inc_dir],
#   cpp_args : [ '-DENABLE_MINING' ])
