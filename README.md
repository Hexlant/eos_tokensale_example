# eos_tokensale_example

Build
$ eosiocpp -o eos_tokensale_example.wast eos_tokensale_example.cpp

$ eosiocpp -g eos_tokensale_example.abi eos_tokensale_example.cpp

Deploy Contract
$ ./cleos.sh set contract [@Contract Account] ~/{path}/eos_tokensale_example -p [@Contract Account]


Usage
  Create Sale
  
$ ./cleos.sh push action hellotestman salestart '["eoscointoken","100.0000 CLUB","1"]' -p hellotestman

$ ./cleos.sh push action [@sale Contract] startsale '[ [@token Contract], [sale cap], [exchange rate]]' -p [@sale Contract]

  Buy Token
  Transfer EOS token to sale contract
  
$ ./cleos.sh push action eosio.token transfer '["clubmateshot", "hellotestman", "1.0000 EOS", ""]' -p clubmateshot


