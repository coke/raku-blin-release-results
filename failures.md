[Blin](https://github.com/Raku/Blin) results between 2026.08 ([24e6e53](https://github.com/rakudo/rakudo/commit/24e6e5312f2868680413b0597aef8772f6b5bcea)) and 00feb606ab ([00feb60](https://github.com/rakudo/rakudo/commit/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2)):

* [ ] [Proxy::Watched](https://raku.land/cpan:THINCH/Proxy::Watched) – Fail, Bisected: [00feb60](https://github.com/rakudo/rakudo/commit/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3616983-i7872900.service; invocation ID: e6a7013ef9914c0ea7cf636789a5c273
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Proxy::Watched
  ===> Found: Proxy::Watched:ver<0.0.2>:auth<cpan:THINCH> [via Zef::Repository::Ecosystems<rea>]
  [Proxy::Watched] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789344963.3616991.635.1593013250567/Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/P/Proxy%3A%3AWatched/Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz
  ===> Fetching [OK]: Proxy::Watched:ver<0.0.2>:auth<cpan:THINCH> to /home/coke/sandbox/blin/data/zef-data/tmp/1789344963.3616991.635.1593013250567/Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz
  [Proxy::Watched] Command: tar -t -f ./Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz
  [Proxy::Watched] Command: tar -xvf ./Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz -C ../Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz
  ===> Extraction [OK]: Proxy::Watched to /home/coke/sandbox/blin/data/zef-data/tmp/Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz
  ===> Testing: Proxy::Watched:ver<0.0.2>:auth<github:spidererrol>
  [Proxy::Watched] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz/Proxy-Watched-0.0.2 t/01-basic.t
  [Proxy::Watched] 1..46
  [Proxy::Watched] ok 1 - watched-int created
  [Proxy::Watched] ok 2 - watched-int tapped
  [Proxy::Watched] ok 3 - watched-int is correct
  [Proxy::Watched] ok 4 - Tap got correct value
  [Proxy::Watched] ok 5 - Type error when assigning string to watched-int
  [Proxy::Watched] ok 6 - No extra tap triggered
  [Proxy::Watched] ok 7 - watched-int-init is defined
  [Proxy::Watched] ok 8 - watched-int-init is 7
  [Proxy::Watched] ok 9 - watched-six created
  [Proxy::Watched] ok 10 - watched-six tapped
  [Proxy::Watched] ok 11 - watched-six is correct
  [Proxy::Watched] ok 12 - Tap got correct value
  [Proxy::Watched] ok 13 - watched-any created
  [Proxy::Watched] ok 14 - watched-any tapped
  [Proxy::Watched] ok 15 - watched-any is correct
  [Proxy::Watched] ok 16 - Tap got correct value
  [Proxy::Watched] ok 17 - watched-any-init
  [Proxy::Watched] ok 18 - waitfor created
  [Proxy::Watched] ok 19 - waitfor succeeded
  [Proxy::Watched] ok 20 - Check correct value was waited for
  [Proxy::Watched] ok 21 - joint created
  [Proxy::Watched] ok 22 - Joint value changed correctly
  [Proxy::Watched] ok 23 - Tap updated with correct value
  [Proxy::Watched] ok 24 - Joint value change to string
  [Proxy::Watched] ok 25 - Tap updated with string value
  [Proxy::Watched] ok 26 - joint wait-for succeeded
  [Proxy::Watched] ok 27 - joint wait-for already-met set succeeded
  [Proxy::Watched] ok 28 - Confirm joint value is as waited for
  [Proxy::Watched] ok 29 - Confirm tapped value is as waited for
  [Proxy::Watched] ok 30 - joint-typed is Int-ish
  [Proxy::Watched] ok 31 - joint-typed is 7
  [Proxy::Watched] ok 32 - Type error when assigning string to joint-typed
  [Proxy::Watched] ok 33 - joint-typed is still 7
  [Proxy::Watched] ok 34 - joint-typed-init is 7
  [Proxy::Watched] ok 35 - Type error when assigning string to joint-typed-init
  [Proxy::Watched] ok 36 - joint-typed-init is still 7
  [Proxy::Watched] ok 37 - joint-init-by-type is 7
  [Proxy::Watched] ok 38 - Type error when assigning string to joint-init-by-type
  [Proxy::Watched] ok 39 - joint-init-by-type is still 7
  [Proxy::Watched] ok 40 - joint-any-init is 7
  [Proxy::Watched] ok 41 - No type error when assigning string to joint-any-init
  [Proxy::Watched] ok 42 - joint-any-init is now String
  [Proxy::Watched] ok 43 - Ensure wait-for(&code) works
  [Proxy::Watched] ok 44 - Ensure wait-for(Junction) works (10)
  [Proxy::Watched] ok 45 - Ensure wait-while(Junction) works (8)
  [Proxy::Watched] ok 46 - Ensure combined wait-for(Junction) works (10)
  ===> Testing [OK] for Proxy::Watched:ver<0.0.2>:auth<github:spidererrol>
  ===> Installing: Proxy::Watched:ver<0.0.2>:auth<github:spidererrol>
  ===> Install [OK] for Proxy::Watched:ver<0.0.2>:auth<github:spidererrol>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 2.378s
               CPU time consumed: 2min 8.429s
                     Memory peak: 1.3G (swap: 175.9M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3615097-i7880992.service; invocation ID: 9aa3184a4b7f441f9c41efc77373718c
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Proxy::Watched
  ===> Found: Proxy::Watched:ver<0.0.2>:auth<cpan:THINCH> [via Zef::Repository::Ecosystems<rea>]
  [Proxy::Watched] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789344840.3615098.3343.0056795235187/Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/P/Proxy%3A%3AWatched/Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz
  ===> Fetching [OK]: Proxy::Watched:ver<0.0.2>:auth<cpan:THINCH> to /home/coke/sandbox/blin/data/zef-data/tmp/1789344840.3615098.3343.0056795235187/Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz
  [Proxy::Watched] Command: tar -t -f ./Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz
  [Proxy::Watched] Command: tar -xvf ./Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz -C ../Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz
  ===> Extraction [OK]: Proxy::Watched to /home/coke/sandbox/blin/data/zef-data/tmp/Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz
  ===> Testing: Proxy::Watched:ver<0.0.2>:auth<github:spidererrol>
  [Proxy::Watched] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Proxy%3A%3AWatched%3Aver%3C0.0.2%3E%3Aauth%3Ccpan%3ATHINCH%3E.tar.gz/Proxy-Watched-0.0.2 t/01-basic.t
  [Proxy::Watched] 1..46
  [Proxy::Watched] ok 1 - watched-int created
  [Proxy::Watched] ok 2 - watched-int tapped
  [Proxy::Watched] ok 3 - watched-int is correct
  [Proxy::Watched] ok 4 - Tap got correct value
  [Proxy::Watched] ok 5 - Type error when assigning string to watched-int
  [Proxy::Watched] ok 6 - No extra tap triggered
  [Proxy::Watched] ok 7 - watched-int-init is defined
  [Proxy::Watched] ok 8 - watched-int-init is 7
  [Proxy::Watched] ok 9 - watched-six created
  [Proxy::Watched] ok 10 - watched-six tapped
  [Proxy::Watched] ok 11 - watched-six is correct
  [Proxy::Watched] ok 12 - Tap got correct value
  [Proxy::Watched] ok 13 - watched-any created
  [Proxy::Watched] ok 14 - watched-any tapped
  [Proxy::Watched] ok 15 - watched-any is correct
  [Proxy::Watched] ok 16 - Tap got correct value
  [Proxy::Watched] ok 17 - watched-any-init
  [Proxy::Watched] ok 18 - waitfor created
  [Proxy::Watched] not ok 19 - Failed to wait-for
  [Proxy::Watched] # Failed test 'Failed to wait-for'
  [Proxy::Watched] # at t/01-basic.t line 67
  [Proxy::Watched] ok 20 - waitfor succeeded
  [Proxy::Watched] ok 21 - Check correct value was waited for
  [Proxy::Watched] ok 22 - joint created
  [Proxy::Watched] ok 23 - Joint value changed correctly
  [Proxy::Watched] ok 24 - Tap updated with correct value
  [Proxy::Watched] ok 25 - Joint value change to string
  [Proxy::Watched] ok 26 - Tap updated with string value
  [Proxy::Watched] ok 27 - joint wait-for succeeded
  [Proxy::Watched] ok 28 - joint wait-for already-met set succeeded
  [Proxy::Watched] ok 29 - Confirm joint value is as waited for
  [Proxy::Watched] ok 30 - Confirm tapped value is as waited for
  [Proxy::Watched] ok 31 - joint-typed is Int-ish
  [Proxy::Watched] ok 32 - joint-typed is 7
  [Proxy::Watched] ok 33 - Type error when assigning string to joint-typed
  [Proxy::Watched] ok 34 - joint-typed is still 7
  [Proxy::Watched] ok 35 - joint-typed-init is 7
  [Proxy::Watched] ok 36 - Type error when assigning string to joint-typed-init
  [Proxy::Watched] ok 37 - joint-typed-init is still 7
  [Proxy::Watched] ok 38 - joint-init-by-type is 7
  [Proxy::Watched] ok 39 - Type error when assigning string to joint-init-by-type
  [Proxy::Watched] ok 40 - joint-init-by-type is still 7
  [Proxy::Watched] ok 41 - joint-any-init is 7
  [Proxy::Watched] ok 42 - No type error when assigning string to joint-any-init
  [Proxy::Watched] ok 43 - joint-any-init is now String
  [Proxy::Watched] ok 44 - Ensure wait-for(&code) works
  [Proxy::Watched] ok 45 - Ensure wait-for(Junction) works (10)
  [Proxy::Watched] ok 46 - Ensure wait-while(Junction) works (8)
  [Proxy::Watched] ok 47 - Ensure combined wait-for(Junction) works (10)
  [Proxy::Watched] # You planned 46 tests, but ran 47
  [Proxy::Watched] # You failed 1 test of 47
  ===> Testing [FAIL]: Proxy::Watched:ver<0.0.2>:auth<github:spidererrol>
  [Proxy::Watched] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Proxy::Watched:ver<0.0.2>:auth<github:spidererrol>
  ===> Install [OK] for Proxy::Watched:ver<0.0.2>:auth<github:spidererrol>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 40.922s
               CPU time consumed: 35.604s
                     Memory peak: 1.2G (swap: 0B)

  ```
  </details>
* [ ] [Polyglot::Regexen](https://raku.land/zef:guifa/Polyglot::Regexen) – Fail, Bisected: [aab0778](https://github.com/rakudo/rakudo/commit/aab0778725da5848824f07514c0ae355d972926a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3617776-i7836324.service; invocation ID: 9f28f1da7f89412abd1f4879230f9a44
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Polyglot::Regexen
  ===> Found: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> [via Zef::Repository::Ecosystems<fez>]
  [Polyglot::Regexen] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789344954.3617777.7322.804729451475/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz https://360.zef.pm/P/OL/POLYGLOT_REGEXEN/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Fetching [OK]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> to /home/coke/sandbox/blin/data/zef-data/tmp/1789344954.3617777.7322.804729451475/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
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
                 Service runtime: 1min 52.688s
               CPU time consumed: 2min 16.022s
                     Memory peak: 1.5G (swap: 2.9M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3614913-i7872861.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Polyglot::Regexen
  ===> Found: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> [via Zef::Repository::Ecosystems<rea>]
  [Polyglot::Regexen] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789344822.3614914.3682.7555271100578/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/P/Polyglot%3A%3ARegexen/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz
  ===> Fetching [OK]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> to /home/coke/sandbox/blin/data/zef-data/tmp/1789344822.3614914.3682.7555271100578/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz
  [Polyglot::Regexen] Command: tar -t -f ./Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz
  [Polyglot::Regexen] Command: tar -xvf ./Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz -C ../Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz
  ===> Extraction [OK]: Polyglot::Regexen to /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz
  ===> Testing: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/00-sanity.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] 1..1
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/ecma/01-literals.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/ecma/02-character-classes.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/ecma/03-alternation.rakutest
  [Polyglot::Regexen] ok 1 - Simple alternation, two terms
  [Polyglot::Regexen] ok 2 - Simple alternation, three terms
  [Polyglot::Regexen] 1..2
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/ecma/04-assertions.rakutest
  [Polyglot::Regexen] ok 1 - Simple lookahead
  [Polyglot::Regexen] ok 2 - Simple negative lookahead
  [Polyglot::Regexen] ok 3 - Simple lookbehind
  [Polyglot::Regexen] ok 4 - Simple negative lookbehind
  [Polyglot::Regexen] 1..4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/ecma/05-quantifiers.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/ecma/06-captures.rakutest
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
  [Polyglot::Regexen] not ok 3 - Sequential positional
  [Polyglot::Regexen] # Failed test 'Sequential positional'
  [Polyglot::Regexen] # at t/ecma/06-captures.rakutest line 14
  [Polyglot::Regexen] # expected: '/[$<1>=[a]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }][$<2>=[b]{ $¢.register-position($/.AT-POS(2, :ECMA262-INTERNAL), 2) }]/'
  [Polyglot::Regexen] #      got: '/[$1=[a]{ $¢.register-position($/.AT-POS(1, :ECMA262-INTERNAL), 1) }][$2=[b]{ $¢.register-position($/.AT-POS(2, :ECMA262-INTERNAL), 2) }]/'
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/ecma/07-unicode.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/ecma/08-modifiers.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] ok 2 - 
  [Polyglot::Regexen] ok 3 - 
  [Polyglot::Regexen] ok 4 - 
  [Polyglot::Regexen] 1..4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/ecma/09-role.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/00feb606ab6eda4beedfd7102d8ae62a20b1a2e2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Polyglot%3A%3ARegexen%3Aver%3C0.1.0%3E%3Aauth%3Czef%3Aguifa%3E.tar.gz/dist t/ecma/10-usage.rakutest
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
                 Service runtime: 1min 6.233s
               CPU time consumed: 1min 5.617s
                     Memory peak: 1.5G (swap: 59.3M)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| InstallableButUntested    |     1 | [IO::Socket::Async::SSL](https://raku.land/zef:raku-community-modules/IO::Socket::Async::SSL) |
| Fail                      |     2 | [Polyglot::Regexen](https://raku.land/zef:guifa/Polyglot::Regexen) [Proxy::Watched](https://raku.land/cpan:THINCH/Proxy::Watched) |
| AlwaysFail                |    14 | [AttrX::Mooish](https://raku.land/zef:vrurg/AttrX::Mooish) [Cairo](https://raku.land//Cairo) [Code::Coverable](https://raku.land/zef:lizmat/Code::Coverable) [DBIish](https://raku.land/zef:raku-community-modules/DBIish) [DBIish](https://raku.land/github:raku-community-modules/DBIish) [DOM::Tiny](https://raku.land/cpan:HANENKAMP/DOM::Tiny) [Data::Dump::Tree](https://raku.land/zef:raku-community-modules/Data::Dump::Tree) [JSON::Class](https://raku.land/zef:jonathanstowe/JSON::Class) [License::SPDX](https://raku.land/zef:jonathanstowe/License::SPDX) [META6](https://raku.land/zef:jonathanstowe/META6) [Net::DNS](https://raku.land/zef:rbt/Net::DNS) [Semaphore::ReadersWriters](https://raku.land//Semaphore::ReadersWriters) [Test::META](https://raku.land/zef:jonathanstowe/Test::META) [Text::CSV](https://raku.land/zef:Tux/Text::CSV) |
| OK                        |   156 | ⋯                         |



This run started on 2026-09-14T00:25:42Z and finished in 13 minutes.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
