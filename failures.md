[Blin](https://github.com/Raku/Blin) results between 2026.08 ([24e6e53](https://github.com/rakudo/rakudo/commit/24e6e5312f2868680413b0597aef8772f6b5bcea)) and b83057b10c ([b83057b](https://github.com/rakudo/rakudo/commit/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8)):

* [ ] [Polyglot::Regexen](https://raku.land/zef:guifa/Polyglot::Regexen) – Fail, Bisected: [aab0778](https://github.com/rakudo/rakudo/commit/aab0778725da5848824f07514c0ae355d972926a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p637754-i645503.service; invocation ID: 43539e535c1b4f00b5d26bbb5459c1ea
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Polyglot::Regexen
  ===> Found: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> [via Zef::Repository::Ecosystems<fez>]
  [Polyglot::Regexen] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789650841.637755.5690.040414612839/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz https://360.zef.pm/P/OL/POLYGLOT_REGEXEN/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Fetching [OK]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> to /home/coke/sandbox/blin/data/zef-data/tmp/1789650841.637755.5690.040414612839/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  [Polyglot::Regexen] Command: tar -t -f ./17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  [Polyglot::Regexen] Command: tar -xvf ./17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz -C ../17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Extraction [OK]: Polyglot::Regexen to /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Testing: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/00-sanity.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] 1..1
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/01-literals.rakutest
  [Polyglot::Regexen] ok 1 - Single literal, alpha
  [Polyglot::Regexen] ok 2 - Double literal
  [Polyglot::Regexen] ok 3 - Single literal, digit
  [Polyglot::Regexen] ok 4 - ECMA literal, Raku escaped
  [Polyglot::Regexen] ok 5 - ECMA literal sequence, Raku sequence with embedded escaped
  [Polyglot::Regexen] ok 6 - Hex escape sequence, Raku literal
  [Polyglot::Regexen] ok 7 - Unicode escape sequence, Raku literal
  [Polyglot::Regexen] ok 8 - Hex escape sequence, Raku escaped
  [Polyglot::Regexen] ok 9 - Unicode escape sequence, Raku escaped
  [Polyglot::Regexen] 1..9
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/02-character-classes.rakutest
  [Polyglot::Regexen] ok 1 - Hyphen as sole character
  [Polyglot::Regexen] ok 2 - Hyphen as first character
  [Polyglot::Regexen] ok 3 - Hyphen as final character
  [Polyglot::Regexen] ok 4 - Range after literal
  [Polyglot::Regexen] ok 5 - Range before literal
  [Polyglot::Regexen] ok 6 - Sequential range
  [Polyglot::Regexen] 1..6
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/03-alternation.rakutest
  [Polyglot::Regexen] ok 1 - Simple alternation, two terms
  [Polyglot::Regexen] ok 2 - Simple alternation, three terms
  [Polyglot::Regexen] 1..2
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/04-assertions.rakutest
  [Polyglot::Regexen] ok 1 - Simple lookahead
  [Polyglot::Regexen] ok 2 - Simple negative lookahead
  [Polyglot::Regexen] ok 3 - Simple lookbehind
  [Polyglot::Regexen] ok 4 - Simple negative lookbehind
  [Polyglot::Regexen] 1..4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/05-quantifiers.rakutest
  [Polyglot::Regexen] ok 1 - One or none
  [Polyglot::Regexen] ok 2 - One or more
  [Polyglot::Regexen] ok 3 - None or more
  [Polyglot::Regexen] ok 4 - Exactly some number
  [Polyglot::Regexen] ok 5 - Some number or more
  [Polyglot::Regexen] ok 6 - Some number to another number
  [Polyglot::Regexen] ok 7 - Frugal one or none
  [Polyglot::Regexen] ok 8 - Frugal one or more
  [Polyglot::Regexen] ok 9 - Frugal none or more
  [Polyglot::Regexen] ok 10 - Frugal exactly some number
  [Polyglot::Regexen] ok 11 - Frugal some number or more
  [Polyglot::Regexen] ok 12 - Frugal some number to another number
  [Polyglot::Regexen] 1..12
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/06-captures.rakutest
  [Polyglot::Regexen] ok 1 - Simple positional
  [Polyglot::Regexen] ok 2 - Embedded positional
  [Polyglot::Regexen] ok 3 - Sequential positional
  [Polyglot::Regexen] ok 4 - Complex positional
  [Polyglot::Regexen] ok 5 - Simple named
  [Polyglot::Regexen] ok 6 - Simple named with simple positional
  [Polyglot::Regexen] 1..6
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/07-unicode.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] ok 2 - 
  [Polyglot::Regexen] ok 3 - 
  [Polyglot::Regexen] ok 4 - 
  [Polyglot::Regexen] ok 5 - 
  [Polyglot::Regexen] ok 6 - 
  [Polyglot::Regexen] ok 7 - 
  [Polyglot::Regexen] ok 8 - 
  [Polyglot::Regexen] ok 9 - 
  [Polyglot::Regexen] ok 10 - 
  [Polyglot::Regexen] ok 11 - 
  [Polyglot::Regexen] ok 12 - 
  [Polyglot::Regexen] 1..12
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/08-modifiers.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] ok 2 - 
  [Polyglot::Regexen] ok 3 - 
  [Polyglot::Regexen] ok 4 - 
  [Polyglot::Regexen] 1..4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/09-role.rakutest
  [Polyglot::Regexen] # Subtest: Pretty print
  [Polyglot::Regexen]     ok 1 - 
  [Polyglot::Regexen]     ok 2 - 
  [Polyglot::Regexen]     ok 3 - 
  [Polyglot::Regexen]     1..3
  [Polyglot::Regexen] ok 1 - Pretty print
  [Polyglot::Regexen] # Subtest: Match variable functionality
  [Polyglot::Regexen]     ok 1 - 
  [Polyglot::Regexen]     ok 2 - 
  [Polyglot::Regexen]     ok 3 - 
  [Polyglot::Regexen]     ok 4 - 
  [Polyglot::Regexen]     ok 5 - 
  [Polyglot::Regexen]     ok 6 - 
  [Polyglot::Regexen]     ok 7 - 
  [Polyglot::Regexen]     1..7
  [Polyglot::Regexen] ok 2 - Match variable functionality
  [Polyglot::Regexen] # Subtest: Positional matches
  [Polyglot::Regexen]     ok 1 - Sequential
  [Polyglot::Regexen]     ok 2 - Simple embedded
  [Polyglot::Regexen]     ok 3 - Deep right embedded
  [Polyglot::Regexen]     ok 4 - Deep left embedded
  [Polyglot::Regexen]     ok 5 - Complex embedded
  [Polyglot::Regexen]     1..5
  [Polyglot::Regexen] ok 3 - Positional matches
  [Polyglot::Regexen] # Subtest: Named matches
  [Polyglot::Regexen]     ok 1 - Sequential
  [Polyglot::Regexen]     ok 2 - Simple embedded
  [Polyglot::Regexen]     ok 3 - Deep right embedded
  [Polyglot::Regexen]     ok 4 - Deep left embedded
  [Polyglot::Regexen] IO::Handle<IO::Special.new("<STDERR>")>(opened){a => a, b => ab, c => cdef, d => d, e => de, g => abcdefgh, h => h, i => abcdefghi}
  [Polyglot::Regexen]     ok 5 - Complex embedded
  [Polyglot::Regexen]     1..5
  [Polyglot::Regexen] ok 4 - Named matches
  [Polyglot::Regexen] # Subtest: Positional match backreferences
  [Polyglot::Regexen]     ok 1 - Sequential
  [Polyglot::Regexen]     ok 2 - Simple embedded
  [Polyglot::Regexen]     ok 3 - Deep right embedded
  [Polyglot::Regexen]     ok 4 - Deep left embedded
  [Polyglot::Regexen]     ok 5 - Complex embedded
  [Polyglot::Regexen]     ok 6 - Multi sequential
  [Polyglot::Regexen]     1..6
  [Polyglot::Regexen] ok 5 - Positional match backreferences
  [Polyglot::Regexen] # Subtest: Named match backreferences
  [Polyglot::Regexen]     ok 1 - Sequential
  [Polyglot::Regexen]     ok 2 - Simple embedded
  [Polyglot::Regexen]     ok 3 - Deep right embedded
  [Polyglot::Regexen]     ok 4 - Deep left embedded
  [Polyglot::Regexen]     ok 5 - Complex embedded
  [Polyglot::Regexen]     ok 6 - Multi sequential
  [Polyglot::Regexen]     1..6
  [Polyglot::Regexen] ok 6 - Named match backreferences
  [Polyglot::Regexen] 1..6
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/10-usage.rakutest
  [Polyglot::Regexen] # Subtest: Quoted forms
  [Polyglot::Regexen]     ok 1 - No modifiers in bare quoted form
  [Polyglot::Regexen]     ok 2 - Postquote case-insensitive bare quoted form
  [Polyglot::Regexen]     ok 3 - Prequote case-insensitive bare quoted form
  [Polyglot::Regexen]     1..3
  [Polyglot::Regexen] ok 1 - Quoted forms
  [Polyglot::Regexen] # Subtest: Grammar-scoped forms
  [Polyglot::Regexen]     ok 1 - Base regex in grammar
  [Polyglot::Regexen]     ok 2 - Regex with case-insensitive modifier in grammar
  [Polyglot::Regexen]     ok 3 - Yes, that’s really an e-mail regex
  [Polyglot::Regexen]     1..3
  [Polyglot::Regexen] ok 2 - Grammar-scoped forms
  [Polyglot::Regexen] # Subtest: Lexically-scoped forms
  [Polyglot::Regexen]     ok 1 - My scoped regex
  [Polyglot::Regexen]     ok 2 - My-scoped regex in package
  [Polyglot::Regexen]     ok 3 - Our-scoped regex in own package
  [Polyglot::Regexen]     ok 4 - My-scoped regex in package not visible from outside
  [Polyglot::Regexen]     ok 5 - Our-scoped regex in package not immediately visible from outside
  [Polyglot::Regexen]     ok 6 - My-scoped regex in package not visible from outside with package name
  [Polyglot::Regexen]     ok 7 - Our-scoped regex in package visible visible from outside with package name
  [Polyglot::Regexen]     1..7
  [Polyglot::Regexen] ok 3 - Lexically-scoped forms
  [Polyglot::Regexen] 1..3
  ===> Testing [OK] for Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  ===> Installing: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  ===> Install [OK] for Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 25.727s
               CPU time consumed: 38.521s
                     Memory peak: 1.5G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p636215-i607871.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Polyglot::Regexen
  ===> Found: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> [via Zef::Repository::Ecosystems<fez>]
  [Polyglot::Regexen] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789650809.636217.1359.954927520991/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz https://360.zef.pm/P/OL/POLYGLOT_REGEXEN/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Fetching [OK]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> to /home/coke/sandbox/blin/data/zef-data/tmp/1789650809.636217.1359.954927520991/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  [Polyglot::Regexen] Command: tar -t -f ./17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  [Polyglot::Regexen] Command: tar -xvf ./17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz -C ../17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Extraction [OK]: Polyglot::Regexen to /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Testing: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/00-sanity.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] 1..1
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/01-literals.rakutest
  [Polyglot::Regexen] ok 1 - Single literal, alpha
  [Polyglot::Regexen] ok 2 - Double literal
  [Polyglot::Regexen] ok 3 - Single literal, digit
  [Polyglot::Regexen] ok 4 - ECMA literal, Raku escaped
  [Polyglot::Regexen] ok 5 - ECMA literal sequence, Raku sequence with embedded escaped
  [Polyglot::Regexen] ok 6 - Hex escape sequence, Raku literal
  [Polyglot::Regexen] ok 7 - Unicode escape sequence, Raku literal
  [Polyglot::Regexen] ok 8 - Hex escape sequence, Raku escaped
  [Polyglot::Regexen] ok 9 - Unicode escape sequence, Raku escaped
  [Polyglot::Regexen] 1..9
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/02-character-classes.rakutest
  [Polyglot::Regexen] not ok 1 - Hyphen as sole character
  [Polyglot::Regexen] # Failed test 'Hyphen as sole character'
  [Polyglot::Regexen] # at t/ecma/02-character-classes.rakutest line 47
  [Polyglot::Regexen] # expected: '/<+[-]>/'
  [Polyglot::Regexen] #      got: '/<+[\-]>/'
  [Polyglot::Regexen] not ok 2 - Hyphen as first character
  [Polyglot::Regexen] # Failed test 'Hyphen as first character'
  [Polyglot::Regexen] # at t/ecma/02-character-classes.rakutest line 48
  [Polyglot::Regexen] # expected: '/<+[- a]>/'
  [Polyglot::Regexen] #      got: '/<+[\- a]>/'
  [Polyglot::Regexen] not ok 3 - Hyphen as final character
  [Polyglot::Regexen] # Failed test 'Hyphen as final character'
  [Polyglot::Regexen] # at t/ecma/02-character-classes.rakutest line 49
  [Polyglot::Regexen] # expected: '/<+[a -]>/'
  [Polyglot::Regexen] #      got: '/<+[a \-]>/'
  [Polyglot::Regexen] ok 4 - Range after literal
  [Polyglot::Regexen] ok 5 - Range before literal
  [Polyglot::Regexen] ok 6 - Sequential range
  [Polyglot::Regexen] 1..6
  [Polyglot::Regexen] # You failed 3 tests of 6
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/03-alternation.rakutest
  [Polyglot::Regexen] ok 1 - Simple alternation, two terms
  [Polyglot::Regexen] ok 2 - Simple alternation, three terms
  [Polyglot::Regexen] 1..2
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/04-assertions.rakutest
  [Polyglot::Regexen] ok 1 - Simple lookahead
  [Polyglot::Regexen] ok 2 - Simple negative lookahead
  [Polyglot::Regexen] ok 3 - Simple lookbehind
  [Polyglot::Regexen] ok 4 - Simple negative lookbehind
  [Polyglot::Regexen] 1..4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/05-quantifiers.rakutest
  [Polyglot::Regexen] ok 1 - One or none
  [Polyglot::Regexen] ok 2 - One or more
  [Polyglot::Regexen] ok 3 - None or more
  [Polyglot::Regexen] ok 4 - Exactly some number
  [Polyglot::Regexen] ok 5 - Some number or more
  [Polyglot::Regexen] ok 6 - Some number to another number
  [Polyglot::Regexen] ok 7 - Frugal one or none
  [Polyglot::Regexen] ok 8 - Frugal one or more
  [Polyglot::Regexen] ok 9 - Frugal none or more
  [Polyglot::Regexen] ok 10 - Frugal exactly some number
  [Polyglot::Regexen] ok 11 - Frugal some number or more
  [Polyglot::Regexen] ok 12 - Frugal some number to another number
  [Polyglot::Regexen] 1..12
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/06-captures.rakutest
  [Polyglot::Regexen] not ok 1 - Simple positional
  [Polyglot::Regexen] # Failed test 'Simple positional'
  [Polyglot::Regexen] # at t/ecma/06-captures.rakutest line 8
  [Polyglot::Regexen] # expected: '/[$<1>=[a]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }]/'
  [Polyglot::Regexen] #      got: '/[$1=[a]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }]/'
  [Polyglot::Regexen] not ok 2 - Embedded positional
  [Polyglot::Regexen] # Failed test 'Embedded positional'
  [Polyglot::Regexen] # at t/ecma/06-captures.rakutest line 11
  [Polyglot::Regexen] # expected: '/[$<1>=[a[$<2>=[b]{ $¢.register-position($/.AT-POS(2, :ECMA262-INTERNAL), 2) }]]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }]/'
  [Polyglot::Regexen] #      got: '/[$1=[a[$2=[b]{ $¢.register-position($/.AT-POS(2, :ECMA262-INTERNAL), 2) }]]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }]/'
  [Polyglot::Regexen] # Failed test 'Sequential positional'
  [Polyglot::Regexen] # at t/ecma/06-captures.rakutest line 14
  [Polyglot::Regexen] # expected: '/[$<1>=[a]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }][$<2>=[b]{ $¢.register-position($/.AT-POS(2, :ECMA262-INTERNAL), 2) }]/'
  [Polyglot::Regexen] #      got: '/[$1=[a]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }][$2=[b]{ $¢.register-position($/.AT-POS(2, :ECMA262-INTERNAL), 2) }]/'
  [Polyglot::Regexen] not ok 3 - Sequential positional
  [Polyglot::Regexen] not ok 4 - Complex positional
  [Polyglot::Regexen] # Failed test 'Complex positional'
  [Polyglot::Regexen] # at t/ecma/06-captures.rakutest line 17
  [Polyglot::Regexen] # expected: '/[$<1>=[a[$<2>=[b]{ $¢.register-position($/.AT-POS(2, :ECMA262-INTERNAL), 2) }]]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }][$<3>=[c]{ $¢.register-position($/.AT-POS(3, :ECMA262-INTERNAL), 3) }]/'
  [Polyglot::Regexen] #      got: '/[$1=[a[$2=[b]{ $¢.register-position($/.AT-POS(2, :ECMA262-INTERNAL), 2) }]]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }][$3=[c]{ $¢.register-position($/.AT-POS(3, :ECMA262-INTERNAL), 3) }]/'
  [Polyglot::Regexen] not ok 5 - Simple named
  [Polyglot::Regexen] # Failed test 'Simple named'
  [Polyglot::Regexen] # at t/ecma/06-captures.rakutest line 20
  [Polyglot::Regexen] # expected: '/[$<1>=[a]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }]/'
  [Polyglot::Regexen] #      got: '/[$1=[a]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }]/'
  [Polyglot::Regexen] not ok 6 - Simple named with simple positional
  [Polyglot::Regexen] # Failed test 'Simple named with simple positional'
  [Polyglot::Regexen] # at t/ecma/06-captures.rakutest line 23
  [Polyglot::Regexen] # expected: '/[$<1>=[a]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }][$<2>=[b]{ $¢.register-position($/.AT-POS(2, :ECMA262-INTERNAL), 2) }]/'
  [Polyglot::Regexen] #      got: '/[$1=[a]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }][$2=[b]{ $¢.register-position($/.AT-POS(2, :ECMA262-INTERNAL), 2) }]/'
  [Polyglot::Regexen] 1..6
  [Polyglot::Regexen] # You failed 6 tests of 6
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/07-unicode.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] ok 2 - 
  [Polyglot::Regexen] ok 3 - 
  [Polyglot::Regexen] ok 4 - 
  [Polyglot::Regexen] ok 5 - 
  [Polyglot::Regexen] ok 6 - 
  [Polyglot::Regexen] ok 7 - 
  [Polyglot::Regexen] ok 8 - 
  [Polyglot::Regexen] ok 9 - 
  [Polyglot::Regexen] ok 10 - 
  [Polyglot::Regexen] ok 11 - 
  [Polyglot::Regexen] ok 12 - 
  [Polyglot::Regexen] 1..12
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/08-modifiers.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] ok 2 - 
  [Polyglot::Regexen] ok 3 - 
  [Polyglot::Regexen] ok 4 - 
  [Polyglot::Regexen] 1..4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/09-role.rakutest
  [Polyglot::Regexen] # Subtest: Pretty print
  [Polyglot::Regexen]     ok 1 - 
  [Polyglot::Regexen]     ok 2 - 
  [Polyglot::Regexen]     ok 3 - 
  [Polyglot::Regexen]     1..3
  [Polyglot::Regexen] ok 1 - Pretty print
  [Polyglot::Regexen] # Subtest: Match variable functionality
  [Polyglot::Regexen]     ok 1 - 
  [Polyglot::Regexen]     ok 2 - 
  [Polyglot::Regexen]     ok 3 - 
  [Polyglot::Regexen]     ok 4 - 
  [Polyglot::Regexen]     ok 5 - 
  [Polyglot::Regexen]     ok 6 - 
  [Polyglot::Regexen]     ok 7 - 
  [Polyglot::Regexen]     1..7
  [Polyglot::Regexen] ok 2 - Match variable functionality
  [Polyglot::Regexen] # Subtest: Positional matches
  [Polyglot::Regexen]     ok 1 - Sequential
  [Polyglot::Regexen]     ok 2 - Simple embedded
  [Polyglot::Regexen]     ok 3 - Deep right embedded
  [Polyglot::Regexen]     ok 4 - Deep left embedded
  [Polyglot::Regexen]     ok 5 - Complex embedded
  [Polyglot::Regexen]     1..5
  [Polyglot::Regexen] ok 3 - Positional matches
  [Polyglot::Regexen] # Subtest: Named matches
  [Polyglot::Regexen]     ok 1 - Sequential
  [Polyglot::Regexen]     ok 2 - Simple embedded
  [Polyglot::Regexen]     ok 3 - Deep right embedded
  [Polyglot::Regexen]     ok 4 - Deep left embedded
  [Polyglot::Regexen] IO::Handle<IO::Special.new("<STDERR>")>(opened){a => a, b => ab, c => cdef, d => d, e => de, g => abcdefgh, h => h, i => abcdefghi}
  [Polyglot::Regexen]     ok 5 - Complex embedded
  [Polyglot::Regexen]     1..5
  [Polyglot::Regexen] ok 4 - Named matches
  [Polyglot::Regexen] # Subtest: Positional match backreferences
  [Polyglot::Regexen]     ok 1 - Sequential
  [Polyglot::Regexen]     ok 2 - Simple embedded
  [Polyglot::Regexen]     ok 3 - Deep right embedded
  [Polyglot::Regexen]     ok 4 - Deep left embedded
  [Polyglot::Regexen]     ok 5 - Complex embedded
  [Polyglot::Regexen]     ok 6 - Multi sequential
  [Polyglot::Regexen]     1..6
  [Polyglot::Regexen] ok 5 - Positional match backreferences
  [Polyglot::Regexen] # Subtest: Named match backreferences
  [Polyglot::Regexen]     ok 1 - Sequential
  [Polyglot::Regexen]     ok 2 - Simple embedded
  [Polyglot::Regexen]     ok 3 - Deep right embedded
  [Polyglot::Regexen]     ok 4 - Deep left embedded
  [Polyglot::Regexen]     ok 5 - Complex embedded
  [Polyglot::Regexen]     ok 6 - Multi sequential
  [Polyglot::Regexen]     1..6
  [Polyglot::Regexen] ok 6 - Named match backreferences
  [Polyglot::Regexen] 1..6
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/10-usage.rakutest
  [Polyglot::Regexen] # Subtest: Quoted forms
  [Polyglot::Regexen]     ok 1 - No modifiers in bare quoted form
  [Polyglot::Regexen]     ok 2 - Postquote case-insensitive bare quoted form
  [Polyglot::Regexen]     ok 3 - Prequote case-insensitive bare quoted form
  [Polyglot::Regexen]     1..3
  [Polyglot::Regexen] ok 1 - Quoted forms
  [Polyglot::Regexen] # Subtest: Grammar-scoped forms
  [Polyglot::Regexen]     ok 1 - Base regex in grammar
  [Polyglot::Regexen]     ok 2 - Regex with case-insensitive modifier in grammar
  [Polyglot::Regexen]     ok 3 - Yes, that’s really an e-mail regex
  [Polyglot::Regexen]     1..3
  [Polyglot::Regexen] ok 2 - Grammar-scoped forms
  [Polyglot::Regexen] # Subtest: Lexically-scoped forms
  [Polyglot::Regexen]     ok 1 - My scoped regex
  [Polyglot::Regexen]     ok 2 - My-scoped regex in package
  [Polyglot::Regexen]     ok 3 - Our-scoped regex in own package
  [Polyglot::Regexen]     ok 4 - My-scoped regex in package not visible from outside
  [Polyglot::Regexen]     ok 5 - Our-scoped regex in package not immediately visible from outside
  [Polyglot::Regexen]     ok 6 - My-scoped regex in package not visible from outside with package name
  [Polyglot::Regexen]     ok 7 - Our-scoped regex in package visible visible from outside with package name
  [Polyglot::Regexen]     1..7
  [Polyglot::Regexen] ok 3 - Lexically-scoped forms
  [Polyglot::Regexen] 1..3
  ===> Testing [FAIL]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  [Polyglot::Regexen] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  ===> Install [OK] for Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 33.550s
               CPU time consumed: 23.239s
                     Memory peak: 1.5G (swap: 0B)

  ```
  </details>
* [ ] [GLib](https://raku.land/cpan:CBWOOD/GLib) – Fail, Bisected: [6357ccf](https://github.com/rakudo/rakudo/commit/6357ccf97f2c4b1dd1067bf4f50b6cdcfdb78373)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p645603-i632872.service; invocation ID: 8ac8a39ff54d4c5fb1c5be53a051fdcb
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: GLib
  ===> Found: GLib:ver<0.0.11>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [GLib] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789651025.645604.3501.8684422383817/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/GLib/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: GLib:ver<0.0.11>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789651025.645604.3501.8684422383817/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [GLib] Command: tar -t -f ./GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [GLib] Command: tar -xvf ./GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz -C ../GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Extraction [OK]: GLib to /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Testing: GLib:ver<0.0.11>:auth<cpan:CBWOOD>
  [GLib] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/00-struct-sizes.t
  [GLib] 1..66
  [GLib] ok 1 - Structure sizes for GArray match
  [GLib] ok 2 - Structure sizes for GByteArray match
  [GLib] ok 3 - Structure sizes for GCClosure match
  [GLib] ok 4 - Structure sizes for GClosure match
  [GLib] ok 5 - Structure sizes for GCond match
  [GLib] ok 6 - Structure sizes for GDate match
  [GLib] ok 7 - Structure sizes for GDebugKey match
  [GLib] ok 8 - Structure sizes for GError match
  [GLib] ok 9 - Structure sizes for GHashTableIter match
  [GLib] ok 10 - Structure sizes for GHookList match
  [GLib] ok 11 - Structure sizes for GInterfaceInfo match
  [GLib] ok 12 - Structure sizes for GList match
  [GLib] ok 13 - Structure sizes for GLogField match
  [GLib] ok 14 - Structure 'GLogField-Str' is not to be tested
  [GLib] ok 15 - Structure sizes for GNode match
  [GLib] ok 16 - Structure sizes for GOnce match
  [GLib] ok 17 - Structure sizes for GOptionEntry match
  [GLib] ok 18 - Structure sizes for GParamSpec match
  [GLib] ok 19 - Structure sizes for GParamSpecBoolean match
  [GLib] ok 20 - Structure sizes for GParamSpecChar match
  [GLib] ok 21 - Structure sizes for GParamSpecDouble match
  [GLib] ok 22 - Structure sizes for GParamSpecEnum match
  [GLib] ok 23 - Structure sizes for GParamSpecFlags match
  [GLib] ok 24 - Structure sizes for GParamSpecFloat match
  [GLib] ok 25 - Structure sizes for GParamSpecInt match
  [GLib] ok 26 - Structure sizes for GParamSpecInt64 match
  [GLib] ok 27 - Structure sizes for GParamSpecLong match
  [GLib] ok 28 - Structure sizes for GParamSpecString match
  [GLib] ok 29 - Structure sizes for GParamSpecTypeInfo match
  [GLib] ok 30 - Structure sizes for GParamSpecUChar match
  [GLib] ok 31 - Structure sizes for GParamSpecUInt match
  [GLib] ok 32 - Structure sizes for GParamSpecUInt64 match
  [GLib] ok 33 - Structure sizes for GParamSpecULong match
  [GLib] ok 34 - Structure sizes for GParamSpecUnichar match
  [GLib] ok 35 - Structure sizes for GParamSpecValueArray match
  [GLib] ok 36 - Structure sizes for GParameter match
  [GLib] ok 37 - Structure 'GPollFD' is not to be tested
  [GLib] ok 38 - Structure 'GPollFDNonWin' is not to be tested
  [GLib] ok 39 - Structure 'GPollFDWin' is not to be tested
  [GLib] ok 40 - Structure sizes for GPtrArray match
  [GLib] ok 41 - Structure sizes for GQueue match
  [GLib] ok 42 - Structure sizes for GRecMutex match
  [GLib] ok 43 - Structure sizes for GSList match
  [GLib] ok 44 - Structure sizes for GSignalInvocationHint match
  [GLib] ok 45 - Structure sizes for GSignalQuery match
  [GLib] ok 46 - Structure sizes for GSourceCallbackFuncs match
  [GLib] ok 47 - Structure sizes for GSourceFuncs match
  [GLib] ok 48 - Structure sizes for GString match
  [GLib] ok 49 - Structure sizes for GTestConfig match
  [GLib] ok 50 - Structure sizes for GTestLogBuffer match
  [GLib] ok 51 - Structure sizes for GTestLogMsg match
  [GLib] ok 52 - Structure sizes for GTimeVal match
  [GLib] ok 53 - Structure sizes for GTypeFundamentalInfo match
  [GLib] ok 54 - Structure sizes for GTypeInfo match
  [GLib] ok 55 - Structure sizes for GTypeInterface match
  [GLib] ok 56 - Structure sizes for GTypeQuery match
  [GLib] ok 57 - Structure sizes for GTypeValueTable match
  [GLib] ok 58 - Structure sizes for GUriParamsIter match
  [GLib] ok 59 - Structure sizes for GValue match
  [GLib] ok 60 - Structure sizes for GValueArray match
  [GLib] ok 61 - Structure sizes for GVariant match
  [GLib] ok 62 - Structure sizes for GVariantIter match
  [GLib] ok 63 - Structure 'GVariantSerialized' is not to be tested (internal struct)
  [GLib] ok 64 - Structure 'GVariantTree' is not to be tested (internal struct)
  [GLib] ok 65 - Structure sizes for GVariantTypeInfo match
  [GLib] ok 66 - Structure sizes for GWeakRef match
  [GLib] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/00b-class-struct-sizes.t
  [GLib] Potential difficulties:
  [GLib]     Declaring class 'GLib::Class::Object' inside an enclosing package of
  [GLib]     the same name silently replaces the package in the outer stash. This is
  [GLib]     legacy behavior specific to Raku 6.d and earlier; in Raku 6.e the same
  [GLib]     pattern installs the class as a nested package instead. Rewrite as 'unit
  [GLib]     class GLib::Class::Object;' in its own file (or otherwise avoid the
  [GLib]     package+same-named-class collision) to work the same way on either
  [GLib]     revision.
  [GLib]     at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Class/Object.pm6 (GLib::Class::Object):103
  [GLib]     ------> class <HERE>GLib::Class::Object is export {
  [GLib] 1..1
  [GLib] ok 1 - Structure sizes for GObjectClass match
  [GLib] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/01-modules.t
  [GLib] 1..174
  [GLib] ok 1 - GLib
  [GLib] ok 2 - GLib::Array
  [GLib] ok 3 - GLib::AsyncQueue
  [GLib] ok 4 - GLib::Base64
  [GLib] ok 5 - GLib::BookmarkFile
  [GLib] ok 6 - GLib::ByteArray
  [GLib] ok 7 - GLib::Bytes
  [GLib] ok 8 - GLib::Checksum
  [GLib] ok 9 - GLib::Class::Object
  [GLib] ok 10 - GLib::Class::Structs
  [GLib] ok 11 - GLib::Class::TypeModule
  [GLib] ok 12 - GLib::Compat::Definitions
  [GLib] ok 13 - GLib::Cond
  [GLib] ok 14 - GLib::Convert
  [GLib] ok 15 - GLib::Dataset
  [GLib] ok 16 - GLib::Date
  [GLib] ok 17 - GLib::DateTime
  [GLib] ok 18 - GLib::Env
  [GLib] ok 19 - GLib::Error
  [GLib] ok 20 - GLib::FileUtils
  [GLib] ok 21 - GLib::GList
  [GLib] ok 22 - GLib::GSList
  [GLib] ok 23 - GLib::HMAC
  [GLib] ok 24 - GLib::HashTable
  [GLib] ok 25 - GLib::Hostname
  [GLib] ok 26 - GLib::IOChannel
  [GLib] ok 27 - GLib::KeyFile
  [GLib] ok 28 - GLib::Log
  [GLib] ok 29 - GLib::MainContext
  [GLib] ok 30 - GLib::MainLoop
  [GLib] ok 31 - GLib::MappedFile
  [GLib] ok 32 - GLib::Markup
  [GLib] ok 33 - GLib::MatchInfo
  [GLib] ok 34 - GLib::Memory
  [GLib] ok 35 - GLib::Module
  [GLib] ok 36 - GLib::Mutex
  [GLib] ok 37 - GLib::Node
  [GLib] ok 38 - GLib::Object::Binding
  [GLib] ok 39 - GLib::Object::Closure
  [GLib] ok 40 - GLib::Object::IsType
  [GLib] ok 41 - GLib::Object::ParamSpec
  [GLib] ok 42 - GLib::Object::Raw::Binding
  [GLib] ok 43 - GLib::Object::Raw::Closure
  [GLib] ok 44 - GLib::Object::Raw::ParamSpec
  [GLib] ok 45 - GLib::Object::Raw::TypeModule
  [GLib] ok 46 - GLib::Object::Raw::Types
  [GLib] ok 47 - GLib::Object::Supplyish
  [GLib] ok 48 - GLib::Object::Type
  [GLib] ok 49 - GLib::Object::TypeModule
  [GLib] ok 50 - GLib::Object::Types
  [GLib] ok 51 - GLib::Pattern
  [GLib] ok 52 - GLib::PtrArray
  [GLib] ok 53 - GLib::Quark
  [GLib] ok 54 - GLib::Queue
  [GLib] ok 55 - GLib::Rand
  [GLib] ok 56 - GLib::Raw::Array
  [GLib] ok 57 - GLib::Raw::Arrays
  [GLib] ok 58 - GLib::Raw::AsyncQueue
  [GLib] ok 59 - GLib::Raw::Base64
  [GLib] ok 60 - GLib::Raw::BookmarkFile
  [GLib] ok 61 - GLib::Raw::Bytes
  [GLib] ok 62 - GLib::Raw::Checksum
  [GLib] ok 63 - GLib::Raw::Convert
  [GLib] ok 64 - GLib::Raw::Dataset
  [GLib] ok 65 - GLib::Raw::Date
  [GLib] ok 66 - GLib::Raw::DateTime
  [GLib] ok 67 - GLib::Raw::Debug
  [GLib] ok 68 - GLib::Raw::Definitions
  [GLib] ok 69 - GLib::Raw::Distro
  [GLib] ok 70 - GLib::Raw::Enum
  [GLib] ok 71 - GLib::Raw::Enums
  [GLib] ok 72 - GLib::Raw::Env
  [GLib] ok 73 - GLib::Raw::Error
  [GLib] ok 74 - GLib::Raw::Exceptions
  [GLib] ok 75 - GLib::Raw::Exports
  [GLib] ok 76 - GLib::Raw::ExtendedTypes
  [GLib] ok 77 - GLib::Raw::FileUtils
  [GLib] ok 78 - GLib::Raw::GList
  [GLib] ok 79 - GLib::Raw::GSList
  [GLib] ok 80 - GLib::Raw::GenericList
  [GLib] ok 81 - GLib::Raw::HMAC
  [GLib] ok 82 - GLib::Raw::HashTable
  [GLib] ok 83 - GLib::Raw::Hostname
  [GLib] ok 84 - GLib::Raw::IOChannel
  [GLib] ok 85 - GLib::Raw::KeyFile
  [GLib] ok 86 - GLib::Raw::Log
  [GLib] ok 87 - GLib::Raw::Macros
  [GLib] ok 88 - GLib::Raw::Main
  [GLib] ok 89 - GLib::Raw::MappedFile
  [GLib] ok 90 - GLib::Raw::Markup
  [GLib] ok 91 - GLib::Raw::Memory
  [GLib] ok 92 - GLib::Raw::Module
  [GLib] ok 93 - GLib::Raw::Node
  [GLib] ok 94 - GLib::Raw::Object
  [GLib] ok 95 - GLib::Raw::Pattern
  [GLib] ok 96 - GLib::Raw::Pointers
  [GLib] ok 97 - GLib::Raw::Quark
  [GLib] ok 98 - GLib::Raw::Quarks
  [GLib] ok 99 - GLib::Raw::Queue
  [GLib] ok 100 - GLib::Raw::Rand
  [GLib] ok 101 - GLib::Raw::Regex
  [GLib] ok 102 - GLib::Raw::ReturnedValue
  [GLib] ok 103 - GLib::Raw::Scanner
  [GLib] ok 104 - GLib::Raw::Sequence
  [GLib] ok 105 - GLib::Raw::Signal
  [GLib] ok 106 - GLib::Raw::Slice
  [GLib] ok 107 - GLib::Raw::Spawn
  [GLib] ok 108 - GLib::Raw::String
  [GLib] ok 109 - GLib::Raw::String::Chunk
  [GLib] ok 110 - GLib::Raw::Struct_Subs
  [GLib] ok 111 - GLib::Raw::Structs
  [GLib] ok 112 - GLib::Raw::Subs
  [GLib] ok 113 - GLib::Raw::Test
  [GLib] ok 114 - GLib::Raw::Thread
  [GLib] ok 115 - GLib::Raw::ThreadPool
  [GLib] ok 116 - GLib::Raw::TimeZone
  [GLib] ok 117 - GLib::Raw::Timer
  [GLib] ok 118 - GLib::Raw::Traits
  [GLib] ok 119 - GLib::Raw::Traps
  [GLib] ok 120 - GLib::Raw::Tree
  [GLib] ok 121 - GLib::Raw::Type
  [GLib] ok 122 - GLib::Raw::TypePlugin
  [GLib] ok 123 - GLib::Raw::Types
  [GLib] ok 124 - GLib::Raw::Unicode
  [GLib] ok 125 - GLib::Raw::Uri
  [GLib] ok 126 - GLib::Raw::Utils
  [GLib] ok 127 - GLib::Raw::Value
  [GLib] ok 128 - GLib::Raw::Variant
  [GLib] ok 129 - GLib::Raw::VariantType
  [GLib] ok 130 - GLib::Raw::VariantTypes
  [GLib] ok 131 - GLib::Regex
  [GLib] ok 132 - GLib::Roles::Bindable
  [GLib] ok 133 - GLib::Roles::HashObject
  [GLib] ok 134 - GLib::Roles::Implementor
  [GLib] ok 135 - GLib::Roles::ListData
  [GLib] ok 136 - GLib::Roles::NewGObject
  [GLib] ok 137 - GLib::Roles::Object
  [GLib] ok 138 - GLib::Roles::PointerBasedList
  [GLib] ok 139 - GLib::Roles::Pointers
  [GLib] ok 140 - GLib::Roles::Properties
  [GLib] ok 141 - GLib::Roles::Protection
  [GLib] ok 142 - GLib::Roles::References
  [GLib] ok 143 - GLib::Roles::Signals::Generic
  [GLib] ok 144 - GLib::Roles::StaticClass
  [GLib] ok 145 - GLib::Roles::TreeData
  [GLib] ok 146 - GLib::Roles::TypeInstance
  [GLib] ok 147 - GLib::Roles::TypePlugin
  [GLib] ok 148 - GLib::Roles::TypedArray
  [GLib] ok 149 - GLib::Roles::TypedBuffer
  [GLib] ok 150 - GLib::Roles::TypedQueue
  [GLib] ok 151 - GLib::Roles::Value
  [GLib] ok 152 - GLib::Scanner
  [GLib] ok 153 - GLib::Sequence
  [GLib] ok 154 - GLib::Signal
  [GLib] ok 155 - GLib::Slice
  [GLib] ok 156 - GLib::Source
  [GLib] ok 157 - GLib::Spawn
  [GLib] ok 158 - GLib::String
  [GLib] ok 159 - GLib::String::Chunk
  [GLib] ok 160 - GLib::Test
  [GLib] ok 161 - GLib::ThreadPool
  [GLib] ok 162 - GLib::TimeZone
  [GLib] ok 163 - GLib::Timeout
  [GLib] ok 164 - GLib::Timer
  [GLib] ok 165 - GLib::Tree
  [GLib] ok 166 - GLib::UUID
  [GLib] ok 167 - GLib::Unicode
  [GLib] ok 168 - GLib::Uri
  [GLib] ok 169 - GLib::Utils
  [GLib] ok 170 - GLib::Value
  [GLib] ok 171 - GLib::Variant
  [GLib] ok 172 - GLib::VariantDict
  [GLib] ok 173 - GLib::VariantIter
  [GLib] ok 174 - GLib::VariantType
  ===> Testing [OK] for GLib:ver<0.0.11>:auth<cpan:CBWOOD>
  ===> Installing: GLib:ver<0.0.11>:auth<cpan:CBWOOD>
  ===> Install [OK] for GLib:ver<0.0.11>:auth<cpan:CBWOOD>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 46.475s
               CPU time consumed: 1min 6.199s
                     Memory peak: 3.5G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p645322-i641901.service; invocation ID: 0bea317312a641fe81bc993f61a05b11
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: GLib
  ===> Found: GLib:ver<0.0.11>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [GLib] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789651001.645323.5766.278481167446/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/GLib/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: GLib:ver<0.0.11>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789651001.645323.5766.278481167446/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [GLib] Command: tar -t -f ./GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [GLib] Command: tar -xvf ./GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz -C ../GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Extraction [OK]: GLib to /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Testing: GLib:ver<0.0.11>:auth<cpan:CBWOOD>
  [GLib] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/00-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs)
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions)
  [GLib] Can only use : as invocant marker in a signature after the first parameter
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions):133
  [GLib] ------>   method new (<HERE> :
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs):10
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00-struct-sizes.t:7
  [GLib] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/00b-class-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00b-class-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs)
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions)
  [GLib] Can only use : as invocant marker in a signature after the first parameter
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions):133
  [GLib] ------>   method new (<HERE> :
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs):10
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00b-class-struct-sizes.t:7
  [GLib] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/01-modules.t
  [GLib] 1..174
  [GLib] ok 1 - GLib
  [GLib] ok 2 - GLib::Array
  [GLib] ok 3 - GLib::AsyncQueue
  [GLib] ok 4 - GLib::Base64
  [GLib] ok 5 - GLib::BookmarkFile
  [GLib] ok 6 - GLib::ByteArray
  [GLib] ok 7 - GLib::Bytes
  [GLib] ok 8 - GLib::Checksum
  [GLib] ok 9 - GLib::Class::Object
  [GLib] ok 10 - GLib::Class::Structs
  [GLib] ok 11 - GLib::Class::TypeModule
  [GLib] ok 12 - GLib::Compat::Definitions
  [GLib] ok 13 - GLib::Cond
  [GLib] ok 14 - GLib::Convert
  [GLib] ok 15 - GLib::Dataset
  [GLib] ok 16 - GLib::Date
  [GLib] ok 17 - GLib::DateTime
  [GLib] ok 18 - GLib::Env
  [GLib] ok 19 - GLib::Error
  [GLib] ok 20 - GLib::FileUtils
  [GLib] ok 21 - GLib::GList
  [GLib] ok 22 - GLib::GSList
  [GLib] ok 23 - GLib::HMAC
  [GLib] ok 24 - GLib::HashTable
  [GLib] ok 25 - GLib::Hostname
  [GLib] ok 26 - GLib::IOChannel
  [GLib] ok 27 - GLib::KeyFile
  [GLib] ok 28 - GLib::Log
  [GLib] ok 29 - GLib::MainContext
  [GLib] ok 30 - GLib::MainLoop
  [GLib] ok 31 - GLib::MappedFile
  [GLib] ok 32 - GLib::Markup
  [GLib] ok 33 - GLib::MatchInfo
  [GLib] ok 34 - GLib::Memory
  [GLib] ok 35 - GLib::Module
  [GLib] ok 36 - GLib::Mutex
  [GLib] ok 37 - GLib::Node
  [GLib] ok 38 - GLib::Object::Binding
  [GLib] ok 39 - GLib::Object::Closure
  [GLib] ok 40 - GLib::Object::IsType
  [GLib] ok 41 - GLib::Object::ParamSpec
  [GLib] ok 42 - GLib::Object::Raw::Binding
  [GLib] ok 43 - GLib::Object::Raw::Closure
  [GLib] ok 44 - GLib::Object::Raw::ParamSpec
  [GLib] ok 45 - GLib::Object::Raw::TypeModule
  [GLib] ok 46 - GLib::Object::Raw::Types
  [GLib] ok 47 - GLib::Object::Supplyish
  [GLib] ok 48 - GLib::Object::Type
  [GLib] ok 49 - GLib::Object::TypeModule
  [GLib] ok 50 - GLib::Object::Types
  [GLib] ok 51 - GLib::Pattern
  [GLib] ok 52 - GLib::PtrArray
  [GLib] ok 53 - GLib::Quark
  [GLib] ok 54 - GLib::Queue
  [GLib] ok 55 - GLib::Rand
  [GLib] ok 56 - GLib::Raw::Array
  [GLib] ok 57 - GLib::Raw::Arrays
  [GLib] ok 58 - GLib::Raw::AsyncQueue
  [GLib] ok 59 - GLib::Raw::Base64
  [GLib] ok 60 - GLib::Raw::BookmarkFile
  [GLib] ok 61 - GLib::Raw::Bytes
  [GLib] ok 62 - GLib::Raw::Checksum
  [GLib] ok 63 - GLib::Raw::Convert
  [GLib] ok 64 - GLib::Raw::Dataset
  [GLib] ok 65 - GLib::Raw::Date
  [GLib] ok 66 - GLib::Raw::DateTime
  [GLib] ok 67 - GLib::Raw::Debug
  [GLib] ok 68 - GLib::Raw::Definitions
  [GLib] ok 69 - GLib::Raw::Distro
  [GLib] ok 70 - GLib::Raw::Enum
  [GLib] ok 71 - GLib::Raw::Enums
  [GLib] ok 72 - GLib::Raw::Env
  [GLib] ok 73 - GLib::Raw::Error
  [GLib] ok 74 - GLib::Raw::Exceptions
  [GLib] ok 75 - GLib::Raw::Exports
  [GLib] ok 76 - GLib::Raw::ExtendedTypes
  [GLib] ok 77 - GLib::Raw::FileUtils
  [GLib] ok 78 - GLib::Raw::GList
  [GLib] ok 79 - GLib::Raw::GSList
  [GLib] ok 80 - GLib::Raw::GenericList
  [GLib] ok 81 - GLib::Raw::HMAC
  [GLib] ok 82 - GLib::Raw::HashTable
  [GLib] ok 83 - GLib::Raw::Hostname
  [GLib] ok 84 - GLib::Raw::IOChannel
  [GLib] ok 85 - GLib::Raw::KeyFile
  [GLib] ok 86 - GLib::Raw::Log
  [GLib] ok 87 - GLib::Raw::Macros
  [GLib] ok 88 - GLib::Raw::Main
  [GLib] ok 89 - GLib::Raw::MappedFile
  [GLib] ok 90 - GLib::Raw::Markup
  [GLib] ok 91 - GLib::Raw::Memory
  [GLib] ok 92 - GLib::Raw::Module
  [GLib] ok 93 - GLib::Raw::Node
  [GLib] ok 94 - GLib::Raw::Object
  [GLib] ok 95 - GLib::Raw::Pattern
  [GLib] ok 96 - GLib::Raw::Pointers
  [GLib] ok 97 - GLib::Raw::Quark
  [GLib] ok 98 - GLib::Raw::Quarks
  [GLib] ok 99 - GLib::Raw::Queue
  [GLib] ok 100 - GLib::Raw::Rand
  [GLib] ok 101 - GLib::Raw::Regex
  [GLib] ok 102 - GLib::Raw::ReturnedValue
  [GLib] ok 103 - GLib::Raw::Scanner
  [GLib] ok 104 - GLib::Raw::Sequence
  [GLib] ok 105 - GLib::Raw::Signal
  [GLib] ok 106 - GLib::Raw::Slice
  [GLib] ok 107 - GLib::Raw::Spawn
  [GLib] ok 108 - GLib::Raw::String
  [GLib] ok 109 - GLib::Raw::String::Chunk
  [GLib] ok 110 - GLib::Raw::Struct_Subs
  [GLib] ok 111 - GLib::Raw::Structs
  [GLib] ok 112 - GLib::Raw::Subs
  [GLib] ok 113 - GLib::Raw::Test
  [GLib] ok 114 - GLib::Raw::Thread
  [GLib] ok 115 - GLib::Raw::ThreadPool
  [GLib] ok 116 - GLib::Raw::TimeZone
  [GLib] ok 117 - GLib::Raw::Timer
  [GLib] ok 118 - GLib::Raw::Traits
  [GLib] ok 119 - GLib::Raw::Traps
  [GLib] ok 120 - GLib::Raw::Tree
  [GLib] ok 121 - GLib::Raw::Type
  [GLib] ok 122 - GLib::Raw::TypePlugin
  [GLib] ok 123 - GLib::Raw::Types
  [GLib] ok 124 - GLib::Raw::Unicode
  [GLib] ok 125 - GLib::Raw::Uri
  [GLib] ok 126 - GLib::Raw::Utils
  [GLib] ok 127 - GLib::Raw::Value
  [GLib] ok 128 - GLib::Raw::Variant
  [GLib] ok 129 - GLib::Raw::VariantType
  [GLib] ok 130 - GLib::Raw::VariantTypes
  [GLib] ok 131 - GLib::Regex
  [GLib] ok 132 - GLib::Roles::Bindable
  [GLib] ok 133 - GLib::Roles::HashObject
  [GLib] ok 134 - GLib::Roles::Implementor
  [GLib] ok 135 - GLib::Roles::ListData
  [GLib] ok 136 - GLib::Roles::NewGObject
  [GLib] ok 137 - GLib::Roles::Object
  [GLib] ok 138 - GLib::Roles::PointerBasedList
  [GLib] ok 139 - GLib::Roles::Pointers
  [GLib] ok 140 - GLib::Roles::Properties
  [GLib] ok 141 - GLib::Roles::Protection
  [GLib] ok 142 - GLib::Roles::References
  [GLib] ok 143 - GLib::Roles::Signals::Generic
  [GLib] ok 144 - GLib::Roles::StaticClass
  [GLib] ok 145 - GLib::Roles::TreeData
  [GLib] ok 146 - GLib::Roles::TypeInstance
  [GLib] ok 147 - GLib::Roles::TypePlugin
  [GLib] ok 148 - GLib::Roles::TypedArray
  [GLib] ok 149 - GLib::Roles::TypedBuffer
  [GLib] ok 150 - GLib::Roles::TypedQueue
  [GLib] ok 151 - GLib::Roles::Value
  [GLib] ok 152 - GLib::Scanner
  [GLib] ok 153 - GLib::Sequence
  [GLib] ok 154 - GLib::Signal
  [GLib] ok 155 - GLib::Slice
  [GLib] ok 156 - GLib::Source
  [GLib] ok 157 - GLib::Spawn
  [GLib] ok 158 - GLib::String
  [GLib] ok 159 - GLib::String::Chunk
  [GLib] ok 160 - GLib::Test
  [GLib] ok 161 - GLib::ThreadPool
  [GLib] ok 162 - GLib::TimeZone
  [GLib] ok 163 - GLib::Timeout
  [GLib] ok 164 - GLib::Timer
  [GLib] ok 165 - GLib::Tree
  [GLib] ok 166 - GLib::UUID
  [GLib] ok 167 - GLib::Unicode
  [GLib] ok 168 - GLib::Uri
  [GLib] ok 169 - GLib::Utils
  [GLib] ok 170 - GLib::Value
  [GLib] ok 171 - GLib::Variant
  [GLib] ok 172 - GLib::VariantDict
  [GLib] ok 173 - GLib::VariantIter
  [GLib] ok 174 - GLib::VariantType
  ===> Testing [FAIL]: GLib:ver<0.0.11>:auth<cpan:CBWOOD>
  [GLib] Failed to get passing tests, but continuing with --force-test
  ===> Installing: GLib:ver<0.0.11>:auth<cpan:CBWOOD>
  ===> Install [OK] for GLib:ver<0.0.11>:auth<cpan:CBWOOD>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 13.850s
               CPU time consumed: 16.941s
                     Memory peak: 2.3G (swap: 0B)

  ```
  </details>
