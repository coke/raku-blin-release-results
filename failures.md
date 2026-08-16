[Blin](https://github.com/Raku/Blin) results between 2026.07 ([d53a85f](https://github.com/rakudo/rakudo/commit/d53a85f9deeffbaba941e1cd1f86149a797b2b09)) and HEAD ([2b05993](https://github.com/rakudo/rakudo/commit/2b05993c58a7884f262f61cb81340e5ed58381b3)):

* [ ] [Cro::FCGI](https://raku.land/zef:patrickb/Cro::FCGI) – Fail, Bisected: [4b4af55](https://github.com/rakudo/rakudo/commit/4b4af55da39bb255f1e540b869e16d338073698b)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3026923-i3068975.service; invocation ID: 0b044b563af842ce8791bab4ecbe012a
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Cro::FCGI
  ===> Found: Cro::FCGI:ver<1.0.1>:auth<zef:patrickb> [via Zef::Repository::Ecosystems<fez>]
  [Cro::FCGI] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849279.3026928.6187.633253712523/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz https://360.zef.pm/C/RO/CRO_FCGI/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz
  ===> Fetching [OK]: Cro::FCGI:ver<1.0.1>:auth<zef:patrickb> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849279.3026928.6187.633253712523/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz
  [Cro::FCGI] Command: tar -t -f ./148040a42819bf474856b9a58e47fdcde62b8314.tar.gz
  [Cro::FCGI] Command: tar -xvf ./148040a42819bf474856b9a58e47fdcde62b8314.tar.gz -C ../148040a42819bf474856b9a58e47fdcde62b8314.tar.gz
  ===> Extraction [OK]: Cro::FCGI to /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz
  ===> Testing: Cro::FCGI:ver<1.0.1>:auth<zef:patrickb>
  [Cro::FCGI] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz/dist t/name-value-pair.rakutest
  [Cro::FCGI] ok 1 - Fail on single byte name value pair
  [Cro::FCGI] ok 2 - Fail on too few bytes for four byte name length
  [Cro::FCGI] ok 3 - Fail on missing content bytes
  [Cro::FCGI] ok 4 - Empty Params record
  [Cro::FCGI] ok 5 - Params record with single byte lengths
  [Cro::FCGI] ok 6 - Params record with multi byte name
  [Cro::FCGI] ok 7 - Params record with multi byte value
  [Cro::FCGI] ok 8 - Params record with multi byte name and value
  [Cro::FCGI] 1..8
  [Cro::FCGI] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz/dist t/record-parser.rakutest
  [Cro::FCGI] ok 1 - FCGI record parser is a transform
  [Cro::FCGI] ok 2 - FCGI record parser consumes TCP messages
  [Cro::FCGI] ok 3 - FCGI record parser produces FCGI records
  [Cro::FCGI] ok 4 - Unsupported version dies
  [Cro::FCGI] ok 5 - Empty Params record
  [Cro::FCGI] ok 6 - GetValues record parses
  [Cro::FCGI] ok 7 - Fail on GetValues with non-empty values
  [Cro::FCGI] ok 8 - Fail on GetValues with request ID
  [Cro::FCGI] ok 9 - Unknown type parses
  [Cro::FCGI] ok 10 - BeginRequest parses
  [Cro::FCGI] ok 11 - Fail on BeginRequest with unknown role
  [Cro::FCGI] ok 12 - STDIN stream record parses
  [Cro::FCGI] ok 13 - Fail on STDIN stream without request ID
  [Cro::FCGI] ok 14 - AbortRequest record parses
  [Cro::FCGI] ok 15 - Fail on AbortRequest without request ID
  [Cro::FCGI] ok 16 - Fail on AbortRequest with non-empty body
  [Cro::FCGI] 1..16
  [Cro::FCGI] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz/dist t/record-serializer.rakutest
  [Cro::FCGI] ok 1 - FCGI record serializer is a transform
  [Cro::FCGI] ok 2 - FCGI record serializer consumes FCGI records
  [Cro::FCGI] ok 3 - FCGI record serializer produces TCP messages
  [Cro::FCGI] ok 4 - Simple unknown type record
  [Cro::FCGI] ok 5 - Simple end request record
  [Cro::FCGI] ok 6 - Simple begin request record
  [Cro::FCGI] ok 7 - Simple params record
  [Cro::FCGI] ok 8 - Simple byte stream record
  [Cro::FCGI] ok 9 - Simple byte stream record on padding boundary
  [Cro::FCGI] ok 10 - Simple byte stream record with end of data
  [Cro::FCGI] ok 11 - Simple byte stream record with end of data
  [Cro::FCGI] 1..11
  [Cro::FCGI] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz/dist t/request-parser.rakutest
  [Cro::FCGI] ok 1 - check 1
  [Cro::FCGI] ok 2 - check 2
  [Cro::FCGI] ok 3 - check 3
  [Cro::FCGI] ok 4 - check 4
  [Cro::FCGI] ok 5 - check 5
  [Cro::FCGI] ok 6 - Params
  [Cro::FCGI] ok 7 - check 1
  [Cro::FCGI] ok 8 - check 2
  [Cro::FCGI] ok 9 - check 3
  [Cro::FCGI] ok 10 - check 4
  [Cro::FCGI] ok 11 - check 5
  [Cro::FCGI] ok 12 - check 6
  [Cro::FCGI] ok 13 - check 7
  [Cro::FCGI] ok 14 - Multiple param records
  [Cro::FCGI] ok 15 - check 1
  [Cro::FCGI] ok 16 - check 2
  [Cro::FCGI] ok 17 - check 3
  [Cro::FCGI] ok 18 - check 4
  [Cro::FCGI] ok 19 - check 5
  [Cro::FCGI] ok 20 - check 6
  [Cro::FCGI] ok 21 - check 7
  [Cro::FCGI] ok 22 - check 8
  [Cro::FCGI] ok 23 - check 9
  [Cro::FCGI] ok 24 - Params + Body
  [Cro::FCGI] ok 25 - check 1
  [Cro::FCGI] ok 26 - check 2
  [Cro::FCGI] ok 27 - check 3
  [Cro::FCGI] ok 28 - check 4
  [Cro::FCGI] ok 29 - check 5
  [Cro::FCGI] ok 30 - check 6
  [Cro::FCGI] ok 31 - check 7
  [Cro::FCGI] ok 32 - check 8
  [Cro::FCGI] ok 33 - check 9
  [Cro::FCGI] ok 34 - check 10
  [Cro::FCGI] ok 35 - Multiple Param records + Body
  [Cro::FCGI] ok 36 - check 1
  [Cro::FCGI] ok 37 - check 2
  [Cro::FCGI] ok 38 - check 3
  [Cro::FCGI] ok 39 - check 4
  [Cro::FCGI] ok 40 - check 5
  [Cro::FCGI] ok 41 - check 6
  [Cro::FCGI] ok 42 - check 7
  [Cro::FCGI] ok 43 - check 8
  [Cro::FCGI] ok 44 - check 9
  [Cro::FCGI] ok 45 - check 1
  [Cro::FCGI] ok 46 - check 2
  [Cro::FCGI] ok 47 - check 10
  [Cro::FCGI] ok 48 - check 3
  [Cro::FCGI] ok 49 - check 4
  [Cro::FCGI] ok 50 - check 5
  [Cro::FCGI] ok 51 - check 6
  [Cro::FCGI] ok 52 - check 7
  [Cro::FCGI] ok 53 - Params1 + Params2 + Body1
  [Cro::FCGI] ok 54 - check 1
  [Cro::FCGI] ok 55 - check 2
  [Cro::FCGI] ok 56 - check 3
  [Cro::FCGI] ok 57 - check 4
  [Cro::FCGI] ok 58 - check 5
  [Cro::FCGI] ok 59 - check 6
  [Cro::FCGI] ok 60 - check 7
  [Cro::FCGI] ok 61 - check 8
  [Cro::FCGI] ok 62 - check 9
  [Cro::FCGI] ok 63 - check 1
  [Cro::FCGI] ok 64 - check 2
  [Cro::FCGI] ok 65 - check 3
  [Cro::FCGI] ok 66 - check 4
  [Cro::FCGI] ok 67 - check 5
  [Cro::FCGI] ok 68 - check 6
  [Cro::FCGI] ok 69 - check 7
  [Cro::FCGI] ok 70 - check 8
  [Cro::FCGI] ok 71 - check 9
  [Cro::FCGI] ok 72 - check 10
  [Cro::FCGI] ok 73 - check 10
  [Cro::FCGI] ok 74 - Params1 + Params2 + Body1 + Body2
  [Cro::FCGI] ok 75 - check 1
  [Cro::FCGI] ok 76 - check 2
  [Cro::FCGI] ok 77 - check 3
  [Cro::FCGI] ok 78 - check 4
  [Cro::FCGI] ok 79 - check 5
  [Cro::FCGI] ok 80 - check 6
  [Cro::FCGI] ok 81 - check 7
  [Cro::FCGI] ok 82 - check 8
  [Cro::FCGI] ok 83 - check 9
  [Cro::FCGI] ok 84 - check 1
  [Cro::FCGI] ok 85 - check 2
  [Cro::FCGI] ok 86 - check 3
  [Cro::FCGI] ok 87 - check 4
  [Cro::FCGI] ok 88 - check 5
  [Cro::FCGI] ok 89 - check 6
  [Cro::FCGI] ok 90 - check 7
  [Cro::FCGI] ok 92 - check 10
  [Cro::FCGI] ok 92 - Params1 + More Params1 + Params2 + Body1
  [Cro::FCGI] ok 93 - check 1
  [Cro::FCGI] ok 94 - check 2
  [Cro::FCGI] ok 95 - check 3
  [Cro::FCGI] ok 96 - check 4
  [Cro::FCGI] ok 97 - check 5
  [Cro::FCGI] ok 98 - check 6
  [Cro::FCGI] ok 99 - check 7
  [Cro::FCGI] ok 100 - check 1
  [Cro::FCGI] ok 101 - check 2
  [Cro::FCGI] ok 102 - check 3
  [Cro::FCGI] ok 103 - check 4
  [Cro::FCGI] ok 104 - check 5
  [Cro::FCGI] ok 105 - check 6
  [Cro::FCGI] ok 106 - check 7
  [Cro::FCGI] ok 107 - Params1 + Params2 + More Params1
  [Cro::FCGI] 1..107
  [Cro::FCGI] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz/dist t/response-serializer.rakutest
  [Cro::FCGI] ok 1 - check 1
  [Cro::FCGI] ok 2 - check 2
  [Cro::FCGI] ok 3 - check 3
  [Cro::FCGI] ok 4 - check 4
  [Cro::FCGI] ok 5 - check 1
  [Cro::FCGI] ok 6 - check 2
  [Cro::FCGI] ok 7 - check 3
  [Cro::FCGI] ok 8 - Header
  [Cro::FCGI] ok 9 - check 1
  [Cro::FCGI] ok 10 - check 2
  [Cro::FCGI] ok 11 - check 3
  [Cro::FCGI] ok 12 - check 4
  [Cro::FCGI] ok 13 - check 1
  [Cro::FCGI] ok 14 - check 2
  [Cro::FCGI] ok 15 - check 3
  [Cro::FCGI] ok 16 - check 4
  [Cro::FCGI] ok 17 - check 1
  [Cro::FCGI] ok 18 - check 2
  [Cro::FCGI] ok 19 - check 3
  [Cro::FCGI] ok 20 - Header + Data
  [Cro::FCGI] ok 21 - check 1
  [Cro::FCGI] ok 22 - check 2
  [Cro::FCGI] ok 23 - check 3
  [Cro::FCGI] ok 24 - check 4
  [Cro::FCGI] ok 25 - check 1
  [Cro::FCGI] ok 26 - check 2
  [Cro::FCGI] ok 27 - check 3
  [Cro::FCGI] ok 28 - check 4
  [Cro::FCGI] ok 29 - check 1
  [Cro::FCGI] ok 30 - check 2
  [Cro::FCGI] ok 31 - check 3
  [Cro::FCGI] ok 32 - Header + Data + Content-Length unspecified
  [Cro::FCGI] ok 33 - Too small body throws
  [Cro::FCGI] ok 34 - Too big body throws
  [Cro::FCGI] 1..34
  ===> Testing [OK] for Cro::FCGI:ver<1.0.1>:auth<zef:patrickb>
  ===> Installing: Cro::FCGI:ver<1.0.1>:auth<zef:patrickb>
  ===> Install [OK] for Cro::FCGI:ver<1.0.1>:auth<zef:patrickb>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 4min 56.852s
               CPU time consumed: 4min 1.200s
                     Memory peak: 2G (swap: 359.4M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3017444-i3041018.service; invocation ID: 588a52f5edeb4e6288abbf4321eba1af
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Cro::FCGI
  ===> Found: Cro::FCGI:ver<1.0.1>:auth<zef:patrickb> [via Zef::Repository::Ecosystems<fez>]
  [Cro::FCGI] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786848961.3017455.3638.7710295541865/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz https://360.zef.pm/C/RO/CRO_FCGI/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz
  ===> Fetching [OK]: Cro::FCGI:ver<1.0.1>:auth<zef:patrickb> to /home/coke/sandbox/blin/data/zef-data/tmp/1786848961.3017455.3638.7710295541865/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz
  [Cro::FCGI] Command: tar -t -f ./148040a42819bf474856b9a58e47fdcde62b8314.tar.gz
  [Cro::FCGI] Command: tar -xvf ./148040a42819bf474856b9a58e47fdcde62b8314.tar.gz -C ../148040a42819bf474856b9a58e47fdcde62b8314.tar.gz
  ===> Extraction [OK]: Cro::FCGI to /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz
  ===> Testing: Cro::FCGI:ver<1.0.1>:auth<zef:patrickb>
  [Cro::FCGI] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz/dist t/name-value-pair.rakutest
  [Cro::FCGI] ok 1 - Fail on single byte name value pair
  [Cro::FCGI] ok 2 - Fail on too few bytes for four byte name length
  [Cro::FCGI] ok 3 - Fail on missing content bytes
  [Cro::FCGI] ok 4 - Empty Params record
  [Cro::FCGI] ok 5 - Params record with single byte lengths
  [Cro::FCGI] ok 6 - Params record with multi byte name
  [Cro::FCGI] ok 7 - Params record with multi byte value
  [Cro::FCGI] ok 8 - Params record with multi byte name and value
  [Cro::FCGI] 1..8
  [Cro::FCGI] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz/dist t/record-parser.rakutest
  [Cro::FCGI] ok 1 - FCGI record parser is a transform
  [Cro::FCGI] ok 2 - FCGI record parser consumes TCP messages
  [Cro::FCGI] ok 3 - FCGI record parser produces FCGI records
  [Cro::FCGI] ok 4 - Unsupported version dies
  [Cro::FCGI] ok 5 - Empty Params record
  [Cro::FCGI] ok 6 - GetValues record parses
  [Cro::FCGI] ok 7 - Fail on GetValues with non-empty values
  [Cro::FCGI] ok 8 - Fail on GetValues with request ID
  [Cro::FCGI] ok 9 - Unknown type parses
  [Cro::FCGI] ok 10 - BeginRequest parses
  [Cro::FCGI] ok 11 - Fail on BeginRequest with unknown role
  [Cro::FCGI] ok 12 - STDIN stream record parses
  [Cro::FCGI] ok 13 - Fail on STDIN stream without request ID
  [Cro::FCGI] ok 14 - AbortRequest record parses
  [Cro::FCGI] ok 15 - Fail on AbortRequest without request ID
  [Cro::FCGI] ok 16 - Fail on AbortRequest with non-empty body
  [Cro::FCGI] 1..16
  [Cro::FCGI] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz/dist t/record-serializer.rakutest
  [Cro::FCGI] ok 1 - FCGI record serializer is a transform
  [Cro::FCGI] ok 2 - FCGI record serializer consumes FCGI records
  [Cro::FCGI] ok 3 - FCGI record serializer produces TCP messages
  [Cro::FCGI] ok 4 - Simple unknown type record
  [Cro::FCGI] ok 5 - Simple end request record
  [Cro::FCGI] ok 6 - Simple begin request record
  [Cro::FCGI] ok 7 - Simple params record
  [Cro::FCGI] ok 8 - Simple byte stream record
  [Cro::FCGI] ok 9 - Simple byte stream record on padding boundary
  [Cro::FCGI] ok 10 - Simple byte stream record with end of data
  [Cro::FCGI] ok 11 - Simple byte stream record with end of data
  [Cro::FCGI] 1..11
  [Cro::FCGI] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz/dist t/request-parser.rakutest
  [Cro::FCGI] ok 1 - check 1
  [Cro::FCGI] ok 2 - check 2
  [Cro::FCGI] ok 3 - check 3
  [Cro::FCGI] ok 4 - check 4
  [Cro::FCGI] ok 5 - check 5
  [Cro::FCGI] ok 6 - Params
  [Cro::FCGI] ok 7 - check 1
  [Cro::FCGI] ok 8 - check 2
  [Cro::FCGI] ok 9 - check 3
  [Cro::FCGI] ok 10 - check 4
  [Cro::FCGI] ok 11 - check 5
  [Cro::FCGI] ok 12 - check 6
  [Cro::FCGI] ok 13 - check 7
  [Cro::FCGI] ok 14 - Multiple param records
  [Cro::FCGI] ok 15 - check 1
  [Cro::FCGI] ok 16 - check 2
  [Cro::FCGI] ok 17 - check 3
  [Cro::FCGI] ok 18 - check 4
  [Cro::FCGI] ok 19 - check 5
  [Cro::FCGI] ok 20 - check 6
  [Cro::FCGI] ok 21 - check 7
  [Cro::FCGI] ok 22 - check 8
  [Cro::FCGI] ok 23 - check 9
  [Cro::FCGI] ok 24 - Params + Body
  [Cro::FCGI] ok 25 - check 1
  [Cro::FCGI] ok 26 - check 2
  [Cro::FCGI] ok 27 - check 3
  [Cro::FCGI] ok 28 - check 4
  [Cro::FCGI] ok 29 - check 5
  [Cro::FCGI] ok 30 - check 6
  [Cro::FCGI] ok 31 - check 7
  [Cro::FCGI] ok 32 - check 8
  [Cro::FCGI] ok 33 - check 9
  [Cro::FCGI] ok 34 - check 10
  [Cro::FCGI] ok 35 - Multiple Param records + Body
  [Cro::FCGI] ok 36 - check 1
  [Cro::FCGI] ok 37 - check 2
  [Cro::FCGI] ok 38 - check 3
  [Cro::FCGI] ok 39 - check 4
  [Cro::FCGI] ok 40 - check 5
  [Cro::FCGI] ok 41 - check 6
  [Cro::FCGI] ok 42 - check 7
  [Cro::FCGI] ok 43 - check 8
  [Cro::FCGI] ok 44 - check 9
  [Cro::FCGI] ok 45 - check 10
  [Cro::FCGI] ok 46 - check 1
  [Cro::FCGI] ok 47 - check 2
  [Cro::FCGI] ok 48 - check 3
  [Cro::FCGI] ok 49 - check 4
  [Cro::FCGI] ok 50 - check 5
  [Cro::FCGI] ok 51 - check 6
  [Cro::FCGI] ok 52 - check 7
  [Cro::FCGI] ok 53 - Params1 + Params2 + Body1
  [Cro::FCGI] ok 54 - check 1
  [Cro::FCGI] ok 55 - check 2
  [Cro::FCGI] ok 56 - check 3
  [Cro::FCGI] ok 57 - check 4
  [Cro::FCGI] ok 58 - check 5
  [Cro::FCGI] ok 59 - check 6
  [Cro::FCGI] ok 60 - check 7
  [Cro::FCGI] ok 61 - check 8
  [Cro::FCGI] ok 62 - check 9
  [Cro::FCGI] ok 63 - check 10
  [Cro::FCGI] ok 64 - check 1
  [Cro::FCGI] ok 65 - check 2
  [Cro::FCGI] ok 66 - check 3
  [Cro::FCGI] ok 67 - check 4
  [Cro::FCGI] ok 68 - check 5
  [Cro::FCGI] ok 69 - check 6
  [Cro::FCGI] ok 70 - check 7
  [Cro::FCGI] ok 71 - check 8
  [Cro::FCGI] ok 72 - check 9
  [Cro::FCGI] ok 73 - check 10
  [Cro::FCGI] ok 74 - Params1 + Params2 + Body1 + Body2
  [Cro::FCGI] ok 75 - check 1
  [Cro::FCGI] ok 76 - check 2
  [Cro::FCGI] ok 77 - check 3
  [Cro::FCGI] ok 78 - check 4
  [Cro::FCGI] ok 79 - check 5
  [Cro::FCGI] ok 80 - check 6
  [Cro::FCGI] ok 81 - check 1
  [Cro::FCGI] ok 82 - check 2
  [Cro::FCGI] ok 83 - check 3
  [Cro::FCGI] ok 84 - check 4
  [Cro::FCGI] ok 85 - check 7
  [Cro::FCGI] ok 86 - check 5
  [Cro::FCGI] ok 87 - check 6
  [Cro::FCGI] ok 88 - check 8
  [Cro::FCGI] ok 89 - check 7
  [Cro::FCGI] ok 90 - check 9
  [Cro::FCGI] ok 91 - Params1 + More Params1 + Params2 + Body1
  [Cro::FCGI] not ok 92 - check 10
  [Cro::FCGI] ok 93 - check 1
  [Cro::FCGI] ok 94 - check 2
  [Cro::FCGI] ok 95 - check 3
  [Cro::FCGI] ok 96 - check 4
  [Cro::FCGI] ok 97 - check 5
  [Cro::FCGI] ok 98 - check 6
  [Cro::FCGI] ok 99 - check 7
  [Cro::FCGI] ok 100 - check 1
  [Cro::FCGI] ok 101 - check 2
  [Cro::FCGI] ok 102 - check 3
  [Cro::FCGI] ok 103 - check 4
  [Cro::FCGI] ok 104 - check 5
  [Cro::FCGI] ok 105 - check 6
  [Cro::FCGI] ok 106 - check 7
  [Cro::FCGI] ok 107 - Params1 + Params2 + More Params1
  [Cro::FCGI] 1..107
  [Cro::FCGI] # You failed 1 test of 107
  [Cro::FCGI] # Failed test 'check 10'
  [Cro::FCGI] # at t/request-parser.rakutest line 28
  [Cro::FCGI] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/148040a42819bf474856b9a58e47fdcde62b8314.tar.gz/dist t/response-serializer.rakutest
  [Cro::FCGI] ok 1 - check 1
  [Cro::FCGI] ok 2 - check 2
  [Cro::FCGI] ok 3 - check 3
  [Cro::FCGI] ok 4 - check 4
  [Cro::FCGI] ok 5 - check 1
  [Cro::FCGI] ok 6 - check 2
  [Cro::FCGI] ok 7 - check 3
  [Cro::FCGI] ok 8 - Header
  [Cro::FCGI] ok 9 - check 1
  [Cro::FCGI] ok 10 - check 2
  [Cro::FCGI] ok 11 - check 3
  [Cro::FCGI] ok 12 - check 4
  [Cro::FCGI] ok 13 - check 1
  [Cro::FCGI] ok 14 - check 2
  [Cro::FCGI] ok 15 - check 3
  [Cro::FCGI] ok 16 - check 4
  [Cro::FCGI] ok 17 - check 1
  [Cro::FCGI] ok 18 - check 2
  [Cro::FCGI] ok 19 - check 3
  [Cro::FCGI] ok 20 - Header + Data
  [Cro::FCGI] ok 21 - check 1
  [Cro::FCGI] ok 22 - check 2
  [Cro::FCGI] ok 23 - check 3
  [Cro::FCGI] ok 24 - check 4
  [Cro::FCGI] ok 25 - check 1
  [Cro::FCGI] ok 26 - check 2
  [Cro::FCGI] ok 27 - check 3
  [Cro::FCGI] ok 28 - check 4
  [Cro::FCGI] ok 29 - check 1
  [Cro::FCGI] ok 30 - check 2
  [Cro::FCGI] ok 31 - check 3
  [Cro::FCGI] ok 32 - Header + Data + Content-Length unspecified
  [Cro::FCGI] ok 33 - Too small body throws
  [Cro::FCGI] ok 34 - Too big body throws
  [Cro::FCGI] 1..34
  ===> Testing [FAIL]: Cro::FCGI:ver<1.0.1>:auth<zef:patrickb>
  [Cro::FCGI] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Cro::FCGI:ver<1.0.1>:auth<zef:patrickb>
  ===> Install [OK] for Cro::FCGI:ver<1.0.1>:auth<zef:patrickb>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 4min 29.786s
               CPU time consumed: 3min 42.937s
                     Memory peak: 2G (swap: 860.5M)

  ```
  </details>
* [ ] [Net::BGP](https://raku.land/zef:jmaslak/Net::BGP) – Fail, Bisected: [8eee823](https://github.com/rakudo/rakudo/commit/8eee823949430a99ce4e2fc8fd2ff8165ac31131)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3148375-i3153008.service; invocation ID: 91edd611c7bc4d0db0f74264a369cc72
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Net::BGP
  ===> Found: Net::BGP:ver<0.9.0>:auth<zef:jmaslak> [via Zef::Repository::Ecosystems<fez>]
  [Net::BGP] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786852451.3148384.9101.882595700548/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz https://360.zef.pm/N/ET/NET_BGP/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  ===> Fetching [OK]: Net::BGP:ver<0.9.0>:auth<zef:jmaslak> to /home/coke/sandbox/blin/data/zef-data/tmp/1786852451.3148384.9101.882595700548/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  [Net::BGP] Command: tar -t -f ./b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  [Net::BGP] Command: tar -xvf ./b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz -C ../b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  ===> Extraction [OK]: Net::BGP to /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  ===> Testing: Net::BGP:ver<0.9.0>:auth<zef:jmaslak>
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/00-conversions.t
  [Net::BGP] # Subtest: nuint16
  [Net::BGP]     ok 1 - 
  [Net::BGP]     ok 2 - 
  [Net::BGP]     ok 3 - 
  [Net::BGP]     ok 4 - 
  [Net::BGP]     ok 5 - 
  [Net::BGP]     ok 6 - 
  [Net::BGP]     ok 7 - 
  [Net::BGP]     ok 8 - 
  [Net::BGP]     ok 9 - 
  [Net::BGP]     ok 10 - 
  [Net::BGP]     ok 11 - 
  [Net::BGP]     ok 12 - 
  [Net::BGP]     ok 13 - 
  [Net::BGP]     ok 14 - 
  [Net::BGP]     ok 15 - 
  [Net::BGP]     ok 16 - 
  [Net::BGP]     ok 17 - 258 is encoded properly
  [Net::BGP]     1..17
  [Net::BGP] ok 1 - nuint16
  [Net::BGP] # Subtest: nunit32
  [Net::BGP]     ok 1 - 
  [Net::BGP]     ok 2 - 
  [Net::BGP]     ok 3 - 
  [Net::BGP]     ok 4 - 
  [Net::BGP]     ok 5 - 
  [Net::BGP]     ok 6 - 
  [Net::BGP]     ok 7 - 
  [Net::BGP]     ok 8 - 
  [Net::BGP]     ok 9 - 
  [Net::BGP]     ok 10 - 
  [Net::BGP]     ok 11 - 
  [Net::BGP]     ok 12 - 
  [Net::BGP]     ok 13 - 
  [Net::BGP]     ok 14 - 
  [Net::BGP]     ok 15 - 
  [Net::BGP]     ok 16 - 
  [Net::BGP]     ok 17 - 
  [Net::BGP]     ok 18 - 
  [Net::BGP]     ok 19 - 
  [Net::BGP]     ok 20 - 
  [Net::BGP]     ok 21 - 
  [Net::BGP]     1..21
  [Net::BGP] ok 2 - nunit32
  [Net::BGP] # Subtest: nunit128
  [Net::BGP]     ok 1 - 
  [Net::BGP]     ok 2 - 
  [Net::BGP]     ok 3 - 
  [Net::BGP]     ok 4 - 
  [Net::BGP]     ok 5 - 
  [Net::BGP]     ok 6 - 
  [Net::BGP]     ok 7 - 
  [Net::BGP]     ok 8 - 
  [Net::BGP]     ok 9 - 
  [Net::BGP]     ok 10 - 
  [Net::BGP]     ok 11 - 
  [Net::BGP]     1..11
  [Net::BGP] ok 3 - nunit128
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/01-ip-test.t
  [Net::BGP] ok 1 - 1.2.3.4 ipv4-to-int
  [Net::BGP] ok 2 - 1.2.3.4 int-to-ipv4
  [Net::BGP] ok 3 - 1.2.3.4 ipv4-to-int-to-ipv4
  [Net::BGP] ok 4 - 1.2.3.4 int-to-ipv4-to-int
  [Net::BGP] ok 5 - 1.2.3.4 ipv4-to-buf8
  [Net::BGP] ok 6 - 1.2.3.4 ip-valid
  [Net::BGP] ok 7 - 2001:db8::1 ipv6-expand
  [Net::BGP] ok 8 - 2001:db8::1 ipv6-expand (full)
  [Net::BGP] ok 9 - 2001:db8::1 ipv6-to-int
  [Net::BGP] ok 10 - 2001:db8::1 ipv6-compact
  [Net::BGP] ok 11 - 2001:db8::1 int-to-ipv6
  [Net::BGP] ok 12 - 2001:db8::1 ip-valid
  [Net::BGP] ok 13 - 2001:db8::1 ipv6-to-buf-length
  [Net::BGP] ok 14 - 2001:db8::1 0 ipv6-to-buf8
  [Net::BGP] ok 15 - 2001:db8::1 1 ipv6-to-buf8
  [Net::BGP] ok 16 - 2001:db8::1 2 ipv6-to-buf8
  [Net::BGP] ok 17 - 2001:db8::1 3 ipv6-to-buf8
  [Net::BGP] ok 18 - 2001:db8::1 4 ipv6-to-buf8
  [Net::BGP] ok 19 - 2001:db8::1 5 ipv6-to-buf8
  [Net::BGP] ok 20 - 2001:db8::1 6 ipv6-to-buf8
  [Net::BGP] ok 21 - 2001:db8::1 7 ipv6-to-buf8
  [Net::BGP] ok 22 - 2001:db8::1 8 ipv6-to-buf8
  [Net::BGP] ok 23 - 2001:db8::1 9 ipv6-to-buf8
  [Net::BGP] ok 24 - 2001:db8::1 10 ipv6-to-buf8
  [Net::BGP] ok 25 - 2001:db8::1 11 ipv6-to-buf8
  [Net::BGP] ok 26 - 2001:db8::1 12 ipv6-to-buf8
  [Net::BGP] ok 27 - 2001:db8::1 13 ipv6-to-buf8
  [Net::BGP] ok 28 - 2001:db8::1 14 ipv6-to-buf8
  [Net::BGP] ok 29 - 2001:db8::1 15 ipv6-to-buf8
  [Net::BGP] ok 30 - 2001:db8::1 buf8-to-ipv6
  [Net::BGP] ok 31 - 2001:db8::1/0 ipv6-to-buf-length
  [Net::BGP] ok 32 - 2001:db8::1/0 buf8-to-ipv6
  [Net::BGP] ok 33 - 2001:db8::1/64 buf8-to-ipv6
  [Net::BGP] ok 34 - 2001:db8::1/127 ipv6-to-buf-length
  [Net::BGP] ok 35 - 2001:db8::1/127 0 ipv6-to-buf8
  [Net::BGP] ok 36 - 2001:db8::1/127 1 ipv6-to-buf8
  [Net::BGP] ok 37 - 2001:db8::1/127 2 ipv6-to-buf8
  [Net::BGP] ok 38 - 2001:db8::1/127 3 ipv6-to-buf8
  [Net::BGP] ok 39 - 2001:db8::1/127 4 ipv6-to-buf8
  [Net::BGP] ok 40 - 2001:db8::1/127 5 ipv6-to-buf8
  [Net::BGP] ok 41 - 2001:db8::1/127 6 ipv6-to-buf8
  [Net::BGP] ok 42 - 2001:db8::1/127 7 ipv6-to-buf8
  [Net::BGP] ok 43 - 2001:db8::1/127 8 ipv6-to-buf8
  [Net::BGP] ok 44 - 2001:db8::1/127 9 ipv6-to-buf8
  [Net::BGP] ok 45 - 2001:db8::1/127 10 ipv6-to-buf8
  [Net::BGP] ok 46 - 2001:db8::1/127 11 ipv6-to-buf8
  [Net::BGP] ok 47 - 2001:db8::1/127 12 ipv6-to-buf8
  [Net::BGP] ok 48 - 2001:db8::1/127 13 ipv6-to-buf8
  [Net::BGP] ok 49 - 2001:db8::1/127 14 ipv6-to-buf8
  [Net::BGP] ok 50 - 2001:db8::1/127 15 ipv6-to-buf8
  [Net::BGP] ok 51 - 2001:db8::1/127 buf8-to-ipv6
  [Net::BGP] ok 52 - 2001:db8:0:2:3::1 ipv6-expand
  [Net::BGP] ok 53 - 2001:db8:0:2:3::1 ipv6-expand (full)
  [Net::BGP] ok 54 - 2001:db8:0:2:3::1 ipv6-to-int
  [Net::BGP] ok 55 - 2001:db8:0:2:3::1 ipv6-compact
  [Net::BGP] ok 56 - 2001:db8:0:2:3::1 int-to-ipv6
  [Net::BGP] ok 57 - 2001:db8:0:2:3::1 ip-valid
  [Net::BGP] ok 58 - 2001:db8:0:2:3::1 buf8-to-ipv6
  [Net::BGP] ok 59 - 2001:db8:0:2:3::1/0 ipv6-to-buf-length
  [Net::BGP] ok 60 - 2001:db8:0:2:3::1/0 buf8-to-ipv6
  [Net::BGP] ok 61 - 2001:db8:0:002:03::1 ipv6-expand
  [Net::BGP] ok 62 - 2001:db8:0:002:03::1 ipv6-expand (full)
  [Net::BGP] ok 63 - 2001:db8:0:002:03::1 ipv6-to-int
  [Net::BGP] ok 64 - 2001:db8:0:002:03::1 ipv6-compact
  [Net::BGP] ok 65 - 2001:db8:0:002:03::1 int-to-ipv6
  [Net::BGP] ok 66 - 2001:db8:0:002:03::1 ip-valid
  [Net::BGP] ok 67 - 2001:db8:0:002:03::1 buf8-to-ipv6
  [Net::BGP] ok 68 - 2001:db8:0:002:03::1/0 ipv6-to-buf-length
  [Net::BGP] ok 69 - 2001:db8:0:002:03::1/0 buf8-to-ipv6
  [Net::BGP] ok 70 - 2001:dB8:0:002:03::1 ipv6-expand
  [Net::BGP] ok 71 - 2001:dB8:0:002:03::1 ipv6-expand (full)
  [Net::BGP] ok 72 - 2001:dB8:0:002:03::1 ipv6-to-int
  [Net::BGP] ok 73 - 2001:dB8:0:002:03::1 ipv6-compact
  [Net::BGP] ok 74 - 2001:dB8:0:002:03::1 int-to-ipv6
  [Net::BGP] ok 75 - 2001:dB8:0:002:03::1 ip-valid
  [Net::BGP] ok 76 - 2001:dB8:0:002:03::1 buf8-to-ipv6
  [Net::BGP] ok 77 - 2001:dB8:0:002:03::1/0 ipv6-to-buf-length
  [Net::BGP] ok 78 - 2001:dB8:0:002:03::1/0 buf8-to-ipv6
  [Net::BGP] ok 79 - 2605:2700:0:3::4713:93e3 ipv6-expand
  [Net::BGP] ok 80 - 2605:2700:0:3::4713:93e3 ipv6-expand (full)
  [Net::BGP] ok 81 - 2605:2700:0:3::4713:93e3 ipv6-to-int
  [Net::BGP] ok 82 - 2605:2700:0:3::4713:93e3 ipv6-compact
  [Net::BGP] ok 83 - 2605:2700:0:3::4713:93e3 int-to-ipv6
  [Net::BGP] ok 84 - 2605:2700:0:3::4713:93e3 ip-valid
  [Net::BGP] ok 85 - 2605:2700:0:3::4713:93e3 buf8-to-ipv6
  [Net::BGP] ok 86 - 2605:2700:0:3::4713:93e3/0 ipv6-to-buf-length
  [Net::BGP] ok 87 - 2605:2700:0:3::4713:93e3/0 buf8-to-ipv6
  [Net::BGP] ok 88 - :: ipv6-expand
  [Net::BGP] ok 89 - :: ipv6-expand (full)
  [Net::BGP] ok 90 - :: ipv6-to-int
  [Net::BGP] ok 91 - :: ipv6-compact
  [Net::BGP] ok 92 - :: int-to-ipv6
  [Net::BGP] ok 93 - :: ip-valid
  [Net::BGP] ok 94 - :: ipv6-to-buf-length
  [Net::BGP] ok 95 - :: 0 ipv6-to-buf8
  [Net::BGP] ok 96 - :: 1 ipv6-to-buf8
  [Net::BGP] ok 97 - :: 2 ipv6-to-buf8
  [Net::BGP] ok 98 - :: 3 ipv6-to-buf8
  [Net::BGP] ok 99 - :: 4 ipv6-to-buf8
  [Net::BGP] ok 100 - :: 5 ipv6-to-buf8
  [Net::BGP] ok 101 - :: 6 ipv6-to-buf8
  [Net::BGP] ok 102 - :: 7 ipv6-to-buf8
  [Net::BGP] ok 103 - :: 8 ipv6-to-buf8
  [Net::BGP] ok 104 - :: 9 ipv6-to-buf8
  [Net::BGP] ok 105 - :: 10 ipv6-to-buf8
  [Net::BGP] ok 106 - :: 11 ipv6-to-buf8
  [Net::BGP] ok 107 - :: 12 ipv6-to-buf8
  [Net::BGP] ok 108 - :: 13 ipv6-to-buf8
  [Net::BGP] ok 109 - :: 14 ipv6-to-buf8
  [Net::BGP] ok 110 - :: 15 ipv6-to-buf8
  [Net::BGP] ok 111 - :: buf8-to-ipv6
  [Net::BGP] ok 112 - ::/0 ipv6-to-buf-length
  [Net::BGP] ok 113 - ::/0 buf8-to-ipv6
  [Net::BGP] ok 114 - ::/64 buf8-to-ipv6
  [Net::BGP] ok 115 - ::/127 ipv6-to-buf-length
  [Net::BGP] ok 116 - ::/127 0 ipv6-to-buf8
  [Net::BGP] ok 117 - ::/127 1 ipv6-to-buf8
  [Net::BGP] ok 118 - ::/127 2 ipv6-to-buf8
  [Net::BGP] ok 119 - ::/127 3 ipv6-to-buf8
  [Net::BGP] ok 120 - ::/127 4 ipv6-to-buf8
  [Net::BGP] ok 121 - ::/127 5 ipv6-to-buf8
  [Net::BGP] ok 122 - ::/127 6 ipv6-to-buf8
  [Net::BGP] ok 123 - ::/127 7 ipv6-to-buf8
  [Net::BGP] ok 124 - ::/127 8 ipv6-to-buf8
  [Net::BGP] ok 125 - ::/127 9 ipv6-to-buf8
  [Net::BGP] ok 126 - ::/127 10 ipv6-to-buf8
  [Net::BGP] ok 127 - ::/127 11 ipv6-to-buf8
  [Net::BGP] ok 128 - ::/127 12 ipv6-to-buf8
  [Net::BGP] ok 129 - ::/127 13 ipv6-to-buf8
  [Net::BGP] ok 130 - ::/127 14 ipv6-to-buf8
  [Net::BGP] ok 131 - ::/127 15 ipv6-to-buf8
  [Net::BGP] ok 132 - ::/127 buf8-to-ipv6
  [Net::BGP] ok 133 - 2001:db8::1 ip-cannonical
  [Net::BGP] ok 134 - 2001:db8::1 ip-cannonical²
  [Net::BGP] ok 135 - 2001:db8:0::0:1 ip-cannonical
  [Net::BGP] ok 136 - 2001:db8:0::0:1 ip-cannonical²
  [Net::BGP] ok 137 - ::ffff:192.0.2.1 ip-cannonical
  [Net::BGP] ok 138 - ::ffff:192.0.2.1 ip-cannonical²
  [Net::BGP] ok 139 - ::FFFF:192.0.2.1 ip-cannonical
  [Net::BGP] ok 140 - ::FFFF:192.0.2.1 ip-cannonical²
  [Net::BGP] ok 141 - 192.0.2.1 ip-cannonical
  [Net::BGP] ok 142 - 192.0.2.1 ip-cannonical²
  [Net::BGP] ok 143 - :: ip-cannonical
  [Net::BGP] ok 144 - :: ip-cannonical²
  [Net::BGP] ok 145 - 127.0.0.1 ip-cannonical
  [Net::BGP] ok 146 - 127.0.0.1 ip-cannonical²
  [Net::BGP] ok 147 - ::ffff:127.0.0.1 ip-cannonical
  [Net::BGP] ok 148 - ::ffff:127.0.0.1 ip-cannonical²
  [Net::BGP] ok 149 - 1920.0.2.1 ip-valid (invalid)
  [Net::BGP] ok 150 - 1::2::3 ip-valid (invalid)
  [Net::BGP] ok 151 - 2001:db8:g::1 ip-valid (invalid)
  [Net::BGP] # Subtest: IPv4 CIDRs
  [Net::BGP]     ok 1 - CIDR 0.0.0.0/24
  [Net::BGP]     ok 2 - CIDR 10.0.0.0/8
  [Net::BGP]     ok 3 - CIDR 0.0.0.0/0 maps to CIDR
  [Net::BGP]     ok 4 - CIDR 10.0.0.0/8 maps to CIDR
  [Net::BGP]     ok 5 - CIDR 10.0.0.0/24 maps to CIDR
  [Net::BGP]     ok 6 - CIDR 192.0.2.4/30 maps to CIDR
  [Net::BGP]     ok 7 - CIDR 255.255.255.255/32 maps to CIDR
  [Net::BGP]     ok 8 - CIDR 0.0.0.0/a dies ok
  [Net::BGP]     ok 9 - CIDR 192.0.2.1/33 dies ok
  [Net::BGP]     not ok 10 - CIDR 3/29 dies ok # TODO Regex matching is slow...fix lib/Net/BGP/IP.pm6
  [Net::BGP]     # Failed test 'CIDR 3/29 dies ok'
  [Net::BGP]     # at t/01-ip-test.t line 194
  [Net::BGP]     ok 11 - Test 1 - Count Correct
  [Net::BGP]     ok 12 - Test 1 - String Correct
  [Net::BGP]     ok 13 - Test 2 - Count Correct
  [Net::BGP]     ok 14 - Test 2 - String Correct
  [Net::BGP]     ok 15 - Test 3 - Count Correct
  [Net::BGP]     ok 16 - Test 3 - String Correct
  [Net::BGP]     ok 17 - Test 4 - Count Correct
  [Net::BGP]     ok 18 - Test 4 - String Correct
  [Net::BGP]     ok 19 - Test 5 - Count Correct
  [Net::BGP]     ok 20 - Test 5a - String Correct
  [Net::BGP]     ok 21 - Test 5b - String Correct
  [Net::BGP]     ok 22 - 0.0.0.0/0 contains 0.0.0.0/0
  [Net::BGP]     ok 23 - 0.0.0.0/32 does not contain 0.0.0.0/0
  [Net::BGP]     ok 24 - 0.0.0.0/0 contains 10.0.0.0/8
  [Net::BGP]     ok 25 - 0.0.0.0/32 does not contain 10.0.0.0/8
  [Net::BGP]     ok 26 - 0.0.0.0/0 contains 10.0.0.0/24
  [Net::BGP]     ok 27 - 0.0.0.0/32 does not contain 10.0.0.0/24
  [Net::BGP]     ok 28 - 0.0.0.0/0 contains 192.0.2.4/30
  [Net::BGP]     ok 29 - 0.0.0.0/32 does not contain 192.0.2.4/30
  [Net::BGP]     ok 30 - 0.0.0.0/0 contains 255.255.255.255/32
  [Net::BGP]     ok 31 - 0.0.0.0/32 does not contain 255.255.255.255/32
  [Net::BGP]     ok 32 - 4.2.2.0/24 contains 4.2.2.0/24
  [Net::BGP]     ok 33 - 4.2.2.0/32 does not contain 4.2.2.0/32
  [Net::BGP]     ok 34 - 4.2.2.0/24 contains 4.2.2.0/24
  [Net::BGP]     ok 35 - 4.2.2.0/24 contains 4.2.2.0/24
  [Net::BGP]     1..35
  [Net::BGP] ok 152 - IPv4 CIDRs
  [Net::BGP] # Subtest: IPv6 CIDRs
  [Net::BGP]     ok 1 - CIDR ::/0
  [Net::BGP]     ok 2 - CIDR 2001::/16
  [Net::BGP]     ok 3 - CIDR ::/0 maps to CIDR
  [Net::BGP]     ok 4 - CIDR 2001:db8::/32 maps to CIDR
  [Net::BGP]     ok 5 - CIDR 2001:db8:1234::/48 maps to CIDR
  [Net::BGP]     ok 6 - CIDR 2001:db8:4321::ff00/120 maps to CIDR
  [Net::BGP]     ok 7 - CIDR ffff:ffff:ffff:ffff:ffff:ffff:ffff:ffff/128 maps to CIDR
  [Net::BGP]     ok 8 - CIDR ::/a dies ok
  [Net::BGP]     ok 9 - CIDR 2001 dies ok
  [Net::BGP]     ok 10 - CIDR db8	True dies ok
  [Net::BGP]     ok 11 - CIDR ::/129 dies ok
  [Net::BGP]     ok 12 - CIDR 2001:/16 dies ok
  [Net::BGP]     ok 13 - CIDR 2001:55555::/32 dies ok
  [Net::BGP]     ok 14 - Test 1 - Count Correct
  [Net::BGP]     ok 15 - Test 1 - String Correct
  [Net::BGP]     ok 16 - Test 2 - Count Correct
  [Net::BGP]     ok 17 - Test 2 - String Correct
  [Net::BGP]     ok 18 - Test 3 - Count Correct
  [Net::BGP]     ok 19 - Test 3 - String Correct
  [Net::BGP]     ok 20 - Test 4 - Count Correct
  [Net::BGP]     ok 21 - Test 4 - String Correct
  [Net::BGP]     ok 22 - Test 5 - Count Correct
  [Net::BGP]     ok 23 - Test 5a - String Correct
  [Net::BGP]     ok 24 - Test 5b - String Correct
  [Net::BGP]     ok 25 - ::/0 contains ::/0
  [Net::BGP]     ok 26 - ::/128 does not contain ::/0
  [Net::BGP]     ok 27 - ::/0 contains 2001:db8::/32
  [Net::BGP]     ok 28 - ::/128 does not contain 2001:db8::/32
  [Net::BGP]     ok 29 - ::/0 contains 2001:db8:1234::/48
  [Net::BGP]     ok 30 - ::/128 does not contain 2001:db8:1234::/48
  [Net::BGP]     ok 31 - ::/0 contains 2001:db8:4321::ff00/120
  [Net::BGP]     ok 32 - ::/128 does not contain 2001:db8:4321::ff00/120
  [Net::BGP]     ok 33 - ::/0 contains ffff:ffff:ffff:ffff:ffff:ffff:ffff:ffff/128
  [Net::BGP]     ok 34 - ::/128 does not contain ffff:ffff:ffff:ffff:ffff:ffff:ffff:ffff/128
  [Net::BGP]     ok 35 - 2001:db8::/32 contains 2001:db8::/32
  [Net::BGP]     ok 36 - 2001:db8::/48 does not contain 2001:db8::/48
  [Net::BGP]     ok 37 - 2001:db8::/32 contains 2001:db8::/32
  [Net::BGP]     ok 38 - 2001:db8::/32 contains 2001:db8::/32
  [Net::BGP]     1..38
  [Net::BGP] ok 153 - IPv6 CIDRs
  [Net::BGP] # Subtest: Misc. Tests
  [Net::BGP]     ok 1 - buf8-to-ipv4 returns good value
  [Net::BGP]     ok 2 - Long IPv6-ish parts fail parse
  [Net::BGP]     1..2
  [Net::BGP] ok 154 - Misc. Tests
  [Net::BGP] 1..154
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/02-as-list.t
  [Net::BGP] ok 1 - (0) ordered
  [Net::BGP] ok 2 - (0) asn-size
  [Net::BGP] ok 3 - (0) asn-count
  [Net::BGP] ok 4 - (0) elems
  [Net::BGP] ok 5 - (1) ordered
  [Net::BGP] ok 6 - (1) asn-size
  [Net::BGP] ok 7 - (1) asn-count
  [Net::BGP] ok 8 - (1) elems
  [Net::BGP] ok 9 - (1) First ASN
  [Net::BGP] ok 10 - (1) Second ASN
  [Net::BGP] ok 11 - (2) ordered
  [Net::BGP] ok 12 - (2) asn-size
  [Net::BGP] ok 13 - (2) asn-count
  [Net::BGP] ok 14 - (2) elems
  [Net::BGP] ok 15 - (2) First ASN
  [Net::BGP] ok 16 - (2) Second ASN
  [Net::BGP] ok 17 - Proper number of AS lists
  [Net::BGP] ok 18 - First AS Sequence is correct
  [Net::BGP] ok 19 - Second AS Sequence is correct
  [Net::BGP] ok 20 - (A) Proper number of AS lists
  [Net::BGP] ok 21 - (A) First AS Sequence is correct
  [Net::BGP] ok 22 - (B) Proper number of AS lists
  [Net::BGP] ok 23 - (B) First AS Sequence is correct
  [Net::BGP] ok 24 - (B) First AS Sequence is correct (elems)
  [Net::BGP] ok 25 - (B) First AS Sequence Ordering
  [Net::BGP] ok 26 - (B) First AS Sequence path length is correct
  [Net::BGP] ok 27 - (B) Second AS Sequence is correct
  [Net::BGP] ok 28 - (B) Second AS Sequence is correct (elems 1)
  [Net::BGP] ok 29 - (B) Second AS Sequence is correct (elems 2)
  [Net::BGP] ok 30 - (B) Second AS Sequence Ordering
  [Net::BGP] ok 31 - (B) Second AS Sequence path length is correct
  [Net::BGP] ok 32 - (B) Third AS Sequence is correct
  [Net::BGP] ok 33 - (B) Third AS Sequence Ordering
  [Net::BGP] ok 34 - (B) Third AS Sequence path length is correct
  [Net::BGP] ok 35 - (B) Forth AS Sequence is correct
  [Net::BGP] ok 36 - (B) Forth AS Sequence is correct (elems 1)
  [Net::BGP] ok 37 - (B) Forth AS Sequence Ordering
  [Net::BGP] ok 38 - (B) Forth AS Sequence path length is correct
  [Net::BGP] ok 39 - (C) Proper number of AS lists
  [Net::BGP] 1..39
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/03-afi-safi.t
  [Net::BGP] # Subtest: afi
  [Net::BGP]     ok 1 - IP correct¹
  [Net::BGP]     ok 2 - IP correct²
  [Net::BGP]     ok 3 - 15000 correct¹
  [Net::BGP]     ok 4 - 15000 correct²
  [Net::BGP]     ok 5 - Properly dies on unknown name
  [Net::BGP]     1..5
  [Net::BGP] ok 1 - afi
  [Net::BGP] # Subtest: safi
  [Net::BGP]     ok 1 - Unicast correct¹
  [Net::BGP]     ok 2 - Unicast correct²
  [Net::BGP]     ok 3 - 77 correct¹
  [Net::BGP]     ok 4 - 77 correct²
  [Net::BGP]     ok 5 - Properly dies on unknown name
  [Net::BGP]     1..5
  [Net::BGP] ok 2 - safi
  [Net::BGP] 1..2
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/10-linux-socket.t
  [Net::BGP] KERNEL Name: linux
  [Net::BGP] # Subtest: Basic Server
  [Net::BGP]     ok 1 - sock is proper type
  [Net::BGP]     ok 2 - sock is defined
  [Net::BGP]     ok 3 - bound port does not die
  [Net::BGP]     ok 4 - bound port in proper range
  [Net::BGP] # Listening on port 39461
  [Net::BGP]     ok 5 - connections is a Supply
  [Net::BGP]     ok 6 - conn is Socket-Connection
  [Net::BGP]     ok 7 - conn is defined
  [Net::BGP]     ok 8 - my-host matches
  [Net::BGP]     ok 9 - my-port matches bound-port
  [Net::BGP]     ok 10 - Peer family is AF_INET
  [Net::BGP]     ok 11 - Connected to localhost
  [Net::BGP]     ok 12 - Socket is UInt
  [Net::BGP]     ok 13 - Socket is defined
  [Net::BGP]     ok 14 - Read line 1
  [Net::BGP]     ok 15 - Read line 2
  [Net::BGP]     ok 16 - Read line 3
  [Net::BGP]     ok 17 - Read line 4
  [Net::BGP]     ok 18 - Read line 5
  [Net::BGP]     ok 19 - Read line 6
  [Net::BGP]     ok 20 - Read line 7
  [Net::BGP]     1..20
  [Net::BGP] ok 1 - Basic Server
  [Net::BGP] # Subtest: Client/Server
  [Net::BGP] # Listening on port 43881
  [Net::BGP]     ok 1 - Listening socket closed
  [Net::BGP]     ok 2 - Read line 1
  [Net::BGP]     ok 3 - Read line 2
  [Net::BGP]     ok 4 - Connection 1 closed
  [Net::BGP]     ok 5 - Connection 2 closed
  [Net::BGP]     1..5
  [Net::BGP] ok 2 - Client/Server
  [Net::BGP] # Subtest: Client/Server - MD5 Non-Match
  [Net::BGP]     ok 1 - Listening socket closed
  [Net::BGP]     ok 2 - Read line 1
  [Net::BGP]     ok 3 - Connection 1 closed
  [Net::BGP]     ok 4 - Connection 2 closed
  [Net::BGP]     1..4
  [Net::BGP] ok 3 - Client/Server - MD5 Non-Match
  [Net::BGP] # Subtest: Client/Server - MD5 Match
  [Net::BGP]     ok 1 - Listening socket closed
  [Net::BGP]     ok 2 - Read line 1
  [Net::BGP]     ok 3 - Connection 1 closed
  [Net::BGP]     ok 4 - Connection 2 closed
  [Net::BGP]     1..4
  [Net::BGP] ok 4 - Client/Server - MD5 Match
  [Net::BGP] 1..4
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/11-socket.t
  [Net::BGP] # Subtest: Basic Server - Native OS
  [Net::BGP]     ok 1 - sock is defined
  [Net::BGP]     ok 2 - connections is a Supply
  [Net::BGP]     ok 3 - bound port promise is kept
  [Net::BGP]     ok 4 - bound port does not die
  [Net::BGP]     ok 5 - bound port in proper range
  [Net::BGP] # Listening on port 41801
  [Net::BGP]     ok 6 - conn is defined
  [Net::BGP]     ok 7 - socket-host matches
  [Net::BGP]     ok 8 - socket-port matches socket-port
  [Net::BGP]     ok 9 - Connected to localhost
  [Net::BGP]     ok 10 - Read line 1
  [Net::BGP]     ok 11 - Read line 2
  [Net::BGP]     ok 12 - Read line 3
  [Net::BGP]     ok 13 - Read line 4
  [Net::BGP]     1..13
  [Net::BGP] ok 1 - Basic Server - Native OS
  [Net::BGP] # Subtest: Basic Server - Fallback
  [Net::BGP]     ok 1 - sock is defined
  [Net::BGP]     ok 2 - connections is a Supply
  [Net::BGP]     ok 3 - bound port promise is kept
  [Net::BGP]     ok 4 - bound port does not die
  [Net::BGP]     ok 5 - bound port in proper range
  [Net::BGP] # Listening on port 39783
  [Net::BGP]     ok 6 - conn is defined
  [Net::BGP]     ok 7 - socket-host matches
  [Net::BGP]     ok 8 - socket-port matches socket-port
  [Net::BGP]     ok 9 - Connected to localhost
  [Net::BGP]     ok 10 - Read line 1
  [Net::BGP]     ok 11 - Read line 2
  [Net::BGP]     ok 12 - Read line 3
  [Net::BGP]     ok 13 - Read line 4
  [Net::BGP]     1..13
  [Net::BGP] ok 2 - Basic Server - Fallback
  [Net::BGP] 1..2
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/30-basic.t
  [Net::BGP] # Subtest: Basic Class Construction
  [Net::BGP]     ok 1 - Created BGP Class
  [Net::BGP]     ok 2 - Port has proper default
  [Net::BGP]     ok 3 - Port is properly set to 1179
  [Net::BGP]     ok 4 - Port is properly set to 179 by Nil
  [Net::BGP]     ok 5 - Cannot change port
  [Net::BGP]     ok 6 - < 0 port rejected
  [Net::BGP]     ok 7 - >65535 port rejected
  [Net::BGP]     ok 8 - >65535 identifier rejected
  [Net::BGP]     ok 9 - Non-existent attribute causes failure
  [Net::BGP]     ok 10 - Must provide my-asn
  [Net::BGP]     ok 11 - Invalid ASN dies
  [Net::BGP]     1..11
  [Net::BGP] ok 1 - Basic Class Construction
  [Net::BGP] # Subtest: Listener
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     1..2
  [Net::BGP] ok 2 - Listener
  [Net::BGP] 1..2
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/31-conn-open-close-event.t
  [Net::BGP] # Subtest: Event
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - Message type is as expected
  [Net::BGP]     ok 4 - Client IP is as expected
  [Net::BGP]     ok 5 - Client port is as expected
  [Net::BGP]     ok 6 - Close message type is as expected
  [Net::BGP]     ok 7 - Close client IP is as expected
  [Net::BGP]     ok 8 - Close client port is as expected
  [Net::BGP]     1..8
  [Net::BGP] ok 1 - Event
  [Net::BGP] 1..1
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/32-Command-Dead-Child.t
  [Net::BGP] ok 1 - Created Net::BGP::Command::Dead-Child Class
  [Net::BGP] ok 2 - Proper Dead-Child command
  [Net::BGP] ok 3 - Payload is correct
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/50-messages.t
  [Net::BGP] # Subtest: Command
  [Net::BGP]     # Subtest: Parent Class
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Message type has proper default
  [Net::BGP]         1..2
  [Net::BGP]     ok 1 - Parent Class
  [Net::BGP]     # Subtest: BGP-Message
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Proper BGP-Message message
  [Net::BGP]         ok 3 - Payload is correct
  [Net::BGP]         1..3
  [Net::BGP]     ok 2 - BGP-Message
  [Net::BGP]     # Subtest: Stop
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Proper Stop message
  [Net::BGP]         1..2
  [Net::BGP]     ok 3 - Stop
  [Net::BGP]     1..3
  [Net::BGP] ok 1 - Command
  [Net::BGP] # Subtest: Event
  [Net::BGP]     # Subtest: Parent Class
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Connection ID is proper
  [Net::BGP]         ok 3 - Message type has proper default
  [Net::BGP]         ok 4 - Message is not an error
  [Net::BGP]         ok 5 - Date time appears correct
  [Net::BGP]         1..5
  [Net::BGP]     ok 1 - Parent Class
  [Net::BGP]     # Subtest: BGP-Message-No-Opt
  [Net::BGP]         ok 1 - Created Event Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is not an error
  [Net::BGP]         ok 5 - BGP message type is correct
  [Net::BGP]         ok 6 - BGP message code is correct
  [Net::BGP]         ok 7 - Proper number of parameter elements
  [Net::BGP]         ok 8 - Date time appears correct
  [Net::BGP]         ok 9 - Peer ASN is proper
  [Net::BGP]         1..9
  [Net::BGP]     ok 2 - BGP-Message-No-Opt
  [Net::BGP]     # Subtest: BGP-Message-With-Opt
  [Net::BGP]         ok 1 - Created Event Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is not an error
  [Net::BGP]         ok 5 - BGP message type is correct
  [Net::BGP]         ok 6 - BGP message code is correct
  [Net::BGP]         ok 7 - Date time appears correct
  [Net::BGP]         ok 8 - Proper number of parameter elements
  [Net::BGP]         ok 9 - 240 Proper parameter-code
  [Net::BGP]         ok 10 - 240 Proper parameter-name
  [Net::BGP]         ok 11 - 240 Proper parameter-length
  [Net::BGP]         ok 12 - 240 Proper parameter-value length
  [Net::BGP]         ok 13 - 241 Proper parameter-code
  [Net::BGP]         ok 14 - 241 Proper parameter-name
  [Net::BGP]         ok 15 - 241 Proper parameter-length
  [Net::BGP]         ok 16 - 241 Proper parameter-value length
  [Net::BGP]         ok 17 - 241 Proper parameter-value
  [Net::BGP]         1..17
  [Net::BGP]     ok 3 - BGP-Message-With-Opt
  [Net::BGP]     # Subtest: Closed-Connection
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Proper Closed-Connection message
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Client IP address
  [Net::BGP]         ok 5 - Client IP port
  [Net::BGP]         ok 6 - Message is not an error
  [Net::BGP]         1..6
  [Net::BGP]     ok 4 - Closed-Connection
  [Net::BGP]     # Subtest: New-Connection
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Proper New-Connection message
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Client IP address
  [Net::BGP]         ok 5 - Client IP port
  [Net::BGP]         ok 6 - Message is not an error
  [Net::BGP]         1..6
  [Net::BGP]     ok 5 - New-Connection
  [Net::BGP]     1..5
  [Net::BGP] ok 2 - Event
  [Net::BGP] # Subtest: Error
  [Net::BGP]     # Subtest: Parent Class
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Message is an error
  [Net::BGP]         ok 4 - Human readable type
  [Net::BGP]         1..4
  [Net::BGP]     ok 1 - Parent Class
  [Net::BGP]     # Subtest: Bad-Option-Length
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         ok 6 - Length is valid
  [Net::BGP]         1..6
  [Net::BGP]     ok 2 - Bad-Option-Length
  [Net::BGP]     # Subtest: Bad-Parameter-Length
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         ok 6 - Length is valid
  [Net::BGP]         1..6
  [Net::BGP]     ok 3 - Bad-Parameter-Length
  [Net::BGP]     # Subtest: Hold-Time-Too-Short
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         ok 6 - Hold-Time is valid
  [Net::BGP]         1..6
  [Net::BGP]     ok 4 - Hold-Time-Too-Short
  [Net::BGP]     # Subtest: Length-Too-Short
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         ok 6 - Length is valid
  [Net::BGP]         1..6
  [Net::BGP]     ok 5 - Length-Too-Short
  [Net::BGP]     # Subtest: Marker-Format
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         1..5
  [Net::BGP]     ok 6 - Marker-Format
  [Net::BGP]     # Subtest: Unknown-Version
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         ok 6 - Version is valid
  [Net::BGP]         1..6
  [Net::BGP]     ok 7 - Unknown-Version
  [Net::BGP]     1..7
  [Net::BGP] ok 3 - Error
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/51-bgp-messages-from-hash.t
  [Net::BGP] # Subtest: Open Message
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - BGP version is correct
  [Net::BGP]     ok 5 - ASN is correct
  [Net::BGP]     ok 6 - Hold time is correct
  [Net::BGP]     ok 7 - BGP identifier is correct
  [Net::BGP]     ok 8 - Supports IPv4
  [Net::BGP]     ok 9 - Supports IPv6
  [Net::BGP]     ok 10 - FH BGP message is defined
  [Net::BGP]     ok 11 - FH Message type is correct
  [Net::BGP]     ok 12 - FH Message code is correct
  [Net::BGP]     ok 13 - BGP version is correct
  [Net::BGP]     ok 14 - FH ASN is correct
  [Net::BGP]     ok 15 - FH Hold time is correct
  [Net::BGP]     ok 16 - FH BGP identifier is correct
  [Net::BGP]     ok 17 - Message value correct
  [Net::BGP]     ok 18 - can create with IP ID
  [Net::BGP]     ok 19 - can create with Int Message Code
  [Net::BGP]     ok 20 - can create with Message Type
  [Net::BGP]     ok 21 - can create with Message Typeand int Code
  [Net::BGP]     ok 22 - can create with Message Type and Code
  [Net::BGP]     1..22
  [Net::BGP] ok 1 - Open Message
  [Net::BGP] # Subtest: Keep-Alive Message
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - FH BGP message is defined
  [Net::BGP]     ok 5 - FH Message type is correct
  [Net::BGP]     ok 6 - FH Message code is correct
  [Net::BGP]     ok 7 - Message value correct
  [Net::BGP]     1..7
  [Net::BGP] ok 2 - Keep-Alive Message
  [Net::BGP] # Subtest: Update-ASN16
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - FH BGP message is defined
  [Net::BGP]     ok 5 - FH Message type is correct
  [Net::BGP]     ok 6 - FH Message code is correct
  [Net::BGP]     ok 7 - Message value correct
  [Net::BGP]     1..7
  [Net::BGP] ok 3 - Update-ASN16
  [Net::BGP] # Subtest: Update-Withdrawal-Only-ASN16
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - FH BGP message is defined
  [Net::BGP]     ok 5 - FH Message type is correct
  [Net::BGP]     ok 6 - FH Message code is correct
  [Net::BGP]     ok 7 - Message value correct
  [Net::BGP]     1..7
  [Net::BGP] ok 4 - Update-Withdrawal-Only-ASN16
  [Net::BGP] # Subtest: Update-MP
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - FH BGP message is defined
  [Net::BGP]     ok 5 - FH Message type is correct
  [Net::BGP]     ok 6 - FH Message code is correct
  [Net::BGP]     ok 7 - Message value correct
  [Net::BGP]     1..7
  [Net::BGP] ok 5 - Update-MP
  [Net::BGP] 1..5
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/52-bgp-messages-raw.t
  [Net::BGP] # Subtest: Generic
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - Message value correct
  [Net::BGP]     1..4
  [Net::BGP] ok 1 - Generic
  [Net::BGP] # Subtest: Open Message
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - BGP version is correct
  [Net::BGP]     ok 5 - ASN is correct
  [Net::BGP]     ok 6 - Hold time is correct
  [Net::BGP]     ok 7 - BGP identifier is correct
  [Net::BGP]     ok 8 - Message value correct
  [Net::BGP]     1..8
  [Net::BGP] ok 2 - Open Message
  [Net::BGP] # Subtest: Open Message w/ Capabilities
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - BGP version is correct
  [Net::BGP]     ok 5 - ASN is correct
  [Net::BGP]     ok 6 - Hold time is correct
  [Net::BGP]     ok 7 - BGP identifier is correct
  [Net::BGP]     ok 8 - IPv4 Support
  [Net::BGP]     ok 9 - IPv6 Support
  [Net::BGP]     ok 10 - Proper number of Parameters
  [Net::BGP]     ok 11 - Parameter is a Capabilitiy
  [Net::BGP]     ok 12 - Parameter has proper code
  [Net::BGP]     ok 13 - Parameter has proper name
  [Net::BGP]     ok 14 - Proper number of capabilities
  [Net::BGP]     ok 15 - Capability¹ is proper type
  [Net::BGP]     ok 16 - Capability¹ has proper code
  [Net::BGP]     ok 17 - Capability¹ has proper name
  [Net::BGP]     ok 18 - Capability² is proper type
  [Net::BGP]     ok 19 - Capability² has proper code
  [Net::BGP]     ok 20 - Capability² has proper name
  [Net::BGP]     ok 21 - Capability² has proper asn
  [Net::BGP]     ok 22 - Capability³ is proper type
  [Net::BGP]     ok 23 - Capability³ has proper code
  [Net::BGP]     ok 24 - Capability³ has proper name
  [Net::BGP]     ok 25 - Capability³ has proper afi
  [Net::BGP]     ok 26 - Capability³ has proper safi
  [Net::BGP]     ok 27 - Capability³ has proper reserved
  [Net::BGP]     ok 28 - Capability⁴ is proper type
  [Net::BGP]     ok 29 - Capability⁴ has proper code
  [Net::BGP]     ok 30 - Capability⁴ has proper name
  [Net::BGP]     ok 31 - Capability⁴ has proper afi
  [Net::BGP]     ok 32 - Capability⁴ has proper safi
  [Net::BGP]     ok 33 - Capability⁴ has proper reserved
  [Net::BGP]     ok 34 - Capability⁵ is proper type
  [Net::BGP]     ok 35 - Capability⁵ has proper code
  [Net::BGP]     ok 36 - Capability⁵ has proper name
  [Net::BGP]     ok 37 - Capability⁵ has proper restart
  [Net::BGP]     ok 38 - Capability⁵ has proper reserved
  [Net::BGP]     ok 39 - Capability⁵ has proper flags
  [Net::BGP]     ok 40 - Capability⁵ has proper restart-time
  [Net::BGP]     ok 41 - Capability⁵ has proper num of per-af
  [Net::BGP]     ok 42 - Capability⁵ has proper per-af AFI
  [Net::BGP]     ok 43 - Capability⁵ has proper per-af SAFI
  [Net::BGP]     ok 44 - Capability⁵ has proper per-af AFI Name
  [Net::BGP]     ok 45 - Capability⁵ has proper per-af SAFI Name
  [Net::BGP]     ok 46 - Capability⁵ has proper per-af Flags
  [Net::BGP]     ok 47 - Capability⁶ is proper type
  [Net::BGP]     ok 48 - Capability⁶ has proper code
  [Net::BGP]     ok 49 - Capability⁶ has proper name
  [Net::BGP]     ok 50 - Capability⁶ has proper hostname
  [Net::BGP]     ok 51 - Capability⁶ has proper domain
  [Net::BGP]     ok 52 - Message value correct
  [Net::BGP]     1..52
  [Net::BGP] ok 3 - Open Message w/ Capabilities
  [Net::BGP] # Subtest: Keep-Alive Message
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - Message value correct
  [Net::BGP]     1..4
  [Net::BGP] ok 4 - Keep-Alive Message
  [Net::BGP] # Subtest: Update Message (ASN16)
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - BGP message is proper type
  [Net::BGP]     ok 3 - Message type is correct
  [Net::BGP]     ok 4 - Message code is correct
  [Net::BGP]     ok 5 - Proper number of withdrawn prefixes
  [Net::BGP]     ok 6 - Withdrawn 1 correct
  [Net::BGP]     ok 7 - Withdrawn 2 correct
  [Net::BGP]     ok 8 - Withdrawn 3 correct
  [Net::BGP]     ok 9 - Proper number of path elements
  [Net::BGP]     ok 10 - Path Attribute 1 Proper Type
  [Net::BGP]     ok 11 - Path Attribute 1 Proper Value
  [Net::BGP]     ok 12 - Origin is valid
  [Net::BGP]     ok 13 - Path Attribute 2 Proper Type
  [Net::BGP]     ok 14 - Path Attribute 2 Proper Value
  [Net::BGP]     ok 15 - as-path is valid
  [Net::BGP]     ok 16 - path is valid
  [Net::BGP]     ok 17 - Path Attribute 3 Proper Type
  [Net::BGP]     ok 18 - Path Attribute 3 Proper Value
  [Net::BGP]     ok 19 - next-hop is valid
  [Net::BGP]     ok 20 - Path Attribute 4 Proper Type
  [Net::BGP]     ok 21 - Path Attribute 4 Proper Value
  [Net::BGP]     ok 22 - Path Attribute 5 Proper Type
  [Net::BGP]     ok 23 - Path Attribute 5 Proper Value
  [Net::BGP]     ok 24 - Path Attribute 6 Proper Type
  [Net::BGP]     ok 25 - Atomic Attribute is present
  [Net::BGP]     ok 26 - Path Attribute 7 Proper Type
  [Net::BGP]     ok 27 - Aggregator ASN correct
  [Net::BGP]     ok 28 - Aggregator IP correct
  [Net::BGP]     ok 29 - Path Attribute 8 Proper Type
  [Net::BGP]     ok 30 - Path Attribute 7 Proper Value
  [Net::BGP]     ok 31 - Communities are proper
  [Net::BGP]     ok 32 - Path Attribute 9 Proper Type
  [Net::BGP]     ok 33 - Path Attribute 9 Proper Value
  [Net::BGP]     ok 34 - Path Attribute 10 Proper Type
  [Net::BGP]     ok 35 - Path Attribute 10 Proper Value
  [Net::BGP]     ok 36 - Path Attribute 10 Proper Type
  [Net::BGP]     ok 37 - Path Attribute 10 Proper Value
  [Net::BGP]     ok 38 - Extended Communities are proper
  [Net::BGP]     ok 39 - Path Attribute 11 Proper Type
  [Net::BGP]     ok 40 - AS4-Aggregator ASN correct
  [Net::BGP]     ok 41 - AS4-Aggregator IP correct
  [Net::BGP]     ok 42 - Path Attribute 12 Proper Type
  [Net::BGP]     ok 43 - Path Attribute 12 Proper Value
  [Net::BGP]     ok 44 - Long Communities are proper
  [Net::BGP]     ok 45 - Proper number of NLRI prefixes
  [Net::BGP]     ok 46 - NLRI 1 correct
  [Net::BGP]     ok 47 - NLRI 1 correct
  [Net::BGP]     ok 48 - NLRI 1 correct
  [Net::BGP]     ok 49 - Message value correct
  [Net::BGP]     1..49
  [Net::BGP] ok 5 - Update Message (ASN16)
  [Net::BGP] # Subtest: Update Message Withdrawal Only (ASN16)
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - BGP message is proper type
  [Net::BGP]     ok 3 - Message type is correct
  [Net::BGP]     ok 4 - Message code is correct
  [Net::BGP]     ok 5 - Proper number of withdrawn prefixes
  [Net::BGP]     ok 6 - Withdrawn 1 correct
  [Net::BGP]     ok 7 - Withdrawn 2 correct
  [Net::BGP]     ok 8 - Withdrawn 3 correct
  [Net::BGP]     ok 9 - Proper number of path elements
  [Net::BGP]     ok 10 - Proper number of NLRI prefixes
  [Net::BGP]     ok 11 - Message value correct
  [Net::BGP]     1..11
  [Net::BGP] ok 6 - Update Message Withdrawal Only (ASN16)
  [Net::BGP] # Subtest: Update Message (MP-BGP)
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - BGP message is proper type
  [Net::BGP]     ok 3 - Message type is correct
  [Net::BGP]     ok 4 - Message code is correct
  [Net::BGP]     ok 5 - Proper number of withdrawn prefixes
  [Net::BGP]     ok 6 - Proper number of path elements
  [Net::BGP]     ok 7 - Path Attribute 1 Proper Type
  [Net::BGP]     ok 8 - Path Attribute 1 Proper Value
  [Net::BGP]     ok 9 - Path Attribute 2 Proper Type
  [Net::BGP]     ok 10 - Path Attribute 2 Proper Value
  [Net::BGP]     ok 11 - AS Path has proper length
  [Net::BGP]     ok 12 - Path Attribute 3 Proper Type
  [Net::BGP]     ok 13 - Path Attribute 3A Proper Value
  [Net::BGP]     ok 14 - Path Attribute 3B Proper Value
  [Net::BGP]     ok 15 - Path Attribute 3C Proper Value
  [Net::BGP]     ok 16 - Path Attribute 3D Proper Value
  [Net::BGP]     ok 17 - Path Attribute 3E Proper Value
  [Net::BGP]     ok 18 - Path Attribute 3F Proper Value
  [Net::BGP]     ok 19 - Path Attribute 4 Proper Type
  [Net::BGP]     ok 20 - Path Attribute 4A Proper Value
  [Net::BGP]     ok 21 - Path Attribute 4B Proper Value
  [Net::BGP]     ok 22 - Path Attribute 4E Proper Value
  [Net::BGP]     ok 23 - Path Attribute 4F Proper Value
  [Net::BGP]     ok 24 - Proper number of NLRI prefixes
  [Net::BGP]     ok 25 - Message value correct
  [Net::BGP]     1..25
  [Net::BGP] ok 7 - Update Message (MP-BGP)
  [Net::BGP] 1..7
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/53-Open-With-Multiple-CapOpts.t
  [Net::BGP] ok 1 - BGP message is defined
  [Net::BGP] ok 2 - Message type is correct
  [Net::BGP] ok 3 - Message code is correct
  [Net::BGP] ok 4 - BGP version is correct
  [Net::BGP] ok 5 - ASN is correct
  [Net::BGP] ok 6 - Hold time is correct
  [Net::BGP] ok 7 - BGP identifier is correct
  [Net::BGP] ok 8 - Proper number of Parameters
  [Net::BGP] ok 9 - Parameter¹ is a Capabilitiy
  [Net::BGP] ok 10 - Parameter¹ has proper code
  [Net::BGP] ok 11 - Parameter¹ has proper name
  [Net::BGP] ok 12 - Parameter² is a Capabilitiy
  [Net::BGP] ok 13 - Parameter² has proper code
  [Net::BGP] ok 14 - Parameter² has proper name
  [Net::BGP] ok 15 - Parameter³ is a Capabilitiy
  [Net::BGP] ok 16 - Parameter³ has proper code
  [Net::BGP] ok 17 - Parameter³ has proper name
  [Net::BGP] ok 18 - Parameter¹ Proper number of capabilities
  [Net::BGP] ok 19 - Capability¹ is proper type
  [Net::BGP] ok 20 - Capability¹ has proper code
  [Net::BGP] ok 21 - Capability¹ has proper name
  [Net::BGP] ok 22 - Parameter² Proper number of capabilities
  [Net::BGP] ok 23 - Capability² is proper type
  [Net::BGP] ok 24 - Capability² has proper code
  [Net::BGP] ok 25 - Capability² has proper name
  [Net::BGP] ok 26 - Capability² has proper asn
  [Net::BGP] ok 27 - Parameter³ Proper number of capabilities
  [Net::BGP] ok 28 - Capability³ is proper type
  [Net::BGP] ok 29 - Capability³ has proper code
  [Net::BGP] ok 30 - Capability³ has proper name
  [Net::BGP] ok 31 - Capability³ has proper afi
  [Net::BGP] ok 32 - Capability³ has proper safi
  [Net::BGP] ok 33 - Capability³ has proper reserved
  [Net::BGP] ok 34 - Message value correct
  [Net::BGP] 1..34
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/54-Update-Failure.t
  [Net::BGP] ok 1 - BGP message is defined
  [Net::BGP] ok 2 - Message type is correct
  [Net::BGP] ok 3 - Message code is correct
  [Net::BGP] ok 4 - NLRI right
  [Net::BGP] ok 5 - right number of path elems
  [Net::BGP] ok 6 - No NLRI6 Elements
  [Net::BGP] ok 7 - Aggregator ASN correct
  [Net::BGP] ok 8 - Aggregator IP correct
  [Net::BGP] 1..8
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/55-bgp-notification-raw.t
  [Net::BGP] # Subtest: Open Notification Unsupported Version
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - Error code is correct
  [Net::BGP]     ok 5 - Error name is correct
  [Net::BGP]     ok 6 - Error subtype is correct
  [Net::BGP]     ok 7 - Error subtype is correct
  [Net::BGP]     ok 8 - Class is correct
  [Net::BGP]     ok 9 - Version is correct
  [Net::BGP]     ok 10 - Message value correct
  [Net::BGP]     1..10
  [Net::BGP] ok 1 - Open Notification Unsupported Version
  [Net::BGP] # Subtest: Open Notification Bad Peer AS
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - Error code is correct
  [Net::BGP]     ok 5 - Error name is correct
  [Net::BGP]     ok 6 - Error subtype is correct
  [Net::BGP]     ok 7 - Error subtype is correct
  [Net::BGP]     ok 8 - Class is correct
  [Net::BGP]     ok 9 - Message value correct
  [Net::BGP]     1..9
  [Net::BGP] ok 2 - Open Notification Bad Peer AS
  [Net::BGP] # Subtest: Open Notification Unsupported Optional Parameter
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - Error code is correct
  [Net::BGP]     ok 5 - Error name is correct
  [Net::BGP]     ok 6 - Error subtype is correct
  [Net::BGP]     ok 7 - Error subtype is correct
  [Net::BGP]     ok 8 - Class is correct
  [Net::BGP]     ok 9 - Message value correct
  [Net::BGP]     1..9
  [Net::BGP] ok 3 - Open Notification Unsupported Optional Parameter
  [Net::BGP] # Subtest: Header Notification Connection not Syncronized
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - AAA
  [Net::BGP]     ok 3 - Message type is correct
  [Net::BGP]     ok 4 - Message code is correct
  [Net::BGP]     ok 5 - Error code is correct
  [Net::BGP]     ok 6 - Error name is correct
  [Net::BGP]     ok 7 - Error subtype is correct
  [Net::BGP]     ok 8 - Error subtype is correct
  [Net::BGP]     ok 9 - Class is correct
  [Net::BGP]     ok 10 - Message value correct
  [Net::BGP]     1..10
  [Net::BGP] ok 4 - Header Notification Connection not Syncronized
  [Net::BGP] # Subtest: Hold-Timer-Expired
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - raw matches message
  [Net::BGP]     ok 3 - Message type is correct
  [Net::BGP]     ok 4 - Message code is correct
  [Net::BGP]     ok 5 - Error code is correct
  [Net::BGP]     ok 6 - Error name is correct
  [Net::BGP]     ok 7 - Error subtype is correct
  [Net::BGP]     ok 8 - Error subtype is correct
  [Net::BGP]     ok 9 - Class is correct
  [Net::BGP]     ok 10 - Message value correct
  [Net::BGP]     1..10
  [Net::BGP] ok 5 - Hold-Timer-Expired
  [Net::BGP] 1..5
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/56-bgp-invalid-marker.t
  [Net::BGP] # Subtest: Syncronization
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Channel message type is as expected
  [Net::BGP]     ok 6 - Is not an error
  [Net::BGP]     ok 7 - Peer is defined
  [Net::BGP]     ok 8 - Peer is Idle
  [Net::BGP]     ok 9 - Close message type is as expected
  [Net::BGP]     ok 10 - Is not an error
  [Net::BGP]     ok 11 - Peer is idle
  [Net::BGP]     ok 12 - Message is proper type
  [Net::BGP]     1..12
  [Net::BGP] ok 1 - Syncronization
  [Net::BGP] 1..1
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/57-bgp-open-bad-asn.t
  [Net::BGP] # Subtest: OPEN
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Peer is defined
  [Net::BGP]     ok 6 - Peer is Idle
  [Net::BGP]     ok 7 - Close message type is as expected
  [Net::BGP]     ok 8 - Is not an error
  [Net::BGP]     ok 9 - Peer is idle
  [Net::BGP]     ok 10 - Message is proper type
  [Net::BGP]     1..10
  [Net::BGP] ok 1 - OPEN
  [Net::BGP] 1..1
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/58-as4-update.t
  [Net::BGP] # Subtest: Both AS4 and AS
  [Net::BGP]     ok 1 - FH BGP message is defined
  [Net::BGP]     ok 2 - AS Path is correct
  [Net::BGP]     ok 3 - AS Path members are correct
  [Net::BGP]     1..3
  [Net::BGP] ok 1 - Both AS4 and AS
  [Net::BGP] # Subtest: Only AS-Path on !ASN32
  [Net::BGP]     ok 1 - FH BGP message is defined
  [Net::BGP]     ok 2 - AS Path is correct
  [Net::BGP]     ok 3 - AS-Path attribute correct
  [Net::BGP]     ok 4 - AS4-Path attribute correct
  [Net::BGP]     1..4
  [Net::BGP] ok 2 - Only AS-Path on !ASN32
  [Net::BGP] # Subtest: Only AS-Path on ASN32
  [Net::BGP]     ok 1 - FH BGP message is defined
  [Net::BGP]     ok 2 - AS Path is correct
  [Net::BGP]     ok 3 - AS-Path attribute correct
  [Net::BGP]     ok 4 - AS4-Path attribute correct
  [Net::BGP]     1..4
  [Net::BGP] ok 3 - Only AS-Path on ASN32
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/60-Path-Attributes.t
  [Net::BGP] # Subtest: Extended-Community
  [Net::BGP]     ok 1 - Created Path Attribute
  [Net::BGP]     ok 2 - From Hash capability correct
  [Net::BGP]     ok 3 - From RAW capability correct
  [Net::BGP]     ok 4 - Route type is correct
  [Net::BGP]     1..4
  [Net::BGP] ok 1 - Extended-Community
  [Net::BGP] 1..1
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/70-peer-object.t
  [Net::BGP] # Subtest: eBGP
  [Net::BGP]     ok 1 - Created BGP Class
  [Net::BGP]     ok 2 - Peer IP is correct
  [Net::BGP]     ok 3 - Peer port is okay
  [Net::BGP]     ok 4 - Peer ASN is okay
  [Net::BGP]     ok 5 - My ASN is okay
  [Net::BGP]     ok 6 - Peer state is okay
  [Net::BGP]     ok 7 - ASN 32 support not indicated
  [Net::BGP]     ok 8 - Not iBGP
  [Net::BGP]     1..8
  [Net::BGP] ok 1 - eBGP
  [Net::BGP] # Subtest: iBGP
  [Net::BGP]     ok 1 - Created BGP Class
  [Net::BGP]     ok 2 - Peer IP is correct
  [Net::BGP]     ok 3 - Peer port is okay
  [Net::BGP]     ok 4 - Peer ASN is okay
  [Net::BGP]     ok 5 - My ASN is okay
  [Net::BGP]     ok 6 - Peer state is okay
  [Net::BGP]     ok 7 - ASN 32 supported
  [Net::BGP]     ok 8 - iBGP
  [Net::BGP]     1..8
  [Net::BGP] ok 2 - iBGP
  [Net::BGP] 1..2
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/80-Validator-Aggregation.t
  [Net::BGP] # Subtest: Good
  [Net::BGP]     ok 1 - No warnings in message
  [Net::BGP]     1..1
  [Net::BGP] ok 1 - Good
  [Net::BGP] # Subtest: AF_MIX
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 2 - AF_MIX
  [Net::BGP] # Subtest: Aggregator ASN
  [Net::BGP]     ok 1 - First message has AGGR_ASN_RESERVED
  [Net::BGP]     ok 2 - Second message has AGGR_ASN_PRIVATE
  [Net::BGP]     ok 3 - Third message has AGGR_ASN_TRANS
  [Net::BGP]     ok 4 - Forth message has MY-ASN
  [Net::BGP]     ok 5 - Fifth message has PEER-ASN
  [Net::BGP]     1..5
  [Net::BGP] ok 3 - Aggregator ASN
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/81-Validator-AS-Path.t
  [Net::BGP] # Subtest: Unexpected AS4 Path
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 1 - Unexpected AS4 Path
  [Net::BGP] # Subtest: Doc ASN
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 2 - Doc ASN
  [Net::BGP] # Subtest: PRIVATE ASN
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 3 - PRIVATE ASN
  [Net::BGP] # Subtest: Reserved ASN
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 4 - Reserved ASN
  [Net::BGP] # Subtest: Trans ASN
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 5 - Trans ASN
  [Net::BGP] 1..5
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/90-basic-bgp.t
  [Net::BGP] # Subtest: invalid-marker
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     1..6
  [Net::BGP] ok 1 - invalid-marker
  [Net::BGP] # Subtest: invalid-length-short
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     1..6
  [Net::BGP] ok 2 - invalid-length-short
  [Net::BGP] # Subtest: invalid-length-long
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     1..6
  [Net::BGP] ok 3 - invalid-length-long
  [Net::BGP] # Subtest: invalid-version
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     ok 7 - Message is proper type
  [Net::BGP]     ok 8 - Max supported version is valid
  [Net::BGP]     1..8
  [Net::BGP] ok 4 - invalid-version
  [Net::BGP] # Subtest: hold-time-too-short
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     1..6
  [Net::BGP] ok 5 - hold-time-too-short
  [Net::BGP] # Subtest: bad-option-length [1]
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     ok 7 - Length == 1
  [Net::BGP]     1..7
  [Net::BGP] ok 6 - bad-option-length [1]
  [Net::BGP] # Subtest: bad-option-length [3]
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     ok 7 - Length == 3
  [Net::BGP]     1..7
  [Net::BGP] ok 7 - bad-option-length [3]
  [Net::BGP] # Subtest: OPEN
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - BGP message type is as expected
  [Net::BGP]     ok 6 - Is not an error
  [Net::BGP]     ok 7 - BGP Message is proper name
  [Net::BGP]     ok 8 - BGP Message is proper type
  [Net::BGP]     ok 9 - Option length is zero
  [Net::BGP]     ok 10 - Option bytes = len
  [Net::BGP]     ok 11 - Peer ASN is proper
  [Net::BGP]     ok 12 - Peer is defined
  [Net::BGP]     ok 13 - Peer is OpenConfirm
  [Net::BGP]     ok 14 - Connection does not support ASN32
  [Net::BGP]     ok 15 - One AF present
  [Net::BGP]     ok 16 - AFI correct
  [Net::BGP]     ok 17 - SAFI correct
  [Net::BGP]     ok 18 - Message is proper type
  [Net::BGP]     ok 19 - Version correct
  [Net::BGP]     ok 20 - ASN is correct
  [Net::BGP]     ok 21 - Hold-Time is correct
  [Net::BGP]     ok 22 - Identifier is correct
  [Net::BGP]     ok 23 - Option length is correct
  [Net::BGP]     ok 24 - No parameters provided
  [Net::BGP]     ok 25 - Close message type is as expected
  [Net::BGP]     ok 26 - Is not an error
  [Net::BGP]     ok 27 - Peer is idle
  [Net::BGP]     1..27
  [Net::BGP] ok 8 - OPEN
  [Net::BGP] 1..8
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/91-send-update.t
  [Net::BGP] ok 1 - BGP Port is 0
  [Net::BGP] ok 2 - BGP Port isnt 0
  [Net::BGP] ok 3 - ASN is correct
  [Net::BGP] ok 4 - Message type is as expected
  [Net::BGP] ok 5 - BGP message type is as expected
  [Net::BGP] ok 6 - Is not an error
  [Net::BGP] ok 7 - BGP Message is proper name
  [Net::BGP] ok 8 - Message is proper type
  [Net::BGP] ok 9 - No parameters provided
  [Net::BGP] ok 10 - Keep-Alive received
  [Net::BGP] ok 11 - UD is proper name
  [Net::BGP] ok 12 - UD NLRI correct
  [Net::BGP] ok 13 - UD next-hop correct
  [Net::BGP] ok 14 - UD path correct
  [Net::BGP] ok 15 - Close message type is as expected
  [Net::BGP] ok 16 - Is not an error
  [Net::BGP] ok 17 - Peer is idle
  [Net::BGP] 1..17
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/95-bgpmon.t
  [Net::BGP] ok 1 - Speaker object defined
  [Net::BGP] ok 2 - BGP defined
  [Net::BGP] ok 3 - Display object defined
  [Net::BGP] ok 4 - Proper listen-host
  [Net::BGP] ok 5 - Proper listen-port
  [Net::BGP] ok 6 - Proper my-asn
  [Net::BGP] ok 7 - proper my-domain
  [Net::BGP] ok 8 - proper my-hostname
  [Net::BGP] ok 9 - Proper wanted CIDR (1)
  [Net::BGP] ok 10 - Proper wanted ASN (1)
  [Net::BGP] ok 11 - Proper wanted CIDR (2)
  [Net::BGP] ok 12 - Proper wanted ASN (2)
  [Net::BGP] ok 13 - Not colored (1)
  [Net::BGP] ok 14 - Not colored (2)
  [Net::BGP] ok 15 - Yes colored (1)
  [Net::BGP] ok 16 - Yes colored (2)
  [Net::BGP] ok 17 - BGP Port is 0
  [Net::BGP] ok 18 - BGP Port isnt 0
  [Net::BGP] ok 19 - ASN is correct
  [Net::BGP] ok 20 - Message type is as expected
  [Net::BGP] ok 21 - BGP message type is as expected
  [Net::BGP] ok 22 - Is not an error
  [Net::BGP] ok 23 - BGP Message is proper name
  [Net::BGP] ok 24 - Message is proper type
  [Net::BGP] ok 25 - No parameters provided
  [Net::BGP] ok 26 - Keep-Alive received
  [Net::BGP] ok 27 - UD is proper name
  [Net::BGP] ok 28 - UD NLRI correct
  [Net::BGP] ok 29 - UD next-hop correct
  [Net::BGP] ok 30 - UD path correct
  [Net::BGP] ok 31 - Close message type is as expected
  [Net::BGP] ok 32 - Is not an error
  [Net::BGP] ok 33 - Peer is idle
  [Net::BGP] 1..33
  ===> Testing [OK] for Net::BGP:ver<0.9.0>:auth<zef:jmaslak>
  ===> Installing: Net::BGP:ver<0.9.0>:auth<zef:jmaslak>
  ===> Install [OK] for Net::BGP:ver<0.9.0>:auth<zef:jmaslak>

  2 bin/ scripts [bgpmon.rakudoc bgpmon.p6] installed to:
  /tmp/vcBPA2bk7Y/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 12min 18.220s
               CPU time consumed: 10min 39.393s
                     Memory peak: 2G (swap: 945.4M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3121634-i3098159.service; invocation ID: 238cf2e98a864daeb3c4b550df5474dc
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Net::BGP
  ===> Found: Net::BGP:ver<0.9.0>:auth<zef:jmaslak> [via Zef::Repository::Ecosystems<fez>]
  [Net::BGP] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786851742.3121643.9454.66628616852/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz https://360.zef.pm/N/ET/NET_BGP/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  ===> Fetching [OK]: Net::BGP:ver<0.9.0>:auth<zef:jmaslak> to /home/coke/sandbox/blin/data/zef-data/tmp/1786851742.3121643.9454.66628616852/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  [Net::BGP] Command: tar -t -f ./b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  [Net::BGP] Command: tar -xvf ./b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz -C ../b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  ===> Extraction [OK]: Net::BGP to /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  ===> Testing: Net::BGP:ver<0.9.0>:auth<zef:jmaslak>
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/00-conversions.t
  [Net::BGP] # Subtest: nuint16
  [Net::BGP]     ok 1 - 
  [Net::BGP]     ok 2 - 
  [Net::BGP]     ok 3 - 
  [Net::BGP]     ok 4 - 
  [Net::BGP]     ok 5 - 
  [Net::BGP]     ok 6 - 
  [Net::BGP]     ok 7 - 
  [Net::BGP]     ok 8 - 
  [Net::BGP]     ok 9 - 
  [Net::BGP]     ok 10 - 
  [Net::BGP]     ok 11 - 
  [Net::BGP]     ok 12 - 
  [Net::BGP]     ok 13 - 
  [Net::BGP]     ok 14 - 
  [Net::BGP]     ok 15 - 
  [Net::BGP]     ok 16 - 
  [Net::BGP]     ok 17 - 258 is encoded properly
  [Net::BGP]     1..17
  [Net::BGP] ok 1 - nuint16
  [Net::BGP] # Subtest: nunit32
  [Net::BGP]     ok 1 - 
  [Net::BGP]     ok 2 - 
  [Net::BGP]     ok 3 - 
  [Net::BGP]     ok 4 - 
  [Net::BGP]     ok 5 - 
  [Net::BGP]     ok 6 - 
  [Net::BGP]     ok 7 - 
  [Net::BGP]     ok 8 - 
  [Net::BGP]     ok 9 - 
  [Net::BGP]     ok 10 - 
  [Net::BGP]     ok 11 - 
  [Net::BGP]     ok 12 - 
  [Net::BGP]     ok 13 - 
  [Net::BGP]     ok 14 - 
  [Net::BGP]     ok 15 - 
  [Net::BGP]     ok 16 - 
  [Net::BGP]     ok 17 - 
  [Net::BGP]     ok 18 - 
  [Net::BGP]     ok 19 - 
  [Net::BGP]     ok 20 - 
  [Net::BGP]     ok 21 - 
  [Net::BGP]     1..21
  [Net::BGP] ok 2 - nunit32
  [Net::BGP] # Subtest: nunit128
  [Net::BGP]     ok 1 - 
  [Net::BGP]     ok 2 - 
  [Net::BGP]     ok 3 - 
  [Net::BGP]     ok 4 - 
  [Net::BGP]     ok 5 - 
  [Net::BGP]     ok 6 - 
  [Net::BGP]     ok 7 - 
  [Net::BGP]     ok 8 - 
  [Net::BGP]     ok 9 - 
  [Net::BGP]     ok 10 - 
  [Net::BGP]     ok 11 - 
  [Net::BGP]     1..11
  [Net::BGP] ok 3 - nunit128
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/01-ip-test.t
  [Net::BGP] ok 1 - 1.2.3.4 ipv4-to-int
  [Net::BGP] ok 2 - 1.2.3.4 int-to-ipv4
  [Net::BGP] ok 3 - 1.2.3.4 ipv4-to-int-to-ipv4
  [Net::BGP] ok 4 - 1.2.3.4 int-to-ipv4-to-int
  [Net::BGP] ok 5 - 1.2.3.4 ipv4-to-buf8
  [Net::BGP] ok 6 - 1.2.3.4 ip-valid
  [Net::BGP] ok 7 - 2001:db8::1 ipv6-expand
  [Net::BGP] ok 8 - 2001:db8::1 ipv6-expand (full)
  [Net::BGP] ok 9 - 2001:db8::1 ipv6-to-int
  [Net::BGP] ok 10 - 2001:db8::1 ipv6-compact
  [Net::BGP] ok 11 - 2001:db8::1 int-to-ipv6
  [Net::BGP] ok 12 - 2001:db8::1 ip-valid
  [Net::BGP] ok 13 - 2001:db8::1 ipv6-to-buf-length
  [Net::BGP] ok 14 - 2001:db8::1 0 ipv6-to-buf8
  [Net::BGP] ok 15 - 2001:db8::1 1 ipv6-to-buf8
  [Net::BGP] ok 16 - 2001:db8::1 2 ipv6-to-buf8
  [Net::BGP] ok 17 - 2001:db8::1 3 ipv6-to-buf8
  [Net::BGP] ok 18 - 2001:db8::1 4 ipv6-to-buf8
  [Net::BGP] ok 19 - 2001:db8::1 5 ipv6-to-buf8
  [Net::BGP] ok 20 - 2001:db8::1 6 ipv6-to-buf8
  [Net::BGP] ok 21 - 2001:db8::1 7 ipv6-to-buf8
  [Net::BGP] ok 22 - 2001:db8::1 8 ipv6-to-buf8
  [Net::BGP] ok 23 - 2001:db8::1 9 ipv6-to-buf8
  [Net::BGP] ok 24 - 2001:db8::1 10 ipv6-to-buf8
  [Net::BGP] ok 25 - 2001:db8::1 11 ipv6-to-buf8
  [Net::BGP] ok 26 - 2001:db8::1 12 ipv6-to-buf8
  [Net::BGP] ok 27 - 2001:db8::1 13 ipv6-to-buf8
  [Net::BGP] ok 28 - 2001:db8::1 14 ipv6-to-buf8
  [Net::BGP] ok 29 - 2001:db8::1 15 ipv6-to-buf8
  [Net::BGP] ok 30 - 2001:db8::1 buf8-to-ipv6
  [Net::BGP] ok 31 - 2001:db8::1/0 ipv6-to-buf-length
  [Net::BGP] ok 32 - 2001:db8::1/0 buf8-to-ipv6
  [Net::BGP] ok 33 - 2001:db8::1/64 buf8-to-ipv6
  [Net::BGP] ok 34 - 2001:db8::1/127 ipv6-to-buf-length
  [Net::BGP] ok 35 - 2001:db8::1/127 0 ipv6-to-buf8
  [Net::BGP] ok 36 - 2001:db8::1/127 1 ipv6-to-buf8
  [Net::BGP] ok 37 - 2001:db8::1/127 2 ipv6-to-buf8
  [Net::BGP] ok 38 - 2001:db8::1/127 3 ipv6-to-buf8
  [Net::BGP] ok 39 - 2001:db8::1/127 4 ipv6-to-buf8
  [Net::BGP] ok 40 - 2001:db8::1/127 5 ipv6-to-buf8
  [Net::BGP] ok 41 - 2001:db8::1/127 6 ipv6-to-buf8
  [Net::BGP] ok 42 - 2001:db8::1/127 7 ipv6-to-buf8
  [Net::BGP] ok 43 - 2001:db8::1/127 8 ipv6-to-buf8
  [Net::BGP] ok 44 - 2001:db8::1/127 9 ipv6-to-buf8
  [Net::BGP] ok 45 - 2001:db8::1/127 10 ipv6-to-buf8
  [Net::BGP] ok 46 - 2001:db8::1/127 11 ipv6-to-buf8
  [Net::BGP] ok 47 - 2001:db8::1/127 12 ipv6-to-buf8
  [Net::BGP] ok 48 - 2001:db8::1/127 13 ipv6-to-buf8
  [Net::BGP] ok 49 - 2001:db8::1/127 14 ipv6-to-buf8
  [Net::BGP] ok 50 - 2001:db8::1/127 15 ipv6-to-buf8
  [Net::BGP] ok 51 - 2001:db8::1/127 buf8-to-ipv6
  [Net::BGP] ok 52 - 2001:db8:0:2:3::1 ipv6-expand
  [Net::BGP] ok 53 - 2001:db8:0:2:3::1 ipv6-expand (full)
  [Net::BGP] ok 54 - 2001:db8:0:2:3::1 ipv6-to-int
  [Net::BGP] ok 55 - 2001:db8:0:2:3::1 ipv6-compact
  [Net::BGP] ok 56 - 2001:db8:0:2:3::1 int-to-ipv6
  [Net::BGP] ok 57 - 2001:db8:0:2:3::1 ip-valid
  [Net::BGP] ok 58 - 2001:db8:0:2:3::1 buf8-to-ipv6
  [Net::BGP] ok 59 - 2001:db8:0:2:3::1/0 ipv6-to-buf-length
  [Net::BGP] ok 60 - 2001:db8:0:2:3::1/0 buf8-to-ipv6
  [Net::BGP] ok 61 - 2001:db8:0:002:03::1 ipv6-expand
  [Net::BGP] ok 62 - 2001:db8:0:002:03::1 ipv6-expand (full)
  [Net::BGP] ok 63 - 2001:db8:0:002:03::1 ipv6-to-int
  [Net::BGP] ok 64 - 2001:db8:0:002:03::1 ipv6-compact
  [Net::BGP] ok 65 - 2001:db8:0:002:03::1 int-to-ipv6
  [Net::BGP] ok 66 - 2001:db8:0:002:03::1 ip-valid
  [Net::BGP] ok 67 - 2001:db8:0:002:03::1 buf8-to-ipv6
  [Net::BGP] ok 68 - 2001:db8:0:002:03::1/0 ipv6-to-buf-length
  [Net::BGP] ok 69 - 2001:db8:0:002:03::1/0 buf8-to-ipv6
  [Net::BGP] ok 70 - 2001:dB8:0:002:03::1 ipv6-expand
  [Net::BGP] ok 71 - 2001:dB8:0:002:03::1 ipv6-expand (full)
  [Net::BGP] ok 72 - 2001:dB8:0:002:03::1 ipv6-to-int
  [Net::BGP] ok 73 - 2001:dB8:0:002:03::1 ipv6-compact
  [Net::BGP] ok 74 - 2001:dB8:0:002:03::1 int-to-ipv6
  [Net::BGP] ok 75 - 2001:dB8:0:002:03::1 ip-valid
  [Net::BGP] ok 76 - 2001:dB8:0:002:03::1 buf8-to-ipv6
  [Net::BGP] ok 77 - 2001:dB8:0:002:03::1/0 ipv6-to-buf-length
  [Net::BGP] ok 78 - 2001:dB8:0:002:03::1/0 buf8-to-ipv6
  [Net::BGP] ok 79 - 2605:2700:0:3::4713:93e3 ipv6-expand
  [Net::BGP] ok 80 - 2605:2700:0:3::4713:93e3 ipv6-expand (full)
  [Net::BGP] ok 81 - 2605:2700:0:3::4713:93e3 ipv6-to-int
  [Net::BGP] ok 82 - 2605:2700:0:3::4713:93e3 ipv6-compact
  [Net::BGP] ok 83 - 2605:2700:0:3::4713:93e3 int-to-ipv6
  [Net::BGP] ok 84 - 2605:2700:0:3::4713:93e3 ip-valid
  [Net::BGP] ok 85 - 2605:2700:0:3::4713:93e3 buf8-to-ipv6
  [Net::BGP] ok 86 - 2605:2700:0:3::4713:93e3/0 ipv6-to-buf-length
  [Net::BGP] ok 87 - 2605:2700:0:3::4713:93e3/0 buf8-to-ipv6
  [Net::BGP] ok 88 - :: ipv6-expand
  [Net::BGP] ok 89 - :: ipv6-expand (full)
  [Net::BGP] ok 90 - :: ipv6-to-int
  [Net::BGP] ok 91 - :: ipv6-compact
  [Net::BGP] ok 92 - :: int-to-ipv6
  [Net::BGP] ok 93 - :: ip-valid
  [Net::BGP] ok 94 - :: ipv6-to-buf-length
  [Net::BGP] ok 95 - :: 0 ipv6-to-buf8
  [Net::BGP] ok 96 - :: 1 ipv6-to-buf8
  [Net::BGP] ok 97 - :: 2 ipv6-to-buf8
  [Net::BGP] ok 98 - :: 3 ipv6-to-buf8
  [Net::BGP] ok 99 - :: 4 ipv6-to-buf8
  [Net::BGP] ok 100 - :: 5 ipv6-to-buf8
  [Net::BGP] ok 101 - :: 6 ipv6-to-buf8
  [Net::BGP] ok 102 - :: 7 ipv6-to-buf8
  [Net::BGP] ok 103 - :: 8 ipv6-to-buf8
  [Net::BGP] ok 104 - :: 9 ipv6-to-buf8
  [Net::BGP] ok 105 - :: 10 ipv6-to-buf8
  [Net::BGP] ok 106 - :: 11 ipv6-to-buf8
  [Net::BGP] ok 107 - :: 12 ipv6-to-buf8
  [Net::BGP] ok 108 - :: 13 ipv6-to-buf8
  [Net::BGP] ok 109 - :: 14 ipv6-to-buf8
  [Net::BGP] ok 110 - :: 15 ipv6-to-buf8
  [Net::BGP] ok 111 - :: buf8-to-ipv6
  [Net::BGP] ok 112 - ::/0 ipv6-to-buf-length
  [Net::BGP] ok 113 - ::/0 buf8-to-ipv6
  [Net::BGP] ok 114 - ::/64 buf8-to-ipv6
  [Net::BGP] ok 115 - ::/127 ipv6-to-buf-length
  [Net::BGP] ok 116 - ::/127 0 ipv6-to-buf8
  [Net::BGP] ok 117 - ::/127 1 ipv6-to-buf8
  [Net::BGP] ok 118 - ::/127 2 ipv6-to-buf8
  [Net::BGP] ok 119 - ::/127 3 ipv6-to-buf8
  [Net::BGP] ok 120 - ::/127 4 ipv6-to-buf8
  [Net::BGP] ok 121 - ::/127 5 ipv6-to-buf8
  [Net::BGP] ok 122 - ::/127 6 ipv6-to-buf8
  [Net::BGP] ok 123 - ::/127 7 ipv6-to-buf8
  [Net::BGP] ok 124 - ::/127 8 ipv6-to-buf8
  [Net::BGP] ok 125 - ::/127 9 ipv6-to-buf8
  [Net::BGP] ok 126 - ::/127 10 ipv6-to-buf8
  [Net::BGP] ok 127 - ::/127 11 ipv6-to-buf8
  [Net::BGP] ok 128 - ::/127 12 ipv6-to-buf8
  [Net::BGP] ok 129 - ::/127 13 ipv6-to-buf8
  [Net::BGP] ok 130 - ::/127 14 ipv6-to-buf8
  [Net::BGP] ok 131 - ::/127 15 ipv6-to-buf8
  [Net::BGP] ok 132 - ::/127 buf8-to-ipv6
  [Net::BGP] ok 133 - 2001:db8::1 ip-cannonical
  [Net::BGP] ok 134 - 2001:db8::1 ip-cannonical²
  [Net::BGP] ok 135 - 2001:db8:0::0:1 ip-cannonical
  [Net::BGP] ok 136 - 2001:db8:0::0:1 ip-cannonical²
  [Net::BGP] ok 137 - ::ffff:192.0.2.1 ip-cannonical
  [Net::BGP] ok 138 - ::ffff:192.0.2.1 ip-cannonical²
  [Net::BGP] ok 139 - ::FFFF:192.0.2.1 ip-cannonical
  [Net::BGP] ok 140 - ::FFFF:192.0.2.1 ip-cannonical²
  [Net::BGP] ok 141 - 192.0.2.1 ip-cannonical
  [Net::BGP] ok 142 - 192.0.2.1 ip-cannonical²
  [Net::BGP] ok 143 - :: ip-cannonical
  [Net::BGP] ok 144 - :: ip-cannonical²
  [Net::BGP] ok 145 - 127.0.0.1 ip-cannonical
  [Net::BGP] ok 146 - 127.0.0.1 ip-cannonical²
  [Net::BGP] ok 147 - ::ffff:127.0.0.1 ip-cannonical
  [Net::BGP] ok 148 - ::ffff:127.0.0.1 ip-cannonical²
  [Net::BGP] ok 149 - 1920.0.2.1 ip-valid (invalid)
  [Net::BGP] ok 150 - 1::2::3 ip-valid (invalid)
  [Net::BGP] ok 151 - 2001:db8:g::1 ip-valid (invalid)
  [Net::BGP] # Subtest: IPv4 CIDRs
  [Net::BGP]     ok 1 - CIDR 0.0.0.0/24
  [Net::BGP]     ok 2 - CIDR 10.0.0.0/8
  [Net::BGP]     ok 3 - CIDR 0.0.0.0/0 maps to CIDR
  [Net::BGP]     ok 4 - CIDR 10.0.0.0/8 maps to CIDR
  [Net::BGP]     ok 5 - CIDR 10.0.0.0/24 maps to CIDR
  [Net::BGP]     ok 6 - CIDR 192.0.2.4/30 maps to CIDR
  [Net::BGP]     ok 7 - CIDR 255.255.255.255/32 maps to CIDR
  [Net::BGP]     ok 8 - CIDR 0.0.0.0/a dies ok
  [Net::BGP]     ok 9 - CIDR 192.0.2.1/33 dies ok
  [Net::BGP]     not ok 10 - CIDR 3/29 dies ok # TODO Regex matching is slow...fix lib/Net/BGP/IP.pm6
  [Net::BGP]     # Failed test 'CIDR 3/29 dies ok'
  [Net::BGP]     # at t/01-ip-test.t line 194
  [Net::BGP]     ok 11 - Test 1 - Count Correct
  [Net::BGP]     ok 12 - Test 1 - String Correct
  [Net::BGP]     ok 13 - Test 2 - Count Correct
  [Net::BGP]     ok 14 - Test 2 - String Correct
  [Net::BGP]     ok 15 - Test 3 - Count Correct
  [Net::BGP]     ok 16 - Test 3 - String Correct
  [Net::BGP]     ok 17 - Test 4 - Count Correct
  [Net::BGP]     ok 18 - Test 4 - String Correct
  [Net::BGP]     ok 19 - Test 5 - Count Correct
  [Net::BGP]     ok 20 - Test 5a - String Correct
  [Net::BGP]     ok 21 - Test 5b - String Correct
  [Net::BGP]     ok 22 - 0.0.0.0/0 contains 0.0.0.0/0
  [Net::BGP]     ok 23 - 0.0.0.0/32 does not contain 0.0.0.0/0
  [Net::BGP]     ok 24 - 0.0.0.0/0 contains 10.0.0.0/8
  [Net::BGP]     ok 25 - 0.0.0.0/32 does not contain 10.0.0.0/8
  [Net::BGP]     ok 26 - 0.0.0.0/0 contains 10.0.0.0/24
  [Net::BGP]     ok 27 - 0.0.0.0/32 does not contain 10.0.0.0/24
  [Net::BGP]     ok 28 - 0.0.0.0/0 contains 192.0.2.4/30
  [Net::BGP]     ok 29 - 0.0.0.0/32 does not contain 192.0.2.4/30
  [Net::BGP]     ok 30 - 0.0.0.0/0 contains 255.255.255.255/32
  [Net::BGP]     ok 31 - 0.0.0.0/32 does not contain 255.255.255.255/32
  [Net::BGP]     ok 32 - 4.2.2.0/24 contains 4.2.2.0/24
  [Net::BGP]     ok 33 - 4.2.2.0/32 does not contain 4.2.2.0/32
  [Net::BGP]     ok 34 - 4.2.2.0/24 contains 4.2.2.0/24
  [Net::BGP]     ok 35 - 4.2.2.0/24 contains 4.2.2.0/24
  [Net::BGP]     1..35
  [Net::BGP] ok 152 - IPv4 CIDRs
  [Net::BGP] # Subtest: IPv6 CIDRs
  [Net::BGP]     ok 1 - CIDR ::/0
  [Net::BGP]     ok 2 - CIDR 2001::/16
  [Net::BGP]     ok 3 - CIDR ::/0 maps to CIDR
  [Net::BGP]     ok 4 - CIDR 2001:db8::/32 maps to CIDR
  [Net::BGP]     ok 5 - CIDR 2001:db8:1234::/48 maps to CIDR
  [Net::BGP]     ok 6 - CIDR 2001:db8:4321::ff00/120 maps to CIDR
  [Net::BGP]     ok 7 - CIDR ffff:ffff:ffff:ffff:ffff:ffff:ffff:ffff/128 maps to CIDR
  [Net::BGP]     ok 8 - CIDR ::/a dies ok
  [Net::BGP]     ok 9 - CIDR 2001 dies ok
  [Net::BGP]     ok 10 - CIDR db8	True dies ok
  [Net::BGP]     ok 11 - CIDR ::/129 dies ok
  [Net::BGP]     ok 12 - CIDR 2001:/16 dies ok
  [Net::BGP]     ok 13 - CIDR 2001:55555::/32 dies ok
  [Net::BGP]     ok 14 - Test 1 - Count Correct
  [Net::BGP]     ok 15 - Test 1 - String Correct
  [Net::BGP]     ok 16 - Test 2 - Count Correct
  [Net::BGP]     ok 17 - Test 2 - String Correct
  [Net::BGP]     ok 18 - Test 3 - Count Correct
  [Net::BGP]     ok 19 - Test 3 - String Correct
  [Net::BGP]     ok 20 - Test 4 - Count Correct
  [Net::BGP]     ok 21 - Test 4 - String Correct
  [Net::BGP]     ok 22 - Test 5 - Count Correct
  [Net::BGP]     ok 23 - Test 5a - String Correct
  [Net::BGP]     ok 24 - Test 5b - String Correct
  [Net::BGP]     ok 25 - ::/0 contains ::/0
  [Net::BGP]     ok 26 - ::/128 does not contain ::/0
  [Net::BGP]     ok 27 - ::/0 contains 2001:db8::/32
  [Net::BGP]     ok 28 - ::/128 does not contain 2001:db8::/32
  [Net::BGP]     ok 29 - ::/0 contains 2001:db8:1234::/48
  [Net::BGP]     ok 30 - ::/128 does not contain 2001:db8:1234::/48
  [Net::BGP]     ok 31 - ::/0 contains 2001:db8:4321::ff00/120
  [Net::BGP]     ok 32 - ::/128 does not contain 2001:db8:4321::ff00/120
  [Net::BGP]     ok 33 - ::/0 contains ffff:ffff:ffff:ffff:ffff:ffff:ffff:ffff/128
  [Net::BGP]     ok 34 - ::/128 does not contain ffff:ffff:ffff:ffff:ffff:ffff:ffff:ffff/128
  [Net::BGP]     ok 35 - 2001:db8::/32 contains 2001:db8::/32
  [Net::BGP]     ok 36 - 2001:db8::/48 does not contain 2001:db8::/48
  [Net::BGP]     ok 37 - 2001:db8::/32 contains 2001:db8::/32
  [Net::BGP]     ok 38 - 2001:db8::/32 contains 2001:db8::/32
  [Net::BGP]     1..38
  [Net::BGP] ok 153 - IPv6 CIDRs
  [Net::BGP] # Subtest: Misc. Tests
  [Net::BGP]     ok 1 - buf8-to-ipv4 returns good value
  [Net::BGP]     ok 2 - Long IPv6-ish parts fail parse
  [Net::BGP]     1..2
  [Net::BGP] ok 154 - Misc. Tests
  [Net::BGP] 1..154
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/02-as-list.t
  [Net::BGP] ok 1 - (0) ordered
  [Net::BGP] ok 2 - (0) asn-size
  [Net::BGP] ok 3 - (0) asn-count
  [Net::BGP] ok 4 - (0) elems
  [Net::BGP] ok 5 - (1) ordered
  [Net::BGP] ok 6 - (1) asn-size
  [Net::BGP] ok 7 - (1) asn-count
  [Net::BGP] ok 8 - (1) elems
  [Net::BGP] ok 9 - (1) First ASN
  [Net::BGP] ok 10 - (1) Second ASN
  [Net::BGP] ok 11 - (2) ordered
  [Net::BGP] ok 12 - (2) asn-size
  [Net::BGP] ok 13 - (2) asn-count
  [Net::BGP] ok 14 - (2) elems
  [Net::BGP] ok 15 - (2) First ASN
  [Net::BGP] ok 16 - (2) Second ASN
  [Net::BGP] ok 17 - Proper number of AS lists
  [Net::BGP] ok 18 - First AS Sequence is correct
  [Net::BGP] ok 19 - Second AS Sequence is correct
  [Net::BGP] ok 20 - (A) Proper number of AS lists
  [Net::BGP] ok 21 - (A) First AS Sequence is correct
  [Net::BGP] ok 22 - (B) Proper number of AS lists
  [Net::BGP] ok 23 - (B) First AS Sequence is correct
  [Net::BGP] ok 24 - (B) First AS Sequence is correct (elems)
  [Net::BGP] ok 25 - (B) First AS Sequence Ordering
  [Net::BGP] ok 26 - (B) First AS Sequence path length is correct
  [Net::BGP] ok 27 - (B) Second AS Sequence is correct
  [Net::BGP] ok 28 - (B) Second AS Sequence is correct (elems 1)
  [Net::BGP] ok 29 - (B) Second AS Sequence is correct (elems 2)
  [Net::BGP] ok 30 - (B) Second AS Sequence Ordering
  [Net::BGP] ok 31 - (B) Second AS Sequence path length is correct
  [Net::BGP] ok 32 - (B) Third AS Sequence is correct
  [Net::BGP] ok 33 - (B) Third AS Sequence Ordering
  [Net::BGP] ok 34 - (B) Third AS Sequence path length is correct
  [Net::BGP] ok 35 - (B) Forth AS Sequence is correct
  [Net::BGP] ok 36 - (B) Forth AS Sequence is correct (elems 1)
  [Net::BGP] ok 37 - (B) Forth AS Sequence Ordering
  [Net::BGP] ok 38 - (B) Forth AS Sequence path length is correct
  [Net::BGP] ok 39 - (C) Proper number of AS lists
  [Net::BGP] 1..39
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/03-afi-safi.t
  [Net::BGP] # Subtest: afi
  [Net::BGP]     ok 1 - IP correct¹
  [Net::BGP]     ok 2 - IP correct²
  [Net::BGP]     ok 3 - 15000 correct¹
  [Net::BGP]     ok 4 - 15000 correct²
  [Net::BGP]     ok 5 - Properly dies on unknown name
  [Net::BGP]     1..5
  [Net::BGP] ok 1 - afi
  [Net::BGP] # Subtest: safi
  [Net::BGP]     ok 1 - Unicast correct¹
  [Net::BGP]     ok 2 - Unicast correct²
  [Net::BGP]     ok 3 - 77 correct¹
  [Net::BGP]     ok 4 - 77 correct²
  [Net::BGP]     ok 5 - Properly dies on unknown name
  [Net::BGP]     1..5
  [Net::BGP] ok 2 - safi
  [Net::BGP] 1..2
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/10-linux-socket.t
  [Net::BGP] KERNEL Name: linux
  [Net::BGP] # Subtest: Basic Server
  [Net::BGP]     ok 1 - sock is proper type
  [Net::BGP]     ok 2 - sock is defined
  [Net::BGP]     ok 3 - bound port does not die
  [Net::BGP]     ok 4 - bound port in proper range
  [Net::BGP] # Listening on port 48373
  [Net::BGP]     ok 5 - connections is a Supply
  [Net::BGP]     ok 6 - conn is Socket-Connection
  [Net::BGP]     ok 7 - conn is defined
  [Net::BGP]     ok 8 - my-host matches
  [Net::BGP]     ok 9 - my-port matches bound-port
  [Net::BGP]     ok 10 - Peer family is AF_INET
  [Net::BGP]     ok 11 - Connected to localhost
  [Net::BGP]     ok 12 - Socket is UInt
  [Net::BGP]     ok 13 - Socket is defined
  [Net::BGP]     ok 14 - Read line 1
  [Net::BGP]     ok 15 - Read line 2
  [Net::BGP]     ok 16 - Read line 3
  [Net::BGP]     ok 17 - Read line 4
  [Net::BGP]     ok 18 - Read line 5
  [Net::BGP]     ok 19 - Read line 6
  [Net::BGP]     ok 20 - Read line 7
  [Net::BGP]     1..20
  [Net::BGP] ok 1 - Basic Server
  [Net::BGP] # Subtest: Client/Server
  [Net::BGP] # Listening on port 51277
  [Net::BGP]     ok 1 - Listening socket closed
  [Net::BGP]     ok 2 - Read line 1
  [Net::BGP]     ok 3 - Read line 2
  [Net::BGP]     ok 4 - Connection 1 closed
  [Net::BGP]     ok 5 - Connection 2 closed
  [Net::BGP]     1..5
  [Net::BGP] ok 2 - Client/Server
  [Net::BGP] # Subtest: Client/Server - MD5 Non-Match
  [Net::BGP]     ok 1 - Listening socket closed
  [Net::BGP] close failed
  [Net::BGP]   in method close at /home/coke/sandbox/blin/installed/TCP::LowLevel_zef:jmaslak_0.1.2_0/sources/FD0DA2442C87EA8FCD884AD3E40CB842A87FE536 (TCP::LowLevel::Socket-Connection-Linux) line 134
  [Net::BGP]   in method recv at /home/coke/sandbox/blin/installed/TCP::LowLevel_zef:jmaslak_0.1.2_0/sources/FD0DA2442C87EA8FCD884AD3E40CB842A87FE536 (TCP::LowLevel::Socket-Connection-Linux) line 68
  [Net::BGP]   in sub  at t/10-linux-socket.t line 134
  [Net::BGP]   in sub subtest at /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/share/perl6/core/sources/EB7292978FA6A0BE4AC1D011ADF25287B8F219B9 (Test) line 430
  [Net::BGP]   in sub subtest at /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/share/perl6/core/sources/EB7292978FA6A0BE4AC1D011ADF25287B8F219B9 (Test) line 418
  [Net::BGP]   in block <unit> at t/10-linux-socket.t line 109
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/11-socket.t
  [Net::BGP] # Subtest: Basic Server - Native OS
  [Net::BGP]     ok 1 - sock is defined
  [Net::BGP]     ok 2 - connections is a Supply
  [Net::BGP]     ok 3 - bound port promise is kept
  [Net::BGP]     ok 4 - bound port does not die
  [Net::BGP]     ok 5 - bound port in proper range
  [Net::BGP] # Listening on port 37537
  [Net::BGP]     ok 6 - conn is defined
  [Net::BGP]     ok 7 - socket-host matches
  [Net::BGP]     ok 8 - socket-port matches socket-port
  [Net::BGP]     ok 9 - Connected to localhost
  [Net::BGP]     ok 10 - Read line 1
  [Net::BGP]     ok 11 - Read line 2
  [Net::BGP]     ok 12 - Read line 3
  [Net::BGP]     ok 13 - Read line 4
  [Net::BGP]     1..13
  [Net::BGP] ok 1 - Basic Server - Native OS
  [Net::BGP] # Subtest: Basic Server - Fallback
  [Net::BGP]     ok 1 - sock is defined
  [Net::BGP]     ok 2 - connections is a Supply
  [Net::BGP]     ok 3 - bound port promise is kept
  [Net::BGP]     ok 4 - bound port does not die
  [Net::BGP]     ok 5 - bound port in proper range
  [Net::BGP] # Listening on port 44557
  [Net::BGP]     ok 6 - conn is defined
  [Net::BGP]     ok 7 - socket-host matches
  [Net::BGP]     ok 8 - socket-port matches socket-port
  [Net::BGP]     ok 9 - Connected to localhost
  [Net::BGP]     ok 10 - Read line 1
  [Net::BGP]     ok 11 - Read line 2
  [Net::BGP]     ok 12 - Read line 3
  [Net::BGP]     ok 13 - Read line 4
  [Net::BGP]     1..13
  [Net::BGP] ok 2 - Basic Server - Fallback
  [Net::BGP] 1..2
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/30-basic.t
  [Net::BGP] # Subtest: Basic Class Construction
  [Net::BGP]     ok 1 - Created BGP Class
  [Net::BGP]     ok 2 - Port has proper default
  [Net::BGP]     ok 3 - Port is properly set to 1179
  [Net::BGP]     ok 4 - Port is properly set to 179 by Nil
  [Net::BGP]     ok 5 - Cannot change port
  [Net::BGP]     ok 6 - < 0 port rejected
  [Net::BGP]     ok 7 - >65535 port rejected
  [Net::BGP]     ok 8 - >65535 identifier rejected
  [Net::BGP]     ok 9 - Non-existent attribute causes failure
  [Net::BGP]     ok 10 - Must provide my-asn
  [Net::BGP]     ok 11 - Invalid ASN dies
  [Net::BGP]     1..11
  [Net::BGP] ok 1 - Basic Class Construction
  [Net::BGP] # Subtest: Listener
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     1..2
  [Net::BGP] ok 2 - Listener
  [Net::BGP] 1..2
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/31-conn-open-close-event.t
  [Net::BGP] # Subtest: Event
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - Message type is as expected
  [Net::BGP]     ok 4 - Client IP is as expected
  [Net::BGP]     ok 5 - Client port is as expected
  [Net::BGP]     ok 6 - Close message type is as expected
  [Net::BGP]     ok 7 - Close client IP is as expected
  [Net::BGP]     ok 8 - Close client port is as expected
  [Net::BGP]     1..8
  [Net::BGP] ok 1 - Event
  [Net::BGP] 1..1
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/32-Command-Dead-Child.t
  [Net::BGP] ok 1 - Created Net::BGP::Command::Dead-Child Class
  [Net::BGP] ok 2 - Proper Dead-Child command
  [Net::BGP] ok 3 - Payload is correct
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/50-messages.t
  [Net::BGP] # Subtest: Command
  [Net::BGP]     # Subtest: Parent Class
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Message type has proper default
  [Net::BGP]         1..2
  [Net::BGP]     ok 1 - Parent Class
  [Net::BGP]     # Subtest: BGP-Message
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Proper BGP-Message message
  [Net::BGP]         ok 3 - Payload is correct
  [Net::BGP]         1..3
  [Net::BGP]     ok 2 - BGP-Message
  [Net::BGP]     # Subtest: Stop
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Proper Stop message
  [Net::BGP]         1..2
  [Net::BGP]     ok 3 - Stop
  [Net::BGP]     1..3
  [Net::BGP] ok 1 - Command
  [Net::BGP] # Subtest: Event
  [Net::BGP]     # Subtest: Parent Class
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Connection ID is proper
  [Net::BGP]         ok 3 - Message type has proper default
  [Net::BGP]         ok 4 - Message is not an error
  [Net::BGP]         ok 5 - Date time appears correct
  [Net::BGP]         1..5
  [Net::BGP]     ok 1 - Parent Class
  [Net::BGP]     # Subtest: BGP-Message-No-Opt
  [Net::BGP]         ok 1 - Created Event Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is not an error
  [Net::BGP]         ok 5 - BGP message type is correct
  [Net::BGP]         ok 6 - BGP message code is correct
  [Net::BGP]         ok 7 - Proper number of parameter elements
  [Net::BGP]         ok 8 - Date time appears correct
  [Net::BGP]         ok 9 - Peer ASN is proper
  [Net::BGP]         1..9
  [Net::BGP]     ok 2 - BGP-Message-No-Opt
  [Net::BGP]     # Subtest: BGP-Message-With-Opt
  [Net::BGP]         ok 1 - Created Event Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is not an error
  [Net::BGP]         ok 5 - BGP message type is correct
  [Net::BGP]         ok 6 - BGP message code is correct
  [Net::BGP]         ok 7 - Date time appears correct
  [Net::BGP]         ok 8 - Proper number of parameter elements
  [Net::BGP]         ok 9 - 240 Proper parameter-code
  [Net::BGP]         ok 10 - 240 Proper parameter-name
  [Net::BGP]         ok 11 - 240 Proper parameter-length
  [Net::BGP]         ok 12 - 240 Proper parameter-value length
  [Net::BGP]         ok 13 - 241 Proper parameter-code
  [Net::BGP]         ok 14 - 241 Proper parameter-name
  [Net::BGP]         ok 15 - 241 Proper parameter-length
  [Net::BGP]         ok 16 - 241 Proper parameter-value length
  [Net::BGP]         ok 17 - 241 Proper parameter-value
  [Net::BGP]         1..17
  [Net::BGP]     ok 3 - BGP-Message-With-Opt
  [Net::BGP]     # Subtest: Closed-Connection
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Proper Closed-Connection message
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Client IP address
  [Net::BGP]         ok 5 - Client IP port
  [Net::BGP]         ok 6 - Message is not an error
  [Net::BGP]         1..6
  [Net::BGP]     ok 4 - Closed-Connection
  [Net::BGP]     # Subtest: New-Connection
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Proper New-Connection message
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Client IP address
  [Net::BGP]         ok 5 - Client IP port
  [Net::BGP]         ok 6 - Message is not an error
  [Net::BGP]         1..6
  [Net::BGP]     ok 5 - New-Connection
  [Net::BGP]     1..5
  [Net::BGP] ok 2 - Event
  [Net::BGP] # Subtest: Error
  [Net::BGP]     # Subtest: Parent Class
  [Net::BGP]         ok 1 - Created BGP Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Message is an error
  [Net::BGP]         ok 4 - Human readable type
  [Net::BGP]         1..4
  [Net::BGP]     ok 1 - Parent Class
  [Net::BGP]     # Subtest: Bad-Option-Length
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         ok 6 - Length is valid
  [Net::BGP]         1..6
  [Net::BGP]     ok 2 - Bad-Option-Length
  [Net::BGP]     # Subtest: Bad-Parameter-Length
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         ok 6 - Length is valid
  [Net::BGP]         1..6
  [Net::BGP]     ok 3 - Bad-Parameter-Length
  [Net::BGP]     # Subtest: Hold-Time-Too-Short
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         ok 6 - Hold-Time is valid
  [Net::BGP]         1..6
  [Net::BGP]     ok 4 - Hold-Time-Too-Short
  [Net::BGP]     # Subtest: Length-Too-Short
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         ok 6 - Length is valid
  [Net::BGP]         1..6
  [Net::BGP]     ok 5 - Length-Too-Short
  [Net::BGP]     # Subtest: Marker-Format
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         1..5
  [Net::BGP]     ok 6 - Marker-Format
  [Net::BGP]     # Subtest: Unknown-Version
  [Net::BGP]         ok 1 - Created Error Class
  [Net::BGP]         ok 2 - Message type has proper value
  [Net::BGP]         ok 3 - Connection ID is proper
  [Net::BGP]         ok 4 - Message is an error
  [Net::BGP]         ok 5 - Human readable type
  [Net::BGP]         ok 6 - Version is valid
  [Net::BGP]         1..6
  [Net::BGP]     ok 7 - Unknown-Version
  [Net::BGP]     1..7
  [Net::BGP] ok 3 - Error
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/51-bgp-messages-from-hash.t
  [Net::BGP] # Subtest: Open Message
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - BGP version is correct
  [Net::BGP]     ok 5 - ASN is correct
  [Net::BGP]     ok 6 - Hold time is correct
  [Net::BGP]     ok 7 - BGP identifier is correct
  [Net::BGP]     ok 8 - Supports IPv4
  [Net::BGP]     ok 9 - Supports IPv6
  [Net::BGP]     ok 10 - FH BGP message is defined
  [Net::BGP]     ok 11 - FH Message type is correct
  [Net::BGP]     ok 12 - FH Message code is correct
  [Net::BGP]     ok 13 - BGP version is correct
  [Net::BGP]     ok 14 - FH ASN is correct
  [Net::BGP]     ok 15 - FH Hold time is correct
  [Net::BGP]     ok 16 - FH BGP identifier is correct
  [Net::BGP]     ok 17 - Message value correct
  [Net::BGP]     ok 18 - can create with IP ID
  [Net::BGP]     ok 19 - can create with Int Message Code
  [Net::BGP]     ok 20 - can create with Message Type
  [Net::BGP]     ok 21 - can create with Message Typeand int Code
  [Net::BGP]     ok 22 - can create with Message Type and Code
  [Net::BGP]     1..22
  [Net::BGP] ok 1 - Open Message
  [Net::BGP] # Subtest: Keep-Alive Message
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - FH BGP message is defined
  [Net::BGP]     ok 5 - FH Message type is correct
  [Net::BGP]     ok 6 - FH Message code is correct
  [Net::BGP]     ok 7 - Message value correct
  [Net::BGP]     1..7
  [Net::BGP] ok 2 - Keep-Alive Message
  [Net::BGP] # Subtest: Update-ASN16
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - FH BGP message is defined
  [Net::BGP]     ok 5 - FH Message type is correct
  [Net::BGP]     ok 6 - FH Message code is correct
  [Net::BGP]     ok 7 - Message value correct
  [Net::BGP]     1..7
  [Net::BGP] ok 3 - Update-ASN16
  [Net::BGP] # Subtest: Update-Withdrawal-Only-ASN16
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - FH BGP message is defined
  [Net::BGP]     ok 5 - FH Message type is correct
  [Net::BGP]     ok 6 - FH Message code is correct
  [Net::BGP]     ok 7 - Message value correct
  [Net::BGP]     1..7
  [Net::BGP] ok 4 - Update-Withdrawal-Only-ASN16
  [Net::BGP] # Subtest: Update-MP
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - FH BGP message is defined
  [Net::BGP]     ok 5 - FH Message type is correct
  [Net::BGP]     ok 6 - FH Message code is correct
  [Net::BGP]     ok 7 - Message value correct
  [Net::BGP]     1..7
  [Net::BGP] ok 5 - Update-MP
  [Net::BGP] 1..5
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/52-bgp-messages-raw.t
  [Net::BGP] # Subtest: Generic
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - Message value correct
  [Net::BGP]     1..4
  [Net::BGP] ok 1 - Generic
  [Net::BGP] # Subtest: Open Message
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - BGP version is correct
  [Net::BGP]     ok 5 - ASN is correct
  [Net::BGP]     ok 6 - Hold time is correct
  [Net::BGP]     ok 7 - BGP identifier is correct
  [Net::BGP]     ok 8 - Message value correct
  [Net::BGP]     1..8
  [Net::BGP] ok 2 - Open Message
  [Net::BGP] # Subtest: Open Message w/ Capabilities
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - BGP version is correct
  [Net::BGP]     ok 5 - ASN is correct
  [Net::BGP]     ok 6 - Hold time is correct
  [Net::BGP]     ok 7 - BGP identifier is correct
  [Net::BGP]     ok 8 - IPv4 Support
  [Net::BGP]     ok 9 - IPv6 Support
  [Net::BGP]     ok 10 - Proper number of Parameters
  [Net::BGP]     ok 11 - Parameter is a Capabilitiy
  [Net::BGP]     ok 12 - Parameter has proper code
  [Net::BGP]     ok 13 - Parameter has proper name
  [Net::BGP]     ok 14 - Proper number of capabilities
  [Net::BGP]     ok 15 - Capability¹ is proper type
  [Net::BGP]     ok 16 - Capability¹ has proper code
  [Net::BGP]     ok 17 - Capability¹ has proper name
  [Net::BGP]     ok 18 - Capability² is proper type
  [Net::BGP]     ok 19 - Capability² has proper code
  [Net::BGP]     ok 20 - Capability² has proper name
  [Net::BGP]     ok 21 - Capability² has proper asn
  [Net::BGP]     ok 22 - Capability³ is proper type
  [Net::BGP]     ok 23 - Capability³ has proper code
  [Net::BGP]     ok 24 - Capability³ has proper name
  [Net::BGP]     ok 25 - Capability³ has proper afi
  [Net::BGP]     ok 26 - Capability³ has proper safi
  [Net::BGP]     ok 27 - Capability³ has proper reserved
  [Net::BGP]     ok 28 - Capability⁴ is proper type
  [Net::BGP]     ok 29 - Capability⁴ has proper code
  [Net::BGP]     ok 30 - Capability⁴ has proper name
  [Net::BGP]     ok 31 - Capability⁴ has proper afi
  [Net::BGP]     ok 32 - Capability⁴ has proper safi
  [Net::BGP]     ok 33 - Capability⁴ has proper reserved
  [Net::BGP]     ok 34 - Capability⁵ is proper type
  [Net::BGP]     ok 35 - Capability⁵ has proper code
  [Net::BGP]     ok 36 - Capability⁵ has proper name
  [Net::BGP]     ok 37 - Capability⁵ has proper restart
  [Net::BGP]     ok 38 - Capability⁵ has proper reserved
  [Net::BGP]     ok 39 - Capability⁵ has proper flags
  [Net::BGP]     ok 40 - Capability⁵ has proper restart-time
  [Net::BGP]     ok 41 - Capability⁵ has proper num of per-af
  [Net::BGP]     ok 42 - Capability⁵ has proper per-af AFI
  [Net::BGP]     ok 43 - Capability⁵ has proper per-af SAFI
  [Net::BGP]     ok 44 - Capability⁵ has proper per-af AFI Name
  [Net::BGP]     ok 45 - Capability⁵ has proper per-af SAFI Name
  [Net::BGP]     ok 46 - Capability⁵ has proper per-af Flags
  [Net::BGP]     ok 47 - Capability⁶ is proper type
  [Net::BGP]     ok 48 - Capability⁶ has proper code
  [Net::BGP]     ok 49 - Capability⁶ has proper name
  [Net::BGP]     ok 50 - Capability⁶ has proper hostname
  [Net::BGP]     ok 51 - Capability⁶ has proper domain
  [Net::BGP]     ok 52 - Message value correct
  [Net::BGP]     1..52
  [Net::BGP] ok 3 - Open Message w/ Capabilities
  [Net::BGP] # Subtest: Keep-Alive Message
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - Message value correct
  [Net::BGP]     1..4
  [Net::BGP] ok 4 - Keep-Alive Message
  [Net::BGP] # Subtest: Update Message (ASN16)
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - BGP message is proper type
  [Net::BGP]     ok 3 - Message type is correct
  [Net::BGP]     ok 4 - Message code is correct
  [Net::BGP]     ok 5 - Proper number of withdrawn prefixes
  [Net::BGP]     ok 6 - Withdrawn 1 correct
  [Net::BGP]     ok 7 - Withdrawn 2 correct
  [Net::BGP]     ok 8 - Withdrawn 3 correct
  [Net::BGP]     ok 9 - Proper number of path elements
  [Net::BGP]     ok 10 - Path Attribute 1 Proper Type
  [Net::BGP]     ok 11 - Path Attribute 1 Proper Value
  [Net::BGP]     ok 12 - Origin is valid
  [Net::BGP]     ok 13 - Path Attribute 2 Proper Type
  [Net::BGP]     ok 14 - Path Attribute 2 Proper Value
  [Net::BGP]     ok 15 - as-path is valid
  [Net::BGP]     ok 16 - path is valid
  [Net::BGP]     ok 17 - Path Attribute 3 Proper Type
  [Net::BGP]     ok 18 - Path Attribute 3 Proper Value
  [Net::BGP]     ok 19 - next-hop is valid
  [Net::BGP]     ok 20 - Path Attribute 4 Proper Type
  [Net::BGP]     ok 21 - Path Attribute 4 Proper Value
  [Net::BGP]     ok 22 - Path Attribute 5 Proper Type
  [Net::BGP]     ok 23 - Path Attribute 5 Proper Value
  [Net::BGP]     ok 24 - Path Attribute 6 Proper Type
  [Net::BGP]     ok 25 - Atomic Attribute is present
  [Net::BGP]     ok 26 - Path Attribute 7 Proper Type
  [Net::BGP]     ok 27 - Aggregator ASN correct
  [Net::BGP]     ok 28 - Aggregator IP correct
  [Net::BGP]     ok 29 - Path Attribute 8 Proper Type
  [Net::BGP]     ok 30 - Path Attribute 7 Proper Value
  [Net::BGP]     ok 31 - Communities are proper
  [Net::BGP]     ok 32 - Path Attribute 9 Proper Type
  [Net::BGP]     ok 33 - Path Attribute 9 Proper Value
  [Net::BGP]     ok 34 - Path Attribute 10 Proper Type
  [Net::BGP]     ok 35 - Path Attribute 10 Proper Value
  [Net::BGP]     ok 36 - Path Attribute 10 Proper Type
  [Net::BGP]     ok 37 - Path Attribute 10 Proper Value
  [Net::BGP]     ok 38 - Extended Communities are proper
  [Net::BGP]     ok 39 - Path Attribute 11 Proper Type
  [Net::BGP]     ok 40 - AS4-Aggregator ASN correct
  [Net::BGP]     ok 41 - AS4-Aggregator IP correct
  [Net::BGP]     ok 42 - Path Attribute 12 Proper Type
  [Net::BGP]     ok 43 - Path Attribute 12 Proper Value
  [Net::BGP]     ok 44 - Long Communities are proper
  [Net::BGP]     ok 45 - Proper number of NLRI prefixes
  [Net::BGP]     ok 46 - NLRI 1 correct
  [Net::BGP]     ok 47 - NLRI 1 correct
  [Net::BGP]     ok 48 - NLRI 1 correct
  [Net::BGP]     ok 49 - Message value correct
  [Net::BGP]     1..49
  [Net::BGP] ok 5 - Update Message (ASN16)
  [Net::BGP] # Subtest: Update Message Withdrawal Only (ASN16)
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - BGP message is proper type
  [Net::BGP]     ok 3 - Message type is correct
  [Net::BGP]     ok 4 - Message code is correct
  [Net::BGP]     ok 5 - Proper number of withdrawn prefixes
  [Net::BGP]     ok 6 - Withdrawn 1 correct
  [Net::BGP]     ok 7 - Withdrawn 2 correct
  [Net::BGP]     ok 8 - Withdrawn 3 correct
  [Net::BGP]     ok 9 - Proper number of path elements
  [Net::BGP]     ok 10 - Proper number of NLRI prefixes
  [Net::BGP]     ok 11 - Message value correct
  [Net::BGP]     1..11
  [Net::BGP] ok 6 - Update Message Withdrawal Only (ASN16)
  [Net::BGP] # Subtest: Update Message (MP-BGP)
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - BGP message is proper type
  [Net::BGP]     ok 3 - Message type is correct
  [Net::BGP]     ok 4 - Message code is correct
  [Net::BGP]     ok 5 - Proper number of withdrawn prefixes
  [Net::BGP]     ok 6 - Proper number of path elements
  [Net::BGP]     ok 7 - Path Attribute 1 Proper Type
  [Net::BGP]     ok 8 - Path Attribute 1 Proper Value
  [Net::BGP]     ok 9 - Path Attribute 2 Proper Type
  [Net::BGP]     ok 10 - Path Attribute 2 Proper Value
  [Net::BGP]     ok 11 - AS Path has proper length
  [Net::BGP]     ok 12 - Path Attribute 3 Proper Type
  [Net::BGP]     ok 13 - Path Attribute 3A Proper Value
  [Net::BGP]     ok 14 - Path Attribute 3B Proper Value
  [Net::BGP]     ok 15 - Path Attribute 3C Proper Value
  [Net::BGP]     ok 16 - Path Attribute 3D Proper Value
  [Net::BGP]     ok 17 - Path Attribute 3E Proper Value
  [Net::BGP]     ok 18 - Path Attribute 3F Proper Value
  [Net::BGP]     ok 19 - Path Attribute 4 Proper Type
  [Net::BGP]     ok 20 - Path Attribute 4A Proper Value
  [Net::BGP]     ok 21 - Path Attribute 4B Proper Value
  [Net::BGP]     ok 22 - Path Attribute 4E Proper Value
  [Net::BGP]     ok 23 - Path Attribute 4F Proper Value
  [Net::BGP]     ok 24 - Proper number of NLRI prefixes
  [Net::BGP]     ok 25 - Message value correct
  [Net::BGP]     1..25
  [Net::BGP] ok 7 - Update Message (MP-BGP)
  [Net::BGP] 1..7
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/53-Open-With-Multiple-CapOpts.t
  [Net::BGP] ok 1 - BGP message is defined
  [Net::BGP] ok 2 - Message type is correct
  [Net::BGP] ok 3 - Message code is correct
  [Net::BGP] ok 4 - BGP version is correct
  [Net::BGP] ok 5 - ASN is correct
  [Net::BGP] ok 6 - Hold time is correct
  [Net::BGP] ok 7 - BGP identifier is correct
  [Net::BGP] ok 8 - Proper number of Parameters
  [Net::BGP] ok 9 - Parameter¹ is a Capabilitiy
  [Net::BGP] ok 10 - Parameter¹ has proper code
  [Net::BGP] ok 11 - Parameter¹ has proper name
  [Net::BGP] ok 12 - Parameter² is a Capabilitiy
  [Net::BGP] ok 13 - Parameter² has proper code
  [Net::BGP] ok 14 - Parameter² has proper name
  [Net::BGP] ok 15 - Parameter³ is a Capabilitiy
  [Net::BGP] ok 16 - Parameter³ has proper code
  [Net::BGP] ok 17 - Parameter³ has proper name
  [Net::BGP] ok 18 - Parameter¹ Proper number of capabilities
  [Net::BGP] ok 19 - Capability¹ is proper type
  [Net::BGP] ok 20 - Capability¹ has proper code
  [Net::BGP] ok 21 - Capability¹ has proper name
  [Net::BGP] ok 22 - Parameter² Proper number of capabilities
  [Net::BGP] ok 23 - Capability² is proper type
  [Net::BGP] ok 24 - Capability² has proper code
  [Net::BGP] ok 25 - Capability² has proper name
  [Net::BGP] ok 26 - Capability² has proper asn
  [Net::BGP] ok 27 - Parameter³ Proper number of capabilities
  [Net::BGP] ok 28 - Capability³ is proper type
  [Net::BGP] ok 29 - Capability³ has proper code
  [Net::BGP] ok 30 - Capability³ has proper name
  [Net::BGP] ok 31 - Capability³ has proper afi
  [Net::BGP] ok 32 - Capability³ has proper safi
  [Net::BGP] ok 33 - Capability³ has proper reserved
  [Net::BGP] ok 34 - Message value correct
  [Net::BGP] 1..34
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/54-Update-Failure.t
  [Net::BGP] ok 1 - BGP message is defined
  [Net::BGP] ok 2 - Message type is correct
  [Net::BGP] ok 3 - Message code is correct
  [Net::BGP] ok 4 - NLRI right
  [Net::BGP] ok 5 - right number of path elems
  [Net::BGP] ok 6 - No NLRI6 Elements
  [Net::BGP] ok 7 - Aggregator ASN correct
  [Net::BGP] ok 8 - Aggregator IP correct
  [Net::BGP] 1..8
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/55-bgp-notification-raw.t
  [Net::BGP] # Subtest: Open Notification Unsupported Version
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - Error code is correct
  [Net::BGP]     ok 5 - Error name is correct
  [Net::BGP]     ok 6 - Error subtype is correct
  [Net::BGP]     ok 7 - Error subtype is correct
  [Net::BGP]     ok 8 - Class is correct
  [Net::BGP]     ok 9 - Version is correct
  [Net::BGP]     ok 10 - Message value correct
  [Net::BGP]     1..10
  [Net::BGP] ok 1 - Open Notification Unsupported Version
  [Net::BGP] # Subtest: Open Notification Bad Peer AS
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - Error code is correct
  [Net::BGP]     ok 5 - Error name is correct
  [Net::BGP]     ok 6 - Error subtype is correct
  [Net::BGP]     ok 7 - Error subtype is correct
  [Net::BGP]     ok 8 - Class is correct
  [Net::BGP]     ok 9 - Message value correct
  [Net::BGP]     1..9
  [Net::BGP] ok 2 - Open Notification Bad Peer AS
  [Net::BGP] # Subtest: Open Notification Unsupported Optional Parameter
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - Message type is correct
  [Net::BGP]     ok 3 - Message code is correct
  [Net::BGP]     ok 4 - Error code is correct
  [Net::BGP]     ok 5 - Error name is correct
  [Net::BGP]     ok 6 - Error subtype is correct
  [Net::BGP]     ok 7 - Error subtype is correct
  [Net::BGP]     ok 8 - Class is correct
  [Net::BGP]     ok 9 - Message value correct
  [Net::BGP]     1..9
  [Net::BGP] ok 3 - Open Notification Unsupported Optional Parameter
  [Net::BGP] # Subtest: Header Notification Connection not Syncronized
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - AAA
  [Net::BGP]     ok 3 - Message type is correct
  [Net::BGP]     ok 4 - Message code is correct
  [Net::BGP]     ok 5 - Error code is correct
  [Net::BGP]     ok 6 - Error name is correct
  [Net::BGP]     ok 7 - Error subtype is correct
  [Net::BGP]     ok 8 - Error subtype is correct
  [Net::BGP]     ok 9 - Class is correct
  [Net::BGP]     ok 10 - Message value correct
  [Net::BGP]     1..10
  [Net::BGP] ok 4 - Header Notification Connection not Syncronized
  [Net::BGP] # Subtest: Hold-Timer-Expired
  [Net::BGP]     ok 1 - BGP message is defined
  [Net::BGP]     ok 2 - raw matches message
  [Net::BGP]     ok 3 - Message type is correct
  [Net::BGP]     ok 4 - Message code is correct
  [Net::BGP]     ok 5 - Error code is correct
  [Net::BGP]     ok 6 - Error name is correct
  [Net::BGP]     ok 7 - Error subtype is correct
  [Net::BGP]     ok 8 - Error subtype is correct
  [Net::BGP]     ok 9 - Class is correct
  [Net::BGP]     ok 10 - Message value correct
  [Net::BGP]     1..10
  [Net::BGP] ok 5 - Hold-Timer-Expired
  [Net::BGP] 1..5
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/56-bgp-invalid-marker.t
  [Net::BGP] # Subtest: Syncronization
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Channel message type is as expected
  [Net::BGP]     ok 6 - Is not an error
  [Net::BGP]     ok 7 - Peer is defined
  [Net::BGP]     ok 8 - Peer is Idle
  [Net::BGP]     ok 9 - Close message type is as expected
  [Net::BGP]     ok 10 - Is not an error
  [Net::BGP]     ok 11 - Peer is idle
  [Net::BGP]     ok 12 - Message is proper type
  [Net::BGP]     1..12
  [Net::BGP] ok 1 - Syncronization
  [Net::BGP] 1..1
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/57-bgp-open-bad-asn.t
  [Net::BGP] # Subtest: OPEN
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Peer is defined
  [Net::BGP]     ok 6 - Peer is Idle
  [Net::BGP]     ok 7 - Close message type is as expected
  [Net::BGP]     ok 8 - Is not an error
  [Net::BGP]     ok 9 - Peer is idle
  [Net::BGP]     ok 10 - Message is proper type
  [Net::BGP]     1..10
  [Net::BGP] ok 1 - OPEN
  [Net::BGP] 1..1
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/58-as4-update.t
  [Net::BGP] # Subtest: Both AS4 and AS
  [Net::BGP]     ok 1 - FH BGP message is defined
  [Net::BGP]     ok 2 - AS Path is correct
  [Net::BGP]     ok 3 - AS Path members are correct
  [Net::BGP]     1..3
  [Net::BGP] ok 1 - Both AS4 and AS
  [Net::BGP] # Subtest: Only AS-Path on !ASN32
  [Net::BGP]     ok 1 - FH BGP message is defined
  [Net::BGP]     ok 2 - AS Path is correct
  [Net::BGP]     ok 3 - AS-Path attribute correct
  [Net::BGP]     ok 4 - AS4-Path attribute correct
  [Net::BGP]     1..4
  [Net::BGP] ok 2 - Only AS-Path on !ASN32
  [Net::BGP] # Subtest: Only AS-Path on ASN32
  [Net::BGP]     ok 1 - FH BGP message is defined
  [Net::BGP]     ok 2 - AS Path is correct
  [Net::BGP]     ok 3 - AS-Path attribute correct
  [Net::BGP]     ok 4 - AS4-Path attribute correct
  [Net::BGP]     1..4
  [Net::BGP] ok 3 - Only AS-Path on ASN32
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/60-Path-Attributes.t
  [Net::BGP] # Subtest: Extended-Community
  [Net::BGP]     ok 1 - Created Path Attribute
  [Net::BGP]     ok 2 - From Hash capability correct
  [Net::BGP]     ok 3 - From RAW capability correct
  [Net::BGP]     ok 4 - Route type is correct
  [Net::BGP]     1..4
  [Net::BGP] ok 1 - Extended-Community
  [Net::BGP] 1..1
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/70-peer-object.t
  [Net::BGP] # Subtest: eBGP
  [Net::BGP]     ok 1 - Created BGP Class
  [Net::BGP]     ok 2 - Peer IP is correct
  [Net::BGP]     ok 3 - Peer port is okay
  [Net::BGP]     ok 4 - Peer ASN is okay
  [Net::BGP]     ok 5 - My ASN is okay
  [Net::BGP]     ok 6 - Peer state is okay
  [Net::BGP]     ok 7 - ASN 32 support not indicated
  [Net::BGP]     ok 8 - Not iBGP
  [Net::BGP]     1..8
  [Net::BGP] ok 1 - eBGP
  [Net::BGP] # Subtest: iBGP
  [Net::BGP]     ok 1 - Created BGP Class
  [Net::BGP]     ok 2 - Peer IP is correct
  [Net::BGP]     ok 3 - Peer port is okay
  [Net::BGP]     ok 4 - Peer ASN is okay
  [Net::BGP]     ok 5 - My ASN is okay
  [Net::BGP]     ok 6 - Peer state is okay
  [Net::BGP]     ok 7 - ASN 32 supported
  [Net::BGP]     ok 8 - iBGP
  [Net::BGP]     1..8
  [Net::BGP] ok 2 - iBGP
  [Net::BGP] 1..2
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/80-Validator-Aggregation.t
  [Net::BGP] # Subtest: Good
  [Net::BGP]     ok 1 - No warnings in message
  [Net::BGP]     1..1
  [Net::BGP] ok 1 - Good
  [Net::BGP] # Subtest: AF_MIX
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 2 - AF_MIX
  [Net::BGP] # Subtest: Aggregator ASN
  [Net::BGP]     ok 1 - First message has AGGR_ASN_RESERVED
  [Net::BGP]     ok 2 - Second message has AGGR_ASN_PRIVATE
  [Net::BGP]     ok 3 - Third message has AGGR_ASN_TRANS
  [Net::BGP]     ok 4 - Forth message has MY-ASN
  [Net::BGP]     ok 5 - Fifth message has PEER-ASN
  [Net::BGP]     1..5
  [Net::BGP] ok 3 - Aggregator ASN
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/81-Validator-AS-Path.t
  [Net::BGP] # Subtest: Unexpected AS4 Path
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 1 - Unexpected AS4 Path
  [Net::BGP] # Subtest: Doc ASN
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 2 - Doc ASN
  [Net::BGP] # Subtest: PRIVATE ASN
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 3 - PRIVATE ASN
  [Net::BGP] # Subtest: Reserved ASN
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 4 - Reserved ASN
  [Net::BGP] # Subtest: Trans ASN
  [Net::BGP]     ok 1 - Errors Found
  [Net::BGP]     1..1
  [Net::BGP] ok 5 - Trans ASN
  [Net::BGP] 1..5
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/90-basic-bgp.t
  [Net::BGP] # Subtest: invalid-marker
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     1..6
  [Net::BGP] ok 1 - invalid-marker
  [Net::BGP] # Subtest: invalid-length-short
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     1..6
  [Net::BGP] ok 2 - invalid-length-short
  [Net::BGP] # Subtest: invalid-length-long
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     1..6
  [Net::BGP] ok 3 - invalid-length-long
  [Net::BGP] # Subtest: invalid-version
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     ok 7 - Message is proper type
  [Net::BGP]     ok 8 - Max supported version is valid
  [Net::BGP]     1..8
  [Net::BGP] ok 4 - invalid-version
  [Net::BGP] # Subtest: hold-time-too-short
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     1..6
  [Net::BGP] ok 5 - hold-time-too-short
  [Net::BGP] # Subtest: bad-option-length [1]
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     ok 7 - Length == 1
  [Net::BGP]     1..7
  [Net::BGP] ok 6 - bad-option-length [1]
  [Net::BGP] # Subtest: bad-option-length [3]
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - Error message type is as expected
  [Net::BGP]     ok 6 - Is an error
  [Net::BGP]     ok 7 - Length == 3
  [Net::BGP]     1..7
  [Net::BGP] ok 7 - bad-option-length [3]
  [Net::BGP] # Subtest: OPEN
  [Net::BGP]     ok 1 - BGP Port is 0
  [Net::BGP]     ok 2 - BGP Port isnt 0
  [Net::BGP]     ok 3 - ASN is correct
  [Net::BGP]     ok 4 - Message type is as expected
  [Net::BGP]     ok 5 - BGP message type is as expected
  [Net::BGP]     ok 6 - Is not an error
  [Net::BGP]     ok 7 - BGP Message is proper name
  [Net::BGP]     ok 8 - BGP Message is proper type
  [Net::BGP]     ok 9 - Option length is zero
  [Net::BGP]     ok 10 - Option bytes = len
  [Net::BGP]     ok 11 - Peer ASN is proper
  [Net::BGP]     ok 12 - Peer is defined
  [Net::BGP]     ok 13 - Peer is OpenConfirm
  [Net::BGP]     ok 14 - Connection does not support ASN32
  [Net::BGP]     ok 15 - One AF present
  [Net::BGP]     ok 16 - AFI correct
  [Net::BGP]     ok 17 - SAFI correct
  [Net::BGP]     ok 18 - Message is proper type
  [Net::BGP]     ok 19 - Version correct
  [Net::BGP]     ok 20 - ASN is correct
  [Net::BGP]     ok 21 - Hold-Time is correct
  [Net::BGP]     ok 22 - Identifier is correct
  [Net::BGP]     ok 23 - Option length is correct
  [Net::BGP]     ok 24 - No parameters provided
  [Net::BGP]     ok 25 - Close message type is as expected
  [Net::BGP]     ok 26 - Is not an error
  [Net::BGP]     ok 27 - Peer is idle
  [Net::BGP]     1..27
  [Net::BGP] ok 8 - OPEN
  [Net::BGP] 1..8
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/91-send-update.t
  [Net::BGP] ok 1 - BGP Port is 0
  [Net::BGP] ok 2 - BGP Port isnt 0
  [Net::BGP] ok 3 - ASN is correct
  [Net::BGP] ok 4 - Message type is as expected
  [Net::BGP] ok 5 - BGP message type is as expected
  [Net::BGP] ok 6 - Is not an error
  [Net::BGP] ok 7 - BGP Message is proper name
  [Net::BGP] ok 8 - Message is proper type
  [Net::BGP] ok 9 - No parameters provided
  [Net::BGP] ok 10 - Keep-Alive received
  [Net::BGP] ok 11 - UD is proper name
  [Net::BGP] ok 12 - UD NLRI correct
  [Net::BGP] ok 13 - UD next-hop correct
  [Net::BGP] ok 14 - UD path correct
  [Net::BGP] ok 15 - Close message type is as expected
  [Net::BGP] ok 16 - Is not an error
  [Net::BGP] ok 17 - Peer is idle
  [Net::BGP] 1..17
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/95-bgpmon.t
  [Net::BGP] ok 1 - Speaker object defined
  [Net::BGP] ok 2 - BGP defined
  [Net::BGP] ok 3 - Display object defined
  [Net::BGP] ok 4 - Proper listen-host
  [Net::BGP] ok 5 - Proper listen-port
  [Net::BGP] ok 6 - Proper my-asn
  [Net::BGP] ok 7 - proper my-domain
  [Net::BGP] ok 8 - proper my-hostname
  [Net::BGP] ok 9 - Proper wanted CIDR (1)
  [Net::BGP] ok 10 - Proper wanted ASN (1)
  [Net::BGP] ok 11 - Proper wanted CIDR (2)
  [Net::BGP] ok 12 - Proper wanted ASN (2)
  [Net::BGP] ok 13 - Not colored (1)
  [Net::BGP] ok 14 - Not colored (2)
  [Net::BGP] ok 15 - Yes colored (1)
  [Net::BGP] ok 16 - Yes colored (2)
  [Net::BGP] ok 17 - BGP Port is 0
  [Net::BGP] ok 18 - BGP Port isnt 0
  [Net::BGP] ok 19 - ASN is correct
  [Net::BGP] ok 20 - Message type is as expected
  [Net::BGP] ok 21 - BGP message type is as expected
  [Net::BGP] ok 22 - Is not an error
  [Net::BGP] ok 23 - BGP Message is proper name
  [Net::BGP] ok 24 - Message is proper type
  [Net::BGP] ok 25 - No parameters provided
  [Net::BGP] ok 26 - Keep-Alive received
  [Net::BGP] ok 27 - UD is proper name
  [Net::BGP] ok 28 - UD NLRI correct
  [Net::BGP] ok 29 - UD next-hop correct
  [Net::BGP] ok 30 - UD path correct
  [Net::BGP] ok 31 - Close message type is as expected
  [Net::BGP] ok 32 - Is not an error
  [Net::BGP] ok 33 - Peer is idle
  [Net::BGP] 1..33
  ===> Testing [FAIL]: Net::BGP:ver<0.9.0>:auth<zef:jmaslak>
  [Net::BGP] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Net::BGP:ver<0.9.0>:auth<zef:jmaslak>
  ===> Install [OK] for Net::BGP:ver<0.9.0>:auth<zef:jmaslak>

  2 bin/ scripts [bgpmon.p6 bgpmon.rakudoc] installed to:
  /home/coke/sandbox/blin/installed/Net::BGP_zef:jmaslak_0.9.0_0/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 11min 33.091s
               CPU time consumed: 10min 16.878s
                     Memory peak: 2.4G (swap: 1G)

  ```
  </details>
* [ ] [CSS::Stylesheet](https://raku.land/zef:dwarring/CSS::Stylesheet) – Fail, Bisected: [2b05993](https://github.com/rakudo/rakudo/commit/2b05993c58a7884f262f61cb81340e5ed58381b3)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3228056-i3157134.service; invocation ID: a8de0e28b7e1427db0fd17f05136bacb
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: CSS::Stylesheet
  ===> Found: CSS::Stylesheet:ver<0.1.5>:auth<zef:dwarring> [via Zef::Repository::Ecosystems<fez>]
  [CSS::Stylesheet] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786854695.3228067.7443.951737547811/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz https://360.zef.pm/C/SS/CSS_STYLESHEET/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz
  ===> Fetching [OK]: CSS::Stylesheet:ver<0.1.5>:auth<zef:dwarring> to /home/coke/sandbox/blin/data/zef-data/tmp/1786854695.3228067.7443.951737547811/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz
  [CSS::Stylesheet] Command: tar -t -f ./d8748e8af89b419fc6af376ff4088458089fa149.tar.gz
  [CSS::Stylesheet] Command: tar -xvf ./d8748e8af89b419fc6af376ff4088458089fa149.tar.gz -C ../d8748e8af89b419fc6af376ff4088458089fa149.tar.gz
  ===> Extraction [OK]: CSS::Stylesheet to /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz
  ===> Testing: CSS::Stylesheet:ver<0.1.5>:auth<zef:dwarring>
  [CSS::Stylesheet] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz/CSS-Stylesheet-0.1.5 t/at-font-face.t
  [CSS::Stylesheet] 1..11
  [CSS::Stylesheet] ok 1 - 
  [CSS::Stylesheet] ok 2 - font face rules loaded
  [CSS::Stylesheet] ok 3 - The object is-a '"CSS::Font::Descriptor"'
  [CSS::Stylesheet] ok 4 - 
  [CSS::Stylesheet] ok 5 - 
  [CSS::Stylesheet] ok 6 - Str method
  [CSS::Stylesheet] ok 7 - # SKIP set TEST_FONT_CONFIG=1 to enable fontconfig tests
  [CSS::Stylesheet] ok 8 - # SKIP set TEST_FONT_CONFIG=1 to enable fontconfig tests
  [CSS::Stylesheet] ok 9 - # SKIP set TEST_FONT_CONFIG=1 to enable fontconfig tests
  [CSS::Stylesheet] ok 10 - # SKIP set TEST_FONT_CONFIG=1 to enable fontconfig tests
  [CSS::Stylesheet] ok 11 - # SKIP set TEST_FONT_CONFIG=1 to enable fontconfig tests
  [CSS::Stylesheet] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz/CSS-Stylesheet-0.1.5 t/at-page.t
  [CSS::Stylesheet] 1..8
  [CSS::Stylesheet] ok 1 - 
  [CSS::Stylesheet] ok 2 - 
  [CSS::Stylesheet] ok 3 - 
  [CSS::Stylesheet] ok 4 - 
  [CSS::Stylesheet] ok 5 - 
  [CSS::Stylesheet] ok 6 - 
  [CSS::Stylesheet] ok 7 - 
  [CSS::Stylesheet] ok 8 - Str method
  [CSS::Stylesheet] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz/CSS-Stylesheet-0.1.5 t/import.t
  [CSS::Stylesheet] 1..3
  [CSS::Stylesheet] ok 1 - single import
  [CSS::Stylesheet] ok 2 - uinfiltered import
  [CSS::Stylesheet] ok 3 - media-filtered import
  [CSS::Stylesheet] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz/CSS-Stylesheet-0.1.5 t/media-basic.t
  [CSS::Stylesheet] 1..22
  [CSS::Stylesheet] ok 1 - media.type
  [CSS::Stylesheet] ok 2 - media.width
  [CSS::Stylesheet] ok 3 - media.height
  [CSS::Stylesheet] ok 4 - media.resolution
  [CSS::Stylesheet] ok 5 - media.device-width
  [CSS::Stylesheet] ok 6 - media.device-height
  [CSS::Stylesheet] ok 7 - media.orientation
  [CSS::Stylesheet] ok 8 - 
  [CSS::Stylesheet] ok 9 - 
  [CSS::Stylesheet] ok 10 - 
  [CSS::Stylesheet] ok 11 - 
  [CSS::Stylesheet] ok 12 - 
  [CSS::Stylesheet] ok 13 - 
  [CSS::Stylesheet] ok 14 - 
  [CSS::Stylesheet] ok 15 - 
  [CSS::Stylesheet] ok 16 - 
  [CSS::Stylesheet] ok 17 - 
  [CSS::Stylesheet] ok 18 - 
  [CSS::Stylesheet] ok 19 - 
  [CSS::Stylesheet] ok 20 - 
  [CSS::Stylesheet] ok 21 - 
  [CSS::Stylesheet] ok 22 - 
  [CSS::Stylesheet] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz/CSS-Stylesheet-0.1.5 t/media-nested.t
  [CSS::Stylesheet] 1..1
  [CSS::Stylesheet] ok 1 - 
  [CSS::Stylesheet] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz/CSS-Stylesheet-0.1.5 t/selector-specificity.t
  [CSS::Stylesheet] ok 1 - specificity of: * (0.0.0)
  [CSS::Stylesheet] ok 2 - specificity of: LI (0.0.1)
  [CSS::Stylesheet] ok 3 - specificity of: UL LI (0.0.2)
  [CSS::Stylesheet] ok 4 - specificity of: UL OL+LI (0.0.3)
  [CSS::Stylesheet] ok 5 - specificity of: H1 + *[REL=up] (0.1.1)
  [CSS::Stylesheet] ok 6 - specificity of: UL OL LI.red (0.1.3)
  [CSS::Stylesheet] ok 7 - specificity of: LI.red.level (0.2.1)
  [CSS::Stylesheet] ok 8 - specificity of:  \#x34y (1.0.0)
  [CSS::Stylesheet] ok 9 - specificity of:  \#s12:not(FOO) (1.0.1)
  [CSS::Stylesheet] 1..9
  [CSS::Stylesheet] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz/CSS-Stylesheet-0.1.5 t/stylesheet-basic.t
  [CSS::Stylesheet] 1..8
  [CSS::Stylesheet] ok 1 - 
  [CSS::Stylesheet] ok 2 - 
  [CSS::Stylesheet] ok 3 - 
  [CSS::Stylesheet] ok 4 - 
  [CSS::Stylesheet] ok 5 - 
  [CSS::Stylesheet] ok 6 - 
  [CSS::Stylesheet] ok 7 - 
  [CSS::Stylesheet] ok 8 - :xml parse mode
  [CSS::Stylesheet] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz/CSS-Stylesheet-0.1.5 t/stylesheet-create.t
  [CSS::Stylesheet] 1..1
  [CSS::Stylesheet] ok 1 - 
  [CSS::Stylesheet] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz/CSS-Stylesheet-0.1.5 t/stylesheet-media-query.t
  [CSS::Stylesheet] 1..4
  [CSS::Stylesheet] ok 1 - no media
  [CSS::Stylesheet] ok 2 - no media selection
  [CSS::Stylesheet] ok 3 - screen media type
  [CSS::Stylesheet] ok 4 - screen media selection
  ===> Testing [OK] for CSS::Stylesheet:ver<0.1.5>:auth<zef:dwarring>
  ===> Installing: CSS::Stylesheet:ver<0.1.5>:auth<zef:dwarring>
  ===> Install [OK] for CSS::Stylesheet:ver<0.1.5>:auth<zef:dwarring>

  1 bin/ script [css-tidy.raku] installed to:
  /tmp/u6wwNKA2pm/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 7min 41.021s
               CPU time consumed: 5min 58.559s
                     Memory peak: 1.7G (swap: 699.1M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3221073-i3132535.service; invocation ID: ec2a74a5f56348959444bdead6cab678
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: CSS::Stylesheet
  ===> Found: CSS::Stylesheet:ver<0.1.5>:auth<zef:dwarring> [via Zef::Repository::Ecosystems<fez>]
  [CSS::Stylesheet] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786854482.3221080.3053.8289381651616/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz https://360.zef.pm/C/SS/CSS_STYLESHEET/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz
  ===> Fetching [OK]: CSS::Stylesheet:ver<0.1.5>:auth<zef:dwarring> to /home/coke/sandbox/blin/data/zef-data/tmp/1786854482.3221080.3053.8289381651616/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz
  [CSS::Stylesheet] Command: tar -t -f ./d8748e8af89b419fc6af376ff4088458089fa149.tar.gz
  [CSS::Stylesheet] Command: tar -xvf ./d8748e8af89b419fc6af376ff4088458089fa149.tar.gz -C ../d8748e8af89b419fc6af376ff4088458089fa149.tar.gz
  ===> Extraction [OK]: CSS::Stylesheet to /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz
  ===> Testing: CSS::Stylesheet:ver<0.1.5>:auth<zef:dwarring>
  [CSS::Stylesheet] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/d8748e8af89b419fc6af376ff4088458089fa149.tar.gz/CSS-Stylesheet-0.1.5 t/at-font-face.t
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 3min 15.880s
               CPU time consumed: 2min 30.872s
                     Memory peak: 2G (swap: 461.9M)

  ```
  </details>
* [ ] [IntlPromptYesNo](https://raku.land/github:alabamenhu/IntlPromptYesNo) – Fail, Bisected: [2b05993](https://github.com/rakudo/rakudo/commit/2b05993c58a7884f262f61cb81340e5ed58381b3)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3044969-i2992580.service; invocation ID: 45124704e1ae451194bcd51045732b48
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: IntlPromptYesNo
  ===> Found: IntlPromptYesNo:ver<0.1>:auth<github:alabamenhu> [via Zef::Repository::Ecosystems<rea>]
  [IntlPromptYesNo] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849780.3044985.5609.7630706925065/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/I/IntlPromptYesNo/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Fetching [OK]: IntlPromptYesNo:ver<0.1>:auth<github:alabamenhu> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849780.3044985.5609.7630706925065/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  [IntlPromptYesNo] Command: tar -t -f ./IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  [IntlPromptYesNo] Command: tar -xvf ./IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz -C ../IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Extraction [OK]: IntlPromptYesNo to /home/coke/sandbox/blin/data/zef-data/tmp/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Testing: IntlPromptYesNo:ver<0.1>:auth<github:alabamenhu>
  [IntlPromptYesNo] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz/IntlPromptYesNo-main t/00-sanity.rakutest
  [IntlPromptYesNo] ⎡ The module Intl::UserLanguage has been renamed to User::Language. ⎤
  [IntlPromptYesNo] ⎢ Please use this name in the future. If you received this message  ⎥
  [IntlPromptYesNo] ⎢ without having explicitly used the module, please contact the     ⎥
  [IntlPromptYesNo] ⎢ author whose module called this to have them update accordingly.  ⎥
  [IntlPromptYesNo] ⎢                                                                   ⎥
  [IntlPromptYesNo] ⎢ Please be aware that fallback languages are not supported when    ⎥
  [IntlPromptYesNo] ⎢ calling by the old name for compile time reasons                  ⎥
  [IntlPromptYesNo] ⎢                                                                   ⎥
  [IntlPromptYesNo] ⎢ You may dismiss this by setting the environment variable          ⎥
  [IntlPromptYesNo] ⎢ RAKU_USER_LANGUAGE_NAMECHANGE_WARNING to OFF. Updates after 2024  ⎥
  [IntlPromptYesNo] ⎣ will no longer provide under the old name.                        ⎦
  [IntlPromptYesNo] 1..0
  [IntlPromptYesNo] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz/IntlPromptYesNo-main t/01-input.rakutest
  [IntlPromptYesNo] 1..0
  ===> Testing [OK] for IntlPromptYesNo:ver<0.1>:auth<github:alabamenhu>
  ===> Installing: IntlPromptYesNo:ver<0.1>:auth<github:alabamenhu>
  ===> Install [OK] for IntlPromptYesNo:ver<0.1>:auth<github:alabamenhu>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 5min 37.458s
               CPU time consumed: 5min 42.088s
                     Memory peak: 2.9G (swap: 387.2M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3037860-i3017826.service; invocation ID: 5a575be38067445090f50178660d3a82
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: IntlPromptYesNo
  ===> Found: IntlPromptYesNo:ver<0.1>:auth<github:alabamenhu> [via Zef::Repository::Ecosystems<rea>]
  [IntlPromptYesNo] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849564.3037867.8125.000382530901/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/I/IntlPromptYesNo/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Fetching [OK]: IntlPromptYesNo:ver<0.1>:auth<github:alabamenhu> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849564.3037867.8125.000382530901/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  [IntlPromptYesNo] Command: tar -t -f ./IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  [IntlPromptYesNo] Command: tar -xvf ./IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz -C ../IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Extraction [OK]: IntlPromptYesNo to /home/coke/sandbox/blin/data/zef-data/tmp/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Testing: IntlPromptYesNo:ver<0.1>:auth<github:alabamenhu>
  [IntlPromptYesNo] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/IntlPromptYesNo%3Aver%3C0.1%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz/IntlPromptYesNo-main t/00-sanity.rakutest
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 3min 30.130s
               CPU time consumed: 2min 43.513s
                     Memory peak: 2.5G (swap: 656.3M)

  ```
  </details>
* [ ] [Resend](https://raku.land/zef:khalidelborai/Resend) – Fail, Bisected: [2b05993](https://github.com/rakudo/rakudo/commit/2b05993c58a7884f262f61cb81340e5ed58381b3)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3031591-i2903683.service; invocation ID: d6fdb99adbe3425e963f4d17831a8f90
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Resend
  ===> Found: Resend:ver<0.0.6>:auth<zef:khalidelborai> [via Zef::Repository::Ecosystems<fez>]
  [Resend] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849397.3031597.1798.679912400729/aacdc7b56a410af9889bfdac83561369168f0138.tar.gz https://360.zef.pm/R/ES/RESEND/aacdc7b56a410af9889bfdac83561369168f0138.tar.gz
  ===> Fetching [OK]: Resend:ver<0.0.6>:auth<zef:khalidelborai> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849397.3031597.1798.679912400729/aacdc7b56a410af9889bfdac83561369168f0138.tar.gz
  [Resend] Command: tar -t -f ./aacdc7b56a410af9889bfdac83561369168f0138.tar.gz
  [Resend] Command: tar -xvf ./aacdc7b56a410af9889bfdac83561369168f0138.tar.gz -C ../aacdc7b56a410af9889bfdac83561369168f0138.tar.gz
  ===> Extraction [OK]: Resend to /home/coke/sandbox/blin/data/zef-data/tmp/aacdc7b56a410af9889bfdac83561369168f0138.tar.gz
  ===> Testing: Resend:ver<0.0.6>:auth<zef:khalidelborai>
  [Resend] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/aacdc7b56a410af9889bfdac83561369168f0138.tar.gz/Resend-0.0.6 t/01-basic.rakutest
  [Resend] ok 1 - replace me
  [Resend] 1..1
  ===> Testing [OK] for Resend:ver<0.0.6>:auth<zef:khalidelborai>
  ===> Installing: Resend:ver<0.0.6>:auth<zef:khalidelborai>
  ===> Install [OK] for Resend:ver<0.0.6>:auth<zef:khalidelborai>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 6min 21.222s
               CPU time consumed: 5min 19.702s
                     Memory peak: 2.1G (swap: 777.5M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3024156-i3041275.service; invocation ID: e7ece7bfac024738880d5e504108f9b0
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Resend
  ===> Found: Resend:ver<0.0.6>:auth<zef:khalidelborai> [via Zef::Repository::Ecosystems<fez>]
  [Resend] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849174.3024157.8070.171214117636/aacdc7b56a410af9889bfdac83561369168f0138.tar.gz https://360.zef.pm/R/ES/RESEND/aacdc7b56a410af9889bfdac83561369168f0138.tar.gz
  ===> Fetching [OK]: Resend:ver<0.0.6>:auth<zef:khalidelborai> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849174.3024157.8070.171214117636/aacdc7b56a410af9889bfdac83561369168f0138.tar.gz
  [Resend] Command: tar -t -f ./aacdc7b56a410af9889bfdac83561369168f0138.tar.gz
  [Resend] Command: tar -xvf ./aacdc7b56a410af9889bfdac83561369168f0138.tar.gz -C ../aacdc7b56a410af9889bfdac83561369168f0138.tar.gz
  ===> Extraction [OK]: Resend to /home/coke/sandbox/blin/data/zef-data/tmp/aacdc7b56a410af9889bfdac83561369168f0138.tar.gz
  ===> Testing: Resend:ver<0.0.6>:auth<zef:khalidelborai>
  [Resend] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/aacdc7b56a410af9889bfdac83561369168f0138.tar.gz/Resend-0.0.6 t/01-basic.rakutest
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 3min 54.603s
               CPU time consumed: 2min 35.903s
                     Memory peak: 1.8G (swap: 885.9M)

  ```
  </details>
* [ ] [Debugging::Tool](https://raku.land/zef:lucs/Debugging::Tool) – Fail, Bisected: [1a08ca7](https://github.com/rakudo/rakudo/commit/1a08ca762010ff035c3ee106c842464a68d301e6)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3037926-i3069401.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Debugging::Tool
  ===> Found: Debugging::Tool:ver<0.3.1>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [Debugging::Tool] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849556.3037930.9506.184316290768/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz https://360.zef.pm/D/EB/DEBUGGING_TOOL/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  ===> Fetching [OK]: Debugging::Tool:ver<0.3.1>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849556.3037930.9506.184316290768/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  [Debugging::Tool] Command: tar -t -f ./e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  [Debugging::Tool] Command: tar -xvf ./e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz -C ../e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  ===> Extraction [OK]: Debugging::Tool to /home/coke/sandbox/blin/data/zef-data/tmp/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  ===> Testing: Debugging::Tool:ver<0.3.1>:auth<zef:lucs>
  [Debugging::Tool] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz t/all.rakutest
  [Debugging::Tool]    # p1
  [Debugging::Tool] ok 1 - Expected OUT
  [Debugging::Tool] ok 2 - Expected ERR
  [Debugging::Tool]    # p2
  [Debugging::Tool] ok 3 - Expected OUT
  [Debugging::Tool] ok 4 - Expected ERR
  [Debugging::Tool]    # p3
  [Debugging::Tool] ok 5 - Expected OUT
  [Debugging::Tool] ok 6 - Expected ERR
  [Debugging::Tool]    # p4
  [Debugging::Tool] ok 7 - Expected OUT
  [Debugging::Tool] ok 8 - Expected ERR
  [Debugging::Tool]    # p5
  [Debugging::Tool] ok 9 - Expected OUT
  [Debugging::Tool] ok 10 - Expected ERR
  [Debugging::Tool]    # p6
  [Debugging::Tool] ok 11 - Expected OUT
  [Debugging::Tool] ok 12 - Expected ERR
  [Debugging::Tool]    # p7
  [Debugging::Tool] ok 13 - Expected OUT
  [Debugging::Tool] ok 14 - Expected ERR
  [Debugging::Tool]    # p8
  [Debugging::Tool] ok 15 - Expected OUT
  [Debugging::Tool] ok 16 - Expected ERR
  [Debugging::Tool]    # pa
  [Debugging::Tool] ok 17 - Expected OUT
  [Debugging::Tool] ok 18 - Expected ERR
  [Debugging::Tool]    # pb
  [Debugging::Tool] ok 19 - Expected OUT
  [Debugging::Tool] ok 20 - Expected ERR
  [Debugging::Tool]    # pc
  [Debugging::Tool] ok 21 - Expected OUT
  [Debugging::Tool] ok 22 - Expected ERR
  [Debugging::Tool]    # pd
  [Debugging::Tool] ok 23 - Expected OUT
  [Debugging::Tool] ok 24 - Expected ERR
  [Debugging::Tool]    # pe
  [Debugging::Tool] ok 25 - Expected OUT
  [Debugging::Tool] ok 26 - Expected ERR
  [Debugging::Tool]    # pf
  [Debugging::Tool] ok 27 - Expected OUT
  [Debugging::Tool] ok 28 - Expected ERR
  [Debugging::Tool]    # pg
  [Debugging::Tool] ok 29 - Expected OUT
  [Debugging::Tool] ok 30 - Expected ERR
  [Debugging::Tool]    # ph
  [Debugging::Tool] ok 31 - Expected OUT
  [Debugging::Tool] ok 32 - Expected ERR
  [Debugging::Tool]    # s1
  [Debugging::Tool] ok 33 - Expected OUT
  [Debugging::Tool] ok 34 - Expected ERR
  [Debugging::Tool]    # s2
  [Debugging::Tool] ok 35 - Expected OUT
  [Debugging::Tool] ok 36 - Expected ERR
  [Debugging::Tool]    # s3
  [Debugging::Tool] ok 37 - Expected OUT
  [Debugging::Tool] ok 38 - Expected ERR
  [Debugging::Tool]    # s4
  [Debugging::Tool] ok 39 - Expected OUT
  [Debugging::Tool] ok 40 - Expected ERR
  [Debugging::Tool]    # s5
  [Debugging::Tool] ok 41 - Expected OUT
  [Debugging::Tool] ok 42 - Expected ERR
  [Debugging::Tool]    # s6
  [Debugging::Tool] ok 43 - Expected OUT
  [Debugging::Tool] ok 44 - Expected ERR
  [Debugging::Tool]    # s7
  [Debugging::Tool] ok 45 - Expected OUT
  [Debugging::Tool] ok 46 - Expected ERR
  [Debugging::Tool]    # s8
  [Debugging::Tool] ok 47 - Expected OUT
  [Debugging::Tool] ok 48 - Expected ERR
  [Debugging::Tool]    # sa
  [Debugging::Tool] ok 49 - Expected OUT
  [Debugging::Tool] ok 50 - Expected ERR
  [Debugging::Tool]    # sb
  [Debugging::Tool] ok 51 - Expected OUT
  [Debugging::Tool] ok 52 - Expected ERR
  [Debugging::Tool]    # sc
  [Debugging::Tool] ok 53 - Expected OUT
  [Debugging::Tool] ok 54 - Expected ERR
  [Debugging::Tool]    # sd
  [Debugging::Tool] ok 55 - Expected OUT
  [Debugging::Tool] ok 56 - Expected ERR
  [Debugging::Tool]    # se
  [Debugging::Tool] ok 57 - Expected OUT
  [Debugging::Tool] ok 58 - Expected ERR
  [Debugging::Tool]    # sf
  [Debugging::Tool] ok 59 - Expected OUT
  [Debugging::Tool] ok 60 - Expected ERR
  [Debugging::Tool]    # sg
  [Debugging::Tool] ok 61 - Expected OUT
  [Debugging::Tool] ok 62 - Expected ERR
  [Debugging::Tool]    # sh
  [Debugging::Tool] ok 63 - Expected OUT
  [Debugging::Tool] ok 64 - Expected ERR
  [Debugging::Tool]    # t2
  [Debugging::Tool] ok 65 - Expected OUT
  [Debugging::Tool] ok 66 - Expected ERR
  [Debugging::Tool] ok 67 - 
  [Debugging::Tool]    # t3
  [Debugging::Tool] ok 68 - Expected OUT
  [Debugging::Tool] ok 69 - Expected ERR
  [Debugging::Tool]    # t5
  [Debugging::Tool] ok 70 - Expected OUT
  [Debugging::Tool] ok 71 - Expected ERR
  [Debugging::Tool]    # t6
  [Debugging::Tool] ok 72 - Expected OUT
  [Debugging::Tool] ok 73 - Expected ERR
  [Debugging::Tool]    # t7
  [Debugging::Tool] ok 74 - Expected OUT
  [Debugging::Tool] ok 75 - Expected ERR
  [Debugging::Tool]    # t8
  [Debugging::Tool] ok 76 - Expected OUT
  [Debugging::Tool] ok 77 - Expected ERR
  [Debugging::Tool]    # t9
  [Debugging::Tool] ok 78 - Expected OUT
  [Debugging::Tool] ok 79 - Expected ERR
  [Debugging::Tool]    # ta
  [Debugging::Tool] ok 80 - Expected OUT
  [Debugging::Tool] ok 81 - Expected ERR
  [Debugging::Tool]    # tb
  [Debugging::Tool] ok 82 - Expected OUT
  [Debugging::Tool] ok 83 - Expected ERR
  [Debugging::Tool]    # tc
  [Debugging::Tool] ok 84 - Expected OUT
  [Debugging::Tool] ok 85 - Expected ERR
  [Debugging::Tool]    # td
  [Debugging::Tool] ok 86 - Expected OUT
  [Debugging::Tool] ok 87 - Expected ERR
  [Debugging::Tool]    # te
  [Debugging::Tool] ok 88 - Expected OUT
  [Debugging::Tool] ok 89 - Expected ERR
  [Debugging::Tool] 1..89
  ===> Testing [OK] for Debugging::Tool:ver<0.3.1>:auth<zef:lucs>
  ===> Installing: Debugging::Tool:ver<0.3.1>:auth<zef:lucs>
  ===> Install [OK] for Debugging::Tool:ver<0.3.1>:auth<zef:lucs>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 4min 39.850s
               CPU time consumed: 3min 54.200s
                     Memory peak: 1006.1M (swap: 358.7M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3033564-i3057195.service; invocation ID: fe9eee77dff04f7eac5118b75abd9432
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Debugging::Tool
  ===> Found: Debugging::Tool:ver<0.3.1>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [Debugging::Tool] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849425.3033571.3197.7449870646446/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz https://360.zef.pm/D/EB/DEBUGGING_TOOL/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  ===> Fetching [OK]: Debugging::Tool:ver<0.3.1>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849425.3033571.3197.7449870646446/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  [Debugging::Tool] Command: tar -t -f ./e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  [Debugging::Tool] Command: tar -xvf ./e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz -C ../e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  ===> Extraction [OK]: Debugging::Tool to /home/coke/sandbox/blin/data/zef-data/tmp/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  ===> Testing: Debugging::Tool:ver<0.3.1>:auth<zef:lucs>
  [Debugging::Tool] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz t/all.rakutest
  [Debugging::Tool] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz/t/all.rakutest
  [Debugging::Tool] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Test::Selector_zef:lucs_0.4.1_0/sources/24399444270EBDCCD786B361A1F0AEB4FE3383FD (Test::Selector)
  [Debugging::Tool] No unspace allowed in regex; if you meant to match the literal
  [Debugging::Tool] character, please enclose in single quotes (' ') or use a backslashed
  [Debugging::Tool] form like \x20.
  [Debugging::Tool] at /home/coke/sandbox/blin/installed/Test::Selector_zef:lucs_0.4.1_0/sources/24399444270EBDCCD786B361A1F0AEB4FE3383FD (Test::Selector):614
  [Debugging::Tool] ------>                     / ^ \s* ok \ <HERE>/ ||
  [Debugging::Tool] at /home/coke/sandbox/blin/data/zef-data/tmp/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz/t/all.rakutest:2
  ===> Testing [FAIL]: Debugging::Tool:ver<0.3.1>:auth<zef:lucs>
  [Debugging::Tool] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Debugging::Tool:ver<0.3.1>:auth<zef:lucs>
  ===> Install [OK] for Debugging::Tool:ver<0.3.1>:auth<zef:lucs>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 53.083s
               CPU time consumed: 1min 56.502s
                     Memory peak: 1.2G (swap: 114M)

  ```
  </details>
* [ ] [File::TreeBuilder](https://raku.land/zef:lucs/File::TreeBuilder) – Fail, Bisected: [1a08ca7](https://github.com/rakudo/rakudo/commit/1a08ca762010ff035c3ee106c842464a68d301e6)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3037214-i2952532.service; invocation ID: 98b555b6a59e4482a19152d963f4c65f
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: File::TreeBuilder
  ===> Found: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [File::TreeBuilder] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849540.3037215.3537.3337533298886/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz https://360.zef.pm/F/IL/FILE_TREEBUILDER/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  ===> Fetching [OK]: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849540.3037215.3537.3337533298886/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  [File::TreeBuilder] Command: tar -t -f ./29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  [File::TreeBuilder] Command: tar -xvf ./29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz -C ../29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  ===> Extraction [OK]: File::TreeBuilder to /home/coke/sandbox/blin/data/zef-data/tmp/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  ===> Testing: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs>
  [File::TreeBuilder] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz t/main.rakutest
  [File::TreeBuilder]    # bd1
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]     1..2
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MalformedLine)
  [File::TreeBuilder] ok 1 - did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]    # bd2
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]     1..2
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MalformedLine)
  [File::TreeBuilder] ok 2 - did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]    # bd3
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]     1..2
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MalformedLine)
  [File::TreeBuilder] ok 3 - did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]    # bd4
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]     1..2
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MalformedLine)
  [File::TreeBuilder] ok 4 - did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]    # bd5
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]     1..2
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MalformedLine)
  [File::TreeBuilder] ok 5 - did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]    # bd6
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]     1..2
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MalformedLine)
  [File::TreeBuilder] ok 6 - did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]    # bd7
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]     1..2
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MalformedLine)
  [File::TreeBuilder] ok 7 - did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]    # bd8
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]     1..2
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MalformedLine)
  [File::TreeBuilder] ok 8 - did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]    # gd1
  [File::TreeBuilder] ok 9 - Expecting lead length '2'.
  [File::TreeBuilder] ok 10 - Expecting node name 'foo'.
  [File::TreeBuilder]    # gd2
  [File::TreeBuilder] ok 11 - Expecting lead length '0'.
  [File::TreeBuilder] ok 12 - Expecting node name 'foo'.
  [File::TreeBuilder]    # gd3
  [File::TreeBuilder] ok 13 - Expecting lead length '2'.
  [File::TreeBuilder] ok 14 - Expecting node name 'foo'.
  [File::TreeBuilder]    # gd4
  [File::TreeBuilder] ok 15 - Expecting lead length '0'.
  [File::TreeBuilder] ok 16 - Expecting node name 'f b'.
  [File::TreeBuilder]    # gd5
  [File::TreeBuilder] ok 17 - Expecting lead length '0'.
  [File::TreeBuilder] ok 18 - Expecting node name 'foo'.
  [File::TreeBuilder]    # gd6
  [File::TreeBuilder] ok 19 - Expecting lead length '0'.
  [File::TreeBuilder] ok 20 - Expecting node name 'foo'.
  [File::TreeBuilder] ok 21 - Expecting text 'txt'.
  [File::TreeBuilder]    # gd7
  [File::TreeBuilder] ok 22 - Expecting lead length '0'.
  [File::TreeBuilder] ok 23 - Expecting node name 'foo'.
  [File::TreeBuilder] ok 24 - Expecting hkey 'a-'key'.
  [File::TreeBuilder]    # gd8
  [File::TreeBuilder] ok 25 - Expecting lead length '0'.
  [File::TreeBuilder] ok 26 - Expecting node name 'foo'.
  [File::TreeBuilder] ok 27 - Expecting perm '644'.
  [File::TreeBuilder]    # gd9
  [File::TreeBuilder] ok 28 - Expecting lead length '0'.
  [File::TreeBuilder] ok 29 - Expecting node name 'f b'.
  [File::TreeBuilder] ok 30 - Expecting perm '345'.
  [File::TreeBuilder]    # gdA
  [File::TreeBuilder] ok 31 - Expecting lead length '0'.
  [File::TreeBuilder] ok 32 - Expecting node name 'f b'.
  [File::TreeBuilder] ok 33 - Expecting perm '222'.
  [File::TreeBuilder]    # gdB
  [File::TreeBuilder] ok 34 - Expecting lead length '0'.
  [File::TreeBuilder] ok 35 - Expecting node name 'f b'.
  [File::TreeBuilder] ok 36 - Expecting perm '222'.
  [File::TreeBuilder]    # gdC
  [File::TreeBuilder] ok 37 - Expecting lead length '0'.
  [File::TreeBuilder] ok 38 - Expecting node name 'foo'.
  [File::TreeBuilder] ok 39 - Expecting hkey 's!+à'.
  [File::TreeBuilder]    # bf1
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::NoFileDataHash?
  [File::TreeBuilder]     1..3
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::NoFileDataHash)
  [File::TreeBuilder]     ok 3 - .line-num matches 1
  [File::TreeBuilder] ok 40 - did we throws-like File::TreeBuilder::NodeX::NoFileDataHash?
  [File::TreeBuilder]    # bf2
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MissingFileData?
  [File::TreeBuilder]     1..3
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MissingFileData)
  [File::TreeBuilder]     ok 3 - .line-num matches 1
  [File::TreeBuilder] ok 41 - did we throws-like File::TreeBuilder::NodeX::MissingFileData?
  [File::TreeBuilder]    # bf2a
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]     1..3
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MalformedLine)
  [File::TreeBuilder]     ok 3 - .line-num matches 2
  [File::TreeBuilder] ok 42 - did we throws-like File::TreeBuilder::NodeX::MalformedLine?
  [File::TreeBuilder]    # bf3
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::MissingFileData?
  [File::TreeBuilder]     1..3
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::MissingFileData)
  [File::TreeBuilder]     ok 3 - .line-num matches 3
  [File::TreeBuilder] ok 43 - did we throws-like File::TreeBuilder::NodeX::MissingFileData?
  [File::TreeBuilder]    # bf4
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::InvalidIndent?
  [File::TreeBuilder]     1..3
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::InvalidIndent)
  [File::TreeBuilder]     ok 3 - .line-num matches 3
  [File::TreeBuilder] ok 44 - did we throws-like File::TreeBuilder::NodeX::InvalidIndent?
  [File::TreeBuilder]    # bf5
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::InvalidIndent?
  [File::TreeBuilder]     1..3
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::InvalidIndent)
  [File::TreeBuilder]     ok 3 - .line-num matches 3
  [File::TreeBuilder] ok 45 - did we throws-like File::TreeBuilder::NodeX::InvalidIndent?
  [File::TreeBuilder]    # bf6
  [File::TreeBuilder] # Subtest: did we throws-like File::TreeBuilder::NodeX::InvalidIndent?
  [File::TreeBuilder]     1..3
  [File::TreeBuilder]     ok 1 - code dies
  [File::TreeBuilder]     ok 2 - right exception type (File::TreeBuilder::NodeX::InvalidIndent)
  [File::TreeBuilder]     ok 3 - .line-num matches 7
  [File::TreeBuilder] ok 46 - did we throws-like File::TreeBuilder::NodeX::InvalidIndent?
  [File::TreeBuilder]    # ab1
  [File::TreeBuilder] ok 47 - Expecting file 'f1'.
  [File::TreeBuilder] ok 48 - Expecting directory 'foo'.
  [File::TreeBuilder] ok 49 - Expecting file 'foo/bar'.
  [File::TreeBuilder] ok 50 - Expecting to skip ' \# a blank line'.
  [File::TreeBuilder] ok 51 - Expecting directory 'foo/baz'.
  [File::TreeBuilder] ok 52 - Expecting correct mode.
  [File::TreeBuilder] ok 53 - Expecting to skip ' \# a comment'.
  [File::TreeBuilder] ok 54 - Expecting directory 'foo/baz/dd'.
  [File::TreeBuilder] ok 55 - Expecting file 'foo/baz/dd/fff'.
  [File::TreeBuilder] ok 56 - Expecting correct mode.
  [File::TreeBuilder] ok 57 - Expecting directory 'foo/ggg'.
  [File::TreeBuilder] ok 58 - Expecting file 'foo/hhh'.
  [File::TreeBuilder] ok 59 - Expecting file 'mlerp'.
  [File::TreeBuilder] 1..59
  ===> Testing [OK] for File::TreeBuilder:ver<0.2.0>:auth<zef:lucs>
  ===> Installing: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs>
  ===> Install [OK] for File::TreeBuilder:ver<0.2.0>:auth<zef:lucs>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 32.337s
               CPU time consumed: 2min 15.861s
                     Memory peak: 980.3M (swap: 204M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3032823-i3060487.service; invocation ID: b9d08234d0be40b3b7d295d18681d9b8
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: File::TreeBuilder
  ===> Found: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [File::TreeBuilder] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849408.3032824.5390.664044090754/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz https://360.zef.pm/F/IL/FILE_TREEBUILDER/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  ===> Fetching [OK]: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849408.3032824.5390.664044090754/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  [File::TreeBuilder] Command: tar -t -f ./29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  [File::TreeBuilder] Command: tar -xvf ./29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz -C ../29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  ===> Extraction [OK]: File::TreeBuilder to /home/coke/sandbox/blin/data/zef-data/tmp/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  ===> Testing: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs>
  [File::TreeBuilder] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz t/main.rakutest
  [File::TreeBuilder] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz/t/main.rakutest
  [File::TreeBuilder] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Test::Selector_zef:lucs_0.4.1_0/sources/24399444270EBDCCD786B361A1F0AEB4FE3383FD (Test::Selector)
  [File::TreeBuilder] No unspace allowed in regex; if you meant to match the literal
  [File::TreeBuilder] character, please enclose in single quotes (' ') or use a backslashed
  [File::TreeBuilder] form like \x20.
  [File::TreeBuilder] at /home/coke/sandbox/blin/installed/Test::Selector_zef:lucs_0.4.1_0/sources/24399444270EBDCCD786B361A1F0AEB4FE3383FD (Test::Selector):614
  [File::TreeBuilder] ------>                     / ^ \s* ok \ <HERE>/ ||
  [File::TreeBuilder] at /home/coke/sandbox/blin/data/zef-data/tmp/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz/t/main.rakutest:2
  ===> Testing [FAIL]: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs>
  [File::TreeBuilder] Failed to get passing tests, but continuing with --force-test
  ===> Installing: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs>
  ===> Install [OK] for File::TreeBuilder:ver<0.2.0>:auth<zef:lucs>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 54.473s
               CPU time consumed: 1min 58.891s
                     Memory peak: 1.2G (swap: 185.6M)

  ```
  </details>
* [ ] [MIDI::Make](https://raku.land/zef:pelevesque/MIDI::Make) – Fail, Bisected: [1a08ca7](https://github.com/rakudo/rakudo/commit/1a08ca762010ff035c3ee106c842464a68d301e6)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3037470-i3069388.service; invocation ID: d3cd8031b5114efebb77475d1a2bb2da
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: MIDI::Make
  ===> Found: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0> [via Zef::Repository::Ecosystems<fez>]
  [MIDI::Make] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849545.3037474.7803.300271716579/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz https://360.zef.pm/M/ID/MIDI_MAKE/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  ===> Fetching [OK]: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849545.3037474.7803.300271716579/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  [MIDI::Make] Command: tar -t -f ./b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  [MIDI::Make] Command: tar -xvf ./b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz -C ../b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  ===> Extraction [OK]: MIDI::Make to /home/coke/sandbox/blin/data/zef-data/tmp/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  ===> Testing: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0>
  [MIDI::Make] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz t/all.rakutest
  [MIDI::Make]    # s1
  [MIDI::Make] ok 1 - Trackless Song Instantiation
  [MIDI::Make]    # s2
  [MIDI::Make] ok 2 - Trackless Song Instantiation: format => 0
  [MIDI::Make]    # s3
  [MIDI::Make] ok 3 - Trackless Song Instantiation: time-division => "frame"
  [MIDI::Make]    # s4
  [MIDI::Make] ok 4 - Trackless Song Instantiation: PPQ => 300
  [MIDI::Make]    # s5
  [MIDI::Make] ok 5 - Trackless Song Instantiation: FPS => 29.97
  [MIDI::Make]    # s6
  [MIDI::Make] ok 6 - Trackless Song Instantiation: PPF => 8
  [MIDI::Make]    # s7
  [MIDI::Make] ok 7 - Trackless Song: Set params after instantiation A
  [MIDI::Make]    # s8
  [MIDI::Make] ok 8 - Trackless Song: Set params after instantiation B
  [MIDI::Make]    # t1
  [MIDI::Make] ok 9 - Track Instantiation
  [MIDI::Make]    # t2
  [MIDI::Make] ok 10 - Track Instantiation: copyright => "c 2022 anonymous"
  [MIDI::Make]    # t3
  [MIDI::Make] ok 11 - Track Instantiation: name => "melody"
  [MIDI::Make]    # t4
  [MIDI::Make] ok 12 - Track Instantiation: delta-time => 100
  [MIDI::Make]    # t5
  [MIDI::Make] ok 13 - Track Instantiation: channel => 1
  [MIDI::Make]    # t6
  [MIDI::Make] ok 14 - Track Instantiation: velocity-off => 10
  [MIDI::Make]    # t7
  [MIDI::Make] ok 15 - Track Instantiation: velocity-on => 100
  [MIDI::Make]    # t8
  [MIDI::Make] ok 16 - Track: Change params after instantiation
  [MIDI::Make]    # t9
  [MIDI::Make] ok 17 - Track: copyright
  [MIDI::Make]    # t10
  [MIDI::Make] ok 18 - Track: copyright with ignored delta-time
  [MIDI::Make]    # t11
  [MIDI::Make] ok 19 - Track: name
  [MIDI::Make]    # t12
  [MIDI::Make] ok 20 - Track: name with ignored delta-time
  [MIDI::Make]    # t13
  [MIDI::Make] ok 21 - Track: instrument
  [MIDI::Make]    # t14
  [MIDI::Make] ok 22 - Track: text
  [MIDI::Make]    # t15
  [MIDI::Make] ok 23 - Track: lyric
  [MIDI::Make]    # t16
  [MIDI::Make] ok 24 - Track: marker
  [MIDI::Make]    # t17
  [MIDI::Make] ok 25 - Track: cue
  [MIDI::Make]    # t18
  [MIDI::Make] ok 26 - Track: program-name
  [MIDI::Make]    # t19
  [MIDI::Make] ok 27 - Track: port
  [MIDI::Make]    # t20
  [MIDI::Make] ok 28 - Track: tempo with default params
  [MIDI::Make]    # t21
  [MIDI::Make] ok 29 - Track: tempo with custom params
  [MIDI::Make]    # t22
  [MIDI::Make] ok 30 - Track: time-signature with default params
  [MIDI::Make]    # t23
  [MIDI::Make] ok 31 - Track: time-signature with custom params
  [MIDI::Make]    # t24
  [MIDI::Make] ok 32 - Track: key-signature
  [MIDI::Make]    # t25
  [MIDI::Make] ok 33 - Track: key-signature using ♭/♯ postfix for accidentals
  [MIDI::Make]    # t26
  [MIDI::Make] ok 34 - Track: key-signature using Modes enums
  [MIDI::Make]    # t27
  [MIDI::Make] ok 35 - Track: note-on and note-off
  [MIDI::Make]    # t28
  [MIDI::Make] ok 36 - Track: note aftertouch
  [MIDI::Make]    # t29
  [MIDI::Make] ok 37 - Track: channel aftertouch
  [MIDI::Make]    # t30
  [MIDI::Make] ok 38 - Track: controller
  [MIDI::Make]    # t31
  [MIDI::Make] ok 39 - Track: controller shortcuts
  [MIDI::Make]    # t32
  [MIDI::Make] ok 40 - Track: controller shortcuts (combined)
  [MIDI::Make]    # t33
  [MIDI::Make] ok 41 - Track: program-change
  [MIDI::Make]    # t34
  [MIDI::Make] ok 42 - Track: pitch-bend with default param, on channel 1
  [MIDI::Make]    # t35
  [MIDI::Make] ok 43 - Track: pitch-bend => none
  [MIDI::Make]    # t36
  [MIDI::Make] ok 44 - Track: pitch-bend => lowest
  [MIDI::Make]    # t37
  [MIDI::Make] ok 45 - Track: pitch-bend => highest
  [MIDI::Make]    # t38
  [MIDI::Make] ok 46 - Track: pitch-bend => 10000
  [MIDI::Make]    # t39
  [MIDI::Make] ok 47 - Track: sysex
  [MIDI::Make]    # t40
  [MIDI::Make] ok 48 - Track: add-bytes
  [MIDI::Make]    # t41
  [MIDI::Make] ok 49 - Track: delta-time remains intact after render
  [MIDI::Make]    # e1
  [MIDI::Make] ok 50 - Everything
  [MIDI::Make] 1..50
  ===> Testing [OK] for MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0>
  ===> Installing: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0>
  ===> Install [OK] for MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 34.744s
               CPU time consumed: 2min 14.243s
                     Memory peak: 1012.6M (swap: 264.5M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3033275-i3060494.service; invocation ID: ba96cf976e1f448c9c748e81f6735c68
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: MIDI::Make
  ===> Found: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0> [via Zef::Repository::Ecosystems<fez>]
  [MIDI::Make] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786849415.3033279.3471.6057492178597/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz https://360.zef.pm/M/ID/MIDI_MAKE/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  ===> Fetching [OK]: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0> to /home/coke/sandbox/blin/data/zef-data/tmp/1786849415.3033279.3471.6057492178597/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  [MIDI::Make] Command: tar -t -f ./b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  [MIDI::Make] Command: tar -xvf ./b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz -C ../b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  ===> Extraction [OK]: MIDI::Make to /home/coke/sandbox/blin/data/zef-data/tmp/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  ===> Testing: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0>
  [MIDI::Make] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz t/all.rakutest
  [MIDI::Make] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz/t/all.rakutest
  [MIDI::Make] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Test::Selector_zef:lucs_0.4.1_0/sources/24399444270EBDCCD786B361A1F0AEB4FE3383FD (Test::Selector)
  [MIDI::Make] No unspace allowed in regex; if you meant to match the literal
  [MIDI::Make] character, please enclose in single quotes (' ') or use a backslashed
  [MIDI::Make] form like \x20.
  [MIDI::Make] at /home/coke/sandbox/blin/installed/Test::Selector_zef:lucs_0.4.1_0/sources/24399444270EBDCCD786B361A1F0AEB4FE3383FD (Test::Selector):614
  [MIDI::Make] ------>                     / ^ \s* ok \ <HERE>/ ||
  [MIDI::Make] at /home/coke/sandbox/blin/data/zef-data/tmp/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz/t/all.rakutest:2
  ===> Testing [FAIL]: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0>
  [MIDI::Make] Failed to get passing tests, but continuing with --force-test
  ===> Installing: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0>
  ===> Install [OK] for MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 48.821s
               CPU time consumed: 1min 55.117s
                     Memory peak: 1.3G (swap: 98M)

  ```
  </details>
* [ ] [Test::Selector](https://raku.land/zef:lucs/Test::Selector) – Fail, Bisected: [1a08ca7](https://github.com/rakudo/rakudo/commit/1a08ca762010ff035c3ee106c842464a68d301e6)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2939717-i2911628.service; invocation ID: a262f78606534181ae0723dbc9a11195
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Test::Selector
  ===> Found: Test::Selector:ver<0.4.1>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [Test::Selector] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786846974.2939718.8813.177547768862/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz https://360.zef.pm/T/ES/TEST_SELECTOR/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  ===> Fetching [OK]: Test::Selector:ver<0.4.1>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1786846974.2939718.8813.177547768862/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  [Test::Selector] Command: tar -t -f ./6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  [Test::Selector] Command: tar -xvf ./6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz -C ../6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  ===> Extraction [OK]: Test::Selector to /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  ===> Testing: Test::Selector:ver<0.4.1>:auth<zef:lucs>
  [Test::Selector] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz t/all.rakutest
  [Test::Selector] ok 1 - Test::Selector module can be use-d ok
  [Test::Selector] ok 2 - t_ignore-test Out okay.
  [Test::Selector] ok 3 - t_ignore-test Err okay.
  [Test::Selector] ok 4 - t_glob_prob Out okay.
  [Test::Selector] ok 5 - t_glob_prob Err okay.
  [Test::Selector] ok 6 - t_char-range Out okay.
  [Test::Selector] ok 7 - t_char-range Err okay.
  [Test::Selector] ok 8 - t_diff-sub-name Out okay.
  [Test::Selector] ok 9 - t_diff-sub-name Err okay.
  [Test::Selector] ok 10 - t_skip-non-match Out okay.
  [Test::Selector] ok 11 - t_skip-non-match Err okay.
  [Test::Selector] ok 12 - t_one-test Out okay.
  [Test::Selector] ok 13 - t_one-test Err okay.
  [Test::Selector] ok 14 - t_var-test-id Out okay.
  [Test::Selector] ok 15 - t_var-test-id Err okay.
  [Test::Selector] ok 16 - t_match-all Out okay.
  [Test::Selector] ok 17 - t_match-all Err okay.
  [Test::Selector] ok 18 - t_matchall_dflt Out okay.
  [Test::Selector] ok 19 - t_matchall_dflt Err okay.
  [Test::Selector] ok 20 - t_no-match Out okay.
  [Test::Selector] ok 21 - t_no-match Err okay.
  [Test::Selector] ok 22 - t_list Out okay.
  [Test::Selector] ok 23 - t_list Err okay.
  [Test::Selector] ok 24 - t_list-subset1 Out okay.
  [Test::Selector] ok 25 - t_list-subset1 Err okay.
  [Test::Selector] ok 26 - t_list-subset2 Out okay.
  [Test::Selector] ok 27 - t_list-subset2 Err okay.
  [Test::Selector] ok 28 - t_list-subset3 Out okay.
  [Test::Selector] ok 29 - t_list-subset3 Err okay.
  [Test::Selector] ok 30 - t_see-label Out okay.
  [Test::Selector] ok 31 - t_see-label Err okay.
  [Test::Selector] ok 32 - t_diff-sub-name2 Out okay.
  [Test::Selector] ok 33 - t_diff-sub-name2 Err okay.
  [Test::Selector] ok 34 - t_diff-sub-name3 Out okay.
  [Test::Selector] ok 35 - t_diff-sub-name3 Err okay.
  [Test::Selector] ok 36 - t_list-subset4 Out okay.
  [Test::Selector] ok 37 - t_list-subset4 Err okay.
  [Test::Selector] ok 38 - t_run-subset Out okay.
  [Test::Selector] ok 39 - t_run-subset Err okay.
  [Test::Selector] ok 40 - t_bad_action Out okay.
  [Test::Selector] ok 41 - t_bad_action Err okay.
  [Test::Selector] 1..41
  ===> Testing [OK] for Test::Selector:ver<0.4.1>:auth<zef:lucs>
  ===> Installing: Test::Selector:ver<0.4.1>:auth<zef:lucs>
  ===> Install [OK] for Test::Selector:ver<0.4.1>:auth<zef:lucs>

  1 bin/ script [tsel] installed to:
  /tmp/J784QtC15N/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 50.178s
               CPU time consumed: 2min 48.151s
                     Memory peak: 1.3G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2930972-i2893461.service; invocation ID: 675287879f3c4d7199226d58119741b8
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Test::Selector
  ===> Found: Test::Selector:ver<0.4.1>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [Test::Selector] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1786846765.2930976.1062.545371666419/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz https://360.zef.pm/T/ES/TEST_SELECTOR/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  ===> Fetching [OK]: Test::Selector:ver<0.4.1>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1786846765.2930976.1062.545371666419/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  [Test::Selector] Command: tar -t -f ./6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  [Test::Selector] Command: tar -xvf ./6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz -C ../6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  ===> Extraction [OK]: Test::Selector to /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  ===> Testing: Test::Selector:ver<0.4.1>:auth<zef:lucs>
  [Test::Selector] Command: /tmp/whateverable/rakudo-moar/2b05993c58a7884f262f61cb81340e5ed58381b3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz t/all.rakutest
  [Test::Selector] not ok 1 - Test::Selector module can be use-d ok
  [Test::Selector] # Failed test 'Test::Selector module can be use-d ok'
  [Test::Selector] # at t/all.rakutest line 4
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] not ok 2 - t_ignore-test Out okay.
  [Test::Selector] # Failed test 't_ignore-test Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 3 - t_ignore-test Err okay.
  [Test::Selector] # Failed test 't_ignore-test Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/2FHSq4adtz
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/2FHSq4adtz:3'
  [Test::Selector] not ok 4 - t_glob_prob Out okay.
  [Test::Selector] # Failed test 't_glob_prob Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # aa11a
  [Test::Selector] # ok 1 - 11
  [Test::Selector] #    # ab22a
  [Test::Selector] # ok 2 - 22
  [Test::Selector] #    # aa33a
  [Test::Selector] # ok 3 - 33
  [Test::Selector] #    # ad44a
  [Test::Selector] # ok 4 - 44
  [Test::Selector] # 1..4'
  [Test::Selector] #      got: ''
  [Test::Selector] # Failed test 't_glob_prob Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] not ok 5 - t_glob_prob Err okay.
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/0vbkgtfPSP
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/0vbkgtfPSP:3'
  [Test::Selector] not ok 6 - t_char-range Out okay.
  [Test::Selector] # Failed test 't_char-range Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # N1d
  [Test::Selector] #    # N1b
  [Test::Selector] #    # N1ba
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 7 - t_char-range Err okay.
  [Test::Selector] # Failed test 't_char-range Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/2EIeJbVwCn
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/2EIeJbVwCn:3'
  [Test::Selector] not ok 8 - t_diff-sub-name Out okay.
  [Test::Selector] # Failed test 't_diff-sub-name Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a1
  [Test::Selector] # ok 1 - 42 is true.
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 9 - t_diff-sub-name Err okay.
  [Test::Selector] # Failed test 't_diff-sub-name Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/tGWCAJHGKJ
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/tGWCAJHGKJ:3'
  [Test::Selector] not ok 10 - t_skip-non-match Out okay.
  [Test::Selector] # Failed test 't_skip-non-match Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 11 - t_skip-non-match Err okay.
  [Test::Selector] # Failed test 't_skip-non-match Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/H2mWVYbGPc
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/H2mWVYbGPc:3'
  [Test::Selector] not ok 12 - t_one-test Out okay.
  [Test::Selector] # Failed test 't_one-test Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a3
  [Test::Selector] # ok 1 - 42 is true.
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 13 - t_one-test Err okay.
  [Test::Selector] # Failed test 't_one-test Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/CvzZut0a8r
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/CvzZut0a8r:3'
  [Test::Selector] not ok 14 - t_var-test-id Out okay.
  [Test::Selector] not ok 15 - t_var-test-id Err okay.
  [Test::Selector] # Failed test 't_var-test-id Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a3b
  [Test::Selector] # ok 1 - 42 is true.
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] # Failed test 't_var-test-id Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/KeYjmGhoHO
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/KeYjmGhoHO:3'
  [Test::Selector] not ok 16 - t_match-all Out okay.
  [Test::Selector] # Failed test 't_match-all Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a4
  [Test::Selector] # ok 1 - 42 is true.
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 17 - t_match-all Err okay.
  [Test::Selector] # Failed test 't_match-all Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/IhX4bhLstS
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/IhX4bhLstS:3'
  [Test::Selector] not ok 18 - t_matchall_dflt Out okay.
  [Test::Selector] # Failed test 't_matchall_dflt Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a5
  [Test::Selector] # ok 1 - 42 is true.
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 19 - t_matchall_dflt Err okay.
  [Test::Selector] # Failed test 't_matchall_dflt Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/BNtk5ClI7_
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/BNtk5ClI7_:3'
  [Test::Selector] not ok 20 - t_no-match Out okay.
  [Test::Selector] # Failed test 't_no-match Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 21 - t_no-match Err okay.
  [Test::Selector] # Failed test 't_no-match Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/c_86mptMhr
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/c_86mptMhr:3'
  [Test::Selector] not ok 22 - t_list Out okay.
  [Test::Selector] not ok 23 - t_list Err okay.
  [Test::Selector] # Failed test 't_list Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: 'a7
  [Test::Selector] # b1
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] # Failed test 't_list Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/cYRqe8rYR1
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/cYRqe8rYR1:3'
  [Test::Selector] not ok 24 - t_list-subset1 Out okay.
  [Test::Selector] # Failed test 't_list-subset1 Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: 'b2
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 25 - t_list-subset1 Err okay.
  [Test::Selector] # Failed test 't_list-subset1 Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/pTxWwVtNbH
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/pTxWwVtNbH:3'
  [Test::Selector] not ok 26 - t_list-subset2 Out okay.
  [Test::Selector] # Failed test 't_list-subset2 Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: 'b3
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] # Failed test 't_list-subset2 Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] not ok 27 - t_list-subset2 Err okay.
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/_ZjT5ke1QA
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/_ZjT5ke1QA:3'
  [Test::Selector] not ok 28 - t_list-subset3 Out okay.
  [Test::Selector] # Failed test 't_list-subset3 Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: 'b3b
  [Test::Selector] # b5b
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] # Failed test 't_list-subset3 Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] not ok 29 - t_list-subset3 Err okay.
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/zr_zDSuUNS
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/zr_zDSuUNS:3'
  [Test::Selector] not ok 30 - t_see-label Out okay.
  [Test::Selector] # Failed test 't_see-label Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a10
  [Test::Selector] # ok 1 - Test ID is 'a10'.
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 31 - t_see-label Err okay.
  [Test::Selector] # Failed test 't_see-label Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/NbIu6MRHez
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/NbIu6MRHez:3'
  [Test::Selector] not ok 32 - t_diff-sub-name2 Out okay.
  [Test::Selector] # Failed test 't_diff-sub-name2 Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a11
  [Test::Selector] # ok 1 - foo
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 33 - t_diff-sub-name2 Err okay.
  [Test::Selector] # Failed test 't_diff-sub-name2 Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/6Q1p9E6WYp
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/6Q1p9E6WYp:3'
  [Test::Selector] not ok 34 - t_diff-sub-name3 Out okay.
  [Test::Selector] # Failed test 't_diff-sub-name3 Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a12a
  [Test::Selector] # ok 1 - t
  [Test::Selector] #    # a12b
  [Test::Selector] # ok 2 - foo
  [Test::Selector] #    # a12c
  [Test::Selector] # ok 3 - bar
  [Test::Selector] # 1..3'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 35 - t_diff-sub-name3 Err okay.
  [Test::Selector] # Failed test 't_diff-sub-name3 Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/o4T_wV0UDV
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/o4T_wV0UDV:3'
  [Test::Selector] not ok 36 - t_list-subset4 Out okay.
  [Test::Selector] # Failed test 't_list-subset4 Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: 'a1
  [Test::Selector] # __a2
  [Test::Selector] # _a3
  [Test::Selector] # a4
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 37 - t_list-subset4 Err okay.
  [Test::Selector] # Failed test 't_list-subset4 Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/XIPUGvnsWt
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/XIPUGvnsWt:3'
  [Test::Selector] not ok 38 - t_run-subset Out okay.
  [Test::Selector] # Failed test 't_run-subset Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a1
  [Test::Selector] #    # _a3 : skipped
  [Test::Selector] #    # a4
  [Test::Selector] # ok 1 - Four
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] # Failed test 't_run-subset Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] not ok 39 - t_run-subset Err okay.
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/1U6D1FELo2
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/1U6D1FELo2:3'
  [Test::Selector] not ok 40 - t_bad_action Out okay.
  [Test::Selector] # Failed test 't_bad_action Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 41 - t_bad_action Err okay.
  [Test::Selector] # Failed test 't_bad_action Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: 'Moo'
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/xnAyGuwe3H
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/xnAyGuwe3H:3'
  [Test::Selector] 1..41
  [Test::Selector] # You failed 41 tests of 41
  ===> Testing [FAIL]: Test::Selector:ver<0.4.1>:auth<zef:lucs>
  [Test::Selector] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Test::Selector:ver<0.4.1>:auth<zef:lucs>
  ===> Install [OK] for Test::Selector:ver<0.4.1>:auth<zef:lucs>

  1 bin/ script [tsel] installed to:
  /home/coke/sandbox/blin/installed/Test::Selector_zef:lucs_0.4.1_0/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 3min 14.554s
               CPU time consumed: 3min 20.287s
                     Memory peak: 1.3G (swap: 277.9M)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| UnhandledException        |     1 | [Foo:: Foo](https://raku.land/github:AlexDaniel/Foo:: Foo) |
| Flapper                   |     1 | [Test::Time](https://raku.land/zef:FCO/Test::Time) |
| Fail                      |     9 | [CSS::Stylesheet](https://raku.land/zef:dwarring/CSS::Stylesheet) [Cro::FCGI](https://raku.land/zef:patrickb/Cro::FCGI) [Debugging::Tool](https://raku.land/zef:lucs/Debugging::Tool) [File::TreeBuilder](https://raku.land/zef:lucs/File::TreeBuilder) [IntlPromptYesNo](https://raku.land/github:alabamenhu/IntlPromptYesNo) [MIDI::Make](https://raku.land/zef:pelevesque/MIDI::Make) [Net::BGP](https://raku.land/zef:jmaslak/Net::BGP) [Resend](https://raku.land/zef:khalidelborai/Resend) [Test::Selector](https://raku.land/zef:lucs/Test::Selector) |
| InstallableButUntested    |     9 | [HTTP::Server::Async](https://raku.land/zef:raku-community-modules/HTTP::Server::Async) [IO::Socket::Async::SSL](https://raku.land/zef:raku-community-modules/IO::Socket::Async::SSL) [IRC::Client](https://raku.land/zef:lizmat/IRC::Client) [Log::Minimal](https://raku.land//Log::Minimal) [Russian](https://raku.land/zef:slavenskoj/Russian) [Time::Duration](https://raku.land/zef:masukomi/Time::Duration) [Toaster](https://raku.land//Toaster) [Uzu](https://raku.land/cpan:SACOMO/Uzu) [Web::Scraper](https://raku.land/zef:tony-o/Web::Scraper) |
| MissingDependency         |    11 | [App::Ebread](https://raku.land/zef:samy/App::Ebread) [App::Perl6LangServer](https://raku.land/cpan:AZAWAWI/App::Perl6LangServer) [Chemistry::Elements](https://raku.land/github:briandfoy/Chemistry::Elements) [DBIx::NamedQueries](https://raku.land/cpan:MZIESCHA/DBIx::NamedQueries) [Ethelia](https://raku.land/zef:knarkhov/Ethelia) [Learn::Raku::With](https://raku.land/zef:codesections/Learn::Raku::With) [META6::To::Man](https://raku.land/cpan:TBROWDER/META6::To::Man) [Pakku](https://raku.land/zef:hythm/Pakku) [Perl6::Tracer](https://raku.land/github:jaffa4/Perl6::Tracer) [Task::Galaxy](https://raku.land//Task::Galaxy) [Touch](https://raku.land/zef:rir/Touch) |
| ZefFailure                |    11 | [BDD::Behave](https://raku.land/zef:gdonald/BDD::Behave) [Concurrent::BoundedChannel](https://raku.land/zef:raku-community-modules/Concurrent::BoundedChannel) [Cro::RPC::JSON](https://raku.land/zef:vrurg/Cro::RPC::JSON) [Gnome::Gtk4](https://raku.land/zef:martimm/Gnome::Gtk4) [JSON::Stream](https://raku.land//JSON::Stream) [ParaSeq](https://raku.land/zef:lizmat/ParaSeq) [Proc::ZMQed](https://raku.land/zef:antononcube/Proc::ZMQed) [TXN](https://raku.land//TXN) [TXN::Parser](https://raku.land//TXN::Parser) [TXN::Remarshal](https://raku.land//TXN::Remarshal) [cro](https://raku.land/zef:cro/cro) |
| CyclicDependency          |    46 | ⋯                         |
| AlwaysFail                |   728 | ⋯                         |
| OK                        |  1693 | ⋯                         |



This run started on 2026-08-16T05:12:24Z and finished in ≈4 hours.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
