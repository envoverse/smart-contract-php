# smart-contract-php

### Installation
``composer install``
needed with the packages listed in composer.json

*Do not forget to set your INFURA ID in line 75* 

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