* [ ] [JSON::GLib::Node](https://raku.land/cpan:CBWOOD/JSON::GLib::Node) – Fail, Bisected: [6357ccf](https://github.com/rakudo/rakudo/commit/6357ccf97f2c4b1dd1067bf4f50b6cdcfdb78373)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p650395-i617799.service; invocation ID: 74ac1a4c3ff548c2920a3e84132da66a
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: JSON::GLib::Node
  ===> Found: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [JSON::GLib::Node] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789651413.650396.1544.3958657868018/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/J/JSON%3A%3AGLib%3A%3ANode/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789651413.650396.1544.3958657868018/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [JSON::GLib::Node] Command: tar -t -f ./JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [JSON::GLib::Node] Command: tar -xvf ./JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz -C ../JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Extraction [OK]: JSON::GLib::Node to /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Testing: JSON::GLib::Node:ver<0.0.1>
  [JSON::GLib::Node] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/JSON-GLib-Node-0.0.1 t/01-basic.t
  [JSON::GLib::Node] Potential difficulties:
  [JSON::GLib::Node]     Declaring class 'GLib::Class::Object' inside an enclosing package of
  [JSON::GLib::Node]     the same name silently replaces the package in the outer stash. This is
  [JSON::GLib::Node]     legacy behavior specific to Raku 6.d and earlier; in Raku 6.e the same
  [JSON::GLib::Node]     pattern installs the class as a nested package instead. Rewrite as 'unit
  [JSON::GLib::Node]     class GLib::Class::Object;' in its own file (or otherwise avoid the
  [JSON::GLib::Node]     package+same-named-class collision) to work the same way on either
  [JSON::GLib::Node]     revision.
  [JSON::GLib::Node]     at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/6CA058F1742AC15AF9A8D119F6535617F1C5EFF5 (GLib::Class::Object):103
  [JSON::GLib::Node]     ------> class <HERE>GLib::Class::Object is export {
  [JSON::GLib::Node] 1..9
  [JSON::GLib::Node] ok 1 - JSON::GLib::Array loads properly
  [JSON::GLib::Node] ok 2 - JSON::GLib::Builder loads properly
  [JSON::GLib::Node] ok 3 - JSON::GLib::Generator loads properly
  [JSON::GLib::Node] ok 4 - JSON::GLib::Node loads properly
  [JSON::GLib::Node] ok 5 - JSON::GLib::Object loads properly
  [JSON::GLib::Node] ok 6 - JSON::GLib::Parser loads properly
  [JSON::GLib::Node] ok 7 - JSON::GLib::Path loads properly
  [JSON::GLib::Node] ok 8 - JSON::GLib::Reader loads properly
  [JSON::GLib::Node] ok 9 - JSON::GLib::Variant loads properly
  ===> Testing [OK] for JSON::GLib::Node:ver<0.0.1>
  ===> Installing: JSON::GLib::Node:ver<0.0.1>
  ===> Install [OK] for JSON::GLib::Node:ver<0.0.1>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 58.450s
               CPU time consumed: 1min 22.989s
                     Memory peak: 3.1G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p650242-i712747.service; invocation ID: e2be7bdb8aa64d059a47fe271f3e250d
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: JSON::GLib::Node
  ===> Found: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [JSON::GLib::Node] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789651393.650243.756.0471866601548/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/J/JSON%3A%3AGLib%3A%3ANode/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789651393.650243.756.0471866601548/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [JSON::GLib::Node] Command: tar -t -f ./JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [JSON::GLib::Node] Command: tar -xvf ./JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz -C ../JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Extraction [OK]: JSON::GLib::Node to /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Testing: JSON::GLib::Node:ver<0.0.1>
  [JSON::GLib::Node] Command: /tmp/whateverable/rakudo-moar/b83057b10c4d37a91a087ab2c87b5cfba8e2c4b8/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/JSON-GLib-Node-0.0.1 t/01-basic.t
  [JSON::GLib::Node] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/JSON-GLib-Node-0.0.1/t/01-basic.t
  [JSON::GLib::Node] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/JSON-GLib-Node-0.0.1/lib/JSON/GLib/Array.pm6 (JSON::GLib::Array)
  [JSON::GLib::Node] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/0C336C09131938C526DC4C924AD2A0CDE35A600C (GLib::GList)
  [JSON::GLib::Node] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/1EA21A570A7AEB653962EFCBE486E61D713CC8D2 (GLib::Raw::Types)
  [JSON::GLib::Node] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions)
  [JSON::GLib::Node] Can only use : as invocant marker in a signature after the first parameter
  [JSON::GLib::Node] at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions):133
  [JSON::GLib::Node] ------>   method new (<HERE> :
  [JSON::GLib::Node] at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/1EA21A570A7AEB653962EFCBE486E61D713CC8D2 (GLib::Raw::Types):10
  [JSON::GLib::Node] at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/0C336C09131938C526DC4C924AD2A0CDE35A600C (GLib::GList):6
  [JSON::GLib::Node] at /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/JSON-GLib-Node-0.0.1/lib/JSON/GLib/Array.pm6 (JSON::GLib::Array):7
  [JSON::GLib::Node] at /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/JSON-GLib-Node-0.0.1/t/01-basic.t:7
  ===> Testing [FAIL]: JSON::GLib::Node:ver<0.0.1>
  [JSON::GLib::Node] Failed to get passing tests, but continuing with --force-test
  ===> Installing: JSON::GLib::Node:ver<0.0.1>
  ===> Install [OK] for JSON::GLib::Node:ver<0.0.1>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 9.732s
               CPU time consumed: 11.775s
                     Memory peak: 2.6G (swap: 0B)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| Fail                      |     3 | [GLib](https://raku.land/cpan:CBWOOD/GLib) [JSON::GLib::Node](https://raku.land/cpan:CBWOOD/JSON::GLib::Node) [Polyglot::Regexen](https://raku.land/zef:guifa/Polyglot::Regexen) |
| AlwaysFail                |     6 | [DOM::Tiny](https://raku.land/cpan:HANENKAMP/DOM::Tiny) [Data::Dump::Tree](https://raku.land/zef:raku-community-modules/Data::Dump::Tree) [JSON::Class](https://raku.land/zef:jonathanstowe/JSON::Class) [License::SPDX](https://raku.land/zef:jonathanstowe/License::SPDX) [META6](https://raku.land/zef:jonathanstowe/META6) [Test::META](https://raku.land/zef:jonathanstowe/Test::META) |
| OK                        |    44 | ⋯                         |



This run started on 2026-09-17T13:30:37Z and finished in 18 minutes.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
