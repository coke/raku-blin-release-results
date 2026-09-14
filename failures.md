[Blin](https://github.com/Raku/Blin) results between 2026.08 ([24e6e53](https://github.com/rakudo/rakudo/commit/24e6e5312f2868680413b0597aef8772f6b5bcea)) and b88ac8f ([b88ac8f](https://github.com/rakudo/rakudo/commit/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a)):

* [ ] [Text::Fortune](https://raku.land/github:zengargoyle/Text::Fortune) – Fail, Bisected: [a22cab8](https://github.com/rakudo/rakudo/commit/a22cab8f9df9b8ad14bd5674cd089c34d62f8a12)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p81997-i8400123.service; invocation ID: 3544efbfe5af438fb6dfbb02998bcce9
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Text::Fortune
  ===> Found: Text::Fortune:ver<0.03>:auth<github:zengargoyle> [via Zef::Repository::Ecosystems<rea>]
  [Text::Fortune] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789391878.81998.6473.258273049376/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/T/Text%3A%3AFortune/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz
  ===> Fetching [OK]: Text::Fortune:ver<0.03>:auth<github:zengargoyle> to /home/coke/sandbox/blin/data/zef-data/tmp/1789391878.81998.6473.258273049376/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz
  [Text::Fortune] Command: tar -t -f ./Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz
  [Text::Fortune] Command: tar -xvf ./Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz -C ../Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz
  ===> Extraction [OK]: Text::Fortune to /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz
  ===> Testing: Text::Fortune:ver<0.03>:auth<github:zengargoyle>
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/01_empty.t
  [Text::Fortune] Buf[uint8]:0x<00 00 00 02 00 00 00 00 00 00 00 00 FF FF FF FF 00 00 00 00 25 00 00 00 00 00 00 00>
  [Text::Fortune] ok 1 - is version: 2
  [Text::Fortune] ok 2 - matches empty.dat
  [Text::Fortune] ok 3 - flags might work
  [Text::Fortune] ok 4 - can set delimiter
  [Text::Fortune] ok 5 - is rotated
  [Text::Fortune] 1..5
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/02_simple.t
  [Text::Fortune] # Subtest: did we throws-like Text::Fortune::X::Index::NotFound?
  [Text::Fortune]     1..3
  [Text::Fortune]     ok 1 - code dies
  [Text::Fortune]     ok 2 - right exception type (Text::Fortune::X::Index::NotFound)
  [Text::Fortune]     ok 3 - .message matches rx:s/not found/
  [Text::Fortune] ok 1 - did we throws-like Text::Fortune::X::Index::NotFound?
  [Text::Fortune] ok 2 - is version: 2
  [Text::Fortune] ok 3 - has count: 0
  [Text::Fortune] ok 4 - has longest: 0
  [Text::Fortune] ok 5 - has shortest: -1
  [Text::Fortune] ok 6 - has flags: 0
  [Text::Fortune] ok 7 - has rotated: False
  [Text::Fortune] ok 8 - has delimiter: %
  [Text::Fortune] ok 9 - only offset is: 0
  [Text::Fortune] ok 10 - serializes correctly
  [Text::Fortune] 1..10
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/03_dodat.t
  [Text::Fortune] ok 1 - first offset correct
  [Text::Fortune] ok 2 - last offset correct
  [Text::Fortune] ok 3 - final offset correct
  [Text::Fortune] ok 4 - first length correct
  [Text::Fortune] ok 5 - last length correct
  [Text::Fortune] # Subtest: did we throws-like Text::Fortune::X::Index::OutOfBounds?
  [Text::Fortune]     1..2
  [Text::Fortune]     ok 1 - code dies
  [Text::Fortune]     ok 2 - right exception type (Text::Fortune::X::Index::OutOfBounds)
  [Text::Fortune] ok 6 - did we throws-like Text::Fortune::X::Index::OutOfBounds?
  [Text::Fortune] ok 7 - serializes correctly
  [Text::Fortune] 1..7
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/04_nodat.t
  [Text::Fortune] ok 1 - first offset correct
  [Text::Fortune] ok 2 - last offset correct
  [Text::Fortune] ok 3 - final offset correct
  [Text::Fortune] ok 4 - first length correct
  [Text::Fortune] ok 5 - last length correct
  [Text::Fortune] # Subtest: did we throws-like Text::Fortune::X::Index::OutOfBounds?
  [Text::Fortune]     1..2
  [Text::Fortune]     ok 1 - code dies
  [Text::Fortune]     ok 2 - right exception type (Text::Fortune::X::Index::OutOfBounds)
  [Text::Fortune] ok 6 - did we throws-like Text::Fortune::X::Index::OutOfBounds?
  [Text::Fortune] ok 7 - serializes correctly
  [Text::Fortune] ok 8 - first/last/final offset correct
  [Text::Fortune] # Subtest: did we throws-like Text::Fortune::X::Index::OutOfBounds?
  [Text::Fortune]     1..2
  [Text::Fortune]     ok 1 - code dies
  [Text::Fortune]     ok 2 - right exception type (Text::Fortune::X::Index::OutOfBounds)
  [Text::Fortune] ok 9 - did we throws-like Text::Fortune::X::Index::OutOfBounds?
  [Text::Fortune] ok 10 - serializes correctly
  [Text::Fortune] 1..10
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/05_broken.t
  [Text::Fortune] ok 1 - bogus
  [Text::Fortune] Buf[uint8]:0x<00 00 00 02 00 00 00 03 00 00 00 06 00 00 00 02 00 00 00 00 25 00 00 00 00 00 00 00 00 00 00 04 00 00 00 09 00 00 00 11>
  [Text::Fortune] Buf:0x<00 00 00 02 00 00 00 03 00 00 00 06 00 00 00 02 00 00 00 00 25 00 00 00 00 00 00 00 00 00 00 04 00 00 00 09 00 00 00 11>
  [Text::Fortune] Buf[uint8]:0x<00 00 00 02 00 00 00 00 00 00 00 00 FF FF FF FF 00 00 00 00 25 00 00 00 00 00 00 00>
  [Text::Fortune] Buf:0x<00 00 00 02 00 00 00 00 00 00 00 00 FF FF FF FF 00 00 00 00 25 00 00 00 00 00 00 00>
  [Text::Fortune] 1..1
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/10_basic.t
  [Text::Fortune] ok 1 - got out count
  [Text::Fortune] ok 2 - not rotated
  [Text::Fortune] ok 3 - got first fortune
  [Text::Fortune] ok 4 - got last fortune
  [Text::Fortune] ok 5 - got first fortune
  [Text::Fortune] ok 6 - got last fortune
  [Text::Fortune] ok 7 - got out count
  [Text::Fortune] ok 8 - got first fortune
  [Text::Fortune] ok 9 - got last fortune
  [Text::Fortune] ok 10 - got first fortune
  [Text::Fortune] ok 11 - got last fortune
  [Text::Fortune] ok 12 - forced rotation
  [Text::Fortune] ok 13 - got first fortune
  [Text::Fortune] ok 14 - got last fortune
  [Text::Fortune] 1..14
  ===> Testing [OK] for Text::Fortune:ver<0.03>:auth<github:zengargoyle>
  ===> Installing: Text::Fortune:ver<0.03>:auth<github:zengargoyle>
  ===> Install [OK] for Text::Fortune:ver<0.03>:auth<github:zengargoyle>

  2 bin/ scripts [strfile.pl fortune.pl] installed to:
  /tmp/b2NPQKl0Pi/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 36.807s
               CPU time consumed: 51.416s
                     Memory peak: 1.3G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p80692-i8516126.service; invocation ID: d194dcf031e24fc7afbad8530ebce8f3
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Text::Fortune
  ===> Found: Text::Fortune:ver<0.03>:auth<github:zengargoyle> [via Zef::Repository::Ecosystems<rea>]
  [Text::Fortune] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789391841.80694.3226.516218182853/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/T/Text%3A%3AFortune/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz
  ===> Fetching [OK]: Text::Fortune:ver<0.03>:auth<github:zengargoyle> to /home/coke/sandbox/blin/data/zef-data/tmp/1789391841.80694.3226.516218182853/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz
  [Text::Fortune] Command: tar -t -f ./Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz
  [Text::Fortune] Command: tar -xvf ./Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz -C ../Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz
  ===> Extraction [OK]: Text::Fortune to /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz
  ===> Testing: Text::Fortune:ver<0.03>:auth<github:zengargoyle>
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/01_empty.t
  [Text::Fortune] Type check failed in assignment; expected IO but got Str ("t/test_data")
  [Text::Fortune]   in block <unit> at t/01_empty.t line 5
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/02_simple.t
  [Text::Fortune] Type check failed in assignment; expected IO but got Str ("t/test_data")
  [Text::Fortune]   in block <unit> at t/02_simple.t line 5
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/03_dodat.t
  [Text::Fortune] Type check failed in assignment; expected IO but got Str ("t/test_data")
  [Text::Fortune]   in block <unit> at t/03_dodat.t line 5
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/04_nodat.t
  [Text::Fortune] Type check failed in assignment; expected IO but got Str ("t/test_data")
  [Text::Fortune]   in block <unit> at t/04_nodat.t line 5
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/05_broken.t
  [Text::Fortune] ok 1 - bogus
  [Text::Fortune] Type check failed in assignment; expected IO but got Str ("t/test_data")
  [Text::Fortune]   in block <unit> at t/05_broken.t line 6
  [Text::Fortune] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AFortune%3Aver%3C0.03%3E%3Aauth%3Cgithub%3Azengargoyle%3E.tar.gz/Text-Fortune-master t/10_basic.t
  [Text::Fortune] Type check failed in assignment; expected IO but got Str ("t/test_data")
  [Text::Fortune]   in block <unit> at t/10_basic.t line 5
  ===> Testing [FAIL]: Text::Fortune:ver<0.03>:auth<github:zengargoyle>
  [Text::Fortune] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Text::Fortune:ver<0.03>:auth<github:zengargoyle>
  ===> Install [OK] for Text::Fortune:ver<0.03>:auth<github:zengargoyle>

  2 bin/ scripts [fortune.pl strfile.pl] installed to:
  /home/coke/sandbox/blin/installed/Text::Fortune_github:zengargoyle_0.03_0/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 26.670s
               CPU time consumed: 16.560s
                     Memory peak: 1.4G (swap: 0B)

  ```
  </details>
* [ ] [Polyglot::Regexen](https://raku.land/zef:guifa/Polyglot::Regexen) – Fail, Bisected: [aab0778](https://github.com/rakudo/rakudo/commit/aab0778725da5848824f07514c0ae355d972926a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p81883-i8400114.service; invocation ID: 8412565a9a3a459c8cc1400261c20dcf
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Polyglot::Regexen
  ===> Found: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> [via Zef::Repository::Ecosystems<fez>]
  [Polyglot::Regexen] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789391870.81884.6101.216346963658/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz https://360.zef.pm/P/OL/POLYGLOT_REGEXEN/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Fetching [OK]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> to /home/coke/sandbox/blin/data/zef-data/tmp/1789391870.81884.6101.216346963658/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
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
                 Service runtime: 37.158s
               CPU time consumed: 55.482s
                     Memory peak: 1.5G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p80361-i8516108.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Polyglot::Regexen
  ===> Found: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> [via Zef::Repository::Ecosystems<fez>]
  [Polyglot::Regexen] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789391828.80366.9428.121040292932/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz https://360.zef.pm/P/OL/POLYGLOT_REGEXEN/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Fetching [OK]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> to /home/coke/sandbox/blin/data/zef-data/tmp/1789391828.80366.9428.121040292932/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  [Polyglot::Regexen] Command: tar -t -f ./17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  [Polyglot::Regexen] Command: tar -xvf ./17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz -C ../17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Extraction [OK]: Polyglot::Regexen to /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Testing: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/00-sanity.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] 1..1
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/01-literals.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/02-character-classes.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/03-alternation.rakutest
  [Polyglot::Regexen] ok 1 - Simple alternation, two terms
  [Polyglot::Regexen] ok 2 - Simple alternation, three terms
  [Polyglot::Regexen] 1..2
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/04-assertions.rakutest
  [Polyglot::Regexen] ok 1 - Simple lookahead
  [Polyglot::Regexen] ok 2 - Simple negative lookahead
  [Polyglot::Regexen] ok 3 - Simple lookbehind
  [Polyglot::Regexen] ok 4 - Simple negative lookbehind
  [Polyglot::Regexen] 1..4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/05-quantifiers.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/06-captures.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/07-unicode.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/08-modifiers.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] ok 2 - 
  [Polyglot::Regexen] ok 3 - 
  [Polyglot::Regexen] ok 4 - 
  [Polyglot::Regexen] 1..4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/09-role.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/10-usage.rakutest
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
                 Service runtime: 32.515s
               CPU time consumed: 27.282s
                     Memory peak: 1.5G (swap: 0B)

  ```
  </details>
* [ ] [Color::Scheme](https://raku.land/cpan:HOLLI/Color::Scheme) – Fail, Bisected: [b88ac8f](https://github.com/rakudo/rakudo/commit/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p81227-i8396030.service; invocation ID: b914bfdd1e9b43e59aa6aa42ce18396a
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Color::Scheme
  ===> Found: Color::Scheme:ver<1.001003>:auth<cpan:HOLLI>:api<1> [via Zef::Repository::Ecosystems<rea>]
  [Color::Scheme] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789391870.81228.7100.044729081471/Color%3A%3AScheme%3Aver%3C1.001003%3E%3Aauth%3Ccpan%3AHOLLI%3E%3Aapi%3C1%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/C/Color%3A%3AScheme/Color%3A%3AScheme%3Aver%3C1.001003%3E%3Aauth%3Ccpan%3AHOLLI%3E%3Aapi%3C1%3E.tar.gz
  ===> Fetching [OK]: Color::Scheme:ver<1.001003>:auth<cpan:HOLLI>:api<1> to /home/coke/sandbox/blin/data/zef-data/tmp/1789391870.81228.7100.044729081471/Color%3A%3AScheme%3Aver%3C1.001003%3E%3Aauth%3Ccpan%3AHOLLI%3E%3Aapi%3C1%3E.tar.gz
  [Color::Scheme] Command: tar -t -f ./Color%3A%3AScheme%3Aver%3C1.001003%3E%3Aauth%3Ccpan%3AHOLLI%3E%3Aapi%3C1%3E.tar.gz
  [Color::Scheme] Command: tar -xvf ./Color%3A%3AScheme%3Aver%3C1.001003%3E%3Aauth%3Ccpan%3AHOLLI%3E%3Aapi%3C1%3E.tar.gz -C ../Color%3A%3AScheme%3Aver%3C1.001003%3E%3Aauth%3Ccpan%3AHOLLI%3E%3Aapi%3C1%3E.tar.gz
  ===> Extraction [OK]: Color::Scheme to /home/coke/sandbox/blin/data/zef-data/tmp/Color%3A%3AScheme%3Aver%3C1.001003%3E%3Aauth%3Ccpan%3AHOLLI%3E%3Aapi%3C1%3E.tar.gz
  ===> Testing: Color::Scheme:ver<1.001003>:auth<github:holli-holzer>:api<1>
  [Color::Scheme] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Color%3A%3AScheme%3Aver%3C1.001003%3E%3Aauth%3Ccpan%3AHOLLI%3E%3Aapi%3C1%3E.tar.gz/Color-Scheme-1.001003 t/01-basic.t
  [Color::Scheme] 1..19
  [Color::Scheme] ok 1 - 
  [Color::Scheme] ok 2 - 
  [Color::Scheme] ok 3 - 
  [Color::Scheme] ok 4 - 
  [Color::Scheme] ok 5 - 
  [Color::Scheme] ok 6 - 
  [Color::Scheme] ok 7 - 
  [Color::Scheme] ok 8 - 
  [Color::Scheme] ok 9 - 
  [Color::Scheme] ok 10 - 
  [Color::Scheme] ok 11 - 
  [Color::Scheme] ok 12 - 
  [Color::Scheme] ok 13 - 
  [Color::Scheme] ok 14 - 
  [Color::Scheme] ok 15 - 
  [Color::Scheme] ok 16 - 
  [Color::Scheme] ok 17 - 
  [Color::Scheme] ok 18 - 
  [Color::Scheme] ok 19 - 
  ===> Testing [OK] for Color::Scheme:ver<1.001003>:auth<github:holli-holzer>:api<1>
  ===> Installing: Color::Scheme:ver<1.001003>:auth<github:holli-holzer>:api<1>
  ===> Install [OK] for Color::Scheme:ver<1.001003>:auth<github:holli-holzer>:api<1>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 45.369s
               CPU time consumed: 1min 2.721s
                     Memory peak: 1.8G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p80945-i8436225.service; invocation ID: 5cd359f5f1be4d2ab1c97f70fd8908ea
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Color::Scheme
  No candidates found matching identity: Color::Scheme
            Finished with result: exit-code
  Main processes terminated with: code=exited, status=255/EXCEPTION
                 Service runtime: 6.380s
               CPU time consumed: 6.779s
                     Memory peak: 559.4M (swap: 0B)

  ```
  </details>
* [ ] [XML::Writer](https://raku.land//XML::Writer) – Fail, Bisected: [b88ac8f](https://github.com/rakudo/rakudo/commit/b88ac8f8f0c5442dcb826b5a9cca668b0282d28a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p81381-i8400087.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: XML::Writer
  ===> Found: XML::Writer [via Zef::Repository::Ecosystems<rea>]
  [XML::Writer] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789391868.81384.8660.601727495516/XML%3A%3AWriter%3Aver%3C%2A%3E%3Aauth%3Cgithub%3Amasak%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/X/XML%3A%3AWriter/XML%3A%3AWriter%3Aver%3C%2A%3E%3Aauth%3Cgithub%3Amasak%3E.tar.gz
  ===> Fetching [OK]: XML::Writer to /home/coke/sandbox/blin/data/zef-data/tmp/1789391868.81384.8660.601727495516/XML%3A%3AWriter%3Aver%3C%2A%3E%3Aauth%3Cgithub%3Amasak%3E.tar.gz
  [XML::Writer] Command: tar -t -f ./XML%3A%3AWriter%3Aver%3C%2A%3E%3Aauth%3Cgithub%3Amasak%3E.tar.gz
  [XML::Writer] Command: tar -xvf ./XML%3A%3AWriter%3Aver%3C%2A%3E%3Aauth%3Cgithub%3Amasak%3E.tar.gz -C ../XML%3A%3AWriter%3Aver%3C%2A%3E%3Aauth%3Cgithub%3Amasak%3E.tar.gz
  ===> Extraction [OK]: XML::Writer to /home/coke/sandbox/blin/data/zef-data/tmp/XML%3A%3AWriter%3Aver%3C%2A%3E%3Aauth%3Cgithub%3Amasak%3E.tar.gz
  ===> Testing: XML::Writer
  [XML::Writer] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/XML%3A%3AWriter%3Aver%3C%2A%3E%3Aauth%3Cgithub%3Amasak%3E.tar.gz/xml-writer-master t/escaping.t
  [XML::Writer] 1..3
  [XML::Writer] ok 1 - plain text is escaped (<>)
  [XML::Writer] ok 2 - plain text is escaped (&)
  [XML::Writer] ok 3 - plain text is escaped (")
  [XML::Writer] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/XML%3A%3AWriter%3Aver%3C%2A%3E%3Aauth%3Cgithub%3Amasak%3E.tar.gz/xml-writer-master t/structure.t
  [XML::Writer] 1..8
  [XML::Writer] ok 1 - Cannot serialize nothing
  [XML::Writer] ok 2 - Single root element (named)
  [XML::Writer] ok 3 - Single root element (positional)
  [XML::Writer] ok 4 - Can either pass named or positional
  [XML::Writer] ok 5 - Single root element with text contents
  [XML::Writer] ok 6 - attribute
  [XML::Writer] ok 7 - numbers also work like text
  [XML::Writer] ok 8 - Long XML is occasionally line-wrapped
  ===> Testing [OK] for XML::Writer
  ===> Installing: XML::Writer
  ===> Install [OK] for XML::Writer
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 36.863s
               CPU time consumed: 51.909s
                     Memory peak: 1.3G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p80388-i8508745.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: XML::Writer
  No candidates found matching identity: XML::Writer
            Finished with result: exit-code
  Main processes terminated with: code=exited, status=255/EXCEPTION
                 Service runtime: 22.540s
               CPU time consumed: 5.256s
                     Memory peak: 591.5M (swap: 0B)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| Fail                      |     4 | [Color::Scheme](https://raku.land/cpan:HOLLI/Color::Scheme) [Polyglot::Regexen](https://raku.land/zef:guifa/Polyglot::Regexen) [Text::Fortune](https://raku.land/github:zengargoyle/Text::Fortune) [XML::Writer](https://raku.land//XML::Writer) |
| AlwaysFail                |     6 | [Intl::LanguageTag](https://raku.land/zef:guifa/Intl::LanguageTag) [JSON::Class](https://raku.land/zef:jonathanstowe/JSON::Class) [License::SPDX](https://raku.land/zef:jonathanstowe/License::SPDX) [META6](https://raku.land/zef:jonathanstowe/META6) [Test::META](https://raku.land/zef:jonathanstowe/Test::META) [User::Language](https://raku.land/zef:guifa/User::Language) |
| OK                        |    36 | ⋯                         |



This run started on 2026-09-14T13:24:56Z and finished in 9 minutes.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
