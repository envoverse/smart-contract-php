# smart-contract-php

### Installation
``composer install``
needed with the packages listed in composer.json

* Do not forget to set the right contract address in line 18
* Also add the write ABI code from your contract then in line 15
* Do not forget to set your INFURA ID in line 75

After installation, adjust the code and look for the accepted commands.
The script is called via GET or POST and delivers JSON results to the caller
for your finest AJAX moments.

``https://localhost/contract.php?c=totasup&w=YOUR_ETH_WALLET&p=OTIONAL_PARAMS``

The contract address is in LINE #18!

### Reasoning
Here a simple PHP script, that is talking to our ENVOVERSE.com smart contract
with a few simple commands (balanceOf, totalSupply, ...)
and most importantly takes a Javascript SIGNED value and extracts the wallet
from the signed value:

In line #63ff:

``
$sigWallet = personal_ecRecover($message, $commandPara);
``

Needed some time to figure that out, so here we go.

Uses the INFURA API to talk to the Blockchain!
