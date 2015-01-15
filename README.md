# piratize

The specification for piratization is outlined below.

- Strings should be translated to "pirish", consider looking at the talk_like_a_pirate gem
- The following should be removed from any instances of Strings: "gold", "treasure", "coin", "coins"
- Hashes and Arrays should be recursively processed, and their values (but not keys) also "piratized"
- Any floats should be converted to the nearest rational where 8 is the denominator, eg 2.5 becomes 20/8 and 0.3 becomes 2/8
- Any values are passed to a block if one is provided for additional processing
- If it encounters an instance that includes the module Ship it should call #board! on it
- If #board! raises PartyRepelledError it should replace the instance with a new instance of ShipWreck
- If #board! raises NoTreasureError it should print "Ya! No treasure were found me 'earty!" and continue
- Symbols should raise WhatBeThisError with the message "'Ere, what be a 'symbol'"
- Version controlled with git
- You may use any 3rd party code you wish, ideally gems will be managed with bundler
- Available as a class method, eg Piratize.process my_object
- Available as a module that can be added to any classes
- Available as a method on the Ruby classes: String, Hash, Array, Float
