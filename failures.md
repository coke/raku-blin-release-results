[Blin](https://github.com/Raku/Blin) results between 2026.08 ([24e6e53](https://github.com/rakudo/rakudo/commit/24e6e5312f2868680413b0597aef8772f6b5bcea)) and HEAD ([fdc7d63](https://github.com/rakudo/rakudo/commit/fdc7d635717d90c06826668936cd708d30fd19c4)):

* [ ] [Text::Markdown::Discount](https://raku.land/github:hartenfels/Text::Markdown::Discount) – Fail, Bisected: [a0a60ed](https://github.com/rakudo/rakudo/commit/a0a60ed3ce28e6e014bf287101a6d454e364aeaa)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p142375-i181374.service; invocation ID: 510df13df6a741b58de5cb9f04e643ac
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Text::Markdown::Discount
  ===> Found: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels> [via Zef::Repository::Ecosystems<rea>]
  [Text::Markdown::Discount] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788469107.142376.6883.408485756529/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/T/Text%3A%3AMarkdown%3A%3ADiscount/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Fetching [OK]: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels> to /home/coke/sandbox/blin/data/zef-data/tmp/1788469107.142376.6883.408485756529/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  [Text::Markdown::Discount] Command: tar -t -f ./Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  [Text::Markdown::Discount] Command: tar -xvf ./Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz -C ../Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Extraction [OK]: Text::Markdown::Discount to /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Testing: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/01_lib.t
  [Text::Markdown::Discount] # markdown_version: NativeCall::Types::Pointer[int8]<5084448664096>
  [Text::Markdown::Discount] ok 1 - libmarkdown is installed
  [Text::Markdown::Discount] 1..1
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/02_make-flags.t
  [Text::Markdown::Discount] ok 1 - no flags
  [Text::Markdown::Discount] ok 2 - single positive flag is set
  [Text::Markdown::Discount] ok 3 - single negated positive flag is unset
  [Text::Markdown::Discount] ok 4 - single negative flag is unset
  [Text::Markdown::Discount] ok 5 - single negated negative flag is set
  [Text::Markdown::Discount] ok 6 - single negative flag with no is set
  [Text::Markdown::Discount] ok 7 - single negated negative flag with no is unset
  [Text::Markdown::Discount] ok 8 - multiple non-zero flags get ORed together
  [Text::Markdown::Discount] ok 9 - case and actual value of flags does not matter
  [Text::Markdown::Discount] # Subtest: single nonexistent flag dies
  [Text::Markdown::Discount]     1..2
  [Text::Markdown::Discount]     ok 1 - code dies
  [Text::Markdown::Discount]     ok 2 - right exception type (Text::Markdown::Discount::X::Text::Markdown::Discount::Flag)
  [Text::Markdown::Discount] ok 10 - single nonexistent flag dies
  [Text::Markdown::Discount] # Subtest: nonexistent flag amongst real flag dies
  [Text::Markdown::Discount]     1..2
  [Text::Markdown::Discount]     ok 1 - code dies
  [Text::Markdown::Discount]     ok 2 - right exception type (Text::Markdown::Discount::X::Text::Markdown::Discount::Flag)
  [Text::Markdown::Discount] ok 11 - nonexistent flag amongst real flag dies
  [Text::Markdown::Discount] 1..11
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/03_interna.t
  [Text::Markdown::Discount] ok 1 - string gets parsed
  [Text::Markdown::Discount] ok 2 - ...conversion to string works
  [Text::Markdown::Discount] ok 3 - ...writing to file works
  [Text::Markdown::Discount] ok 4 - file gets parsed
  [Text::Markdown::Discount] ok 5 - ...conversion to string works
  [Text::Markdown::Discount] ok 6 - ...writing to file works
  [Text::Markdown::Discount] ok 7 - from string with flags ()
  [Text::Markdown::Discount] ok 8 - from file with flags ()
  [Text::Markdown::Discount] ok 9 - from string with flags (nolinks)
  [Text::Markdown::Discount] ok 10 - from file with flags (nolinks)
  [Text::Markdown::Discount] ok 11 - from string with flags (nohtml)
  [Text::Markdown::Discount] ok 12 - from file with flags (nohtml)
  [Text::Markdown::Discount] ok 13 - from string with flags (nolinks nohtml)
  [Text::Markdown::Discount] ok 14 - from file with flags (nolinks nohtml)
  [Text::Markdown::Discount] # Subtest: sourcing from nonexistent file fails
  [Text::Markdown::Discount]     1..2
  [Text::Markdown::Discount]     ok 1 - code dies
  [Text::Markdown::Discount]     ok 2 - right exception type (Text::Markdown::Discount::X::Text::Markdown::Discount::File)
  [Text::Markdown::Discount] ok 15 - sourcing from nonexistent file fails
  [Text::Markdown::Discount] 1..15
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/04_markdown.t
  [Text::Markdown::Discount] ok 1 - string to string
  [Text::Markdown::Discount] ok 2 - file to string
  [Text::Markdown::Discount] ok 3 - string to file
  [Text::Markdown::Discount] ok 4 - file to file
  [Text::Markdown::Discount] ok 5 - HTML conversion ()
  [Text::Markdown::Discount] ok 6 - HTML conversion (nolinks)
  [Text::Markdown::Discount] ok 7 - HTML conversion (nohtml)
  [Text::Markdown::Discount] ok 8 - HTML conversion (nolinks nohtml)
  [Text::Markdown::Discount] 1..8
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/05_dump.t
  [Text::Markdown::Discount] ok 1 - LINKS IMAGE
  [Text::Markdown::Discount] ok 2 - !LINKS IMAGE
  [Text::Markdown::Discount] ok 3 - LINKS !IMAGE
  [Text::Markdown::Discount] ok 4 - !LINKS !IMAGE
  [Text::Markdown::Discount] 1..4
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/06_headers.t
  [Text::Markdown::Discount] ok 1 - 
  [Text::Markdown::Discount] ok 2 - 
  [Text::Markdown::Discount] ok 3 - 
  [Text::Markdown::Discount] ok 4 - 
  [Text::Markdown::Discount] ok 5 - 
  [Text::Markdown::Discount] ok 6 - 
  [Text::Markdown::Discount] ok 7 - 
  [Text::Markdown::Discount] ok 8 - 
  [Text::Markdown::Discount] 1..8
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/07_meta.t
  [Text::Markdown::Discount] 1..1
  [Text::Markdown::Discount] ok 1 - # SKIP Skipping author test
  ===> Testing [OK] for Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  ===> Installing: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  ===> Install [OK] for Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 59.718s
               CPU time consumed: 2min 6.030s
                     Memory peak: 1.2G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p137835-i160872.service; invocation ID: dd8ce439bfd84bc2b301e12450ecd9d7
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Text::Markdown::Discount
  ===> Found: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels> [via Zef::Repository::Ecosystems<rea>]
  [Text::Markdown::Discount] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788468983.137837.5453.053435453218/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/T/Text%3A%3AMarkdown%3A%3ADiscount/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Fetching [OK]: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels> to /home/coke/sandbox/blin/data/zef-data/tmp/1788468983.137837.5453.053435453218/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  [Text::Markdown::Discount] Command: tar -t -f ./Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  [Text::Markdown::Discount] Command: tar -xvf ./Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz -C ../Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Extraction [OK]: Text::Markdown::Discount to /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Testing: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/01_lib.t
  [Text::Markdown::Discount] # markdown_version: NativeCall::Types::Pointer[int8]<2279788912192>
  [Text::Markdown::Discount] ok 1 - libmarkdown is installed
  [Text::Markdown::Discount] 1..1
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/02_make-flags.t
  [Text::Markdown::Discount] ok 1 - no flags
  [Text::Markdown::Discount] ok 2 - single positive flag is set
  [Text::Markdown::Discount] ok 3 - single negated positive flag is unset
  [Text::Markdown::Discount] ok 4 - single negative flag is unset
  [Text::Markdown::Discount] ok 5 - single negated negative flag is set
  [Text::Markdown::Discount] ok 6 - single negative flag with no is set
  [Text::Markdown::Discount] ok 7 - single negated negative flag with no is unset
  [Text::Markdown::Discount] ok 8 - multiple non-zero flags get ORed together
  [Text::Markdown::Discount] ok 9 - case and actual value of flags does not matter
  [Text::Markdown::Discount] # Subtest: single nonexistent flag dies
  [Text::Markdown::Discount]     1..2
  [Text::Markdown::Discount]     ok 1 - code dies
  [Text::Markdown::Discount]     ok 2 - right exception type (Text::Markdown::Discount::X::Text::Markdown::Discount::Flag)
  [Text::Markdown::Discount] ok 10 - single nonexistent flag dies
  [Text::Markdown::Discount] # Subtest: nonexistent flag amongst real flag dies
  [Text::Markdown::Discount]     1..2
  [Text::Markdown::Discount]     ok 1 - code dies
  [Text::Markdown::Discount]     ok 2 - right exception type (Text::Markdown::Discount::X::Text::Markdown::Discount::Flag)
  [Text::Markdown::Discount] ok 11 - nonexistent flag amongst real flag dies
  [Text::Markdown::Discount] 1..11
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/03_interna.t
  [Text::Markdown::Discount] ok 1 - string gets parsed
  [Text::Markdown::Discount] ok 2 - ...conversion to string works
  [Text::Markdown::Discount] ok 3 - ...writing to file works
  [Text::Markdown::Discount] ok 4 - file gets parsed
  [Text::Markdown::Discount] ok 5 - ...conversion to string works
  [Text::Markdown::Discount] ok 6 - ...writing to file works
  [Text::Markdown::Discount] ok 7 - from string with flags ()
  [Text::Markdown::Discount] ok 8 - from file with flags ()
  [Text::Markdown::Discount] ok 9 - from string with flags (nolinks)
  [Text::Markdown::Discount] ok 10 - from file with flags (nolinks)
  [Text::Markdown::Discount] ok 11 - from string with flags (nohtml)
  [Text::Markdown::Discount] ok 12 - from file with flags (nohtml)
  [Text::Markdown::Discount] ok 13 - from string with flags (nohtml nolinks)
  [Text::Markdown::Discount] ok 14 - from file with flags (nohtml nolinks)
  [Text::Markdown::Discount] # Subtest: sourcing from nonexistent file fails
  [Text::Markdown::Discount]     1..2
  [Text::Markdown::Discount]     ok 1 - code dies
  [Text::Markdown::Discount]     ok 2 - right exception type (Text::Markdown::Discount::X::Text::Markdown::Discount::File)
  [Text::Markdown::Discount] ok 15 - sourcing from nonexistent file fails
  [Text::Markdown::Discount] 1..15
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/04_markdown.t
  [Text::Markdown::Discount] ok 1 - string to string
  [Text::Markdown::Discount] ok 2 - file to string
  [Text::Markdown::Discount] ok 3 - string to file
  [Text::Markdown::Discount] ok 4 - file to file
  [Text::Markdown::Discount] ok 5 - HTML conversion ()
  [Text::Markdown::Discount] ok 6 - HTML conversion (nolinks)
  [Text::Markdown::Discount] ok 7 - HTML conversion (nohtml)
  [Text::Markdown::Discount] ok 8 - HTML conversion (nolinks nohtml)
  [Text::Markdown::Discount] 1..8
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/05_dump.t
  [Text::Markdown::Discount] ok 1 - LINKS IMAGE
  [Text::Markdown::Discount] ok 2 - !LINKS IMAGE
  [Text::Markdown::Discount] ok 3 - LINKS !IMAGE
  [Text::Markdown::Discount] ok 4 - !LINKS !IMAGE
  [Text::Markdown::Discount] 1..4
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/06_headers.t
  [Text::Markdown::Discount] ok 1 - 
  [Text::Markdown::Discount] ok 2 - 
  [Text::Markdown::Discount] ok 3 - 
  [Text::Markdown::Discount] ok 4 - 
  [Text::Markdown::Discount] ok 5 - 
  [Text::Markdown::Discount] ok 6 - 
  [Text::Markdown::Discount] ok 7 - 
  [Text::Markdown::Discount] ok 8 - 
  [Text::Markdown::Discount] 1..8
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/07_meta.t
  [Text::Markdown::Discount] 1..1
  [Text::Markdown::Discount] ok 1 - # SKIP Skipping author test
  ===> Testing [FAIL]: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  [Text::Markdown::Discount] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  ===> Install [OK] for Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 58.873s
               CPU time consumed: 2min 1.351s
                     Memory peak: 1.4G (swap: 0B)

  ```
  </details>
* [ ] [Uni63](https://raku.land//Uni63) – Fail, Bisected: [d2e7633](https://github.com/rakudo/rakudo/commit/d2e76337e8551531cf2275cbc3e61c49a4014bd1)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p149621-i64993.service; invocation ID: 985e4765eced4a1990d2793f5a2c7be8
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Uni63
  ===> Found: Uni63:ver<0.2.0> [via Zef::Repository::Ecosystems<rea>]
  [Uni63] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788469309.149624.3983.585032029913/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/U/Uni63/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz
  ===> Fetching [OK]: Uni63:ver<0.2.0> to /home/coke/sandbox/blin/data/zef-data/tmp/1788469309.149624.3983.585032029913/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz
  [Uni63] Command: tar -t -f ./Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz
  [Uni63] Command: tar -xvf ./Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz -C ../Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz
  ===> Extraction [OK]: Uni63 to /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz
  ===> Testing: Uni63:ver<0.2.0>
  [Uni63] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master t/01-sanity.t
  [Uni63] 1..5
  [Uni63] ok 1 - encode Leberkäse
  [Uni63] ok 2 - count escapes
  [Uni63] ok 3 - decode Leberk_23Gse
  [Uni63] ok 4 - round trip Shakespeare
  [Uni63] ok 5 - iterated round trip
  [Uni63] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master t/02-null.t
  [Uni63] 1..4
  [Uni63] ok 1 - encode NUL
  [Uni63] ok 2 - decode encoded NUL
  [Uni63] ok 3 - round trip NUL
  [Uni63] ok 4 - round trip encoded NUL
  [Uni63] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master t/03-crlf.t
  [Uni63] 1..4
  [Uni63] ok 1 - encode CRLF
  [Uni63] ok 2 - decode encoded CRLF
  [Uni63] ok 3 - round trip CRLF
  [Uni63] ok 4 - round trip encoded CRLF
  ===> Testing [OK] for Uni63:ver<0.2.0>
  ===> Installing: Uni63:ver<0.2.0>
  ===> Install [OK] for Uni63:ver<0.2.0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 54.683s
               CPU time consumed: 1min 57.287s
                     Memory peak: 1.4G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p145643-i15083.service; invocation ID: a685562a093544ff9ad688064a0d857d
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Uni63
  ===> Found: Uni63:ver<0.2.0> [via Zef::Repository::Ecosystems<rea>]
  [Uni63] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788469193.145644.2481.3192898811476/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/U/Uni63/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz
  ===> Fetching [OK]: Uni63:ver<0.2.0> to /home/coke/sandbox/blin/data/zef-data/tmp/1788469193.145644.2481.3192898811476/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz
  [Uni63] Command: tar -t -f ./Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz
  [Uni63] Command: tar -xvf ./Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz -C ../Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz
  ===> Extraction [OK]: Uni63 to /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz
  ===> Testing: Uni63:ver<0.2.0>
  [Uni63] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master t/01-sanity.t
  [Uni63] 1..5
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] not ok 1 - encode Leberkäse
  [Uni63] # Failed test 'encode Leberkäse'
  [Uni63] # at t/01-sanity.t line 13
  [Uni63] not ok 2 - count escapes
  [Uni63] # Failed test 'count escapes'
  [Uni63] # at t/01-sanity.t line 14
  [Uni63] not ok 3 - decode 
  [Uni63] # Failed test 'decode '
  [Uni63] # at t/01-sanity.t line 17
  [Uni63] # expected: 'Leberkäse'
  [Uni63] #      got: ''
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] not ok 4 - round trip Shakespeare
  [Uni63] # Failed test 'round trip Shakespeare'
  [Uni63] # at t/01-sanity.t line 27
  [Uni63] # expected: 'Over hill, over dale,
  [Uni63] # Thorough bush, thorough brier,
  [Uni63] # Over park, over pale,
  [Uni63] # Thorough flood, thorough fire,
  [Uni63] # I do wander everywhere.
  [Uni63] # '
  [Uni63] #      got: ''
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] not ok 5 - iterated round trip
  [Uni63] # Failed test 'iterated round trip'
  [Uni63] # at t/01-sanity.t line 28
  [Uni63] # expected: 'Over hill, over dale,
  [Uni63] # Thorough bush, thorough brier,
  [Uni63] # Over park, over pale,
  [Uni63] # Thorough flood, thorough fire,
  [Uni63] # I do wander everywhere.
  [Uni63] # '
  [Uni63] #      got: ''
  [Uni63] # You failed 5 tests of 5
  [Uni63] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master t/02-null.t
  [Uni63] 1..4
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] not ok 1 - encode NUL
  [Uni63] # Failed test 'encode NUL'
  [Uni63] # at t/02-null.t line 10
  [Uni63] # expected: '_0'
  [Uni63] #      got: ''
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 44
  [Uni63] not ok 2 - decode encoded NUL
  [Uni63] # Failed test 'decode encoded NUL'
  [Uni63] # at t/02-null.t line 11
  [Uni63] # expected: ' '
  [Uni63] #      got: ''
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] not ok 3 - round trip NUL
  [Uni63] # Failed test 'round trip NUL'
  [Uni63] # at t/02-null.t line 12
  [Uni63] # expected: ' '
  [Uni63] #      got: ''
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 44
  [Uni63] not ok 4 - round trip encoded NUL
  [Uni63] # Failed test 'round trip encoded NUL'
  [Uni63] # at t/02-null.t line 13
  [Uni63] # expected: '_0'
  [Uni63] #      got: ''
  [Uni63] # You failed 4 tests of 4
  [Uni63] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master t/03-crlf.t
  [Uni63] 1..4
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] not ok 1 - encode CRLF
  [Uni63] # Failed test 'encode CRLF'
  [Uni63] # at t/03-crlf.t line 10
  [Uni63] # expected: '_1d_1a'
  [Uni63] #      got: ''
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 44
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 44
  [Uni63] # Failed test 'decode encoded CRLF'
  [Uni63] # at t/03-crlf.t line 11
  [Uni63] not ok 2 - decode encoded CRLF
  [Uni63] # expected: "\r\n"
  [Uni63] #      got: ""
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 35
  [Uni63] not ok 3 - round trip CRLF
  [Uni63] # Failed test 'round trip CRLF'
  [Uni63] # at t/03-crlf.t line 12
  [Uni63] # expected: "\r\n"
  [Uni63] #      got: ""
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 44
  [Uni63] Use of uninitialized value element of type Any in string context.
  [Uni63] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Uni63]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/Uni63%3Aver%3C0.2.0%3E%3Aauth%3Cgithub%3Acygx%3E.tar.gz/p6-uni63-master/lib/Uni63.pm6 (Uni63) line 44
  [Uni63] not ok 4 - round trip encoded CRLF
  [Uni63] # Failed test 'round trip encoded CRLF'
  [Uni63] # at t/03-crlf.t line 13
  [Uni63] # expected: '_1d_1a'
  [Uni63] #      got: ''
  [Uni63] # You failed 4 tests of 4
  ===> Testing [FAIL]: Uni63:ver<0.2.0>
  [Uni63] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Uni63:ver<0.2.0>
  ===> Install [OK] for Uni63:ver<0.2.0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 51.566s
               CPU time consumed: 1min 54.500s
                     Memory peak: 1.3G (swap: 0B)

  ```
  </details>
* [ ] [Sitemap](https://raku.land/zef:sasha/Sitemap) – Fail, Bisected: [00ccf31](https://github.com/rakudo/rakudo/commit/00ccf31f6078091762e1071c2bcd8fcb07ca9a7d)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p541192-i445736.service; invocation ID: 20e3a18867b74fe8ae46617d6bfca23e
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Sitemap
  ===> Found: Sitemap:ver<0.0.1>:auth<zef:sasha> [via Zef::Repository::Ecosystems<fez>]
  [Sitemap] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788479235.541194.4498.566970820146/af1773e4378f172b4c420c4738db2912543073e5.tar.gz https://360.zef.pm/S/IT/SITEMAP/af1773e4378f172b4c420c4738db2912543073e5.tar.gz
  ===> Fetching [OK]: Sitemap:ver<0.0.1>:auth<zef:sasha> to /home/coke/sandbox/blin/data/zef-data/tmp/1788479235.541194.4498.566970820146/af1773e4378f172b4c420c4738db2912543073e5.tar.gz
  [Sitemap] Command: tar -t -f ./af1773e4378f172b4c420c4738db2912543073e5.tar.gz
  [Sitemap] Command: tar -xvf ./af1773e4378f172b4c420c4738db2912543073e5.tar.gz -C ../af1773e4378f172b4c420c4738db2912543073e5.tar.gz
  ===> Extraction [OK]: Sitemap to /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz
  ===> Testing: Sitemap:ver<0.0.1>:auth<zef:sasha>
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/01-item.rakutest
  [Sitemap] 1..23
  [Sitemap] # Subtest: Sitemap::Item - basic creation
  [Sitemap]     ok 1 - URL set correctly
  [Sitemap]     ok 2 - Priority set correctly
  [Sitemap]     ok 3 - lastmod not set
  [Sitemap]     ok 4 - changefreq not set
  [Sitemap]     1..4
  [Sitemap] ok 1 - Sitemap::Item - basic creation
  [Sitemap] # Subtest: Sitemap::Item - URL encoding
  [Sitemap]     ok 1 - URL is encoded
  [Sitemap]     1..1
  [Sitemap] ok 2 - Sitemap::Item - URL encoding
  [Sitemap] # Subtest: Sitemap::Item - URL normalization preserves port and userinfo
  [Sitemap]     ok 1 - Scheme/host lowercased, port and path preserved
  [Sitemap]     ok 2 - Userinfo case preserved, host lowercased
  [Sitemap]     ok 3 - Bare host unchanged
  [Sitemap]     1..3
  [Sitemap] ok 3 - Sitemap::Item - URL normalization preserves port and userinfo
  [Sitemap] # Subtest: Sitemap::Item - add-image
  [Sitemap]     ok 1 - Image added
  [Sitemap]     ok 2 - Image URL correct
  [Sitemap]     ok 3 - Image caption correct
  [Sitemap]     1..3
  [Sitemap] ok 4 - Sitemap::Item - add-image
  [Sitemap] # Subtest: Sitemap::Item - add-video
  [Sitemap]     ok 1 - Video added
  [Sitemap]     ok 2 - Content URL correct
  [Sitemap]     ok 3 - Thumbnail correct
  [Sitemap]     ok 4 - Title correct
  [Sitemap]     1..4
  [Sitemap] ok 5 - Sitemap::Item - add-video
  [Sitemap] # Subtest: Sitemap::Item - add-link
  [Sitemap]     ok 1 - Link added
  [Sitemap]     ok 2 - Link URL correct
  [Sitemap]     1..2
  [Sitemap] ok 6 - Sitemap::Item - add-link
  [Sitemap] # Subtest: Sitemap::Item - add-news
  [Sitemap]     ok 1 - News added
  [Sitemap]     ok 2 - Publication correct
  [Sitemap]     ok 3 - Language correct
  [Sitemap]     ok 4 - Title correct
  [Sitemap]     1..4
  [Sitemap] ok 7 - Sitemap::Item - add-news
  [Sitemap] # Subtest: Sitemap::Item - write-xml
  [Sitemap]     ok 1 - Contains url element
  [Sitemap]     ok 2 - Contains domain
  [Sitemap]     ok 3 - Contains path
  [Sitemap]     ok 4 - Contains priority
  [Sitemap]     1..4
  [Sitemap] ok 8 - Sitemap::Item - write-xml
  [Sitemap] # Subtest: Sitemap::Item - from-hash changefreq coercion
  [Sitemap]     ok 1 - lowercase changefreq coerces to enum
  [Sitemap]     ok 2 - lowercase daily coerces
  [Sitemap]     ok 3 - uppercase weekly coerces
  [Sitemap]     # Subtest: invalid changefreq throws instead of silently dropping
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches / 'bogus' /
  [Sitemap]     ok 4 - invalid changefreq throws instead of silently dropping
  [Sitemap]     1..4
  [Sitemap] ok 9 - Sitemap::Item - from-hash changefreq coercion
  [Sitemap] # Subtest: Sitemap::Item - from-hash accepts DateTime lastmod
  [Sitemap]     ok 1 - DateTime lastmod survives from-hash
  [Sitemap]     ok 2 - DateTime value preserved
  [Sitemap]     ok 3 - ISO string still parsed by from-hash
  [Sitemap]     ok 4 - missing lastmod stays unset
  [Sitemap]     ok 5 - undef lastmod stays unset
  [Sitemap]     ok 6 - date-only lastmod gets DateOnly precision
  [Sitemap]     ok 7 - date-only lastmod round-trips through to-hash as 2024-01-15
  [Sitemap]     ok 8 - year-month lastmod gets YearMonth precision
  [Sitemap]     ok 9 - year-month lastmod round-trips through to-hash as 2024-01
  [Sitemap]     ok 10 - year-only lastmod gets Year precision
  [Sitemap]     ok 11 - year-only lastmod round-trips through to-hash as 2024
  [Sitemap]     ok 12 - full datetime keeps Precise precision
  [Sitemap]     ok 13 - full datetime round-trips unchanged
  [Sitemap]     ok 14 - from-hash consumes a persisted lastmod-precision key
  [Sitemap]     ok 15 - hash round-trip preserves the date-only form
  [Sitemap]     1..15
  [Sitemap] ok 10 - Sitemap::Item - from-hash accepts DateTime lastmod
  [Sitemap] # Subtest: Sitemap::Item - always changefreq is emitted despite being falsy
  [Sitemap]     ok 1 - Changefreq::Always rendered
  [Sitemap]     ok 2 - from-hash keeps changefreq=always
  [Sitemap]     ok 3 - to-hash round-trips the always changefreq
  [Sitemap]     ok 4 - from-hash keeps a raw Changefreq::Always enum (value 0)
  [Sitemap]     ok 5 - raw enum value preserved
  [Sitemap]     ok 6 - Unset changefreq still omitted
  [Sitemap]     1..6
  [Sitemap] ok 11 - Sitemap::Item - always changefreq is emitted despite being falsy
  [Sitemap] # Subtest: Sitemap::Item - from-hash accepts Pair and Pair-list nested elements
  [Sitemap]     ok 1 - itemized Hash element works
  [Sitemap]     ok 2 - image url parsed
  [Sitemap]     ok 3 - image caption parsed
  [Sitemap]     ok 4 - single-attr inline hash coerces to one image
  [Sitemap]     ok 5 - inline image url parsed
  [Sitemap]     ok 6 - itemized link element works
  [Sitemap]     ok 7 - link lang preserved
  [Sitemap]     ok 8 - link url preserved
  [Sitemap]     ok 9 - flattened inline link pair without url dies instead of building an empty link
  [Sitemap]     ok 10 - itemized video element works
  [Sitemap]     ok 11 - video content-loc preserved
  [Sitemap]     ok 12 - video thumbnail-loc preserved
  [Sitemap]     ok 13 - itemized news element works
  [Sitemap]     ok 14 - news title preserved
  [Sitemap]     1..14
  [Sitemap] ok 12 - Sitemap::Item - from-hash accepts Pair and Pair-list nested elements
  [Sitemap] # Subtest: Sitemap::Item - from-hash reports unparseable dates with a clear message
  [Sitemap]     ok 1 - Item.from-hash dies on an unparseable lastmod
  [Sitemap]     ok 2 - message names the offending value
  [Sitemap]     ok 3 - message names the item URL
  [Sitemap]     ok 4 - News.from-hash dies on an unparseable publication-date
  [Sitemap]     ok 5 - news message names the offending value
  [Sitemap]     ok 6 - news message names the title
  [Sitemap]     ok 7 - a parseable lastmod still round-trips
  [Sitemap]     ok 8 - a DateTime publication-date passes through unchanged
  [Sitemap]     1..8
  [Sitemap] ok 13 - Sitemap::Item - from-hash reports unparseable dates with a clear message
  [Sitemap] # Subtest: Sitemap::Item - from-hash requires mandatory fields instead of building empties
  [Sitemap]     ok 1 - Image.from-hash without url dies
  [Sitemap]     ok 2 - Link.from-hash without url dies
  [Sitemap]     ok 3 - Link.from-hash without lang dies
  [Sitemap]     ok 4 - Item.from-hash without url dies
  [Sitemap]     ok 5 - News.from-hash without publication dies
  [Sitemap]     ok 6 - News.from-hash without publication-language dies
  [Sitemap]     ok 7 - News.from-hash without title dies
  [Sitemap]     ok 8 - a hash with the mandatory url still builds
  [Sitemap]     1..8
  [Sitemap] ok 14 - Sitemap::Item - from-hash requires mandatory fields instead of building empties
  [Sitemap] # Subtest: Sitemap::Item - explicit default ports are stripped from URLs
  [Sitemap]     ok 1 - http :80 stripped
  [Sitemap]     ok 2 - https :443 stripped
  [Sitemap]     ok 3 - non-default https :80 preserved
  [Sitemap]     ok 4 - non-default http :443 preserved
  [Sitemap]     ok 5 - userinfo survives with the default port stripped
  [Sitemap]     ok 6 - uppercase default port stripped, path preserved
  [Sitemap]     ok 7 - IPv6 default port stripped
  [Sitemap]     ok 8 - IPv6 non-default port preserved
  [Sitemap]     1..8
  [Sitemap] ok 15 - Sitemap::Item - explicit default ports are stripped from URLs
  [Sitemap] # Subtest: Sitemap::Item::Video - renderable matches the Google spec
  [Sitemap]     ok 1 - thumbnail + content_loc is renderable
  [Sitemap]     ok 2 - thumbnail + player_loc is renderable without content_loc
  [Sitemap]     ok 3 - no thumbnail_loc is not renderable
  [Sitemap]     ok 4 - no content_loc and no player_loc is not renderable
  [Sitemap]     ok 5 - player_loc is emitted for a player-based video
  [Sitemap]     ok 6 - no content_loc element emitted when absent
  [Sitemap]     1..6
  [Sitemap] ok 16 - Sitemap::Item::Video - renderable matches the Google spec
  [Sitemap] # Subtest: W3CDTF output: no fractional seconds in lastmod / publication_date
  [Sitemap]     ok 1 - no fractional seconds anywhere in dates
  [Sitemap]     ok 2 - item lastmod is whole-second W3CDTF
  [Sitemap]     ok 3 - news publication_date truncated to seconds
  [Sitemap]     1..3
  [Sitemap] ok 17 - W3CDTF output: no fractional seconds in lastmod / publication_date
  [Sitemap] # Subtest: priority: scientific-notation values render as plain decimals
  [Sitemap]     ok 1 - 1e-05 renders expanded, not "1e-05.0"
  [Sitemap]     ok 2 - no exponent form in priority
  [Sitemap]     1..2
  [Sitemap] ok 18 - priority: scientific-notation values render as plain decimals
  [Sitemap] # Subtest: priority: sub-1e-10 values are preserved, not flattened to 0.0
  [Sitemap]     ok 1 - a 1e-11 priority renders as its real decimal, not "0.0"
  [Sitemap]     ok 2 - tiny priority is not flattened to 0.0
  [Sitemap]     1..2
  [Sitemap] ok 19 - priority: sub-1e-10 values are preserved, not flattened to 0.0
  [Sitemap] # Subtest: add-video Nil fields and add-news optional publication-date
  [Sitemap]     ok 1 - omitted title coalesces to a defined empty string
  [Sitemap]     ok 2 - omitted description coalesces to a defined empty string
  [Sitemap]     ok 3 - omitted thumbnail-loc coalesces to a defined empty string
  [Sitemap]     ok 4 - title defaults to empty string
  [Sitemap]     ok 5 - add-news works without a publication-date
  [Sitemap]     ok 6 - omitted publication-date stays undefined
  [Sitemap]     1..6
  [Sitemap] ok 20 - add-video Nil fields and add-news optional publication-date
  [Sitemap] # Subtest: from-hash enforces the 0.0..1.0 priority range
  [Sitemap]     # Subtest: out-of-range high priority throws
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches / '42' /
  [Sitemap]     ok 1 - out-of-range high priority throws
  [Sitemap]     # Subtest: negative priority throws
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches / '-3' /
  [Sitemap]     ok 2 - negative priority throws
  [Sitemap]     ok 3 - in-range priority preserved through from-hash
  [Sitemap]     1..3
  [Sitemap] ok 21 - from-hash enforces the 0.0..1.0 priority range
  [Sitemap] # Subtest: Video.from-hash floors ints, keeps rating Real, drops non-finite
  [Sitemap]     ok 1 - duration 1.9 floors to whole seconds
  [Sitemap]     ok 2 - view-count 2.9 floors to whole views
  [Sitemap]     ok 3 - rating keeps its fraction (Real) through from-hash
  [Sitemap]     ok 4 - Inf duration is dropped, not a "Cannot convert Inf to Int" crash
  [Sitemap]     ok 5 - NaN view-count is dropped
  [Sitemap]     ok 6 - 1e400 (overflow to Inf) duration is dropped
  [Sitemap]     1..6
  [Sitemap] ok 22 - Video.from-hash floors ints, keeps rating Real, drops non-finite
  [Sitemap] # Subtest: video dates render whole-second W3CDTF (canonical-date)
  [Sitemap]     ok 1 - expiration_date truncated to whole seconds, offset kept
  [Sitemap]     ok 2 - publication_date truncated to whole seconds with a TZD
  [Sitemap]     ok 3 - no fractional-second digits anywhere
  [Sitemap]     1..3
  [Sitemap] ok 23 - video dates render whole-second W3CDTF (canonical-date)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/02-builder.rakutest
  [Sitemap] 1..44
  [Sitemap] # Subtest: Sitemap::Builder - add-item
  [Sitemap]     ok 1 - Items added
  [Sitemap]     1..1
  [Sitemap] ok 1 - Sitemap::Builder - add-item
  [Sitemap] # Subtest: Sitemap::Builder - add-item with options
  [Sitemap]     ok 1 - Item added with options
  [Sitemap]     1..1
  [Sitemap] ok 2 - Sitemap::Builder - add-item with options
  [Sitemap] # Subtest: Sitemap::Builder - render
  [Sitemap]     ok 1 - Contains urlset element
  [Sitemap]     ok 2 - Contains first URL
  [Sitemap]     ok 3 - Contains second URL
  [Sitemap]     ok 4 - Contains namespace
  [Sitemap]     1..4
  [Sitemap] ok 3 - Sitemap::Builder - render
  [Sitemap] # Subtest: Sitemap::Builder - write to file
  [Sitemap]     ok 1 - File created
  [Sitemap]     ok 2 - File contains URL
  [Sitemap]     1..2
  [Sitemap] ok 4 - Sitemap::Builder - write to file
  [Sitemap] # Subtest: Sitemap::Builder - get-items
  [Sitemap]     ok 1 - Returns 2 items
  [Sitemap]     ok 2 - First item correct
  [Sitemap]     1..2
  [Sitemap] ok 5 - Sitemap::Builder - get-items
  [Sitemap] # Subtest: Sitemap::Builder - clear
  [Sitemap]     ok 1 - Has 1 item
  [Sitemap]     ok 2 - Cleared
  [Sitemap]     1..2
  [Sitemap] ok 6 - Sitemap::Builder - clear
  [Sitemap] # Subtest: Sitemap::Builder - render with XSL
  [Sitemap]     ok 1 - Contains stylesheet PI
  [Sitemap]     ok 2 - Contains text/xsl type
  [Sitemap]     ok 3 - Contains stylesheet URL
  [Sitemap]     1..3
  [Sitemap] ok 7 - Sitemap::Builder - render with XSL
  [Sitemap] # Subtest: Sitemap::Builder - gzip compression
  [Sitemap]     ok 1 - Compressed file created
  [Sitemap]     ok 2 - Contains urlset element
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains second URL
  [Sitemap]     1..4
  [Sitemap] ok 8 - Sitemap::Builder - gzip compression
  [Sitemap] # Subtest: Sitemap::Builder - write with .xml.gz path
  [Sitemap]     ok 1 - Plain (non-compressed) write keeps the literal .gz suffix
  [Sitemap]     ok 2 - No .gz-stripped file is written
  [Sitemap]     1..2
  [Sitemap] ok 9 - Sitemap::Builder - write with .xml.gz path
  [Sitemap] # Subtest: Sitemap::Builder - write keeps an explicit non-xml extension
  [Sitemap]     ok 1 - -o out.txt writes exactly out.txt
  [Sitemap]     ok 2 - No .xml suffix appended to an explicit extension
  [Sitemap]     ok 3 - File contains the item URL
  [Sitemap]     ok 4 - A bare stem still gains the .xml extension
  [Sitemap]     1..4
  [Sitemap] ok 10 - Sitemap::Builder - write keeps an explicit non-xml extension
  [Sitemap] # Subtest: Sitemap::Builder - write .gz and uppercase .XML paths normalize
  [Sitemap]     ok 1 - -o out.txt.gz (non-compressed) keeps the literal .gz suffix
  [Sitemap]     ok 2 - No .gz-stripped out.txt left behind
  [Sitemap]     ok 3 - No mangled out.txt.xml
  [Sitemap]     ok 4 - -o SITEMAP.XML normalizes to SITEMAP.xml (case-insensitive)
  [Sitemap]     ok 5 - The uppercase .XML path is not written literally
  [Sitemap]     1..5
  [Sitemap] ok 11 - Sitemap::Builder - write .gz and uppercase .XML paths normalize
  [Sitemap] # Subtest: Sitemap::Builder - .gz handling respects the compress flag
  [Sitemap]     ok 1 - compression off: out.xml.gz keeps the literal .gz suffix
  [Sitemap]     ok 2 - compression off: the .gz is not stripped
  [Sitemap]     ok 3 - compression off: an explicit .gz without .xml is kept whole
  [Sitemap]     ok 4 - compression off: bare foo.gz is not rewritten
  [Sitemap]     ok 5 - compression on: out.xml emits out.xml.gz
  [Sitemap]     ok 6 - compression on: out.xml.gz stays out.xml.gz
  [Sitemap]     1..6
  [Sitemap] ok 12 - Sitemap::Builder - .gz handling respects the compress flag
  [Sitemap] # Subtest: Sitemap::Builder - write multi-file with an explicit non-xml extension
  [Sitemap]     ok 1 - Chunk keeps the explicit extension with a -1 suffix
  [Sitemap]     ok 2 - Index file uses the explicit extension
  [Sitemap]     ok 3 - No stray .xml appended
  [Sitemap]     1..3
  [Sitemap] ok 13 - Sitemap::Builder - write multi-file with an explicit non-xml extension
  [Sitemap] # Subtest: Sitemap::Builder - render-index
  [Sitemap]     ok 1 - Contains sitemapindex element
  [Sitemap]     ok 2 - Contains first sitemap
  [Sitemap]     ok 3 - Contains second sitemap
  [Sitemap]     1..3
  [Sitemap] ok 14 - Sitemap::Builder - render-index
  [Sitemap] # Subtest: Sitemap::Builder - render-index requires base-url for relative locs
  [Sitemap]     # Subtest: Relative <loc> without :base-url dies instead of emitting a broken index
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'relative loc'/
  [Sitemap]     ok 1 - Relative <loc> without :base-url dies instead of emitting a broken index
  [Sitemap]     1..1
  [Sitemap] ok 15 - Sitemap::Builder - render-index requires base-url for relative locs
  [Sitemap] # Subtest: Sitemap::Builder - render-index base-url without doubled slash
  [Sitemap]     ok 1 - base-url without trailing slash joins once
  [Sitemap]     ok 2 - base-url with trailing slash joins without doubling
  [Sitemap]     ok 3 - all trailing slashes stripped
  [Sitemap]     ok 4 - no double slash anywhere
  [Sitemap]     1..4
  [Sitemap] ok 16 - Sitemap::Builder - render-index base-url without doubled slash
  [Sitemap] # Subtest: Sitemap::Builder - render-index trims leading slashes from relative locs
  [Sitemap]     ok 1 - leading slash of a root-relative loc is not doubled
  [Sitemap]     ok 2 - no double slash anywhere in the index
  [Sitemap]     ok 3 - a loc of '/' alone collapses to the bare base URL
  [Sitemap]     1..3
  [Sitemap] ok 17 - Sitemap::Builder - render-index trims leading slashes from relative locs
  [Sitemap] # Subtest: Sitemap::Builder - render-index absolute-loc check is case-insensitive
  [Sitemap]     ok 1 - uppercase-scheme loc passes through unchanged (not base-prefixed)
  [Sitemap]     ok 2 - non-http absolute loc passes through unchanged
  [Sitemap]     ok 3 - relative loc still base-prefixed
  [Sitemap]     1..3
  [Sitemap] ok 18 - Sitemap::Builder - render-index absolute-loc check is case-insensitive
  [Sitemap] # Subtest: Sitemap::Builder - render-index with XSL
  [Sitemap]     ok 1 - Contains stylesheet PI
  [Sitemap]     ok 2 - Contains sitemapindex element
  [Sitemap]     1..2
  [Sitemap] ok 19 - Sitemap::Builder - render-index with XSL
  [Sitemap] # Subtest: Sitemap::Builder - XSL + gzip compression
  [Sitemap]     ok 1 - Compressed file created
  [Sitemap]     ok 2 - Decompressed output contains stylesheet PI
  [Sitemap]     ok 3 - Contains text/xsl type
  [Sitemap]     ok 4 - Contains stylesheet URL
  [Sitemap]     1..4
  [Sitemap] ok 20 - Sitemap::Builder - XSL + gzip compression
  [Sitemap] # Subtest: Sitemap::Builder - XSL + multi-file split
  [Sitemap]     ok 1 - Chunk 1 created
  [Sitemap]     ok 2 - Chunk 1 contains stylesheet PI
  [Sitemap]     ok 3 - Chunk 2 created
  [Sitemap]     ok 4 - Chunk 2 contains stylesheet PI
  [Sitemap]     ok 5 - Index file created
  [Sitemap]     ok 6 - Index contains stylesheet PI
  [Sitemap]     1..6
  [Sitemap] ok 21 - Sitemap::Builder - XSL + multi-file split
  [Sitemap] # Subtest: Sitemap::Builder - write multi-file with compression
  [Sitemap]     ok 1 - Index file created
  [Sitemap]     ok 2 - Index contains sitemapindex
  [Sitemap]     1..2
  [Sitemap] ok 22 - Sitemap::Builder - write multi-file with compression
  [Sitemap] # Subtest: Sitemap::Builder - items below max-entries keep plain chunk name
  [Sitemap]     ok 1 - Items written to plain {stem}.xml (was -1.xml)
  [Sitemap]     ok 2 - No -1 chunk file created
  [Sitemap]     ok 3 - Single chunk contains the item
  [Sitemap]     ok 4 - Index references plain {stem}.xml
  [Sitemap]     1..4
  [Sitemap] ok 23 - Sitemap::Builder - items below max-entries keep plain chunk name
  [Sitemap] # Subtest: Sitemap::Builder - pretty printing
  [Sitemap]     ok 1 - Contains newlines (pretty)
  [Sitemap]     ok 2 - Contains indented tags
  [Sitemap]     1..2
  [Sitemap] ok 24 - Sitemap::Builder - pretty printing
  [Sitemap] # Subtest: Sitemap::Builder - no pretty printing
  [Sitemap]     ok 1 - Contains loc tag
  [Sitemap]     ok 2 - No indented loc tag
  [Sitemap]     1..2
  [Sitemap] ok 25 - Sitemap::Builder - no pretty printing
  [Sitemap] # Subtest: Sitemap::Builder - add-item with images
  [Sitemap]     ok 1 - Contains image element
  [Sitemap]     ok 2 - Contains image URL
  [Sitemap]     1..2
  [Sitemap] ok 26 - Sitemap::Builder - add-item with images
  [Sitemap] # Subtest: Sitemap::Builder - add-item with video
  [Sitemap]     ok 1 - Contains video element
  [Sitemap]     ok 2 - Contains video title
  [Sitemap]     ok 3 - xmlns:video declared when a video renders
  [Sitemap]     1..3
  [Sitemap] ok 27 - Sitemap::Builder - add-item with video
  [Sitemap] # Subtest: Sitemap::Builder - unrenderable video emits no element and no namespace
  [Sitemap]     ok 1 - video without thumbnail_loc is not emitted
  [Sitemap]     ok 2 - its title is not emitted either
  [Sitemap]     ok 3 - xmlns:video omitted when no renderable video
  [Sitemap]     ok 4 - video without content_loc is not emitted
  [Sitemap]     ok 5 - xmlns:video omitted when no renderable video
  [Sitemap]     1..5
  [Sitemap] ok 28 - Sitemap::Builder - unrenderable video emits no element and no namespace
  [Sitemap] # Subtest: Sitemap::Builder - render does not mutate caller items
  [Sitemap] Warning: dropping video (no content_loc/player_loc) for item https://example.com/video: thumbnail_loc plus content_loc or player_loc are required
  [Sitemap]     ok 1 - unrenderable video still dropped
  [Sitemap]     ok 2 - item.verbose untouched by a verbose builder
  [Sitemap]     ok 3 - renderable video emitted with the threaded verbose param
  [Sitemap]     ok 4 - item.verbose untouched even after a second render
  [Sitemap]     1..4
  [Sitemap] ok 29 - Sitemap::Builder - render does not mutate caller items
  [Sitemap] # Subtest: Sitemap::Builder - add-item-from preserves all fields
  [Sitemap]     ok 1 - changefreq preserved
  [Sitemap]     ok 2 - priority preserved
  [Sitemap]     ok 3 - non-standard url-level <title> is no longer emitted
  [Sitemap]     ok 4 - image preserved
  [Sitemap]     ok 5 - url preserved
  [Sitemap]     1..5
  [Sitemap] ok 30 - Sitemap::Builder - add-item-from preserves all fields
  [Sitemap] # Subtest: Sitemap::Builder - add-item-from deep-clones arrays
  [Sitemap]     ok 1 - builder copy still has the original image
  [Sitemap]     ok 2 - image added to original after add-item-from does not leak into builder
  [Sitemap]     1..2
  [Sitemap] ok 31 - Sitemap::Builder - add-item-from deep-clones arrays
  [Sitemap] # Subtest: Sitemap::Builder - add-item with android/amp links
  [Sitemap]     ok 1 - Renders android:link element
  [Sitemap]     ok 2 - Contains android link URL
  [Sitemap]     ok 3 - Renders amp:link element
  [Sitemap]     ok 4 - Contains amp link URL
  [Sitemap]     ok 5 - android namespace declared when android:link used
  [Sitemap]     ok 6 - amp namespace declared when amp:link used
  [Sitemap]     1..6
  [Sitemap] ok 32 - Sitemap::Builder - add-item with android/amp links
  [Sitemap] # Subtest: Sitemap::Builder - extension namespaces omitted when unused
  [Sitemap]     ok 1 - xmlns:android omitted when no android:link used
  [Sitemap]     ok 2 - xmlns:amp omitted when no amp:link used
  [Sitemap]     ok 3 - xmlns:xhtml omitted when no links used
  [Sitemap]     ok 4 - xmlns:image omitted when no images used
  [Sitemap]     ok 5 - xmlns:video omitted when no videos used
  [Sitemap]     ok 6 - xmlns:news omitted when no news used
  [Sitemap]     1..6
  [Sitemap] ok 33 - Sitemap::Builder - extension namespaces omitted when unused
  [Sitemap] # Subtest: Sitemap::Builder - add-item rejects unsupported object types
  [Sitemap]     # Subtest: Dies on unsupported image object
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'unsupported object type'/
  [Sitemap]     ok 1 - Dies on unsupported image object
  [Sitemap]     ok 2 - No item added after the die
  [Sitemap]     1..2
  [Sitemap] ok 34 - Sitemap::Builder - add-item rejects unsupported object types
  [Sitemap] # Subtest: Sitemap::Builder - xsl-url PI escapes only " and cannot break out
  [Sitemap]     ok 1 - & stays raw in the stylesheet PI
  [Sitemap]     ok 2 - " escaped in the stylesheet PI
  [Sitemap]     ok 3 - Raw & preserved so browsers receive the real URL
  [Sitemap]     ok 4 - PI keeps its shape with the real URL and the escaped quote
  [Sitemap]     ok 5 - < stays raw in the stylesheet PI
  [Sitemap]     ok 6 - < is not entity-escaped
  [Sitemap]     # Subtest: PI value containing ?> dies instead of injecting markup
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'xsl-url contains'/
  [Sitemap]     ok 7 - PI value containing ?> dies instead of injecting markup
  [Sitemap]     ok 8 - Index PI keeps the raw &
  [Sitemap]     1..8
  [Sitemap] ok 35 - Sitemap::Builder - xsl-url PI escapes only " and cannot break out
  [Sitemap] # Subtest: Sitemap::Builder - add-item coerces string attrs
  [Sitemap]     ok 1 - Item accepted with string attrs
  [Sitemap]     ok 2 - lastmod coerced to DateTime
  [Sitemap]     ok 3 - lastmod value preserved
  [Sitemap]     ok 4 - changefreq coerced case-insensitively
  [Sitemap]     ok 5 - priority coerced to Numeric
  [Sitemap]     ok 6 - XML emits coerced changefreq
  [Sitemap]     ok 7 - XML emits coerced priority
  [Sitemap]     # Subtest: Invalid lastmod string dies clearly
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'Invalid lastmod'/
  [Sitemap]     ok 8 - Invalid lastmod string dies clearly
  [Sitemap]     # Subtest: Invalid changefreq string dies clearly
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'Invalid changefreq'/
  [Sitemap]     ok 9 - Invalid changefreq string dies clearly
  [Sitemap]     # Subtest: Invalid priority string dies clearly
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'Invalid priority'/
  [Sitemap]     ok 10 - Invalid priority string dies clearly
  [Sitemap]     1..10
  [Sitemap] ok 36 - Sitemap::Builder - add-item coerces string attrs
  [Sitemap] # Subtest: Sitemap::Builder - whole priorities render as 1.0
  [Sitemap]     ok 1 - priority 1 renders as 1.0 (not bare 1)
  [Sitemap]     ok 2 - fractional priority unchanged
  [Sitemap]     ok 3 - multi-decimal priority not rounded
  [Sitemap]     1..3
  [Sitemap] ok 37 - Sitemap::Builder - whole priorities render as 1.0
  [Sitemap] # Subtest: Sitemap::Builder - accepts partial W3CDTF lastmod (A8)
  [Sitemap]     ok 1 - date-only lastmod precision recorded
  [Sitemap]     ok 2 - year-month lastmod precision recorded
  [Sitemap]     ok 3 - year-only lastmod precision recorded
  [Sitemap]     ok 4 - full datetime stays Precise
  [Sitemap]     ok 5 - year-month parses to a DateTime (no longer dies)
  [Sitemap]     ok 6 - year-only parses to a DateTime (no longer dies)
  [Sitemap]     ok 7 - date-only form rendered verbatim
  [Sitemap]     ok 8 - year-month form rendered verbatim
  [Sitemap]     ok 9 - year-only form rendered verbatim
  [Sitemap]     ok 10 - full datetime rendered verbatim
  [Sitemap]     1..10
  [Sitemap] ok 38 - Sitemap::Builder - accepts partial W3CDTF lastmod (A8)
  [Sitemap] # Subtest: Sitemap::Builder - render-index skips a Nil/empty lastmod
  [Sitemap]     ok 1 - No empty <lastmod></lastmod> tag is emitted
  [Sitemap]     ok 2 - A valid lastmod is still rendered
  [Sitemap]     ok 3 - Entry without lastmod is still present
  [Sitemap]     1..3
  [Sitemap] ok 39 - Sitemap::Builder - render-index skips a Nil/empty lastmod
  [Sitemap] # Subtest: Sitemap::Builder - scheme-relative locs stay absolute in render-index
  [Sitemap]     ok 1 - scheme-relative loc is not prefixed with the base URL
  [Sitemap]     ok 2 - no doubled scheme in the loc
  [Sitemap]     ok 3 - a plain relative loc still gets the base URL
  [Sitemap]     1..3
  [Sitemap] ok 40 - Sitemap::Builder - scheme-relative locs stay absolute in render-index
  [Sitemap] # Subtest: Sitemap::Builder - non-alpha schemes stay absolute in render-index
  [Sitemap]     ok 1 - hyphenated scheme loc is not prefixed with the base URL
  [Sitemap]     ok 2 - plus scheme loc is not prefixed with the base URL
  [Sitemap]     ok 3 - no base prepended onto hyphenated scheme
  [Sitemap]     ok 4 - no base prepended onto plus scheme
  [Sitemap]     1..4
  [Sitemap] ok 41 - Sitemap::Builder - non-alpha schemes stay absolute in render-index
  [Sitemap] # Subtest: Sitemap::Builder - write returns the written file paths
  [Sitemap]     ok 1 - single-file write returns one path
  [Sitemap]     ok 2 - returned path is the real written file
  [Sitemap]     ok 3 - the returned file exists
  [Sitemap]     ok 4 - multi-file write returns chunks plus index
  [Sitemap]     ok 5 - chunk 1 is in the returned paths
  [Sitemap]     ok 6 - chunk 2 is in the returned paths
  [Sitemap]     ok 7 - index is in the returned paths
  [Sitemap]     ok 8 - every returned path exists on disk
  [Sitemap]     1..8
  [Sitemap] ok 42 - Sitemap::Builder - write returns the written file paths
  [Sitemap] # Subtest: video numeric fields: out-of-range values are omitted, valid ones kept
  [Sitemap]     ok 1 - duration above 28800s omitted
  [Sitemap]     ok 2 - negative view_count omitted
  [Sitemap]     ok 3 - rating above 5.0 omitted
  [Sitemap]     ok 4 - valid duration kept
  [Sitemap]     ok 5 - valid view_count kept
  [Sitemap]     ok 6 - valid rating kept
  [Sitemap]     1..6
  [Sitemap] ok 43 - video numeric fields: out-of-range values are omitted, valid ones kept
  [Sitemap] # Subtest: add-item-from validates priority like add-item
  [Sitemap]     # Subtest: out-of-range priority from a direct Item dies
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'priority'/
  [Sitemap]     ok 1 - out-of-range priority from a direct Item dies
  [Sitemap]     ok 2 - in-range priority passes through
  [Sitemap]     ok 3 - valid value renders unchanged
  [Sitemap]     1..3
  [Sitemap] ok 44 - add-item-from validates priority like add-item
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/03-parser.rakutest
  [Sitemap] 1..38
  [Sitemap] # Subtest: Sitemap::Parser - parse simple XML
  [Sitemap]     ok 1 - Parsed 2 items
  [Sitemap]     ok 2 - First URL correct
  [Sitemap]     ok 3 - Priority parsed
  [Sitemap]     ok 4 - Second URL correct
  [Sitemap]     1..4
  [Sitemap] ok 1 - Sitemap::Parser - parse simple XML
  [Sitemap] # Subtest: Sitemap::Parser - a foreign-namespaced child is not misread as a sitemap field
  [Sitemap]     ok 1 - Parsed 1 item
  [Sitemap]     ok 2 - the sitemap-namespace <loc> wins, not the foreign-namespaced one
  [Sitemap]     ok 3 - foreign-namespaced <loc> did not leak into the url
  [Sitemap]     1..3
  [Sitemap] ok 2 - Sitemap::Parser - a foreign-namespaced child is not misread as a sitemap field
  [Sitemap] # Subtest: Sitemap::Parser - parse from file
  [Sitemap]     ok 1 - Parsed 1 item
  [Sitemap]     ok 2 - URL correct
  [Sitemap]     1..2
  [Sitemap] ok 3 - Sitemap::Parser - parse from file
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-file gunzips a .gz file
  [Sitemap]     ok 1 - Gzipped file parsed via parse-xml-file (not a "Start tag expected" failure)
  [Sitemap]     ok 2 - URL correct
  [Sitemap]     1..2
  [Sitemap] ok 4 - Sitemap::Parser - parse-xml-file gunzips a .gz file
  [Sitemap] # Subtest: Sitemap::Parser - invalid gzip file raises a clear error from parse-xml-file
  [Sitemap]     # Subtest: Undecodable gzip raises a clear error
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /:i 'failed to decode'/
  [Sitemap]     ok 1 - Undecodable gzip raises a clear error
  [Sitemap]     1..1
  [Sitemap] ok 5 - Sitemap::Parser - invalid gzip file raises a clear error from parse-xml-file
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-files parallel
  [Sitemap]     ok 1 - Has items key
  [Sitemap]     ok 2 - Has errors key
  [Sitemap]     ok 3 - Parsed 3 items total
  [Sitemap]     ok 4 - No errors
  [Sitemap]     1..4
  [Sitemap] ok 6 - Sitemap::Parser - parse-xml-files parallel
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-files with errors
  [Sitemap]     ok 1 - Parsed 1 valid item
  [Sitemap]     ok 2 - Recorded 1 error
  [Sitemap]     ok 3 - Error file recorded
  [Sitemap]     ok 4 - Error message recorded
  [Sitemap]     ok 5 - Error message is non-empty
  [Sitemap]     ok 6 - Real parser message surfaced, not generic fallback
  [Sitemap]     1..6
  [Sitemap] ok 7 - Sitemap::Parser - parse-xml-files with errors
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-file-recursive with index
  [Sitemap]     ok 1 - Has items key
  [Sitemap]     ok 2 - Has sitemaps key
  [Sitemap]     ok 3 - Parsed 3 items total
  [Sitemap]     ok 4 - Found 1 index
  [Sitemap]     1..4
  [Sitemap] ok 8 - Sitemap::Parser - parse-xml-file-recursive with index
  [Sitemap] # Subtest: Sitemap::Parser - query/fragment child locs resolve; missing children error
  [Sitemap]     ok 1 - Query/fragment child locs resolved to the local files
  [Sitemap]     ok 2 - First child parsed
  [Sitemap]     ok 3 - Fragment child parsed
  [Sitemap]     ok 4 - Missing child recorded as an error
  [Sitemap]     ok 5 - Error names the missing child
  [Sitemap]     1..5
  [Sitemap] ok 9 - Sitemap::Parser - query/fragment child locs resolve; missing children error
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-file-recursive gzipped
  [Sitemap]     ok 1 - Parsed 1 item from gzipped file
  [Sitemap]     ok 2 - URL correct
  [Sitemap]     1..2
  [Sitemap] ok 10 - Sitemap::Parser - parse-xml-file-recursive gzipped
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-file-recursive files-parsed counts only successful parses
  [Sitemap]     ok 1 - files-parsed counts 3 successfully parsed files (index + 2 children, not the bad one)
  [Sitemap]     ok 2 - Only the 2 valid children produced items
  [Sitemap]     ok 3 - The bad file generated 1 error
  [Sitemap]     1..3
  [Sitemap] ok 11 - Sitemap::Parser - parse-xml-file-recursive files-parsed counts only successful parses
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-file-recursive surfaces the real load error
  [Sitemap]     ok 1 - Structural failure recorded as one error
  [Sitemap]     ok 2 - Structural error keeps its real LibXML message, not "Failed to load XML"
  [Sitemap]     ok 3 - Error names the failing file
  [Sitemap]     ok 4 - Decode failure recorded as one error
  [Sitemap]     ok 5 - Decode failure keeps its explicit decode message
  [Sitemap]     1..5
  [Sitemap] ok 12 - Sitemap::Parser - parse-xml-file-recursive surfaces the real load error
  [Sitemap] # Subtest: Sitemap::Parser - invalid lastmod does not abort parse
  [Sitemap]     ok 1 - Both items parsed despite bad lastmod
  [Sitemap]     ok 2 - Invalid lastmod dropped, not fatal
  [Sitemap]     1..2
  [Sitemap] ok 13 - Sitemap::Parser - invalid lastmod does not abort parse
  [Sitemap] # Subtest: Sitemap::Parser - accepts partial W3CDTF lastmod (A7)
  [Sitemap]     ok 1 - all four items parsed
  [Sitemap]     ok 2 - date-only precision kept (was dropped entirely)
  [Sitemap]     ok 3 - year-month precision kept
  [Sitemap]     ok 4 - year-only precision kept
  [Sitemap]     ok 5 - year-month lastmod parses (no longer silently dropped)
  [Sitemap]     ok 6 - year-only lastmod parses (no longer silently dropped)
  [Sitemap]     ok 7 - date-only resolves to the given calendar date
  [Sitemap]     1..7
  [Sitemap] ok 14 - Sitemap::Parser - accepts partial W3CDTF lastmod (A7)
  [Sitemap] # Subtest: Sitemap::Parser - invalid priority/duration does not abort parse
  [Sitemap]     ok 1 - All three items parsed despite invalid numbers
  [Sitemap]     ok 2 - Invalid priority dropped
  [Sitemap]     ok 3 - Valid priority kept
  [Sitemap]     ok 4 - Invalid video duration dropped (not defaulted to 0)
  [Sitemap]     ok 5 - Video without content_loc gets empty string, not thumbnail URL
  [Sitemap]     ok 6 - Zero priority preserved
  [Sitemap]     1..6
  [Sitemap] ok 15 - Sitemap::Parser - invalid priority/duration does not abort parse
  [Sitemap] # Subtest: Sitemap::Parser - out-of-range priority drops the value, not the URL
  [Sitemap] Warning: ignoring out-of-range priority '2.5' for 'https://example.com/a'
  [Sitemap] Warning: ignoring out-of-range priority '-1' for 'https://example.com/b'
  [Sitemap]     ok 1 - All three items parsed despite out-of-range priorities
  [Sitemap]     ok 2 - First URL kept
  [Sitemap]     ok 3 - Out-of-range priority > 1 dropped
  [Sitemap]     ok 4 - Second URL kept
  [Sitemap]     ok 5 - Out-of-range priority < 0 dropped
  [Sitemap]     ok 6 - In-range priority kept
  [Sitemap]     1..6
  [Sitemap] ok 16 - Sitemap::Parser - out-of-range priority drops the value, not the URL
  [Sitemap] # Subtest: Sitemap::Parser - parse-url-recursive gunzips
  [Sitemap]     ok 1 - Parsed item from gzip URL
  [Sitemap]     ok 2 - Gzipped item URL correct
  [Sitemap]     ok 3 - No errors
  [Sitemap]     1..3
  [Sitemap] ok 17 - Sitemap::Parser - parse-url-recursive gunzips
  [Sitemap] # Subtest: Sitemap::Parser - ../ traversal locs are rejected
  [Sitemap]     ok 1 - Only the in-tree child is parsed
  [Sitemap]     ok 2 - In-tree child URL correct
  [Sitemap]     ok 3 - Outside file not reached via ../
  [Sitemap]     1..3
  [Sitemap] ok 18 - Sitemap::Parser - ../ traversal locs are rejected
  [Sitemap] # Subtest: Sitemap::Parser - parse-url-recursive file:// counts urls-parsed
  [Sitemap]     ok 1 - Both items parsed from a file:// URL
  [Sitemap]     ok 2 - file:// branch counts its single URL as parsed
  [Sitemap]     ok 3 - No errors
  [Sitemap]     1..3
  [Sitemap] ok 19 - Sitemap::Parser - parse-url-recursive file:// counts urls-parsed
  [Sitemap] # Subtest: Sitemap::Parser - file:// sitemap index recurses into children
  [Sitemap]     ok 1 - No spurious "Failed to parse XML" error for an index
  [Sitemap]     ok 2 - Child items parsed via the file:// branch recursing into the index
  [Sitemap]     ok 3 - First child item parsed
  [Sitemap]     ok 4 - Second child item parsed
  [Sitemap]     1..4
  [Sitemap] ok 20 - Sitemap::Parser - file:// sitemap index recurses into children
  [Sitemap] # Subtest: Sitemap::Parser - cyclic index graph fetches each sitemap once
  [Sitemap]     ok 1 - Each of the 4 cyclic sitemaps parsed exactly once
  [Sitemap]     ok 2 - No errors
  [Sitemap]     1..2
  [Sitemap] ok 21 - Sitemap::Parser - cyclic index graph fetches each sitemap once
  [Sitemap] # Subtest: Sitemap::Builder - discover-sitemaps preserves non-default port
  [Sitemap]     ok 1 - robots.txt sitemap URL keeps the non-default port
  [Sitemap]     1..1
  [Sitemap] ok 22 - Sitemap::Builder - discover-sitemaps preserves non-default port
  [Sitemap] # Subtest: Sitemap::Builder - discover-sitemap decompresses a gzip robots.txt
  [Sitemap]     ok 1 - Sitemap URL discovered from a gzip-encoded robots.txt
  [Sitemap]     1..1
  [Sitemap] ok 23 - Sitemap::Builder - discover-sitemap decompresses a gzip robots.txt
  [Sitemap] # Subtest: Sitemap::Builder - relative Sitemap entries resolve against robots.txt
  [Sitemap]     ok 1 - relative Sitemap: value resolved against the robots.txt URL (RFC 9309)
  [Sitemap]     1..1
  [Sitemap] ok 24 - Sitemap::Builder - relative Sitemap entries resolve against robots.txt
  [Sitemap] # Subtest: decompress-content defends against decompression bombs
  [Sitemap]     # Subtest: Inflating past the cap dies
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /exceeds/
  [Sitemap]     ok 1 - Inflating past the cap dies
  [Sitemap]     ok 2 - In-range gzip still decodes
  [Sitemap]     ok 3 - Non-gzip data decodes unchanged
  [Sitemap]     1..3
  [Sitemap] ok 25 - decompress-content defends against decompression bombs
  [Sitemap] # Subtest: Sitemap::Parser - parse-url-recursive defaults to same-host children
  [Sitemap]     ok 1 - Foreign-host child excluded by default
  [Sitemap]     ok 2 - Follow-foreign-children parses both children
  [Sitemap]     1..2
  [Sitemap] ok 26 - Sitemap::Parser - parse-url-recursive defaults to same-host children
  [Sitemap] # Subtest: Sitemap::Parser - parse-url-recursive excludes a different-port child by default
  [Sitemap]     ok 1 - Different-port child excluded by default
  [Sitemap]     ok 2 - Follow-foreign-children still skips the dead different-port child
  [Sitemap]     1..2
  [Sitemap] ok 27 - Sitemap::Parser - parse-url-recursive excludes a different-port child by default
  [Sitemap] # Subtest: Sitemap::Parser - relative child locs resolve before the origin check
  [Sitemap]     ok 1 - Both relative child locs resolved, same-origin and parsed
  [Sitemap]     ok 2 - No errors recorded
  [Sitemap]     1..2
  [Sitemap] ok 28 - Sitemap::Parser - relative child locs resolve before the origin check
  [Sitemap] # Subtest: Sitemap::Parser - parse-url-recursive fetches children in parallel
  [Sitemap]     ok 1 - All three children parsed with concurrency=4 (2 items each)
  [Sitemap]     ok 2 - No errors recorded
  [Sitemap]     ok 3 - Index recorded in sitemaps
  [Sitemap]     ok 4 - Index + 3 children counted as parsed
  [Sitemap]     1..4
  [Sitemap] ok 29 - Sitemap::Parser - parse-url-recursive fetches children in parallel
  [Sitemap] # Subtest: decompress-content rejects gzip magic that is not gzip
  [Sitemap]     # Subtest: Magic bytes with invalid gzip data die
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /:s gzip magic/
  [Sitemap]     ok 1 - Magic bytes with invalid gzip data die
  [Sitemap]     ok 2 - .gz suffix with no magic still decodes as plain text
  [Sitemap]     1..2
  [Sitemap] ok 30 - decompress-content rejects gzip magic that is not gzip
  [Sitemap] # Subtest: decompress-content rejects a truncated gzip stream
  [Sitemap]     # Subtest: Mid-stream truncation dies
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /:s truncated/
  [Sitemap]     ok 1 - Mid-stream truncation dies
  [Sitemap]     # Subtest: Header-only gzip dies
  [Sitemap]         1..2
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]     ok 2 - Header-only gzip dies
  [Sitemap]     ok 3 - Complete gzip stream still decodes
  [Sitemap]     1..3
  [Sitemap] ok 31 - decompress-content rejects a truncated gzip stream
  [Sitemap] # Subtest: Sitemap::Parser - is-sitemap-index tolerates comments in the preamble
  [Sitemap]     ok 1 - Index with a DOCTYPE before <sitemapindex> is detected
  [Sitemap]     ok 2 - Plain index still detected
  [Sitemap]     ok 3 - A leading comment before <sitemapindex> is detected as an index
  [Sitemap]     ok 4 - Generator comment between declaration and <sitemapindex> is tolerated
  [Sitemap]     ok 5 - Comment after a DOCTYPE is tolerated
  [Sitemap]     ok 6 - BOM plus multiple comments are tolerated
  [Sitemap]     ok 7 - Comment containing a > is tolerated
  [Sitemap]     ok 8 - Multi-line comment containing a > is tolerated
  [Sitemap]     ok 9 - A urlset is not an index
  [Sitemap]     1..9
  [Sitemap] ok 32 - Sitemap::Parser - is-sitemap-index tolerates comments in the preamble
  [Sitemap] # Subtest: Sitemap::Parser - a throwing worker does not deadlock the queue
  [Sitemap]     ok 1 - Valid child parsed despite the throwing sibling
  [Sitemap]     ok 2 - Valid item URL correct
  [Sitemap]     ok 3 - The throwing child recorded an error, not a hang
  [Sitemap]     ok 4 - The real parser error surfaced
  [Sitemap]     1..4
  [Sitemap] ok 33 - Sitemap::Parser - a throwing worker does not deadlock the queue
  [Sitemap] # Subtest: Sitemap::Parser - unparseable index lastmod is dropped, not Nil
  [Sitemap]     ok 1 - Both index entries parsed
  [Sitemap]     ok 2 - Invalid lastmod key is absent, not Nil
  [Sitemap]     ok 3 - Valid lastmod key present
  [Sitemap]     ok 4 - Valid lastmod parsed to a DateTime
  [Sitemap]     1..4
  [Sitemap] ok 34 - Sitemap::Parser - unparseable index lastmod is dropped, not Nil
  [Sitemap] # Subtest: Sitemap::Parser - huge text nodes parse in local files
  [Sitemap]     ok 1 - Local file with an oversized text node parses via :huge
  [Sitemap]     ok 2 - Huge caption preserved in full
  [Sitemap]     1..2
  [Sitemap] ok 35 - Sitemap::Parser - huge text nodes parse in local files
  [Sitemap] # Subtest: Sitemap::Parser - dedup happens before the max-children budget
  [Sitemap]     ok 1 - Duplicate child did not consume the budget: c1 and c2 both parsed
  [Sitemap]     ok 2 - c2 item present
  [Sitemap]     1..2
  [Sitemap] ok 36 - Sitemap::Parser - dedup happens before the max-children budget
  [Sitemap] # Subtest: Sitemap::Parser - video tags extracted from video:tag elements
  [Sitemap]     ok 1 - three video tags extracted
  [Sitemap]     ok 2 - video tags contain expected values
  [Sitemap]     ok 3 - non-namespaced <tag> is not treated as video:tag (A1)
  [Sitemap]     1..3
  [Sitemap] ok 37 - Sitemap::Parser - video tags extracted from video:tag elements
  [Sitemap] # Subtest: Sitemap::Parser - video booleans accept yes/true/1 case-insensitively
  [Sitemap]     ok 1 - family_friendly=TRUE parses as True
  [Sitemap]     ok 2 - requires_subscription=Yes parses as True
  [Sitemap]     ok 3 - live=1 parses as True
  [Sitemap]     1..3
  [Sitemap] ok 38 - Sitemap::Parser - video booleans accept yes/true/1 case-insensitively
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/04-grammars.rakutest
  [Sitemap] 1..48
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - extract hrefs
  [Sitemap]     ok 1 - Found 3 links
  [Sitemap]     1..1
  [Sitemap] ok 1 - Sitemap::Grammar::LinkExtract - extract hrefs
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - filter special URLs
  [Sitemap]     ok 1 - Only 1 normal link extracted
  [Sitemap]     ok 2 - Correct link
  [Sitemap]     1..2
  [Sitemap] ok 2 - Sitemap::Grammar::LinkExtract - filter special URLs
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - single-pass hrefs match the regex path
  [Sitemap]     ok 1 - single-pass href extraction matches the regex path
  [Sitemap]     ok 2 - five links kept (protocols and anchors dropped)
  [Sitemap]     1..2
  [Sitemap] ok 3 - Sitemap::Grammar::LinkExtract - single-pass hrefs match the regex path
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - script/style tag-name boundary is honored
  [Sitemap]     ok 1 - a link after <scriptx> is preserved
  [Sitemap]     ok 2 - a link after <stylesheet> is preserved
  [Sitemap]     ok 3 - a link after <scripture> is preserved
  [Sitemap]     ok 4 - real script body (and markup inside it) is stripped
  [Sitemap]     ok 5 - script with attributes is still stripped
  [Sitemap]     1..5
  [Sitemap] ok 4 - Sitemap::Grammar::LinkExtract - script/style tag-name boundary is honored
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - extract with base URL
  [Sitemap]     ok 1 - Found 2 links
  [Sitemap]     1..1
  [Sitemap] ok 5 - Sitemap::Grammar::LinkExtract - extract with base URL
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - AMP detection via html-open helpers
  [Sitemap]     ok 1 - amp attribute detected in <html> tag
  [Sitemap]     ok 2 - ⚡ marker detected
  [Sitemap]     ok 3 - ⚡ with no whitespace detected
  [Sitemap]     ok 4 - plain html not detected as AMP
  [Sitemap]     ok 5 - no <html> tag yields empty string
  [Sitemap]     1..5
  [Sitemap] ok 6 - Sitemap::Grammar::LinkExtract - AMP detection via html-open helpers
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - src/srcset ordering, source tags, protocol-relative
  [Sitemap]     ok 1 - img src (before srcset) extracted
  [Sitemap]     ok 2 - img srcset entries extracted regardless of order
  [Sitemap]     ok 3 - img src (after srcset) extracted
  [Sitemap]     ok 4 - srcset-before-src entries extracted
  [Sitemap]     ok 5 - source srcset extracted
  [Sitemap]     ok 6 - og:image protocol-relative resolved to https
  [Sitemap]     ok 7 - Protocol-relative href resolves with base scheme
  [Sitemap]     ok 8 - Single-quoted srcset captured
  [Sitemap]     ok 9 - Unquoted srcset captured
  [Sitemap]     1..9
  [Sitemap] ok 7 - Sitemap::Grammar::LinkExtract - src/srcset ordering, source tags, protocol-relative
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - href stays inside its own tag
  [Sitemap]     ok 1 - href from a later tag is not swallowed by an earlier bare <a>
  [Sitemap]     ok 2 - Only the in-tag href extracted
  [Sitemap]     ok 3 - Malformed nested anchor still extracts its own href
  [Sitemap]     ok 4 - Correct href extracted from malformed HTML
  [Sitemap]     1..4
  [Sitemap] ok 8 - Sitemap::Grammar::LinkExtract - href stays inside its own tag
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - unquoted values keep their trailing slash
  [Sitemap]     ok 1 - Unquoted href keeps its trailing slash
  [Sitemap]     ok 2 - Unquoted href without a slash is untouched
  [Sitemap]     ok 3 - Unquoted attribute keeps its trailing slash (data, not self-closing)
  [Sitemap]     ok 4 - Quoted attribute value keeps its trailing slash
  [Sitemap]     ok 5 - extract-with-text unquoted href keeps its trailing slash
  [Sitemap]     ok 6 - A bare unquoted slash is the root link
  [Sitemap]     1..6
  [Sitemap] ok 9 - Sitemap::Grammar::LinkExtract - unquoted values keep their trailing slash
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - relative resolution keeps port and userinfo
  [Sitemap]     ok 1 - non-default port preserved on absolute path
  [Sitemap]     ok 2 - non-default port preserved on relative path
  [Sitemap]     ok 3 - userinfo and port preserved
  [Sitemap]     ok 4 - default port omitted
  [Sitemap]     ok 5 - protocol-relative URL keeps its own port
  [Sitemap]     1..5
  [Sitemap] ok 10 - Sitemap::Grammar::LinkExtract - relative resolution keeps port and userinfo
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - ../ and ./ segments collapse
  [Sitemap]     ok 1 - parent-relative ../ collapses
  [Sitemap]     ok 2 - multiple ../ collapse
  [Sitemap]     ok 3 - ./ collapses
  [Sitemap]     ok 4 - .. above the root is dropped
  [Sitemap]     ok 5 - query and fragment survive the collapse
  [Sitemap]     ok 6 - bare .. resolves to the parent directory (RFC 3986 keeps the trailing slash)
  [Sitemap]     ok 7 - image src ../ collapses (image:loc)
  [Sitemap]     ok 8 - hreflang ../ collapses (xhtml:link)
  [Sitemap]     ok 9 - video ../ collapses (video:content_loc)
  [Sitemap]     ok 10 - video poster ../ collapses
  [Sitemap]     1..10
  [Sitemap] ok 11 - Sitemap::Grammar::LinkExtract - ../ and ./ segments collapse
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - query-only refs keep the base path
  [Sitemap]     ok 1 - query-only href keeps the full base path and replaces the query (RFC 3986 §5.2.2)
  [Sitemap]     ok 2 - image src query-only resolves against the full base path
  [Sitemap]     ok 3 - hreflang href query-only resolves against the full base path
  [Sitemap]     1..3
  [Sitemap] ok 12 - Sitemap::Grammar::LinkExtract - query-only refs keep the base path
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - <a boundary excludes abbr/area
  [Sitemap]     ok 1 - Only real anchors extracted, abbr/area hrefs ignored
  [Sitemap]     ok 2 - First real anchor
  [Sitemap]     ok 3 - Anchor href on a new line still extracted
  [Sitemap]     1..3
  [Sitemap] ok 13 - Sitemap::Grammar::LinkExtract - <a boundary excludes abbr/area
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - default page scan needs no tag-name boundary
  [Sitemap]     ok 1 - <a> captures only real anchors, not article/area/abbr/address
  [Sitemap]     ok 2 - The captured anchor is the real one
  [Sitemap]     ok 3 - <meta> does not capture <metadata>
  [Sitemap]     ok 4 - <base> does not capture <baseline>
  [Sitemap]     ok 5 - <link> does not capture <linkage>
  [Sitemap]     ok 6 - <source> does not capture <sourcex>
  [Sitemap]     ok 7 - <img> does not capture <image>
  [Sitemap]     ok 8 - <picture> captured once
  [Sitemap]     ok 9 - <video> captured once
  [Sitemap]     ok 10 - <html> captured once
  [Sitemap]     1..10
  [Sitemap] ok 14 - Sitemap::Grammar::LinkExtract - default page scan needs no tag-name boundary
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - HTML entities decode exactly once
  [Sitemap]     ok 1 - amp decoded in quoted href
  [Sitemap]     ok 2 - numeric entity decoded in single-quoted href
  [Sitemap]     ok 3 - href via tag-attrs decoded
  [Sitemap]     ok 4 - double-escaped title decoded exactly once
  [Sitemap]     ok 5 - srcset yields one image
  [Sitemap]     ok 6 - srcset capture entity-decoded
  [Sitemap]     ok 7 - %26 preserved while &amp; decoded
  [Sitemap]     1..7
  [Sitemap] ok 15 - Sitemap::Grammar::LinkExtract - HTML entities decode exactly once
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - Crawl-delay parses without crashing
  [Sitemap]     ok 1 - Robots.txt with Crawl-delay parses
  [Sitemap]     ok 2 - get-crawl-delay returns the parsed delay
  [Sitemap]     ok 3 - Wildcard delay propagates to other agents
  [Sitemap]     ok 4 - Sitemap entries still found
  [Sitemap]     ok 5 - Sitemap URL correct
  [Sitemap]     ok 6 - Allowed path remains allowed
  [Sitemap]     ok 7 - Disallowed path remains disallowed
  [Sitemap]     1..7
  [Sitemap] ok 16 - Sitemap::Grammar::RobotsTxt - Crawl-delay parses without crashing
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - case-insensitive fields, mixed-case UA, CR/LF/CRLF
  [Sitemap]     ok 1 - Uppercase fields with CR/LF/CRLF line endings parse
  [Sitemap]     ok 2 - Mixed-case UA uses its own rules
  [Sitemap]     ok 3 - Mixed-case UA respects Disallow
  [Sitemap]     ok 4 - Crawl-Delay found for mixed-case UA
  [Sitemap]     ok 5 - Uppercase SITEMAP found
  [Sitemap]     ok 6 - Lowercase fields with LF parses
  [Sitemap]     ok 7 - Lowercase disallow enforced
  [Sitemap]     1..7
  [Sitemap] ok 17 - Sitemap::Grammar::RobotsTxt - case-insensitive fields, mixed-case UA, CR/LF/CRLF
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - get-crawl-delay resolves bot-specific groups
  [Sitemap]     ok 1 - Bot-specific group parses
  [Sitemap]     ok 2 - Versioned UA finds the bare product-token group Crawl-delay
  [Sitemap]     ok 3 - Exact lowercase key still works
  [Sitemap]     ok 4 - Any version suffix matches the token group
  [Sitemap]     ok 5 - Unknown UA falls back to the * group
  [Sitemap]     ok 6 - Default argument falls back to *
  [Sitemap]     ok 7 - Token match works without any * fallback present
  [Sitemap]     ok 8 - Unknown UA with no * group yields Nil, not a crash
  [Sitemap]     1..8
  [Sitemap] ok 18 - Sitemap::Grammar::RobotsTxt - get-crawl-delay resolves bot-specific groups
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - malformed Crawl-delay does not crash
  [Sitemap]     ok 1 - Robots.txt with bare-dot Crawl-delay parses
  [Sitemap]     ok 2 - Bare-dot Crawl-delay does not throw
  [Sitemap]     ok 3 - Disallow still enforced after bad Crawl-delay
  [Sitemap]     ok 4 - Multi-dot Crawl-delay parses
  [Sitemap]     ok 5 - Multi-dot Crawl-delay does not throw
  [Sitemap]     ok 6 - Invalid crawl-delay value ignored
  [Sitemap]     1..6
  [Sitemap] ok 19 - Sitemap::Grammar::RobotsTxt - malformed Crawl-delay does not crash
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - empty Disallow does not swallow next entry
  [Sitemap]     ok 1 - Robots.txt with empty Disallow parses
  [Sitemap]     ok 2 - Sitemap entry after empty Disallow still found
  [Sitemap]     ok 3 - Sitemap URL correct
  [Sitemap]     ok 4 - Empty Disallow disallows nothing
  [Sitemap]     1..4
  [Sitemap] ok 20 - Sitemap::Grammar::RobotsTxt - empty Disallow does not swallow next entry
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - empty User-agent/Sitemap values do not discard the file
  [Sitemap]     ok 1 - Robots.txt with an empty User-agent line parses
  [Sitemap]     ok 2 - Empty User-agent defaults to the * wildcard rules
  [Sitemap]     ok 3 - Robots.txt with an empty Sitemap line parses
  [Sitemap]     ok 4 - Empty Sitemap value is skipped, later Sitemap kept
  [Sitemap]     ok 5 - Non-empty Sitemap URL correct
  [Sitemap]     ok 6 - Disallow after empty Sitemap still enforced
  [Sitemap]     1..6
  [Sitemap] ok 21 - Sitemap::Grammar::RobotsTxt - empty User-agent/Sitemap values do not discard the file
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - path matching is anchored unless the pattern starts with *
  [Sitemap]     ok 1 - Robots.txt parses
  [Sitemap]     ok 2 - Exact /admin path is blocked
  [Sitemap]     ok 3 - Prefix /admin/x is blocked
  [Sitemap]     ok 4 - Mid-path /x/admin is NOT blocked (RFC 9309 anchor)
  [Sitemap]     ok 5 - Wildcard-prefixed robots.txt parses
  [Sitemap]     ok 6 - Leading * keeps matching unanchored
  [Sitemap]     1..6
  [Sitemap] ok 22 - Sitemap::Grammar::RobotsTxt - path matching is anchored unless the pattern starts with *
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - unknown and indented directives are skipped, not fatal
  [Sitemap]     ok 1 - Robots.txt with non-standard and indented directives parses
  [Sitemap]     ok 2 - Allowed path remains allowed
  [Sitemap]     ok 3 - Disallow after unknown directives still enforced
  [Sitemap]     ok 4 - Sitemap entry after unknown directives still found
  [Sitemap]     ok 5 - Sitemap URL correct
  [Sitemap]     ok 6 - Trailing unknown directive without a final newline parses
  [Sitemap]     ok 7 - Rules from the partial file still apply
  [Sitemap]     1..7
  [Sitemap] ok 23 - Sitemap::Grammar::RobotsTxt - unknown and indented directives are skipped, not fatal
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - rel values are case-insensitive
  [Sitemap]     ok 1 - rel="ALTERNATE" matches alternate
  [Sitemap]     ok 2 - alternate href resolved
  [Sitemap]     ok 3 - rel="stylesheet" is not treated as alternate
  [Sitemap]     1..3
  [Sitemap] ok 24 - Sitemap::Grammar::LinkExtract - rel values are case-insensitive
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - extract-tag-bodies accepts a bare Str :tags
  [Sitemap]     ok 1 - bare Str :tags<meta> scans only the meta tag
  [Sitemap]     ok 2 - meta body collected
  [Sitemap]     ok 3 - meta body returned
  [Sitemap]     ok 4 - Positional :tags(<meta link>) scans both
  [Sitemap]     ok 5 - meta body present in list result
  [Sitemap]     ok 6 - link body present in list result
  [Sitemap]     ok 7 - default tag set includes meta
  [Sitemap]     ok 8 - default tag set includes link
  [Sitemap]     ok 9 - default tag set includes video
  [Sitemap]     ok 10 - default tag set includes img
  [Sitemap]     1..10
  [Sitemap] ok 25 - Sitemap::Grammar::LinkExtract - extract-tag-bodies accepts a bare Str :tags
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - uppercase tag names match
  [Sitemap]     ok 1 - uppercase <META> matches :tags<meta>
  [Sitemap]     ok 2 - uppercase meta body returned
  [Sitemap]     ok 3 - uppercase <META> present in list result
  [Sitemap]     ok 4 - uppercase <LINK> matches :tags<link>
  [Sitemap]     ok 5 - uppercase link body returned
  [Sitemap]     ok 6 - uppercase <META> in default set
  [Sitemap]     ok 7 - uppercase <LINK> in default set
  [Sitemap]     ok 8 - uppercase <VIDEO> in default set
  [Sitemap]     ok 9 - uppercase <IMG> in default set
  [Sitemap]     ok 10 - uppercase <SOURCE> in default set
  [Sitemap]     1..10
  [Sitemap] ok 26 - Sitemap::Grammar::LinkExtract - uppercase tag names match
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - bare/self-closing tags and single-pass equivalence
  [Sitemap]     ok 1 - bare <img/> captured alongside <img src>
  [Sitemap]     ok 2 - bare <meta/> captured alongside <meta property>
  [Sitemap]     ok 3 - bare <video> captured
  [Sitemap]     ok 4 - both <source> tags captured
  [Sitemap]     ok 5 - single-pass image count matches the scan path
  [Sitemap]     ok 6 - single-pass images equal the scan path results
  [Sitemap]     ok 7 - images actually extracted
  [Sitemap]     ok 8 - single-pass video count matches the scan path
  [Sitemap]     ok 9 - single-pass videos equal the scan path results
  [Sitemap]     1..9
  [Sitemap] ok 27 - Sitemap::Grammar::LinkExtract - bare/self-closing tags and single-pass equivalence
  [Sitemap] # Subtest: Sitemap::Grammar::SitemapSniff - comments in the preamble are tolerated
  [Sitemap]     ok 1 - comment-first index matches
  [Sitemap]     ok 2 - detected as a sitemap
  [Sitemap]     ok 3 - bare comment before sitemapindex matches
  [Sitemap]     ok 4 - still a sitemap
  [Sitemap]     ok 5 - plain index still matches
  [Sitemap]     ok 6 - html document still matches
  [Sitemap]     ok 7 - and is classified as html, not as a sitemap
  [Sitemap]     1..7
  [Sitemap] ok 28 - Sitemap::Grammar::SitemapSniff - comments in the preamble are tolerated
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - srcset commas inside balanced parens are kept
  [Sitemap]     ok 1 - Comma-containing candidate is not split, so both candidates extracted
  [Sitemap]     ok 2 - Parenthesized candidate kept whole, wrappers stripped
  [Sitemap]     ok 3 - Plain candidate resolved and extracted
  [Sitemap]     ok 4 - Parenthesized data URI is not emitted as a junk relative URL
  [Sitemap]     ok 5 - Sibling candidate still extracted
  [Sitemap]     1..5
  [Sitemap] ok 29 - Sitemap::Grammar::LinkExtract - srcset commas inside balanced parens are kept
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - rel token set matches alternate anywhere
  [Sitemap]     ok 1 - rel="alternate x-default" matches
  [Sitemap]     ok 2 - x-default href resolved
  [Sitemap]     ok 3 - rel="x-default alternate" matches
  [Sitemap]     ok 4 - alternate-last href resolved
  [Sitemap]     1..4
  [Sitemap] ok 30 - Sitemap::Grammar::LinkExtract - rel token set matches alternate anywhere
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - script/style bodies and comments do not leak links
  [Sitemap]     ok 1 - Comment does not leak a link
  [Sitemap]     ok 2 - The real link is still found
  [Sitemap]     ok 3 - Script body with angle brackets does not leak a link
  [Sitemap]     ok 4 - The link after the script is found
  [Sitemap]     ok 5 - Style body does not leak a link
  [Sitemap]     ok 6 - The link after the style is found
  [Sitemap]     1..6
  [Sitemap] ok 31 - Sitemap::Grammar::LinkExtract - script/style bodies and comments do not leak links
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - non-canonical close tags still end ignorable regions (CQ)
  [Sitemap]     ok 1 - link after </script > (space before >) survives
  [Sitemap]     ok 2 - the real link is preserved
  [Sitemap]     ok 3 - link after </style newline> survives
  [Sitemap]     ok 4 - the real link is preserved
  [Sitemap]     ok 5 - </scriptx> is not a </script> close; body stays swallowed
  [Sitemap]     1..5
  [Sitemap] ok 32 - Sitemap::Grammar::LinkExtract - non-canonical close tags still end ignorable regions (CQ)
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - extract-images is case-insensitive
  [Sitemap]     ok 1 - uppercase <IMG SRC> matched
  [Sitemap]     ok 2 - uppercase SRCSET= matched
  [Sitemap]     ok 3 - lowercase <img src> still matched
  [Sitemap]     1..3
  [Sitemap] ok 33 - Sitemap::Grammar::LinkExtract - extract-images is case-insensitive
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - Allow specificity beats a shorter Disallow (E1)
  [Sitemap]     ok 1 - Robots.txt with Allow + Disallow parses
  [Sitemap]     ok 2 - Allow /foo* matches 10 octets and beats Disallow /foobar (7) on /foobarxyz (E1)
  [Sitemap]     ok 3 - Length tie on /foobar: the disallow wins (E1)
  [Sitemap]     ok 4 - Disallow + more specific Allow parses
  [Sitemap]     ok 5 - The longer Allow /private/public/ wins inside /private/ (E1)
  [Sitemap]     ok 6 - A sibling under /private/ stays blocked (E1)
  [Sitemap]     1..6
  [Sitemap] ok 34 - Sitemap::Grammar::RobotsTxt - Allow specificity beats a shorter Disallow (E1)
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - scheme matching is case-insensitive (CQ)
  [Sitemap]     ok 1 - robots.txt parses
  [Sitemap]     ok 2 - uppercase HTTP:// scheme still applies the Disallow (was bypassed)
  [Sitemap]     ok 3 - uppercase HTTPS:// scheme still applies the Disallow
  [Sitemap]     ok 4 - lowercase scheme Disallow still applies
  [Sitemap]     ok 5 - an allowed path stays allowed regardless of scheme case
  [Sitemap]     1..5
  [Sitemap] ok 35 - Sitemap::Grammar::RobotsTxt - scheme matching is case-insensitive (CQ)
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - namespaced attrs, html default tag, script-video skip
  [Sitemap]     ok 1 - namespaced xml:lang captured under its full name
  [Sitemap]     ok 2 - namespaced xlink:href captured under its full name
  [Sitemap]     ok 3 - xlink:href no longer collides with the plain href
  [Sitemap]     ok 4 - default tag set includes html (AMP check rides the fast pass)
  [Sitemap]     ok 5 - html body keeps the AMP marker whitespace
  [Sitemap]     ok 6 - tag-bodies path skips the script-embedded video
  [Sitemap]     ok 7 - tag-bodies and scan paths agree on the surviving video
  [Sitemap]     1..7
  [Sitemap] ok 36 - Sitemap::Grammar::LinkExtract - namespaced attrs, html default tag, script-video skip
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - uppercase schemes and data: are filtered
  [Sitemap]     ok 1 - Uppercase javascript:/data:/mailto:/tel: hrefs filtered
  [Sitemap]     ok 2 - Only the normal link survives
  [Sitemap]     ok 3 - data:/javascript: img srcs filtered case-insensitively
  [Sitemap]     ok 4 - Only the real image survives
  [Sitemap]     ok 5 - Real video content_loc survives
  [Sitemap]     ok 6 - Uppercase data: content_loc filtered
  [Sitemap]     1..6
  [Sitemap] ok 37 - Sitemap::Grammar::LinkExtract - uppercase schemes and data: are filtered
  [Sitemap] # Subtest: SitemapSniff: comments may contain ">" (valid XML)
  [Sitemap]     ok 1 - comment containing > still sniffs as sitemap
  [Sitemap]     ok 2 - plain comment unaffected
  [Sitemap]     ok 3 - unterminated comment still fails
  [Sitemap]     1..3
  [Sitemap] ok 38 - SitemapSniff: comments may contain ">" (valid XML)
  [Sitemap] # Subtest: extract-with-text matches uppercase <A> tags
  [Sitemap]     ok 1 - both cases matched
  [Sitemap]     ok 2 - uppercase href resolved
  [Sitemap]     1..2
  [Sitemap] ok 39 - extract-with-text matches uppercase <A> tags
  [Sitemap] # Subtest: SitemapSniff: prolog items in any order + DOCTYPE
  [Sitemap]     ok 1 - BOM+decl+urlset classifies as xml-sitemap
  [Sitemap]     ok 2 - BOM+newline+decl classifies as xml-sitemap
  [Sitemap]     ok 3 - comment then decl classifies as xml-sitemap
  [Sitemap]     ok 4 - decl then comment classifies as xml-sitemap
  [Sitemap]     ok 5 - DOCTYPE urlset classifies as xml-sitemap
  [Sitemap]     ok 6 - DOCTYPE w/ subset classifies as xml-sitemap
  [Sitemap]     ok 7 - HTML doctype root classifies as html
  [Sitemap]     ok 8 - unclosed doctype classifies as NO-MATCH
  [Sitemap]     1..8
  [Sitemap] ok 40 - SitemapSniff: prolog items in any order + DOCTYPE
  [Sitemap] # Subtest: RobotsTxt: UA lookup matches product token with version suffix
  [Sitemap]     ok 1 - versioned UA matches bare-token group (RFC 9309)
  [Sitemap]     ok 2 - exact lowercase token still works
  [Sitemap]     ok 3 - unknown bot falls back to * group
  [Sitemap]     ok 4 - most specific prefix group wins over *
  [Sitemap]     1..4
  [Sitemap] ok 41 - RobotsTxt: UA lookup matches product token with version suffix
  [Sitemap] # Subtest: LinkExtract: duplicate attribute keeps the first occurrence
  [Sitemap]     ok 1 - HTML parsers keep the first duplicated attribute
  [Sitemap]     1..1
  [Sitemap] ok 42 - LinkExtract: duplicate attribute keeps the first occurrence
  [Sitemap] # Subtest: RobotsTxt: BOM before the first User-agent does not poison the * group
  [Sitemap]     ok 1 - BOM-prefixed robots.txt parses
  [Sitemap]     ok 2 - the swallowed User-agent line must not attach its Disallow to *
  [Sitemap]     ok 3 - googlebot itself is still blocked via fallback to the * rules
  [Sitemap]     ok 4 - newline after the BOM still leaves * untouched
  [Sitemap]     1..4
  [Sitemap] ok 43 - RobotsTxt: BOM before the first User-agent does not poison the * group
  [Sitemap] # Subtest: LinkExtract: extraction tolerates tag-bodies sets missing extractor keys
  [Sitemap]     ok 1 - no images found without an img key, and no death
  [Sitemap]     ok 2 - extract-images survives a tag-bodies hash lacking img/source
  [Sitemap]     ok 3 - no videos found without a video key, and no death
  [Sitemap]     ok 4 - extract-videos survives a tag-bodies hash lacking video/img
  [Sitemap]     1..4
  [Sitemap] ok 44 - LinkExtract: extraction tolerates tag-bodies sets missing extractor keys
  [Sitemap] # Subtest: LinkExtract: extract-base-href ignores commented bases and honors attribute-less first base
  [Sitemap]     ok 1 - a commented-out <base> must not hijack relative resolution
  [Sitemap]     ok 2 - an attribute-less first <base> wins over a later one and yields empty
  [Sitemap]     ok 3 - normal <base href> still found
  [Sitemap]     ok 4 - tag-name prefix like baseboard does not match
  [Sitemap]     ok 5 - script body cannot inject a fake base
  [Sitemap]     1..5
  [Sitemap] ok 45 - LinkExtract: extract-base-href ignores commented bases and honors attribute-less first base
  [Sitemap] # Subtest: LinkExtract: custom tag names with digits and hyphens tokenize
  [Sitemap]     ok 1 - plain letter tag still captured
  [Sitemap]     ok 2 - hyphenated custom element captured whole
  [Sitemap]     ok 3 - custom element body returned
  [Sitemap]     ok 4 - digit-bearing heading tag captured (used to truncate at h)
  [Sitemap]     1..4
  [Sitemap] ok 46 - LinkExtract: custom tag names with digits and hyphens tokenize
  [Sitemap] # Subtest: RobotsTxt: allowed() preserves query on bare-domain URLs
  [Sitemap]     ok 1 - bare domain + matching query is blocked via /?q=test
  [Sitemap]     ok 2 - bare domain + non-matching query is allowed
  [Sitemap]     ok 3 - bare domain without query is allowed
  [Sitemap]     ok 4 - /page?q=test does not start with /?q=test so is allowed
  [Sitemap]     ok 5 - fragment is stripped before matching
  [Sitemap]     1..5
  [Sitemap] ok 47 - RobotsTxt: allowed() preserves query on bare-domain URLs
  [Sitemap] # Subtest: empty href="" is deliberately unmatchable across all extractors (CQ-F3)
  [Sitemap]     ok 1 - extract-href-only finds no empty href
  [Sitemap]     ok 2 - extract with base finds no empty href
  [Sitemap]     ok 3 - single-pass body extractor agrees (no empty href)
  [Sitemap]     1..3
  [Sitemap] ok 48 - empty href="" is deliberately unmatchable across all extractors (CQ-F3)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/05-formats.rakutest
  [Sitemap] 1..25
  [Sitemap] # Subtest: Sitemap::Format::HTML - render-list
  [Sitemap]     ok 1 - Contains html tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains second URL
  [Sitemap]     1..4
  [Sitemap] ok 1 - Sitemap::Format::HTML - render-list
  [Sitemap] # Subtest: Sitemap::Format::HTML - doctype
  [Sitemap]     ok 1 - Contains DOCTYPE
  [Sitemap]     ok 2 - Contains lang attribute
  [Sitemap]     1..2
  [Sitemap] ok 2 - Sitemap::Format::HTML - doctype
  [Sitemap] # Subtest: Sitemap::Format::TXT - render-list
  [Sitemap]     ok 1 - Correct content
  [Sitemap]     1..1
  [Sitemap] ok 3 - Sitemap::Format::TXT - render-list
  [Sitemap] # Subtest: Sitemap::Format::TXT - empty list
  [Sitemap]     ok 1 - Empty output for empty list
  [Sitemap]     1..1
  [Sitemap] ok 4 - Sitemap::Format::TXT - empty list
  [Sitemap] # Subtest: Sitemap::Format::TXT - render items
  [Sitemap]     ok 1 - Correct content
  [Sitemap]     1..1
  [Sitemap] ok 5 - Sitemap::Format::TXT - render items
  [Sitemap] # Subtest: Sitemap::Format::TXT - render empty items
  [Sitemap]     ok 1 - Empty output for empty items
  [Sitemap]     1..1
  [Sitemap] ok 6 - Sitemap::Format::TXT - render empty items
  [Sitemap] # Subtest: Sitemap::Format::RSS - render-list
  [Sitemap]     ok 1 - Contains rss tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains second URL
  [Sitemap]     ok 5 - Contains item elements
  [Sitemap]     ok 6 - output is well-formed XML
  [Sitemap]     1..6
  [Sitemap] ok 7 - Sitemap::Format::RSS - render-list
  [Sitemap] # Subtest: Sitemap::Format::Atom - render-list
  [Sitemap]     ok 1 - Contains feed tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains entry elements
  [Sitemap]     ok 5 - output is well-formed XML
  [Sitemap]     1..5
  [Sitemap] ok 8 - Sitemap::Format::Atom - render-list
  [Sitemap] # Subtest: Sitemap::Format::MRSS - render-list
  [Sitemap]     ok 1 - Contains rss tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains media namespace
  [Sitemap]     ok 4 - Contains first URL
  [Sitemap]     ok 5 - output is well-formed XML even without media elements
  [Sitemap]     1..5
  [Sitemap] ok 9 - Sitemap::Format::MRSS - render-list
  [Sitemap] # Subtest: Sitemap::Format::RSS - render with default args (title only)
  [Sitemap]     ok 1 - Contains rss tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains item elements
  [Sitemap]     1..4
  [Sitemap] ok 10 - Sitemap::Format::RSS - render with default args (title only)
  [Sitemap] # Subtest: Sitemap::Format::RSS - render-list without description
  [Sitemap]     ok 1 - Contains rss tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     1..3
  [Sitemap] ok 11 - Sitemap::Format::RSS - render-list without description
  [Sitemap] # Subtest: Sitemap::Format::Atom - render with default args (title only)
  [Sitemap]     ok 1 - Contains feed tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains entry elements
  [Sitemap]     1..4
  [Sitemap] ok 12 - Sitemap::Format::Atom - render with default args (title only)
  [Sitemap] # Subtest: Sitemap::Format::RSS/Atom - :pretty actually indents (default) vs flat (:pretty False)
  [Sitemap]     ok 1 - RSS default output is indented per nesting level
  [Sitemap]     ok 2 - RSS :pretty(False) keeps the feed on one line
  [Sitemap]     ok 3 - RSS pretty and flat are identical modulo whitespace
  [Sitemap]     ok 4 - Atom default output is indented per nesting level
  [Sitemap]     ok 5 - Atom :pretty(False) keeps the feed on one line
  [Sitemap]     1..5
  [Sitemap] ok 13 - Sitemap::Format::RSS/Atom - :pretty actually indents (default) vs flat (:pretty False)
  [Sitemap] # Subtest: Sitemap::Format::HTML - lang attribute is xml-escaped
  [Sitemap]     ok 1 - quotes in lang are escaped so the attribute cannot be broken out of
  [Sitemap]     ok 2 - plain lang passes through untouched
  [Sitemap]     1..2
  [Sitemap] ok 14 - Sitemap::Format::HTML - lang attribute is xml-escaped
  [Sitemap] # Subtest: Sitemap::Format::RSS - render Sitemap::Item without title
  [Sitemap]     ok 1 - Contains rss tag
  [Sitemap]     ok 2 - Contains item URL
  [Sitemap]     1..2
  [Sitemap] ok 15 - Sitemap::Format::RSS - render Sitemap::Item without title
  [Sitemap] # Subtest: Sitemap::Format::MRSS - pubDate is RFC-822
  [Sitemap]     ok 1 - pubDate rendered in RFC-822 format
  [Sitemap]     ok 2 - ISO-8601 lastmod no longer leaked into pubDate
  [Sitemap]     ok 3 - UTC lastmod renders as +0000
  [Sitemap]     ok 4 - Negative-offset lastmod renders correctly
  [Sitemap]     1..4
  [Sitemap] ok 16 - Sitemap::Format::MRSS - pubDate is RFC-822
  [Sitemap] # Subtest: Sitemap::Format::MRSS - media items carry an item <link>
  [Sitemap]     ok 1 - media:content emitted for video item
  [Sitemap]     ok 2 - Item <link> emitted alongside media:content
  [Sitemap]     1..2
  [Sitemap] ok 17 - Sitemap::Format::MRSS - media items carry an item <link>
  [Sitemap] # Subtest: MRSS render accepts :$now like RSS/Atom (lastBuildDate parity)
  [Sitemap]     ok 1 - explicit :$now lands in lastBuildDate
  [Sitemap]     ok 2 - default now() fills lastBuildDate too
  [Sitemap]     1..2
  [Sitemap] ok 18 - MRSS render accepts :$now like RSS/Atom (lastBuildDate parity)
  [Sitemap] # Subtest: MRSS media:content never points at the page URL
  [Sitemap]     ok 1 - player-loc-only video falls back to the player URL
  [Sitemap]     ok 2 - and never to the enclosing page URL
  [Sitemap]     ok 3 - video with neither loc emits no media:content element
  [Sitemap]     1..3
  [Sitemap] ok 19 - MRSS media:content never points at the page URL
  [Sitemap] # Subtest: MRSS duration is only emitted when the video has a positive duration
  [Sitemap]     ok 1 - media:content emitted without a duration
  [Sitemap]     ok 2 - no duration attribute when the video has none
  [Sitemap]     ok 3 - duration attribute present when the video has one
  [Sitemap]     1..3
  [Sitemap] ok 20 - MRSS duration is only emitted when the video has a positive duration
  [Sitemap] # Subtest: C1 - with-meta lastmod wiring survives FeedBuilder refactor
  [Sitemap]     ok 1 - RSS with-meta pubDate uses the item lastmod, not the feed $now
  [Sitemap]     ok 2 - RSS with-meta entry keeps the item title
  [Sitemap]     ok 3 - Atom with-meta updated/published use the item lastmod
  [Sitemap]     ok 4 - Atom with-meta entry keeps the item title
  [Sitemap]     ok 5 - MRSS with-meta pubDate uses the item lastmod
  [Sitemap]     1..5
  [Sitemap] ok 21 - C1 - with-meta lastmod wiring survives FeedBuilder refactor
  [Sitemap] # Subtest: C1/C2 - MRSS output is byte-pinned (flat, deterministic)
  [Sitemap]     ok 1 - MRSS render-list bytes unchanged by the FeedBuilder refactor
  [Sitemap]     ok 2 - MRSS stays flat (still ignores :pretty, like pre-refactor)
  [Sitemap]     1..2
  [Sitemap] ok 22 - C1/C2 - MRSS output is byte-pinned (flat, deterministic)
  [Sitemap] # Subtest: C1 - RSS/Atom white-space-normalized parity across refactor
  [Sitemap]     ok 1 - RSS has <rss root
  [Sitemap]     ok 2 - RSS has feed title S
  [Sitemap]     ok 3 - RSS has item title Alpha
  [Sitemap]     ok 4 - RSS has item link
  [Sitemap]     ok 5 - RSS has pubDate
  [Sitemap]     ok 6 - Atom has feed title S
  [Sitemap]     ok 7 - Atom has item title Alpha
  [Sitemap]     ok 8 - Atom emits <link
  [Sitemap]     ok 9 - Atom has id
  [Sitemap]     ok 10 - Atom has updated
  [Sitemap]     1..10
  [Sitemap] ok 23 - C1 - RSS/Atom white-space-normalized parity across refactor
  [Sitemap] # Subtest: C2 - media namespace injection is scoped to the opening <rss> tag
  [Sitemap]     ok 1 - exactly one xmlns:media on the <rss> tag
  [Sitemap]     ok 2 - declared media namespace resolves to the MRSS URI
  [Sitemap]     ok 3 - xmlns:media text elsewhere leaves exactly one real declaration
  [Sitemap]     ok 4 - scoped-guard output is well-formed XML
  [Sitemap]     ok 5 - title-triggered output is well-formed XML
  [Sitemap]     1..5
  [Sitemap] ok 24 - C2 - media namespace injection is scoped to the opening <rss> tag
  [Sitemap] # Subtest: F - TXT/HTML render-to streams identically to render-list
  [Sitemap]     ok 1 - TXT render-to matches render-list for plain URLs
  [Sitemap]     ok 2 - TXT render-to matches render-list for Item objects
  [Sitemap]     ok 3 - TXT render-to matches render-list for an empty list
  [Sitemap]     ok 4 - HTML render-to matches render-list for plain URLs
  [Sitemap]     ok 5 - HTML render-to matches render-list with lastmod metadata
  [Sitemap]     ok 6 - HTML render-to matches render-list for a mixed list in flat mode
  [Sitemap]     1..6
  [Sitemap] ok 25 - F - TXT/HTML render-to streams identically to render-list
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/06-crawler.rakutest
  [Sitemap] 1..54
  [Sitemap] # Subtest: Sitemap::Crawler - creation
  [Sitemap]     ok 1 - Crawler created
  [Sitemap]     ok 2 - User agent set
  [Sitemap]     ok 3 - Max depth set
  [Sitemap]     ok 4 - Max urls set
  [Sitemap]     1..4
  [Sitemap] ok 1 - Sitemap::Crawler - creation
  [Sitemap] # Subtest: Sitemap::Crawler - events
  [Sitemap]     ok 1 - Event handlers set without error
  [Sitemap]     1..1
  [Sitemap] ok 2 - Sitemap::Crawler - events
  [Sitemap] # Subtest: Sitemap::Crawler - on-error payload shape is consistent
  [Sitemap]     ok 1 - At least one error surfaced
  [Sitemap]     ok 2 - Payload has a url key
  [Sitemap]     ok 3 - Payload has an error key
  [Sitemap]     ok 4 - Payload has a status key (Nil for non-HTTP errors)
  [Sitemap]     ok 5 - HTTP error carries its status
  [Sitemap]     1..5
  [Sitemap] ok 3 - Sitemap::Crawler - on-error payload shape is consistent
  [Sitemap] # Subtest: Sitemap::Crawler - preserves port through crawl
  [Sitemap]     ok 1 - Crawled both pages on non-default port
  [Sitemap]     ok 2 - Item URLs retain the port
  [Sitemap]     1..2
  [Sitemap] ok 4 - Sitemap::Crawler - preserves port through crawl
  [Sitemap] # Subtest: Sitemap::Crawler - no deadlock when workers outpace queue
  [Sitemap]     ok 1 - Crawl completed without deadlock
  [Sitemap]     ok 2 - Crawled all 12 pages
  [Sitemap]     1..2
  [Sitemap] ok 5 - Sitemap::Crawler - no deadlock when workers outpace queue
  [Sitemap] # Subtest: Sitemap::Crawler - robots.txt Crawl-delay is honored
  [Sitemap]     ok 1 - Crawled both pages despite Crawl-delay (no crash)
  [Sitemap]     ok 2 - Crawl-delay spaced requests (~2.1s elapsed)
  [Sitemap]     1..2
  [Sitemap] ok 6 - Sitemap::Crawler - robots.txt Crawl-delay is honored
  [Sitemap] # Subtest: Sitemap::Crawler - each crawl() starts fresh
  [Sitemap]     ok 1 - First crawl found both pages
  [Sitemap]     ok 2 - Second crawl found both pages again
  [Sitemap]     ok 3 - Second crawl issued fresh HTTP requests
  [Sitemap]     1..3
  [Sitemap] ok 7 - Sitemap::Crawler - each crawl() starts fresh
  [Sitemap] # Subtest: Sitemap::Crawler - multiple crawls with extract-news do not crash on reset
  [Sitemap]     ok 1 - First crawl (with extract-news) visited both pages
  [Sitemap]     ok 2 - First crawl extracted the NewsArticle
  [Sitemap]     ok 3 - First crawl raised no errors
  [Sitemap]     ok 4 - Second crawl did not crash on !reset-state
  [Sitemap]     ok 5 - Second crawl re-extracted the NewsArticle
  [Sitemap]     ok 6 - Second crawl raised no errors
  [Sitemap]     1..6
  [Sitemap] ok 8 - Sitemap::Crawler - multiple crawls with extract-news do not crash on reset
  [Sitemap] # Subtest: Sitemap::Crawler - noindex page excluded via on-ignore
  [Sitemap]     ok 1 - Noindex page excluded from sitemap
  [Sitemap]     ok 2 - Child of noindex page still discovered
  [Sitemap]     ok 3 - on-ignore called once
  [Sitemap]     ok 4 - on-ignore got the URL
  [Sitemap]     ok 5 - on-ignore got the reason
  [Sitemap]     1..5
  [Sitemap] ok 9 - Sitemap::Crawler - noindex page excluded via on-ignore
  [Sitemap] # Subtest: Sitemap::Crawler - noindex requires a whole directive token
  [Sitemap]     ok 1 - content="notnoindex" is NOT treated as noindex
  [Sitemap]     ok 2 - child of notnoindex page still crawled
  [Sitemap]     ok 3 - content="noindex, follow" IS still excluded (whole-token match)
  [Sitemap]     ok 4 - directive-list excluded via on-ignore
  [Sitemap]     ok 5 - content="noindexed" is NOT treated as noindex
  [Sitemap]     1..5
  [Sitemap] ok 10 - Sitemap::Crawler - noindex requires a whole directive token
  [Sitemap] # Subtest: Sitemap::Crawler - throwing subscriber does not leak urls-found
  [Sitemap] Error in on-ignore handler: subscriber boom
  [Sitemap]     ok 1 - noindex page not added to sitemap
  [Sitemap]     ok 2 - urls-found balanced despite throwing on-ignore
  [Sitemap]     1..2
  [Sitemap] ok 11 - Sitemap::Crawler - throwing subscriber does not leak urls-found
  [Sitemap] # Subtest: Sitemap::Crawler - gzip-encoded pages decompressed
  [Sitemap]     ok 1 - Both gzipped pages crawled
  [Sitemap]     ok 2 - Link from gzipped page discovered
  [Sitemap]     ok 3 - Gzipped page itself added
  [Sitemap]     1..3
  [Sitemap] ok 12 - Sitemap::Crawler - gzip-encoded pages decompressed
  [Sitemap] # Subtest: Sitemap::Crawler - default user agent carries the package version
  [Sitemap]     ok 1 - Default UA derives from Sitemap::Config::VERSION, not a hardcoded string
  [Sitemap]     1..1
  [Sitemap] ok 13 - Sitemap::Crawler - default user agent carries the package version
  [Sitemap] # Subtest: Sitemap::Crawler - gzip robots.txt rules and fractional Crawl-delay honored
  [Sitemap]     ok 1 - Both allowed pages crawled
  [Sitemap]     ok 2 - Disallowed /secret not crawled (gzip robots parsed)
  [Sitemap]     ok 3 - Fractional Crawl-delay honored (~0.47s elapsed)
  [Sitemap]     1..3
  [Sitemap] ok 14 - Sitemap::Crawler - gzip robots.txt rules and fractional Crawl-delay honored
  [Sitemap] # Subtest: Sitemap::Crawler - ../ image and hreflang URLs collapse in sitemap output
  [Sitemap]     ok 1 - page1 item found
  [Sitemap]     ok 2 - one image extracted
  [Sitemap]     ok 3 - image ../ collapsed, no literal dot segment: http://127.0.0.1:19510/img/x.jpg
  [Sitemap]     ok 4 - one hreflang extracted
  [Sitemap]     ok 5 - hreflang ../ collapsed, no literal dot segment: http://127.0.0.1:19510/en/
  [Sitemap]     ok 6 - page link ../ still resolves and is followed
  [Sitemap]     1..6
  [Sitemap] ok 15 - Sitemap::Crawler - ../ image and hreflang URLs collapse in sitemap output
  [Sitemap] # Subtest: Sitemap::Crawler - query-only start URL keeps its empty path
  [Sitemap]     ok 1 - normalized start URL keeps the empty path (no / inserted before ?)
  [Sitemap]     ok 2 - crawled item URL keeps the empty path + query
  [Sitemap]     ok 3 - no spurious / inserted before the query
  [Sitemap]     1..3
  [Sitemap] ok 16 - Sitemap::Crawler - query-only start URL keeps its empty path
  [Sitemap] # Subtest: Sitemap::Crawler - links with brackets are followed
  [Sitemap]     ok 1 - Both pages crawled
  [Sitemap]     ok 2 - Bracketed link discovered, encoded and followed
  [Sitemap]     1..2
  [Sitemap] ok 17 - Sitemap::Crawler - links with brackets are followed
  [Sitemap] # Subtest: Sitemap::Crawler - malformed start URL errors clearly
  [Sitemap]     # Subtest: Space in URL dies with a clear message
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'invalid start URL'/
  [Sitemap]     ok 1 - Space in URL dies with a clear message
  [Sitemap]     # Subtest: Bad percent-escape dies with a clear message
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'invalid start URL'/
  [Sitemap]     ok 2 - Bad percent-escape dies with a clear message
  [Sitemap]     ok 3 - Brackets in start URL are accepted (encoded by normalize-url)
  [Sitemap]     1..3
  [Sitemap] ok 18 - Sitemap::Crawler - malformed start URL errors clearly
  [Sitemap] # Subtest: Sitemap::Crawler - schemeless start URLs are normalized
  [Sitemap]     ok 1 - Bare domain start URL becomes https
  [Sitemap]     ok 2 - Bare domain with a path keeps the path
  [Sitemap]     ok 3 - Scheme-relative //host start URL becomes https
  [Sitemap]     ok 4 - Explicit http URL is untouched
  [Sitemap]     1..4
  [Sitemap] ok 19 - Sitemap::Crawler - schemeless start URLs are normalized
  [Sitemap] # Subtest: Sitemap::Crawler - https falls back to http
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] HTTPS page failed (The socket was closed during negotiation), retrying http://127.0.0.1:19706/ over HTTP...
  [Sitemap]     ok 1 - Start URL and the http page crawled after the https→http fallback
  [Sitemap]     ok 2 - Both items were fetched over http (fallback fired)
  [Sitemap]     ok 3 - https link stays skipped: different scheme is foreign (same-origin)
  [Sitemap]     1..3
  [Sitemap] ok 20 - Sitemap::Crawler - https falls back to http
  [Sitemap] # Subtest: Sitemap::Crawler - no per-page https retry after the whole-run fallback
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap]     ok 1 - https child was not retried over http after the whole-run fallback
  [Sitemap]     ok 2 - https child reported its own https error via on-error
  [Sitemap]     1..2
  [Sitemap] ok 21 - Sitemap::Crawler - no per-page https retry after the whole-run fallback
  [Sitemap] # Subtest: Sitemap::Crawler - crawl() resets tried-http-fallback for reuse
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] HTTPS page failed (The socket was closed during negotiation), retrying http://127.0.0.1:19709/ over HTTP...
  [Sitemap]     ok 1 - First crawl() succeeded via HTTPS→HTTP fallback
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] HTTPS page failed (The socket was closed during negotiation), retrying http://127.0.0.1:19709/ over HTTP...
  [Sitemap]     ok 2 - Second crawl() also succeeded (fallback flag was reset)
  [Sitemap]     1..2
  [Sitemap] ok 22 - Sitemap::Crawler - crawl() resets tried-http-fallback for reuse
  [Sitemap] # Subtest: Sitemap::Crawler - close releases resources
  [Sitemap]     ok 1 - Crawl ran
  [Sitemap]     ok 2 - close() runs after a crawl
  [Sitemap]     ok 3 - close() is safe to call twice
  [Sitemap]     1..3
  [Sitemap] ok 23 - Sitemap::Crawler - close releases resources
  [Sitemap] # Subtest: Sitemap::Crawler - max-depth check runs before mark-queued (race)
  [Sitemap]     ok 1 - /target was requested (reachable at depth 2 via /slow, not deduped)
  [Sitemap]     ok 2 - /target is present in the sitemap
  [Sitemap]     1..2
  [Sitemap] ok 24 - Sitemap::Crawler - max-depth check runs before mark-queued (race)
  [Sitemap] # Subtest: Sitemap::Crawler - query-only href resolves against the full base path
  [Sitemap]     ok 1 - query-only href resolved to /a/b?x=1 (full base path kept)
  [Sitemap]     ok 2 - no bogus /a/?x=1 request (base dir not used for query-only refs)
  [Sitemap]     ok 3 - resolved query-only URL present in the sitemap
  [Sitemap]     1..3
  [Sitemap] ok 25 - Sitemap::Crawler - query-only href resolves against the full base path
  [Sitemap] # Subtest: Sitemap::Crawler - AMP detection is scoped to real link tags
  [Sitemap]     ok 1 - page with literal rel="amphtml" only in JS is NOT excluded
  [Sitemap]     ok 2 - child of the JS-amp page still discovered
  [Sitemap]     ok 3 - page with a real <link rel="amphtml"> IS excluded
  [Sitemap]     ok 4 - excluded via on-ignore reason "AMP page"
  [Sitemap]     ok 5 - page with <html lang="en" amp> IS excluded
  [Sitemap]     ok 6 - excluded via on-ignore reason "AMP page"
  [Sitemap]     1..6
  [Sitemap] ok 26 - Sitemap::Crawler - AMP detection is scoped to real link tags
  [Sitemap] # Subtest: Sitemap::Crawler - exclude-dirs skips path prefixes
  [Sitemap]     ok 1 - start URL still crawled
  [Sitemap]     ok 2 - non-excluded child still crawled
  [Sitemap]     ok 3 - /admin prefix excluded from sitemap
  [Sitemap]     ok 4 - /administrator NOT excluded (prefix matches whole segments only)
  [Sitemap]     ok 5 - /admin/secret never requested
  [Sitemap]     1..5
  [Sitemap] ok 27 - Sitemap::Crawler - exclude-dirs skips path prefixes
  [Sitemap] # Subtest: Sitemap::Crawler - exclude-dirs applies to the start URL
  [Sitemap]     ok 1 - excluded start URL adds no items
  [Sitemap]     ok 2 - excluded start URL is never fetched
  [Sitemap]     ok 3 - start URL reported via on-ignore as "excluded dir"
  [Sitemap]     1..3
  [Sitemap] ok 28 - Sitemap::Crawler - exclude-dirs applies to the start URL
  [Sitemap] # Subtest: Sitemap::Crawler - rejects empty/fragment-only start URLs
  [Sitemap]     # Subtest: fragment-only start URL rejected
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / 'invalid start URL' /
  [Sitemap]     ok 1 - fragment-only start URL rejected
  [Sitemap]     # Subtest: empty start URL rejected
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / 'invalid start URL' /
  [Sitemap]     ok 2 - empty start URL rejected
  [Sitemap]     1..2
  [Sitemap] ok 29 - Sitemap::Crawler - rejects empty/fragment-only start URLs
  [Sitemap] # Subtest: Sitemap::Crawler - rejects non-http(s) start URLs
  [Sitemap]     # Subtest: ftp seed rejected
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / 'must be http:// or https://' /
  [Sitemap]     ok 1 - ftp seed rejected
  [Sitemap]     # Subtest: file seed rejected
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / 'must be http:// or https://' /
  [Sitemap]     ok 2 - file seed rejected
  [Sitemap]     ok 3 - http seed accepted
  [Sitemap]     1..3
  [Sitemap] ok 30 - Sitemap::Crawler - rejects non-http(s) start URLs
  [Sitemap] # Subtest: Sitemap::Crawler - follow-links False crawls only the start URL
  [Sitemap]     ok 1 - only the start URL is in the sitemap
  [Sitemap]     ok 2 - start URL is /index
  [Sitemap]     ok 3 - discovered links are never requested
  [Sitemap]     1..3
  [Sitemap] ok 31 - Sitemap::Crawler - follow-links False crawls only the start URL
  [Sitemap] # Subtest: Sitemap::Crawler - max-images caps images per page
  [Sitemap]     ok 1 - images capped at max-images: 2
  [Sitemap]     1..1
  [Sitemap] ok 32 - Sitemap::Crawler - max-images caps images per page
  [Sitemap] # Subtest: Sitemap::Crawler - <base href> used for link and asset resolution
  [Sitemap]     ok 1 - both pages under the base path crawled
  [Sitemap]     ok 2 - relative link resolved against <base href> (/sub/page2, not /page2)
  [Sitemap]     ok 3 - link was not resolved against the page URL alone
  [Sitemap]     ok 4 - page itself is present
  [Sitemap]     ok 5 - one image extracted
  [Sitemap]     ok 6 - relative image src resolved against <base href>: {@img-urls[0]}
  [Sitemap]     ok 7 - one hreflang extracted
  [Sitemap]     ok 8 - relative hreflang href resolved against <base href>: {@hreflang-urls[0]}
  [Sitemap]     1..8
  [Sitemap] ok 33 - Sitemap::Crawler - <base href> used for link and asset resolution
  [Sitemap] # Subtest: Sitemap::Crawler - excluded-extension seed reported via on-ignore
  [Sitemap]     ok 1 - no items from an excluded-extension seed
  [Sitemap]     ok 2 - one on-ignore event for the seed
  [Sitemap]     ok 3 - reason names the excluded extension
  [Sitemap]     ok 4 - the seed URL is reported
  [Sitemap]     1..4
  [Sitemap] ok 34 - Sitemap::Crawler - excluded-extension seed reported via on-ignore
  [Sitemap] # Subtest: Sitemap::Crawler - robots-disallowed seed reported via on-ignore
  [Sitemap]     ok 1 - no items from a robots-disallowed seed
  [Sitemap]     ok 2 - one on-ignore event for the seed
  [Sitemap]     ok 3 - reason names the robots rule
  [Sitemap]     1..3
  [Sitemap] ok 35 - Sitemap::Crawler - robots-disallowed seed reported via on-ignore
  [Sitemap] # Subtest: Sitemap::Crawler - robots-disallowed children stay silent
  [Sitemap]     ok 1 - disallowed child not crawled
  [Sitemap]     ok 2 - allowed seed page crawled
  [Sitemap]     ok 3 - disallowed child dropped silently (no on-ignore)
  [Sitemap]     1..3
  [Sitemap] ok 36 - Sitemap::Crawler - robots-disallowed children stay silent
  [Sitemap] # Subtest: Sitemap::Crawler - retries 429/5xx, not 4xx
  [Sitemap]     ok 1 - 429 response retried once (Retry-After honored)
  [Sitemap]     ok 2 - 503 response retried once
  [Sitemap]     ok 3 - 404 response not retried
  [Sitemap]     ok 4 - slow page crawled after 429
  [Sitemap]     ok 5 - oops page crawled after 503
  [Sitemap]     ok 6 - gone page not crawled
  [Sitemap]     ok 7 - 404 recorded as an on-error with its status
  [Sitemap]     1..7
  [Sitemap] ok 37 - Sitemap::Crawler - retries 429/5xx, not 4xx
  [Sitemap] # Subtest: Sitemap::Crawler - empty 200 body reported via on-error
  [Sitemap]     ok 1 - empty-body page not added to the sitemap
  [Sitemap]     ok 2 - empty-body page reported exactly once
  [Sitemap]     ok 3 - on-error carries the 200 status
  [Sitemap]     ok 4 - on-error names the empty body
  [Sitemap]     ok 5 - on-error carries the page URL
  [Sitemap]     1..5
  [Sitemap] ok 38 - Sitemap::Crawler - empty 200 body reported via on-error
  [Sitemap] # Subtest: Sitemap::Crawler - foreign <base href> honors that host robots.txt
  [Sitemap]     ok 1 - foreign-host /secret never requested (its robots.txt disallows it)
  [Sitemap]     ok 2 - foreign-host /public crawled (allowed by that host robots.txt)
  [Sitemap]     ok 3 - allowed foreign page in sitemap
  [Sitemap]     ok 4 - disallowed foreign page not in sitemap
  [Sitemap]     ok 5 - without robots, the foreign page is still crawled (deliberate boundary)
  [Sitemap]     1..5
  [Sitemap] ok 39 - Sitemap::Crawler - foreign <base href> honors that host robots.txt
  [Sitemap] # Subtest: Sitemap::Crawler - https fallback is tracked per origin
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 53
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 53
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] HTTPS page failed (The socket was closed during negotiation), retrying http://127.0.0.1:19812/page over HTTP...
  [Sitemap] HTTPS page failed (The socket was closed during negotiation), retrying http://127.0.0.1:19811/page over HTTP...
  [Sitemap]     ok 1 - origin A retried over http (its own https→http fallback)
  [Sitemap]     ok 2 - origin B ALSO retried over http (per-origin tracking, not a single global cap)
  [Sitemap]     ok 3 - failed https URLs were retried, not emitted as errors
  [Sitemap]     ok 4 - no https error surfaced (both were recovered by fallback)
  [Sitemap]     1..4
  [Sitemap] ok 40 - Sitemap::Crawler - https fallback is tracked per origin
  [Sitemap] # Subtest: Sitemap::Crawler - per-origin robots.txt is fetched once and applied per host
  [Sitemap]     ok 1 - origin B robots.txt fetched exactly once
  [Sitemap]     ok 2 - origin C robots.txt fetched exactly once
  [Sitemap]     ok 3 - B public crawled
  [Sitemap]     ok 4 - C public crawled
  [Sitemap]     ok 5 - B secret blocked by its own robots.txt
  [Sitemap]     ok 6 - C secret blocked by its own robots.txt
  [Sitemap]     1..6
  [Sitemap] ok 41 - Sitemap::Crawler - per-origin robots.txt is fetched once and applied per host
  [Sitemap] # Subtest: Sitemap::Crawler - :queued-cap caps the URL queue
  [Sitemap]     ok 1 - :queued-cap accepted
  [Sitemap]     ok 2 - default queued-cap is 100000
  [Sitemap]     1..2
  [Sitemap] ok 42 - Sitemap::Crawler - :queued-cap caps the URL queue
  [Sitemap] # Subtest: Sitemap::Crawler - a latin-1 page body does not crash the crawl
  [Sitemap]     ok 1 - latin-1 page and its link both crawled
  [Sitemap]     ok 2 - link inside the latin-1 page discovered
  [Sitemap]     1..2
  [Sitemap] ok 43 - Sitemap::Crawler - a latin-1 page body does not crash the crawl
  [Sitemap] # Subtest: Sitemap::Crawler - crawl-delay is enforced per origin, not globally
  [Sitemap]     ok 1 - All A and C pages crawled (a1..a4, c1, c2)
  [Sitemap]     ok 2 - Origin A served 4 pages
  [Sitemap]     ok 3 - Origin C served 2 pages
  [Sitemap]     ok 4 - Crawl-delay sleeps overlap across origins (~16.1s, globally-serialized would be ~16s)
  [Sitemap]     ok 5 - Origin A pages spaced by its own crawl-delay (4.0s gap)
  [Sitemap]     ok 6 - Origin A pages spaced by its own crawl-delay (4.0s gap)
  [Sitemap]     ok 7 - Origin A pages spaced by its own crawl-delay (4.0s gap)
  [Sitemap]     ok 8 - Origin C pages spaced by its own crawl-delay
  [Sitemap]     1..8
  [Sitemap] ok 44 - Sitemap::Crawler - crawl-delay is enforced per origin, not globally
  [Sitemap] # Subtest: Sitemap::Crawler - crawl() still works after close()
  [Sitemap]     ok 1 - first crawl discovers both pages
  [Sitemap]     ok 2 - on-add fired during the first crawl
  [Sitemap]     ok 3 - crawl after close() runs without crashing
  [Sitemap]     ok 4 - on-add fires again after close() (suppliers stay live)
  [Sitemap]     1..4
  [Sitemap] ok 45 - Sitemap::Crawler - crawl() still works after close()
  [Sitemap] # Subtest: Sitemap::Crawler - redirects are re-enqueued through normal gates
  [Sitemap]     ok 1 - redirect target crawled
  [Sitemap]     ok 2 - links on the redirect target were followed
  [Sitemap]     ok 3 - redirect surfaced via on-ignore
  [Sitemap]     1..3
  [Sitemap] ok 46 - Sitemap::Crawler - redirects are re-enqueued through normal gates
  [Sitemap] # Subtest: Sitemap::Crawler - :max-redirects bounds endlessly-unique redirect chains
  [Sitemap]     ok 1 - chain of 3 real redirect hops fetched, the 4th refused
  [Sitemap]     ok 2 - cap refusal surfaced via on-ignore with the hop limit
  [Sitemap]     1..2
  [Sitemap] ok 47 - Sitemap::Crawler - :max-redirects bounds endlessly-unique redirect chains
  [Sitemap] # Subtest: Sitemap::Crawler - redirect into robots-disallowed path is refused
  [Sitemap]     ok 1 - disallowed redirect target never added
  [Sitemap]     ok 2 - refused by the robots gate after redirect
  [Sitemap]     1..2
  [Sitemap] ok 48 - Sitemap::Crawler - redirect into robots-disallowed path is refused
  [Sitemap] # Subtest: Sitemap::Crawler - non-HTML content types are skipped
  [Sitemap]     ok 1 - PDF response never added
  [Sitemap]     ok 2 - skipped with a clear reason
  [Sitemap]     1..2
  [Sitemap] ok 49 - Sitemap::Crawler - non-HTML content types are skipped
  [Sitemap] # Subtest: Sitemap::Crawler - redirect Location fragment is stripped from the target
  [Sitemap]     ok 1 - redirect target crawled exactly once
  [Sitemap]     ok 2 - target URL carries no " \#..." fragment
  [Sitemap]     1..2
  [Sitemap] ok 50 - Sitemap::Crawler - redirect Location fragment is stripped from the target
  [Sitemap] # Subtest: Sitemap::Crawler - cross-origin redirect target is refused
  [Sitemap]     ok 1 - foreign redirect target never added
  [Sitemap]     ok 2 - refused with an explicit reason
  [Sitemap]     1..2
  [Sitemap] ok 51 - Sitemap::Crawler - cross-origin redirect target is refused
  [Sitemap] # Subtest: Sitemap::Crawler - 3xx with Location follows, 304 is not a crawl error
  [Sitemap]     ok 1 - 300 with Location followed to target
  [Sitemap]     ok 2 - 300 not surfaced as a crawl error
  [Sitemap]     ok 3 - 304 not surfaced as a crawl error
  [Sitemap]     ok 4 - 304 reported via on-ignore
  [Sitemap]     1..4
  [Sitemap] ok 52 - Sitemap::Crawler - 3xx with Location follows, 304 is not a crawl error
  [Sitemap] # Subtest: Sitemap::Crawler - is-retryable-error distinguishes transport from permanent errors
  [Sitemap]     ok 1 - header timeout is retried
  [Sitemap]     ok 2 - HTTP 404 is not retried (permanent)
  [Sitemap]     ok 3 - HTTP 410 is not retried (permanent)
  [Sitemap]     ok 4 - HTTP 429 is retried
  [Sitemap]     ok 5 - HTTP 500 is retried
  [Sitemap]     ok 6 - HTTP 502 is retried
  [Sitemap]     ok 7 - HTTP 503 is retried
  [Sitemap]     1..7
  [Sitemap] ok 53 - Sitemap::Crawler - is-retryable-error distinguishes transport from permanent errors
  [Sitemap] # Subtest: Sitemap::Crawler - non-web, excluded-extension and fragment-only links are skipped without crash (CQ-F5)
  [Sitemap]     ok 1 - the real link is queued and crawled
  [Sitemap]     ok 2 - excluded-extension (.js) link is not queued
  [Sitemap]     ok 3 - non-web scheme links are not queued
  [Sitemap]     1..3
  [Sitemap] ok 54 - Sitemap::Crawler - non-web, excluded-extension and fragment-only links are skipped without crash (CQ-F5)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/07-extensions.rakutest
  [Sitemap] 1..26
  [Sitemap] # Subtest: extract-images from img tags
  [Sitemap]     ok 1 - Found 3 images
  [Sitemap]     ok 2 - Found image1.jpg
  [Sitemap]     ok 3 - Found image2.png
  [Sitemap]     ok 4 - Found image3.gif
  [Sitemap]     1..4
  [Sitemap] ok 1 - extract-images from img tags
  [Sitemap] # Subtest: extract-images from picture/srcset
  [Sitemap]     ok 1 - Found small.jpg from srcset
  [Sitemap]     ok 2 - Found large.jpg from srcset
  [Sitemap]     ok 3 - Found fallback.jpg
  [Sitemap]     1..3
  [Sitemap] ok 2 - extract-images from picture/srcset
  [Sitemap] # Subtest: extract-images from og:image
  [Sitemap]     ok 1 - Found 1 og:image
  [Sitemap]     ok 2 - Found og-image.jpg
  [Sitemap]     1..2
  [Sitemap] ok 3 - extract-images from og:image
  [Sitemap] # Subtest: extract-hreflang-links
  [Sitemap]     ok 1 - Found 2 hreflang links
  [Sitemap]     ok 2 - First link has lang=en
  [Sitemap]     ok 3 - First link has correct URL
  [Sitemap]     ok 4 - Second link has lang=de
  [Sitemap]     1..4
  [Sitemap] ok 4 - extract-hreflang-links
  [Sitemap] # Subtest: image deduplication
  [Sitemap]     ok 1 - Deduplicated to 1 image
  [Sitemap]     1..1
  [Sitemap] ok 5 - image deduplication
  [Sitemap] # Subtest: exclude-extensions filters images
  [Sitemap]     ok 1 - jpg is excluded
  [Sitemap]     1..1
  [Sitemap] ok 6 - exclude-extensions filters images
  [Sitemap] # Subtest: Builder omits extension namespaces when not used
  [Sitemap]     ok 1 - xmlns:image omitted when no images
  [Sitemap]     ok 2 - xmlns:xhtml omitted when no links
  [Sitemap]     ok 3 - xmlns:video omitted when no videos
  [Sitemap]     ok 4 - xmlns:news omitted when no news
  [Sitemap]     ok 5 - xmlns:android omitted when no android:link
  [Sitemap]     ok 6 - xmlns:amp omitted when no amp:link
  [Sitemap]     1..6
  [Sitemap] ok 7 - Builder omits extension namespaces when not used
  [Sitemap] # Subtest: Builder namespace gating - with images
  [Sitemap]     ok 1 - Has xmlns:image when images present
  [Sitemap]     1..1
  [Sitemap] ok 8 - Builder namespace gating - with images
  [Sitemap] # Subtest: Builder namespace gating - with hreflang links
  [Sitemap]     ok 1 - Has xmlns:xhtml when links present
  [Sitemap]     1..1
  [Sitemap] ok 9 - Builder namespace gating - with hreflang links
  [Sitemap] # Subtest: extract-images=False
  [Sitemap]     ok 1 - extract-images is False
  [Sitemap]     1..1
  [Sitemap] ok 10 - extract-images=False
  [Sitemap] # Subtest: extract-hreflang=False
  [Sitemap]     ok 1 - extract-hreflang is False
  [Sitemap]     1..1
  [Sitemap] ok 11 - extract-hreflang=False
  [Sitemap] # Subtest: Image URL resolution with base
  [Sitemap]     ok 1 - Found 1 image
  [Sitemap]     ok 2 - URL resolved with base
  [Sitemap]     1..2
  [Sitemap] ok 12 - Image URL resolution with base
  [Sitemap] # Subtest: extract-videos from video tag with src and poster
  [Sitemap]     ok 1 - Found 1 video
  [Sitemap]     ok 2 - Video URL correct
  [Sitemap]     ok 3 - Poster correct
  [Sitemap]     1..3
  [Sitemap] ok 13 - extract-videos from video tag with src and poster
  [Sitemap] # Subtest: extract-videos from source inside video
  [Sitemap]     ok 1 - Found 2 videos
  [Sitemap]     ok 2 - First video URL correct
  [Sitemap]     ok 3 - First video has poster
  [Sitemap]     ok 4 - Second video URL correct
  [Sitemap]     1..4
  [Sitemap] ok 14 - extract-videos from source inside video
  [Sitemap] # Subtest: extract-videos from og:video meta tag
  [Sitemap]     ok 1 - Found 1 og:video
  [Sitemap]     ok 2 - og:video URL correct
  [Sitemap]     1..2
  [Sitemap] ok 15 - extract-videos from og:video meta tag
  [Sitemap] # Subtest: og:video paired with og:image
  [Sitemap]     ok 1 - Found 1 video
  [Sitemap]     ok 2 - og:image used as poster
  [Sitemap]     1..2
  [Sitemap] ok 16 - og:video paired with og:image
  [Sitemap] # Subtest: extract-videos relative URL resolution
  [Sitemap]     ok 1 - Found 1 video
  [Sitemap]     ok 2 - Video URL resolved
  [Sitemap]     ok 3 - Poster URL resolved
  [Sitemap]     1..3
  [Sitemap] ok 17 - extract-videos relative URL resolution
  [Sitemap] # Subtest: extract-videos deduplication
  [Sitemap]     ok 1 - Deduplicated to 1 video
  [Sitemap]     1..1
  [Sitemap] ok 18 - extract-videos deduplication
  [Sitemap] # Subtest: extract-videos returns empty list when no videos
  [Sitemap]     ok 1 - No videos found
  [Sitemap]     1..1
  [Sitemap] ok 19 - extract-videos returns empty list when no videos
  [Sitemap] # Subtest: extract-videos=False
  [Sitemap]     ok 1 - extract-videos is False
  [Sitemap]     1..1
  [Sitemap] ok 20 - extract-videos=False
  [Sitemap] # Subtest: Builder namespace gating - with videos
  [Sitemap]     ok 1 - Has xmlns:video when videos present
  [Sitemap]     ok 2 - Contains video:video element
  [Sitemap]     1..2
  [Sitemap] ok 21 - Builder namespace gating - with videos
  [Sitemap] # Subtest: Video with no thumbnail is skipped
  [Sitemap]     ok 1 - No video element without thumbnail
  [Sitemap]     1..1
  [Sitemap] ok 22 - Video with no thumbnail is skipped
  [Sitemap] # Subtest: Video boolean flags are tri-state
  [Sitemap]     ok 1 - Explicit "no" parses to False
  [Sitemap]     ok 2 - Explicit "yes" parses to True
  [Sitemap]     ok 3 - Absent flag stays unset (not False)
  [Sitemap]     ok 4 - False renders as "no"
  [Sitemap]     ok 5 - Unset flags emit no element
  [Sitemap]     ok 6 - True renders as "yes"
  [Sitemap]     1..6
  [Sitemap] ok 23 - Video boolean flags are tri-state
  [Sitemap] # Subtest: Video without thumbnail/content-loc warns on drop
  [Sitemap]     ok 1 - Dropped video emits a warning
  [Sitemap]     1..1
  [Sitemap] ok 24 - Video without thumbnail/content-loc warns on drop
  [Sitemap] # Subtest: Video.from-hash parses boolean strings
  [Sitemap]     ok 1 - "no" parses to False, not True
  [Sitemap]     ok 2 - "false" parses to False, not True
  [Sitemap]     ok 3 - "0" parses to False, not True
  [Sitemap]     ok 4 - "TRUE" parses to True
  [Sitemap]     ok 5 - "yes" parses to True
  [Sitemap]     ok 6 - "1" parses to True
  [Sitemap]     ok 7 - Absent flag stays unset (tri-state preserved)
  [Sitemap]     1..7
  [Sitemap] ok 25 - Video.from-hash parses boolean strings
  [Sitemap] # Subtest: url-path-extension considers only the URL path, never the host
  [Sitemap]     ok 1 - a dotted host yields no extension
  [Sitemap]     ok 2 - path extension is extracted
  [Sitemap]     ok 3 - extensionless path yields an empty string
  [Sitemap]     ok 4 - extension is case-folded and the query is stripped
  [Sitemap]     ok 5 - fragment is stripped
  [Sitemap]     ok 6 - only the final extension segment is returned
  [Sitemap]     1..6
  [Sitemap] ok 26 - url-path-extension considers only the URL path, never the host
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/08-input-parser.rakutest
  [Sitemap] 1..34
  [Sitemap] # Subtest: Sitemap::InputParser - detect-format from string
  [Sitemap]     ok 1 - XML sitemap detected
  [Sitemap]     ok 2 - Sitemap index detected
  [Sitemap]     ok 3 - RSS detected
  [Sitemap]     ok 4 - Atom detected
  [Sitemap]     ok 5 - RSS content detected
  [Sitemap]     1..5
  [Sitemap] ok 1 - Sitemap::InputParser - detect-format from string
  [Sitemap] # Subtest: Sitemap::InputParser - BOM before xml declaration is detected (CQ-BOM)
  [Sitemap]     ok 1 - BOM + xml-decl + urlset detected (was TXT)
  [Sitemap]     ok 2 - BOM + urlset without decl still detected
  [Sitemap]     ok 3 - BOM + xml-decl + rss detected
  [Sitemap]     ok 4 - no BOM unchanged
  [Sitemap]     1..4
  [Sitemap] ok 2 - Sitemap::InputParser - BOM before xml declaration is detected (CQ-BOM)
  [Sitemap] # Subtest: Sitemap::InputParser - case-insensitive HTML/DOCTYPE sniffing
  [Sitemap]     ok 1 - Lowercase doctype html detected
  [Sitemap]     ok 2 - Uppercase doctype HTML detected (was TXT)
  [Sitemap]     ok 3 - Lowercase doctype keyword detected
  [Sitemap]     ok 4 - Uppercase html element detected (was TXT)
  [Sitemap]     ok 5 - Uppercase html element with attributes detected
  [Sitemap]     1..5
  [Sitemap] ok 3 - Sitemap::InputParser - case-insensitive HTML/DOCTYPE sniffing
  [Sitemap] # Subtest: Sitemap::InputParser - parse-rss
  [Sitemap]     ok 1 - Parsed 2 RSS items
  [Sitemap]     ok 2 - First URL correct
  [Sitemap]     ok 3 - Second URL correct
  [Sitemap]     1..3
  [Sitemap] ok 4 - Sitemap::InputParser - parse-rss
  [Sitemap] # Subtest: Sitemap::InputParser - parse-atom prefers rel=alternate over rel=self
  [Sitemap]     ok 1 - Parsed 1 Atom entry
  [Sitemap]     ok 2 - rel=alternate chosen over rel=self
  [Sitemap]     1..2
  [Sitemap] ok 5 - Sitemap::InputParser - parse-atom prefers rel=alternate over rel=self
  [Sitemap] # Subtest: Sitemap::InputParser - parse-rss skips namespaced atom:link
  [Sitemap]     ok 1 - Parsed 1 RSS item
  [Sitemap]     ok 2 - Plain link chosen over atom:link
  [Sitemap]     1..2
  [Sitemap] ok 6 - Sitemap::InputParser - parse-rss skips namespaced atom:link
  [Sitemap] # Subtest: Sitemap::InputParser - malformed RSS/Atom/MRSS returns () not a backtrace
  [Sitemap]     ok 1 - Malformed RSS yields no items
  [Sitemap]     ok 2 - Malformed Atom yields no items
  [Sitemap]     ok 3 - Malformed MRSS yields no items
  [Sitemap]     ok 4 - Garbage RSS yields no items
  [Sitemap]     ok 5 - Garbage Atom yields no items
  [Sitemap]     ok 6 - Garbage MRSS yields no items
  [Sitemap]     1..6
  [Sitemap] ok 7 - Sitemap::InputParser - malformed RSS/Atom/MRSS returns () not a backtrace
  [Sitemap] # Subtest: Sitemap::InputParser - parse-atom
  [Sitemap]     ok 1 - Parsed 2 Atom entries
  [Sitemap]     ok 2 - First URL correct
  [Sitemap]     ok 3 - Second URL correct
  [Sitemap]     1..3
  [Sitemap] ok 8 - Sitemap::InputParser - parse-atom
  [Sitemap] # Subtest: Sitemap::InputParser - parse-mrss
  [Sitemap]     ok 1 - Parsed 1 MRSS item
  [Sitemap]     ok 2 - URL correct (prefers media:content over <link>)
  [Sitemap]     1..2
  [Sitemap] ok 9 - Sitemap::InputParser - parse-mrss
  [Sitemap] # Subtest: Sitemap::InputParser - parse-html
  [Sitemap]     ok 1 - Parsed 2 HTML links
  [Sitemap]     ok 2 - First URL correct
  [Sitemap]     1..2
  [Sitemap] ok 10 - Sitemap::InputParser - parse-html
  [Sitemap] # Subtest: Sitemap::InputParser - parse-txt
  [Sitemap]     ok 1 - Parsed 3 TXT URLs (skipped comment)
  [Sitemap]     ok 2 - First URL correct
  [Sitemap]     1..2
  [Sitemap] ok 11 - Sitemap::InputParser - parse-txt
  [Sitemap] # Subtest: Sitemap::InputParser - parse-txt resolves relative paths with base-url
  [Sitemap]     ok 1 - 3 TXT lines still parsed
  [Sitemap]     ok 2 - Root-relative path resolved against the base URL
  [Sitemap]     ok 3 - Absolute URL left untouched
  [Sitemap]     ok 4 - Bare hostname line left untouched (ambiguous, not resolved)
  [Sitemap]     1..4
  [Sitemap] ok 12 - Sitemap::InputParser - parse-txt resolves relative paths with base-url
  [Sitemap] # Subtest: Sitemap::InputParser - RSS/Atom/MRSS resolve relative links against base-url (CQ)
  [Sitemap]     ok 1 - RSS items parsed
  [Sitemap]     ok 2 - RSS relative <link> resolved against base-url
  [Sitemap]     ok 3 - RSS absolute <link> left untouched
  [Sitemap]     ok 4 - Atom relative <link href> resolved against base-url
  [Sitemap]     ok 5 - MRSS relative <link> resolved against base-url
  [Sitemap]     1..5
  [Sitemap] ok 13 - Sitemap::InputParser - RSS/Atom/MRSS resolve relative links against base-url (CQ)
  [Sitemap] # Subtest: Sitemap::InputParser - parse-html resolves relative hrefs with base-url
  [Sitemap]     ok 1 - relative + absolute links kept, mailto dropped
  [Sitemap]     ok 2 - Relative href resolved against the base URL
  [Sitemap]     ok 3 - Absolute href unchanged
  [Sitemap]     ok 4 - Relative href still dropped without a base URL (unchanged behavior)
  [Sitemap]     1..4
  [Sitemap] ok 14 - Sitemap::InputParser - parse-html resolves relative hrefs with base-url
  [Sitemap] # Subtest: Sitemap::InputParser - parse-file with RSS file
  [Sitemap]     ok 1 - Parsed 2 items from RSS file
  [Sitemap]     1..1
  [Sitemap] ok 15 - Sitemap::InputParser - parse-file with RSS file
  [Sitemap] # Subtest: Sitemap::InputParser - parse-file with Atom file
  [Sitemap]     ok 1 - Parsed 2 items from Atom file
  [Sitemap]     1..1
  [Sitemap] ok 16 - Sitemap::InputParser - parse-file with Atom file
  [Sitemap] # Subtest: Sitemap::InputParser - parse-file with HTML file
  [Sitemap]     ok 1 - Parsed 3 items from HTML file
  [Sitemap]     1..1
  [Sitemap] ok 17 - Sitemap::InputParser - parse-file with HTML file
  [Sitemap] # Subtest: Sitemap::InputParser - parse-file with TXT file
  [Sitemap]     ok 1 - Parsed 4 items from TXT file (skipped comment)
  [Sitemap]     1..1
  [Sitemap] ok 18 - Sitemap::InputParser - parse-file with TXT file
  [Sitemap] # Subtest: Sitemap::InputParser - parse-url fetches and parses
  [Sitemap]     ok 1 - Parsed 1 item from remote sitemap
  [Sitemap]     ok 2 - Remote URL correct
  [Sitemap]     1..2
  [Sitemap] ok 19 - Sitemap::InputParser - parse-url fetches and parses
  [Sitemap] # Subtest: Sitemap::InputParser - pubDate parsed via parse-date(:optional)
  [Sitemap]     ok 1 - RSS RFC-822 pubDate parsed
  [Sitemap]     ok 2 - RSS RFC-822 offset preserved
  [Sitemap]     ok 3 - Atom RFC-822 updated parsed
  [Sitemap]     ok 4 - MRSS RFC-822 pubDate parsed
  [Sitemap]     ok 5 - Invalid pubDate dropped without aborting parse
  [Sitemap]     1..5
  [Sitemap] ok 20 - Sitemap::InputParser - pubDate parsed via parse-date(:optional)
  [Sitemap] # Subtest: Sitemap::InputParser - parse-file handles gzipped sitemap
  [Sitemap]     ok 1 - Parsed 1 item from gzipped file
  [Sitemap]     ok 2 - Gzip file URL correct
  [Sitemap]     1..2
  [Sitemap] ok 21 - Sitemap::InputParser - parse-file handles gzipped sitemap
  [Sitemap] # Subtest: Sitemap::InputParser - parse-txt-file gunzips gzip magic bytes (CQ)
  [Sitemap]     ok 1 - gzip .txt yields both URLs (was 0: decode-text-body did not gunzip)
  [Sitemap]     ok 2 - First gzip URL correct
  [Sitemap]     ok 3 - missing .txt returns () not a crash
  [Sitemap]     1..3
  [Sitemap] ok 22 - Sitemap::InputParser - parse-txt-file gunzips gzip magic bytes (CQ)
  [Sitemap] # Subtest: Sitemap::InputParser - detect-format gunzips .gz files
  [Sitemap]     ok 1 - detect-format sniffs a gzipped XML sitemap as XML-Sitemap (was TXT)
  [Sitemap]     1..1
  [Sitemap] ok 23 - Sitemap::InputParser - detect-format gunzips .gz files
  [Sitemap] # Subtest: Sitemap::InputParser - truncated gzip returns () instead of throwing
  [Sitemap]     ok 1 - Truncated gzip yields no items, not a crash
  [Sitemap]     1..1
  [Sitemap] ok 24 - Sitemap::InputParser - truncated gzip returns () instead of throwing
  [Sitemap] # Subtest: Sitemap::InputParser - parse-url handles Content-Encoding: gzip
  [Sitemap]     ok 1 - Parsed 1 item from gzip-encoded response
  [Sitemap]     ok 2 - Gzip URL correct
  [Sitemap]     1..2
  [Sitemap] ok 25 - Sitemap::InputParser - parse-url handles Content-Encoding: gzip
  [Sitemap] # Subtest: unrecognised XML never degrades to TXT
  [Sitemap]     ok 1 - namespace-prefixed urlset is Unknown, not TXT
  [Sitemap]     1..1
  [Sitemap] ok 26 - unrecognised XML never degrades to TXT
  [Sitemap] # Subtest: RDF (RSS 1.0) content is Unknown, not TXT garbage
  [Sitemap]     ok 1 - RDF root sniffed as Unknown
  [Sitemap]     1..1
  [Sitemap] ok 27 - RDF (RSS 1.0) content is Unknown, not TXT garbage
  [Sitemap] # Subtest: MRSS detection requires an xmlns:media attribute binding
  [Sitemap]     ok 1 - CDATA mention of media: does not flip detection
  [Sitemap]     ok 2 - xmlns:media= inside description text does not flip to MRSS
  [Sitemap]     ok 3 - xmlns:media on the <rss> root open tag still flips to MRSS
  [Sitemap]     1..3
  [Sitemap] ok 28 - MRSS detection requires an xmlns:media attribute binding
  [Sitemap] # Subtest: atom rel matching uses whole tokens
  [Sitemap]     ok 1 - entry parsed
  [Sitemap]     ok 2 - alternate picked by exact token
  [Sitemap]     ok 3 - second fixture parsed
  [Sitemap]     ok 4 - rel="alternate" beats rel="alternate-link" (whole-token match)
  [Sitemap]     1..4
  [Sitemap] ok 29 - atom rel matching uses whole tokens
  [Sitemap] # Subtest: detect-format file branch is symmetric about missing files
  [Sitemap]     ok 1 - missing .xml file is Unknown, not assumed XML-Sitemap
  [Sitemap]     1..1
  [Sitemap] ok 30 - detect-format file branch is symmetric about missing files
  [Sitemap] # Subtest: Sitemap::InputParser - parse-txt drops non-URL junk lines
  [Sitemap]     ok 1 - Junk lines no longer become items
  [Sitemap]     ok 2 - Absolute URL preserved
  [Sitemap]     ok 3 - Host-shaped schemeless line preserved
  [Sitemap]     ok 4 - Relative refs resolve against the base URL and survive the junk filter
  [Sitemap]     1..4
  [Sitemap] ok 31 - Sitemap::InputParser - parse-txt drops non-URL junk lines
  [Sitemap] # Subtest: Sitemap::InputParser - parse-url -v failure messages never stringify a Str as a hash (CQ-F1)
  [Sitemap]     ok 1 - 500 response returns () not a crash
  [Sitemap]     ok 2 - fetch failure message mentions the fetch step
  [Sitemap]     ok 3 - no Str-hash crash in the -v fetch message
  [Sitemap]     ok 4 - no type-backtrace leaking to user
  [Sitemap]     ok 5 - corrupt gzip body returns () not a crash
  [Sitemap]     ok 6 - body failure message mentions the body step
  [Sitemap]     ok 7 - no Str-hash crash in the -v body message
  [Sitemap]     1..7
  [Sitemap] ok 32 - Sitemap::InputParser - parse-url -v failure messages never stringify a Str as a hash (CQ-F1)
  [Sitemap] # Subtest: Sitemap::InputParser - .rss file containing MRSS is sniffed, not parsed as RSS (B2)
  [Sitemap]     ok 1 - one item parsed from the .rss file
  [Sitemap]     ok 2 - .rss MRSS body parsed as MRSS: media:content URL preferred over <link>
  [Sitemap]     1..2
  [Sitemap] ok 33 - Sitemap::InputParser - .rss file containing MRSS is sniffed, not parsed as RSS (B2)
  [Sitemap] # Subtest: Sitemap::InputParser - parse-txt keeps bracketed IPv6 literals with a port (R1)
  [Sitemap]     ok 1 - IPv6-literal and plain URL lines kept, junk line dropped
  [Sitemap]     ok 2 - bracketed IPv6 literal with port and path kept
  [Sitemap]     ok 3 - bracketed IPv6 literal with bare port kept
  [Sitemap]     ok 4 - regular dotted-host line still kept
  [Sitemap]     1..4
  [Sitemap] ok 34 - Sitemap::InputParser - parse-txt keeps bracketed IPv6 literals with a port (R1)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/09-dir-scanner.rakutest
  [Sitemap] 1..38
  [Sitemap] # Subtest: Basic scan discovers correct URLs
  [Sitemap]     ok 1 - about.html found
  [Sitemap]     ok 2 - contact.html found
  [Sitemap]     ok 3 - blog/ found (directory)
  [Sitemap]     ok 4 - blog/post1.html found
  [Sitemap]     ok 5 - external link excluded
  [Sitemap]     ok 6 - index.html maps to root URL
  [Sitemap]     1..6
  [Sitemap] ok 1 - Basic scan discovers correct URLs
  [Sitemap] # Subtest: Entry fallback uses first sorted .html when no index.html
  [Sitemap]     ok 1 - First sorted .html is entry point
  [Sitemap]     1..1
  [Sitemap] ok 2 - Entry fallback uses first sorted .html when no index.html
  [Sitemap] # Subtest: Cycle detection prevents infinite loop
  [Sitemap]     ok 1 - Root URL appears only once despite cycles
  [Sitemap]     1..1
  [Sitemap] ok 3 - Cycle detection prevents infinite loop
  [Sitemap] # Subtest: Images extracted and included in sitemap
  [Sitemap]     ok 1 - Root page item found
  [Sitemap]     ok 2 - Images extracted
  [Sitemap]     ok 3 - Image URL contains logo.png
  [Sitemap]     1..3
  [Sitemap] ok 4 - Images extracted and included in sitemap
  [Sitemap] # Subtest: Hreflang links extracted
  [Sitemap]     ok 1 - One page found
  [Sitemap]     ok 2 - Two hreflang links extracted
  [Sitemap]     1..2
  [Sitemap] ok 5 - Hreflang links extracted
  [Sitemap] # Subtest: Base URL from --base-url flag
  [Sitemap]     ok 1 - All URLs use custom base URL
  [Sitemap]     1..1
  [Sitemap] ok 6 - Base URL from --base-url flag
  [Sitemap] # Subtest: Base URL derived from robots.txt
  [Sitemap]     ok 1 - All URLs use base from robots.txt
  [Sitemap]     1..1
  [Sitemap] ok 7 - Base URL derived from robots.txt
  [Sitemap] # Subtest: Default file:/// fallback when no robots.txt
  [Sitemap]     ok 1 - URL is file:/// for root
  [Sitemap]     1..1
  [Sitemap] ok 8 - Default file:/// fallback when no robots.txt
  [Sitemap] # Subtest: Relative robots Sitemap: URL roots URLs at the scan directory (CQ)
  [Sitemap]     ok 1 - relative Sitemap: does not collapse to filesystem root file:///
  [Sitemap]     ok 2 - URLs carry a directory path (rooted at the scan dir), not the bare filesystem root
  [Sitemap]     1..2
  [Sitemap] ok 9 - Relative robots Sitemap: URL roots URLs at the scan directory (CQ)
  [Sitemap] # Subtest: Empty file does not report a spurious read error (CQ)
  [Sitemap]     ok 1 - empty file emits no "Cannot read file" error
  [Sitemap]     ok 2 - root page is still scanned
  [Sitemap]     1..2
  [Sitemap] ok 10 - Empty file does not report a spurious read error (CQ)
  [Sitemap] # Subtest: Max depth limits crawling
  [Sitemap]     ok 1 - about.html found (depth 1)
  [Sitemap]     ok 2 - contact.html found (depth 1)
  [Sitemap]     ok 3 - blog/ found (depth 1)
  [Sitemap]     ok 4 - blog/post1.html not found (depth 2)
  [Sitemap]     1..4
  [Sitemap] ok 11 - Max depth limits crawling
  [Sitemap] # Subtest: Max depth limits index-less directory expansion
  [Sitemap]     ok 1 - docs/ found (depth 1)
  [Sitemap]     ok 2 - docs/readme.html not crawled (depth 2)
  [Sitemap]     1..2
  [Sitemap] ok 12 - Max depth limits index-less directory expansion
  [Sitemap] # Subtest: Max URLs limits results
  [Sitemap]     ok 1 - Only 2 URLs returned
  [Sitemap]     1..1
  [Sitemap] ok 13 - Max URLs limits results
  [Sitemap] # Subtest: Directory with index.html maps to trailing slash URL
  [Sitemap]     ok 1 - blog/ has trailing slash
  [Sitemap]     ok 2 - blog/index.html not in URLs
  [Sitemap]     1..2
  [Sitemap] ok 14 - Directory with index.html maps to trailing slash URL
  [Sitemap] # Subtest: Fragment and query links resolve to the file
  [Sitemap]     ok 1 - Fragment and query variants collapse to one page URL
  [Sitemap]     ok 2 - No resolve errors for fragment/query links
  [Sitemap]     1..2
  [Sitemap] ok 15 - Fragment and query links resolve to the file
  [Sitemap] # Subtest: Index-less dir does not duplicate subdir-with-index URL
  [Sitemap]     ok 1 - No duplicate URLs
  [Sitemap]     ok 2 - subdir-with-index URL appears exactly once
  [Sitemap]     ok 3 - index-less dir URL appears once
  [Sitemap]     ok 4 - sibling page crawled
  [Sitemap]     1..4
  [Sitemap] ok 16 - Index-less dir does not duplicate subdir-with-index URL
  [Sitemap] # Subtest: Page link to subdir index.html does not duplicate dir URL
  [Sitemap]     ok 1 - subdir-with-index URL appears exactly once (concurrency=1)
  [Sitemap]     ok 2 - No duplicate URLs (concurrency=1)
  [Sitemap]     ok 3 - subdir-with-index URL appears exactly once (concurrency=4)
  [Sitemap]     ok 4 - No duplicate URLs (concurrency=4)
  [Sitemap]     1..4
  [Sitemap] ok 17 - Page link to subdir index.html does not duplicate dir URL
  [Sitemap] # Subtest: Subdir-with-index reached via a dir task carries full extraction
  [Sitemap]     ok 1 - Subdir-with-index URL present
  [Sitemap]     ok 2 - Dir-with-index URL carries the index page images (not a bare add)
  [Sitemap]     ok 3 - Image URL correct
  [Sitemap]     ok 4 - Unlinked sibling page still crawled
  [Sitemap]     ok 5 - No duplicate URLs
  [Sitemap]     1..5
  [Sitemap] ok 18 - Subdir-with-index reached via a dir task carries full extraction
  [Sitemap] # Subtest: Directory without index.html is expanded
  [Sitemap]     ok 1 - docs/ URL added
  [Sitemap]     ok 2 - docs/readme.html crawled from index-less dir
  [Sitemap]     ok 3 - docs/guide.html crawled via link
  [Sitemap]     ok 4 - nested subdir manual.html crawled
  [Sitemap]     ok 5 - docs/ URL added even with no html children
  [Sitemap]     ok 6 - non-html children ignored
  [Sitemap]     1..6
  [Sitemap] ok 19 - Directory without index.html is expanded
  [Sitemap] # Subtest: Index-less directory respects max-urls cap
  [Sitemap]     ok 1 - No more than 2 URLs despite index-less dir
  [Sitemap]     ok 2 - docs/ not added once cap reached
  [Sitemap]     ok 3 - docs/b.html not crawled once cap reached
  [Sitemap]     1..3
  [Sitemap] ok 20 - Index-less directory respects max-urls cap
  [Sitemap] # Subtest: Symlink escaping root is rejected
  [Sitemap]     ok 1 - Symlink escape detected or resolved path rejected
  [Sitemap]     1..1
  [Sitemap] ok 21 - Symlink escaping root is rejected
  [Sitemap] # Subtest: Path escape attempt is handled safely
  [Sitemap]     ok 1 - Path escape handled safely
  [Sitemap]     1..1
  [Sitemap] ok 22 - Path escape attempt is handled safely
  [Sitemap] # Subtest: Non-HTML files completely ignored
  [Sitemap]     ok 1 - PDF not in sitemap
  [Sitemap]     ok 2 - PNG not in sitemap (as page)
  [Sitemap]     1..2
  [Sitemap] ok 23 - Non-HTML files completely ignored
  [Sitemap] # Subtest: on-add events emitted with URL strings
  [Sitemap]     ok 1 - on-add events emitted
  [Sitemap]     ok 2 - Event payload is a string
  [Sitemap]     ok 3 - URL uses derived base URL
  [Sitemap]     1..3
  [Sitemap] ok 24 - on-add events emitted with URL strings
  [Sitemap] # Subtest: Videos extracted and included in sitemap
  [Sitemap]     ok 1 - One page found
  [Sitemap]     ok 2 - Videos extracted
  [Sitemap]     ok 3 - Video URL contains video.mp4
  [Sitemap]     1..3
  [Sitemap] ok 25 - Videos extracted and included in sitemap
  [Sitemap] # Subtest: Parallel scan deduplicates self-linking seed
  [Sitemap]     ok 1 - No duplicate URLs in parallel scan
  [Sitemap]     ok 2 - Root URL appears exactly once
  [Sitemap]     1..2
  [Sitemap] ok 26 - Parallel scan deduplicates self-linking seed
  [Sitemap] # Subtest: Relative assets resolve against <base href> (filesystem linking kept)
  [Sitemap]     ok 1 - page found
  [Sitemap]     ok 2 - image resolves against <base href>
  [Sitemap]     ok 3 - hreflang resolves against <base href>
  [Sitemap]     ok 4 - relative link still followed via filesystem (not dragged off-tree by base)
  [Sitemap]     1..4
  [Sitemap] ok 27 - Relative assets resolve against <base href> (filesystem linking kept)
  [Sitemap] # Subtest: Unreadable subdirectory does not hang the parallel scan
  [Sitemap]     ok 1 - parallel scan completes despite unreadable subdirectory
  [Sitemap]     ok 2 - readable page still crawled
  [Sitemap]     ok 3 - on-error fired for the unreadable subdirectory
  [Sitemap]     1..3
  [Sitemap] ok 28 - Unreadable subdirectory does not hang the parallel scan
  [Sitemap] # Subtest: Unreadable subdirectory does not abort the sequential scan
  [Sitemap]     ok 1 - sequential scan completes and crawls the readable page despite unreadable subdirectory
  [Sitemap]     ok 2 - on-error fired for the unreadable subdirectory
  [Sitemap]     1..2
  [Sitemap] ok 29 - Unreadable subdirectory does not abort the sequential scan
  [Sitemap] # Subtest: scan() twice resets state and re-crawls
  [Sitemap]     ok 1 - each scan returns a fresh builder
  [Sitemap]     ok 2 - first scan found a.html
  [Sitemap]     ok 3 - second scan re-crawled and found a.html again
  [Sitemap]     ok 4 - second scan produced the same number of items
  [Sitemap]     1..4
  [Sitemap] ok 30 - scan() twice resets state and re-crawls
  [Sitemap] # Subtest: max-images caps images per page (was hardcoded 1000)
  [Sitemap]     ok 1 - root page found
  [Sitemap]     ok 2 - images capped at max-images: 2
  [Sitemap]     ok 3 - default max-images (1000) does not truncate 6 images
  [Sitemap]     1..3
  [Sitemap] ok 31 - max-images caps images per page (was hardcoded 1000)
  [Sitemap] # Subtest: Multiple on-add handlers all fire
  [Sitemap]     ok 1 - first on-add handler fires
  [Sitemap]     ok 2 - second on-add handler fires too, not replaced
  [Sitemap]     ok 3 - both handlers see the same number of URLs
  [Sitemap]     1..3
  [Sitemap] ok 32 - Multiple on-add handlers all fire
  [Sitemap] # Subtest: Repeated links to a subdir index file are not re-added
  [Sitemap]     ok 1 - sub/ added exactly once despite repeated links (concurrency=1)
  [Sitemap]     ok 2 - sub/index.html never added as its own URL (concurrency=1)
  [Sitemap]     ok 3 - No duplicate URLs (concurrency=1)
  [Sitemap]     ok 4 - sub/ added exactly once despite repeated links (concurrency=4)
  [Sitemap]     ok 5 - sub/index.html never added as its own URL (concurrency=4)
  [Sitemap]     ok 6 - No duplicate URLs (concurrency=4)
  [Sitemap]     1..6
  [Sitemap] ok 33 - Repeated links to a subdir index file are not re-added
  [Sitemap] # Subtest: Entry fallback sorts case-insensitively
  [Sitemap]     ok 1 - apple.html precedes Zebra.html (byte-sort would pick Zebra)
  [Sitemap]     1..1
  [Sitemap] ok 34 - Entry fallback sorts case-insensitively
  [Sitemap] # Subtest: No-index root: clean root URL + sibling pages discovered
  [Sitemap]     ok 1 - Root "/" URL added exactly once
  [Sitemap]     ok 2 - Root URL is not the literal "/./" form
  [Sitemap]     ok 3 - Root pages the fallback entry does not link to are still discovered
  [Sitemap]     ok 4 - parallel: sibling page discovered
  [Sitemap]     ok 5 - parallel: no duplicate URLs
  [Sitemap]     1..5
  [Sitemap] ok 35 - No-index root: clean root URL + sibling pages discovered
  [Sitemap] # Subtest: Root-relative "/" from a subdir resolves to the root, not the subdir
  [Sitemap]     ok 1 - Root URL present exactly once
  [Sitemap]     ok 2 - Linking page discovered
  [Sitemap]     ok 3 - href="/" from a subdir page does not resolve to the subdir itself
  [Sitemap]     1..3
  [Sitemap] ok 36 - Root-relative "/" from a subdir resolves to the root, not the subdir
  [Sitemap] # Subtest: Root index expansion discovers unlinked root pages
  [Sitemap]     ok 1 - Root URL present
  [Sitemap]     ok 2 - Root pages not linked from index.html are discovered (like subdir siblings)
  [Sitemap]     ok 3 - No duplicate URLs
  [Sitemap]     1..3
  [Sitemap] ok 37 - Root index expansion discovers unlinked root pages
  [Sitemap] # Subtest: urls-found and on-done report the scan results
  [Sitemap]     ok 1 - urls-found matches builder item count
  [Sitemap]     ok 2 - on-done received the discovered items
  [Sitemap]     1..2
  [Sitemap] ok 38 - urls-found and on-done report the scan results
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/10-jsonld.rakutest
  [Sitemap] 1..42
  [Sitemap] # Subtest: extract-jsonld — single block
  [Sitemap]     ok 1 - One object extracted
  [Sitemap]     ok 2 - Headline correct
  [Sitemap]     1..2
  [Sitemap] ok 1 - extract-jsonld — single block
  [Sitemap] # Subtest: extract-jsonld — multiple blocks
  [Sitemap]     ok 1 - Two objects extracted
  [Sitemap]     ok 2 - First headline correct
  [Sitemap]     ok 3 - Second name correct
  [Sitemap]     1..3
  [Sitemap] ok 2 - extract-jsonld — multiple blocks
  [Sitemap] # Subtest: extract-jsonld — array body
  [Sitemap]     ok 1 - Two items from array
  [Sitemap]     1..1
  [Sitemap] ok 3 - extract-jsonld — array body
  [Sitemap] # Subtest: extract-jsonld — JS comments stripped
  [Sitemap]     ok 1 - One object despite comments
  [Sitemap]     ok 2 - Headline correct
  [Sitemap]     1..2
  [Sitemap] ok 4 - extract-jsonld — JS comments stripped
  [Sitemap] # Subtest: extract-jsonld — HTML comment wrapper stripped
  [Sitemap]     ok 1 - One object extracted
  [Sitemap]     1..1
  [Sitemap] ok 5 - extract-jsonld — HTML comment wrapper stripped
  [Sitemap] # Subtest: extract-jsonld — malformed JSON returns empty
  [Sitemap]     ok 1 - Malformed JSON returns empty list
  [Sitemap]     1..1
  [Sitemap] ok 6 - extract-jsonld — malformed JSON returns empty
  [Sitemap] # Subtest: find-by-type — exact match
  [Sitemap]     ok 1 - One VideoObject found
  [Sitemap]     ok 2 - Correct item returned
  [Sitemap]     1..2
  [Sitemap] ok 7 - find-by-type — exact match
  [Sitemap] # Subtest: find-by-type — @graph unwraps
  [Sitemap]     ok 1 - VideoObject found inside @graph
  [Sitemap]     ok 2 - Correct item from @graph
  [Sitemap]     1..2
  [Sitemap] ok 8 - find-by-type — @graph unwraps
  [Sitemap] # Subtest: find-by-type — no match
  [Sitemap]     ok 1 - No match returns empty list
  [Sitemap]     1..1
  [Sitemap] ok 9 - find-by-type — no match
  [Sitemap] # Subtest: find-by-type — generic Article does NOT match NewsArticle
  [Sitemap]     ok 1 - Article type does not match NewsArticle
  [Sitemap]     ok 2 - Article does not match ReportageNewsArticle
  [Sitemap]     1..2
  [Sitemap] ok 10 - find-by-type — generic Article does NOT match NewsArticle
  [Sitemap] # Subtest: find-by-type — BlogPosting does NOT match news types
  [Sitemap]     ok 1 - BlogPosting does not match NewsArticle
  [Sitemap]     ok 2 - BlogPosting does not match ReportageNewsArticle
  [Sitemap]     1..2
  [Sitemap] ok 11 - find-by-type — BlogPosting does NOT match news types
  [Sitemap] # Subtest: find-by-type — schema.org URL prefixes match
  [Sitemap]     ok 1 - https://schema.org/NewsArticle matches NewsArticle
  [Sitemap]     ok 2 - http://schema.org/NewsArticle matches NewsArticle
  [Sitemap]     ok 3 - schema:NewsArticle matches NewsArticle
  [Sitemap]     1..3
  [Sitemap] ok 12 - find-by-type — schema.org URL prefixes match
  [Sitemap] # Subtest: extract-video-objects — all fields mapped
  [Sitemap]     ok 1 - One video extracted
  [Sitemap]     ok 2 - contentUrl mapped
  [Sitemap]     ok 3 - thumbnailUrl mapped
  [Sitemap]     ok 4 - name mapped to title
  [Sitemap]     ok 5 - description mapped
  [Sitemap]     ok 6 - duration PT1H2M3S = 3723s
  [Sitemap]     ok 7 - uploadDate mapped
  [Sitemap]     1..7
  [Sitemap] ok 13 - extract-video-objects — all fields mapped
  [Sitemap] # Subtest: extract-video-objects — url fallback
  [Sitemap]     ok 1 - Video found via url fallback
  [Sitemap]     ok 2 - url used as contentUrl
  [Sitemap]     1..2
  [Sitemap] ok 14 - extract-video-objects — url fallback
  [Sitemap] # Subtest: extract-video-objects — ImageObject thumbnail
  [Sitemap]     ok 1 - ImageObject.url extracted
  [Sitemap]     1..1
  [Sitemap] ok 15 - extract-video-objects — ImageObject thumbnail
  [Sitemap] # Subtest: extract-video-objects — missing url skipped
  [Sitemap]     ok 1 - Video without contentUrl or url skipped
  [Sitemap]     1..1
  [Sitemap] ok 16 - extract-video-objects — missing url skipped
  [Sitemap] # Subtest: extract-news-objects — basic NewsArticle
  [Sitemap]     ok 1 - One news item extracted
  [Sitemap]     ok 2 - Publication name correct
  [Sitemap]     ok 3 - Language correct
  [Sitemap]     ok 4 - Headline mapped to title
  [Sitemap]     ok 5 - Publication date is DateTime
  [Sitemap]     ok 6 - Fresh article not stale
  [Sitemap]     1..6
  [Sitemap] ok 17 - extract-news-objects — basic NewsArticle
  [Sitemap] # Subtest: extract-news-objects — named subtypes match
  [Sitemap]     ok 1 - ReportageNewsArticle matches news extraction
  [Sitemap]     ok 2 - OpinionNewsArticle matches news extraction
  [Sitemap]     ok 3 - ReviewNewsArticle matches news extraction
  [Sitemap]     ok 4 - AnalysisNewsArticle matches news extraction
  [Sitemap]     ok 5 - BackgroundNewsArticle matches news extraction
  [Sitemap]     1..5
  [Sitemap] ok 18 - extract-news-objects — named subtypes match
  [Sitemap] # Subtest: extract-news-objects — stale detection
  [Sitemap]     ok 1 - Old article still returned
  [Sitemap]     ok 2 - Old article marked stale
  [Sitemap]     1..2
  [Sitemap] ok 19 - extract-news-objects — stale detection
  [Sitemap] # Subtest: extract-news-objects — missing publisher skipped
  [Sitemap]     ok 1 - Article without publisher skipped
  [Sitemap]     1..1
  [Sitemap] ok 20 - extract-news-objects — missing publisher skipped
  [Sitemap] # Subtest: extract-news-objects — missing headline skipped
  [Sitemap]     ok 1 - Article without headline skipped
  [Sitemap]     1..1
  [Sitemap] ok 21 - extract-news-objects — missing headline skipped
  [Sitemap] # Subtest: extract-news-objects — invalid date skipped
  [Sitemap]     ok 1 - Article with invalid date skipped
  [Sitemap]     1..1
  [Sitemap] ok 22 - extract-news-objects — invalid date skipped
  [Sitemap] # Subtest: extract-news-objects — generic Article does NOT match
  [Sitemap]     ok 1 - Generic Article not extracted as news
  [Sitemap]     1..1
  [Sitemap] ok 23 - extract-news-objects — generic Article does NOT match
  [Sitemap] # Subtest: extract-news-objects — BlogPosting does NOT match
  [Sitemap]     ok 1 - BlogPosting not extracted as news
  [Sitemap]     1..1
  [Sitemap] ok 24 - extract-news-objects — BlogPosting does NOT match
  [Sitemap] # Subtest: parse-iso8601-duration — edge cases
  [Sitemap]     ok 1 - PT1H2M3S = 3723s
  [Sitemap]     ok 2 - PT30S = 30s
  [Sitemap]     ok 3 - PT0S = 0s
  [Sitemap]     ok 4 - P0D = 0s
  [Sitemap]     ok 5 - PT bare = 0s
  [Sitemap]     ok 6 - P7D = 604800s
  [Sitemap]     ok 7 - P1W = 604800s
  [Sitemap]     ok 8 - P2W = 1209600s
  [Sitemap]     ok 9 - P3W4D = 3 weeks + 4 days
  [Sitemap]     ok 10 - Invalid string = 0s
  [Sitemap]     ok 11 - PT1.5H = 5400s (fractional hours)
  [Sitemap]     ok 12 - PT0.5M = 30s (fractional minutes)
  [Sitemap]     ok 13 - PT0.5S = 0s (fraction truncated to Int)
  [Sitemap]     ok 14 - P1.5D = 129600s (fractional days)
  [Sitemap]     ok 15 - PT1.5H30M = 7200s (fraction mixed with ints)
  [Sitemap]     ok 16 - PT12.5S = 12s (fraction truncated)
  [Sitemap]     ok 17 - P1.5W = 907200s (fractional weeks)
  [Sitemap]     ok 18 - P1Y rejected: years have no fixed second value
  [Sitemap]     ok 19 - P2M rejected: months have no fixed second value
  [Sitemap]     ok 20 - Y/M in the date part rejected, even with valid time parts
  [Sitemap]     ok 21 - P1Y6M rejected
  [Sitemap]     ok 22 - Minutes in the TIME part still convert
  [Sitemap]     ok 23 - P-1D rejected: durations are non-negative
  [Sitemap]     ok 24 - -P1D rejected: durations are non-negative
  [Sitemap]     ok 25 - PT-1S rejected: durations are non-negative
  [Sitemap]     1..25
  [Sitemap] ok 25 - parse-iso8601-duration — edge cases
  [Sitemap] # Subtest: extract-jsonld — robust script tag matching
  [Sitemap]     ok 1 - Scripts with extra attrs/spacing/case all extracted
  [Sitemap]     ok 2 - Unquoted attribute value matched
  [Sitemap]     ok 3 - Trailing attribute after type matched
  [Sitemap]     1..3
  [Sitemap] ok 26 - extract-jsonld — robust script tag matching
  [Sitemap] # Subtest: find-by-type — deeply nested document
  [Sitemap]     ok 1 - Deeply nested VideoObject found
  [Sitemap]     ok 2 - Deep item content correct
  [Sitemap]     1..2
  [Sitemap] ok 27 - find-by-type — deeply nested document
  [Sitemap] # Subtest: array thumbnailUrl / inLanguage / publisher no longer crash
  [Sitemap]     ok 1 - video extracted from array-bearing object
  [Sitemap]     ok 2 - first array element used for thumbnail
  [Sitemap]     ok 3 - first array element used for title
  [Sitemap]     1..3
  [Sitemap] ok 28 - array thumbnailUrl / inLanguage / publisher no longer crash
  [Sitemap] # Subtest: relative contentUrl/thumbnail resolve against page URL
  [Sitemap]     ok 1 - video extracted
  [Sitemap]     ok 2 - relative contentUrl resolved against page URL
  [Sitemap]     ok 3 - relative thumbnailUrl resolved against page URL
  [Sitemap]     1..3
  [Sitemap] ok 29 - relative contentUrl/thumbnail resolve against page URL
  [Sitemap] # Subtest: coerce-media-url handles Hash elements in arrays
  [Sitemap]     ok 1 - video extracted from Hash-bearing contentUrl array
  [Sitemap]     ok 2 - Hash element contributes its url key
  [Sitemap]     ok 3 - Hash element falls back to contentUrl
  [Sitemap]     1..3
  [Sitemap] ok 30 - coerce-media-url handles Hash elements in arrays
  [Sitemap] # Subtest: empty provided @jsonld list is trusted, not re-parsed
  [Sitemap]     ok 1 - caller-supplied empty parse result is authoritative
  [Sitemap]     ok 2 - omitted @jsonld argument parses the document
  [Sitemap]     1..2
  [Sitemap] ok 31 - empty provided @jsonld list is trusted, not re-parsed
  [Sitemap] # Subtest: video seen-check runs on resolved URLs
  [Sitemap]     ok 1 - relative JSON-LD twin deduped after resolution
  [Sitemap]     ok 2 - the surviving video is the resolved URL
  [Sitemap]     1..2
  [Sitemap] ok 32 - video seen-check runs on resolved URLs
  [Sitemap] # Subtest: extract-jsonld ignores data-type attribute (not a type attribute)
  [Sitemap]     ok 1 - data-type="application/ld+json" is not treated as JSON-LD
  [Sitemap]     ok 2 - type="application/ld+json" is still extracted correctly
  [Sitemap]     1..2
  [Sitemap] ok 33 - extract-jsonld ignores data-type attribute (not a type attribute)
  [Sitemap] # Subtest: bare-number duration counts as seconds
  [Sitemap]     ok 1 - JSON number 90 parses as 90 seconds (not 0)
  [Sitemap]     ok 2 - string "90" parses as 90 seconds
  [Sitemap]     ok 3 - ISO-8601 duration still parses
  [Sitemap]     ok 4 - signed durations still rejected
  [Sitemap]     1..4
  [Sitemap] ok 34 - bare-number duration counts as seconds
  [Sitemap] # Subtest: same @id via @graph and top level dedupes
  [Sitemap]     ok 1 - one record for a shared @id (top-level + @graph)
  [Sitemap]     ok 2 - URL correct
  [Sitemap]     1..2
  [Sitemap] ok 35 - same @id via @graph and top level dedupes
  [Sitemap] # Subtest: nested MediaObject URL merges into the wrapper record
  [Sitemap]     ok 1 - nested media twin does not double-publish the video
  [Sitemap]     ok 2 - nested MediaObject URL wins
  [Sitemap]     ok 3 - outer name merged into the record
  [Sitemap]     ok 4 - outer thumbnail merged
  [Sitemap]     ok 5 - outer uploadDate merged
  [Sitemap]     ok 6 - identical nested URL collapses to one record
  [Sitemap]     1..6
  [Sitemap] ok 36 - nested MediaObject URL merges into the wrapper record
  [Sitemap] # Subtest: @id-less VideoObjects with the same URL dedupe
  [Sitemap]     ok 1 - two @id-less objects with the same URL collapse to one
  [Sitemap]     ok 2 - URL correct
  [Sitemap]     1..2
  [Sitemap] ok 37 - @id-less VideoObjects with the same URL dedupe
  [Sitemap] # Subtest: extract-videos-for-item wires JSON-LD uploadDate into publication-date
  [Sitemap]     ok 1 - one video extracted from the page
  [Sitemap]     ok 2 - content-loc set
  [Sitemap]     ok 3 - JSON-LD uploadDate wired into publication-date
  [Sitemap]     1..3
  [Sitemap] ok 38 - extract-videos-for-item wires JSON-LD uploadDate into publication-date
  [Sitemap] # Subtest: </script> inside a JSON string does not truncate the block
  [Sitemap]     ok 1 - block extracted despite literal </script> in a string
  [Sitemap]     ok 2 - full string content preserved
  [Sitemap]     ok 3 - news object parsed from the full block
  [Sitemap]     1..3
  [Sitemap] ok 39 - </script> inside a JSON string does not truncate the block
  [Sitemap] # Subtest: inline // comments stripped, protocol-relative URLs preserved
  [Sitemap]     ok 1 - object parsed despite inline // comment
  [Sitemap]     ok 2 - protocol-relative URL inside a string is not treated as a comment
  [Sitemap]     1..2
  [Sitemap] ok 40 - inline // comments stripped, protocol-relative URLs preserved
  [Sitemap] # Subtest: nested url array in an ImageObject is reduced to a single URL
  [Sitemap]     ok 1 - video extracted
  [Sitemap]     ok 2 - nested url array reduced to a single URL (first element)
  [Sitemap]     1..2
  [Sitemap] ok 41 - nested url array in an ImageObject is reduced to a single URL
  [Sitemap] # Subtest: extract-page-assets max-videos caps videos per page
  [Sitemap]     ok 1 - default max-videos caps 120 videos at 100
  [Sitemap]     ok 2 - :max-videos(50) caps videos at 50
  [Sitemap]     1..2
  [Sitemap] ok 42 - extract-page-assets max-videos caps videos per page
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/11-news-sitemap.rakutest
  [Sitemap] 1..9
  [Sitemap] # Subtest: DirScanner extracts news via --news
  [Sitemap]     ok 1 - News builder returned
  [Sitemap]     ok 2 - One news item in builder
  [Sitemap]     ok 3 - Publication correct
  [Sitemap]     ok 4 - Title correct
  [Sitemap]     1..4
  [Sitemap] ok 1 - DirScanner extracts news via --news
  [Sitemap] # Subtest: News builder gets correct items with full fields
  [Sitemap]     ok 1 - One news item
  [Sitemap]     ok 2 - Language correct
  [Sitemap]     ok 3 - Date is DateTime
  [Sitemap]     1..3
  [Sitemap] ok 2 - News builder gets correct items with full fields
  [Sitemap] # Subtest: Stale articles filtered out
  [Sitemap]     ok 1 - Stale article filtered
  [Sitemap]     1..1
  [Sitemap] ok 3 - Stale articles filtered out
  [Sitemap] # Subtest: No news when flag off
  [Sitemap]     ok 1 - News builder is Nil without flag
  [Sitemap]     1..1
  [Sitemap] ok 4 - No news when flag off
  [Sitemap] # Subtest: Multiple news articles on one page via @graph
  [Sitemap]     ok 1 - One page with news
  [Sitemap]     ok 2 - Two news items on page
  [Sitemap]     1..2
  [Sitemap] ok 5 - Multiple news articles on one page via @graph
  [Sitemap] # Subtest: Mixed fresh and stale on same page
  [Sitemap]     ok 1 - One page with news
  [Sitemap]     ok 2 - Only fresh article kept
  [Sitemap]     ok 3 - Fresh article preserved
  [Sitemap]     1..3
  [Sitemap] ok 6 - Mixed fresh and stale on same page
  [Sitemap] # Subtest: News sitemap XML output structure
  [Sitemap]     ok 1 - News sitemap file written
  [Sitemap]     ok 2 - Contains news:news tag
  [Sitemap]     ok 3 - Contains publication name
  [Sitemap]     ok 4 - Contains news title
  [Sitemap]     1..4
  [Sitemap] ok 7 - News sitemap XML output structure
  [Sitemap] # Subtest: @graph NewsArticle is found
  [Sitemap]     ok 1 - NewsArticle inside @graph found
  [Sitemap]     ok 2 - Title correct
  [Sitemap]     1..2
  [Sitemap] ok 8 - @graph NewsArticle is found
  [Sitemap] # Subtest: ReportageNewsArticle works end-to-end
  [Sitemap]     ok 1 - ReportageNewsArticle extracted
  [Sitemap]     ok 2 - Title correct
  [Sitemap]     ok 3 - Publication correct
  [Sitemap]     1..3
  [Sitemap] ok 9 - ReportageNewsArticle works end-to-end
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/12-site-tree.rakutest
  [Sitemap] 1..23
  [Sitemap] # Subtest: basic creation
  [Sitemap]     ok 1 - root stub is empty
  [Sitemap]     ok 2 - root depth is 0
  [Sitemap]     ok 3 - root segments is empty
  [Sitemap]     ok 4 - root full-url
  [Sitemap]     1..4
  [Sitemap] ok 1 - basic creation
  [Sitemap] # Subtest: add-child
  [Sitemap]     ok 1 - child stub
  [Sitemap]     ok 2 - child parent is root
  [Sitemap]     ok 3 - root depth unchanged
  [Sitemap]     ok 4 - child depth 1
  [Sitemap]     ok 5 - child segments
  [Sitemap]     ok 6 - child full-url
  [Sitemap]     1..6
  [Sitemap] ok 2 - add-child
  [Sitemap] # Subtest: nested children
  [Sitemap]     ok 1 - nested depth 2
  [Sitemap]     ok 2 - nested segments
  [Sitemap]     ok 3 - nested full-url
  [Sitemap]     1..3
  [Sitemap] ok 3 - nested children
  [Sitemap] # Subtest: segments handles the root empty list
  [Sitemap]     ok 1 - root segments is empty
  [Sitemap]     ok 2 - segments returns a List (empty root list is cached, not re-walked)
  [Sitemap]     1..2
  [Sitemap] ok 4 - segments handles the root empty list
  [Sitemap] # Subtest: tree visualization
  [Sitemap]     ok 1 - tree contains blog
  [Sitemap]     ok 2 - tree has bullet points
  [Sitemap]     1..2
  [Sitemap] ok 5 - tree visualization
  [Sitemap] # Subtest: flatten
  [Sitemap]     ok 1 - flatten includes root, blog, post1, post2
  [Sitemap]     ok 2 - first is root
  [Sitemap]     ok 3 - second is blog
  [Sitemap]     1..3
  [Sitemap] ok 6 - flatten
  [Sitemap] # Subtest: to-builder
  [Sitemap]     ok 1 - builder has 3 items (root + 2 children)
  [Sitemap]     ok 2 - xml contains page1
  [Sitemap]     ok 3 - xml contains page2
  [Sitemap]     1..3
  [Sitemap] ok 7 - to-builder
  [Sitemap] # Subtest: changefreq coercion
  [Sitemap]     ok 1 - lowercase Str coerced to enum
  [Sitemap]     ok 2 - mixed-case Str coerced to enum
  [Sitemap]     ok 3 - enum passes through unchanged
  [Sitemap]     ok 4 - invalid changefreq dropped
  [Sitemap]     1..4
  [Sitemap] ok 8 - changefreq coercion
  [Sitemap] # Subtest: to-builder forwards all item fields
  [Sitemap]     ok 1 - title forwarded
  [Sitemap]     ok 2 - expires forwarded
  [Sitemap]     ok 3 - changefreq forwarded
  [Sitemap]     1..3
  [Sitemap] ok 9 - to-builder forwards all item fields
  [Sitemap] # Subtest: to-builder emits the falsy always changefreq
  [Sitemap]     ok 1 - always changefreq forwarded through to-builder
  [Sitemap]     ok 2 - always changefreq rendered
  [Sitemap]     1..2
  [Sitemap] ok 10 - to-builder emits the falsy always changefreq
  [Sitemap] # Subtest: to-builder forwards android/amp links
  [Sitemap]     ok 1 - android-link forwarded
  [Sitemap]     ok 2 - amp-link forwarded
  [Sitemap]     ok 3 - Renders android:link
  [Sitemap]     ok 4 - Renders amp:link
  [Sitemap]     1..4
  [Sitemap] ok 11 - to-builder forwards android/amp links
  [Sitemap] # Subtest: wire-parents
  [Sitemap]     ok 1 - blog parent is home
  [Sitemap]     ok 2 - post parent is blog
  [Sitemap]     ok 3 - home has 1 child
  [Sitemap]     ok 4 - blog has 1 child
  [Sitemap]     1..4
  [Sitemap] ok 12 - wire-parents
  [Sitemap] # Subtest: duplicate stub detection
  [Sitemap]     ok 1 - dies on duplicate
  [Sitemap]     1..1
  [Sitemap] ok 13 - duplicate stub detection
  [Sitemap] # Subtest: add-child stub is URL-safe
  [Sitemap]     ok 1 - stub '' rejected
  [Sitemap]     ok 2 - stub '/' rejected
  [Sitemap]     ok 3 - stub '..' rejected
  [Sitemap]     ok 4 - stub 'a/b' rejected
  [Sitemap]     ok 5 - stub 'a b' rejected
  [Sitemap]     ok 6 - stub 'a?b' rejected
  [Sitemap]     ok 7 - stub 'a \#b' rejected
  [Sitemap]     ok 8 - stub 'a..b' rejected
  [Sitemap]     ok 9 - stub 'a:b' rejected
  [Sitemap]     ok 10 - stub '.' rejected
  [Sitemap]     ok 11 - stub 'a;b' rejected
  [Sitemap]     ok 12 - stub 'a	b' rejected
  [Sitemap]     ok 13 - valid stub bound
  [Sitemap]     ok 14 - dots/underscores allowed
  [Sitemap]     ok 15 - leading dash allowed
  [Sitemap]     ok 16 - only valid child attached
  [Sitemap]     1..16
  [Sitemap] ok 14 - add-child stub is URL-safe
  [Sitemap] # Subtest: wire-parents missing parent
  [Sitemap]     ok 1 - dies on missing parent
  [Sitemap]     1..1
  [Sitemap] ok 15 - wire-parents missing parent
  [Sitemap] # Subtest: cycle detection in wire-parents
  [Sitemap]     ok 1 - mutual parent-stub references die
  [Sitemap]     1..1
  [Sitemap] ok 16 - cycle detection in wire-parents
  [Sitemap] # Subtest: cycle detection in attach-child
  [Sitemap]     ok 1 - attaching an ancestor as its own descendant dies
  [Sitemap]     1..1
  [Sitemap] ok 17 - cycle detection in attach-child
  [Sitemap] # Subtest: attach-child reparents: child leaves its previous parent
  [Sitemap]     ok 1 - child starts under branch
  [Sitemap]     ok 2 - root does not list child
  [Sitemap]     ok 3 - child moved to root
  [Sitemap]     ok 4 - branch no longer lists child
  [Sitemap]     ok 5 - root lists child exactly once
  [Sitemap]     ok 6 - root lists the same child object
  [Sitemap]     1..6
  [Sitemap] ok 18 - attach-child reparents: child leaves its previous parent
  [Sitemap] # Subtest: to-hash serializes the live parent, not a stale parent-stub
  [Sitemap]     ok 1 - live parent is new
  [Sitemap]     ok 2 - to-hash prefers the live parent over the stale stub
  [Sitemap]     ok 3 - round-trip parent-stub matches the live parent
  [Sitemap]     ok 4 - unattached node keeps its parent-stub
  [Sitemap]     1..4
  [Sitemap] ok 19 - to-hash serializes the live parent, not a stale parent-stub
  [Sitemap] # Subtest: from-hash stays linear for deep chains
  [Sitemap]     ok 1 - from-hash rebuilt a 15000-node chain in 0.29s (<15s)
  [Sitemap]     ok 2 - Deepest node reachable by walking the chain
  [Sitemap]     ok 3 - Deepest node depth correct after the rebuild
  [Sitemap]     ok 4 - Deepest node segments cover the chain below the root
  [Sitemap]     1..4
  [Sitemap] ok 20 - from-hash stays linear for deep chains
  [Sitemap] # Subtest: reparent invalidates cached depth/segments of an uncached ancestor
  [Sitemap]     ok 1 - grandchild depth cached at 3
  [Sitemap]     ok 2 - grandchild segments cached
  [Sitemap]     ok 3 - grandchild depth recomputed after reparenting its uncached ancestor
  [Sitemap]     ok 4 - grandchild segments recomputed after reparenting its uncached ancestor
  [Sitemap]     ok 5 - reparented ancestor depth updated
  [Sitemap]     ok 6 - reparented ancestor segments updated
  [Sitemap]     1..6
  [Sitemap] ok 21 - reparent invalidates cached depth/segments of an uncached ancestor
  [Sitemap] # Subtest: to-builder auto-priority uses the shared depth formula
  [Sitemap]     ok 1 - depth 0 (root) auto-priority 1.0
  [Sitemap]     ok 2 - depth 1 auto-priority 0.8
  [Sitemap]     ok 3 - depth 2 auto-priority 0.6
  [Sitemap]     ok 4 - depth 3 auto-priority 0.4
  [Sitemap]     ok 5 - depth 4 auto-priority 0.2 (not clamped at 0.4)
  [Sitemap]     ok 6 - depth 5+ auto-priority floors at 0.1
  [Sitemap]     1..6
  [Sitemap] ok 22 - to-builder auto-priority uses the shared depth formula
  [Sitemap] # Subtest: add-child builds a deep chain in linear time (A10)
  [Sitemap]     ok 1 - 5000-deep add-child chain built in 0.13s (<30s)
  [Sitemap]     ok 2 - deepest leaf depth correct
  [Sitemap]     ok 3 - deepest leaf segments cover the whole chain
  [Sitemap]     ok 4 - innermost segment is the chain tail
  [Sitemap]     ok 5 - outermost segment is the chain head
  [Sitemap]     ok 6 - full-url still produces a string for the rebuilt tree
  [Sitemap]     1..6
  [Sitemap] ok 23 - add-child builds a deep chain in linear time (A10)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/13-site-tree-yaml.rakutest
  [Sitemap] 1..9
  [Sitemap] # Subtest: Image roundtrip
  [Sitemap]     ok 1 - url
  [Sitemap]     ok 2 - caption
  [Sitemap]     ok 3 - title defaults to empty
  [Sitemap]     ok 4 - geo-location defaults
  [Sitemap]     1..4
  [Sitemap] ok 1 - Image roundtrip
  [Sitemap] # Subtest: Video roundtrip
  [Sitemap]     ok 1 - thumbnail-loc
  [Sitemap]     ok 2 - title
  [Sitemap]     ok 3 - content-loc
  [Sitemap]     ok 4 - duration
  [Sitemap]     ok 5 - tags
  [Sitemap]     ok 6 - description defaults to empty
  [Sitemap]     ok 7 - family-friendly tri-state: unspecified stays unset
  [Sitemap]     1..7
  [Sitemap] ok 2 - Video roundtrip
  [Sitemap] # Subtest: Link roundtrip
  [Sitemap]     ok 1 - lang
  [Sitemap]     ok 2 - url
  [Sitemap]     1..2
  [Sitemap] ok 3 - Link roundtrip
  [Sitemap] # Subtest: News roundtrip
  [Sitemap]     ok 1 - publication
  [Sitemap]     ok 2 - title
  [Sitemap]     ok 3 - publication-date
  [Sitemap]     ok 4 - keywords
  [Sitemap]     ok 5 - stock-tickers defaults to empty
  [Sitemap]     1..5
  [Sitemap] ok 4 - News roundtrip
  [Sitemap] # Subtest: News edge cases
  [Sitemap]     ok 1 - News without publication-date constructs
  [Sitemap]     ok 2 - publication-date stays undefined
  [Sitemap]     ok 3 - DateTime instance survives from-hash
  [Sitemap]     ok 4 - ISO string parsed by from-hash
  [Sitemap]     1..4
  [Sitemap] ok 5 - News edge cases
  [Sitemap] # Subtest: Item roundtrip
  [Sitemap]     ok 1 - url
  [Sitemap]     ok 2 - lastmod
  [Sitemap]     ok 3 - changefreq
  [Sitemap]     ok 4 - priority
  [Sitemap]     ok 5 - title
  [Sitemap]     ok 6 - images count
  [Sitemap]     ok 7 - videos count
  [Sitemap]     ok 8 - links count
  [Sitemap]     ok 9 - news count
  [Sitemap]     ok 10 - image caption preserved
  [Sitemap]     ok 11 - link lang preserved
  [Sitemap]     1..11
  [Sitemap] ok 6 - Item roundtrip
  [Sitemap] # Subtest: SiteTree roundtrip
  [Sitemap]     ok 1 - root stub
  [Sitemap]     ok 2 - root depth
  [Sitemap]     ok 3 - root has 2 children
  [Sitemap]     ok 4 - 5 nodes total (root + blog + 2 posts + about)
  [Sitemap]     ok 5 - blog stub
  [Sitemap]     ok 6 - blog depth
  [Sitemap]     ok 7 - blog has item
  [Sitemap]     ok 8 - blog changefreq
  [Sitemap]     ok 9 - blog priority
  [Sitemap]     ok 10 - first-post stub
  [Sitemap]     ok 11 - first-post depth
  [Sitemap]     ok 12 - first-post url
  [Sitemap]     ok 13 - second-post stub
  [Sitemap]     ok 14 - second-post priority
  [Sitemap]     ok 15 - about stub
  [Sitemap]     ok 16 - about depth
  [Sitemap]     1..16
  [Sitemap] ok 7 - SiteTree roundtrip
  [Sitemap] # Subtest: YAML roundtrip
  [Sitemap]     ok 1 - yaml contains blog
  [Sitemap]     ok 2 - yaml contains first-post
  [Sitemap]     ok 3 - yaml contains priority
  [Sitemap]     ok 4 - 1 child after from-yaml
  [Sitemap]     ok 5 - blog stub after roundtrip
  [Sitemap]     ok 6 - first-post stub after roundtrip
  [Sitemap]     ok 7 - second serialization matches first
  [Sitemap]     1..7
  [Sitemap] ok 8 - YAML roundtrip
  [Sitemap] # Subtest: Edge cases
  [Sitemap]     ok 1 - deep nesting preserves all 6 nodes
  [Sitemap]     ok 2 - deepest node has depth 5
  [Sitemap]     ok 3 - deepest stub preserved
  [Sitemap]     ok 4 - simple stub preserved
  [Sitemap]     ok 5 - no item when none was set
  [Sitemap]     ok 6 - from-hash tolerates missing parent-stub
  [Sitemap]     ok 7 - parent-stub stays undefined
  [Sitemap]     ok 8 - empty item hash stays a defined item
  [Sitemap]     ok 9 - empty item round-trips with default fields
  [Sitemap]     1..9
  [Sitemap] ok 9 - Edge cases
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/14-cli.rakutest
  [Sitemap] 1..35
  [Sitemap] ok 1 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 2 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 3 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 4 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 5 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 6 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 7 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 8 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 9 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 10 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 11 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 12 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 13 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 14 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 15 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 16 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 17 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 18 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 19 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 20 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 21 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 22 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 23 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 24 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 25 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 26 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 27 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 28 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 29 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 30 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 31 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 32 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 33 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 34 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 35 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/15-fetcher.rakutest
  [Sitemap] 1..25
  [Sitemap] # Subtest: fetch-recursive dedups concurrent child writes
  [Sitemap]     ok 1 - Two children saved for duplicate locs
  [Sitemap]     ok 2 - Children paths are distinct
  [Sitemap]     ok 3 - Child file exists: test-index/child.xml
  [Sitemap]     ok 4 - Child file has content: test-index/child.xml
  [Sitemap]     ok 5 - Child file exists: test-index/child-0.xml
  [Sitemap]     ok 6 - Child file has content: test-index/child-0.xml
  [Sitemap]     1..6
  [Sitemap] ok 1 - fetch-recursive dedups concurrent child writes
  [Sitemap] # Subtest: fetch-recursive keeps distinct files for distinct URLs mapping to the same name
  [Sitemap]     ok 1 - Both colliding children saved
  [Sitemap]     ok 2 - Distinct files assigned to colliding names
  [Sitemap]     ok 3 - First child keeps the plain name
  [Sitemap]     ok 4 - Second child gets a suffixed name starting at -0
  [Sitemap]     ok 5 - Child file exists: test-index2/child.xml
  [Sitemap]     ok 6 - Child file has content: test-index2/child.xml
  [Sitemap]     ok 7 - Child file exists: test-index2/child-0.xml
  [Sitemap]     ok 8 - Child file has content: test-index2/child-0.xml
  [Sitemap]     1..8
  [Sitemap] ok 2 - fetch-recursive keeps distinct files for distinct URLs mapping to the same name
  [Sitemap] # Subtest: fetch-recursive rewrites index <loc> to local paths
  [Sitemap]     ok 1 - Saved index no longer points at remote child URLs
  [Sitemap]     ok 2 - Rewritten index has one <loc> per fetched child
  [Sitemap]     ok 3 - Rewritten index <loc> 'test-index3/child.xml' exists on disk
  [Sitemap]     ok 4 - Rewritten index <loc> 'test-index3/child.xml' is a local path, not a URL
  [Sitemap]     ok 5 - Rewritten index <loc> 'test-index3/child-0.xml' exists on disk
  [Sitemap]     ok 6 - Rewritten index <loc> 'test-index3/child-0.xml' is a local path, not a URL
  [Sitemap]     ok 7 - lastmod carried over into the rewritten index
  [Sitemap]     1..7
  [Sitemap] ok 3 - fetch-recursive rewrites index <loc> to local paths
  [Sitemap] # Subtest: fetch-recursive extensionless -o derives index file + child dir
  [Sitemap]     ok 1 - extensionless -o gains the format extension for the index file
  [Sitemap]     ok 2 - child directory derived from the extensionless stem
  [Sitemap]     ok 3 - index file written as noext.xml, not a directory
  [Sitemap]     ok 4 - child written into the noext/ directory
  [Sitemap]     1..4
  [Sitemap] ok 4 - fetch-recursive extensionless -o derives index file + child dir
  [Sitemap] # Subtest: fetch-recursive does not overwrite pre-existing child
  [Sitemap]     ok 1 - Original child file untouched
  [Sitemap]     ok 2 - New child written to distinct file
  [Sitemap]     1..2
  [Sitemap] ok 5 - fetch-recursive does not overwrite pre-existing child
  [Sitemap] # Subtest: fetch-recursive refuses .. in output dir even with --force
  [Sitemap]     ok 1 - fetch-recursive dies on .. output path
  [Sitemap]     ok 2 - victim directory not deleted by --force
  [Sitemap]     1..2
  [Sitemap] ok 6 - fetch-recursive refuses .. in output dir even with --force
  [Sitemap] # Subtest: fetch-recursive refuses an absolute -o outside the current directory, allows one inside
  [Sitemap]     ok 1 - fetch-recursive dies on an absolute -o path outside the current directory
  [Sitemap]     ok 2 - nothing written outside the current directory
  [Sitemap]     ok 3 - no output directory created outside the current directory
  [Sitemap]     ok 4 - recursive absolute -o inside the current directory is accepted
  [Sitemap]     ok 5 - absolute index rewritten with local child path
  [Sitemap]     ok 6 - absolute children directory created inside the current directory
  [Sitemap]     1..6
  [Sitemap] ok 7 - fetch-recursive refuses an absolute -o outside the current directory, allows one inside
  [Sitemap] # Subtest: fetch-recursive refuses -o through an intermediate symlink
  [Sitemap]     # Subtest: fetch-recursive dies when -o resolves outside the current directory
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'outside the current directory'/
  [Sitemap]     ok 1 - fetch-recursive dies when -o resolves outside the current directory
  [Sitemap]     ok 2 - the symlink target was not deleted
  [Sitemap]     ok 3 - nothing written through the intermediate symlink
  [Sitemap]     1..3
  [Sitemap] ok 8 - fetch-recursive refuses -o through an intermediate symlink
  [Sitemap] # Subtest: fetch-recursive defaults to same-host children with a cap
  [Sitemap]     ok 1 - 127.0.0.2 (foreign-host string) child excluded, same-host children fetched
  [Sitemap]     ok 2 - --follow-foreign-children fetches 127.0.0.2 child too
  [Sitemap]     ok 3 - max-children caps the number of fetched children
  [Sitemap]     1..3
  [Sitemap] ok 9 - fetch-recursive defaults to same-host children with a cap
  [Sitemap] # Subtest: fetch-recursive skips non-XML leaf responses
  [Sitemap]     ok 1 - HTML leaf skipped, only XML child saved
  [Sitemap]     1..1
  [Sitemap] ok 10 - fetch-recursive skips non-XML leaf responses
  [Sitemap] # Subtest: is-sitemap-index anchors detection to the root
  [Sitemap]     ok 1 - real index detected
  [Sitemap]     ok 2 - plain urlset is not an index
  [Sitemap]     ok 3 - sitemapindex inside a comment is not an index
  [Sitemap]     ok 4 - HTML mentioning sitemapindex is not an index
  [Sitemap]     ok 5 - BOM + xml-decl index detected
  [Sitemap]     ok 6 - urlset with a sitemapindex comment saved as a leaf, not an index
  [Sitemap]     ok 7 - leaf file written
  [Sitemap]     ok 8 - leaf content preserved
  [Sitemap]     1..8
  [Sitemap] ok 11 - is-sitemap-index anchors detection to the root
  [Sitemap] # Subtest: fetch-recursive --force handles short dir names and file-blocked out-dirs
  [Sitemap]     ok 1 - stale file removed from short-named out-dir
  [Sitemap]     ok 2 - child written into short-named out-dir
  [Sitemap]     ok 3 - regular file removed and replaced with out-dir
  [Sitemap]     ok 4 - child written into new out-dir
  [Sitemap]     # Subtest: fetch-recursive dies when out-dir is an existing file without --force
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / existing ' ' file /
  [Sitemap]     ok 5 - fetch-recursive dies when out-dir is an existing file without --force
  [Sitemap]     ok 6 - blocking file untouched
  [Sitemap]     1..6
  [Sitemap] ok 12 - fetch-recursive --force handles short dir names and file-blocked out-dirs
  [Sitemap] # Subtest: fetch-recursive --force removes nested stale directories
  [Sitemap]     ok 1 - new child written into the replaced out-dir
  [Sitemap]     ok 2 - stale top-level file removed
  [Sitemap]     ok 3 - nested stale directory removed
  [Sitemap]     ok 4 - deeply nested stale directory removed
  [Sitemap]     ok 5 - stale file in deepest subtree removed
  [Sitemap]     ok 6 - only the new child remains in the out-dir
  [Sitemap]     1..6
  [Sitemap] ok 13 - fetch-recursive --force removes nested stale directories
  [Sitemap] # Subtest: discover-sitemap normalizes schemeless domains
  [Sitemap]     ok 1 - explicit http scheme discovery reads robots.txt
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap]     ok 2 - schemeless domain normalized to https:// in fallback message
  [Sitemap]     1..2
  [Sitemap] ok 14 - discover-sitemap normalizes schemeless domains
  [Sitemap] # Subtest: output-filename strips query/fragment via URI parsing
  [Sitemap]     ok 1 - query string does not leak into the filename
  [Sitemap]     ok 2 - fragment does not leak into the filename
  [Sitemap]     ok 3 - gz + query handled, path context preserved
  [Sitemap]     ok 4 - host-only URL derives stem from the host
  [Sitemap]     ok 5 - query stripped across formats
  [Sitemap]     ok 6 - local file behavior unchanged
  [Sitemap]     ok 7 - uppercase scheme still treated as a URL
  [Sitemap]     ok 8 - host stem strips www. prefix and TLD
  [Sitemap]     ok 9 - www. stripped and multi-part TLD (co.uk) stripped
  [Sitemap]     ok 10 - multi-part TLD (com.au) stripped with both labels
  [Sitemap]     ok 11 - multi-part TLD (org.uk) stripped with both labels
  [Sitemap]     1..11
  [Sitemap] ok 15 - output-filename strips query/fragment via URI parsing
  [Sitemap] # Subtest: fetch-recursive resolves relative child locs
  [Sitemap]     ok 1 - Relative child loc resolved against the index URL and fetched
  [Sitemap]     ok 2 - Child file exists
  [Sitemap]     ok 3 - Child file has content
  [Sitemap]     1..3
  [Sitemap] ok 16 - fetch-recursive resolves relative child locs
  [Sitemap] # Subtest: fetch-recursive records failed children
  [Sitemap]     ok 1 - Good child still saved
  [Sitemap]     ok 2 - Failed child recorded in <errors>
  [Sitemap]     ok 3 - Error mentions the HTTP status
  [Sitemap]     1..3
  [Sitemap] ok 17 - fetch-recursive records failed children
  [Sitemap] # Subtest: fetch-recursive fails loudly on an empty top-level body
  [Sitemap]     # Subtest: empty top-level body dies with a clear message
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / 'empty response body' /
  [Sitemap]     ok 1 - empty top-level body dies with a clear message
  [Sitemap]     1..1
  [Sitemap] ok 18 - fetch-recursive fails loudly on an empty top-level body
  [Sitemap] # Subtest: fetch-recursive records an empty child body as an error
  [Sitemap]     ok 1 - empty child body saved no file
  [Sitemap]     ok 2 - empty child body recorded as an error
  [Sitemap]     ok 3 - error message names the empty body, not a fetch failure
  [Sitemap]     1..3
  [Sitemap] ok 19 - fetch-recursive records an empty child body as an error
  [Sitemap] # Subtest: fetch-recursive skips converted output when nothing was fetched
  [Sitemap]     ok 1 - no children from an empty index
  [Sitemap]     ok 2 - no converted output key when there is nothing to convert
  [Sitemap]     ok 3 - no empty converted file left behind
  [Sitemap]     1..3
  [Sitemap] ok 20 - fetch-recursive skips converted output when nothing was fetched
  [Sitemap] # Subtest: discover-sitemap honors --no-verify-ssl
  [Sitemap] .....+...+....+......+.........+...+...+.....+...+.........+.+++++++++++++++++++++++++++++++++++++++*.+..+++++++++++++++++++++++++++++++++++++++*.+...................+......++++++
  [Sitemap] .+......+...+......+++++++++++++++++++++++++++++++++++++++*.+...+.....+...+............+++++++++++++++++++++++++++++++++++++++*........+.......+........+..........+...........+....+..+...+............+..........+......+........+.......+....................+...+.+...............+...+......+..+...++++++
  [Sitemap] -----
  [Sitemap]     ok 1 - openssl generated a self-signed certificate
  [Sitemap]     ok 2 - verify=True fails against the self-signed cert
  [Sitemap]     ok 3 - ssl-verify(False) reads robots.txt and returns the sitemap URL
  [Sitemap]     1..3
  [Sitemap] ok 21 - discover-sitemap honors --no-verify-ssl
  [Sitemap] # Subtest: Fetcher exported subs are package-accessible
  [Sitemap]     ok 1 - fetch reachable qualified
  [Sitemap]     ok 2 - get-decompressed-content reachable qualified
  [Sitemap]     ok 3 - output-filename callable qualified
  [Sitemap]     ok 4 - format-output reachable qualified
  [Sitemap]     ok 5 - discover-sitemap reachable qualified
  [Sitemap]     1..5
  [Sitemap] ok 22 - Fetcher exported subs are package-accessible
  [Sitemap] # Subtest: fetch-recursive accepts BOM/comment/DOCTYPE-prefixed children
  [Sitemap]     ok 1 - BOM/comment/DOCTYPE children all saved
  [Sitemap]     1..1
  [Sitemap] ok 23 - fetch-recursive accepts BOM/comment/DOCTYPE-prefixed children
  [Sitemap] # Subtest: fetch-recursive default dir name is portable (host:port colon sanitized)
  [Sitemap]     ok 1 - derived dir uses dashes for dots: 127-0-0-1-20110-index
  [Sitemap]     ok 2 - no colon in the derived directory name
  [Sitemap]     1..2
  [Sitemap] ok 24 - fetch-recursive default dir name is portable (host:port colon sanitized)
  [Sitemap] # Subtest: fetch follows same-origin redirects but refuses cross-origin (SSRF guard)
  [Sitemap]     ok 1 - same-origin redirect is followed and returns the sitemap
  [Sitemap]     ok 2 - cross-origin redirect returns no content
  [Sitemap]     ok 3 - error message names the cross-origin refusal
  [Sitemap]     1..3
  [Sitemap] ok 25 - fetch follows same-origin redirects but refuses cross-origin (SSRF guard)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/16-config.rakutest
  [Sitemap] 1..24
  [Sitemap] # Subtest: read-bounded-body rejects an oversized declared Content-Length
  [Sitemap]     # Subtest: Oversized Content-Length rejected before reading
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches rx/declared \s+ body \s+ length/
  [Sitemap]     ok 1 - Oversized Content-Length rejected before reading
  [Sitemap]     ok 2 - Body stream is not tapped for oversized Content-Length
  [Sitemap]     1..2
  [Sitemap] ok 1 - read-bounded-body rejects an oversized declared Content-Length
  [Sitemap] # Subtest: read-bounded-body aborts an over-cap body mid-stream
  [Sitemap]     # Subtest: Over-cap body aborts mid-stream
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /body \s+ exceeds/
  [Sitemap]     ok 1 - Over-cap body aborts mid-stream
  [Sitemap]     ok 2 - cancel() invoked to abort the download
  [Sitemap]     1..2
  [Sitemap] ok 2 - read-bounded-body aborts an over-cap body mid-stream
  [Sitemap] # Subtest: read-bounded-body returns in-range bodies
  [Sitemap]     ok 1 - In-range body assembled from stream chunks
  [Sitemap]     ok 2 - cancel() not called for an in-range body
  [Sitemap]     1..2
  [Sitemap] ok 3 - read-bounded-body returns in-range bodies
  [Sitemap] # Subtest: read-bounded-body ignores an unparseable Content-Length
  [Sitemap]     ok 1 - Unparseable Content-Length falls back to the streaming cap
  [Sitemap]     1..1
  [Sitemap] ok 4 - read-bounded-body ignores an unparseable Content-Length
  [Sitemap] # Subtest: fetch rejects an oversized body via the declared length
  [Sitemap]     # Subtest: fetch() rejects a response with an oversized Content-Length
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches rx/declared \s+ body \s+ length/
  [Sitemap]     ok 1 - fetch() rejects a response with an oversized Content-Length
  [Sitemap]     1..1
  [Sitemap] ok 5 - fetch rejects an oversized body via the declared length
  [Sitemap] # Subtest: read-bounded-body aborts a chunked HTTP body over the cap
  [Sitemap]     ok 1 - Chunked response has no Content-Length
  [Sitemap]     # Subtest: Chunked over-cap body aborts mid-stream over real HTTP
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /body \s+ exceeds/
  [Sitemap]     ok 2 - Chunked over-cap body aborts mid-stream over real HTTP
  [Sitemap]     1..2
  [Sitemap] ok 6 - read-bounded-body aborts a chunked HTTP body over the cap
  [Sitemap] # Subtest: fetch-robots decompresses a gzip-encoded robots.txt
  [Sitemap]     ok 1 - Actions parsed from gzip-encoded robots.txt
  [Sitemap]     ok 2 - No fetch error on success
  [Sitemap]     ok 3 - Crawl-delay parsed from gzip content
  [Sitemap]     ok 4 - Disallow rule honored
  [Sitemap]     ok 5 - Allowed path unaffected
  [Sitemap]     ok 6 - Sitemap entry parsed from gzip content
  [Sitemap]     1..6
  [Sitemap] ok 7 - fetch-robots decompresses a gzip-encoded robots.txt
  [Sitemap] # Subtest: discover-sitemaps refuses sitemaps on a foreign host (SSRF guard)
  [Sitemap]     ok 1 - same-origin sitemap is kept
  [Sitemap]     ok 2 - scheme-relative sitemap resolves to the same origin and is kept
  [Sitemap]     ok 3 - foreign-host sitemap is refused
  [Sitemap]     1..3
  [Sitemap] ok 8 - discover-sitemaps refuses sitemaps on a foreign host (SSRF guard)
  [Sitemap] # Subtest: fetch-robots rejects an oversized robots.txt
  [Sitemap]     ok 1 - Oversized robots.txt yields no actions (bounded read)
  [Sitemap]     1..1
  [Sitemap] ok 9 - fetch-robots rejects an oversized robots.txt
  [Sitemap] # Subtest: decode-text-body falls back to latin-1 for invalid UTF-8
  [Sitemap]     ok 1 - Valid UTF-8 decoded as-is
  [Sitemap]     ok 2 - Pure ASCII decoded
  [Sitemap]     ok 3 - Invalid UTF-8 byte falls back to latin-1 code point
  [Sitemap]     1..3
  [Sitemap] ok 10 - decode-text-body falls back to latin-1 for invalid UTF-8
  [Sitemap] # Subtest: normalize-origin and same-origin are port-aware
  [Sitemap]     ok 1 - Default port 80 dropped, host lowercased
  [Sitemap]     ok 2 - Default port 443 dropped
  [Sitemap]     ok 3 - Non-default port preserved
  [Sitemap]     ok 4 - Bare hostname has no origin
  [Sitemap]     ok 5 - Default-port variants are the same origin
  [Sitemap]     ok 6 - https default-port variants are the same origin
  [Sitemap]     ok 7 - Different ports are not the same origin
  [Sitemap]     ok 8 - Different schemes are not the same origin
  [Sitemap]     ok 9 - Origin-less URL never matches
  [Sitemap]     1..9
  [Sitemap] ok 11 - normalize-origin and same-origin are port-aware
  [Sitemap] # Subtest: resolve-relative-url resolves relative sitemap locs
  [Sitemap]     ok 1 - Bare relative resolved against base directory
  [Sitemap]     ok 2 - Root-relative resolved against origin
  [Sitemap]     ok 3 - Parent-relative collapses one level
  [Sitemap]     ok 4 - Multi-segment relative path resolved
  [Sitemap]     ok 5 - Dot segment folded away
  [Sitemap]     ok 6 - Resolved against a root-level sitemap
  [Sitemap]     ok 7 - Absolute loc returned unchanged
  [Sitemap]     ok 8 - Scheme-relative loc inherits the scheme
  [Sitemap]     ok 9 - Scheme-relative ref against an empty-scheme context is Nil, not ://x/y
  [Sitemap]     ok 10 - Non-default port preserved
  [Sitemap]     ok 11 - Unparseable base yields Nil (A2) rather than silently echoing the reference
  [Sitemap]     ok 12 - Query-only ref keeps the base path (was /sitemaps/?page=2)
  [Sitemap]     ok 13 - Fragment-only ref keeps the base path (was /sitemaps/ \#top)
  [Sitemap]     ok 14 - Query-only ref replaces the base query
  [Sitemap]     ok 15 - Fragment-only ref keeps the base query
  [Sitemap]     1..15
  [Sitemap] ok 12 - resolve-relative-url resolves relative sitemap locs
  [Sitemap] # Subtest: normalize-start-url guarantees a usable scheme
  [Sitemap]     ok 1 - Bare domain gets https:// prepended
  [Sitemap]     ok 2 - Bare domain with a path keeps the path
  [Sitemap]     ok 3 - Scheme-relative //host becomes https
  [Sitemap]     ok 4 - Explicit http URL unchanged
  [Sitemap]     ok 5 - Explicit https URL unchanged
  [Sitemap]     ok 6 - Uppercase scheme is left alone
  [Sitemap]     1..6
  [Sitemap] ok 13 - normalize-start-url guarantees a usable scheme
  [Sitemap] # Subtest: decompress-content :lenient decodes invalid UTF-8 losslessly
  [Sitemap]     ok 1 - :lenient does not throw on invalid UTF-8
  [Sitemap]     ok 2 - utf8-c8 round-trips the original bytes
  [Sitemap]     ok 3 - Valid UTF-8 still decodes normally without :lenient
  [Sitemap]     1..3
  [Sitemap] ok 14 - decompress-content :lenient decodes invalid UTF-8 losslessly
  [Sitemap] # Subtest: decompress-content decodes every member of a multi-member gzip
  [Sitemap]     ok 1 - All concatenated gzip members decoded, not just the first
  [Sitemap]     ok 2 - A single member still decodes
  [Sitemap]     1..2
  [Sitemap] ok 15 - decompress-content decodes every member of a multi-member gzip
  [Sitemap] # Subtest: canonical-origin and normalize-origin share one implementation
  [Sitemap]     ok 1 - canonical-origin lowercases scheme/host and drops the default port
  [Sitemap]     ok 2 - canonical-origin(URI) and normalize-origin(Str) agree
  [Sitemap]     ok 3 - canonical-origin preserves a non-default port
  [Sitemap]     ok 4 - canonical-origin drops the https default port
  [Sitemap]     ok 5 - canonical-origin yields Nil for a scheme without an http(s) host (A9)
  [Sitemap]     1..5
  [Sitemap] ok 16 - canonical-origin and normalize-origin share one implementation
  [Sitemap] # Subtest: normalize-http-url is the single URL normalizer used by Item
  [Sitemap]     ok 1 - scheme/host lowercased, default port dropped
  [Sitemap]     ok 2 - https default port dropped
  [Sitemap]     ok 3 - non-default port preserved
  [Sitemap]     ok 4 - userinfo survives the default-port strip
  [Sitemap]     ok 5 - IPv6 default port dropped
  [Sitemap]     ok 6 - bare http URL unchanged
  [Sitemap]     ok 7 - non-http scheme returned unchanged
  [Sitemap]     ok 8 - query preserved
  [Sitemap]     ok 9 - Item TWEAK delegates to normalize-http-url
  [Sitemap]     1..9
  [Sitemap] ok 17 - normalize-http-url is the single URL normalizer used by Item
  [Sitemap] # Subtest: cached-client caps the pool with FIFO eviction
  [Sitemap]     ok 1 - oldest client evicted once the pool exceeds the cap
  [Sitemap]     ok 2 - next-oldest evicted in FIFO order
  [Sitemap]     ok 3 - most recent client still pooled
  [Sitemap]     1..3
  [Sitemap] ok 18 - cached-client caps the pool with FIFO eviction
  [Sitemap] # Subtest: detect-input-type: existing files win over URL heuristics
  [Sitemap]     ok 1 - existing dotted path is a file
  [Sitemap]     ok 2 - same path missing is neither (denylisted ext)
  [Sitemap]     ok 3 - bare domain is url
  [Sitemap]     ok 4 - ccTLD-looking domain is url
  [Sitemap]     ok 5 - host with port is url
  [Sitemap]     ok 6 - scheme always wins over denylist
  [Sitemap]     ok 7 - denylisted ext, missing file is neither
  [Sitemap]     1..7
  [Sitemap] ok 19 - detect-input-type: existing files win over URL heuristics
  [Sitemap] # Subtest: cached-client keys follow mode into the pool
  [Sitemap]     ok 1 - follow=False gets a dedicated client, not the auto-follow one
  [Sitemap]     ok 2 - follow=False clients are pooled among themselves
  [Sitemap]     1..2
  [Sitemap] ok 20 - cached-client keys follow mode into the pool
  [Sitemap] # Subtest: resolve-relative-url splits at first of ? or # (no .. leak)
  [Sitemap]     ok 1 - fragment containing ? no longer leaks a literal ..
  [Sitemap]     ok 2 - fragment content preserved verbatim
  [Sitemap]     ok 3 - normal ?-before- \# unchanged
  [Sitemap]     ok 4 - path dot-segments still collapse
  [Sitemap]     ok 5 - a relative ref splits at the fragment first; ../ inside it is untouched
  [Sitemap]     1..5
  [Sitemap] ok 21 - resolve-relative-url splits at first of ? or  \# (no .. leak)
  [Sitemap] # Subtest: resolve-relative-url: trailing . segment normalizes like a slash (RFC 3986 5.2.4)
  [Sitemap]     ok 1 - "/a/." collapses to "/a/", not "/a"
  [Sitemap]     ok 2 - relative "a/." also keeps the trailing slash
  [Sitemap]     ok 3 - interior dot-segments unchanged
  [Sitemap]     ok 4 - a trailing ".." folds like a trailing "." and keeps the slash
  [Sitemap]     ok 5 - a bare ".." resolves to the parent directory with its slash
  [Sitemap]     ok 6 - a ".." back at the root leaves a lone slash, not an empty path
  [Sitemap]     1..6
  [Sitemap] ok 22 - resolve-relative-url: trailing . segment normalizes like a slash (RFC 3986 5.2.4)
  [Sitemap] # Subtest: normalize-http-url drops zero-padded default ports; origins keep non-http ports
  [Sitemap]     ok 1 - ":0080" normalizes like ":80" (numeric comparison, not Str eq)
  [Sitemap]     ok 2 - path/query/fragment survive default-port stripping
  [Sitemap]     ok 3 - non-numeric port garbage is preserved, not coerced
  [Sitemap]     ok 4 - userinfo and non-default ports untouched
  [Sitemap]     ok 5 - distinct explicit ports on a non-http(s) scheme are distinct origins
  [Sitemap]     1..5
  [Sitemap] ok 23 - normalize-http-url drops zero-padded default ports; origins keep non-http ports
  [Sitemap] # Subtest: fifo-evict keeps the map bounded and drops oldest keys (CQ-F7)
  [Sitemap]     ok 1 - batch keeps order at/below cap (got 10)
  [Sitemap]     ok 2 - map size tracks order size after batch
  [Sitemap]     ok 3 - oldest key evicted
  [Sitemap]     ok 4 - newest key survives
  [Sitemap]     ok 5 - order head advanced past evicted keys
  [Sitemap]     ok 6 - half strategy drops half of 20
  [Sitemap]     ok 7 - map size follows after half eviction
  [Sitemap]     ok 8 - oldest half evicted
  [Sitemap]     ok 9 - newest half survives
  [Sitemap]     ok 10 - one strategy drops exactly one
  [Sitemap]     ok 11 - oldest single key evicted
  [Sitemap]     ok 12 - newest survives
  [Sitemap]     ok 13 - no eviction below the cap
  [Sitemap]     ok 14 - map untouched below the cap
  [Sitemap]     1..14
  [Sitemap] ok 24 - fifo-evict keeps the map bounded and drops oldest keys (CQ-F7)
  ===> Testing [OK] for Sitemap:ver<0.0.1>:auth<zef:sasha>
  ===> Installing: Sitemap:ver<0.0.1>:auth<zef:sasha>
  ===> Install [OK] for Sitemap:ver<0.0.1>:auth<zef:sasha>

  1 bin/ script [sitemap] installed to:
  /tmp/xuG6MARERs/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 12min 10.521s
               CPU time consumed: 12min 8.366s
                     Memory peak: 3G (swap: 1G)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p497553-i485333.service; invocation ID: db11ff6fce5f408eb3edd3eaf0daecf2
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Sitemap
  ===> Found: Sitemap:ver<0.0.1>:auth<zef:sasha> [via Zef::Repository::Ecosystems<fez>]
  [Sitemap] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788478123.497565.6278.125995534078/af1773e4378f172b4c420c4738db2912543073e5.tar.gz https://360.zef.pm/S/IT/SITEMAP/af1773e4378f172b4c420c4738db2912543073e5.tar.gz
  ===> Fetching [OK]: Sitemap:ver<0.0.1>:auth<zef:sasha> to /home/coke/sandbox/blin/data/zef-data/tmp/1788478123.497565.6278.125995534078/af1773e4378f172b4c420c4738db2912543073e5.tar.gz
  [Sitemap] Command: tar -t -f ./af1773e4378f172b4c420c4738db2912543073e5.tar.gz
  [Sitemap] Command: tar -xvf ./af1773e4378f172b4c420c4738db2912543073e5.tar.gz -C ../af1773e4378f172b4c420c4738db2912543073e5.tar.gz
  ===> Extraction [OK]: Sitemap to /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz
  ===> Testing: Sitemap:ver<0.0.1>:auth<zef:sasha>
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/01-item.rakutest
  [Sitemap] 1..23
  [Sitemap] # Subtest: Sitemap::Item - basic creation
  [Sitemap]     ok 1 - URL set correctly
  [Sitemap]     ok 2 - Priority set correctly
  [Sitemap]     ok 3 - lastmod not set
  [Sitemap]     ok 4 - changefreq not set
  [Sitemap]     1..4
  [Sitemap] ok 1 - Sitemap::Item - basic creation
  [Sitemap] # Subtest: Sitemap::Item - URL encoding
  [Sitemap]     ok 1 - URL is encoded
  [Sitemap]     1..1
  [Sitemap] ok 2 - Sitemap::Item - URL encoding
  [Sitemap] # Subtest: Sitemap::Item - URL normalization preserves port and userinfo
  [Sitemap]     ok 1 - Scheme/host lowercased, port and path preserved
  [Sitemap]     ok 2 - Userinfo case preserved, host lowercased
  [Sitemap]     ok 3 - Bare host unchanged
  [Sitemap]     1..3
  [Sitemap] ok 3 - Sitemap::Item - URL normalization preserves port and userinfo
  [Sitemap] # Subtest: Sitemap::Item - add-image
  [Sitemap]     ok 1 - Image added
  [Sitemap]     ok 2 - Image URL correct
  [Sitemap]     ok 3 - Image caption correct
  [Sitemap]     1..3
  [Sitemap] ok 4 - Sitemap::Item - add-image
  [Sitemap] # Subtest: Sitemap::Item - add-video
  [Sitemap]     ok 1 - Video added
  [Sitemap]     ok 2 - Content URL correct
  [Sitemap]     ok 3 - Thumbnail correct
  [Sitemap]     ok 4 - Title correct
  [Sitemap]     1..4
  [Sitemap] ok 5 - Sitemap::Item - add-video
  [Sitemap] # Subtest: Sitemap::Item - add-link
  [Sitemap]     ok 1 - Link added
  [Sitemap]     ok 2 - Link URL correct
  [Sitemap]     1..2
  [Sitemap] ok 6 - Sitemap::Item - add-link
  [Sitemap] # Subtest: Sitemap::Item - add-news
  [Sitemap]     ok 1 - News added
  [Sitemap]     ok 2 - Publication correct
  [Sitemap]     ok 3 - Language correct
  [Sitemap]     ok 4 - Title correct
  [Sitemap]     1..4
  [Sitemap] ok 7 - Sitemap::Item - add-news
  [Sitemap] # Subtest: Sitemap::Item - write-xml
  [Sitemap]     ok 1 - Contains url element
  [Sitemap]     ok 2 - Contains domain
  [Sitemap]     ok 3 - Contains path
  [Sitemap]     ok 4 - Contains priority
  [Sitemap]     1..4
  [Sitemap] ok 8 - Sitemap::Item - write-xml
  [Sitemap] # Subtest: Sitemap::Item - from-hash changefreq coercion
  [Sitemap]     ok 1 - lowercase changefreq coerces to enum
  [Sitemap]     ok 2 - lowercase daily coerces
  [Sitemap]     ok 3 - uppercase weekly coerces
  [Sitemap]     # Subtest: invalid changefreq throws instead of silently dropping
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches / 'bogus' /
  [Sitemap]     ok 4 - invalid changefreq throws instead of silently dropping
  [Sitemap]     1..4
  [Sitemap] ok 9 - Sitemap::Item - from-hash changefreq coercion
  [Sitemap] # Subtest: Sitemap::Item - from-hash accepts DateTime lastmod
  [Sitemap]     ok 1 - DateTime lastmod survives from-hash
  [Sitemap]     ok 2 - DateTime value preserved
  [Sitemap]     ok 3 - ISO string still parsed by from-hash
  [Sitemap]     ok 4 - missing lastmod stays unset
  [Sitemap]     ok 5 - undef lastmod stays unset
  [Sitemap]     ok 6 - date-only lastmod gets DateOnly precision
  [Sitemap]     ok 7 - date-only lastmod round-trips through to-hash as 2024-01-15
  [Sitemap]     ok 8 - year-month lastmod gets YearMonth precision
  [Sitemap]     ok 9 - year-month lastmod round-trips through to-hash as 2024-01
  [Sitemap]     ok 10 - year-only lastmod gets Year precision
  [Sitemap]     ok 11 - year-only lastmod round-trips through to-hash as 2024
  [Sitemap]     ok 12 - full datetime keeps Precise precision
  [Sitemap]     ok 13 - full datetime round-trips unchanged
  [Sitemap]     ok 14 - from-hash consumes a persisted lastmod-precision key
  [Sitemap]     ok 15 - hash round-trip preserves the date-only form
  [Sitemap]     1..15
  [Sitemap] ok 10 - Sitemap::Item - from-hash accepts DateTime lastmod
  [Sitemap] # Subtest: Sitemap::Item - always changefreq is emitted despite being falsy
  [Sitemap]     ok 1 - Changefreq::Always rendered
  [Sitemap]     ok 2 - from-hash keeps changefreq=always
  [Sitemap]     ok 3 - to-hash round-trips the always changefreq
  [Sitemap]     ok 4 - from-hash keeps a raw Changefreq::Always enum (value 0)
  [Sitemap]     ok 5 - raw enum value preserved
  [Sitemap]     ok 6 - Unset changefreq still omitted
  [Sitemap]     1..6
  [Sitemap] ok 11 - Sitemap::Item - always changefreq is emitted despite being falsy
  [Sitemap] # Subtest: Sitemap::Item - from-hash accepts Pair and Pair-list nested elements
  [Sitemap]     ok 1 - itemized Hash element works
  [Sitemap]     ok 2 - image url parsed
  [Sitemap]     ok 3 - image caption parsed
  [Sitemap]     ok 4 - single-attr inline hash coerces to one image
  [Sitemap]     ok 5 - inline image url parsed
  [Sitemap]     ok 6 - itemized link element works
  [Sitemap]     ok 7 - link lang preserved
  [Sitemap]     ok 8 - link url preserved
  [Sitemap]     ok 9 - flattened inline link pair without url dies instead of building an empty link
  [Sitemap]     ok 10 - itemized video element works
  [Sitemap]     ok 11 - video content-loc preserved
  [Sitemap]     ok 12 - video thumbnail-loc preserved
  [Sitemap]     ok 13 - itemized news element works
  [Sitemap]     ok 14 - news title preserved
  [Sitemap]     1..14
  [Sitemap] ok 12 - Sitemap::Item - from-hash accepts Pair and Pair-list nested elements
  [Sitemap] # Subtest: Sitemap::Item - from-hash reports unparseable dates with a clear message
  [Sitemap]     ok 1 - Item.from-hash dies on an unparseable lastmod
  [Sitemap]     ok 2 - message names the offending value
  [Sitemap]     ok 3 - message names the item URL
  [Sitemap]     ok 4 - News.from-hash dies on an unparseable publication-date
  [Sitemap]     ok 5 - news message names the offending value
  [Sitemap]     ok 6 - news message names the title
  [Sitemap]     ok 7 - a parseable lastmod still round-trips
  [Sitemap]     ok 8 - a DateTime publication-date passes through unchanged
  [Sitemap]     1..8
  [Sitemap] ok 13 - Sitemap::Item - from-hash reports unparseable dates with a clear message
  [Sitemap] # Subtest: Sitemap::Item - from-hash requires mandatory fields instead of building empties
  [Sitemap]     ok 1 - Image.from-hash without url dies
  [Sitemap]     ok 2 - Link.from-hash without url dies
  [Sitemap]     ok 3 - Link.from-hash without lang dies
  [Sitemap]     ok 4 - Item.from-hash without url dies
  [Sitemap]     ok 5 - News.from-hash without publication dies
  [Sitemap]     ok 6 - News.from-hash without publication-language dies
  [Sitemap]     ok 7 - News.from-hash without title dies
  [Sitemap]     ok 8 - a hash with the mandatory url still builds
  [Sitemap]     1..8
  [Sitemap] ok 14 - Sitemap::Item - from-hash requires mandatory fields instead of building empties
  [Sitemap] # Subtest: Sitemap::Item - explicit default ports are stripped from URLs
  [Sitemap]     ok 1 - http :80 stripped
  [Sitemap]     ok 2 - https :443 stripped
  [Sitemap]     ok 3 - non-default https :80 preserved
  [Sitemap]     ok 4 - non-default http :443 preserved
  [Sitemap]     ok 5 - userinfo survives with the default port stripped
  [Sitemap]     ok 6 - uppercase default port stripped, path preserved
  [Sitemap]     ok 7 - IPv6 default port stripped
  [Sitemap]     ok 8 - IPv6 non-default port preserved
  [Sitemap]     1..8
  [Sitemap] ok 15 - Sitemap::Item - explicit default ports are stripped from URLs
  [Sitemap] # Subtest: Sitemap::Item::Video - renderable matches the Google spec
  [Sitemap]     ok 1 - thumbnail + content_loc is renderable
  [Sitemap]     ok 2 - thumbnail + player_loc is renderable without content_loc
  [Sitemap]     ok 3 - no thumbnail_loc is not renderable
  [Sitemap]     ok 4 - no content_loc and no player_loc is not renderable
  [Sitemap]     ok 5 - player_loc is emitted for a player-based video
  [Sitemap]     ok 6 - no content_loc element emitted when absent
  [Sitemap]     1..6
  [Sitemap] ok 16 - Sitemap::Item::Video - renderable matches the Google spec
  [Sitemap] # Subtest: W3CDTF output: no fractional seconds in lastmod / publication_date
  [Sitemap]     ok 1 - no fractional seconds anywhere in dates
  [Sitemap]     ok 2 - item lastmod is whole-second W3CDTF
  [Sitemap]     ok 3 - news publication_date truncated to seconds
  [Sitemap]     1..3
  [Sitemap] ok 17 - W3CDTF output: no fractional seconds in lastmod / publication_date
  [Sitemap] # Subtest: priority: scientific-notation values render as plain decimals
  [Sitemap]     ok 1 - 1e-05 renders expanded, not "1e-05.0"
  [Sitemap]     ok 2 - no exponent form in priority
  [Sitemap]     1..2
  [Sitemap] ok 18 - priority: scientific-notation values render as plain decimals
  [Sitemap] # Subtest: priority: sub-1e-10 values are preserved, not flattened to 0.0
  [Sitemap]     ok 1 - a 1e-11 priority renders as its real decimal, not "0.0"
  [Sitemap]     ok 2 - tiny priority is not flattened to 0.0
  [Sitemap]     1..2
  [Sitemap] ok 19 - priority: sub-1e-10 values are preserved, not flattened to 0.0
  [Sitemap] # Subtest: add-video Nil fields and add-news optional publication-date
  [Sitemap]     ok 1 - omitted title coalesces to a defined empty string
  [Sitemap]     ok 2 - omitted description coalesces to a defined empty string
  [Sitemap]     ok 3 - omitted thumbnail-loc coalesces to a defined empty string
  [Sitemap]     ok 4 - title defaults to empty string
  [Sitemap]     ok 5 - add-news works without a publication-date
  [Sitemap]     ok 6 - omitted publication-date stays undefined
  [Sitemap]     1..6
  [Sitemap] ok 20 - add-video Nil fields and add-news optional publication-date
  [Sitemap] # Subtest: from-hash enforces the 0.0..1.0 priority range
  [Sitemap]     # Subtest: out-of-range high priority throws
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches / '42' /
  [Sitemap]     ok 1 - out-of-range high priority throws
  [Sitemap]     # Subtest: negative priority throws
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches / '-3' /
  [Sitemap]     ok 2 - negative priority throws
  [Sitemap]     ok 3 - in-range priority preserved through from-hash
  [Sitemap]     1..3
  [Sitemap] ok 21 - from-hash enforces the 0.0..1.0 priority range
  [Sitemap] # Subtest: Video.from-hash floors ints, keeps rating Real, drops non-finite
  [Sitemap]     ok 1 - duration 1.9 floors to whole seconds
  [Sitemap]     ok 2 - view-count 2.9 floors to whole views
  [Sitemap]     ok 3 - rating keeps its fraction (Real) through from-hash
  [Sitemap]     ok 4 - Inf duration is dropped, not a "Cannot convert Inf to Int" crash
  [Sitemap]     ok 5 - NaN view-count is dropped
  [Sitemap]     ok 6 - 1e400 (overflow to Inf) duration is dropped
  [Sitemap]     1..6
  [Sitemap] ok 22 - Video.from-hash floors ints, keeps rating Real, drops non-finite
  [Sitemap] # Subtest: video dates render whole-second W3CDTF (canonical-date)
  [Sitemap]     ok 1 - expiration_date truncated to whole seconds, offset kept
  [Sitemap]     ok 2 - publication_date truncated to whole seconds with a TZD
  [Sitemap]     ok 3 - no fractional-second digits anywhere
  [Sitemap]     1..3
  [Sitemap] ok 23 - video dates render whole-second W3CDTF (canonical-date)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/02-builder.rakutest
  [Sitemap] 1..44
  [Sitemap] # Subtest: Sitemap::Builder - add-item
  [Sitemap]     ok 1 - Items added
  [Sitemap]     1..1
  [Sitemap] ok 1 - Sitemap::Builder - add-item
  [Sitemap] # Subtest: Sitemap::Builder - add-item with options
  [Sitemap]     ok 1 - Item added with options
  [Sitemap]     1..1
  [Sitemap] ok 2 - Sitemap::Builder - add-item with options
  [Sitemap] # Subtest: Sitemap::Builder - render
  [Sitemap]     ok 1 - Contains urlset element
  [Sitemap]     ok 2 - Contains first URL
  [Sitemap]     ok 3 - Contains second URL
  [Sitemap]     ok 4 - Contains namespace
  [Sitemap]     1..4
  [Sitemap] ok 3 - Sitemap::Builder - render
  [Sitemap] # Subtest: Sitemap::Builder - write to file
  [Sitemap]     ok 1 - File created
  [Sitemap]     ok 2 - File contains URL
  [Sitemap]     1..2
  [Sitemap] ok 4 - Sitemap::Builder - write to file
  [Sitemap] # Subtest: Sitemap::Builder - get-items
  [Sitemap]     ok 1 - Returns 2 items
  [Sitemap]     ok 2 - First item correct
  [Sitemap]     1..2
  [Sitemap] ok 5 - Sitemap::Builder - get-items
  [Sitemap] # Subtest: Sitemap::Builder - clear
  [Sitemap]     ok 1 - Has 1 item
  [Sitemap]     ok 2 - Cleared
  [Sitemap]     1..2
  [Sitemap] ok 6 - Sitemap::Builder - clear
  [Sitemap] # Subtest: Sitemap::Builder - render with XSL
  [Sitemap]     ok 1 - Contains stylesheet PI
  [Sitemap]     ok 2 - Contains text/xsl type
  [Sitemap]     ok 3 - Contains stylesheet URL
  [Sitemap]     1..3
  [Sitemap] ok 7 - Sitemap::Builder - render with XSL
  [Sitemap] # Subtest: Sitemap::Builder - gzip compression
  [Sitemap]     ok 1 - Compressed file created
  [Sitemap]     ok 2 - Contains urlset element
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains second URL
  [Sitemap]     1..4
  [Sitemap] ok 8 - Sitemap::Builder - gzip compression
  [Sitemap] # Subtest: Sitemap::Builder - write with .xml.gz path
  [Sitemap]     ok 1 - Plain (non-compressed) write keeps the literal .gz suffix
  [Sitemap]     ok 2 - No .gz-stripped file is written
  [Sitemap]     1..2
  [Sitemap] ok 9 - Sitemap::Builder - write with .xml.gz path
  [Sitemap] # Subtest: Sitemap::Builder - write keeps an explicit non-xml extension
  [Sitemap]     ok 1 - -o out.txt writes exactly out.txt
  [Sitemap]     ok 2 - No .xml suffix appended to an explicit extension
  [Sitemap]     ok 3 - File contains the item URL
  [Sitemap]     ok 4 - A bare stem still gains the .xml extension
  [Sitemap]     1..4
  [Sitemap] ok 10 - Sitemap::Builder - write keeps an explicit non-xml extension
  [Sitemap] # Subtest: Sitemap::Builder - write .gz and uppercase .XML paths normalize
  [Sitemap]     ok 1 - -o out.txt.gz (non-compressed) keeps the literal .gz suffix
  [Sitemap]     ok 2 - No .gz-stripped out.txt left behind
  [Sitemap]     ok 3 - No mangled out.txt.xml
  [Sitemap]     ok 4 - -o SITEMAP.XML normalizes to SITEMAP.xml (case-insensitive)
  [Sitemap]     ok 5 - The uppercase .XML path is not written literally
  [Sitemap]     1..5
  [Sitemap] ok 11 - Sitemap::Builder - write .gz and uppercase .XML paths normalize
  [Sitemap] # Subtest: Sitemap::Builder - .gz handling respects the compress flag
  [Sitemap]     ok 1 - compression off: out.xml.gz keeps the literal .gz suffix
  [Sitemap]     ok 2 - compression off: the .gz is not stripped
  [Sitemap]     ok 3 - compression off: an explicit .gz without .xml is kept whole
  [Sitemap]     ok 4 - compression off: bare foo.gz is not rewritten
  [Sitemap]     ok 5 - compression on: out.xml emits out.xml.gz
  [Sitemap]     ok 6 - compression on: out.xml.gz stays out.xml.gz
  [Sitemap]     1..6
  [Sitemap] ok 12 - Sitemap::Builder - .gz handling respects the compress flag
  [Sitemap] # Subtest: Sitemap::Builder - write multi-file with an explicit non-xml extension
  [Sitemap]     ok 1 - Chunk keeps the explicit extension with a -1 suffix
  [Sitemap]     ok 2 - Index file uses the explicit extension
  [Sitemap]     ok 3 - No stray .xml appended
  [Sitemap]     1..3
  [Sitemap] ok 13 - Sitemap::Builder - write multi-file with an explicit non-xml extension
  [Sitemap] # Subtest: Sitemap::Builder - render-index
  [Sitemap]     ok 1 - Contains sitemapindex element
  [Sitemap]     ok 2 - Contains first sitemap
  [Sitemap]     ok 3 - Contains second sitemap
  [Sitemap]     1..3
  [Sitemap] ok 14 - Sitemap::Builder - render-index
  [Sitemap] # Subtest: Sitemap::Builder - render-index requires base-url for relative locs
  [Sitemap]     # Subtest: Relative <loc> without :base-url dies instead of emitting a broken index
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'relative loc'/
  [Sitemap]     ok 1 - Relative <loc> without :base-url dies instead of emitting a broken index
  [Sitemap]     1..1
  [Sitemap] ok 15 - Sitemap::Builder - render-index requires base-url for relative locs
  [Sitemap] # Subtest: Sitemap::Builder - render-index base-url without doubled slash
  [Sitemap]     ok 1 - base-url without trailing slash joins once
  [Sitemap]     ok 2 - base-url with trailing slash joins without doubling
  [Sitemap]     ok 3 - all trailing slashes stripped
  [Sitemap]     ok 4 - no double slash anywhere
  [Sitemap]     1..4
  [Sitemap] ok 16 - Sitemap::Builder - render-index base-url without doubled slash
  [Sitemap] # Subtest: Sitemap::Builder - render-index trims leading slashes from relative locs
  [Sitemap]     ok 1 - leading slash of a root-relative loc is not doubled
  [Sitemap]     ok 2 - no double slash anywhere in the index
  [Sitemap]     ok 3 - a loc of '/' alone collapses to the bare base URL
  [Sitemap]     1..3
  [Sitemap] ok 17 - Sitemap::Builder - render-index trims leading slashes from relative locs
  [Sitemap] # Subtest: Sitemap::Builder - render-index absolute-loc check is case-insensitive
  [Sitemap]     ok 1 - uppercase-scheme loc passes through unchanged (not base-prefixed)
  [Sitemap]     ok 2 - non-http absolute loc passes through unchanged
  [Sitemap]     ok 3 - relative loc still base-prefixed
  [Sitemap]     1..3
  [Sitemap] ok 18 - Sitemap::Builder - render-index absolute-loc check is case-insensitive
  [Sitemap] # Subtest: Sitemap::Builder - render-index with XSL
  [Sitemap]     ok 1 - Contains stylesheet PI
  [Sitemap]     ok 2 - Contains sitemapindex element
  [Sitemap]     1..2
  [Sitemap] ok 19 - Sitemap::Builder - render-index with XSL
  [Sitemap] # Subtest: Sitemap::Builder - XSL + gzip compression
  [Sitemap]     ok 1 - Compressed file created
  [Sitemap]     ok 2 - Decompressed output contains stylesheet PI
  [Sitemap]     ok 3 - Contains text/xsl type
  [Sitemap]     ok 4 - Contains stylesheet URL
  [Sitemap]     1..4
  [Sitemap] ok 20 - Sitemap::Builder - XSL + gzip compression
  [Sitemap] # Subtest: Sitemap::Builder - XSL + multi-file split
  [Sitemap]     ok 1 - Chunk 1 created
  [Sitemap]     ok 2 - Chunk 1 contains stylesheet PI
  [Sitemap]     ok 3 - Chunk 2 created
  [Sitemap]     ok 4 - Chunk 2 contains stylesheet PI
  [Sitemap]     ok 5 - Index file created
  [Sitemap]     ok 6 - Index contains stylesheet PI
  [Sitemap]     1..6
  [Sitemap] ok 21 - Sitemap::Builder - XSL + multi-file split
  [Sitemap] # Subtest: Sitemap::Builder - write multi-file with compression
  [Sitemap]     ok 1 - Index file created
  [Sitemap]     ok 2 - Index contains sitemapindex
  [Sitemap]     1..2
  [Sitemap] ok 22 - Sitemap::Builder - write multi-file with compression
  [Sitemap] # Subtest: Sitemap::Builder - items below max-entries keep plain chunk name
  [Sitemap]     ok 1 - Items written to plain {stem}.xml (was -1.xml)
  [Sitemap]     ok 2 - No -1 chunk file created
  [Sitemap]     ok 3 - Single chunk contains the item
  [Sitemap]     ok 4 - Index references plain {stem}.xml
  [Sitemap]     1..4
  [Sitemap] ok 23 - Sitemap::Builder - items below max-entries keep plain chunk name
  [Sitemap] # Subtest: Sitemap::Builder - pretty printing
  [Sitemap]     ok 1 - Contains newlines (pretty)
  [Sitemap]     ok 2 - Contains indented tags
  [Sitemap]     1..2
  [Sitemap] ok 24 - Sitemap::Builder - pretty printing
  [Sitemap] # Subtest: Sitemap::Builder - no pretty printing
  [Sitemap]     ok 1 - Contains loc tag
  [Sitemap]     ok 2 - No indented loc tag
  [Sitemap]     1..2
  [Sitemap] ok 25 - Sitemap::Builder - no pretty printing
  [Sitemap] # Subtest: Sitemap::Builder - add-item with images
  [Sitemap]     ok 1 - Contains image element
  [Sitemap]     ok 2 - Contains image URL
  [Sitemap]     1..2
  [Sitemap] ok 26 - Sitemap::Builder - add-item with images
  [Sitemap] # Subtest: Sitemap::Builder - add-item with video
  [Sitemap]     ok 1 - Contains video element
  [Sitemap]     ok 2 - Contains video title
  [Sitemap]     ok 3 - xmlns:video declared when a video renders
  [Sitemap]     1..3
  [Sitemap] ok 27 - Sitemap::Builder - add-item with video
  [Sitemap] # Subtest: Sitemap::Builder - unrenderable video emits no element and no namespace
  [Sitemap]     ok 1 - video without thumbnail_loc is not emitted
  [Sitemap]     ok 2 - its title is not emitted either
  [Sitemap]     ok 3 - xmlns:video omitted when no renderable video
  [Sitemap]     ok 4 - video without content_loc is not emitted
  [Sitemap]     ok 5 - xmlns:video omitted when no renderable video
  [Sitemap]     1..5
  [Sitemap] ok 28 - Sitemap::Builder - unrenderable video emits no element and no namespace
  [Sitemap] # Subtest: Sitemap::Builder - render does not mutate caller items
  [Sitemap] Warning: dropping video (no content_loc/player_loc) for item https://example.com/video: thumbnail_loc plus content_loc or player_loc are required
  [Sitemap]     ok 1 - unrenderable video still dropped
  [Sitemap]     ok 2 - item.verbose untouched by a verbose builder
  [Sitemap]     ok 3 - renderable video emitted with the threaded verbose param
  [Sitemap]     ok 4 - item.verbose untouched even after a second render
  [Sitemap]     1..4
  [Sitemap] ok 29 - Sitemap::Builder - render does not mutate caller items
  [Sitemap] # Subtest: Sitemap::Builder - add-item-from preserves all fields
  [Sitemap]     ok 1 - changefreq preserved
  [Sitemap]     ok 2 - priority preserved
  [Sitemap]     ok 3 - non-standard url-level <title> is no longer emitted
  [Sitemap]     ok 4 - image preserved
  [Sitemap]     ok 5 - url preserved
  [Sitemap]     1..5
  [Sitemap] ok 30 - Sitemap::Builder - add-item-from preserves all fields
  [Sitemap] # Subtest: Sitemap::Builder - add-item-from deep-clones arrays
  [Sitemap]     ok 1 - builder copy still has the original image
  [Sitemap]     ok 2 - image added to original after add-item-from does not leak into builder
  [Sitemap]     1..2
  [Sitemap] ok 31 - Sitemap::Builder - add-item-from deep-clones arrays
  [Sitemap] # Subtest: Sitemap::Builder - add-item with android/amp links
  [Sitemap]     ok 1 - Renders android:link element
  [Sitemap]     ok 2 - Contains android link URL
  [Sitemap]     ok 3 - Renders amp:link element
  [Sitemap]     ok 4 - Contains amp link URL
  [Sitemap]     ok 5 - android namespace declared when android:link used
  [Sitemap]     ok 6 - amp namespace declared when amp:link used
  [Sitemap]     1..6
  [Sitemap] ok 32 - Sitemap::Builder - add-item with android/amp links
  [Sitemap] # Subtest: Sitemap::Builder - extension namespaces omitted when unused
  [Sitemap]     ok 1 - xmlns:android omitted when no android:link used
  [Sitemap]     ok 2 - xmlns:amp omitted when no amp:link used
  [Sitemap]     ok 3 - xmlns:xhtml omitted when no links used
  [Sitemap]     ok 4 - xmlns:image omitted when no images used
  [Sitemap]     ok 5 - xmlns:video omitted when no videos used
  [Sitemap]     ok 6 - xmlns:news omitted when no news used
  [Sitemap]     1..6
  [Sitemap] ok 33 - Sitemap::Builder - extension namespaces omitted when unused
  [Sitemap] # Subtest: Sitemap::Builder - add-item rejects unsupported object types
  [Sitemap]     # Subtest: Dies on unsupported image object
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'unsupported object type'/
  [Sitemap]     ok 1 - Dies on unsupported image object
  [Sitemap]     ok 2 - No item added after the die
  [Sitemap]     1..2
  [Sitemap] ok 34 - Sitemap::Builder - add-item rejects unsupported object types
  [Sitemap] # Subtest: Sitemap::Builder - xsl-url PI escapes only " and cannot break out
  [Sitemap]     ok 1 - & stays raw in the stylesheet PI
  [Sitemap]     ok 2 - " escaped in the stylesheet PI
  [Sitemap]     ok 3 - Raw & preserved so browsers receive the real URL
  [Sitemap]     ok 4 - PI keeps its shape with the real URL and the escaped quote
  [Sitemap]     ok 5 - < stays raw in the stylesheet PI
  [Sitemap]     ok 6 - < is not entity-escaped
  [Sitemap]     # Subtest: PI value containing ?> dies instead of injecting markup
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'xsl-url contains'/
  [Sitemap]     ok 7 - PI value containing ?> dies instead of injecting markup
  [Sitemap]     ok 8 - Index PI keeps the raw &
  [Sitemap]     1..8
  [Sitemap] ok 35 - Sitemap::Builder - xsl-url PI escapes only " and cannot break out
  [Sitemap] # Subtest: Sitemap::Builder - add-item coerces string attrs
  [Sitemap]     ok 1 - Item accepted with string attrs
  [Sitemap]     ok 2 - lastmod coerced to DateTime
  [Sitemap]     ok 3 - lastmod value preserved
  [Sitemap]     ok 4 - changefreq coerced case-insensitively
  [Sitemap]     ok 5 - priority coerced to Numeric
  [Sitemap]     ok 6 - XML emits coerced changefreq
  [Sitemap]     ok 7 - XML emits coerced priority
  [Sitemap]     # Subtest: Invalid lastmod string dies clearly
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'Invalid lastmod'/
  [Sitemap]     ok 8 - Invalid lastmod string dies clearly
  [Sitemap]     # Subtest: Invalid changefreq string dies clearly
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'Invalid changefreq'/
  [Sitemap]     ok 9 - Invalid changefreq string dies clearly
  [Sitemap]     # Subtest: Invalid priority string dies clearly
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'Invalid priority'/
  [Sitemap]     ok 10 - Invalid priority string dies clearly
  [Sitemap]     1..10
  [Sitemap] ok 36 - Sitemap::Builder - add-item coerces string attrs
  [Sitemap] # Subtest: Sitemap::Builder - whole priorities render as 1.0
  [Sitemap]     ok 1 - priority 1 renders as 1.0 (not bare 1)
  [Sitemap]     ok 2 - fractional priority unchanged
  [Sitemap]     ok 3 - multi-decimal priority not rounded
  [Sitemap]     1..3
  [Sitemap] ok 37 - Sitemap::Builder - whole priorities render as 1.0
  [Sitemap] # Subtest: Sitemap::Builder - accepts partial W3CDTF lastmod (A8)
  [Sitemap]     ok 1 - date-only lastmod precision recorded
  [Sitemap]     ok 2 - year-month lastmod precision recorded
  [Sitemap]     ok 3 - year-only lastmod precision recorded
  [Sitemap]     ok 4 - full datetime stays Precise
  [Sitemap]     ok 5 - year-month parses to a DateTime (no longer dies)
  [Sitemap]     ok 6 - year-only parses to a DateTime (no longer dies)
  [Sitemap]     ok 7 - date-only form rendered verbatim
  [Sitemap]     ok 8 - year-month form rendered verbatim
  [Sitemap]     ok 9 - year-only form rendered verbatim
  [Sitemap]     ok 10 - full datetime rendered verbatim
  [Sitemap]     1..10
  [Sitemap] ok 38 - Sitemap::Builder - accepts partial W3CDTF lastmod (A8)
  [Sitemap] # Subtest: Sitemap::Builder - render-index skips a Nil/empty lastmod
  [Sitemap]     ok 1 - No empty <lastmod></lastmod> tag is emitted
  [Sitemap]     ok 2 - A valid lastmod is still rendered
  [Sitemap]     ok 3 - Entry without lastmod is still present
  [Sitemap]     1..3
  [Sitemap] ok 39 - Sitemap::Builder - render-index skips a Nil/empty lastmod
  [Sitemap] # Subtest: Sitemap::Builder - scheme-relative locs stay absolute in render-index
  [Sitemap]     ok 1 - scheme-relative loc is not prefixed with the base URL
  [Sitemap]     ok 2 - no doubled scheme in the loc
  [Sitemap]     ok 3 - a plain relative loc still gets the base URL
  [Sitemap]     1..3
  [Sitemap] ok 40 - Sitemap::Builder - scheme-relative locs stay absolute in render-index
  [Sitemap] # Subtest: Sitemap::Builder - non-alpha schemes stay absolute in render-index
  [Sitemap]     ok 1 - hyphenated scheme loc is not prefixed with the base URL
  [Sitemap]     ok 2 - plus scheme loc is not prefixed with the base URL
  [Sitemap]     ok 3 - no base prepended onto hyphenated scheme
  [Sitemap]     ok 4 - no base prepended onto plus scheme
  [Sitemap]     1..4
  [Sitemap] ok 41 - Sitemap::Builder - non-alpha schemes stay absolute in render-index
  [Sitemap] # Subtest: Sitemap::Builder - write returns the written file paths
  [Sitemap]     ok 1 - single-file write returns one path
  [Sitemap]     ok 2 - returned path is the real written file
  [Sitemap]     ok 3 - the returned file exists
  [Sitemap]     ok 4 - multi-file write returns chunks plus index
  [Sitemap]     ok 5 - chunk 1 is in the returned paths
  [Sitemap]     ok 6 - chunk 2 is in the returned paths
  [Sitemap]     ok 7 - index is in the returned paths
  [Sitemap]     ok 8 - every returned path exists on disk
  [Sitemap]     1..8
  [Sitemap] ok 42 - Sitemap::Builder - write returns the written file paths
  [Sitemap] # Subtest: video numeric fields: out-of-range values are omitted, valid ones kept
  [Sitemap]     ok 1 - duration above 28800s omitted
  [Sitemap]     ok 2 - negative view_count omitted
  [Sitemap]     ok 3 - rating above 5.0 omitted
  [Sitemap]     ok 4 - valid duration kept
  [Sitemap]     ok 5 - valid view_count kept
  [Sitemap]     ok 6 - valid rating kept
  [Sitemap]     1..6
  [Sitemap] ok 43 - video numeric fields: out-of-range values are omitted, valid ones kept
  [Sitemap] # Subtest: add-item-from validates priority like add-item
  [Sitemap]     # Subtest: out-of-range priority from a direct Item dies
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'priority'/
  [Sitemap]     ok 1 - out-of-range priority from a direct Item dies
  [Sitemap]     ok 2 - in-range priority passes through
  [Sitemap]     ok 3 - valid value renders unchanged
  [Sitemap]     1..3
  [Sitemap] ok 44 - add-item-from validates priority like add-item
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/03-parser.rakutest
  [Sitemap] 1..38
  [Sitemap] # Subtest: Sitemap::Parser - parse simple XML
  [Sitemap]     ok 1 - Parsed 2 items
  [Sitemap]     ok 2 - First URL correct
  [Sitemap]     ok 3 - Priority parsed
  [Sitemap]     ok 4 - Second URL correct
  [Sitemap]     1..4
  [Sitemap] ok 1 - Sitemap::Parser - parse simple XML
  [Sitemap] # Subtest: Sitemap::Parser - a foreign-namespaced child is not misread as a sitemap field
  [Sitemap]     ok 1 - Parsed 1 item
  [Sitemap]     ok 2 - the sitemap-namespace <loc> wins, not the foreign-namespaced one
  [Sitemap]     ok 3 - foreign-namespaced <loc> did not leak into the url
  [Sitemap]     1..3
  [Sitemap] ok 2 - Sitemap::Parser - a foreign-namespaced child is not misread as a sitemap field
  [Sitemap] # Subtest: Sitemap::Parser - parse from file
  [Sitemap]     ok 1 - Parsed 1 item
  [Sitemap]     ok 2 - URL correct
  [Sitemap]     1..2
  [Sitemap] ok 3 - Sitemap::Parser - parse from file
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-file gunzips a .gz file
  [Sitemap]     ok 1 - Gzipped file parsed via parse-xml-file (not a "Start tag expected" failure)
  [Sitemap]     ok 2 - URL correct
  [Sitemap]     1..2
  [Sitemap] ok 4 - Sitemap::Parser - parse-xml-file gunzips a .gz file
  [Sitemap] # Subtest: Sitemap::Parser - invalid gzip file raises a clear error from parse-xml-file
  [Sitemap]     # Subtest: Undecodable gzip raises a clear error
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /:i 'failed to decode'/
  [Sitemap]     ok 1 - Undecodable gzip raises a clear error
  [Sitemap]     1..1
  [Sitemap] ok 5 - Sitemap::Parser - invalid gzip file raises a clear error from parse-xml-file
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-files parallel
  [Sitemap]     ok 1 - Has items key
  [Sitemap]     ok 2 - Has errors key
  [Sitemap]     ok 3 - Parsed 3 items total
  [Sitemap]     ok 4 - No errors
  [Sitemap]     1..4
  [Sitemap] ok 6 - Sitemap::Parser - parse-xml-files parallel
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-files with errors
  [Sitemap]     ok 1 - Parsed 1 valid item
  [Sitemap]     ok 2 - Recorded 1 error
  [Sitemap]     ok 3 - Error file recorded
  [Sitemap]     ok 4 - Error message recorded
  [Sitemap]     ok 5 - Error message is non-empty
  [Sitemap]     ok 6 - Real parser message surfaced, not generic fallback
  [Sitemap]     1..6
  [Sitemap] ok 7 - Sitemap::Parser - parse-xml-files with errors
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-file-recursive with index
  [Sitemap]     ok 1 - Has items key
  [Sitemap]     ok 2 - Has sitemaps key
  [Sitemap]     ok 3 - Parsed 3 items total
  [Sitemap]     ok 4 - Found 1 index
  [Sitemap]     1..4
  [Sitemap] ok 8 - Sitemap::Parser - parse-xml-file-recursive with index
  [Sitemap] # Subtest: Sitemap::Parser - query/fragment child locs resolve; missing children error
  [Sitemap]     ok 1 - Query/fragment child locs resolved to the local files
  [Sitemap]     ok 2 - First child parsed
  [Sitemap]     ok 3 - Fragment child parsed
  [Sitemap]     ok 4 - Missing child recorded as an error
  [Sitemap]     ok 5 - Error names the missing child
  [Sitemap]     1..5
  [Sitemap] ok 9 - Sitemap::Parser - query/fragment child locs resolve; missing children error
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-file-recursive gzipped
  [Sitemap]     ok 1 - Parsed 1 item from gzipped file
  [Sitemap]     ok 2 - URL correct
  [Sitemap]     1..2
  [Sitemap] ok 10 - Sitemap::Parser - parse-xml-file-recursive gzipped
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-file-recursive files-parsed counts only successful parses
  [Sitemap]     ok 1 - files-parsed counts 3 successfully parsed files (index + 2 children, not the bad one)
  [Sitemap]     ok 2 - Only the 2 valid children produced items
  [Sitemap]     ok 3 - The bad file generated 1 error
  [Sitemap]     1..3
  [Sitemap] ok 11 - Sitemap::Parser - parse-xml-file-recursive files-parsed counts only successful parses
  [Sitemap] # Subtest: Sitemap::Parser - parse-xml-file-recursive surfaces the real load error
  [Sitemap]     ok 1 - Structural failure recorded as one error
  [Sitemap]     ok 2 - Structural error keeps its real LibXML message, not "Failed to load XML"
  [Sitemap]     ok 3 - Error names the failing file
  [Sitemap]     ok 4 - Decode failure recorded as one error
  [Sitemap]     ok 5 - Decode failure keeps its explicit decode message
  [Sitemap]     1..5
  [Sitemap] ok 12 - Sitemap::Parser - parse-xml-file-recursive surfaces the real load error
  [Sitemap] # Subtest: Sitemap::Parser - invalid lastmod does not abort parse
  [Sitemap]     ok 1 - Both items parsed despite bad lastmod
  [Sitemap]     ok 2 - Invalid lastmod dropped, not fatal
  [Sitemap]     1..2
  [Sitemap] ok 13 - Sitemap::Parser - invalid lastmod does not abort parse
  [Sitemap] # Subtest: Sitemap::Parser - accepts partial W3CDTF lastmod (A7)
  [Sitemap]     ok 1 - all four items parsed
  [Sitemap]     ok 2 - date-only precision kept (was dropped entirely)
  [Sitemap]     ok 3 - year-month precision kept
  [Sitemap]     ok 4 - year-only precision kept
  [Sitemap]     ok 5 - year-month lastmod parses (no longer silently dropped)
  [Sitemap]     ok 6 - year-only lastmod parses (no longer silently dropped)
  [Sitemap]     ok 7 - date-only resolves to the given calendar date
  [Sitemap]     1..7
  [Sitemap] ok 14 - Sitemap::Parser - accepts partial W3CDTF lastmod (A7)
  [Sitemap] # Subtest: Sitemap::Parser - invalid priority/duration does not abort parse
  [Sitemap]     ok 1 - All three items parsed despite invalid numbers
  [Sitemap]     ok 2 - Invalid priority dropped
  [Sitemap]     ok 3 - Valid priority kept
  [Sitemap]     ok 4 - Invalid video duration dropped (not defaulted to 0)
  [Sitemap]     ok 5 - Video without content_loc gets empty string, not thumbnail URL
  [Sitemap]     ok 6 - Zero priority preserved
  [Sitemap]     1..6
  [Sitemap] ok 15 - Sitemap::Parser - invalid priority/duration does not abort parse
  [Sitemap] # Subtest: Sitemap::Parser - out-of-range priority drops the value, not the URL
  [Sitemap] Warning: ignoring out-of-range priority '2.5' for 'https://example.com/a'
  [Sitemap] Warning: ignoring out-of-range priority '-1' for 'https://example.com/b'
  [Sitemap]     ok 1 - All three items parsed despite out-of-range priorities
  [Sitemap]     ok 2 - First URL kept
  [Sitemap]     ok 3 - Out-of-range priority > 1 dropped
  [Sitemap]     ok 4 - Second URL kept
  [Sitemap]     ok 5 - Out-of-range priority < 0 dropped
  [Sitemap]     ok 6 - In-range priority kept
  [Sitemap]     1..6
  [Sitemap] ok 16 - Sitemap::Parser - out-of-range priority drops the value, not the URL
  [Sitemap] # Subtest: Sitemap::Parser - parse-url-recursive gunzips
  [Sitemap]     ok 1 - Parsed item from gzip URL
  [Sitemap]     ok 2 - Gzipped item URL correct
  [Sitemap]     ok 3 - No errors
  [Sitemap]     1..3
  [Sitemap] ok 17 - Sitemap::Parser - parse-url-recursive gunzips
  [Sitemap] # Subtest: Sitemap::Parser - ../ traversal locs are rejected
  [Sitemap]     ok 1 - Only the in-tree child is parsed
  [Sitemap]     ok 2 - In-tree child URL correct
  [Sitemap]     ok 3 - Outside file not reached via ../
  [Sitemap]     1..3
  [Sitemap] ok 18 - Sitemap::Parser - ../ traversal locs are rejected
  [Sitemap] # Subtest: Sitemap::Parser - parse-url-recursive file:// counts urls-parsed
  [Sitemap]     ok 1 - Both items parsed from a file:// URL
  [Sitemap]     ok 2 - file:// branch counts its single URL as parsed
  [Sitemap]     ok 3 - No errors
  [Sitemap]     1..3
  [Sitemap] ok 19 - Sitemap::Parser - parse-url-recursive file:// counts urls-parsed
  [Sitemap] # Subtest: Sitemap::Parser - file:// sitemap index recurses into children
  [Sitemap]     ok 1 - No spurious "Failed to parse XML" error for an index
  [Sitemap]     ok 2 - Child items parsed via the file:// branch recursing into the index
  [Sitemap]     ok 3 - First child item parsed
  [Sitemap]     ok 4 - Second child item parsed
  [Sitemap]     1..4
  [Sitemap] ok 20 - Sitemap::Parser - file:// sitemap index recurses into children
  [Sitemap] # Subtest: Sitemap::Parser - cyclic index graph fetches each sitemap once
  [Sitemap]     ok 1 - Each of the 4 cyclic sitemaps parsed exactly once
  [Sitemap]     ok 2 - No errors
  [Sitemap]     1..2
  [Sitemap] ok 21 - Sitemap::Parser - cyclic index graph fetches each sitemap once
  [Sitemap] # Subtest: Sitemap::Builder - discover-sitemaps preserves non-default port
  [Sitemap]     ok 1 - robots.txt sitemap URL keeps the non-default port
  [Sitemap]     1..1
  [Sitemap] ok 22 - Sitemap::Builder - discover-sitemaps preserves non-default port
  [Sitemap] # Subtest: Sitemap::Builder - discover-sitemap decompresses a gzip robots.txt
  [Sitemap]     ok 1 - Sitemap URL discovered from a gzip-encoded robots.txt
  [Sitemap]     1..1
  [Sitemap] ok 23 - Sitemap::Builder - discover-sitemap decompresses a gzip robots.txt
  [Sitemap] # Subtest: Sitemap::Builder - relative Sitemap entries resolve against robots.txt
  [Sitemap]     ok 1 - relative Sitemap: value resolved against the robots.txt URL (RFC 9309)
  [Sitemap]     1..1
  [Sitemap] ok 24 - Sitemap::Builder - relative Sitemap entries resolve against robots.txt
  [Sitemap] # Subtest: decompress-content defends against decompression bombs
  [Sitemap]     # Subtest: Inflating past the cap dies
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /exceeds/
  [Sitemap]     ok 1 - Inflating past the cap dies
  [Sitemap]     ok 2 - In-range gzip still decodes
  [Sitemap]     ok 3 - Non-gzip data decodes unchanged
  [Sitemap]     1..3
  [Sitemap] ok 25 - decompress-content defends against decompression bombs
  [Sitemap] # Subtest: Sitemap::Parser - parse-url-recursive defaults to same-host children
  [Sitemap]     ok 1 - Foreign-host child excluded by default
  [Sitemap]     ok 2 - Follow-foreign-children parses both children
  [Sitemap]     1..2
  [Sitemap] ok 26 - Sitemap::Parser - parse-url-recursive defaults to same-host children
  [Sitemap] # Subtest: Sitemap::Parser - parse-url-recursive excludes a different-port child by default
  [Sitemap]     ok 1 - Different-port child excluded by default
  [Sitemap]     ok 2 - Follow-foreign-children still skips the dead different-port child
  [Sitemap]     1..2
  [Sitemap] ok 27 - Sitemap::Parser - parse-url-recursive excludes a different-port child by default
  [Sitemap] # Subtest: Sitemap::Parser - relative child locs resolve before the origin check
  [Sitemap]     ok 1 - Both relative child locs resolved, same-origin and parsed
  [Sitemap]     ok 2 - No errors recorded
  [Sitemap]     1..2
  [Sitemap] ok 28 - Sitemap::Parser - relative child locs resolve before the origin check
  [Sitemap] # Subtest: Sitemap::Parser - parse-url-recursive fetches children in parallel
  [Sitemap]     ok 1 - All three children parsed with concurrency=4 (2 items each)
  [Sitemap]     ok 2 - No errors recorded
  [Sitemap]     ok 3 - Index recorded in sitemaps
  [Sitemap]     ok 4 - Index + 3 children counted as parsed
  [Sitemap]     1..4
  [Sitemap] ok 29 - Sitemap::Parser - parse-url-recursive fetches children in parallel
  [Sitemap] # Subtest: decompress-content rejects gzip magic that is not gzip
  [Sitemap]     # Subtest: Magic bytes with invalid gzip data die
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /:s gzip magic/
  [Sitemap]     ok 1 - Magic bytes with invalid gzip data die
  [Sitemap]     ok 2 - .gz suffix with no magic still decodes as plain text
  [Sitemap]     1..2
  [Sitemap] ok 30 - decompress-content rejects gzip magic that is not gzip
  [Sitemap] # Subtest: decompress-content rejects a truncated gzip stream
  [Sitemap]     # Subtest: Mid-stream truncation dies
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /:s truncated/
  [Sitemap]     ok 1 - Mid-stream truncation dies
  [Sitemap]     # Subtest: Header-only gzip dies
  [Sitemap]         1..2
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]     ok 2 - Header-only gzip dies
  [Sitemap]     ok 3 - Complete gzip stream still decodes
  [Sitemap]     1..3
  [Sitemap] ok 31 - decompress-content rejects a truncated gzip stream
  [Sitemap] # Subtest: Sitemap::Parser - is-sitemap-index tolerates comments in the preamble
  [Sitemap]     ok 1 - Index with a DOCTYPE before <sitemapindex> is detected
  [Sitemap]     ok 2 - Plain index still detected
  [Sitemap]     ok 3 - A leading comment before <sitemapindex> is detected as an index
  [Sitemap]     ok 4 - Generator comment between declaration and <sitemapindex> is tolerated
  [Sitemap]     ok 5 - Comment after a DOCTYPE is tolerated
  [Sitemap]     ok 6 - BOM plus multiple comments are tolerated
  [Sitemap]     ok 7 - Comment containing a > is tolerated
  [Sitemap]     ok 8 - Multi-line comment containing a > is tolerated
  [Sitemap]     ok 9 - A urlset is not an index
  [Sitemap]     1..9
  [Sitemap] ok 32 - Sitemap::Parser - is-sitemap-index tolerates comments in the preamble
  [Sitemap] # Subtest: Sitemap::Parser - a throwing worker does not deadlock the queue
  [Sitemap]     ok 1 - Valid child parsed despite the throwing sibling
  [Sitemap]     ok 2 - Valid item URL correct
  [Sitemap]     ok 3 - The throwing child recorded an error, not a hang
  [Sitemap]     ok 4 - The real parser error surfaced
  [Sitemap]     1..4
  [Sitemap] ok 33 - Sitemap::Parser - a throwing worker does not deadlock the queue
  [Sitemap] # Subtest: Sitemap::Parser - unparseable index lastmod is dropped, not Nil
  [Sitemap]     ok 1 - Both index entries parsed
  [Sitemap]     ok 2 - Invalid lastmod key is absent, not Nil
  [Sitemap]     ok 3 - Valid lastmod key present
  [Sitemap]     ok 4 - Valid lastmod parsed to a DateTime
  [Sitemap]     1..4
  [Sitemap] ok 34 - Sitemap::Parser - unparseable index lastmod is dropped, not Nil
  [Sitemap] # Subtest: Sitemap::Parser - huge text nodes parse in local files
  [Sitemap]     ok 1 - Local file with an oversized text node parses via :huge
  [Sitemap]     ok 2 - Huge caption preserved in full
  [Sitemap]     1..2
  [Sitemap] ok 35 - Sitemap::Parser - huge text nodes parse in local files
  [Sitemap] # Subtest: Sitemap::Parser - dedup happens before the max-children budget
  [Sitemap]     ok 1 - Duplicate child did not consume the budget: c1 and c2 both parsed
  [Sitemap]     ok 2 - c2 item present
  [Sitemap]     1..2
  [Sitemap] ok 36 - Sitemap::Parser - dedup happens before the max-children budget
  [Sitemap] # Subtest: Sitemap::Parser - video tags extracted from video:tag elements
  [Sitemap]     ok 1 - three video tags extracted
  [Sitemap]     ok 2 - video tags contain expected values
  [Sitemap]     ok 3 - non-namespaced <tag> is not treated as video:tag (A1)
  [Sitemap]     1..3
  [Sitemap] ok 37 - Sitemap::Parser - video tags extracted from video:tag elements
  [Sitemap] # Subtest: Sitemap::Parser - video booleans accept yes/true/1 case-insensitively
  [Sitemap]     ok 1 - family_friendly=TRUE parses as True
  [Sitemap]     ok 2 - requires_subscription=Yes parses as True
  [Sitemap]     ok 3 - live=1 parses as True
  [Sitemap]     1..3
  [Sitemap] ok 38 - Sitemap::Parser - video booleans accept yes/true/1 case-insensitively
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/04-grammars.rakutest
  [Sitemap] 1..48
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - extract hrefs
  [Sitemap]     ok 1 - Found 3 links
  [Sitemap]     1..1
  [Sitemap] ok 1 - Sitemap::Grammar::LinkExtract - extract hrefs
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - filter special URLs
  [Sitemap]     ok 1 - Only 1 normal link extracted
  [Sitemap]     ok 2 - Correct link
  [Sitemap]     1..2
  [Sitemap] ok 2 - Sitemap::Grammar::LinkExtract - filter special URLs
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - single-pass hrefs match the regex path
  [Sitemap]     ok 1 - single-pass href extraction matches the regex path
  [Sitemap]     ok 2 - five links kept (protocols and anchors dropped)
  [Sitemap]     1..2
  [Sitemap] ok 3 - Sitemap::Grammar::LinkExtract - single-pass hrefs match the regex path
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - script/style tag-name boundary is honored
  [Sitemap]     ok 1 - a link after <scriptx> is preserved
  [Sitemap]     ok 2 - a link after <stylesheet> is preserved
  [Sitemap]     ok 3 - a link after <scripture> is preserved
  [Sitemap]     ok 4 - real script body (and markup inside it) is stripped
  [Sitemap]     ok 5 - script with attributes is still stripped
  [Sitemap]     1..5
  [Sitemap] ok 4 - Sitemap::Grammar::LinkExtract - script/style tag-name boundary is honored
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - extract with base URL
  [Sitemap]     ok 1 - Found 2 links
  [Sitemap]     1..1
  [Sitemap] ok 5 - Sitemap::Grammar::LinkExtract - extract with base URL
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - AMP detection via html-open helpers
  [Sitemap]     ok 1 - amp attribute detected in <html> tag
  [Sitemap]     ok 2 - ⚡ marker detected
  [Sitemap]     ok 3 - ⚡ with no whitespace detected
  [Sitemap]     ok 4 - plain html not detected as AMP
  [Sitemap]     ok 5 - no <html> tag yields empty string
  [Sitemap]     1..5
  [Sitemap] ok 6 - Sitemap::Grammar::LinkExtract - AMP detection via html-open helpers
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - src/srcset ordering, source tags, protocol-relative
  [Sitemap]     ok 1 - img src (before srcset) extracted
  [Sitemap]     ok 2 - img srcset entries extracted regardless of order
  [Sitemap]     ok 3 - img src (after srcset) extracted
  [Sitemap]     ok 4 - srcset-before-src entries extracted
  [Sitemap]     ok 5 - source srcset extracted
  [Sitemap]     ok 6 - og:image protocol-relative resolved to https
  [Sitemap]     ok 7 - Protocol-relative href resolves with base scheme
  [Sitemap]     ok 8 - Single-quoted srcset captured
  [Sitemap]     ok 9 - Unquoted srcset captured
  [Sitemap]     1..9
  [Sitemap] ok 7 - Sitemap::Grammar::LinkExtract - src/srcset ordering, source tags, protocol-relative
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - href stays inside its own tag
  [Sitemap]     ok 1 - href from a later tag is not swallowed by an earlier bare <a>
  [Sitemap]     ok 2 - Only the in-tag href extracted
  [Sitemap]     ok 3 - Malformed nested anchor still extracts its own href
  [Sitemap]     ok 4 - Correct href extracted from malformed HTML
  [Sitemap]     1..4
  [Sitemap] ok 8 - Sitemap::Grammar::LinkExtract - href stays inside its own tag
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - unquoted values keep their trailing slash
  [Sitemap]     ok 1 - Unquoted href keeps its trailing slash
  [Sitemap]     ok 2 - Unquoted href without a slash is untouched
  [Sitemap]     ok 3 - Unquoted attribute keeps its trailing slash (data, not self-closing)
  [Sitemap]     ok 4 - Quoted attribute value keeps its trailing slash
  [Sitemap]     ok 5 - extract-with-text unquoted href keeps its trailing slash
  [Sitemap]     ok 6 - A bare unquoted slash is the root link
  [Sitemap]     1..6
  [Sitemap] ok 9 - Sitemap::Grammar::LinkExtract - unquoted values keep their trailing slash
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - relative resolution keeps port and userinfo
  [Sitemap]     ok 1 - non-default port preserved on absolute path
  [Sitemap]     ok 2 - non-default port preserved on relative path
  [Sitemap]     ok 3 - userinfo and port preserved
  [Sitemap]     ok 4 - default port omitted
  [Sitemap]     ok 5 - protocol-relative URL keeps its own port
  [Sitemap]     1..5
  [Sitemap] ok 10 - Sitemap::Grammar::LinkExtract - relative resolution keeps port and userinfo
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - ../ and ./ segments collapse
  [Sitemap]     ok 1 - parent-relative ../ collapses
  [Sitemap]     ok 2 - multiple ../ collapse
  [Sitemap]     ok 3 - ./ collapses
  [Sitemap]     ok 4 - .. above the root is dropped
  [Sitemap]     ok 5 - query and fragment survive the collapse
  [Sitemap]     ok 6 - bare .. resolves to the parent directory (RFC 3986 keeps the trailing slash)
  [Sitemap]     ok 7 - image src ../ collapses (image:loc)
  [Sitemap]     ok 8 - hreflang ../ collapses (xhtml:link)
  [Sitemap]     ok 9 - video ../ collapses (video:content_loc)
  [Sitemap]     ok 10 - video poster ../ collapses
  [Sitemap]     1..10
  [Sitemap] ok 11 - Sitemap::Grammar::LinkExtract - ../ and ./ segments collapse
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - query-only refs keep the base path
  [Sitemap]     ok 1 - query-only href keeps the full base path and replaces the query (RFC 3986 §5.2.2)
  [Sitemap]     ok 2 - image src query-only resolves against the full base path
  [Sitemap]     ok 3 - hreflang href query-only resolves against the full base path
  [Sitemap]     1..3
  [Sitemap] ok 12 - Sitemap::Grammar::LinkExtract - query-only refs keep the base path
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - <a boundary excludes abbr/area
  [Sitemap]     ok 1 - Only real anchors extracted, abbr/area hrefs ignored
  [Sitemap]     ok 2 - First real anchor
  [Sitemap]     ok 3 - Anchor href on a new line still extracted
  [Sitemap]     1..3
  [Sitemap] ok 13 - Sitemap::Grammar::LinkExtract - <a boundary excludes abbr/area
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - default page scan needs no tag-name boundary
  [Sitemap]     ok 1 - <a> captures only real anchors, not article/area/abbr/address
  [Sitemap]     ok 2 - The captured anchor is the real one
  [Sitemap]     ok 3 - <meta> does not capture <metadata>
  [Sitemap]     ok 4 - <base> does not capture <baseline>
  [Sitemap]     ok 5 - <link> does not capture <linkage>
  [Sitemap]     ok 6 - <source> does not capture <sourcex>
  [Sitemap]     ok 7 - <img> does not capture <image>
  [Sitemap]     ok 8 - <picture> captured once
  [Sitemap]     ok 9 - <video> captured once
  [Sitemap]     ok 10 - <html> captured once
  [Sitemap]     1..10
  [Sitemap] ok 14 - Sitemap::Grammar::LinkExtract - default page scan needs no tag-name boundary
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - HTML entities decode exactly once
  [Sitemap]     ok 1 - amp decoded in quoted href
  [Sitemap]     ok 2 - numeric entity decoded in single-quoted href
  [Sitemap]     ok 3 - href via tag-attrs decoded
  [Sitemap]     ok 4 - double-escaped title decoded exactly once
  [Sitemap]     ok 5 - srcset yields one image
  [Sitemap]     ok 6 - srcset capture entity-decoded
  [Sitemap]     ok 7 - %26 preserved while &amp; decoded
  [Sitemap]     1..7
  [Sitemap] ok 15 - Sitemap::Grammar::LinkExtract - HTML entities decode exactly once
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - Crawl-delay parses without crashing
  [Sitemap]     ok 1 - Robots.txt with Crawl-delay parses
  [Sitemap]     ok 2 - get-crawl-delay returns the parsed delay
  [Sitemap]     ok 3 - Wildcard delay propagates to other agents
  [Sitemap]     ok 4 - Sitemap entries still found
  [Sitemap]     ok 5 - Sitemap URL correct
  [Sitemap]     ok 6 - Allowed path remains allowed
  [Sitemap]     ok 7 - Disallowed path remains disallowed
  [Sitemap]     1..7
  [Sitemap] ok 16 - Sitemap::Grammar::RobotsTxt - Crawl-delay parses without crashing
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - case-insensitive fields, mixed-case UA, CR/LF/CRLF
  [Sitemap]     ok 1 - Uppercase fields with CR/LF/CRLF line endings parse
  [Sitemap]     ok 2 - Mixed-case UA uses its own rules
  [Sitemap]     ok 3 - Mixed-case UA respects Disallow
  [Sitemap]     ok 4 - Crawl-Delay found for mixed-case UA
  [Sitemap]     ok 5 - Uppercase SITEMAP found
  [Sitemap]     ok 6 - Lowercase fields with LF parses
  [Sitemap]     ok 7 - Lowercase disallow enforced
  [Sitemap]     1..7
  [Sitemap] ok 17 - Sitemap::Grammar::RobotsTxt - case-insensitive fields, mixed-case UA, CR/LF/CRLF
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - get-crawl-delay resolves bot-specific groups
  [Sitemap]     ok 1 - Bot-specific group parses
  [Sitemap]     ok 2 - Versioned UA finds the bare product-token group Crawl-delay
  [Sitemap]     ok 3 - Exact lowercase key still works
  [Sitemap]     ok 4 - Any version suffix matches the token group
  [Sitemap]     ok 5 - Unknown UA falls back to the * group
  [Sitemap]     ok 6 - Default argument falls back to *
  [Sitemap]     ok 7 - Token match works without any * fallback present
  [Sitemap]     ok 8 - Unknown UA with no * group yields Nil, not a crash
  [Sitemap]     1..8
  [Sitemap] ok 18 - Sitemap::Grammar::RobotsTxt - get-crawl-delay resolves bot-specific groups
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - malformed Crawl-delay does not crash
  [Sitemap]     ok 1 - Robots.txt with bare-dot Crawl-delay parses
  [Sitemap]     ok 2 - Bare-dot Crawl-delay does not throw
  [Sitemap]     ok 3 - Disallow still enforced after bad Crawl-delay
  [Sitemap]     ok 4 - Multi-dot Crawl-delay parses
  [Sitemap]     ok 5 - Multi-dot Crawl-delay does not throw
  [Sitemap]     ok 6 - Invalid crawl-delay value ignored
  [Sitemap]     1..6
  [Sitemap] ok 19 - Sitemap::Grammar::RobotsTxt - malformed Crawl-delay does not crash
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - empty Disallow does not swallow next entry
  [Sitemap]     ok 1 - Robots.txt with empty Disallow parses
  [Sitemap]     ok 2 - Sitemap entry after empty Disallow still found
  [Sitemap]     ok 3 - Sitemap URL correct
  [Sitemap]     ok 4 - Empty Disallow disallows nothing
  [Sitemap]     1..4
  [Sitemap] ok 20 - Sitemap::Grammar::RobotsTxt - empty Disallow does not swallow next entry
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - empty User-agent/Sitemap values do not discard the file
  [Sitemap]     ok 1 - Robots.txt with an empty User-agent line parses
  [Sitemap]     ok 2 - Empty User-agent defaults to the * wildcard rules
  [Sitemap]     ok 3 - Robots.txt with an empty Sitemap line parses
  [Sitemap]     ok 4 - Empty Sitemap value is skipped, later Sitemap kept
  [Sitemap]     ok 5 - Non-empty Sitemap URL correct
  [Sitemap]     ok 6 - Disallow after empty Sitemap still enforced
  [Sitemap]     1..6
  [Sitemap] ok 21 - Sitemap::Grammar::RobotsTxt - empty User-agent/Sitemap values do not discard the file
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - path matching is anchored unless the pattern starts with *
  [Sitemap]     ok 1 - Robots.txt parses
  [Sitemap]     ok 2 - Exact /admin path is blocked
  [Sitemap]     ok 3 - Prefix /admin/x is blocked
  [Sitemap]     ok 4 - Mid-path /x/admin is NOT blocked (RFC 9309 anchor)
  [Sitemap]     ok 5 - Wildcard-prefixed robots.txt parses
  [Sitemap]     ok 6 - Leading * keeps matching unanchored
  [Sitemap]     1..6
  [Sitemap] ok 22 - Sitemap::Grammar::RobotsTxt - path matching is anchored unless the pattern starts with *
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - unknown and indented directives are skipped, not fatal
  [Sitemap]     ok 1 - Robots.txt with non-standard and indented directives parses
  [Sitemap]     ok 2 - Allowed path remains allowed
  [Sitemap]     ok 3 - Disallow after unknown directives still enforced
  [Sitemap]     ok 4 - Sitemap entry after unknown directives still found
  [Sitemap]     ok 5 - Sitemap URL correct
  [Sitemap]     ok 6 - Trailing unknown directive without a final newline parses
  [Sitemap]     ok 7 - Rules from the partial file still apply
  [Sitemap]     1..7
  [Sitemap] ok 23 - Sitemap::Grammar::RobotsTxt - unknown and indented directives are skipped, not fatal
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - rel values are case-insensitive
  [Sitemap]     ok 1 - rel="ALTERNATE" matches alternate
  [Sitemap]     ok 2 - alternate href resolved
  [Sitemap]     ok 3 - rel="stylesheet" is not treated as alternate
  [Sitemap]     1..3
  [Sitemap] ok 24 - Sitemap::Grammar::LinkExtract - rel values are case-insensitive
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - extract-tag-bodies accepts a bare Str :tags
  [Sitemap]     ok 1 - bare Str :tags<meta> scans only the meta tag
  [Sitemap]     ok 2 - meta body collected
  [Sitemap]     ok 3 - meta body returned
  [Sitemap]     ok 4 - Positional :tags(<meta link>) scans both
  [Sitemap]     ok 5 - meta body present in list result
  [Sitemap]     ok 6 - link body present in list result
  [Sitemap]     ok 7 - default tag set includes meta
  [Sitemap]     ok 8 - default tag set includes link
  [Sitemap]     ok 9 - default tag set includes video
  [Sitemap]     ok 10 - default tag set includes img
  [Sitemap]     1..10
  [Sitemap] ok 25 - Sitemap::Grammar::LinkExtract - extract-tag-bodies accepts a bare Str :tags
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - uppercase tag names match
  [Sitemap]     ok 1 - uppercase <META> matches :tags<meta>
  [Sitemap]     ok 2 - uppercase meta body returned
  [Sitemap]     ok 3 - uppercase <META> present in list result
  [Sitemap]     ok 4 - uppercase <LINK> matches :tags<link>
  [Sitemap]     ok 5 - uppercase link body returned
  [Sitemap]     ok 6 - uppercase <META> in default set
  [Sitemap]     ok 7 - uppercase <LINK> in default set
  [Sitemap]     ok 8 - uppercase <VIDEO> in default set
  [Sitemap]     ok 9 - uppercase <IMG> in default set
  [Sitemap]     ok 10 - uppercase <SOURCE> in default set
  [Sitemap]     1..10
  [Sitemap] ok 26 - Sitemap::Grammar::LinkExtract - uppercase tag names match
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - bare/self-closing tags and single-pass equivalence
  [Sitemap]     ok 1 - bare <img/> captured alongside <img src>
  [Sitemap]     ok 2 - bare <meta/> captured alongside <meta property>
  [Sitemap]     ok 3 - bare <video> captured
  [Sitemap]     ok 4 - both <source> tags captured
  [Sitemap]     ok 5 - single-pass image count matches the scan path
  [Sitemap]     ok 6 - single-pass images equal the scan path results
  [Sitemap]     ok 7 - images actually extracted
  [Sitemap]     ok 8 - single-pass video count matches the scan path
  [Sitemap]     ok 9 - single-pass videos equal the scan path results
  [Sitemap]     1..9
  [Sitemap] ok 27 - Sitemap::Grammar::LinkExtract - bare/self-closing tags and single-pass equivalence
  [Sitemap] # Subtest: Sitemap::Grammar::SitemapSniff - comments in the preamble are tolerated
  [Sitemap]     ok 1 - comment-first index matches
  [Sitemap]     ok 2 - detected as a sitemap
  [Sitemap]     ok 3 - bare comment before sitemapindex matches
  [Sitemap]     ok 4 - still a sitemap
  [Sitemap]     ok 5 - plain index still matches
  [Sitemap]     ok 6 - html document still matches
  [Sitemap]     ok 7 - and is classified as html, not as a sitemap
  [Sitemap]     1..7
  [Sitemap] ok 28 - Sitemap::Grammar::SitemapSniff - comments in the preamble are tolerated
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - srcset commas inside balanced parens are kept
  [Sitemap]     ok 1 - Comma-containing candidate is not split, so both candidates extracted
  [Sitemap]     ok 2 - Parenthesized candidate kept whole, wrappers stripped
  [Sitemap]     ok 3 - Plain candidate resolved and extracted
  [Sitemap]     ok 4 - Parenthesized data URI is not emitted as a junk relative URL
  [Sitemap]     ok 5 - Sibling candidate still extracted
  [Sitemap]     1..5
  [Sitemap] ok 29 - Sitemap::Grammar::LinkExtract - srcset commas inside balanced parens are kept
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - rel token set matches alternate anywhere
  [Sitemap]     ok 1 - rel="alternate x-default" matches
  [Sitemap]     ok 2 - x-default href resolved
  [Sitemap]     ok 3 - rel="x-default alternate" matches
  [Sitemap]     ok 4 - alternate-last href resolved
  [Sitemap]     1..4
  [Sitemap] ok 30 - Sitemap::Grammar::LinkExtract - rel token set matches alternate anywhere
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - script/style bodies and comments do not leak links
  [Sitemap]     ok 1 - Comment does not leak a link
  [Sitemap]     ok 2 - The real link is still found
  [Sitemap]     ok 3 - Script body with angle brackets does not leak a link
  [Sitemap]     ok 4 - The link after the script is found
  [Sitemap]     ok 5 - Style body does not leak a link
  [Sitemap]     ok 6 - The link after the style is found
  [Sitemap]     1..6
  [Sitemap] ok 31 - Sitemap::Grammar::LinkExtract - script/style bodies and comments do not leak links
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - non-canonical close tags still end ignorable regions (CQ)
  [Sitemap]     ok 1 - link after </script > (space before >) survives
  [Sitemap]     ok 2 - the real link is preserved
  [Sitemap]     ok 3 - link after </style newline> survives
  [Sitemap]     ok 4 - the real link is preserved
  [Sitemap]     ok 5 - </scriptx> is not a </script> close; body stays swallowed
  [Sitemap]     1..5
  [Sitemap] ok 32 - Sitemap::Grammar::LinkExtract - non-canonical close tags still end ignorable regions (CQ)
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - extract-images is case-insensitive
  [Sitemap]     ok 1 - uppercase <IMG SRC> matched
  [Sitemap]     ok 2 - uppercase SRCSET= matched
  [Sitemap]     ok 3 - lowercase <img src> still matched
  [Sitemap]     1..3
  [Sitemap] ok 33 - Sitemap::Grammar::LinkExtract - extract-images is case-insensitive
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - Allow specificity beats a shorter Disallow (E1)
  [Sitemap]     ok 1 - Robots.txt with Allow + Disallow parses
  [Sitemap]     ok 2 - Allow /foo* matches 10 octets and beats Disallow /foobar (7) on /foobarxyz (E1)
  [Sitemap]     ok 3 - Length tie on /foobar: the disallow wins (E1)
  [Sitemap]     ok 4 - Disallow + more specific Allow parses
  [Sitemap]     ok 5 - The longer Allow /private/public/ wins inside /private/ (E1)
  [Sitemap]     ok 6 - A sibling under /private/ stays blocked (E1)
  [Sitemap]     1..6
  [Sitemap] ok 34 - Sitemap::Grammar::RobotsTxt - Allow specificity beats a shorter Disallow (E1)
  [Sitemap] # Subtest: Sitemap::Grammar::RobotsTxt - scheme matching is case-insensitive (CQ)
  [Sitemap]     ok 1 - robots.txt parses
  [Sitemap]     ok 2 - uppercase HTTP:// scheme still applies the Disallow (was bypassed)
  [Sitemap]     ok 3 - uppercase HTTPS:// scheme still applies the Disallow
  [Sitemap]     ok 4 - lowercase scheme Disallow still applies
  [Sitemap]     ok 5 - an allowed path stays allowed regardless of scheme case
  [Sitemap]     1..5
  [Sitemap] ok 35 - Sitemap::Grammar::RobotsTxt - scheme matching is case-insensitive (CQ)
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - namespaced attrs, html default tag, script-video skip
  [Sitemap]     ok 1 - namespaced xml:lang captured under its full name
  [Sitemap]     ok 2 - namespaced xlink:href captured under its full name
  [Sitemap]     ok 3 - xlink:href no longer collides with the plain href
  [Sitemap]     ok 4 - default tag set includes html (AMP check rides the fast pass)
  [Sitemap]     ok 5 - html body keeps the AMP marker whitespace
  [Sitemap]     ok 6 - tag-bodies path skips the script-embedded video
  [Sitemap]     ok 7 - tag-bodies and scan paths agree on the surviving video
  [Sitemap]     1..7
  [Sitemap] ok 36 - Sitemap::Grammar::LinkExtract - namespaced attrs, html default tag, script-video skip
  [Sitemap] # Subtest: Sitemap::Grammar::LinkExtract - uppercase schemes and data: are filtered
  [Sitemap]     ok 1 - Uppercase javascript:/data:/mailto:/tel: hrefs filtered
  [Sitemap]     ok 2 - Only the normal link survives
  [Sitemap]     ok 3 - data:/javascript: img srcs filtered case-insensitively
  [Sitemap]     ok 4 - Only the real image survives
  [Sitemap]     ok 5 - Real video content_loc survives
  [Sitemap]     ok 6 - Uppercase data: content_loc filtered
  [Sitemap]     1..6
  [Sitemap] ok 37 - Sitemap::Grammar::LinkExtract - uppercase schemes and data: are filtered
  [Sitemap] # Subtest: SitemapSniff: comments may contain ">" (valid XML)
  [Sitemap]     ok 1 - comment containing > still sniffs as sitemap
  [Sitemap]     ok 2 - plain comment unaffected
  [Sitemap]     ok 3 - unterminated comment still fails
  [Sitemap]     1..3
  [Sitemap] ok 38 - SitemapSniff: comments may contain ">" (valid XML)
  [Sitemap] # Subtest: extract-with-text matches uppercase <A> tags
  [Sitemap]     ok 1 - both cases matched
  [Sitemap]     ok 2 - uppercase href resolved
  [Sitemap]     1..2
  [Sitemap] ok 39 - extract-with-text matches uppercase <A> tags
  [Sitemap] # Subtest: SitemapSniff: prolog items in any order + DOCTYPE
  [Sitemap]     ok 1 - BOM+decl+urlset classifies as xml-sitemap
  [Sitemap]     ok 2 - BOM+newline+decl classifies as xml-sitemap
  [Sitemap]     ok 3 - comment then decl classifies as xml-sitemap
  [Sitemap]     ok 4 - decl then comment classifies as xml-sitemap
  [Sitemap]     ok 5 - DOCTYPE urlset classifies as xml-sitemap
  [Sitemap]     ok 6 - DOCTYPE w/ subset classifies as xml-sitemap
  [Sitemap]     ok 7 - HTML doctype root classifies as html
  [Sitemap]     ok 8 - unclosed doctype classifies as NO-MATCH
  [Sitemap]     1..8
  [Sitemap] ok 40 - SitemapSniff: prolog items in any order + DOCTYPE
  [Sitemap] # Subtest: RobotsTxt: UA lookup matches product token with version suffix
  [Sitemap]     ok 1 - versioned UA matches bare-token group (RFC 9309)
  [Sitemap]     ok 2 - exact lowercase token still works
  [Sitemap]     ok 3 - unknown bot falls back to * group
  [Sitemap]     ok 4 - most specific prefix group wins over *
  [Sitemap]     1..4
  [Sitemap] ok 41 - RobotsTxt: UA lookup matches product token with version suffix
  [Sitemap] # Subtest: LinkExtract: duplicate attribute keeps the first occurrence
  [Sitemap]     ok 1 - HTML parsers keep the first duplicated attribute
  [Sitemap]     1..1
  [Sitemap] ok 42 - LinkExtract: duplicate attribute keeps the first occurrence
  [Sitemap] # Subtest: RobotsTxt: BOM before the first User-agent does not poison the * group
  [Sitemap]     ok 1 - BOM-prefixed robots.txt parses
  [Sitemap]     ok 2 - the swallowed User-agent line must not attach its Disallow to *
  [Sitemap]     ok 3 - googlebot itself is still blocked via fallback to the * rules
  [Sitemap]     ok 4 - newline after the BOM still leaves * untouched
  [Sitemap]     1..4
  [Sitemap] ok 43 - RobotsTxt: BOM before the first User-agent does not poison the * group
  [Sitemap] # Subtest: LinkExtract: extraction tolerates tag-bodies sets missing extractor keys
  [Sitemap]     ok 1 - no images found without an img key, and no death
  [Sitemap]     ok 2 - extract-images survives a tag-bodies hash lacking img/source
  [Sitemap]     ok 3 - no videos found without a video key, and no death
  [Sitemap]     ok 4 - extract-videos survives a tag-bodies hash lacking video/img
  [Sitemap]     1..4
  [Sitemap] ok 44 - LinkExtract: extraction tolerates tag-bodies sets missing extractor keys
  [Sitemap] # Subtest: LinkExtract: extract-base-href ignores commented bases and honors attribute-less first base
  [Sitemap]     ok 1 - a commented-out <base> must not hijack relative resolution
  [Sitemap]     ok 2 - an attribute-less first <base> wins over a later one and yields empty
  [Sitemap]     ok 3 - normal <base href> still found
  [Sitemap]     ok 4 - tag-name prefix like baseboard does not match
  [Sitemap]     ok 5 - script body cannot inject a fake base
  [Sitemap]     1..5
  [Sitemap] ok 45 - LinkExtract: extract-base-href ignores commented bases and honors attribute-less first base
  [Sitemap] # Subtest: LinkExtract: custom tag names with digits and hyphens tokenize
  [Sitemap]     ok 1 - plain letter tag still captured
  [Sitemap]     ok 2 - hyphenated custom element captured whole
  [Sitemap]     ok 3 - custom element body returned
  [Sitemap]     ok 4 - digit-bearing heading tag captured (used to truncate at h)
  [Sitemap]     1..4
  [Sitemap] ok 46 - LinkExtract: custom tag names with digits and hyphens tokenize
  [Sitemap] # Subtest: RobotsTxt: allowed() preserves query on bare-domain URLs
  [Sitemap]     ok 1 - bare domain + matching query is blocked via /?q=test
  [Sitemap]     ok 2 - bare domain + non-matching query is allowed
  [Sitemap]     ok 3 - bare domain without query is allowed
  [Sitemap]     ok 4 - /page?q=test does not start with /?q=test so is allowed
  [Sitemap]     ok 5 - fragment is stripped before matching
  [Sitemap]     1..5
  [Sitemap] ok 47 - RobotsTxt: allowed() preserves query on bare-domain URLs
  [Sitemap] # Subtest: empty href="" is deliberately unmatchable across all extractors (CQ-F3)
  [Sitemap]     ok 1 - extract-href-only finds no empty href
  [Sitemap]     ok 2 - extract with base finds no empty href
  [Sitemap]     ok 3 - single-pass body extractor agrees (no empty href)
  [Sitemap]     1..3
  [Sitemap] ok 48 - empty href="" is deliberately unmatchable across all extractors (CQ-F3)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/05-formats.rakutest
  [Sitemap] 1..25
  [Sitemap] # Subtest: Sitemap::Format::HTML - render-list
  [Sitemap]     ok 1 - Contains html tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains second URL
  [Sitemap]     1..4
  [Sitemap] ok 1 - Sitemap::Format::HTML - render-list
  [Sitemap] # Subtest: Sitemap::Format::HTML - doctype
  [Sitemap]     ok 1 - Contains DOCTYPE
  [Sitemap]     ok 2 - Contains lang attribute
  [Sitemap]     1..2
  [Sitemap] ok 2 - Sitemap::Format::HTML - doctype
  [Sitemap] # Subtest: Sitemap::Format::TXT - render-list
  [Sitemap]     ok 1 - Correct content
  [Sitemap]     1..1
  [Sitemap] ok 3 - Sitemap::Format::TXT - render-list
  [Sitemap] # Subtest: Sitemap::Format::TXT - empty list
  [Sitemap]     ok 1 - Empty output for empty list
  [Sitemap]     1..1
  [Sitemap] ok 4 - Sitemap::Format::TXT - empty list
  [Sitemap] # Subtest: Sitemap::Format::TXT - render items
  [Sitemap]     ok 1 - Correct content
  [Sitemap]     1..1
  [Sitemap] ok 5 - Sitemap::Format::TXT - render items
  [Sitemap] # Subtest: Sitemap::Format::TXT - render empty items
  [Sitemap]     ok 1 - Empty output for empty items
  [Sitemap]     1..1
  [Sitemap] ok 6 - Sitemap::Format::TXT - render empty items
  [Sitemap] # Subtest: Sitemap::Format::RSS - render-list
  [Sitemap]     ok 1 - Contains rss tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains second URL
  [Sitemap]     ok 5 - Contains item elements
  [Sitemap]     ok 6 - output is well-formed XML
  [Sitemap]     1..6
  [Sitemap] ok 7 - Sitemap::Format::RSS - render-list
  [Sitemap] # Subtest: Sitemap::Format::Atom - render-list
  [Sitemap]     ok 1 - Contains feed tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains entry elements
  [Sitemap]     ok 5 - output is well-formed XML
  [Sitemap]     1..5
  [Sitemap] ok 8 - Sitemap::Format::Atom - render-list
  [Sitemap] # Subtest: Sitemap::Format::MRSS - render-list
  [Sitemap]     ok 1 - Contains rss tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains media namespace
  [Sitemap]     ok 4 - Contains first URL
  [Sitemap]     ok 5 - output is well-formed XML even without media elements
  [Sitemap]     1..5
  [Sitemap] ok 9 - Sitemap::Format::MRSS - render-list
  [Sitemap] # Subtest: Sitemap::Format::RSS - render with default args (title only)
  [Sitemap]     ok 1 - Contains rss tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains item elements
  [Sitemap]     1..4
  [Sitemap] ok 10 - Sitemap::Format::RSS - render with default args (title only)
  [Sitemap] # Subtest: Sitemap::Format::RSS - render-list without description
  [Sitemap]     ok 1 - Contains rss tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     1..3
  [Sitemap] ok 11 - Sitemap::Format::RSS - render-list without description
  [Sitemap] # Subtest: Sitemap::Format::Atom - render with default args (title only)
  [Sitemap]     ok 1 - Contains feed tag
  [Sitemap]     ok 2 - Contains title
  [Sitemap]     ok 3 - Contains first URL
  [Sitemap]     ok 4 - Contains entry elements
  [Sitemap]     1..4
  [Sitemap] ok 12 - Sitemap::Format::Atom - render with default args (title only)
  [Sitemap] # Subtest: Sitemap::Format::RSS/Atom - :pretty actually indents (default) vs flat (:pretty False)
  [Sitemap]     ok 1 - RSS default output is indented per nesting level
  [Sitemap]     ok 2 - RSS :pretty(False) keeps the feed on one line
  [Sitemap]     ok 3 - RSS pretty and flat are identical modulo whitespace
  [Sitemap]     ok 4 - Atom default output is indented per nesting level
  [Sitemap]     ok 5 - Atom :pretty(False) keeps the feed on one line
  [Sitemap]     1..5
  [Sitemap] ok 13 - Sitemap::Format::RSS/Atom - :pretty actually indents (default) vs flat (:pretty False)
  [Sitemap] # Subtest: Sitemap::Format::HTML - lang attribute is xml-escaped
  [Sitemap]     ok 1 - quotes in lang are escaped so the attribute cannot be broken out of
  [Sitemap]     ok 2 - plain lang passes through untouched
  [Sitemap]     1..2
  [Sitemap] ok 14 - Sitemap::Format::HTML - lang attribute is xml-escaped
  [Sitemap] # Subtest: Sitemap::Format::RSS - render Sitemap::Item without title
  [Sitemap]     ok 1 - Contains rss tag
  [Sitemap]     ok 2 - Contains item URL
  [Sitemap]     1..2
  [Sitemap] ok 15 - Sitemap::Format::RSS - render Sitemap::Item without title
  [Sitemap] # Subtest: Sitemap::Format::MRSS - pubDate is RFC-822
  [Sitemap]     ok 1 - pubDate rendered in RFC-822 format
  [Sitemap]     ok 2 - ISO-8601 lastmod no longer leaked into pubDate
  [Sitemap]     ok 3 - UTC lastmod renders as +0000
  [Sitemap]     ok 4 - Negative-offset lastmod renders correctly
  [Sitemap]     1..4
  [Sitemap] ok 16 - Sitemap::Format::MRSS - pubDate is RFC-822
  [Sitemap] # Subtest: Sitemap::Format::MRSS - media items carry an item <link>
  [Sitemap]     not ok 1 - media:content emitted for video item
  [Sitemap]     # Failed test 'media:content emitted for video item'
  [Sitemap]     # at t/05-formats.rakutest line 202
  [Sitemap]     ok 2 - Item <link> emitted alongside media:content
  [Sitemap]     1..2
  [Sitemap]     # You failed 1 test of 2
  [Sitemap] # Failed test 'Sitemap::Format::MRSS - media items carry an item <link>'
  [Sitemap] # at t/05-formats.rakutest line 191
  [Sitemap] not ok 17 - Sitemap::Format::MRSS - media items carry an item <link>
  [Sitemap] # Subtest: MRSS render accepts :$now like RSS/Atom (lastBuildDate parity)
  [Sitemap]     ok 1 - explicit :$now lands in lastBuildDate
  [Sitemap]     ok 2 - default now() fills lastBuildDate too
  [Sitemap]     1..2
  [Sitemap] ok 18 - MRSS render accepts :$now like RSS/Atom (lastBuildDate parity)
  [Sitemap] # Subtest: MRSS media:content never points at the page URL
  [Sitemap]     not ok 1 - player-loc-only video falls back to the player URL
  [Sitemap]     # Failed test 'player-loc-only video falls back to the player URL'
  [Sitemap]     # at t/05-formats.rakutest line 223
  [Sitemap]     ok 2 - and never to the enclosing page URL
  [Sitemap]     ok 3 - video with neither loc emits no media:content element
  [Sitemap]     1..3
  [Sitemap]     # You failed 1 test of 3
  [Sitemap] not ok 19 - MRSS media:content never points at the page URL
  [Sitemap] # Failed test 'MRSS media:content never points at the page URL'
  [Sitemap] # at t/05-formats.rakutest line 217
  [Sitemap] # Subtest: MRSS duration is only emitted when the video has a positive duration
  [Sitemap]     not ok 1 - media:content emitted without a duration
  [Sitemap]     # Failed test 'media:content emitted without a duration'
  [Sitemap]     # at t/05-formats.rakutest line 240
  [Sitemap]     ok 2 - no duration attribute when the video has none
  [Sitemap]     not ok 3 - duration attribute present when the video has one
  [Sitemap]     # Failed test 'duration attribute present when the video has one'
  [Sitemap]     # at t/05-formats.rakutest line 247
  [Sitemap]     1..3
  [Sitemap]     # You failed 2 tests of 3
  [Sitemap] not ok 20 - MRSS duration is only emitted when the video has a positive duration
  [Sitemap] # Failed test 'MRSS duration is only emitted when the video has a positive duration'
  [Sitemap] # at t/05-formats.rakutest line 233
  [Sitemap] # Subtest: C1 - with-meta lastmod wiring survives FeedBuilder refactor
  [Sitemap]     ok 1 - RSS with-meta pubDate uses the item lastmod, not the feed $now
  [Sitemap]     ok 2 - RSS with-meta entry keeps the item title
  [Sitemap]     ok 3 - Atom with-meta updated/published use the item lastmod
  [Sitemap]     ok 4 - Atom with-meta entry keeps the item title
  [Sitemap]     ok 5 - MRSS with-meta pubDate uses the item lastmod
  [Sitemap]     1..5
  [Sitemap] ok 21 - C1 - with-meta lastmod wiring survives FeedBuilder refactor
  [Sitemap] # Subtest: C1/C2 - MRSS output is byte-pinned (flat, deterministic)
  [Sitemap]     ok 1 - MRSS render-list bytes unchanged by the FeedBuilder refactor
  [Sitemap]     ok 2 - MRSS stays flat (still ignores :pretty, like pre-refactor)
  [Sitemap]     1..2
  [Sitemap] ok 22 - C1/C2 - MRSS output is byte-pinned (flat, deterministic)
  [Sitemap] # Subtest: C1 - RSS/Atom white-space-normalized parity across refactor
  [Sitemap]     ok 1 - RSS has <rss root
  [Sitemap]     ok 2 - RSS has feed title S
  [Sitemap]     ok 3 - RSS has item title Alpha
  [Sitemap]     ok 4 - RSS has item link
  [Sitemap]     ok 5 - RSS has pubDate
  [Sitemap]     ok 6 - Atom has feed title S
  [Sitemap]     ok 7 - Atom has item title Alpha
  [Sitemap]     ok 8 - Atom emits <link
  [Sitemap]     ok 9 - Atom has id
  [Sitemap]     ok 10 - Atom has updated
  [Sitemap]     1..10
  [Sitemap] ok 23 - C1 - RSS/Atom white-space-normalized parity across refactor
  [Sitemap] # Subtest: C2 - media namespace injection is scoped to the opening <rss> tag
  [Sitemap]     ok 1 - exactly one xmlns:media on the <rss> tag
  [Sitemap]     ok 2 - declared media namespace resolves to the MRSS URI
  [Sitemap]     ok 3 - xmlns:media text elsewhere leaves exactly one real declaration
  [Sitemap]     ok 4 - scoped-guard output is well-formed XML
  [Sitemap]     ok 5 - title-triggered output is well-formed XML
  [Sitemap]     1..5
  [Sitemap] ok 24 - C2 - media namespace injection is scoped to the opening <rss> tag
  [Sitemap] # Subtest: F - TXT/HTML render-to streams identically to render-list
  [Sitemap]     ok 1 - TXT render-to matches render-list for plain URLs
  [Sitemap]     ok 2 - TXT render-to matches render-list for Item objects
  [Sitemap]     ok 3 - TXT render-to matches render-list for an empty list
  [Sitemap]     ok 4 - HTML render-to matches render-list for plain URLs
  [Sitemap]     ok 5 - HTML render-to matches render-list with lastmod metadata
  [Sitemap]     ok 6 - HTML render-to matches render-list for a mixed list in flat mode
  [Sitemap]     1..6
  [Sitemap] ok 25 - F - TXT/HTML render-to streams identically to render-list
  [Sitemap] # You failed 3 tests of 25
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/06-crawler.rakutest
  [Sitemap] 1..54
  [Sitemap] # Subtest: Sitemap::Crawler - creation
  [Sitemap]     ok 1 - Crawler created
  [Sitemap]     ok 2 - User agent set
  [Sitemap]     ok 3 - Max depth set
  [Sitemap]     ok 4 - Max urls set
  [Sitemap]     1..4
  [Sitemap] ok 1 - Sitemap::Crawler - creation
  [Sitemap] # Subtest: Sitemap::Crawler - events
  [Sitemap]     ok 1 - Event handlers set without error
  [Sitemap]     1..1
  [Sitemap] ok 2 - Sitemap::Crawler - events
  [Sitemap] # Subtest: Sitemap::Crawler - on-error payload shape is consistent
  [Sitemap]     ok 1 - At least one error surfaced
  [Sitemap]     ok 2 - Payload has a url key
  [Sitemap]     ok 3 - Payload has an error key
  [Sitemap]     ok 4 - Payload has a status key (Nil for non-HTTP errors)
  [Sitemap]     ok 5 - HTTP error carries its status
  [Sitemap]     1..5
  [Sitemap] ok 3 - Sitemap::Crawler - on-error payload shape is consistent
  [Sitemap] # Subtest: Sitemap::Crawler - preserves port through crawl
  [Sitemap]     ok 1 - Crawled both pages on non-default port
  [Sitemap]     ok 2 - Item URLs retain the port
  [Sitemap]     1..2
  [Sitemap] ok 4 - Sitemap::Crawler - preserves port through crawl
  [Sitemap] # Subtest: Sitemap::Crawler - no deadlock when workers outpace queue
  [Sitemap]     ok 1 - Crawl completed without deadlock
  [Sitemap]     ok 2 - Crawled all 12 pages
  [Sitemap]     1..2
  [Sitemap] ok 5 - Sitemap::Crawler - no deadlock when workers outpace queue
  [Sitemap] # Subtest: Sitemap::Crawler - robots.txt Crawl-delay is honored
  [Sitemap]     ok 1 - Crawled both pages despite Crawl-delay (no crash)
  [Sitemap]     ok 2 - Crawl-delay spaced requests (~2.2s elapsed)
  [Sitemap]     1..2
  [Sitemap] ok 6 - Sitemap::Crawler - robots.txt Crawl-delay is honored
  [Sitemap] # Subtest: Sitemap::Crawler - each crawl() starts fresh
  [Sitemap]     ok 1 - First crawl found both pages
  [Sitemap]     ok 2 - Second crawl found both pages again
  [Sitemap]     ok 3 - Second crawl issued fresh HTTP requests
  [Sitemap]     1..3
  [Sitemap] ok 7 - Sitemap::Crawler - each crawl() starts fresh
  [Sitemap] # Subtest: Sitemap::Crawler - multiple crawls with extract-news do not crash on reset
  [Sitemap]     ok 1 - First crawl (with extract-news) visited both pages
  [Sitemap]     ok 2 - First crawl extracted the NewsArticle
  [Sitemap]     ok 3 - First crawl raised no errors
  [Sitemap]     ok 4 - Second crawl did not crash on !reset-state
  [Sitemap]     ok 5 - Second crawl re-extracted the NewsArticle
  [Sitemap]     ok 6 - Second crawl raised no errors
  [Sitemap]     1..6
  [Sitemap] ok 8 - Sitemap::Crawler - multiple crawls with extract-news do not crash on reset
  [Sitemap] # Subtest: Sitemap::Crawler - noindex page excluded via on-ignore
  [Sitemap]     ok 1 - Noindex page excluded from sitemap
  [Sitemap]     ok 2 - Child of noindex page still discovered
  [Sitemap]     ok 3 - on-ignore called once
  [Sitemap]     ok 4 - on-ignore got the URL
  [Sitemap]     ok 5 - on-ignore got the reason
  [Sitemap]     1..5
  [Sitemap] ok 9 - Sitemap::Crawler - noindex page excluded via on-ignore
  [Sitemap] # Subtest: Sitemap::Crawler - noindex requires a whole directive token
  [Sitemap]     ok 1 - content="notnoindex" is NOT treated as noindex
  [Sitemap]     ok 2 - child of notnoindex page still crawled
  [Sitemap]     ok 3 - content="noindex, follow" IS still excluded (whole-token match)
  [Sitemap]     ok 4 - directive-list excluded via on-ignore
  [Sitemap]     ok 5 - content="noindexed" is NOT treated as noindex
  [Sitemap]     1..5
  [Sitemap] ok 10 - Sitemap::Crawler - noindex requires a whole directive token
  [Sitemap] # Subtest: Sitemap::Crawler - throwing subscriber does not leak urls-found
  [Sitemap] Error in on-ignore handler: subscriber boom
  [Sitemap]     ok 1 - noindex page not added to sitemap
  [Sitemap]     ok 2 - urls-found balanced despite throwing on-ignore
  [Sitemap]     1..2
  [Sitemap] ok 11 - Sitemap::Crawler - throwing subscriber does not leak urls-found
  [Sitemap] # Subtest: Sitemap::Crawler - gzip-encoded pages decompressed
  [Sitemap]     ok 1 - Both gzipped pages crawled
  [Sitemap]     ok 2 - Link from gzipped page discovered
  [Sitemap]     ok 3 - Gzipped page itself added
  [Sitemap]     1..3
  [Sitemap] ok 12 - Sitemap::Crawler - gzip-encoded pages decompressed
  [Sitemap] # Subtest: Sitemap::Crawler - default user agent carries the package version
  [Sitemap]     ok 1 - Default UA derives from Sitemap::Config::VERSION, not a hardcoded string
  [Sitemap]     1..1
  [Sitemap] ok 13 - Sitemap::Crawler - default user agent carries the package version
  [Sitemap] # Subtest: Sitemap::Crawler - gzip robots.txt rules and fractional Crawl-delay honored
  [Sitemap]     ok 1 - Both allowed pages crawled
  [Sitemap]     ok 2 - Disallowed /secret not crawled (gzip robots parsed)
  [Sitemap]     ok 3 - Fractional Crawl-delay honored (~0.57s elapsed)
  [Sitemap]     1..3
  [Sitemap] ok 14 - Sitemap::Crawler - gzip robots.txt rules and fractional Crawl-delay honored
  [Sitemap] # Subtest: Sitemap::Crawler - ../ image and hreflang URLs collapse in sitemap output
  [Sitemap]     ok 1 - page1 item found
  [Sitemap]     ok 2 - one image extracted
  [Sitemap]     ok 3 - image ../ collapsed, no literal dot segment: http://127.0.0.1:19510/img/x.jpg
  [Sitemap]     ok 4 - one hreflang extracted
  [Sitemap]     ok 5 - hreflang ../ collapsed, no literal dot segment: http://127.0.0.1:19510/en/
  [Sitemap]     ok 6 - page link ../ still resolves and is followed
  [Sitemap]     1..6
  [Sitemap] ok 15 - Sitemap::Crawler - ../ image and hreflang URLs collapse in sitemap output
  [Sitemap] # Subtest: Sitemap::Crawler - query-only start URL keeps its empty path
  [Sitemap]     ok 1 - normalized start URL keeps the empty path (no / inserted before ?)
  [Sitemap]     ok 2 - crawled item URL keeps the empty path + query
  [Sitemap]     ok 3 - no spurious / inserted before the query
  [Sitemap]     1..3
  [Sitemap] ok 16 - Sitemap::Crawler - query-only start URL keeps its empty path
  [Sitemap] # Subtest: Sitemap::Crawler - links with brackets are followed
  [Sitemap]     ok 1 - Both pages crawled
  [Sitemap]     ok 2 - Bracketed link discovered, encoded and followed
  [Sitemap]     1..2
  [Sitemap] ok 17 - Sitemap::Crawler - links with brackets are followed
  [Sitemap] # Subtest: Sitemap::Crawler - malformed start URL errors clearly
  [Sitemap]     # Subtest: Space in URL dies with a clear message
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'invalid start URL'/
  [Sitemap]     ok 1 - Space in URL dies with a clear message
  [Sitemap]     # Subtest: Bad percent-escape dies with a clear message
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'invalid start URL'/
  [Sitemap]     ok 2 - Bad percent-escape dies with a clear message
  [Sitemap]     ok 3 - Brackets in start URL are accepted (encoded by normalize-url)
  [Sitemap]     1..3
  [Sitemap] ok 18 - Sitemap::Crawler - malformed start URL errors clearly
  [Sitemap] # Subtest: Sitemap::Crawler - schemeless start URLs are normalized
  [Sitemap]     ok 1 - Bare domain start URL becomes https
  [Sitemap]     ok 2 - Bare domain with a path keeps the path
  [Sitemap]     ok 3 - Scheme-relative //host start URL becomes https
  [Sitemap]     ok 4 - Explicit http URL is untouched
  [Sitemap]     1..4
  [Sitemap] ok 19 - Sitemap::Crawler - schemeless start URLs are normalized
  [Sitemap] # Subtest: Sitemap::Crawler - https falls back to http
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] HTTPS page failed (The socket was closed during negotiation), retrying http://127.0.0.1:19706/ over HTTP...
  [Sitemap]     ok 1 - Start URL and the http page crawled after the https→http fallback
  [Sitemap]     ok 2 - Both items were fetched over http (fallback fired)
  [Sitemap]     ok 3 - https link stays skipped: different scheme is foreign (same-origin)
  [Sitemap]     1..3
  [Sitemap] ok 20 - Sitemap::Crawler - https falls back to http
  [Sitemap] # Subtest: Sitemap::Crawler - no per-page https retry after the whole-run fallback
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap]     ok 1 - https child was not retried over http after the whole-run fallback
  [Sitemap]     ok 2 - https child reported its own https error via on-error
  [Sitemap]     1..2
  [Sitemap] ok 21 - Sitemap::Crawler - no per-page https retry after the whole-run fallback
  [Sitemap] # Subtest: Sitemap::Crawler - crawl() resets tried-http-fallback for reuse
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] HTTPS page failed (The socket was closed during negotiation), retrying http://127.0.0.1:19709/ over HTTP...
  [Sitemap]     ok 1 - First crawl() succeeded via HTTPS→HTTP fallback
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] HTTPS page failed (The socket was closed during negotiation), retrying http://127.0.0.1:19709/ over HTTP...
  [Sitemap]     ok 2 - Second crawl() also succeeded (fallback flag was reset)
  [Sitemap]     1..2
  [Sitemap] ok 22 - Sitemap::Crawler - crawl() resets tried-http-fallback for reuse
  [Sitemap] # Subtest: Sitemap::Crawler - close releases resources
  [Sitemap]     ok 1 - Crawl ran
  [Sitemap]     ok 2 - close() runs after a crawl
  [Sitemap]     ok 3 - close() is safe to call twice
  [Sitemap]     1..3
  [Sitemap] ok 23 - Sitemap::Crawler - close releases resources
  [Sitemap] # Subtest: Sitemap::Crawler - max-depth check runs before mark-queued (race)
  [Sitemap]     ok 1 - /target was requested (reachable at depth 2 via /slow, not deduped)
  [Sitemap]     ok 2 - /target is present in the sitemap
  [Sitemap]     1..2
  [Sitemap] ok 24 - Sitemap::Crawler - max-depth check runs before mark-queued (race)
  [Sitemap] # Subtest: Sitemap::Crawler - query-only href resolves against the full base path
  [Sitemap]     ok 1 - query-only href resolved to /a/b?x=1 (full base path kept)
  [Sitemap]     ok 2 - no bogus /a/?x=1 request (base dir not used for query-only refs)
  [Sitemap]     ok 3 - resolved query-only URL present in the sitemap
  [Sitemap]     1..3
  [Sitemap] ok 25 - Sitemap::Crawler - query-only href resolves against the full base path
  [Sitemap] # Subtest: Sitemap::Crawler - AMP detection is scoped to real link tags
  [Sitemap]     ok 1 - page with literal rel="amphtml" only in JS is NOT excluded
  [Sitemap]     ok 2 - child of the JS-amp page still discovered
  [Sitemap]     ok 3 - page with a real <link rel="amphtml"> IS excluded
  [Sitemap]     ok 4 - excluded via on-ignore reason "AMP page"
  [Sitemap]     ok 5 - page with <html lang="en" amp> IS excluded
  [Sitemap]     ok 6 - excluded via on-ignore reason "AMP page"
  [Sitemap]     1..6
  [Sitemap] ok 26 - Sitemap::Crawler - AMP detection is scoped to real link tags
  [Sitemap] # Subtest: Sitemap::Crawler - exclude-dirs skips path prefixes
  [Sitemap]     ok 1 - start URL still crawled
  [Sitemap]     ok 2 - non-excluded child still crawled
  [Sitemap]     ok 3 - /admin prefix excluded from sitemap
  [Sitemap]     ok 4 - /administrator NOT excluded (prefix matches whole segments only)
  [Sitemap]     ok 5 - /admin/secret never requested
  [Sitemap]     1..5
  [Sitemap] ok 27 - Sitemap::Crawler - exclude-dirs skips path prefixes
  [Sitemap] # Subtest: Sitemap::Crawler - exclude-dirs applies to the start URL
  [Sitemap]     ok 1 - excluded start URL adds no items
  [Sitemap]     ok 2 - excluded start URL is never fetched
  [Sitemap]     ok 3 - start URL reported via on-ignore as "excluded dir"
  [Sitemap]     1..3
  [Sitemap] ok 28 - Sitemap::Crawler - exclude-dirs applies to the start URL
  [Sitemap] # Subtest: Sitemap::Crawler - rejects empty/fragment-only start URLs
  [Sitemap]     # Subtest: fragment-only start URL rejected
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / 'invalid start URL' /
  [Sitemap]     ok 1 - fragment-only start URL rejected
  [Sitemap]     # Subtest: empty start URL rejected
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / 'invalid start URL' /
  [Sitemap]     ok 2 - empty start URL rejected
  [Sitemap]     1..2
  [Sitemap] ok 29 - Sitemap::Crawler - rejects empty/fragment-only start URLs
  [Sitemap] # Subtest: Sitemap::Crawler - rejects non-http(s) start URLs
  [Sitemap]     # Subtest: ftp seed rejected
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / 'must be http:// or https://' /
  [Sitemap]     ok 1 - ftp seed rejected
  [Sitemap]     # Subtest: file seed rejected
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / 'must be http:// or https://' /
  [Sitemap]     ok 2 - file seed rejected
  [Sitemap]     ok 3 - http seed accepted
  [Sitemap]     1..3
  [Sitemap] ok 30 - Sitemap::Crawler - rejects non-http(s) start URLs
  [Sitemap] # Subtest: Sitemap::Crawler - follow-links False crawls only the start URL
  [Sitemap]     ok 1 - only the start URL is in the sitemap
  [Sitemap]     ok 2 - start URL is /index
  [Sitemap]     ok 3 - discovered links are never requested
  [Sitemap]     1..3
  [Sitemap] ok 31 - Sitemap::Crawler - follow-links False crawls only the start URL
  [Sitemap] # Subtest: Sitemap::Crawler - max-images caps images per page
  [Sitemap]     ok 1 - images capped at max-images: 2
  [Sitemap]     1..1
  [Sitemap] ok 32 - Sitemap::Crawler - max-images caps images per page
  [Sitemap] # Subtest: Sitemap::Crawler - <base href> used for link and asset resolution
  [Sitemap]     ok 1 - both pages under the base path crawled
  [Sitemap]     ok 2 - relative link resolved against <base href> (/sub/page2, not /page2)
  [Sitemap]     ok 3 - link was not resolved against the page URL alone
  [Sitemap]     ok 4 - page itself is present
  [Sitemap]     ok 5 - one image extracted
  [Sitemap]     ok 6 - relative image src resolved against <base href>: {@img-urls[0]}
  [Sitemap]     ok 7 - one hreflang extracted
  [Sitemap]     ok 8 - relative hreflang href resolved against <base href>: {@hreflang-urls[0]}
  [Sitemap]     1..8
  [Sitemap] ok 33 - Sitemap::Crawler - <base href> used for link and asset resolution
  [Sitemap] # Subtest: Sitemap::Crawler - excluded-extension seed reported via on-ignore
  [Sitemap]     ok 1 - no items from an excluded-extension seed
  [Sitemap]     ok 2 - one on-ignore event for the seed
  [Sitemap]     ok 3 - reason names the excluded extension
  [Sitemap]     ok 4 - the seed URL is reported
  [Sitemap]     1..4
  [Sitemap] ok 34 - Sitemap::Crawler - excluded-extension seed reported via on-ignore
  [Sitemap] # Subtest: Sitemap::Crawler - robots-disallowed seed reported via on-ignore
  [Sitemap]     ok 1 - no items from a robots-disallowed seed
  [Sitemap]     ok 2 - one on-ignore event for the seed
  [Sitemap]     ok 3 - reason names the robots rule
  [Sitemap]     1..3
  [Sitemap] ok 35 - Sitemap::Crawler - robots-disallowed seed reported via on-ignore
  [Sitemap] # Subtest: Sitemap::Crawler - robots-disallowed children stay silent
  [Sitemap]     ok 1 - disallowed child not crawled
  [Sitemap]     ok 2 - allowed seed page crawled
  [Sitemap]     ok 3 - disallowed child dropped silently (no on-ignore)
  [Sitemap]     1..3
  [Sitemap] ok 36 - Sitemap::Crawler - robots-disallowed children stay silent
  [Sitemap] # Subtest: Sitemap::Crawler - retries 429/5xx, not 4xx
  [Sitemap]     ok 1 - 429 response retried once (Retry-After honored)
  [Sitemap]     ok 2 - 503 response retried once
  [Sitemap]     ok 3 - 404 response not retried
  [Sitemap]     ok 4 - slow page crawled after 429
  [Sitemap]     ok 5 - oops page crawled after 503
  [Sitemap]     ok 6 - gone page not crawled
  [Sitemap]     ok 7 - 404 recorded as an on-error with its status
  [Sitemap]     1..7
  [Sitemap] ok 37 - Sitemap::Crawler - retries 429/5xx, not 4xx
  [Sitemap] # Subtest: Sitemap::Crawler - empty 200 body reported via on-error
  [Sitemap]     ok 1 - empty-body page not added to the sitemap
  [Sitemap]     ok 2 - empty-body page reported exactly once
  [Sitemap]     ok 3 - on-error carries the 200 status
  [Sitemap]     ok 4 - on-error names the empty body
  [Sitemap]     ok 5 - on-error carries the page URL
  [Sitemap]     1..5
  [Sitemap] ok 38 - Sitemap::Crawler - empty 200 body reported via on-error
  [Sitemap] # Subtest: Sitemap::Crawler - foreign <base href> honors that host robots.txt
  [Sitemap]     ok 1 - foreign-host /secret never requested (its robots.txt disallows it)
  [Sitemap]     ok 2 - foreign-host /public crawled (allowed by that host robots.txt)
  [Sitemap]     ok 3 - allowed foreign page in sitemap
  [Sitemap]     ok 4 - disallowed foreign page not in sitemap
  [Sitemap]     ok 5 - without robots, the foreign page is still crawled (deliberate boundary)
  [Sitemap]     1..5
  [Sitemap] ok 39 - Sitemap::Crawler - foreign <base href> honors that host robots.txt
  [Sitemap] # Subtest: Sitemap::Crawler - https fallback is tracked per origin
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] HTTPS page failed (The socket was closed during negotiation), retrying http://127.0.0.1:19812/page over HTTP...
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] HTTPS page failed (The socket was closed during negotiation), retrying http://127.0.0.1:19811/page over HTTP...
  [Sitemap]     ok 1 - origin A retried over http (its own https→http fallback)
  [Sitemap]     ok 2 - origin B ALSO retried over http (per-origin tracking, not a single global cap)
  [Sitemap]     ok 3 - failed https URLs were retried, not emitted as errors
  [Sitemap]     ok 4 - no https error surfaced (both were recovered by fallback)
  [Sitemap]     1..4
  [Sitemap] ok 40 - Sitemap::Crawler - https fallback is tracked per origin
  [Sitemap] # Subtest: Sitemap::Crawler - per-origin robots.txt is fetched once and applied per host
  [Sitemap]     ok 1 - origin B robots.txt fetched exactly once
  [Sitemap]     ok 2 - origin C robots.txt fetched exactly once
  [Sitemap]     ok 3 - B public crawled
  [Sitemap]     ok 4 - C public crawled
  [Sitemap]     ok 5 - B secret blocked by its own robots.txt
  [Sitemap]     ok 6 - C secret blocked by its own robots.txt
  [Sitemap]     1..6
  [Sitemap] ok 41 - Sitemap::Crawler - per-origin robots.txt is fetched once and applied per host
  [Sitemap] # Subtest: Sitemap::Crawler - :queued-cap caps the URL queue
  [Sitemap]     ok 1 - :queued-cap accepted
  [Sitemap]     ok 2 - default queued-cap is 100000
  [Sitemap]     1..2
  [Sitemap] ok 42 - Sitemap::Crawler - :queued-cap caps the URL queue
  [Sitemap] # Subtest: Sitemap::Crawler - a latin-1 page body does not crash the crawl
  [Sitemap]     ok 1 - latin-1 page and its link both crawled
  [Sitemap]     ok 2 - link inside the latin-1 page discovered
  [Sitemap]     1..2
  [Sitemap] ok 43 - Sitemap::Crawler - a latin-1 page body does not crash the crawl
  [Sitemap] # Subtest: Sitemap::Crawler - crawl-delay is enforced per origin, not globally
  [Sitemap]     ok 1 - All A and C pages crawled (a1..a4, c1, c2)
  [Sitemap]     ok 2 - Origin A served 4 pages
  [Sitemap]     ok 3 - Origin C served 2 pages
  [Sitemap]     ok 4 - Crawl-delay sleeps overlap across origins (~12.2s, globally-serialized would be ~16s)
  [Sitemap]     ok 5 - Origin A pages spaced by its own crawl-delay (4.0s gap)
  [Sitemap]     ok 6 - Origin A pages spaced by its own crawl-delay (4.0s gap)
  [Sitemap]     ok 7 - Origin A pages spaced by its own crawl-delay (4.0s gap)
  [Sitemap]     ok 8 - Origin C pages spaced by its own crawl-delay
  [Sitemap]     1..8
  [Sitemap] ok 44 - Sitemap::Crawler - crawl-delay is enforced per origin, not globally
  [Sitemap] # Subtest: Sitemap::Crawler - crawl() still works after close()
  [Sitemap]     ok 1 - first crawl discovers both pages
  [Sitemap]     ok 2 - on-add fired during the first crawl
  [Sitemap]     ok 3 - crawl after close() runs without crashing
  [Sitemap]     ok 4 - on-add fires again after close() (suppliers stay live)
  [Sitemap]     1..4
  [Sitemap] ok 45 - Sitemap::Crawler - crawl() still works after close()
  [Sitemap] # Subtest: Sitemap::Crawler - redirects are re-enqueued through normal gates
  [Sitemap]     ok 1 - redirect target crawled
  [Sitemap]     ok 2 - links on the redirect target were followed
  [Sitemap]     ok 3 - redirect surfaced via on-ignore
  [Sitemap]     1..3
  [Sitemap] ok 46 - Sitemap::Crawler - redirects are re-enqueued through normal gates
  [Sitemap] # Subtest: Sitemap::Crawler - :max-redirects bounds endlessly-unique redirect chains
  [Sitemap]     ok 1 - chain of 3 real redirect hops fetched, the 4th refused
  [Sitemap]     ok 2 - cap refusal surfaced via on-ignore with the hop limit
  [Sitemap]     1..2
  [Sitemap] ok 47 - Sitemap::Crawler - :max-redirects bounds endlessly-unique redirect chains
  [Sitemap] # Subtest: Sitemap::Crawler - redirect into robots-disallowed path is refused
  [Sitemap]     ok 1 - disallowed redirect target never added
  [Sitemap]     ok 2 - refused by the robots gate after redirect
  [Sitemap]     1..2
  [Sitemap] ok 48 - Sitemap::Crawler - redirect into robots-disallowed path is refused
  [Sitemap] # Subtest: Sitemap::Crawler - non-HTML content types are skipped
  [Sitemap]     ok 1 - PDF response never added
  [Sitemap]     ok 2 - skipped with a clear reason
  [Sitemap]     1..2
  [Sitemap] ok 49 - Sitemap::Crawler - non-HTML content types are skipped
  [Sitemap] # Subtest: Sitemap::Crawler - redirect Location fragment is stripped from the target
  [Sitemap]     ok 1 - redirect target crawled exactly once
  [Sitemap]     ok 2 - target URL carries no " \#..." fragment
  [Sitemap]     1..2
  [Sitemap] ok 50 - Sitemap::Crawler - redirect Location fragment is stripped from the target
  [Sitemap] # Subtest: Sitemap::Crawler - cross-origin redirect target is refused
  [Sitemap]     ok 1 - foreign redirect target never added
  [Sitemap]     ok 2 - refused with an explicit reason
  [Sitemap]     1..2
  [Sitemap] ok 51 - Sitemap::Crawler - cross-origin redirect target is refused
  [Sitemap] # Subtest: Sitemap::Crawler - 3xx with Location follows, 304 is not a crawl error
  [Sitemap]     ok 1 - 300 with Location followed to target
  [Sitemap]     ok 2 - 300 not surfaced as a crawl error
  [Sitemap]     ok 3 - 304 not surfaced as a crawl error
  [Sitemap]     ok 4 - 304 reported via on-ignore
  [Sitemap]     1..4
  [Sitemap] ok 52 - Sitemap::Crawler - 3xx with Location follows, 304 is not a crawl error
  [Sitemap] # Subtest: Sitemap::Crawler - is-retryable-error distinguishes transport from permanent errors
  [Sitemap]     ok 1 - header timeout is retried
  [Sitemap]     ok 2 - HTTP 404 is not retried (permanent)
  [Sitemap]     ok 3 - HTTP 410 is not retried (permanent)
  [Sitemap]     ok 4 - HTTP 429 is retried
  [Sitemap]     ok 5 - HTTP 500 is retried
  [Sitemap]     ok 6 - HTTP 502 is retried
  [Sitemap]     ok 7 - HTTP 503 is retried
  [Sitemap]     1..7
  [Sitemap] ok 53 - Sitemap::Crawler - is-retryable-error distinguishes transport from permanent errors
  [Sitemap] # Subtest: Sitemap::Crawler - non-web, excluded-extension and fragment-only links are skipped without crash (CQ-F5)
  [Sitemap]     ok 1 - the real link is queued and crawled
  [Sitemap]     ok 2 - excluded-extension (.js) link is not queued
  [Sitemap]     ok 3 - non-web scheme links are not queued
  [Sitemap]     1..3
  [Sitemap] ok 54 - Sitemap::Crawler - non-web, excluded-extension and fragment-only links are skipped without crash (CQ-F5)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/07-extensions.rakutest
  [Sitemap] 1..26
  [Sitemap] # Subtest: extract-images from img tags
  [Sitemap]     ok 1 - Found 3 images
  [Sitemap]     ok 2 - Found image1.jpg
  [Sitemap]     ok 3 - Found image2.png
  [Sitemap]     ok 4 - Found image3.gif
  [Sitemap]     1..4
  [Sitemap] ok 1 - extract-images from img tags
  [Sitemap] # Subtest: extract-images from picture/srcset
  [Sitemap]     ok 1 - Found small.jpg from srcset
  [Sitemap]     ok 2 - Found large.jpg from srcset
  [Sitemap]     ok 3 - Found fallback.jpg
  [Sitemap]     1..3
  [Sitemap] ok 2 - extract-images from picture/srcset
  [Sitemap] # Subtest: extract-images from og:image
  [Sitemap]     ok 1 - Found 1 og:image
  [Sitemap]     ok 2 - Found og-image.jpg
  [Sitemap]     1..2
  [Sitemap] ok 3 - extract-images from og:image
  [Sitemap] # Subtest: extract-hreflang-links
  [Sitemap]     ok 1 - Found 2 hreflang links
  [Sitemap]     ok 2 - First link has lang=en
  [Sitemap]     ok 3 - First link has correct URL
  [Sitemap]     ok 4 - Second link has lang=de
  [Sitemap]     1..4
  [Sitemap] ok 4 - extract-hreflang-links
  [Sitemap] # Subtest: image deduplication
  [Sitemap]     ok 1 - Deduplicated to 1 image
  [Sitemap]     1..1
  [Sitemap] ok 5 - image deduplication
  [Sitemap] # Subtest: exclude-extensions filters images
  [Sitemap]     ok 1 - jpg is excluded
  [Sitemap]     1..1
  [Sitemap] ok 6 - exclude-extensions filters images
  [Sitemap] # Subtest: Builder omits extension namespaces when not used
  [Sitemap]     ok 1 - xmlns:image omitted when no images
  [Sitemap]     ok 2 - xmlns:xhtml omitted when no links
  [Sitemap]     ok 3 - xmlns:video omitted when no videos
  [Sitemap]     ok 4 - xmlns:news omitted when no news
  [Sitemap]     ok 5 - xmlns:android omitted when no android:link
  [Sitemap]     ok 6 - xmlns:amp omitted when no amp:link
  [Sitemap]     1..6
  [Sitemap] ok 7 - Builder omits extension namespaces when not used
  [Sitemap] # Subtest: Builder namespace gating - with images
  [Sitemap]     ok 1 - Has xmlns:image when images present
  [Sitemap]     1..1
  [Sitemap] ok 8 - Builder namespace gating - with images
  [Sitemap] # Subtest: Builder namespace gating - with hreflang links
  [Sitemap]     ok 1 - Has xmlns:xhtml when links present
  [Sitemap]     1..1
  [Sitemap] ok 9 - Builder namespace gating - with hreflang links
  [Sitemap] # Subtest: extract-images=False
  [Sitemap]     ok 1 - extract-images is False
  [Sitemap]     1..1
  [Sitemap] ok 10 - extract-images=False
  [Sitemap] # Subtest: extract-hreflang=False
  [Sitemap]     ok 1 - extract-hreflang is False
  [Sitemap]     1..1
  [Sitemap] ok 11 - extract-hreflang=False
  [Sitemap] # Subtest: Image URL resolution with base
  [Sitemap]     ok 1 - Found 1 image
  [Sitemap]     ok 2 - URL resolved with base
  [Sitemap]     1..2
  [Sitemap] ok 12 - Image URL resolution with base
  [Sitemap] # Subtest: extract-videos from video tag with src and poster
  [Sitemap]     ok 1 - Found 1 video
  [Sitemap]     ok 2 - Video URL correct
  [Sitemap]     ok 3 - Poster correct
  [Sitemap]     1..3
  [Sitemap] ok 13 - extract-videos from video tag with src and poster
  [Sitemap] # Subtest: extract-videos from source inside video
  [Sitemap]     ok 1 - Found 2 videos
  [Sitemap]     ok 2 - First video URL correct
  [Sitemap]     ok 3 - First video has poster
  [Sitemap]     ok 4 - Second video URL correct
  [Sitemap]     1..4
  [Sitemap] ok 14 - extract-videos from source inside video
  [Sitemap] # Subtest: extract-videos from og:video meta tag
  [Sitemap]     ok 1 - Found 1 og:video
  [Sitemap]     ok 2 - og:video URL correct
  [Sitemap]     1..2
  [Sitemap] ok 15 - extract-videos from og:video meta tag
  [Sitemap] # Subtest: og:video paired with og:image
  [Sitemap]     ok 1 - Found 1 video
  [Sitemap]     ok 2 - og:image used as poster
  [Sitemap]     1..2
  [Sitemap] ok 16 - og:video paired with og:image
  [Sitemap] # Subtest: extract-videos relative URL resolution
  [Sitemap]     ok 1 - Found 1 video
  [Sitemap]     ok 2 - Video URL resolved
  [Sitemap]     ok 3 - Poster URL resolved
  [Sitemap]     1..3
  [Sitemap] ok 17 - extract-videos relative URL resolution
  [Sitemap] # Subtest: extract-videos deduplication
  [Sitemap]     ok 1 - Deduplicated to 1 video
  [Sitemap]     1..1
  [Sitemap] ok 18 - extract-videos deduplication
  [Sitemap] # Subtest: extract-videos returns empty list when no videos
  [Sitemap]     ok 1 - No videos found
  [Sitemap]     1..1
  [Sitemap] ok 19 - extract-videos returns empty list when no videos
  [Sitemap] # Subtest: extract-videos=False
  [Sitemap]     ok 1 - extract-videos is False
  [Sitemap]     1..1
  [Sitemap] ok 20 - extract-videos=False
  [Sitemap] # Subtest: Builder namespace gating - with videos
  [Sitemap]     ok 1 - Has xmlns:video when videos present
  [Sitemap]     ok 2 - Contains video:video element
  [Sitemap]     1..2
  [Sitemap] ok 21 - Builder namespace gating - with videos
  [Sitemap] # Subtest: Video with no thumbnail is skipped
  [Sitemap]     ok 1 - No video element without thumbnail
  [Sitemap]     1..1
  [Sitemap] ok 22 - Video with no thumbnail is skipped
  [Sitemap] # Subtest: Video boolean flags are tri-state
  [Sitemap]     ok 1 - Explicit "no" parses to False
  [Sitemap]     ok 2 - Explicit "yes" parses to True
  [Sitemap]     ok 3 - Absent flag stays unset (not False)
  [Sitemap]     ok 4 - False renders as "no"
  [Sitemap]     ok 5 - Unset flags emit no element
  [Sitemap]     ok 6 - True renders as "yes"
  [Sitemap]     1..6
  [Sitemap] ok 23 - Video boolean flags are tri-state
  [Sitemap] # Subtest: Video without thumbnail/content-loc warns on drop
  [Sitemap]     ok 1 - Dropped video emits a warning
  [Sitemap]     1..1
  [Sitemap] ok 24 - Video without thumbnail/content-loc warns on drop
  [Sitemap] # Subtest: Video.from-hash parses boolean strings
  [Sitemap]     ok 1 - "no" parses to False, not True
  [Sitemap]     ok 2 - "false" parses to False, not True
  [Sitemap]     ok 3 - "0" parses to False, not True
  [Sitemap]     ok 4 - "TRUE" parses to True
  [Sitemap]     ok 5 - "yes" parses to True
  [Sitemap]     ok 6 - "1" parses to True
  [Sitemap]     ok 7 - Absent flag stays unset (tri-state preserved)
  [Sitemap]     1..7
  [Sitemap] ok 25 - Video.from-hash parses boolean strings
  [Sitemap] # Subtest: url-path-extension considers only the URL path, never the host
  [Sitemap]     ok 1 - a dotted host yields no extension
  [Sitemap]     ok 2 - path extension is extracted
  [Sitemap]     ok 3 - extensionless path yields an empty string
  [Sitemap]     ok 4 - extension is case-folded and the query is stripped
  [Sitemap]     ok 5 - fragment is stripped
  [Sitemap]     ok 6 - only the final extension segment is returned
  [Sitemap]     1..6
  [Sitemap] ok 26 - url-path-extension considers only the URL path, never the host
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/08-input-parser.rakutest
  [Sitemap] 1..34
  [Sitemap] # Subtest: Sitemap::InputParser - detect-format from string
  [Sitemap]     ok 1 - XML sitemap detected
  [Sitemap]     ok 2 - Sitemap index detected
  [Sitemap]     ok 3 - RSS detected
  [Sitemap]     ok 4 - Atom detected
  [Sitemap]     ok 5 - RSS content detected
  [Sitemap]     1..5
  [Sitemap] ok 1 - Sitemap::InputParser - detect-format from string
  [Sitemap] # Subtest: Sitemap::InputParser - BOM before xml declaration is detected (CQ-BOM)
  [Sitemap]     ok 1 - BOM + xml-decl + urlset detected (was TXT)
  [Sitemap]     ok 2 - BOM + urlset without decl still detected
  [Sitemap]     ok 3 - BOM + xml-decl + rss detected
  [Sitemap]     ok 4 - no BOM unchanged
  [Sitemap]     1..4
  [Sitemap] ok 2 - Sitemap::InputParser - BOM before xml declaration is detected (CQ-BOM)
  [Sitemap] # Subtest: Sitemap::InputParser - case-insensitive HTML/DOCTYPE sniffing
  [Sitemap]     ok 1 - Lowercase doctype html detected
  [Sitemap]     ok 2 - Uppercase doctype HTML detected (was TXT)
  [Sitemap]     ok 3 - Lowercase doctype keyword detected
  [Sitemap]     ok 4 - Uppercase html element detected (was TXT)
  [Sitemap]     ok 5 - Uppercase html element with attributes detected
  [Sitemap]     1..5
  [Sitemap] ok 3 - Sitemap::InputParser - case-insensitive HTML/DOCTYPE sniffing
  [Sitemap] # Subtest: Sitemap::InputParser - parse-rss
  [Sitemap]     ok 1 - Parsed 2 RSS items
  [Sitemap]     ok 2 - First URL correct
  [Sitemap]     ok 3 - Second URL correct
  [Sitemap]     1..3
  [Sitemap] ok 4 - Sitemap::InputParser - parse-rss
  [Sitemap] # Subtest: Sitemap::InputParser - parse-atom prefers rel=alternate over rel=self
  [Sitemap]     ok 1 - Parsed 1 Atom entry
  [Sitemap]     ok 2 - rel=alternate chosen over rel=self
  [Sitemap]     1..2
  [Sitemap] ok 5 - Sitemap::InputParser - parse-atom prefers rel=alternate over rel=self
  [Sitemap] # Subtest: Sitemap::InputParser - parse-rss skips namespaced atom:link
  [Sitemap]     ok 1 - Parsed 1 RSS item
  [Sitemap]     ok 2 - Plain link chosen over atom:link
  [Sitemap]     1..2
  [Sitemap] ok 6 - Sitemap::InputParser - parse-rss skips namespaced atom:link
  [Sitemap] # Subtest: Sitemap::InputParser - malformed RSS/Atom/MRSS returns () not a backtrace
  [Sitemap]     ok 1 - Malformed RSS yields no items
  [Sitemap]     ok 2 - Malformed Atom yields no items
  [Sitemap]     ok 3 - Malformed MRSS yields no items
  [Sitemap]     ok 4 - Garbage RSS yields no items
  [Sitemap]     ok 5 - Garbage Atom yields no items
  [Sitemap]     ok 6 - Garbage MRSS yields no items
  [Sitemap]     1..6
  [Sitemap] ok 7 - Sitemap::InputParser - malformed RSS/Atom/MRSS returns () not a backtrace
  [Sitemap] # Subtest: Sitemap::InputParser - parse-atom
  [Sitemap]     ok 1 - Parsed 2 Atom entries
  [Sitemap]     ok 2 - First URL correct
  [Sitemap]     ok 3 - Second URL correct
  [Sitemap]     1..3
  [Sitemap] ok 8 - Sitemap::InputParser - parse-atom
  [Sitemap] # Subtest: Sitemap::InputParser - parse-mrss
  [Sitemap]     ok 1 - Parsed 1 MRSS item
  [Sitemap]     ok 2 - URL correct (prefers media:content over <link>)
  [Sitemap]     1..2
  [Sitemap] ok 9 - Sitemap::InputParser - parse-mrss
  [Sitemap] # Subtest: Sitemap::InputParser - parse-html
  [Sitemap]     ok 1 - Parsed 2 HTML links
  [Sitemap]     ok 2 - First URL correct
  [Sitemap]     1..2
  [Sitemap] ok 10 - Sitemap::InputParser - parse-html
  [Sitemap] # Subtest: Sitemap::InputParser - parse-txt
  [Sitemap]     ok 1 - Parsed 3 TXT URLs (skipped comment)
  [Sitemap]     ok 2 - First URL correct
  [Sitemap]     1..2
  [Sitemap] ok 11 - Sitemap::InputParser - parse-txt
  [Sitemap] # Subtest: Sitemap::InputParser - parse-txt resolves relative paths with base-url
  [Sitemap]     ok 1 - 3 TXT lines still parsed
  [Sitemap]     ok 2 - Root-relative path resolved against the base URL
  [Sitemap]     ok 3 - Absolute URL left untouched
  [Sitemap]     ok 4 - Bare hostname line left untouched (ambiguous, not resolved)
  [Sitemap]     1..4
  [Sitemap] ok 12 - Sitemap::InputParser - parse-txt resolves relative paths with base-url
  [Sitemap] # Subtest: Sitemap::InputParser - RSS/Atom/MRSS resolve relative links against base-url (CQ)
  [Sitemap]     ok 1 - RSS items parsed
  [Sitemap]     ok 2 - RSS relative <link> resolved against base-url
  [Sitemap]     ok 3 - RSS absolute <link> left untouched
  [Sitemap]     ok 4 - Atom relative <link href> resolved against base-url
  [Sitemap]     ok 5 - MRSS relative <link> resolved against base-url
  [Sitemap]     1..5
  [Sitemap] ok 13 - Sitemap::InputParser - RSS/Atom/MRSS resolve relative links against base-url (CQ)
  [Sitemap] # Subtest: Sitemap::InputParser - parse-html resolves relative hrefs with base-url
  [Sitemap]     ok 1 - relative + absolute links kept, mailto dropped
  [Sitemap]     ok 2 - Relative href resolved against the base URL
  [Sitemap]     ok 3 - Absolute href unchanged
  [Sitemap]     ok 4 - Relative href still dropped without a base URL (unchanged behavior)
  [Sitemap]     1..4
  [Sitemap] ok 14 - Sitemap::InputParser - parse-html resolves relative hrefs with base-url
  [Sitemap] # Subtest: Sitemap::InputParser - parse-file with RSS file
  [Sitemap]     ok 1 - Parsed 2 items from RSS file
  [Sitemap]     1..1
  [Sitemap] ok 15 - Sitemap::InputParser - parse-file with RSS file
  [Sitemap] # Subtest: Sitemap::InputParser - parse-file with Atom file
  [Sitemap]     ok 1 - Parsed 2 items from Atom file
  [Sitemap]     1..1
  [Sitemap] ok 16 - Sitemap::InputParser - parse-file with Atom file
  [Sitemap] # Subtest: Sitemap::InputParser - parse-file with HTML file
  [Sitemap]     ok 1 - Parsed 3 items from HTML file
  [Sitemap]     1..1
  [Sitemap] ok 17 - Sitemap::InputParser - parse-file with HTML file
  [Sitemap] # Subtest: Sitemap::InputParser - parse-file with TXT file
  [Sitemap]     ok 1 - Parsed 4 items from TXT file (skipped comment)
  [Sitemap]     1..1
  [Sitemap] ok 18 - Sitemap::InputParser - parse-file with TXT file
  [Sitemap] # Subtest: Sitemap::InputParser - parse-url fetches and parses
  [Sitemap]     ok 1 - Parsed 1 item from remote sitemap
  [Sitemap]     ok 2 - Remote URL correct
  [Sitemap]     1..2
  [Sitemap] ok 19 - Sitemap::InputParser - parse-url fetches and parses
  [Sitemap] # Subtest: Sitemap::InputParser - pubDate parsed via parse-date(:optional)
  [Sitemap]     ok 1 - RSS RFC-822 pubDate parsed
  [Sitemap]     ok 2 - RSS RFC-822 offset preserved
  [Sitemap]     ok 3 - Atom RFC-822 updated parsed
  [Sitemap]     ok 4 - MRSS RFC-822 pubDate parsed
  [Sitemap]     ok 5 - Invalid pubDate dropped without aborting parse
  [Sitemap]     1..5
  [Sitemap] ok 20 - Sitemap::InputParser - pubDate parsed via parse-date(:optional)
  [Sitemap] # Subtest: Sitemap::InputParser - parse-file handles gzipped sitemap
  [Sitemap]     ok 1 - Parsed 1 item from gzipped file
  [Sitemap]     ok 2 - Gzip file URL correct
  [Sitemap]     1..2
  [Sitemap] ok 21 - Sitemap::InputParser - parse-file handles gzipped sitemap
  [Sitemap] # Subtest: Sitemap::InputParser - parse-txt-file gunzips gzip magic bytes (CQ)
  [Sitemap]     ok 1 - gzip .txt yields both URLs (was 0: decode-text-body did not gunzip)
  [Sitemap]     ok 2 - First gzip URL correct
  [Sitemap]     ok 3 - missing .txt returns () not a crash
  [Sitemap]     1..3
  [Sitemap] ok 22 - Sitemap::InputParser - parse-txt-file gunzips gzip magic bytes (CQ)
  [Sitemap] # Subtest: Sitemap::InputParser - detect-format gunzips .gz files
  [Sitemap]     ok 1 - detect-format sniffs a gzipped XML sitemap as XML-Sitemap (was TXT)
  [Sitemap]     1..1
  [Sitemap] ok 23 - Sitemap::InputParser - detect-format gunzips .gz files
  [Sitemap] # Subtest: Sitemap::InputParser - truncated gzip returns () instead of throwing
  [Sitemap]     ok 1 - Truncated gzip yields no items, not a crash
  [Sitemap]     1..1
  [Sitemap] ok 24 - Sitemap::InputParser - truncated gzip returns () instead of throwing
  [Sitemap] # Subtest: Sitemap::InputParser - parse-url handles Content-Encoding: gzip
  [Sitemap]     ok 1 - Parsed 1 item from gzip-encoded response
  [Sitemap]     ok 2 - Gzip URL correct
  [Sitemap]     1..2
  [Sitemap] ok 25 - Sitemap::InputParser - parse-url handles Content-Encoding: gzip
  [Sitemap] # Subtest: unrecognised XML never degrades to TXT
  [Sitemap]     ok 1 - namespace-prefixed urlset is Unknown, not TXT
  [Sitemap]     1..1
  [Sitemap] ok 26 - unrecognised XML never degrades to TXT
  [Sitemap] # Subtest: RDF (RSS 1.0) content is Unknown, not TXT garbage
  [Sitemap]     ok 1 - RDF root sniffed as Unknown
  [Sitemap]     1..1
  [Sitemap] ok 27 - RDF (RSS 1.0) content is Unknown, not TXT garbage
  [Sitemap] # Subtest: MRSS detection requires an xmlns:media attribute binding
  [Sitemap]     ok 1 - CDATA mention of media: does not flip detection
  [Sitemap]     ok 2 - xmlns:media= inside description text does not flip to MRSS
  [Sitemap]     ok 3 - xmlns:media on the <rss> root open tag still flips to MRSS
  [Sitemap]     1..3
  [Sitemap] ok 28 - MRSS detection requires an xmlns:media attribute binding
  [Sitemap] # Subtest: atom rel matching uses whole tokens
  [Sitemap]     ok 1 - entry parsed
  [Sitemap]     ok 2 - alternate picked by exact token
  [Sitemap]     ok 3 - second fixture parsed
  [Sitemap]     ok 4 - rel="alternate" beats rel="alternate-link" (whole-token match)
  [Sitemap]     1..4
  [Sitemap] ok 29 - atom rel matching uses whole tokens
  [Sitemap] # Subtest: detect-format file branch is symmetric about missing files
  [Sitemap]     ok 1 - missing .xml file is Unknown, not assumed XML-Sitemap
  [Sitemap]     1..1
  [Sitemap] ok 30 - detect-format file branch is symmetric about missing files
  [Sitemap] # Subtest: Sitemap::InputParser - parse-txt drops non-URL junk lines
  [Sitemap]     ok 1 - Junk lines no longer become items
  [Sitemap]     ok 2 - Absolute URL preserved
  [Sitemap]     ok 3 - Host-shaped schemeless line preserved
  [Sitemap]     ok 4 - Relative refs resolve against the base URL and survive the junk filter
  [Sitemap]     1..4
  [Sitemap] ok 31 - Sitemap::InputParser - parse-txt drops non-URL junk lines
  [Sitemap] # Subtest: Sitemap::InputParser - parse-url -v failure messages never stringify a Str as a hash (CQ-F1)
  [Sitemap]     ok 1 - 500 response returns () not a crash
  [Sitemap]     ok 2 - fetch failure message mentions the fetch step
  [Sitemap]     ok 3 - no Str-hash crash in the -v fetch message
  [Sitemap]     ok 4 - no type-backtrace leaking to user
  [Sitemap]     ok 5 - corrupt gzip body returns () not a crash
  [Sitemap]     ok 6 - body failure message mentions the body step
  [Sitemap]     ok 7 - no Str-hash crash in the -v body message
  [Sitemap]     1..7
  [Sitemap] ok 32 - Sitemap::InputParser - parse-url -v failure messages never stringify a Str as a hash (CQ-F1)
  [Sitemap] # Subtest: Sitemap::InputParser - .rss file containing MRSS is sniffed, not parsed as RSS (B2)
  [Sitemap]     ok 1 - one item parsed from the .rss file
  [Sitemap]     ok 2 - .rss MRSS body parsed as MRSS: media:content URL preferred over <link>
  [Sitemap]     1..2
  [Sitemap] ok 33 - Sitemap::InputParser - .rss file containing MRSS is sniffed, not parsed as RSS (B2)
  [Sitemap] # Subtest: Sitemap::InputParser - parse-txt keeps bracketed IPv6 literals with a port (R1)
  [Sitemap]     ok 1 - IPv6-literal and plain URL lines kept, junk line dropped
  [Sitemap]     ok 2 - bracketed IPv6 literal with port and path kept
  [Sitemap]     ok 3 - bracketed IPv6 literal with bare port kept
  [Sitemap]     ok 4 - regular dotted-host line still kept
  [Sitemap]     1..4
  [Sitemap] ok 34 - Sitemap::InputParser - parse-txt keeps bracketed IPv6 literals with a port (R1)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/09-dir-scanner.rakutest
  [Sitemap] 1..38
  [Sitemap] # Subtest: Basic scan discovers correct URLs
  [Sitemap]     ok 1 - about.html found
  [Sitemap]     ok 2 - contact.html found
  [Sitemap]     ok 3 - blog/ found (directory)
  [Sitemap]     ok 4 - blog/post1.html found
  [Sitemap]     ok 5 - external link excluded
  [Sitemap]     ok 6 - index.html maps to root URL
  [Sitemap]     1..6
  [Sitemap] ok 1 - Basic scan discovers correct URLs
  [Sitemap] # Subtest: Entry fallback uses first sorted .html when no index.html
  [Sitemap]     ok 1 - First sorted .html is entry point
  [Sitemap]     1..1
  [Sitemap] ok 2 - Entry fallback uses first sorted .html when no index.html
  [Sitemap] # Subtest: Cycle detection prevents infinite loop
  [Sitemap]     ok 1 - Root URL appears only once despite cycles
  [Sitemap]     1..1
  [Sitemap] ok 3 - Cycle detection prevents infinite loop
  [Sitemap] # Subtest: Images extracted and included in sitemap
  [Sitemap]     ok 1 - Root page item found
  [Sitemap]     ok 2 - Images extracted
  [Sitemap]     ok 3 - Image URL contains logo.png
  [Sitemap]     1..3
  [Sitemap] ok 4 - Images extracted and included in sitemap
  [Sitemap] # Subtest: Hreflang links extracted
  [Sitemap]     ok 1 - One page found
  [Sitemap]     ok 2 - Two hreflang links extracted
  [Sitemap]     1..2
  [Sitemap] ok 5 - Hreflang links extracted
  [Sitemap] # Subtest: Base URL from --base-url flag
  [Sitemap]     ok 1 - All URLs use custom base URL
  [Sitemap]     1..1
  [Sitemap] ok 6 - Base URL from --base-url flag
  [Sitemap] # Subtest: Base URL derived from robots.txt
  [Sitemap]     ok 1 - All URLs use base from robots.txt
  [Sitemap]     1..1
  [Sitemap] ok 7 - Base URL derived from robots.txt
  [Sitemap] # Subtest: Default file:/// fallback when no robots.txt
  [Sitemap]     ok 1 - URL is file:/// for root
  [Sitemap]     1..1
  [Sitemap] ok 8 - Default file:/// fallback when no robots.txt
  [Sitemap] # Subtest: Relative robots Sitemap: URL roots URLs at the scan directory (CQ)
  [Sitemap]     ok 1 - relative Sitemap: does not collapse to filesystem root file:///
  [Sitemap]     ok 2 - URLs carry a directory path (rooted at the scan dir), not the bare filesystem root
  [Sitemap]     1..2
  [Sitemap] ok 9 - Relative robots Sitemap: URL roots URLs at the scan directory (CQ)
  [Sitemap] # Subtest: Empty file does not report a spurious read error (CQ)
  [Sitemap]     ok 1 - empty file emits no "Cannot read file" error
  [Sitemap]     ok 2 - root page is still scanned
  [Sitemap]     1..2
  [Sitemap] ok 10 - Empty file does not report a spurious read error (CQ)
  [Sitemap] # Subtest: Max depth limits crawling
  [Sitemap]     ok 1 - about.html found (depth 1)
  [Sitemap]     ok 2 - contact.html found (depth 1)
  [Sitemap]     ok 3 - blog/ found (depth 1)
  [Sitemap]     ok 4 - blog/post1.html not found (depth 2)
  [Sitemap]     1..4
  [Sitemap] ok 11 - Max depth limits crawling
  [Sitemap] # Subtest: Max depth limits index-less directory expansion
  [Sitemap]     ok 1 - docs/ found (depth 1)
  [Sitemap]     ok 2 - docs/readme.html not crawled (depth 2)
  [Sitemap]     1..2
  [Sitemap] ok 12 - Max depth limits index-less directory expansion
  [Sitemap] # Subtest: Max URLs limits results
  [Sitemap]     ok 1 - Only 2 URLs returned
  [Sitemap]     1..1
  [Sitemap] ok 13 - Max URLs limits results
  [Sitemap] # Subtest: Directory with index.html maps to trailing slash URL
  [Sitemap]     ok 1 - blog/ has trailing slash
  [Sitemap]     ok 2 - blog/index.html not in URLs
  [Sitemap]     1..2
  [Sitemap] ok 14 - Directory with index.html maps to trailing slash URL
  [Sitemap] # Subtest: Fragment and query links resolve to the file
  [Sitemap]     ok 1 - Fragment and query variants collapse to one page URL
  [Sitemap]     ok 2 - No resolve errors for fragment/query links
  [Sitemap]     1..2
  [Sitemap] ok 15 - Fragment and query links resolve to the file
  [Sitemap] # Subtest: Index-less dir does not duplicate subdir-with-index URL
  [Sitemap]     ok 1 - No duplicate URLs
  [Sitemap]     ok 2 - subdir-with-index URL appears exactly once
  [Sitemap]     ok 3 - index-less dir URL appears once
  [Sitemap]     ok 4 - sibling page crawled
  [Sitemap]     1..4
  [Sitemap] ok 16 - Index-less dir does not duplicate subdir-with-index URL
  [Sitemap] # Subtest: Page link to subdir index.html does not duplicate dir URL
  [Sitemap]     ok 1 - subdir-with-index URL appears exactly once (concurrency=1)
  [Sitemap]     ok 2 - No duplicate URLs (concurrency=1)
  [Sitemap]     ok 3 - subdir-with-index URL appears exactly once (concurrency=4)
  [Sitemap]     ok 4 - No duplicate URLs (concurrency=4)
  [Sitemap]     1..4
  [Sitemap] ok 17 - Page link to subdir index.html does not duplicate dir URL
  [Sitemap] # Subtest: Subdir-with-index reached via a dir task carries full extraction
  [Sitemap]     ok 1 - Subdir-with-index URL present
  [Sitemap]     ok 2 - Dir-with-index URL carries the index page images (not a bare add)
  [Sitemap]     ok 3 - Image URL correct
  [Sitemap]     ok 4 - Unlinked sibling page still crawled
  [Sitemap]     ok 5 - No duplicate URLs
  [Sitemap]     1..5
  [Sitemap] ok 18 - Subdir-with-index reached via a dir task carries full extraction
  [Sitemap] # Subtest: Directory without index.html is expanded
  [Sitemap]     ok 1 - docs/ URL added
  [Sitemap]     ok 2 - docs/readme.html crawled from index-less dir
  [Sitemap]     ok 3 - docs/guide.html crawled via link
  [Sitemap]     ok 4 - nested subdir manual.html crawled
  [Sitemap]     ok 5 - docs/ URL added even with no html children
  [Sitemap]     ok 6 - non-html children ignored
  [Sitemap]     1..6
  [Sitemap] ok 19 - Directory without index.html is expanded
  [Sitemap] # Subtest: Index-less directory respects max-urls cap
  [Sitemap]     ok 1 - No more than 2 URLs despite index-less dir
  [Sitemap]     ok 2 - docs/ not added once cap reached
  [Sitemap]     ok 3 - docs/b.html not crawled once cap reached
  [Sitemap]     1..3
  [Sitemap] ok 20 - Index-less directory respects max-urls cap
  [Sitemap] # Subtest: Symlink escaping root is rejected
  [Sitemap]     ok 1 - Symlink escape detected or resolved path rejected
  [Sitemap]     1..1
  [Sitemap] ok 21 - Symlink escaping root is rejected
  [Sitemap] # Subtest: Path escape attempt is handled safely
  [Sitemap]     ok 1 - Path escape handled safely
  [Sitemap]     1..1
  [Sitemap] ok 22 - Path escape attempt is handled safely
  [Sitemap] # Subtest: Non-HTML files completely ignored
  [Sitemap]     ok 1 - PDF not in sitemap
  [Sitemap]     ok 2 - PNG not in sitemap (as page)
  [Sitemap]     1..2
  [Sitemap] ok 23 - Non-HTML files completely ignored
  [Sitemap] # Subtest: on-add events emitted with URL strings
  [Sitemap]     ok 1 - on-add events emitted
  [Sitemap]     ok 2 - Event payload is a string
  [Sitemap]     ok 3 - URL uses derived base URL
  [Sitemap]     1..3
  [Sitemap] ok 24 - on-add events emitted with URL strings
  [Sitemap] # Subtest: Videos extracted and included in sitemap
  [Sitemap]     ok 1 - One page found
  [Sitemap]     ok 2 - Videos extracted
  [Sitemap]     ok 3 - Video URL contains video.mp4
  [Sitemap]     1..3
  [Sitemap] ok 25 - Videos extracted and included in sitemap
  [Sitemap] # Subtest: Parallel scan deduplicates self-linking seed
  [Sitemap]     ok 1 - No duplicate URLs in parallel scan
  [Sitemap]     ok 2 - Root URL appears exactly once
  [Sitemap]     1..2
  [Sitemap] ok 26 - Parallel scan deduplicates self-linking seed
  [Sitemap] # Subtest: Relative assets resolve against <base href> (filesystem linking kept)
  [Sitemap]     ok 1 - page found
  [Sitemap]     ok 2 - image resolves against <base href>
  [Sitemap]     ok 3 - hreflang resolves against <base href>
  [Sitemap]     ok 4 - relative link still followed via filesystem (not dragged off-tree by base)
  [Sitemap]     1..4
  [Sitemap] ok 27 - Relative assets resolve against <base href> (filesystem linking kept)
  [Sitemap] # Subtest: Unreadable subdirectory does not hang the parallel scan
  [Sitemap]     ok 1 - parallel scan completes despite unreadable subdirectory
  [Sitemap]     ok 2 - readable page still crawled
  [Sitemap]     ok 3 - on-error fired for the unreadable subdirectory
  [Sitemap]     1..3
  [Sitemap] ok 28 - Unreadable subdirectory does not hang the parallel scan
  [Sitemap] # Subtest: Unreadable subdirectory does not abort the sequential scan
  [Sitemap]     ok 1 - sequential scan completes and crawls the readable page despite unreadable subdirectory
  [Sitemap]     ok 2 - on-error fired for the unreadable subdirectory
  [Sitemap]     1..2
  [Sitemap] ok 29 - Unreadable subdirectory does not abort the sequential scan
  [Sitemap] # Subtest: scan() twice resets state and re-crawls
  [Sitemap]     ok 1 - each scan returns a fresh builder
  [Sitemap]     ok 2 - first scan found a.html
  [Sitemap]     ok 3 - second scan re-crawled and found a.html again
  [Sitemap]     ok 4 - second scan produced the same number of items
  [Sitemap]     1..4
  [Sitemap] ok 30 - scan() twice resets state and re-crawls
  [Sitemap] # Subtest: max-images caps images per page (was hardcoded 1000)
  [Sitemap]     ok 1 - root page found
  [Sitemap]     ok 2 - images capped at max-images: 2
  [Sitemap]     ok 3 - default max-images (1000) does not truncate 6 images
  [Sitemap]     1..3
  [Sitemap] ok 31 - max-images caps images per page (was hardcoded 1000)
  [Sitemap] # Subtest: Multiple on-add handlers all fire
  [Sitemap]     ok 1 - first on-add handler fires
  [Sitemap]     ok 2 - second on-add handler fires too, not replaced
  [Sitemap]     ok 3 - both handlers see the same number of URLs
  [Sitemap]     1..3
  [Sitemap] ok 32 - Multiple on-add handlers all fire
  [Sitemap] # Subtest: Repeated links to a subdir index file are not re-added
  [Sitemap]     ok 1 - sub/ added exactly once despite repeated links (concurrency=1)
  [Sitemap]     ok 2 - sub/index.html never added as its own URL (concurrency=1)
  [Sitemap]     ok 3 - No duplicate URLs (concurrency=1)
  [Sitemap]     ok 4 - sub/ added exactly once despite repeated links (concurrency=4)
  [Sitemap]     ok 5 - sub/index.html never added as its own URL (concurrency=4)
  [Sitemap]     ok 6 - No duplicate URLs (concurrency=4)
  [Sitemap]     1..6
  [Sitemap] ok 33 - Repeated links to a subdir index file are not re-added
  [Sitemap] # Subtest: Entry fallback sorts case-insensitively
  [Sitemap]     ok 1 - apple.html precedes Zebra.html (byte-sort would pick Zebra)
  [Sitemap]     1..1
  [Sitemap] ok 34 - Entry fallback sorts case-insensitively
  [Sitemap] # Subtest: No-index root: clean root URL + sibling pages discovered
  [Sitemap]     ok 1 - Root "/" URL added exactly once
  [Sitemap]     ok 2 - Root URL is not the literal "/./" form
  [Sitemap]     ok 3 - Root pages the fallback entry does not link to are still discovered
  [Sitemap]     ok 4 - parallel: sibling page discovered
  [Sitemap]     ok 5 - parallel: no duplicate URLs
  [Sitemap]     1..5
  [Sitemap] ok 35 - No-index root: clean root URL + sibling pages discovered
  [Sitemap] # Subtest: Root-relative "/" from a subdir resolves to the root, not the subdir
  [Sitemap]     ok 1 - Root URL present exactly once
  [Sitemap]     ok 2 - Linking page discovered
  [Sitemap]     ok 3 - href="/" from a subdir page does not resolve to the subdir itself
  [Sitemap]     1..3
  [Sitemap] ok 36 - Root-relative "/" from a subdir resolves to the root, not the subdir
  [Sitemap] # Subtest: Root index expansion discovers unlinked root pages
  [Sitemap]     ok 1 - Root URL present
  [Sitemap]     ok 2 - Root pages not linked from index.html are discovered (like subdir siblings)
  [Sitemap]     ok 3 - No duplicate URLs
  [Sitemap]     1..3
  [Sitemap] ok 37 - Root index expansion discovers unlinked root pages
  [Sitemap] # Subtest: urls-found and on-done report the scan results
  [Sitemap]     ok 1 - urls-found matches builder item count
  [Sitemap]     ok 2 - on-done received the discovered items
  [Sitemap]     1..2
  [Sitemap] ok 38 - urls-found and on-done report the scan results
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/10-jsonld.rakutest
  [Sitemap] 1..42
  [Sitemap] # Subtest: extract-jsonld — single block
  [Sitemap]     ok 1 - One object extracted
  [Sitemap]     ok 2 - Headline correct
  [Sitemap]     1..2
  [Sitemap] ok 1 - extract-jsonld — single block
  [Sitemap] # Subtest: extract-jsonld — multiple blocks
  [Sitemap]     ok 1 - Two objects extracted
  [Sitemap]     ok 2 - First headline correct
  [Sitemap]     ok 3 - Second name correct
  [Sitemap]     1..3
  [Sitemap] ok 2 - extract-jsonld — multiple blocks
  [Sitemap] # Subtest: extract-jsonld — array body
  [Sitemap]     ok 1 - Two items from array
  [Sitemap]     1..1
  [Sitemap] ok 3 - extract-jsonld — array body
  [Sitemap] # Subtest: extract-jsonld — JS comments stripped
  [Sitemap]     ok 1 - One object despite comments
  [Sitemap]     ok 2 - Headline correct
  [Sitemap]     1..2
  [Sitemap] ok 4 - extract-jsonld — JS comments stripped
  [Sitemap] # Subtest: extract-jsonld — HTML comment wrapper stripped
  [Sitemap]     ok 1 - One object extracted
  [Sitemap]     1..1
  [Sitemap] ok 5 - extract-jsonld — HTML comment wrapper stripped
  [Sitemap] # Subtest: extract-jsonld — malformed JSON returns empty
  [Sitemap]     ok 1 - Malformed JSON returns empty list
  [Sitemap]     1..1
  [Sitemap] ok 6 - extract-jsonld — malformed JSON returns empty
  [Sitemap] # Subtest: find-by-type — exact match
  [Sitemap]     ok 1 - One VideoObject found
  [Sitemap]     ok 2 - Correct item returned
  [Sitemap]     1..2
  [Sitemap] ok 7 - find-by-type — exact match
  [Sitemap] # Subtest: find-by-type — @graph unwraps
  [Sitemap]     ok 1 - VideoObject found inside @graph
  [Sitemap]     ok 2 - Correct item from @graph
  [Sitemap]     1..2
  [Sitemap] ok 8 - find-by-type — @graph unwraps
  [Sitemap] # Subtest: find-by-type — no match
  [Sitemap]     ok 1 - No match returns empty list
  [Sitemap]     1..1
  [Sitemap] ok 9 - find-by-type — no match
  [Sitemap] # Subtest: find-by-type — generic Article does NOT match NewsArticle
  [Sitemap]     ok 1 - Article type does not match NewsArticle
  [Sitemap]     ok 2 - Article does not match ReportageNewsArticle
  [Sitemap]     1..2
  [Sitemap] ok 10 - find-by-type — generic Article does NOT match NewsArticle
  [Sitemap] # Subtest: find-by-type — BlogPosting does NOT match news types
  [Sitemap]     ok 1 - BlogPosting does not match NewsArticle
  [Sitemap]     ok 2 - BlogPosting does not match ReportageNewsArticle
  [Sitemap]     1..2
  [Sitemap] ok 11 - find-by-type — BlogPosting does NOT match news types
  [Sitemap] # Subtest: find-by-type — schema.org URL prefixes match
  [Sitemap]     ok 1 - https://schema.org/NewsArticle matches NewsArticle
  [Sitemap]     ok 2 - http://schema.org/NewsArticle matches NewsArticle
  [Sitemap]     ok 3 - schema:NewsArticle matches NewsArticle
  [Sitemap]     1..3
  [Sitemap] ok 12 - find-by-type — schema.org URL prefixes match
  [Sitemap] # Subtest: extract-video-objects — all fields mapped
  [Sitemap]     ok 1 - One video extracted
  [Sitemap]     ok 2 - contentUrl mapped
  [Sitemap]     ok 3 - thumbnailUrl mapped
  [Sitemap]     ok 4 - name mapped to title
  [Sitemap]     ok 5 - description mapped
  [Sitemap]     ok 6 - duration PT1H2M3S = 3723s
  [Sitemap]     ok 7 - uploadDate mapped
  [Sitemap]     1..7
  [Sitemap] ok 13 - extract-video-objects — all fields mapped
  [Sitemap] # Subtest: extract-video-objects — url fallback
  [Sitemap]     ok 1 - Video found via url fallback
  [Sitemap]     ok 2 - url used as contentUrl
  [Sitemap]     1..2
  [Sitemap] ok 14 - extract-video-objects — url fallback
  [Sitemap] # Subtest: extract-video-objects — ImageObject thumbnail
  [Sitemap]     ok 1 - ImageObject.url extracted
  [Sitemap]     1..1
  [Sitemap] ok 15 - extract-video-objects — ImageObject thumbnail
  [Sitemap] # Subtest: extract-video-objects — missing url skipped
  [Sitemap]     ok 1 - Video without contentUrl or url skipped
  [Sitemap]     1..1
  [Sitemap] ok 16 - extract-video-objects — missing url skipped
  [Sitemap] # Subtest: extract-news-objects — basic NewsArticle
  [Sitemap]     ok 1 - One news item extracted
  [Sitemap]     ok 2 - Publication name correct
  [Sitemap]     ok 3 - Language correct
  [Sitemap]     ok 4 - Headline mapped to title
  [Sitemap]     ok 5 - Publication date is DateTime
  [Sitemap]     ok 6 - Fresh article not stale
  [Sitemap]     1..6
  [Sitemap] ok 17 - extract-news-objects — basic NewsArticle
  [Sitemap] # Subtest: extract-news-objects — named subtypes match
  [Sitemap]     ok 1 - ReportageNewsArticle matches news extraction
  [Sitemap]     ok 2 - OpinionNewsArticle matches news extraction
  [Sitemap]     ok 3 - ReviewNewsArticle matches news extraction
  [Sitemap]     ok 4 - AnalysisNewsArticle matches news extraction
  [Sitemap]     ok 5 - BackgroundNewsArticle matches news extraction
  [Sitemap]     1..5
  [Sitemap] ok 18 - extract-news-objects — named subtypes match
  [Sitemap] # Subtest: extract-news-objects — stale detection
  [Sitemap]     ok 1 - Old article still returned
  [Sitemap]     ok 2 - Old article marked stale
  [Sitemap]     1..2
  [Sitemap] ok 19 - extract-news-objects — stale detection
  [Sitemap] # Subtest: extract-news-objects — missing publisher skipped
  [Sitemap]     ok 1 - Article without publisher skipped
  [Sitemap]     1..1
  [Sitemap] ok 20 - extract-news-objects — missing publisher skipped
  [Sitemap] # Subtest: extract-news-objects — missing headline skipped
  [Sitemap]     ok 1 - Article without headline skipped
  [Sitemap]     1..1
  [Sitemap] ok 21 - extract-news-objects — missing headline skipped
  [Sitemap] # Subtest: extract-news-objects — invalid date skipped
  [Sitemap]     ok 1 - Article with invalid date skipped
  [Sitemap]     1..1
  [Sitemap] ok 22 - extract-news-objects — invalid date skipped
  [Sitemap] # Subtest: extract-news-objects — generic Article does NOT match
  [Sitemap]     ok 1 - Generic Article not extracted as news
  [Sitemap]     1..1
  [Sitemap] ok 23 - extract-news-objects — generic Article does NOT match
  [Sitemap] # Subtest: extract-news-objects — BlogPosting does NOT match
  [Sitemap]     ok 1 - BlogPosting not extracted as news
  [Sitemap]     1..1
  [Sitemap] ok 24 - extract-news-objects — BlogPosting does NOT match
  [Sitemap] # Subtest: parse-iso8601-duration — edge cases
  [Sitemap]     ok 1 - PT1H2M3S = 3723s
  [Sitemap]     ok 2 - PT30S = 30s
  [Sitemap]     ok 3 - PT0S = 0s
  [Sitemap]     ok 4 - P0D = 0s
  [Sitemap]     ok 5 - PT bare = 0s
  [Sitemap]     ok 6 - P7D = 604800s
  [Sitemap]     ok 7 - P1W = 604800s
  [Sitemap]     ok 8 - P2W = 1209600s
  [Sitemap]     ok 9 - P3W4D = 3 weeks + 4 days
  [Sitemap]     ok 10 - Invalid string = 0s
  [Sitemap]     ok 11 - PT1.5H = 5400s (fractional hours)
  [Sitemap]     ok 12 - PT0.5M = 30s (fractional minutes)
  [Sitemap]     ok 13 - PT0.5S = 0s (fraction truncated to Int)
  [Sitemap]     ok 14 - P1.5D = 129600s (fractional days)
  [Sitemap]     ok 15 - PT1.5H30M = 7200s (fraction mixed with ints)
  [Sitemap]     ok 16 - PT12.5S = 12s (fraction truncated)
  [Sitemap]     ok 17 - P1.5W = 907200s (fractional weeks)
  [Sitemap]     ok 18 - P1Y rejected: years have no fixed second value
  [Sitemap]     ok 19 - P2M rejected: months have no fixed second value
  [Sitemap]     ok 20 - Y/M in the date part rejected, even with valid time parts
  [Sitemap]     ok 21 - P1Y6M rejected
  [Sitemap]     ok 22 - Minutes in the TIME part still convert
  [Sitemap]     ok 23 - P-1D rejected: durations are non-negative
  [Sitemap]     ok 24 - -P1D rejected: durations are non-negative
  [Sitemap]     ok 25 - PT-1S rejected: durations are non-negative
  [Sitemap]     1..25
  [Sitemap] ok 25 - parse-iso8601-duration — edge cases
  [Sitemap] # Subtest: extract-jsonld — robust script tag matching
  [Sitemap]     ok 1 - Scripts with extra attrs/spacing/case all extracted
  [Sitemap]     ok 2 - Unquoted attribute value matched
  [Sitemap]     ok 3 - Trailing attribute after type matched
  [Sitemap]     1..3
  [Sitemap] ok 26 - extract-jsonld — robust script tag matching
  [Sitemap] # Subtest: find-by-type — deeply nested document
  [Sitemap]     ok 1 - Deeply nested VideoObject found
  [Sitemap]     ok 2 - Deep item content correct
  [Sitemap]     1..2
  [Sitemap] ok 27 - find-by-type — deeply nested document
  [Sitemap] # Subtest: array thumbnailUrl / inLanguage / publisher no longer crash
  [Sitemap]     ok 1 - video extracted from array-bearing object
  [Sitemap]     ok 2 - first array element used for thumbnail
  [Sitemap]     ok 3 - first array element used for title
  [Sitemap]     1..3
  [Sitemap] ok 28 - array thumbnailUrl / inLanguage / publisher no longer crash
  [Sitemap] # Subtest: relative contentUrl/thumbnail resolve against page URL
  [Sitemap]     ok 1 - video extracted
  [Sitemap]     ok 2 - relative contentUrl resolved against page URL
  [Sitemap]     ok 3 - relative thumbnailUrl resolved against page URL
  [Sitemap]     1..3
  [Sitemap] ok 29 - relative contentUrl/thumbnail resolve against page URL
  [Sitemap] # Subtest: coerce-media-url handles Hash elements in arrays
  [Sitemap]     ok 1 - video extracted from Hash-bearing contentUrl array
  [Sitemap]     ok 2 - Hash element contributes its url key
  [Sitemap]     ok 3 - Hash element falls back to contentUrl
  [Sitemap]     1..3
  [Sitemap] ok 30 - coerce-media-url handles Hash elements in arrays
  [Sitemap] # Subtest: empty provided @jsonld list is trusted, not re-parsed
  [Sitemap]     ok 1 - caller-supplied empty parse result is authoritative
  [Sitemap]     ok 2 - omitted @jsonld argument parses the document
  [Sitemap]     1..2
  [Sitemap] ok 31 - empty provided @jsonld list is trusted, not re-parsed
  [Sitemap] # Subtest: video seen-check runs on resolved URLs
  [Sitemap]     ok 1 - relative JSON-LD twin deduped after resolution
  [Sitemap]     ok 2 - the surviving video is the resolved URL
  [Sitemap]     1..2
  [Sitemap] ok 32 - video seen-check runs on resolved URLs
  [Sitemap] # Subtest: extract-jsonld ignores data-type attribute (not a type attribute)
  [Sitemap]     ok 1 - data-type="application/ld+json" is not treated as JSON-LD
  [Sitemap]     ok 2 - type="application/ld+json" is still extracted correctly
  [Sitemap]     1..2
  [Sitemap] ok 33 - extract-jsonld ignores data-type attribute (not a type attribute)
  [Sitemap] # Subtest: bare-number duration counts as seconds
  [Sitemap]     ok 1 - JSON number 90 parses as 90 seconds (not 0)
  [Sitemap]     ok 2 - string "90" parses as 90 seconds
  [Sitemap]     ok 3 - ISO-8601 duration still parses
  [Sitemap]     ok 4 - signed durations still rejected
  [Sitemap]     1..4
  [Sitemap] ok 34 - bare-number duration counts as seconds
  [Sitemap] # Subtest: same @id via @graph and top level dedupes
  [Sitemap]     ok 1 - one record for a shared @id (top-level + @graph)
  [Sitemap]     ok 2 - URL correct
  [Sitemap]     1..2
  [Sitemap] ok 35 - same @id via @graph and top level dedupes
  [Sitemap] # Subtest: nested MediaObject URL merges into the wrapper record
  [Sitemap]     ok 1 - nested media twin does not double-publish the video
  [Sitemap]     ok 2 - nested MediaObject URL wins
  [Sitemap]     ok 3 - outer name merged into the record
  [Sitemap]     ok 4 - outer thumbnail merged
  [Sitemap]     ok 5 - outer uploadDate merged
  [Sitemap]     ok 6 - identical nested URL collapses to one record
  [Sitemap]     1..6
  [Sitemap] ok 36 - nested MediaObject URL merges into the wrapper record
  [Sitemap] # Subtest: @id-less VideoObjects with the same URL dedupe
  [Sitemap]     ok 1 - two @id-less objects with the same URL collapse to one
  [Sitemap]     ok 2 - URL correct
  [Sitemap]     1..2
  [Sitemap] ok 37 - @id-less VideoObjects with the same URL dedupe
  [Sitemap] # Subtest: extract-videos-for-item wires JSON-LD uploadDate into publication-date
  [Sitemap]     ok 1 - one video extracted from the page
  [Sitemap]     ok 2 - content-loc set
  [Sitemap]     ok 3 - JSON-LD uploadDate wired into publication-date
  [Sitemap]     1..3
  [Sitemap] ok 38 - extract-videos-for-item wires JSON-LD uploadDate into publication-date
  [Sitemap] # Subtest: </script> inside a JSON string does not truncate the block
  [Sitemap]     ok 1 - block extracted despite literal </script> in a string
  [Sitemap]     ok 2 - full string content preserved
  [Sitemap]     ok 3 - news object parsed from the full block
  [Sitemap]     1..3
  [Sitemap] ok 39 - </script> inside a JSON string does not truncate the block
  [Sitemap] # Subtest: inline // comments stripped, protocol-relative URLs preserved
  [Sitemap]     ok 1 - object parsed despite inline // comment
  [Sitemap]     ok 2 - protocol-relative URL inside a string is not treated as a comment
  [Sitemap]     1..2
  [Sitemap] ok 40 - inline // comments stripped, protocol-relative URLs preserved
  [Sitemap] # Subtest: nested url array in an ImageObject is reduced to a single URL
  [Sitemap]     ok 1 - video extracted
  [Sitemap]     ok 2 - nested url array reduced to a single URL (first element)
  [Sitemap]     1..2
  [Sitemap] ok 41 - nested url array in an ImageObject is reduced to a single URL
  [Sitemap] # Subtest: extract-page-assets max-videos caps videos per page
  [Sitemap]     ok 1 - default max-videos caps 120 videos at 100
  [Sitemap]     ok 2 - :max-videos(50) caps videos at 50
  [Sitemap]     1..2
  [Sitemap] ok 42 - extract-page-assets max-videos caps videos per page
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/11-news-sitemap.rakutest
  [Sitemap] 1..9
  [Sitemap] # Subtest: DirScanner extracts news via --news
  [Sitemap]     ok 1 - News builder returned
  [Sitemap]     ok 2 - One news item in builder
  [Sitemap]     ok 3 - Publication correct
  [Sitemap]     ok 4 - Title correct
  [Sitemap]     1..4
  [Sitemap] ok 1 - DirScanner extracts news via --news
  [Sitemap] # Subtest: News builder gets correct items with full fields
  [Sitemap]     ok 1 - One news item
  [Sitemap]     ok 2 - Language correct
  [Sitemap]     ok 3 - Date is DateTime
  [Sitemap]     1..3
  [Sitemap] ok 2 - News builder gets correct items with full fields
  [Sitemap] # Subtest: Stale articles filtered out
  [Sitemap]     ok 1 - Stale article filtered
  [Sitemap]     1..1
  [Sitemap] ok 3 - Stale articles filtered out
  [Sitemap] # Subtest: No news when flag off
  [Sitemap]     ok 1 - News builder is Nil without flag
  [Sitemap]     1..1
  [Sitemap] ok 4 - No news when flag off
  [Sitemap] # Subtest: Multiple news articles on one page via @graph
  [Sitemap]     ok 1 - One page with news
  [Sitemap]     ok 2 - Two news items on page
  [Sitemap]     1..2
  [Sitemap] ok 5 - Multiple news articles on one page via @graph
  [Sitemap] # Subtest: Mixed fresh and stale on same page
  [Sitemap]     ok 1 - One page with news
  [Sitemap]     ok 2 - Only fresh article kept
  [Sitemap]     ok 3 - Fresh article preserved
  [Sitemap]     1..3
  [Sitemap] ok 6 - Mixed fresh and stale on same page
  [Sitemap] # Subtest: News sitemap XML output structure
  [Sitemap]     ok 1 - News sitemap file written
  [Sitemap]     ok 2 - Contains news:news tag
  [Sitemap]     ok 3 - Contains publication name
  [Sitemap]     ok 4 - Contains news title
  [Sitemap]     1..4
  [Sitemap] ok 7 - News sitemap XML output structure
  [Sitemap] # Subtest: @graph NewsArticle is found
  [Sitemap]     ok 1 - NewsArticle inside @graph found
  [Sitemap]     ok 2 - Title correct
  [Sitemap]     1..2
  [Sitemap] ok 8 - @graph NewsArticle is found
  [Sitemap] # Subtest: ReportageNewsArticle works end-to-end
  [Sitemap]     ok 1 - ReportageNewsArticle extracted
  [Sitemap]     ok 2 - Title correct
  [Sitemap]     ok 3 - Publication correct
  [Sitemap]     1..3
  [Sitemap] ok 9 - ReportageNewsArticle works end-to-end
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/12-site-tree.rakutest
  [Sitemap] 1..23
  [Sitemap] # Subtest: basic creation
  [Sitemap]     ok 1 - root stub is empty
  [Sitemap]     ok 2 - root depth is 0
  [Sitemap]     ok 3 - root segments is empty
  [Sitemap]     ok 4 - root full-url
  [Sitemap]     1..4
  [Sitemap] ok 1 - basic creation
  [Sitemap] # Subtest: add-child
  [Sitemap]     ok 1 - child stub
  [Sitemap]     ok 2 - child parent is root
  [Sitemap]     ok 3 - root depth unchanged
  [Sitemap]     ok 4 - child depth 1
  [Sitemap]     ok 5 - child segments
  [Sitemap]     ok 6 - child full-url
  [Sitemap]     1..6
  [Sitemap] ok 2 - add-child
  [Sitemap] # Subtest: nested children
  [Sitemap]     ok 1 - nested depth 2
  [Sitemap]     ok 2 - nested segments
  [Sitemap]     ok 3 - nested full-url
  [Sitemap]     1..3
  [Sitemap] ok 3 - nested children
  [Sitemap] # Subtest: segments handles the root empty list
  [Sitemap]     ok 1 - root segments is empty
  [Sitemap]     ok 2 - segments returns a List (empty root list is cached, not re-walked)
  [Sitemap]     1..2
  [Sitemap] ok 4 - segments handles the root empty list
  [Sitemap] # Subtest: tree visualization
  [Sitemap]     ok 1 - tree contains blog
  [Sitemap]     ok 2 - tree has bullet points
  [Sitemap]     1..2
  [Sitemap] ok 5 - tree visualization
  [Sitemap] # Subtest: flatten
  [Sitemap]     ok 1 - flatten includes root, blog, post1, post2
  [Sitemap]     ok 2 - first is root
  [Sitemap]     ok 3 - second is blog
  [Sitemap]     1..3
  [Sitemap] ok 6 - flatten
  [Sitemap] # Subtest: to-builder
  [Sitemap]     ok 1 - builder has 3 items (root + 2 children)
  [Sitemap]     ok 2 - xml contains page1
  [Sitemap]     ok 3 - xml contains page2
  [Sitemap]     1..3
  [Sitemap] ok 7 - to-builder
  [Sitemap] # Subtest: changefreq coercion
  [Sitemap]     ok 1 - lowercase Str coerced to enum
  [Sitemap]     ok 2 - mixed-case Str coerced to enum
  [Sitemap]     ok 3 - enum passes through unchanged
  [Sitemap]     ok 4 - invalid changefreq dropped
  [Sitemap]     1..4
  [Sitemap] ok 8 - changefreq coercion
  [Sitemap] # Subtest: to-builder forwards all item fields
  [Sitemap]     ok 1 - title forwarded
  [Sitemap]     ok 2 - expires forwarded
  [Sitemap]     ok 3 - changefreq forwarded
  [Sitemap]     1..3
  [Sitemap] ok 9 - to-builder forwards all item fields
  [Sitemap] # Subtest: to-builder emits the falsy always changefreq
  [Sitemap]     ok 1 - always changefreq forwarded through to-builder
  [Sitemap]     ok 2 - always changefreq rendered
  [Sitemap]     1..2
  [Sitemap] ok 10 - to-builder emits the falsy always changefreq
  [Sitemap] # Subtest: to-builder forwards android/amp links
  [Sitemap]     ok 1 - android-link forwarded
  [Sitemap]     ok 2 - amp-link forwarded
  [Sitemap]     ok 3 - Renders android:link
  [Sitemap]     ok 4 - Renders amp:link
  [Sitemap]     1..4
  [Sitemap] ok 11 - to-builder forwards android/amp links
  [Sitemap] # Subtest: wire-parents
  [Sitemap]     ok 1 - blog parent is home
  [Sitemap]     ok 2 - post parent is blog
  [Sitemap]     ok 3 - home has 1 child
  [Sitemap]     ok 4 - blog has 1 child
  [Sitemap]     1..4
  [Sitemap] ok 12 - wire-parents
  [Sitemap] # Subtest: duplicate stub detection
  [Sitemap]     ok 1 - dies on duplicate
  [Sitemap]     1..1
  [Sitemap] ok 13 - duplicate stub detection
  [Sitemap] # Subtest: add-child stub is URL-safe
  [Sitemap]     ok 1 - stub '' rejected
  [Sitemap]     ok 2 - stub '/' rejected
  [Sitemap]     ok 3 - stub '..' rejected
  [Sitemap]     ok 4 - stub 'a/b' rejected
  [Sitemap]     ok 5 - stub 'a b' rejected
  [Sitemap]     ok 6 - stub 'a?b' rejected
  [Sitemap]     ok 7 - stub 'a \#b' rejected
  [Sitemap]     ok 8 - stub 'a..b' rejected
  [Sitemap]     ok 9 - stub 'a:b' rejected
  [Sitemap]     ok 10 - stub '.' rejected
  [Sitemap]     ok 11 - stub 'a;b' rejected
  [Sitemap]     ok 12 - stub 'a	b' rejected
  [Sitemap]     ok 13 - valid stub bound
  [Sitemap]     ok 14 - dots/underscores allowed
  [Sitemap]     ok 15 - leading dash allowed
  [Sitemap]     ok 16 - only valid child attached
  [Sitemap]     1..16
  [Sitemap] ok 14 - add-child stub is URL-safe
  [Sitemap] # Subtest: wire-parents missing parent
  [Sitemap]     ok 1 - dies on missing parent
  [Sitemap]     1..1
  [Sitemap] ok 15 - wire-parents missing parent
  [Sitemap] # Subtest: cycle detection in wire-parents
  [Sitemap]     ok 1 - mutual parent-stub references die
  [Sitemap]     1..1
  [Sitemap] ok 16 - cycle detection in wire-parents
  [Sitemap] # Subtest: cycle detection in attach-child
  [Sitemap]     ok 1 - attaching an ancestor as its own descendant dies
  [Sitemap]     1..1
  [Sitemap] ok 17 - cycle detection in attach-child
  [Sitemap] # Subtest: attach-child reparents: child leaves its previous parent
  [Sitemap]     ok 1 - child starts under branch
  [Sitemap]     ok 2 - root does not list child
  [Sitemap]     ok 3 - child moved to root
  [Sitemap]     ok 4 - branch no longer lists child
  [Sitemap]     ok 5 - root lists child exactly once
  [Sitemap]     ok 6 - root lists the same child object
  [Sitemap]     1..6
  [Sitemap] ok 18 - attach-child reparents: child leaves its previous parent
  [Sitemap] # Subtest: to-hash serializes the live parent, not a stale parent-stub
  [Sitemap]     ok 1 - live parent is new
  [Sitemap]     ok 2 - to-hash prefers the live parent over the stale stub
  [Sitemap]     ok 3 - round-trip parent-stub matches the live parent
  [Sitemap]     ok 4 - unattached node keeps its parent-stub
  [Sitemap]     1..4
  [Sitemap] ok 19 - to-hash serializes the live parent, not a stale parent-stub
  [Sitemap] # Subtest: from-hash stays linear for deep chains
  [Sitemap]     ok 1 - from-hash rebuilt a 15000-node chain in 0.74s (<15s)
  [Sitemap]     ok 2 - Deepest node reachable by walking the chain
  [Sitemap]     ok 3 - Deepest node depth correct after the rebuild
  [Sitemap]     ok 4 - Deepest node segments cover the chain below the root
  [Sitemap]     1..4
  [Sitemap] ok 20 - from-hash stays linear for deep chains
  [Sitemap] # Subtest: reparent invalidates cached depth/segments of an uncached ancestor
  [Sitemap]     ok 1 - grandchild depth cached at 3
  [Sitemap]     ok 2 - grandchild segments cached
  [Sitemap]     ok 3 - grandchild depth recomputed after reparenting its uncached ancestor
  [Sitemap]     ok 4 - grandchild segments recomputed after reparenting its uncached ancestor
  [Sitemap]     ok 5 - reparented ancestor depth updated
  [Sitemap]     ok 6 - reparented ancestor segments updated
  [Sitemap]     1..6
  [Sitemap] ok 21 - reparent invalidates cached depth/segments of an uncached ancestor
  [Sitemap] # Subtest: to-builder auto-priority uses the shared depth formula
  [Sitemap]     ok 1 - depth 0 (root) auto-priority 1.0
  [Sitemap]     ok 2 - depth 1 auto-priority 0.8
  [Sitemap]     ok 3 - depth 2 auto-priority 0.6
  [Sitemap]     ok 4 - depth 3 auto-priority 0.4
  [Sitemap]     ok 5 - depth 4 auto-priority 0.2 (not clamped at 0.4)
  [Sitemap]     ok 6 - depth 5+ auto-priority floors at 0.1
  [Sitemap]     1..6
  [Sitemap] ok 22 - to-builder auto-priority uses the shared depth formula
  [Sitemap] # Subtest: add-child builds a deep chain in linear time (A10)
  [Sitemap]     ok 1 - 5000-deep add-child chain built in 0.42s (<30s)
  [Sitemap]     ok 2 - deepest leaf depth correct
  [Sitemap]     ok 3 - deepest leaf segments cover the whole chain
  [Sitemap]     ok 4 - innermost segment is the chain tail
  [Sitemap]     ok 5 - outermost segment is the chain head
  [Sitemap]     ok 6 - full-url still produces a string for the rebuilt tree
  [Sitemap]     1..6
  [Sitemap] ok 23 - add-child builds a deep chain in linear time (A10)
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/13-site-tree-yaml.rakutest
  [Sitemap] 1..9
  [Sitemap] # Subtest: Image roundtrip
  [Sitemap]     ok 1 - url
  [Sitemap]     ok 2 - caption
  [Sitemap]     ok 3 - title defaults to empty
  [Sitemap]     ok 4 - geo-location defaults
  [Sitemap]     1..4
  [Sitemap] ok 1 - Image roundtrip
  [Sitemap] # Subtest: Video roundtrip
  [Sitemap]     ok 1 - thumbnail-loc
  [Sitemap]     ok 2 - title
  [Sitemap]     ok 3 - content-loc
  [Sitemap]     ok 4 - duration
  [Sitemap]     ok 5 - tags
  [Sitemap]     ok 6 - description defaults to empty
  [Sitemap]     ok 7 - family-friendly tri-state: unspecified stays unset
  [Sitemap]     1..7
  [Sitemap] ok 2 - Video roundtrip
  [Sitemap] # Subtest: Link roundtrip
  [Sitemap]     ok 1 - lang
  [Sitemap]     ok 2 - url
  [Sitemap]     1..2
  [Sitemap] ok 3 - Link roundtrip
  [Sitemap] # Subtest: News roundtrip
  [Sitemap]     ok 1 - publication
  [Sitemap]     ok 2 - title
  [Sitemap]     ok 3 - publication-date
  [Sitemap]     ok 4 - keywords
  [Sitemap]     ok 5 - stock-tickers defaults to empty
  [Sitemap]     1..5
  [Sitemap] ok 4 - News roundtrip
  [Sitemap] # Subtest: News edge cases
  [Sitemap]     ok 1 - News without publication-date constructs
  [Sitemap]     ok 2 - publication-date stays undefined
  [Sitemap]     ok 3 - DateTime instance survives from-hash
  [Sitemap]     ok 4 - ISO string parsed by from-hash
  [Sitemap]     1..4
  [Sitemap] ok 5 - News edge cases
  [Sitemap] # Subtest: Item roundtrip
  [Sitemap]     ok 1 - url
  [Sitemap]     ok 2 - lastmod
  [Sitemap]     ok 3 - changefreq
  [Sitemap]     ok 4 - priority
  [Sitemap]     ok 5 - title
  [Sitemap]     ok 6 - images count
  [Sitemap]     ok 7 - videos count
  [Sitemap]     ok 8 - links count
  [Sitemap]     ok 9 - news count
  [Sitemap]     ok 10 - image caption preserved
  [Sitemap]     ok 11 - link lang preserved
  [Sitemap]     1..11
  [Sitemap] ok 6 - Item roundtrip
  [Sitemap] # Subtest: SiteTree roundtrip
  [Sitemap]     ok 1 - root stub
  [Sitemap]     ok 2 - root depth
  [Sitemap]     ok 3 - root has 2 children
  [Sitemap]     ok 4 - 5 nodes total (root + blog + 2 posts + about)
  [Sitemap]     ok 5 - blog stub
  [Sitemap]     ok 6 - blog depth
  [Sitemap]     ok 7 - blog has item
  [Sitemap]     ok 8 - blog changefreq
  [Sitemap]     ok 9 - blog priority
  [Sitemap]     ok 10 - first-post stub
  [Sitemap]     ok 11 - first-post depth
  [Sitemap]     ok 12 - first-post url
  [Sitemap]     ok 13 - second-post stub
  [Sitemap]     ok 14 - second-post priority
  [Sitemap]     ok 15 - about stub
  [Sitemap]     ok 16 - about depth
  [Sitemap]     1..16
  [Sitemap] ok 7 - SiteTree roundtrip
  [Sitemap] # Subtest: YAML roundtrip
  [Sitemap]     ok 1 - yaml contains blog
  [Sitemap]     ok 2 - yaml contains first-post
  [Sitemap]     ok 3 - yaml contains priority
  [Sitemap]     ok 4 - 1 child after from-yaml
  [Sitemap]     ok 5 - blog stub after roundtrip
  [Sitemap]     ok 6 - first-post stub after roundtrip
  [Sitemap]     ok 7 - second serialization matches first
  [Sitemap]     1..7
  [Sitemap] ok 8 - YAML roundtrip
  [Sitemap] # Subtest: Edge cases
  [Sitemap]     ok 1 - deep nesting preserves all 6 nodes
  [Sitemap]     ok 2 - deepest node has depth 5
  [Sitemap]     ok 3 - deepest stub preserved
  [Sitemap]     ok 4 - simple stub preserved
  [Sitemap]     ok 5 - no item when none was set
  [Sitemap]     ok 6 - from-hash tolerates missing parent-stub
  [Sitemap]     ok 7 - parent-stub stays undefined
  [Sitemap]     ok 8 - empty item hash stays a defined item
  [Sitemap]     ok 9 - empty item round-trips with default fields
  [Sitemap]     1..9
  [Sitemap] ok 9 - Edge cases
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/14-cli.rakutest
  [Sitemap] 1..35
  [Sitemap] ok 1 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 2 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 3 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 4 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 5 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 6 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 7 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 8 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 9 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 10 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 11 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 12 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 13 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 14 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 15 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 16 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 17 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 18 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 19 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 20 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 21 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 22 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 23 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 24 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 25 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 26 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 27 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 28 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 29 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 30 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 31 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 32 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 33 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 34 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] ok 35 - # SKIP CLI subtests skipped (slow: 41 subprocess spawns + HTTP servers); set SITEMAP_SLOW_TESTS=1 to run
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/15-fetcher.rakutest
  [Sitemap] 1..25
  [Sitemap] # Subtest: fetch-recursive dedups concurrent child writes
  [Sitemap]     ok 1 - Two children saved for duplicate locs
  [Sitemap]     ok 2 - Children paths are distinct
  [Sitemap]     ok 3 - Child file exists: test-index/child-0.xml
  [Sitemap]     ok 4 - Child file has content: test-index/child-0.xml
  [Sitemap]     ok 5 - Child file exists: test-index/child.xml
  [Sitemap]     ok 6 - Child file has content: test-index/child.xml
  [Sitemap]     1..6
  [Sitemap] ok 1 - fetch-recursive dedups concurrent child writes
  [Sitemap] # Subtest: fetch-recursive keeps distinct files for distinct URLs mapping to the same name
  [Sitemap]     ok 1 - Both colliding children saved
  [Sitemap]     ok 2 - Distinct files assigned to colliding names
  [Sitemap]     ok 3 - First child keeps the plain name
  [Sitemap]     ok 4 - Second child gets a suffixed name starting at -0
  [Sitemap]     ok 5 - Child file exists: test-index2/child.xml
  [Sitemap]     ok 6 - Child file has content: test-index2/child.xml
  [Sitemap]     ok 7 - Child file exists: test-index2/child-0.xml
  [Sitemap]     ok 8 - Child file has content: test-index2/child-0.xml
  [Sitemap]     1..8
  [Sitemap] ok 2 - fetch-recursive keeps distinct files for distinct URLs mapping to the same name
  [Sitemap] # Subtest: fetch-recursive rewrites index <loc> to local paths
  [Sitemap]     ok 1 - Saved index no longer points at remote child URLs
  [Sitemap]     ok 2 - Rewritten index has one <loc> per fetched child
  [Sitemap]     ok 3 - Rewritten index <loc> 'test-index3/child.xml' exists on disk
  [Sitemap]     ok 4 - Rewritten index <loc> 'test-index3/child.xml' is a local path, not a URL
  [Sitemap]     ok 5 - Rewritten index <loc> 'test-index3/child-0.xml' exists on disk
  [Sitemap]     ok 6 - Rewritten index <loc> 'test-index3/child-0.xml' is a local path, not a URL
  [Sitemap]     ok 7 - lastmod carried over into the rewritten index
  [Sitemap]     1..7
  [Sitemap] ok 3 - fetch-recursive rewrites index <loc> to local paths
  [Sitemap] # Subtest: fetch-recursive extensionless -o derives index file + child dir
  [Sitemap]     ok 1 - extensionless -o gains the format extension for the index file
  [Sitemap]     ok 2 - child directory derived from the extensionless stem
  [Sitemap]     ok 3 - index file written as noext.xml, not a directory
  [Sitemap]     ok 4 - child written into the noext/ directory
  [Sitemap]     1..4
  [Sitemap] ok 4 - fetch-recursive extensionless -o derives index file + child dir
  [Sitemap] # Subtest: fetch-recursive does not overwrite pre-existing child
  [Sitemap]     ok 1 - Original child file untouched
  [Sitemap]     ok 2 - New child written to distinct file
  [Sitemap]     1..2
  [Sitemap] ok 5 - fetch-recursive does not overwrite pre-existing child
  [Sitemap] # Subtest: fetch-recursive refuses .. in output dir even with --force
  [Sitemap]     ok 1 - fetch-recursive dies on .. output path
  [Sitemap]     ok 2 - victim directory not deleted by --force
  [Sitemap]     1..2
  [Sitemap] ok 6 - fetch-recursive refuses .. in output dir even with --force
  [Sitemap] # Subtest: fetch-recursive refuses an absolute -o outside the current directory, allows one inside
  [Sitemap]     ok 1 - fetch-recursive dies on an absolute -o path outside the current directory
  [Sitemap]     ok 2 - nothing written outside the current directory
  [Sitemap]     ok 3 - no output directory created outside the current directory
  [Sitemap]     ok 4 - recursive absolute -o inside the current directory is accepted
  [Sitemap]     ok 5 - absolute index rewritten with local child path
  [Sitemap]     ok 6 - absolute children directory created inside the current directory
  [Sitemap]     1..6
  [Sitemap] ok 7 - fetch-recursive refuses an absolute -o outside the current directory, allows one inside
  [Sitemap] # Subtest: fetch-recursive refuses -o through an intermediate symlink
  [Sitemap]     # Subtest: fetch-recursive dies when -o resolves outside the current directory
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /'outside the current directory'/
  [Sitemap]     ok 1 - fetch-recursive dies when -o resolves outside the current directory
  [Sitemap]     ok 2 - the symlink target was not deleted
  [Sitemap]     ok 3 - nothing written through the intermediate symlink
  [Sitemap]     1..3
  [Sitemap] ok 8 - fetch-recursive refuses -o through an intermediate symlink
  [Sitemap] # Subtest: fetch-recursive defaults to same-host children with a cap
  [Sitemap]     ok 1 - 127.0.0.2 (foreign-host string) child excluded, same-host children fetched
  [Sitemap]     ok 2 - --follow-foreign-children fetches 127.0.0.2 child too
  [Sitemap]     ok 3 - max-children caps the number of fetched children
  [Sitemap]     1..3
  [Sitemap] ok 9 - fetch-recursive defaults to same-host children with a cap
  [Sitemap] # Subtest: fetch-recursive skips non-XML leaf responses
  [Sitemap]     ok 1 - HTML leaf skipped, only XML child saved
  [Sitemap]     1..1
  [Sitemap] ok 10 - fetch-recursive skips non-XML leaf responses
  [Sitemap] # Subtest: is-sitemap-index anchors detection to the root
  [Sitemap]     ok 1 - real index detected
  [Sitemap]     ok 2 - plain urlset is not an index
  [Sitemap]     ok 3 - sitemapindex inside a comment is not an index
  [Sitemap]     ok 4 - HTML mentioning sitemapindex is not an index
  [Sitemap]     ok 5 - BOM + xml-decl index detected
  [Sitemap]     ok 6 - urlset with a sitemapindex comment saved as a leaf, not an index
  [Sitemap]     ok 7 - leaf file written
  [Sitemap]     ok 8 - leaf content preserved
  [Sitemap]     1..8
  [Sitemap] ok 11 - is-sitemap-index anchors detection to the root
  [Sitemap] # Subtest: fetch-recursive --force handles short dir names and file-blocked out-dirs
  [Sitemap]     ok 1 - stale file removed from short-named out-dir
  [Sitemap]     ok 2 - child written into short-named out-dir
  [Sitemap]     ok 3 - regular file removed and replaced with out-dir
  [Sitemap]     ok 4 - child written into new out-dir
  [Sitemap]     # Subtest: fetch-recursive dies when out-dir is an existing file without --force
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / existing ' ' file /
  [Sitemap]     ok 5 - fetch-recursive dies when out-dir is an existing file without --force
  [Sitemap]     ok 6 - blocking file untouched
  [Sitemap]     1..6
  [Sitemap] ok 12 - fetch-recursive --force handles short dir names and file-blocked out-dirs
  [Sitemap] # Subtest: fetch-recursive --force removes nested stale directories
  [Sitemap]     ok 1 - new child written into the replaced out-dir
  [Sitemap]     ok 2 - stale top-level file removed
  [Sitemap]     ok 3 - nested stale directory removed
  [Sitemap]     ok 4 - deeply nested stale directory removed
  [Sitemap]     ok 5 - stale file in deepest subtree removed
  [Sitemap]     ok 6 - only the new child remains in the out-dir
  [Sitemap]     1..6
  [Sitemap] ok 13 - fetch-recursive --force removes nested stale directories
  [Sitemap] # Subtest: discover-sitemap normalizes schemeless domains
  [Sitemap]     ok 1 - explicit http scheme discovery reads robots.txt
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap] Malformed request line
  [Sitemap]   in sub bad-request at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 163
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 71
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::HTTP_zef:cro_0.8.13_0/sources/0BD8971A468105F8FED70471BA5482D8565FA726 (Cro::HTTP::RequestParser) line 54
  [Sitemap]   in block  at /home/coke/sandbox/blin/installed/Cro::Core_zef:cro_0.8.10_0/sources/BECCB970FB76D53C78A87E43F9B9AD8A59D8A0A3 (Cro::TCP) line 54
  [Sitemap]     ok 2 - schemeless domain normalized to https:// in fallback message
  [Sitemap]     1..2
  [Sitemap] ok 14 - discover-sitemap normalizes schemeless domains
  [Sitemap] # Subtest: output-filename strips query/fragment via URI parsing
  [Sitemap]     ok 1 - query string does not leak into the filename
  [Sitemap]     ok 2 - fragment does not leak into the filename
  [Sitemap]     ok 3 - gz + query handled, path context preserved
  [Sitemap]     ok 4 - host-only URL derives stem from the host
  [Sitemap]     ok 5 - query stripped across formats
  [Sitemap]     ok 6 - local file behavior unchanged
  [Sitemap]     ok 7 - uppercase scheme still treated as a URL
  [Sitemap]     ok 8 - host stem strips www. prefix and TLD
  [Sitemap]     ok 9 - www. stripped and multi-part TLD (co.uk) stripped
  [Sitemap]     ok 10 - multi-part TLD (com.au) stripped with both labels
  [Sitemap]     ok 11 - multi-part TLD (org.uk) stripped with both labels
  [Sitemap]     1..11
  [Sitemap] ok 15 - output-filename strips query/fragment via URI parsing
  [Sitemap] # Subtest: fetch-recursive resolves relative child locs
  [Sitemap]     ok 1 - Relative child loc resolved against the index URL and fetched
  [Sitemap]     ok 2 - Child file exists
  [Sitemap]     ok 3 - Child file has content
  [Sitemap]     1..3
  [Sitemap] ok 16 - fetch-recursive resolves relative child locs
  [Sitemap] # Subtest: fetch-recursive records failed children
  [Sitemap]     ok 1 - Good child still saved
  [Sitemap]     ok 2 - Failed child recorded in <errors>
  [Sitemap]     ok 3 - Error mentions the HTTP status
  [Sitemap]     1..3
  [Sitemap] ok 17 - fetch-recursive records failed children
  [Sitemap] # Subtest: fetch-recursive fails loudly on an empty top-level body
  [Sitemap]     # Subtest: empty top-level body dies with a clear message
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (Exception)
  [Sitemap]         ok 3 - .message matches / 'empty response body' /
  [Sitemap]     ok 1 - empty top-level body dies with a clear message
  [Sitemap]     1..1
  [Sitemap] ok 18 - fetch-recursive fails loudly on an empty top-level body
  [Sitemap] # Subtest: fetch-recursive records an empty child body as an error
  [Sitemap]     ok 1 - empty child body saved no file
  [Sitemap]     ok 2 - empty child body recorded as an error
  [Sitemap]     ok 3 - error message names the empty body, not a fetch failure
  [Sitemap]     1..3
  [Sitemap] ok 19 - fetch-recursive records an empty child body as an error
  [Sitemap] # Subtest: fetch-recursive skips converted output when nothing was fetched
  [Sitemap] Failed to fetch http://127.0.0.1:20110/index.xml (connection reset by peer)
  [Sitemap]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1/lib/Sitemap/Fetcher.rakumod (Sitemap::Fetcher) line 54
  [Sitemap]   in sub fetch at /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1/lib/Sitemap/Fetcher.rakumod (Sitemap::Fetcher) line 28
  [Sitemap]   in sub fetch-recursive at /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1/lib/Sitemap/Fetcher.rakumod (Sitemap::Fetcher) line 309
  [Sitemap]   in block <unit> at t/15-fetcher.rakutest line 515
  [Sitemap] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/af1773e4378f172b4c420c4738db2912543073e5.tar.gz/Sitemap-0.0.1 t/16-config.rakutest
  [Sitemap] 1..24
  [Sitemap] # Subtest: read-bounded-body rejects an oversized declared Content-Length
  [Sitemap]     # Subtest: Oversized Content-Length rejected before reading
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches rx/declared \s+ body \s+ length/
  [Sitemap]     ok 1 - Oversized Content-Length rejected before reading
  [Sitemap]     ok 2 - Body stream is not tapped for oversized Content-Length
  [Sitemap]     1..2
  [Sitemap] ok 1 - read-bounded-body rejects an oversized declared Content-Length
  [Sitemap] # Subtest: read-bounded-body aborts an over-cap body mid-stream
  [Sitemap]     # Subtest: Over-cap body aborts mid-stream
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /body \s+ exceeds/
  [Sitemap]     ok 1 - Over-cap body aborts mid-stream
  [Sitemap]     ok 2 - cancel() invoked to abort the download
  [Sitemap]     1..2
  [Sitemap] ok 2 - read-bounded-body aborts an over-cap body mid-stream
  [Sitemap] # Subtest: read-bounded-body returns in-range bodies
  [Sitemap]     ok 1 - In-range body assembled from stream chunks
  [Sitemap]     ok 2 - cancel() not called for an in-range body
  [Sitemap]     1..2
  [Sitemap] ok 3 - read-bounded-body returns in-range bodies
  [Sitemap] # Subtest: read-bounded-body ignores an unparseable Content-Length
  [Sitemap]     ok 1 - Unparseable Content-Length falls back to the streaming cap
  [Sitemap]     1..1
  [Sitemap] ok 4 - read-bounded-body ignores an unparseable Content-Length
  [Sitemap] # Subtest: fetch rejects an oversized body via the declared length
  [Sitemap]     # Subtest: fetch() rejects a response with an oversized Content-Length
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches rx/declared \s+ body \s+ length/
  [Sitemap]     ok 1 - fetch() rejects a response with an oversized Content-Length
  [Sitemap]     1..1
  [Sitemap] ok 5 - fetch rejects an oversized body via the declared length
  [Sitemap] # Subtest: read-bounded-body aborts a chunked HTTP body over the cap
  [Sitemap]     ok 1 - Chunked response has no Content-Length
  [Sitemap]     # Subtest: Chunked over-cap body aborts mid-stream over real HTTP
  [Sitemap]         1..3
  [Sitemap]         ok 1 - code dies
  [Sitemap]         ok 2 - right exception type (X::AdHoc)
  [Sitemap]         ok 3 - .message matches /body \s+ exceeds/
  [Sitemap]     ok 2 - Chunked over-cap body aborts mid-stream over real HTTP
  [Sitemap]     1..2
  [Sitemap] ok 6 - read-bounded-body aborts a chunked HTTP body over the cap
  [Sitemap] # Subtest: fetch-robots decompresses a gzip-encoded robots.txt
  [Sitemap]     ok 1 - Actions parsed from gzip-encoded robots.txt
  [Sitemap]     ok 2 - No fetch error on success
  [Sitemap]     ok 3 - Crawl-delay parsed from gzip content
  [Sitemap]     ok 4 - Disallow rule honored
  [Sitemap]     ok 5 - Allowed path unaffected
  [Sitemap]     ok 6 - Sitemap entry parsed from gzip content
  [Sitemap]     1..6
  [Sitemap] ok 7 - fetch-robots decompresses a gzip-encoded robots.txt
  [Sitemap] # Subtest: discover-sitemaps refuses sitemaps on a foreign host (SSRF guard)
  [Sitemap]     ok 1 - same-origin sitemap is kept
  [Sitemap]     ok 2 - scheme-relative sitemap resolves to the same origin and is kept
  [Sitemap]     ok 3 - foreign-host sitemap is refused
  [Sitemap]     1..3
  [Sitemap] ok 8 - discover-sitemaps refuses sitemaps on a foreign host (SSRF guard)
  [Sitemap] # Subtest: fetch-robots rejects an oversized robots.txt
  [Sitemap]     ok 1 - Oversized robots.txt yields no actions (bounded read)
  [Sitemap]     1..1
  [Sitemap] ok 9 - fetch-robots rejects an oversized robots.txt
  [Sitemap] # Subtest: decode-text-body falls back to latin-1 for invalid UTF-8
  [Sitemap]     ok 1 - Valid UTF-8 decoded as-is
  [Sitemap]     ok 2 - Pure ASCII decoded
  [Sitemap]     ok 3 - Invalid UTF-8 byte falls back to latin-1 code point
  [Sitemap]     1..3
  [Sitemap] ok 10 - decode-text-body falls back to latin-1 for invalid UTF-8
  [Sitemap] # Subtest: normalize-origin and same-origin are port-aware
  [Sitemap]     ok 1 - Default port 80 dropped, host lowercased
  [Sitemap]     ok 2 - Default port 443 dropped
  [Sitemap]     ok 3 - Non-default port preserved
  [Sitemap]     ok 4 - Bare hostname has no origin
  [Sitemap]     ok 5 - Default-port variants are the same origin
  [Sitemap]     ok 6 - https default-port variants are the same origin
  [Sitemap]     ok 7 - Different ports are not the same origin
  [Sitemap]     ok 8 - Different schemes are not the same origin
  [Sitemap]     ok 9 - Origin-less URL never matches
  [Sitemap]     1..9
  [Sitemap] ok 11 - normalize-origin and same-origin are port-aware
  [Sitemap] # Subtest: resolve-relative-url resolves relative sitemap locs
  [Sitemap]     ok 1 - Bare relative resolved against base directory
  [Sitemap]     ok 2 - Root-relative resolved against origin
  [Sitemap]     ok 3 - Parent-relative collapses one level
  [Sitemap]     ok 4 - Multi-segment relative path resolved
  [Sitemap]     ok 5 - Dot segment folded away
  [Sitemap]     ok 6 - Resolved against a root-level sitemap
  [Sitemap]     ok 7 - Absolute loc returned unchanged
  [Sitemap]     ok 8 - Scheme-relative loc inherits the scheme
  [Sitemap]     ok 9 - Scheme-relative ref against an empty-scheme context is Nil, not ://x/y
  [Sitemap]     ok 10 - Non-default port preserved
  [Sitemap]     ok 11 - Unparseable base yields Nil (A2) rather than silently echoing the reference
  [Sitemap]     ok 12 - Query-only ref keeps the base path (was /sitemaps/?page=2)
  [Sitemap]     ok 13 - Fragment-only ref keeps the base path (was /sitemaps/ \#top)
  [Sitemap]     ok 14 - Query-only ref replaces the base query
  [Sitemap]     ok 15 - Fragment-only ref keeps the base query
  [Sitemap]     1..15
  [Sitemap] ok 12 - resolve-relative-url resolves relative sitemap locs
  [Sitemap] # Subtest: normalize-start-url guarantees a usable scheme
  [Sitemap]     ok 1 - Bare domain gets https:// prepended
  [Sitemap]     ok 2 - Bare domain with a path keeps the path
  [Sitemap]     ok 3 - Scheme-relative //host becomes https
  [Sitemap]     ok 4 - Explicit http URL unchanged
  [Sitemap]     ok 5 - Explicit https URL unchanged
  [Sitemap]     ok 6 - Uppercase scheme is left alone
  [Sitemap]     1..6
  [Sitemap] ok 13 - normalize-start-url guarantees a usable scheme
  [Sitemap] # Subtest: decompress-content :lenient decodes invalid UTF-8 losslessly
  [Sitemap]     ok 1 - :lenient does not throw on invalid UTF-8
  [Sitemap]     ok 2 - utf8-c8 round-trips the original bytes
  [Sitemap]     ok 3 - Valid UTF-8 still decodes normally without :lenient
  [Sitemap]     1..3
  [Sitemap] ok 14 - decompress-content :lenient decodes invalid UTF-8 losslessly
  [Sitemap] # Subtest: decompress-content decodes every member of a multi-member gzip
  [Sitemap]     ok 1 - All concatenated gzip members decoded, not just the first
  [Sitemap]     ok 2 - A single member still decodes
  [Sitemap]     1..2
  [Sitemap] ok 15 - decompress-content decodes every member of a multi-member gzip
  [Sitemap] # Subtest: canonical-origin and normalize-origin share one implementation
  [Sitemap]     ok 1 - canonical-origin lowercases scheme/host and drops the default port
  [Sitemap]     ok 2 - canonical-origin(URI) and normalize-origin(Str) agree
  [Sitemap]     ok 3 - canonical-origin preserves a non-default port
  [Sitemap]     ok 4 - canonical-origin drops the https default port
  [Sitemap]     ok 5 - canonical-origin yields Nil for a scheme without an http(s) host (A9)
  [Sitemap]     1..5
  [Sitemap] ok 16 - canonical-origin and normalize-origin share one implementation
  [Sitemap] # Subtest: normalize-http-url is the single URL normalizer used by Item
  [Sitemap]     ok 1 - scheme/host lowercased, default port dropped
  [Sitemap]     ok 2 - https default port dropped
  [Sitemap]     ok 3 - non-default port preserved
  [Sitemap]     ok 4 - userinfo survives the default-port strip
  [Sitemap]     ok 5 - IPv6 default port dropped
  [Sitemap]     ok 6 - bare http URL unchanged
  [Sitemap]     ok 7 - non-http scheme returned unchanged
  [Sitemap]     ok 8 - query preserved
  [Sitemap]     ok 9 - Item TWEAK delegates to normalize-http-url
  [Sitemap]     1..9
  [Sitemap] ok 17 - normalize-http-url is the single URL normalizer used by Item
  [Sitemap] # Subtest: cached-client caps the pool with FIFO eviction
  [Sitemap]     ok 1 - oldest client evicted once the pool exceeds the cap
  [Sitemap]     ok 2 - next-oldest evicted in FIFO order
  [Sitemap]     ok 3 - most recent client still pooled
  [Sitemap]     1..3
  [Sitemap] ok 18 - cached-client caps the pool with FIFO eviction
  [Sitemap] # Subtest: detect-input-type: existing files win over URL heuristics
  [Sitemap]     ok 1 - existing dotted path is a file
  [Sitemap]     ok 2 - same path missing is neither (denylisted ext)
  [Sitemap]     ok 3 - bare domain is url
  [Sitemap]     ok 4 - ccTLD-looking domain is url
  [Sitemap]     ok 5 - host with port is url
  [Sitemap]     ok 6 - scheme always wins over denylist
  [Sitemap]     ok 7 - denylisted ext, missing file is neither
  [Sitemap]     1..7
  [Sitemap] ok 19 - detect-input-type: existing files win over URL heuristics
  [Sitemap] # Subtest: cached-client keys follow mode into the pool
  [Sitemap]     ok 1 - follow=False gets a dedicated client, not the auto-follow one
  [Sitemap]     ok 2 - follow=False clients are pooled among themselves
  [Sitemap]     1..2
  [Sitemap] ok 20 - cached-client keys follow mode into the pool
  [Sitemap] # Subtest: resolve-relative-url splits at first of ? or # (no .. leak)
  [Sitemap]     ok 1 - fragment containing ? no longer leaks a literal ..
  [Sitemap]     ok 2 - fragment content preserved verbatim
  [Sitemap]     ok 3 - normal ?-before- \# unchanged
  [Sitemap]     ok 4 - path dot-segments still collapse
  [Sitemap]     ok 5 - a relative ref splits at the fragment first; ../ inside it is untouched
  [Sitemap]     1..5
  [Sitemap] ok 21 - resolve-relative-url splits at first of ? or  \# (no .. leak)
  [Sitemap] # Subtest: resolve-relative-url: trailing . segment normalizes like a slash (RFC 3986 5.2.4)
  [Sitemap]     ok 1 - "/a/." collapses to "/a/", not "/a"
  [Sitemap]     ok 2 - relative "a/." also keeps the trailing slash
  [Sitemap]     ok 3 - interior dot-segments unchanged
  [Sitemap]     ok 4 - a trailing ".." folds like a trailing "." and keeps the slash
  [Sitemap]     ok 5 - a bare ".." resolves to the parent directory with its slash
  [Sitemap]     ok 6 - a ".." back at the root leaves a lone slash, not an empty path
  [Sitemap]     1..6
  [Sitemap] ok 22 - resolve-relative-url: trailing . segment normalizes like a slash (RFC 3986 5.2.4)
  [Sitemap] # Subtest: normalize-http-url drops zero-padded default ports; origins keep non-http ports
  [Sitemap]     ok 1 - ":0080" normalizes like ":80" (numeric comparison, not Str eq)
  [Sitemap]     ok 2 - path/query/fragment survive default-port stripping
  [Sitemap]     ok 3 - non-numeric port garbage is preserved, not coerced
  [Sitemap]     ok 4 - userinfo and non-default ports untouched
  [Sitemap]     ok 5 - distinct explicit ports on a non-http(s) scheme are distinct origins
  [Sitemap]     1..5
  [Sitemap] ok 23 - normalize-http-url drops zero-padded default ports; origins keep non-http ports
  [Sitemap] # Subtest: fifo-evict keeps the map bounded and drops oldest keys (CQ-F7)
  [Sitemap]     ok 1 - batch keeps order at/below cap (got 10)
  [Sitemap]     ok 2 - map size tracks order size after batch
  [Sitemap]     ok 3 - oldest key evicted
  [Sitemap]     ok 4 - newest key survives
  [Sitemap]     ok 5 - order head advanced past evicted keys
  [Sitemap]     ok 6 - half strategy drops half of 20
  [Sitemap]     ok 7 - map size follows after half eviction
  [Sitemap]     ok 8 - oldest half evicted
  [Sitemap]     ok 9 - newest half survives
  [Sitemap]     ok 10 - one strategy drops exactly one
  [Sitemap]     ok 11 - oldest single key evicted
  [Sitemap]     ok 12 - newest survives
  [Sitemap]     ok 13 - no eviction below the cap
  [Sitemap]     ok 14 - map untouched below the cap
  [Sitemap]     1..14
  [Sitemap] ok 24 - fifo-evict keeps the map bounded and drops oldest keys (CQ-F7)
  ===> Testing [FAIL]: Sitemap:ver<0.0.1>:auth<zef:sasha>
  [Sitemap] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Sitemap:ver<0.0.1>:auth<zef:sasha>
  ===> Install [OK] for Sitemap:ver<0.0.1>:auth<zef:sasha>

  1 bin/ script [sitemap] installed to:
  /home/coke/sandbox/blin/installed/Sitemap_zef:sasha_0.0.1_0/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 18min 10.023s
               CPU time consumed: 15min 45.870s
                     Memory peak: 2.6G (swap: 1G)

  ```
  </details>
* [ ] [Syndicate](https://raku.land/zef:sasha/Syndicate) – Fail, Bisected: [00ccf31](https://github.com/rakudo/rakudo/commit/00ccf31f6078091762e1071c2bcd8fcb07ca9a7d)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p297114-i344633.service; invocation ID: 6cd63e8084934a34b8a64303eb1c6723
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Syndicate
  ===> Found: Syndicate:ver<0.0.6>:auth<zef:sasha> [via Zef::Repository::Ecosystems<fez>]
  [Syndicate] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788473056.297121.2301.5368770332525/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz https://360.zef.pm/S/YN/SYNDICATE/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz
  ===> Fetching [OK]: Syndicate:ver<0.0.6>:auth<zef:sasha> to /home/coke/sandbox/blin/data/zef-data/tmp/1788473056.297121.2301.5368770332525/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz
  [Syndicate] Command: tar -t -f ./37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz
  [Syndicate] Command: tar -xvf ./37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz -C ../37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz
  ===> Extraction [OK]: Syndicate to /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz
  ===> Testing: Syndicate:ver<0.0.6>:auth<zef:sasha>
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/00-basic.rakutest
  [Syndicate] 1..10
  [Syndicate] ok 1 - Syndicate module can be use-d ok
  [Syndicate] ok 2 - RSS::Item generates XML
  [Syndicate] ok 3 - RSS::Item Str contains item tag
  [Syndicate] ok 4 - RSS feed generates XML
  [Syndicate] ok 5 - RSS feed Str contains rss tag
  [Syndicate] ok 6 - RSS feed contains channel tag
  [Syndicate] ok 7 - RSS feed contains title text
  [Syndicate] ok 8 - RSS feed contains item tag
  [Syndicate] ok 9 - RSS::Item.new(Str) parses item XML
  [Syndicate] ok 10 - RSS::Item.new(Str) title
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/01-roundtrip.rakutest
  [Syndicate] 1..18
  [Syndicate] ok 1 - RSS output encodes & in title
  [Syndicate] ok 2 - RSS output encodes <> in title
  [Syndicate] ok 3 - RSS output encodes & in link
  [Syndicate] ok 4 - RSS output encodes <> in description
  [Syndicate] ok 5 - RSS output encodes item title
  [Syndicate] ok 6 - RSS entity roundtrip title
  [Syndicate] ok 7 - RSS entity roundtrip item title
  [Syndicate] ok 8 - RSS roundtrip item count
  [Syndicate] ok 9 - Atom self-link type preserved in output
  [Syndicate] ok 10 - Atom roundtrip title
  [Syndicate] ok 11 - Atom self-link type roundtrips
  [Syndicate] ok 12 - Atom roundtrip item count
  [Syndicate] ok 13 - RSS 0.91 roundtrip title
  [Syndicate] ok 14 - RSS 0.91 image roundtrip
  [Syndicate] ok 15 - RSS 0.91 textInput roundtrip
  [Syndicate] ok 16 - RSS 0.91 skipHours count
  [Syndicate] ok 17 - RSS 0.91 skipDays count
  [Syndicate] ok 18 - RSS 0.91 item count
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/02-parse.rakutest
  [Syndicate] 1..38
  [Syndicate] ok 1 - atom-full.xml detected as Atom
  [Syndicate] ok 2 - rss2-full.xml detected as RSS2
  [Syndicate] ok 3 - rss091-full.xml detected as RSS091
  [Syndicate] ok 4 - RSS without version -> RSS2
  [Syndicate] ok 5 - RSS version="2.0" -> RSS2
  [Syndicate] ok 6 - RSS version="0.91" -> RSS091
  [Syndicate] ok 7 - bare Atom -> Atom
  [Syndicate] ok 8 - jsonfeed-full.json detected as JSONFeedFmt
  [Syndicate] ok 9 - bare JSON -> JSONFeedFmt
  [Syndicate] ok 10 - parse-feed json returns JSONFeed
  [Syndicate] ok 11 - parse-feed atom returns Atom
  [Syndicate] ok 12 - parse-feed rss2 returns RSS
  [Syndicate] ok 13 - parse-feed rss091 returns V0_91
  [Syndicate] ok 14 - parse() atom returns Atom
  [Syndicate] ok 15 - parse() rss2 returns RSS
  [Syndicate] ok 16 - parse() rss091 returns V0_91
  [Syndicate] ok 17 - parse() json returns JSONFeed
  [Syndicate] ok 18 - parse() atom title
  [Syndicate] ok 19 - parse() rss2 title
  [Syndicate] ok 20 - parse() rss091 title
  [Syndicate] ok 21 - parse() json title
  [Syndicate] ok 22 - rss1-full.xml detected as RSS1
  [Syndicate] ok 23 - bare RSS1 -> RSS1
  [Syndicate] ok 24 - parse-feed rss1 returns V1_0
  [Syndicate] ok 25 - parse() rss1 returns V1_0
  [Syndicate] ok 26 - parse() rss1 title
  [Syndicate] ok 27 - empty string dies
  [Syndicate] ok 28 - whitespace-only dies
  [Syndicate] ok 29 - non-XML dies
  [Syndicate] ok 30 - unknown root element dies
  [Syndicate] ok 31 - feed-format is exported
  [Syndicate] ok 32 - parse-feed is exported
  [Syndicate] ok 33 - parse is exported from Syndicate
  [Syndicate] ok 34 - parse-file atom
  [Syndicate] ok 35 - parse-file rss2
  [Syndicate] ok 36 - parse-file rss1
  [Syndicate] ok 37 - parse-file jsonfeed IO::Path
  [Syndicate] ok 38 - parse-file nonexistent file dies
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/03-rss-parse.rakutest
  [Syndicate] 1..20
  [Syndicate] ok 1 - Parsed RSS 2.0 feed
  [Syndicate] ok 2 - Does Syndicate::Feed role
  [Syndicate] ok 3 - channel title
  [Syndicate] ok 4 - channel link
  [Syndicate] ok 5 - channel description
  [Syndicate] ok 6 - channel language
  [Syndicate] ok 7 - channel copyright
  [Syndicate] ok 8 - channel managingEditor
  [Syndicate] ok 9 - channel webMaster
  [Syndicate] ok 10 - channel category
  [Syndicate] ok 11 - channel generator
  [Syndicate] ok 12 - channel docs
  [Syndicate] ok 13 - channel ttl
  [Syndicate] ok 14 - pubDate is DateTime
  [Syndicate] ok 15 - pubDate year
  [Syndicate] ok 16 - pubDate month
  [Syndicate] ok 17 - pubDate day
  [Syndicate] ok 18 - dc:creator feed has 1 item
  [Syndicate] ok 19 - dc:creator maps to author
  [Syndicate] ok 20 - dc:creator item title preserved
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/04-rss091-parse.rakutest
  [Syndicate] 1..59
  [Syndicate] ok 1 - Parsed RSS 0.91 feed
  [Syndicate] ok 2 - Does Syndicate::Feed role
  [Syndicate] ok 3 - channel title
  [Syndicate] ok 4 - channel link
  [Syndicate] ok 5 - channel description
  [Syndicate] ok 6 - channel language
  [Syndicate] ok 7 - channel rating
  [Syndicate] ok 8 - channel copyright
  [Syndicate] ok 9 - channel managingEditor
  [Syndicate] ok 10 - channel webMaster
  [Syndicate] ok 11 - channel docs
  [Syndicate] ok 12 - pubDate is DateTime
  [Syndicate] ok 13 - pubDate year
  [Syndicate] ok 14 - pubDate month
  [Syndicate] ok 15 - pubDate day
  [Syndicate] ok 16 - lastBuildDate is DateTime
  [Syndicate] ok 17 - lastBuildDate year
  [Syndicate] ok 18 - image exists
  [Syndicate] ok 19 - image title
  [Syndicate] ok 20 - image url
  [Syndicate] ok 21 - image link
  [Syndicate] ok 22 - image width
  [Syndicate] ok 23 - image height
  [Syndicate] ok 24 - image description
  [Syndicate] ok 25 - textInput exists
  [Syndicate] ok 26 - textInput title
  [Syndicate] ok 27 - textInput description
  [Syndicate] ok 28 - textInput name
  [Syndicate] ok 29 - textInput link
  [Syndicate] ok 30 - skipHours count
  [Syndicate] ok 31 - skipHours first hour
  [Syndicate] ok 32 - skipHours second hour
  [Syndicate] ok 33 - skipDays count
  [Syndicate] ok 34 - skipDays first day
  [Syndicate] ok 35 - skipDays second day
  [Syndicate] ok 36 - item count
  [Syndicate] ok 37 - first item is V0_91::Item
  [Syndicate] ok 38 - first item title
  [Syndicate] ok 39 - first item link
  [Syndicate] ok 40 - first item description
  [Syndicate] ok 41 - second item title
  [Syndicate] ok 42 - second item link
  [Syndicate] ok 43 - second item description
  [Syndicate] ok 44 - third item title
  [Syndicate] ok 45 - third item description
  [Syndicate] ok 46 - items missing title/link/description are skipped
  [Syndicate] ok 47 - valid item still parsed
  [Syndicate] ok 48 - roundtrip title
  [Syndicate] ok 49 - roundtrip link
  [Syndicate] ok 50 - roundtrip description
  [Syndicate] ok 51 - roundtrip item count
  [Syndicate] ok 52 - roundtrip item title
  [Syndicate] ok 53 - roundtrip pubDate is DateTime
  [Syndicate] ok 54 - XML has rss root
  [Syndicate] ok 55 - XML has channel
  [Syndicate] ok 56 - XML has skipHours
  [Syndicate] ok 57 - XML has textInput
  [Syndicate] ok 58 - XML has image
  [Syndicate] ok 59 - XML has items
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/05-rss1-parse.rakutest
  [Syndicate] 1..32
  [Syndicate] ok 1 - Parsed RSS 1.0 feed
  [Syndicate] ok 2 - Does Syndicate::Feed role
  [Syndicate] ok 3 - channel title
  [Syndicate] ok 4 - channel link
  [Syndicate] ok 5 - channel description
  [Syndicate] ok 6 - channel about
  [Syndicate] ok 7 - image url
  [Syndicate] ok 8 - image title
  [Syndicate] ok 9 - image link
  [Syndicate] ok 10 - image about
  [Syndicate] ok 11 - two items
  [Syndicate] ok 12 - item is correct type
  [Syndicate] ok 13 - item 0 title
  [Syndicate] ok 14 - item 0 link
  [Syndicate] ok 15 - item 0 summary
  [Syndicate] ok 16 - item 0 about
  [Syndicate] ok 17 - item 1 title
  [Syndicate] ok 18 - item 1 link
  [Syndicate] ok 19 - Str roundtrip
  [Syndicate] ok 20 - roundtrip title matches
  [Syndicate] ok 21 - dc feed has 2 items
  [Syndicate] ok 22 - dc:creator maps to author
  [Syndicate] ok 23 - dc:date maps to DateTime
  [Syndicate] ok 24 - dc:date year
  [Syndicate] ok 25 - two dc:subject elements
  [Syndicate] ok 26 - first dc:subject
  [Syndicate] ok 27 - second dc:subject
  [Syndicate] ok 28 - dc:creator maps to author on item 1
  [Syndicate] ok 29 - one dc:subject on item 1
  [Syndicate] ok 30 - dc:subject on item 1
  [Syndicate] ok 31 - roundtrip dc:creator
  [Syndicate] ok 32 - roundtrip dc:subjects count
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/06-atom-parse.rakutest
  [Syndicate] 1..55
  [Syndicate] ok 1 - Parsed Atom 1.0 feed
  [Syndicate] ok 2 - Does Syndicate::Feed role
  [Syndicate] ok 3 - feed title
  [Syndicate] ok 4 - feed id
  [Syndicate] ok 5 - feed subtitle
  [Syndicate] ok 6 - feed rights
  [Syndicate] ok 7 - feed generator
  [Syndicate] ok 8 - feed icon
  [Syndicate] ok 9 - feed logo
  [Syndicate] ok 10 - updated is DateTime
  [Syndicate] ok 11 - updated year
  [Syndicate] ok 12 - feed link (alternate)
  [Syndicate] ok 13 - feed link-self href
  [Syndicate] ok 14 - feed link-alternate href
  [Syndicate] ok 15 - feed author-detail name defined
  [Syndicate] ok 16 - feed author-detail name
  [Syndicate] ok 17 - feed author-detail email
  [Syndicate] ok 18 - feed author-detail uri
  [Syndicate] ok 19 - two categories
  [Syndicate] ok 20 - first category
  [Syndicate] ok 21 - second category
  [Syndicate] ok 22 - two entries
  [Syndicate] ok 23 - entry is Atom::Item
  [Syndicate] ok 24 - entry title
  [Syndicate] ok 25 - entry link
  [Syndicate] ok 26 - entry id
  [Syndicate] ok 27 - entry summary
  [Syndicate] ok 28 - entry content
  [Syndicate] ok 29 - entry content-type
  [Syndicate] ok 30 - entry published is DateTime
  [Syndicate] ok 31 - entry updated is DateTime
  [Syndicate] ok 32 - entry rights
  [Syndicate] ok 33 - entry author name
  [Syndicate] ok 34 - entry author email
  [Syndicate] ok 35 - entry has one category
  [Syndicate] ok 36 - entry category term
  [Syndicate] ok 37 - entry has one contributor
  [Syndicate] ok 38 - entry contributor name
  [Syndicate] ok 39 - entry source-feed title defined
  [Syndicate] ok 40 - entry source-feed title
  [Syndicate] ok 41 - entry source-feed link
  [Syndicate] ok 42 - entry source-feed updated is DateTime
  [Syndicate] ok 43 - roundtrip title
  [Syndicate] ok 44 - roundtrip rights
  [Syndicate] ok 45 - roundtrip generator
  [Syndicate] ok 46 - roundtrip icon
  [Syndicate] ok 47 - roundtrip logo
  [Syndicate] ok 48 - roundtrip author name
  [Syndicate] ok 49 - roundtrip 2 categories
  [Syndicate] ok 50 - roundtrip 2 entries
  [Syndicate] ok 51 - roundtrip entry title
  [Syndicate] ok 52 - roundtrip entry content
  [Syndicate] ok 53 - roundtrip entry content-type
  [Syndicate] ok 54 - roundtrip entry 1 category
  [Syndicate] ok 55 - roundtrip entry 1 contributor
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/07-jsonfeed-parse.rakutest
  [Syndicate] 1..63
  [Syndicate] ok 1 - Parsed JSON Feed
  [Syndicate] ok 2 - Does Syndicate::Feed role
  [Syndicate] ok 3 - feed title
  [Syndicate] ok 4 - feed link (home_page_url)
  [Syndicate] ok 5 - feed description
  [Syndicate] ok 6 - feed feed_url
  [Syndicate] ok 7 - feed user_comment
  [Syndicate] ok 8 - feed next_url
  [Syndicate] ok 9 - feed icon
  [Syndicate] ok 10 - feed favicon
  [Syndicate] ok 11 - feed language
  [Syndicate] ok 12 - feed expired is Bool
  [Syndicate] ok 13 - feed expired is false
  [Syndicate] ok 14 - feed author name
  [Syndicate] ok 15 - feed author url
  [Syndicate] ok 16 - feed author avatar
  [Syndicate] ok 17 - two entries
  [Syndicate] ok 18 - entry is JSONFeed::Item
  [Syndicate] ok 19 - entry title
  [Syndicate] ok 20 - entry link (url)
  [Syndicate] ok 21 - entry id
  [Syndicate] ok 22 - entry external_url
  [Syndicate] ok 23 - entry summary
  [Syndicate] ok 24 - entry content_html
  [Syndicate] ok 25 - entry content_text
  [Syndicate] ok 26 - entry image
  [Syndicate] ok 27 - entry banner_image
  [Syndicate] ok 28 - entry date_published is DateTime
  [Syndicate] ok 29 - entry date_published year
  [Syndicate] ok 30 - entry date_modified is DateTime
  [Syndicate] ok 31 - entry date_modified year
  [Syndicate] ok 32 - entry has one author
  [Syndicate] ok 33 - entry author name
  [Syndicate] ok 34 - entry author url
  [Syndicate] ok 35 - entry author avatar
  [Syndicate] ok 36 - entry has 2 tags
  [Syndicate] ok 37 - entry first tag
  [Syndicate] ok 38 - entry second tag
  [Syndicate] ok 39 - entry2 title
  [Syndicate] ok 40 - entry2 link
  [Syndicate] ok 41 - entry2 id
  [Syndicate] ok 42 - entry2 external_url is undefined
  [Syndicate] ok 43 - entry2 content_html is undefined
  [Syndicate] ok 44 - entry2 date_published is undefined
  [Syndicate] ok 45 - entry2 date_modified is DateTime
  [Syndicate] ok 46 - entry2 date_modified year
  [Syndicate] ok 47 - entry2 has no authors
  [Syndicate] ok 48 - entry2 has no tags
  [Syndicate] ok 49 - roundtrip title
  [Syndicate] ok 50 - roundtrip link
  [Syndicate] ok 51 - roundtrip description
  [Syndicate] ok 52 - roundtrip feed_url
  [Syndicate] ok 53 - roundtrip icon
  [Syndicate] ok 54 - roundtrip favicon
  [Syndicate] ok 55 - roundtrip language
  [Syndicate] ok 56 - roundtrip author name
  [Syndicate] ok 57 - roundtrip 2 entries
  [Syndicate] ok 58 - roundtrip entry1 title
  [Syndicate] ok 59 - roundtrip entry1 content_html
  [Syndicate] ok 60 - roundtrip entry1 2 tags
  [Syndicate] ok 61 - roundtrip entry1 1 author
  [Syndicate] ok 62 - roundtrip entry2 title
  [Syndicate] ok 63 - Str roundtrip lives
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/08-builder.rakutest
  [Syndicate] 1..140
  [Syndicate] ok 1 - Feed builder created
  [Syndicate] ok 2 - feed title get/set
  [Syndicate] ok 3 - feed link get/set
  [Syndicate] ok 4 - feed description get/set
  [Syndicate] ok 5 - feed id get/set
  [Syndicate] ok 6 - feed language get/set
  [Syndicate] ok 7 - feed rights get/set
  [Syndicate] ok 8 - feed generator get/set
  [Syndicate] ok 9 - feed icon get/set
  [Syndicate] ok 10 - feed logo get/set
  [Syndicate] ok 11 - feed author name
  [Syndicate] ok 12 - feed author email
  [Syndicate] ok 13 - feed has 2 categories
  [Syndicate] ok 14 - default generator value
  [Syndicate] ok 15 - entry created via add-entry
  [Syndicate] ok 16 - entry title get/set
  [Syndicate] ok 17 - entry link get/set
  [Syndicate] ok 18 - entry summary get/set
  [Syndicate] ok 19 - entry id get/set
  [Syndicate] ok 20 - entry updated is defined
  [Syndicate] ok 21 - feed has 2 entries
  [Syndicate] ok 22 - entry content get/set
  [Syndicate] ok 23 - rss-str generates output
  [Syndicate] ok 24 - RSS output has rss root
  [Syndicate] ok 25 - RSS output has channel
  [Syndicate] ok 26 - RSS output has feed title
  [Syndicate] ok 27 - RSS output has language
  [Syndicate] ok 28 - RSS output has copyright
  [Syndicate] ok 29 - RSS output has managingEditor
  [Syndicate] ok 30 - RSS output has generator
  [Syndicate] ok 31 - RSS output has items
  [Syndicate] ok 32 - atom-str generates output
  [Syndicate] ok 33 - Atom output has feed root
  [Syndicate] ok 34 - Atom output has feed title
  [Syndicate] ok 35 - Atom output has feed id
  [Syndicate] ok 36 - Atom output has subtitle
  [Syndicate] ok 37 - Atom output has author email (from entry)
  [Syndicate] ok 38 - Atom output has entries
  [Syndicate] ok 39 - Atom output has rights
  [Syndicate] ok 40 - Atom output has generator
  [Syndicate] ok 41 - Atom output has icon
  [Syndicate] ok 42 - Atom output has logo
  [Syndicate] ok 43 - Atom output has category
  [Syndicate] ok 44 - Atom output has second category
  [Syndicate] ok 45 - RSS roundtrip parsed
  [Syndicate] ok 46 - RSS roundtrip title
  [Syndicate] ok 47 - RSS roundtrip link
  [Syndicate] ok 48 - RSS roundtrip description
  [Syndicate] ok 49 - RSS roundtrip language
  [Syndicate] ok 50 - RSS roundtrip copyright
  [Syndicate] ok 51 - RSS roundtrip item count
  [Syndicate] ok 52 - RSS roundtrip first item title
  [Syndicate] ok 53 - RSS roundtrip second item title
  [Syndicate] ok 54 - RSS roundtrip pubDate is DateTime
  [Syndicate] ok 55 - Atom roundtrip parsed
  [Syndicate] ok 56 - Atom roundtrip title
  [Syndicate] ok 57 - Atom roundtrip id
  [Syndicate] ok 58 - Atom roundtrip subtitle
  [Syndicate] ok 59 - Atom roundtrip rights
  [Syndicate] ok 60 - Atom roundtrip generator
  [Syndicate] ok 61 - Atom roundtrip icon
  [Syndicate] ok 62 - Atom roundtrip logo
  [Syndicate] ok 63 - Atom roundtrip author name
  [Syndicate] ok 64 - Atom roundtrip author email
  [Syndicate] ok 65 - Atom roundtrip 2 categories
  [Syndicate] ok 66 - Atom roundtrip entry count
  [Syndicate] ok 67 - Atom roundtrip first entry title
  [Syndicate] ok 68 - Atom roundtrip second entry title
  [Syndicate] ok 69 - Atom roundtrip updated is DateTime
  [Syndicate] ok 70 - Atom output has content with type
  [Syndicate] ok 71 - Atom output has XHTML content body
  [Syndicate] ok 72 - content roundtrip body (RFC 4287 xhtml div wrapper)
  [Syndicate] ok 73 - content roundtrip type
  [Syndicate] ok 74 - empty RSS has root
  [Syndicate] ok 75 - empty RSS has title
  [Syndicate] ok 76 - empty Atom has root
  [Syndicate] ok 77 - empty Atom has title
  [Syndicate] ok 78 - rss091-str generates output
  [Syndicate] ok 79 - RSS 0.91 output has version 0.91
  [Syndicate] ok 80 - RSS 0.91 output has channel
  [Syndicate] ok 81 - RSS 0.91 output has feed title
  [Syndicate] ok 82 - RSS 0.91 output has language
  [Syndicate] ok 83 - RSS 0.91 output has copyright
  [Syndicate] ok 84 - RSS 0.91 output has managingEditor
  [Syndicate] ok 85 - RSS 0.91 output has items
  [Syndicate] ok 86 - rss091-feed returns V0_91
  [Syndicate] ok 87 - RSS 0.91 roundtrip parsed
  [Syndicate] ok 88 - RSS 0.91 roundtrip title
  [Syndicate] ok 89 - RSS 0.91 roundtrip link
  [Syndicate] ok 90 - RSS 0.91 roundtrip description
  [Syndicate] ok 91 - RSS 0.91 roundtrip language
  [Syndicate] ok 92 - RSS 0.91 roundtrip copyright
  [Syndicate] ok 93 - RSS 0.91 roundtrip item count
  [Syndicate] ok 94 - RSS 0.91 roundtrip first item title
  [Syndicate] ok 95 - RSS 0.91 roundtrip first item link
  [Syndicate] ok 96 - RSS 0.91 roundtrip first item description
  [Syndicate] ok 97 - empty RSS 0.91 has root
  [Syndicate] ok 98 - empty RSS 0.91 has title
  [Syndicate] ok 99 - rss1-str generates output
  [Syndicate] ok 100 - RSS 1.0 output has rdf:RDF root
  [Syndicate] ok 101 - RSS 1.0 output has channel
  [Syndicate] ok 102 - RSS 1.0 output has feed title
  [Syndicate] ok 103 - RSS 1.0 output has items
  [Syndicate] ok 104 - rss1-feed returns V1_0
  [Syndicate] ok 105 - RSS 1.0 roundtrip parsed
  [Syndicate] ok 106 - RSS 1.0 roundtrip title
  [Syndicate] ok 107 - RSS 1.0 roundtrip link
  [Syndicate] ok 108 - RSS 1.0 roundtrip description
  [Syndicate] ok 109 - RSS 1.0 roundtrip item count
  [Syndicate] ok 110 - RSS 1.0 roundtrip first item title
  [Syndicate] ok 111 - RSS 1.0 roundtrip first item link
  [Syndicate] ok 112 - RSS 1.0 roundtrip first item summary
  [Syndicate] ok 113 - RSS 1.0 roundtrip first item author (dc:creator)
  [Syndicate] ok 114 - RSS 1.0 output omits non-standard <author>
  [Syndicate] ok 115 - RSS 1.0 output omits non-standard <category>
  [Syndicate] ok 116 - RSS 1.0 output carries author as dc:creator
  [Syndicate] ok 117 - RSS 1.0 output carries category as dc:subject
  [Syndicate] ok 118 - RSS 1.0 dc:subject roundtrip
  [Syndicate] ok 119 - empty RSS 1.0 has root
  [Syndicate] ok 120 - empty RSS 1.0 has title
  [Syndicate] ok 121 - json-str generates output
  [Syndicate] ok 122 - json-str output is valid JSON
  [Syndicate] ok 123 - JSON output has feed title
  [Syndicate] ok 124 - JSON output has 2 items
  [Syndicate] ok 125 - JSON roundtrip parsed
  [Syndicate] ok 126 - JSON roundtrip title
  [Syndicate] ok 127 - JSON roundtrip item count
  [Syndicate] ok 128 - JSON roundtrip first item title
  [Syndicate] ok 129 - RSS 1.0 builder output declares xmlns:dc
  [Syndicate] ok 130 - RSS 1.0 builder output has dc:creator
  [Syndicate] ok 131 - RSS builder output declares xmlns:content
  [Syndicate] ok 132 - RSS builder output has content:encoded
  [Syndicate] ok 133 - RSS 1.0 builder output has no pubDate
  [Syndicate] ok 134 - RSS 1.0 builder output has dc:date
  [Syndicate] ok 135 - RSS 1.0 dc:date roundtrip year
  [Syndicate] ok 136 - RSS 0.91 builder output has no content:encoded
  [Syndicate] ok 137 - RSS 0.91 builder output has no xmlns:content
  [Syndicate] # Subtest: str(:pretty) indents without changing content
  [Syndicate]     ok 1 - plain rss-str is stable/idempotent
  [Syndicate]     ok 2 - pretty output puts <channel> on its own line
  [Syndicate]     ok 3 - pretty output indents a leaf element and keeps its escaped text intact
  [Syndicate]     ok 4 - pretty output is plain output with whitespace inserted only
  [Syndicate]     ok 5 - pretty output parses back with the same title
  [Syndicate]     ok 6 - pretty output preserves entity-escaped leaf text on parse
  [Syndicate]     ok 7 - atom pretty output indents entries
  [Syndicate]     1..7
  [Syndicate] ok 138 - str(:pretty) indents without changing content
  [Syndicate] # Subtest: str(:pretty) differs from Str only by whitespace on one object
  [Syndicate]     ok 1 - RSS 2.0 Str and str(:pretty) differ only by whitespace
  [Syndicate]     ok 2 - RSS 1.0 Str and str(:pretty) differ only by whitespace
  [Syndicate]     ok 3 - RSS 0.91 Str and str(:pretty) differ only by whitespace
  [Syndicate]     ok 4 - Atom Str and str(:pretty) differ only by whitespace
  [Syndicate]     1..4
  [Syndicate] ok 139 - str(:pretty) differs from Str only by whitespace on one object
  [Syndicate] # Subtest: indent-xml handles arbitrary element shapes without changing content
  [Syndicate]     ok 1 - flat-preserving: 0 (<rss><channel><item>one</item><item2 id="x">two</item2></channel></rss>)
  [Syndicate]     ok 2 - no spurious empty close tag for: 0
  [Syndicate]     ok 3 - flat-preserving: 1 (<rss><channel><item-rss>text</item-rss></channel></rss>)
  [Syndicate]     ok 4 - no spurious empty close tag for: 1
  [Syndicate]     ok 5 - flat-preserving: 2 (<rss><channel><rdf.RDF>text</rdf.RDF></channel></rss>)
  [Syndicate]     ok 6 - no spurious empty close tag for: 2
  [Syndicate]     ok 7 - flat-preserving: 3 (<rss><a/><b>hi</b><c></c></rss>)
  [Syndicate]     ok 8 - no spurious empty close tag for: 3
  [Syndicate]     ok 9 - flat-preserving: 4 (<a>just text</a>)
  [Syndicate]     ok 10 - no spurious empty close tag for: 4
  [Syndicate]     ok 11 - flat-preserving: 5 (<a>lead<b>hi</b>tail</a>)
  [Syndicate]     ok 12 - no spurious empty close tag for: 5
  [Syndicate]     ok 13 - flat-preserving: 6 (<a>text <em>one</em> and <em>two</em> done</a>)
  [Syndicate]     ok 14 - no spurious empty close tag for: 6
  [Syndicate]     ok 15 - flat-preserving: 7 (<a>before<b>nested<c>deep</c>after</b>tail</a>)
  [Syndicate]     ok 16 - no spurious empty close tag for: 7
  [Syndicate]     ok 17 - flat-preserving: 8 (<rss><!--comment--><a>x</a></rss>)
  [Syndicate]     ok 18 - no spurious empty close tag for: 8
  [Syndicate]     ok 19 - flat-preserving: 9 (<rss><a><![CDATA[<b>raw & unparsed</b>]]></a></rss>)
  [Syndicate]     ok 20 - no spurious empty close tag for: 9
  [Syndicate]     ok 21 - flat-preserving: 10 (<rss xmlns:c="x"><c:item>v</c:item></rss>)
  [Syndicate]     ok 22 - no spurious empty close tag for: 10
  [Syndicate]     ok 23 - mixed content keeps child elements in order
  [Syndicate]     ok 24 - mixed content keeps inline text spans intact
  [Syndicate]     1..24
  [Syndicate] ok 140 - indent-xml handles arbitrary element shapes without changing content
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/09-discovery.rakutest
  [Syndicate] 1..61
  [Syndicate] ok 1 - absolute URL unchanged
  [Syndicate] ok 2 - root-relative URL
  [Syndicate] ok 3 - relative URL with trailing slash
  [Syndicate] ok 4 - relative URL without trailing slash
  [Syndicate] ok 5 - root-relative URL with path base
  [Syndicate] ok 6 - different origin https URL
  [Syndicate] ok 7 - protocol-relative URL
  [Syndicate] ok 8 - extract <base href>
  [Syndicate] ok 9 - no <base> tag returns Str
  [Syndicate] ok 10 - single-quoted base href
  [Syndicate] ok 11 - found 2 feed links
  [Syndicate] ok 12 - first feed is RSS
  [Syndicate] ok 13 - second feed is Atom
  [Syndicate] ok 14 - no feeds found when none present
  [Syndicate] ok 15 - found JSON feed link
  [Syndicate] ok 16 - JSON feed URL
  [Syndicate] ok 17 - found feed in multi-line HTML
  [Syndicate] ok 18 - multi-line feed URL
  [Syndicate] ok 19 - found feed with base href
  [Syndicate] ok 20 - base href affects URL resolution
  [Syndicate] ok 21 - found HTTPS feed link
  [Syndicate] ok 22 - HTTPS feed URL preserved
  [Syndicate] ok 23 - no feeds when rel is not alternate
  [Syndicate] ok 24 - single-quoted attributes work
  [Syndicate] ok 25 - single-quoted href
  [Syndicate] ok 26 - SSRF blocked: http://127.0.0.1/feed
  [Syndicate] ok 27 - SSRF blocked: http://127.1/feed
  [Syndicate] ok 28 - SSRF blocked: http://0x7f.1/feed
  [Syndicate] ok 29 - SSRF blocked: http://0177.0.0.1/feed
  [Syndicate] ok 30 - SSRF blocked: http://127.0.0.01/feed
  [Syndicate] ok 31 - SSRF blocked: http://0.0.0.0/feed
  [Syndicate] ok 32 - SSRF blocked: http://10.0.0.1/feed
  [Syndicate] ok 33 - SSRF blocked: http://192.168.1.1/feed
  [Syndicate] ok 34 - SSRF blocked: http://172.16.0.1/feed
  [Syndicate] ok 35 - SSRF blocked: http://169.254.0.1/feed
  [Syndicate] ok 36 - SSRF blocked: http://2130706433/feed
  [Syndicate] ok 37 - SSRF blocked: http://[::1]/feed
  [Syndicate] ok 38 - SSRF blocked: http://[::ffff:127.0.0.1]/feed
  [Syndicate] ok 39 - SSRF blocked: http://[::ffff:2130706433]/feed
  [Syndicate] ok 40 - SSRF blocked: http://[::ffff:7f00:1]/feed
  [Syndicate] ok 41 - SSRF blocked: http://[::ffff:10.0.0.1]/feed
  [Syndicate] ok 42 - SSRF allowed: http://8.8.8.8/feed
  [Syndicate] ok 43 - SSRF allowed: http://[::ffff:8.8.8.8]/feed
  [Syndicate] ok 44 - SSRF allowed: http://example.com/feed
  [Syndicate] ok 45 - SSRF allowed: http://01.example.com/feed
  [Syndicate] ok 46 - Content-Type with charset param accepted
  [Syndicate] ok 47 - Content-Type with multiple params accepted
  [Syndicate] ok 48 - missing Content-Type accepted
  [Syndicate] ok 49 - text/xml accepted
  [Syndicate] ok 50 - text/html rejected
  [Syndicate] ok 51 - bare href attribute skipped without crash
  [Syndicate] ok 52 - valid link found alongside bare href
  [Syndicate] ok 53 - bare rel attribute does not match alternate
  [Syndicate] ok 54 - SSRF blocked: http://[::127.0.0.1]/feed
  [Syndicate] ok 55 - SSRF blocked: http://[0:0:0:0:0:0:127.0.0.1]/feed
  [Syndicate] ok 56 - SSRF allowed: http://[::123.0.0.1]/feed
  [Syndicate] ok 57 - SSRF allowed: http://[2001:db8::1.2.3.4]/feed
  [Syndicate] ok 58 - Content-Length over MAX-FEED-SIZE rejected
  [Syndicate] ok 59 - body over MAX-FEED-SIZE rejected
  [Syndicate] ok 60 - custom duck-typed ua works
  [Syndicate] ok 61 - duck-typed ua fetch returns feed
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/10-media-rss.rakutest
  [Syndicate] 1..51
  [Syndicate] ok 1 - Parsed Media RSS feed
  [Syndicate] ok 2 - two items
  [Syndicate] ok 3 - item 0 title
  [Syndicate] ok 4 - item 0 link
  [Syndicate] ok 5 - item 0 description
  [Syndicate] ok 6 - item 0 has 1 media:content
  [Syndicate] ok 7 - media:content url
  [Syndicate] ok 8 - media:content type
  [Syndicate] ok 9 - media:content medium
  [Syndicate] ok 10 - media:content duration
  [Syndicate] ok 11 - media:content fileSize
  [Syndicate] ok 12 - media:content width
  [Syndicate] ok 13 - media:content height
  [Syndicate] ok 14 - item 0 has 1 media:thumbnail
  [Syndicate] ok 15 - media:thumbnail url
  [Syndicate] ok 16 - media:thumbnail width
  [Syndicate] ok 17 - media:thumbnail height
  [Syndicate] ok 18 - media:thumbnail time
  [Syndicate] ok 19 - media:title
  [Syndicate] ok 20 - media:description
  [Syndicate] ok 21 - item 1 title
  [Syndicate] ok 22 - item 1 link
  [Syndicate] ok 23 - item 1 has 1 media:content
  [Syndicate] ok 24 - item 1 media:content url
  [Syndicate] ok 25 - item 1 media:content type
  [Syndicate] ok 26 - item 1 media:content medium
  [Syndicate] ok 27 - item 1 media:content duration
  [Syndicate] ok 28 - item 1 has 1 media:thumbnail
  [Syndicate] ok 29 - item 1 thumbnail url
  [Syndicate] ok 30 - roundtrip media:content count
  [Syndicate] ok 31 - roundtrip media:content url
  [Syndicate] ok 32 - roundtrip media:title
  [Syndicate] ok 33 - Parsed HH:MM:SS Media RSS feed
  [Syndicate] ok 34 - 3 items in HH:MM:SS test feed
  [Syndicate] ok 35 - HH:MM:SS item title
  [Syndicate] ok 36 - HH:MM:SS item has 1 media:content
  [Syndicate] ok 37 - HH:MM:SS duration is defined
  [Syndicate] ok 38 - HH:MM:SS duration preserved as string
  [Syndicate] ok 39 - multi-content item title
  [Syndicate] ok 40 - multi-content item has 3 media:content elements
  [Syndicate] ok 41 - multi-content[0] url
  [Syndicate] ok 42 - multi-content[0] duration
  [Syndicate] ok 43 - multi-content[1] url
  [Syndicate] ok 44 - multi-content[1] duration
  [Syndicate] ok 45 - multi-content[2] url
  [Syndicate] ok 46 - multi-content[2] medium
  [Syndicate] ok 47 - HH:MM:SS roundtrip parsed
  [Syndicate] ok 48 - HH:MM:SS roundtrip item count
  [Syndicate] ok 49 - HH:MM:SS roundtrip duration
  [Syndicate] ok 50 - multi-content roundtrip count
  [Syndicate] # Subtest: Builder media-content carries medium and nested title/description
  [Syndicate]     ok 1 - media:content emitted
  [Syndicate]     ok 2 - media:content carries url
  [Syndicate]     ok 3 - media:content carries medium
  [Syndicate]     ok 4 - content-level media:title emitted
  [Syndicate]     ok 5 - content-level media:description emitted
  [Syndicate]     ok 6 - roundtrip content url
  [Syndicate]     ok 7 - roundtrip content medium
  [Syndicate]     ok 8 - roundtrip content duration
  [Syndicate]     ok 9 - roundtrip content title
  [Syndicate]     ok 10 - roundtrip content description
  [Syndicate]     ok 11 - medium survives new-from-feed roundtrip
  [Syndicate]     ok 12 - content title survives new-from-feed roundtrip
  [Syndicate]     1..12
  [Syndicate] ok 51 - Builder media-content carries medium and nested title/description
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/11-itunes-podcast.rakutest
  [Syndicate] 1..33
  [Syndicate] ok 1 - Parsed iTunes podcast feed
  [Syndicate] ok 2 - channel itunes:author
  [Syndicate] ok 3 - channel itunes:summary
  [Syndicate] ok 4 - item 0 title
  [Syndicate] ok 5 - item 0 link
  [Syndicate] ok 6 - item 0 itunes:author
  [Syndicate] ok 7 - item 0 itunes:summary
  [Syndicate] ok 8 - item 0 itunes:duration
  [Syndicate] ok 9 - item 1 title
  [Syndicate] ok 10 - item 1 link
  [Syndicate] ok 11 - item 1 itunes:author
  [Syndicate] ok 12 - item 1 itunes:summary
  [Syndicate] ok 13 - item 1 itunes:duration
  [Syndicate] ok 14 - item 2 title
  [Syndicate] ok 15 - item 2 itunes:duration (seconds)
  [Syndicate] ok 16 - item 2 itunes:author is undefined
  [Syndicate] ok 17 - item 2 itunes:summary is undefined
  [Syndicate] ok 18 - Roundtripped feed parsed
  [Syndicate] ok 19 - roundtrip channel itunes:author
  [Syndicate] ok 20 - roundtrip channel itunes:summary
  [Syndicate] ok 21 - roundtrip item count
  [Syndicate] ok 22 - roundtrip item 0 itunes:author
  [Syndicate] ok 23 - roundtrip item 0 itunes:summary
  [Syndicate] ok 24 - roundtrip item 0 itunes:duration
  [Syndicate] ok 25 - roundtrip item 1 itunes:author
  [Syndicate] ok 26 - roundtrip item 1 itunes:duration
  [Syndicate] ok 27 - roundtrip item 2 itunes:duration (seconds)
  [Syndicate] ok 28 - XML output contains xmlns:itunes
  [Syndicate] ok 29 - XML output contains itunes:author
  [Syndicate] ok 30 - XML output contains itunes:summary
  [Syndicate] ok 31 - XML output contains itunes:duration
  [Syndicate] ok 32 - builder channel itunes:author
  [Syndicate] ok 33 - builder item title
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/12-concurrency.rakutest
  [Syndicate] 1..6
  [Syndicate] ok 1 - Stats class exists
  [Syndicate] ok 2 - starts at zero
  [Syndicate] ok 3 - items starts at zero
  [Syndicate] ok 4 - errors starts at zero
  [Syndicate] ok 5 - feeds-parsed = 10 after concurrent increments
  [Syndicate] ok 6 - items-parsed = 50 after concurrent increments
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/13-errors.rakutest
  [Syndicate] 1..16
  [Syndicate] ok 1 - empty input dies
  [Syndicate] ok 2 - whitespace-only input dies
  [Syndicate] ok 3 - unknown root element dies
  [Syndicate] ok 4 - garbage input dies
  [Syndicate] ok 5 - JSON without version key dies
  [Syndicate] ok 6 - parse-feed clarifies that valid JSON is not a JSON Feed
  [Syndicate] ok 7 - parse-feed keeps generic message for non-JSON input
  [Syndicate] ok 8 - wrong root element dies
  [Syndicate] ok 9 - no channel element dies
  [Syndicate] ok 10 - wrong RSS version dies
  [Syndicate] ok 11 - wrong item root element dies
  [Syndicate] ok 12 - wrong Atom entry root element dies
  [Syndicate] ok 13 - wrong Atom root element dies
  [Syndicate] ok 14 - invalid JSON dies
  [Syndicate] ok 15 - wrong RDF root element dies
  [Syndicate] ok 16 - all errors recorded by Stats
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/14-utils.rakutest
  [Syndicate] 1..27
  [Syndicate] ok 1 - encode &
  [Syndicate] ok 2 - encode <
  [Syndicate] ok 3 - encode Str returns Str
  [Syndicate] ok 4 - decode &amp;
  [Syndicate] ok 5 - decode &lt;
  [Syndicate] ok 6 - decode Str returns Str
  [Syndicate] ok 7 - add-element encodes value
  [Syndicate] ok 8 - add-element with Str appends nothing
  [Syndicate] ok 9 - get-text returns decoded text
  [Syndicate] ok 10 - get-text on missing element dies
  [Syndicate] ok 11 - get-text on empty element dies
  [Syndicate] ok 12 - get-text-optional returns text
  [Syndicate] ok 13 - get-text-optional on missing returns Str
  [Syndicate] ok 14 - parse-date RFC3339 returns DateTime
  [Syndicate] ok 15 - year correct
  [Syndicate] ok 16 - parse-date on empty dies
  [Syndicate] ok 17 - parse-date :optional valid returns DateTime
  [Syndicate] ok 18 - parse-date :optional invalid returns Nil
  [Syndicate] ok 19 - parse-date :optional empty returns Nil
  [Syndicate] ok 20 - AM/PM without seconds parses
  [Syndicate] ok 21 - AM hour preserved
  [Syndicate] ok 22 - missing seconds default to 0
  [Syndicate] ok 23 - AM/PM with seconds parses
  [Syndicate] ok 24 - PM hour converted to 24h
  [Syndicate] ok 25 - seconds preserved
  [Syndicate] ok 26 - 12 AM parses
  [Syndicate] ok 27 - 12 AM maps to midnight
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/15-extensions.rakutest
  [Syndicate] 1..6
  [Syndicate] ok 1 - run-parsers calls registered parse callbacks
  [Syndicate] ok 2 - run-parsers callback can modify %attrs
  [Syndicate] ok 3 - run-generators calls registered generate callbacks
  [Syndicate] ok 4 - run-generators callback can modify $xml
  [Syndicate] ok 5 - run-parsers catches dying callbacks
  [Syndicate] ok 6 - run-generators catches dying callbacks
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/16-ext-utils.rakutest
  [Syndicate] 1..19
  [Syndicate] ok 1 - DC: get-dc-text returns creator
  [Syndicate] ok 2 - DC: get-dc-text on missing returns Str
  [Syndicate] ok 3 - DC: get-dc-texts returns all subjects
  [Syndicate] ok 4 - DC: first dc:subject
  [Syndicate] ok 5 - DC: add-dc-declaration sets xmlns
  [Syndicate] ok 6 - DC: add-dc-element creates element with text
  [Syndicate] ok 7 - DC: add-dc-element with Str adds nothing
  [Syndicate] ok 8 - MRSS: get-media-text returns title
  [Syndicate] ok 9 - MRSS: get-media-text on missing returns Str
  [Syndicate] ok 10 - MRSS: get-media-contents count
  [Syndicate] ok 11 - MRSS: media:content url
  [Syndicate] ok 12 - MRSS: get-media-thumbnails count
  [Syndicate] ok 13 - MRSS: media:thumbnail url
  [Syndicate] ok 14 - IT: get-itunes-text returns author
  [Syndicate] ok 15 - IT: get-itunes-text returns summary
  [Syndicate] ok 16 - IT: get-itunes-duration returns duration
  [Syndicate] ok 17 - IT: get-itunes-text on missing returns Str
  [Syndicate] ok 18 - IT: add-itunes-declaration sets xmlns
  [Syndicate] ok 19 - IT: add-itunes-element creates element
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/17-dublin-core.rakutest
  [Syndicate] 1..12
  [Syndicate] ok 1 - Parsed RSS 2.0 with dc:date
  [Syndicate] ok 2 - 3 items parsed
  [Syndicate] ok 3 - item with dc:date only has DateTime updated
  [Syndicate] ok 4 - dc:date year
  [Syndicate] ok 5 - dc:date month
  [Syndicate] ok 6 - dc:date day
  [Syndicate] ok 7 - item with pubDate only has DateTime updated
  [Syndicate] ok 8 - pubDate year
  [Syndicate] ok 9 - item with both has DateTime updated
  [Syndicate] ok 10 - pubDate takes priority over dc:date
  [Syndicate] ok 11 - RSS 0.91 dc:date maps to updated
  [Syndicate] ok 12 - RSS 1.0 dc:date maps to updated
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/18-audit-regressions.rakutest
  [Syndicate] 1..30
  [Syndicate] ok 1 - RSS 1.0 CDATA item kept
  [Syndicate] ok 2 - RSS 1.0 CDATA item title
  [Syndicate] ok 3 - RSS 1.0 dc:subject CDATA captured
  [Syndicate] ok 4 - RSS 1.0 item with raw & < in CDATA kept
  [Syndicate] ok 5 - RSS 1.0 CDATA with raw & and < preserved
  [Syndicate] ok 6 - RSS 2.0 CDATA guid captured
  [Syndicate] ok 7 - RSS 0.91 CDATA skipHours captured
  [Syndicate] ok 8 - RSS 0.91 CDATA skipDays captured
  [Syndicate] ok 9 - media:title CDATA captured
  [Syndicate] ok 10 - media:description CDATA captured
  [Syndicate] ok 11 - itunes:summary CDATA captured
  [Syndicate] ok 12 - Atom CDATA content captured
  [Syndicate] ok 13 - direct Atom construction emits link rel=alternate
  [Syndicate] ok 14 - direct Atom construction emits link href
  [Syndicate] ok 15 - direct Atom construction emits author
  [Syndicate] ok 16 - builder atom output emits link rel=alternate
  [Syndicate] ok 17 - builder atom output emits link href
  [Syndicate] ok 18 - builder atom output emits author
  [Syndicate] ok 19 - JSON Feed numeric dates do not throw
  [Syndicate] ok 20 - numeric date_published ignored, not fatal
  [Syndicate] ok 21 - numeric date_modified ignored, not fatal
  [Syndicate] ok 22 - to-hash deep copy: tags cache intact
  [Syndicate] ok 23 - to-hash deep copy: authors cache intact
  [Syndicate] ok 24 - bare xhtml content wrapped in div
  [Syndicate] ok 25 - already-wrapped xhtml content not double-wrapped
  [Syndicate] ok 26 - multi-div xhtml parse keeps first child
  [Syndicate] ok 27 - multi-div xhtml parse keeps second child
  [Syndicate] ok 28 - multi-div xhtml output keeps first child
  [Syndicate] ok 29 - multi-div xhtml output keeps second child
  [Syndicate] ok 30 - multi-div xhtml roundtrips all children
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/19-followup-audit.rakutest
  [Syndicate] 1..43
  [Syndicate] ok 1 - qualified Syndicate::Parse::parse-feed works
  [Syndicate] ok 2 - qualified parse-feed returns RSS
  [Syndicate] ok 3 - qualified Syndicate::Parse::feed-format works
  [Syndicate] ok 4 - qualified Syndicate::Parse::sanitize-input works
  [Syndicate] ok 5 - qualified Syndicate::Parse::parse-feed-with-format works
  [Syndicate] ok 6 - qualified Syndicate::Parse::parse-file works
  [Syndicate] ok 7 - qualified parse-file returns RSS
  [Syndicate] ok 8 - parse-rss works
  [Syndicate] ok 9 - parse-atom works
  [Syndicate] ok 10 - parse-json works
  [Syndicate] ok 11 - parse-rss1 works
  [Syndicate] ok 12 - parse-rss091 works
  [Syndicate] ok 13 - query-only ref keeps base path
  [Syndicate] ok 14 - fragment-only ref keeps base path
  [Syndicate] ok 15 - empty ref keeps base path
  [Syndicate] ok 16 - to-hash author hash not leaked
  [Syndicate] ok 17 - to-hash item hash not leaked
  [Syndicate] ok 18 - to-hash item tags not leaked
  [Syndicate] ok 19 - MediaRSS feed with non-numeric attrs parses
  [Syndicate] ok 20 - non-numeric fileSize kept as string
  [Syndicate] ok 21 - numeric width parsed as Int
  [Syndicate] ok 22 - non-numeric thumbnail width kept as string
  [Syndicate] ok 23 - SSRF blocked: http://[2002:7f00:1::]/feed
  [Syndicate] ok 24 - SSRF blocked: http://[2002:c0a8:1::]/feed
  [Syndicate] ok 25 - SSRF blocked: http://[2001:0:7f00:1::]/feed
  [Syndicate] ok 26 - SSRF blocked: http://[64:ff9b::7f00:1]/feed
  [Syndicate] ok 27 - SSRF blocked: http://[64:ff9b::c0a8:1]/feed
  [Syndicate] ok 28 - SSRF blocked: http://[::7f00:1]/feed
  [Syndicate] ok 29 - SSRF allowed: http://[2002:0808:0808::]/feed
  [Syndicate] ok 30 - SSRF allowed: http://[64:ff9b::0808:0808]/feed
  [Syndicate] ok 31 - SSRF allowed: http://[2001:db8::abcd]/feed
  [Syndicate] ok 32 - prefix bound to matching namespace-uri is active
  [Syndicate] ok 33 - prefix bound to wrong namespace-uri is inactive
  [Syndicate] ok 34 - unbound canonical prefix is active (lenient feeds)
  [Syndicate] ok 35 - extension registry restored after set-active tests
  [Syndicate] ok 36 - rel tokens other than 'alternate' do not prevent match
  [Syndicate] ok 37 - rel without alternate token excluded
  [Syndicate] ok 38 - empty feed category term skipped
  [Syndicate] ok 39 - empty entry category term skipped
  [Syndicate] ok 40 - no empty term attribute regenerated in output
  [Syndicate] ok 41 - JSONFeed tags must be an array
  [Syndicate] ok 42 - JSONFeed tags elements must be strings
  [Syndicate] ok 43 - valid JSONFeed tags accepted
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/20-rss-common.rakutest
  [Syndicate] 1..16
  [Syndicate] ok 1 - RSS 2.0 parses item count
  [Syndicate] ok 2 - RSS 2.0 XML is cached (same object)
  [Syndicate] ok 3 - RSS 2.0 regenerates dc declaration from item needs
  [Syndicate] ok 4 - RSS 2.0 regenerates media declaration from item needs
  [Syndicate] ok 5 - RSS 2.0 regenerates content declaration from item needs
  [Syndicate] ok 6 - RSS 2.0 new(Str) error uses shared constructor message
  [Syndicate] ok 7 - RSS 0.91 parses item count
  [Syndicate] ok 8 - RSS 0.91 XML is cached (same object)
  [Syndicate] ok 9 - RSS 0.91 regenerates itunes declaration from item needs
  [Syndicate] ok 10 - RSS 0.91 new(Str) error uses shared constructor message
  [Syndicate] ok 11 - RSS 1.0 parses item count
  [Syndicate] ok 12 - RSS 1.0 XML is cached (same object)
  [Syndicate] ok 13 - RSS 1.0 regenerates dc declaration from categories
  [Syndicate] ok 14 - RSS 1.0 shared XML path builds rdf:RDF root
  [Syndicate] ok 15 - RSS 2.0 shared XML path builds rss root
  [Syndicate] ok 16 - RSS 1.0 new(Str) error uses shared constructor message
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/21-entity-roundtrip.rakutest
  [Syndicate] 1..39
  [Syndicate] ok 1 - dc:language parses into language
  [Syndicate] ok 2 - dc:language-only feed regenerates dc declaration
  [Syndicate] ok 3 - dc:language element regenerated
  [Syndicate] ok 4 - MediaRSS url decoded on parse
  [Syndicate] ok 5 - MediaRSS type decoded on parse
  [Syndicate] ok 6 - MediaRSS url single-encoded on generate
  [Syndicate] ok 7 - MediaRSS type single-encoded on generate
  [Syndicate] ok 8 - MediaRSS not double-encoded
  [Syndicate] ok 9 - atom:self href decoded on parse
  [Syndicate] ok 10 - atom:self href single-encoded on generate
  [Syndicate] ok 11 - channel rdf:about decoded on parse
  [Syndicate] ok 12 - item rdf:about decoded on parse
  [Syndicate] ok 13 - image rdf:about decoded on parse
  [Syndicate] ok 14 - channel rdf:about single-encoded on generate
  [Syndicate] ok 15 - item rdf:about single-encoded on generate
  [Syndicate] ok 16 - image rdf:about single-encoded on generate
  [Syndicate] ok 17 - source link href decoded on parse
  [Syndicate] ok 18 - source link href single-encoded on generate
  [Syndicate] ok 19 - feed category term decoded on parse
  [Syndicate] ok 20 - entry category term decoded on parse
  [Syndicate] ok 21 - feed category term single-encoded on generate
  [Syndicate] ok 22 - entry category term single-encoded on generate
  [Syndicate] ok 23 - user-constructed category term encoded on generate
  [Syndicate] ok 24 - link type decoded on parse
  [Syndicate] ok 25 - content type decoded on parse
  [Syndicate] ok 26 - link type single-encoded on generate
  [Syndicate] ok 27 - content type single-encoded on generate
  [Syndicate] ok 28 - empty JSON Feed to-hash includes items key
  [Syndicate] ok 29 - empty JSON Feed items is an empty array
  [Syndicate] ok 30 - empty JSON Feed to-json includes items: []
  [Syndicate] ok 31 - decimal character references decode
  [Syndicate] ok 32 - hexadecimal character references decode
  [Syndicate] ok 33 - encoded numeric reference stays literal (no double decode)
  [Syndicate] ok 34 - numeric reference roundtrips single-encoded
  [Syndicate] ok 35 - unknown named entity stays literal
  [Syndicate] ok 36 - out-of-range numeric reference stays literal
  [Syndicate] ok 37 - numeric references decoded on parse
  [Syndicate] ok 38 - numeric references single-encoded on generate
  [Syndicate] ok 39 - no double-encoded ampersand
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/22-code-quality.rakutest
  [Syndicate] 1..10
  [Syndicate] ok 1 - skipDays normalizes day names
  [Syndicate] ok 2 - invalid skipDays value is skipped
  [Syndicate] ok 3 - all-invalid skipDays yields empty list
  [Syndicate] ok 4 - all-invalid skipDays feeds still parse
  [Syndicate] ok 5 - expired: true accepted
  [Syndicate] ok 6 - expired: false accepted
  [Syndicate] ok 7 - non-Bool expired dies
  [Syndicate] ok 8 - non-Bool expired dies with graceful message
  [Syndicate] ok 9 - rethrow-style constructors still record errors
  [Syndicate] ok 10 - normalized skipDays regenerated
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/23-audit-round-6.rakutest
  [Syndicate] 1..34
  [Syndicate] ok 1 - content:encoded found via URI-bound prefix
  [Syndicate] ok 2 - wrong-URI prefix does not match as content
  [Syndicate] ok 3 - default-namespace encoded element matches
  [Syndicate] ok 4 - space-separated ISO + EST parses
  [Syndicate] ok 5 - EST offset applied
  [Syndicate] ok 6 - space-separated ISO + numeric offset parses
  [Syndicate] ok 7 - numeric offset applied
  [Syndicate] ok 8 - space-separated ISO + colon offset parses
  [Syndicate] ok 9 - space-separated ISO without TZ parses as UTC
  [Syndicate] ok 10 - tz-less datetime treated as UTC
  [Syndicate] ok 11 - RFC 2822 dates still parse
  [Syndicate] ok 12 - RSS pubDate with space-separated ISO parses
  [Syndicate] ok 13 - RSS pubDate space-separated ISO offset applied
  [Syndicate] ok 14 - 0.91 item guid retained in object model
  [Syndicate] ok 15 - 0.91 item comments retained in object model
  [Syndicate] ok 16 - 0.91 item source retained in object model
  [Syndicate] ok 17 - 0.91 item dc:creator author retained in object model
  [Syndicate] ok 18 - 0.91 output omits guid
  [Syndicate] ok 19 - 0.91 output omits comments
  [Syndicate] ok 20 - 0.91 output omits enclosure
  [Syndicate] ok 21 - 0.91 output omits source
  [Syndicate] ok 22 - 0.91 output omits author
  [Syndicate] ok 23 - 0.91 output omits item pubDate
  [Syndicate] ok 24 - 0.91 output omits xmlns:dc declaration
  [Syndicate] ok 25 - 0.91 output omits dc:creator
  [Syndicate] ok 26 - 0.91 item regenerates only title, link, description
  [Syndicate] ok 27 - builder 0.91 item emits only title, link, description
  [Syndicate] ok 28 - builder 0.91 item omits author
  [Syndicate] ok 29 - builder 0.91 item omits comments
  [Syndicate] ok 30 - builder 0.91 item omits source
  [Syndicate] ok 31 - empty xhtml content parses to empty Str
  [Syndicate] ok 32 - empty xhtml content does not record an error
  [Syndicate] ok 33 - Set.new active-ext default still runs generators
  [Syndicate] ok 34 - entries without updated share a single build timestamp
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/24-date-offsets.rakutest
  [Syndicate] 1..43
  [Syndicate] ok 1 - ISO +05:30 parses
  [Syndicate] ok 2 - ISO +05:30 offset applied
  [Syndicate] ok 3 - ISO +05:30 stored as +05:30
  [Syndicate] ok 4 - ISO +0530 parses
  [Syndicate] ok 5 - ISO +0530 offset applied
  [Syndicate] ok 6 - space-separated ISO +05:30 parses
  [Syndicate] ok 7 - space-separated ISO +05:30 offset applied
  [Syndicate] ok 8 - RFC 2822 +0530 parses
  [Syndicate] ok 9 - RFC 2822 +0530 not mangled (was +05:18)
  [Syndicate] ok 10 - RFC 2822 +0530 stored as +05:30
  [Syndicate] ok 11 - RFC 2822 -0330 parses
  [Syndicate] ok 12 - RFC 2822 -0330 not mangled (was -03:18)
  [Syndicate] ok 13 - RFC 2822 -0330 stored as -03:30
  [Syndicate] ok 14 - IST abbreviation parses
  [Syndicate] ok 15 - half-hour abbreviation IST offset applied
  [Syndicate] ok 16 - whole-hour EST still correct
  [Syndicate] ok 17 - whole-hour -0500 still correct
  [Syndicate] ok 18 - explicit Z unaffected
  [Syndicate] ok 19 - Atom feed updated +05:30 applied
  [Syndicate] ok 20 - Atom entry updated +0530 applied
  [Syndicate] ok 21 - RSS pubDate RFC +0530 applied
  [Syndicate] ok 22 - JSON Feed date_published +0530 applied
  [Syndicate] ok 23 - JSON Feed date_modified -0330 applied
  [Syndicate] ok 24 - tz-less T-form parses
  [Syndicate] ok 25 - tz-less T-form treated as UTC
  [Syndicate] ok 26 - tz-less space-separated form parses
  [Syndicate] ok 27 - tz-less space-separated form treated as UTC
  [Syndicate] ok 28 - date-only still parses
  [Syndicate] ok 29 - date-only is midnight UTC
  [Syndicate] ok 30 - invalid ttl not set on feed
  [Syndicate] ok 31 - invalid ttl records no Stats error (optional metadata, feed parses fine)
  [Syndicate] ok 32 - valid ttl parses
  [Syndicate] ok 33 - &nbsp; decodes to non-breaking space
  [Syndicate] ok 34 - &mdash; decodes to em dash
  [Syndicate] ok 35 - &rsquo; decodes to right single quote
  [Syndicate] ok 36 - &ldquo; decodes to left double quote
  [Syndicate] ok 37 - &Aacute; decodes case-sensitively (Á)
  [Syndicate] ok 38 - &aacute; decodes case-sensitively (á)
  [Syndicate] ok 39 - uppercase &AMP; still decodes
  [Syndicate] ok 40 - uppercase &LT; still decodes
  [Syndicate] ok 41 - no double decode of named entities
  [Syndicate] ok 42 - unknown named entity stays literal
  [Syndicate] ok 43 - named entity roundtrips single-encoded
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/25-audit-round-8.rakutest
  [Syndicate] 1..47
  [Syndicate] ok 1 - B1: self-only feed has no $.link (no alternate)
  [Syndicate] ok 2 - B1: output emits no alternate link
  [Syndicate] ok 3 - B1: output keeps the self link
  [Syndicate] ok 4 - B1: self href preserved
  [Syndicate] ok 5 - B1: self link survives roundtrip
  [Syndicate] ok 6 - B2: RSS to-hash has copyright
  [Syndicate] ok 7 - B2: RSS to-hash has ttl
  [Syndicate] ok 8 - B2: RSS to-hash has pubDate
  [Syndicate] ok 9 - B2: RSS to-hash image includes width
  [Syndicate] ok 10 - B2: RSS to-hash has atom-self-link
  [Syndicate] ok 11 - B2: RSS to-hash omits categories when empty
  [Syndicate] ok 12 - B2: item to-hash has guid
  [Syndicate] ok 13 - B2: item to-hash has guid-is-permalink
  [Syndicate] ok 14 - B2: item to-hash has comments
  [Syndicate] ok 15 - B2: item to-hash has enclosure
  [Syndicate] ok 16 - B2: item to-hash has updated (pubDate)
  [Syndicate] ok 17 - B2: Atom to-hash has id
  [Syndicate] ok 18 - B2: Atom to-hash has updated
  [Syndicate] ok 19 - B2: Atom to-hash has subtitle
  [Syndicate] ok 20 - B2: Atom to-hash has icon
  [Syndicate] ok 21 - B2: Atom to-hash has logo
  [Syndicate] ok 22 - B2: Atom to-hash has rights
  [Syndicate] ok 23 - B2: Atom to-hash has author-detail
  [Syndicate] ok 24 - B2: Atom to-hash has contributors
  [Syndicate] ok 25 - B2: Atom to-hash has link-self
  [Syndicate] ok 26 - B2: Atom to-hash has link-alternate
  [Syndicate] ok 27 - B2: Atom item to-hash has content
  [Syndicate] ok 28 - B2: Atom item to-hash has content-type
  [Syndicate] ok 29 - B2: Atom item to-hash has published
  [Syndicate] ok 30 - B2: Atom item to-hash has contributors
  [Syndicate] ok 31 - B2: Atom item to-hash has categories
  [Syndicate] ok 32 - B4: JSON feed served as application/json fetches
  [Syndicate] ok 33 - B4: application/json with charset fetches
  [Syndicate] ok 34 - B5: skipHours keeps in-range hours, drops invalid
  [Syndicate] ok 35 - P2: non-numeric width leaves no key
  [Syndicate] ok 36 - P2: non-numeric height leaves no key
  [Syndicate] ok 37 - P2: other image fields intact
  [Syndicate] ok 38 - Q2: alt-prefix itunes:author parsed at feed level
  [Syndicate] ok 39 - Q2: alt-prefix itunes:summary parsed at feed level
  [Syndicate] ok 40 - Q2: alt-prefix itunes:summary parsed at item level
  [Syndicate] ok 41 - Q2: alt-prefix itunes:duration parsed (extension active)
  [Syndicate] ok 42 - Q2: alt-prefix dc:creator parsed as author
  [Syndicate] ok 43 - Q2: alt-prefix dc:subject parsed
  [Syndicate] ok 44 - Q4: builder feed categories returns a List
  [Syndicate] ok 45 - Q4: builder feed category value present
  [Syndicate] ok 46 - Q6: RSS 1.0 output has no <guid>
  [Syndicate] ok 47 - Q6: RSS 2.0 output still has <guid>
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/26-audit-round-9.rakutest
  [Syndicate] 1..41
  [Syndicate] ok 1 - digit-named entities (frac12/sup2/frac34) decode
  [Syndicate] ok 2 - encoded digit-entity stays literal (no double decode)
  [Syndicate] ok 3 - unknown digit-named entity stays literal
  [Syndicate] ok 4 - RFC 2822 UT offset parses as UTC
  [Syndicate] ok 5 - tz-less RFC 2822 month-name date defaults to UTC
  [Syndicate] ok 6 - tz-less ISO shape still defaults to UTC
  [Syndicate] ok 7 - fragment-only ref keeps base query
  [Syndicate] ok 8 - empty ref keeps base query
  [Syndicate] ok 9 - query-only ref replaces base query
  [Syndicate] ok 10 - path ref drops base query
  [Syndicate] ok 11 - RSS 1.0 dc:subject via declared alt prefix
  [Syndicate] ok 12 - RSS 1.0 dc:subject via undeclared canonical prefix
  [Syndicate] ok 13 - undeclared itunes:author parsed at item level
  [Syndicate] ok 14 - undeclared itunes:duration parsed at item level
  [Syndicate] ok 15 - undeclared dc:creator parsed at item level
  [Syndicate] ok 16 - canonical prefix bound to wrong URI stays inactive
  [Syndicate] ok 17 - bare xhtml child normalized to div-wrapped form at parse
  [Syndicate] ok 18 - bare xhtml parse->regen->reparse is byte-stable
  [Syndicate] ok 19 - single xhtml div kept as-is at parse
  [Syndicate] ok 20 - div xhtml parse->regen->reparse is byte-stable
  [Syndicate] ok 21 - multi-div xhtml keeps all children at parse
  [Syndicate] ok 22 - parse-feed-or-nil returns parsed feed
  [Syndicate] ok 23 - parse-feed-or-nil returns Nil for HTML
  [Syndicate] ok 24 - parse-feed-or-nil returns Nil for garbage
  [Syndicate] ok 25 - parse-feed-or-nil records no error for non-feed input
  [Syndicate] ok 26 - items cache: author nested hash intact
  [Syndicate] ok 27 - items cache: tags array intact
  [Syndicate] ok 28 - items cache: author container replace isolated
  [Syndicate] ok 29 - items cache: tags container replace isolated
  [Syndicate] ok 30 - feed built without its own updated
  [Syndicate] ok 31 - Atom to-hash includes computed (entry-max) updated when feed updated unset
  [Syndicate] ok 32 - Atom XML emits the same computed updated
  [Syndicate] ok 33 - parse-file missing path raises friendly error
  [Syndicate] ok 34 - no per-item note() left in V0_91.rakumod
  [Syndicate] ok 35 - no per-item note() left in V1_0.rakumod
  [Syndicate] ok 36 - no per-item note() left in RSS.rakumod
  [Syndicate] ok 37 - extension callback failures are not noted
  [Syndicate] ok 38 - extension error counter retained
  [Syndicate] ok 39 - extension errors recorded in stats
  [Syndicate] ok 40 - no extension callback-failure notes remain
  [Syndicate] ok 41 - atom:link rel=self still parsed after redundant-check removal
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/27-audit-round-10.rakutest
  [Syndicate] 1..41
  [Syndicate] ok 1 - path+query ref replaces query
  [Syndicate] ok 2 - path+fragment ref drops base query
  [Syndicate] ok 3 - dot-relative ref
  [Syndicate] ok 4 - parent-relative ref
  [Syndicate] ok 5 - alt prefix bound to MRSS URI parses as media:content
  [Syndicate] ok 6 - undeclared canonical media: prefix parses leniently
  [Syndicate] ok 7 - prefix bound to a wrong URI is never media:content
  [Syndicate] ok 8 - author preserved from parse
  [Syndicate] ok 9 - dc:creator values stored
  [Syndicate] ok 10 - dc:creator regenerated
  [Syndicate] ok 11 - author preserved through round-trip
  [Syndicate] ok 12 - dc:subject values stored
  [Syndicate] ok 13 - dc:subject 1 regenerated
  [Syndicate] ok 14 - dc:subject 2 regenerated
  [Syndicate] ok 15 - xmlns:dc declared for subject-only item
  [Syndicate] ok 16 - dc:subject survives round-trip
  [Syndicate] ok 17 - plain <language> parsed as $.language
  [Syndicate] ok 18 - language regenerates as dc:language
  [Syndicate] ok 19 - xmlns:dc declared for dc:language
  [Syndicate] ok 20 - second to-hash unaffected by title mutation
  [Syndicate] ok 21 - second to-hash unaffected by nested media mutation
  [Syndicate] ok 22 - mutation visible only in first result
  [Syndicate] ok 23 - third to-hash still pristine
  [Syndicate] ok 24 - failing extension parse is counted
  [Syndicate] ok 25 - failing extension parse is not noted to STDERR
  [Syndicate] ok 26 - missing semicolon tolerated
  [Syndicate] ok 27 - bare &amp decodes
  [Syndicate] ok 28 - bare digit-named entity decodes
  [Syndicate] ok 29 - encoded entity stays literal
  [Syndicate] ok 30 - greedy unknown name stays literal
  [Syndicate] ok 31 - ampersand without &name untouched
  [Syndicate] ok 32 - ampersand mid-word untouched
  [Syndicate] ok 33 - name terminated by space decodes
  [Syndicate] ok 34 - RSS 0.91 item dies without description
  [Syndicate] ok 35 - RSS 2.0 item dies without link
  [Syndicate] ok 36 - RSS 2.0 item dies without title
  [Syndicate] ok 37 - RSS 1.0 item dies without link
  [Syndicate] ok 38 - Atom item dies without title
  [Syndicate] ok 39 - JSON Feed item dies without title
  [Syndicate] ok 40 - RSS 2.0 title error message
  [Syndicate] ok 41 - RSS 2.0 link error message
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/28-audit-round-11.rakutest
  [Syndicate] 1..60
  [Syndicate] ok 1 - B1: wrong-URI and bare unprefixed dc:subject rejected; URI-bound/default-ns matched
  [Syndicate] ok 2 - B1: exactly the namespace-correct dc:subject elements match
  [Syndicate] ok 3 - B1: media:content bound to a foreign URI is not media
  [Syndicate] ok 4 - B1: undeclared canonical media:thumbnail still matches (lenient)
  [Syndicate] ok 5 - B2: get-text-by-ns sees a prefix declared on the child element itself
  [Syndicate] ok 6 - B1: get-text-by-ns skips children bound to a wrong URI
  [Syndicate] ok 7 - B2: RSS item content:encoded picked up via child-declared prefix
  [Syndicate] ok 8 - B1: RSS item ignores content:encoded bound to a wrong URI
  [Syndicate] ok 9 - B1: RSS 1.0 parses with foreign-URI dc prefix
  [Syndicate] ok 10 - B1: wrong-URI dc:subject is not a channel category
  [Syndicate] ok 11 - B1: wrong-URI dc:language is ignored
  [Syndicate] ok 12 - B1 control: correct dc:subject becomes a category
  [Syndicate] ok 13 - B1 control: category value
  [Syndicate] ok 14 - B1 control: correct dc:language maps to language
  [Syndicate] ok 15 - B5: Atom feed parses despite one invalid entry
  [Syndicate] ok 16 - B5: valid entries retained, invalid skipped
  [Syndicate] ok 17 - B5: exactly one error recorded for the skipped entry
  [Syndicate] ok 18 - B6: has-dc-date flag set from parsed dc:date
  [Syndicate] ok 19 - B6: regenerated RSS 2.0 emits pubDate
  [Syndicate] ok 20 - B6: regenerated RSS 2.0 keeps dc:date
  [Syndicate] ok 21 - B6: single dc:date, no duplicate
  [Syndicate] ok 22 - B6: dc namespace declared on regeneration
  [Syndicate] ok 23 - B6: builder RSS 2.0 emits pubDate
  [Syndicate] ok 24 - B6: builder RSS 2.0 emits no dc:date
  [Syndicate] ok 25 - B6: builder RSS 2.0 emits no dc namespace
  [Syndicate] ok 26 - B6: RSS 1.0 dc:date regenerates exactly once
  [Syndicate] ok 27 - B6: RSS 1.0 emits no pubDate
  [Syndicate] ok 28 - B6: RSS 1.0 dc namespace declared on regeneration
  [Syndicate] ok 29 - B3: mutating image in to-hash leaves the feed alone
  [Syndicate] ok 30 - B3: second to-hash is not corrupted
  [Syndicate] ok 31 - B3: Atom link-self not shared with to-hash
  [Syndicate] ok 32 - B3: Atom link-alternate not shared with to-hash
  [Syndicate] ok 33 - B3: Atom contributors not shared with to-hash
  [Syndicate] ok 34 - B3: second Atom to-hash is clean
  [Syndicate] ok 35 - B3: second Atom to-hash keeps contributors
  [Syndicate] ok 36 - B3: RSS 1.0 image not shared with to-hash
  [Syndicate] ok 37 - B4: no undefined values anywhere in RSS 2.0 to-hash
  [Syndicate] ok 38 - B4: absent enclosure length has no key (no null)
  [Syndicate] ok 39 - B4: enclosure url preserved
  [Syndicate] ok 40 - B4: RSS 2.0 to-json has no null
  [Syndicate] ok 41 - B4: to-json keeps enclosure url
  [Syndicate] ok 42 - B4: no undefined values in Atom to-hash
  [Syndicate] ok 43 - B4: absent author email has no key
  [Syndicate] ok 44 - B4: absent author uri has no key
  [Syndicate] ok 45 - B4: author name preserved
  [Syndicate] ok 46 - B4: Atom to-json has no null
  [Syndicate] ok 47 - B4: absent image description has no key
  [Syndicate] ok 48 - B4: image hash free of undefined values
  [Syndicate] ok 49 - B4: image-less-description to-json has no null
  [Syndicate] ok 50 - B7: image about is parsed
  [Syndicate] ok 51 - B7: degenerate image regenerates no dangling reference
  [Syndicate] ok 52 - B7 control: spec-correct image emits reference + element
  [Syndicate] ok 53 - sanitize keeps defined scalars
  [Syndicate] ok 54 - sanitize drops undefined scalars
  [Syndicate] ok 55 - sanitize recurses into hashes
  [Syndicate] ok 56 - sanitize keeps nested defined values
  [Syndicate] ok 57 - sanitize recurses into arrays
  [Syndicate] ok 58 - sanitize drops undefined array-element keys
  [Syndicate] ok 59 - sanitize output has no undefined values
  [Syndicate] ok 60 - sanitize returns a fresh clone
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/29-audit-round-12.rakutest
  [Syndicate] 1..26
  [Syndicate] ok 1 - B1: V0_91 mutating image in to-hash leaves the feed alone
  [Syndicate] ok 2 - B1: V0_91 mutating skipHours in to-hash leaves the feed alone
  [Syndicate] ok 3 - B1: V0_91 mutating skipDays in to-hash leaves the feed alone
  [Syndicate] ok 4 - B2: Atom mutating categories in to-hash leaves the feed alone
  [Syndicate] ok 5 - B2: Atom entry categories round-trip unchanged
  [Syndicate] ok 6 - B3: builder item declares xmlns:content
  [Syndicate] ok 7 - B3: builder item emits content:encoded
  [Syndicate] ok 8 - B3: builder item declares xmlns:media
  [Syndicate] ok 9 - B3: builder item declares xmlns:itunes
  [Syndicate] ok 10 - B3: feed-embedded items stay byte-identical (no item-level xmlns)
  [Syndicate] ok 11 - B4: V1_0 direct construction emits dc:date (not pubDate)
  [Syndicate] ok 12 - B4: V1_0 direct construction emits no pubDate
  [Syndicate] ok 13 - B4: V0_91 direct construction emits no content:encoded
  [Syndicate] ok 14 - B4: V0_91 direct construction emits no pubDate
  [Syndicate] ok 15 - B4: V0_91 direct construction emits description
  [Syndicate] ok 16 - Q4: dc-only V1_0 builder item declares xmlns:dc
  [Syndicate] ok 17 - Q4: plain V1_0 builder item declares no namespaces
  [Syndicate] ok 18 - Q2: Atom to-hash updated matches XML updated
  [Syndicate] ok 19 - Q2: computed updated is the newest entry timestamp
  [Syndicate] ok 20 - Q3: media duration is Str
  [Syndicate] ok 21 - Q3: media fileSize is Str
  [Syndicate] ok 22 - Q3: media width is Str
  [Syndicate] ok 23 - Q3: media duration value preserved
  [Syndicate] ok 24 - P1: default to-hash deep-clones item hashes
  [Syndicate] ok 25 - P1: to-hash(:!clone) shares the cached item hashes (opt-out)
  [Syndicate] ok 26 - P1: feed item object itself is never mutated
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/30-audit-round-13.rakutest
  [Syndicate] 1..13
  [Syndicate] ok 1 - B1: to-hash uses the newest entry updated when it beats the feed updated
  [Syndicate] ok 2 - B1: to-hash updated matches XML updated when an entry is newer
  [Syndicate] ok 3 - B1: to-hash keeps the feed updated when it beats all entries
  [Syndicate] ok 4 - B2: standalone V1_0 item declares xmlns:rdf
  [Syndicate] ok 5 - B2: standalone V1_0 item emits rdf:about
  [Syndicate] ok 6 - B2: V1_0 item without about declares no namespaces
  [Syndicate] ok 7 - B2: builder V1_0 feed item still carries rdf:about
  [Syndicate] ok 8 - B2: builder V1_0 feed item stays namespace-bare (root declares rdf)
  [Syndicate] ok 9 - B3: foreign-namespace link rel=self is not captured
  [Syndicate] ok 10 - B3: foreign link is not re-emitted as atom:link
  [Syndicate] ok 11 - B3: atom-namespaced link rel=self is still parsed
  [Syndicate] ok 12 - B3: atom:link rel=self with empty href is not captured
  [Syndicate] ok 13 - B3: no empty atom:link is emitted
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/31-audit-round-14.rakutest
  [Syndicate] 1..38
  [Syndicate] ok 1 - R1: RSS 2.0 keeps all items despite bad item dates
  [Syndicate] ok 2 - R1: good item pubDate parsed
  [Syndicate] ok 3 - R1: bad pubDate item degrades to Nil
  [Syndicate] ok 4 - R1: structurally-invalid ISO date degrades to Nil
  [Syndicate] ok 5 - R1: bad channel pubDate degrades to Nil
  [Syndicate] ok 6 - R1: feed still parses with bad channel pubDate
  [Syndicate] ok 7 - R1: RSS 2.0 item with bad dc:date still parses
  [Syndicate] ok 8 - R1: bad dc:date degrades to Nil
  [Syndicate] ok 9 - R1: RSS 0.91 item with bad dc:date still parses
  [Syndicate] ok 10 - R1: 0.91 bad dc:date degrades to Nil
  [Syndicate] ok 11 - R1: RSS 1.0 item with bad dc:date still parses
  [Syndicate] ok 12 - R1: 1.0 bad dc:date degrades to Nil
  [Syndicate] ok 13 - R1: JSON Feed with bad item dates still parses
  [Syndicate] ok 14 - R1: bad date_published degrades to Nil
  [Syndicate] ok 15 - R1: bad date_modified degrades to Nil
  [Syndicate] ok 16 - R1: Atom skips entry with bad updated, keeps good one
  [Syndicate] ok 17 - R1: surviving Atom entry is the good one
  [Syndicate] ok 18 - R1: one error recorded for skipped entry
  [Syndicate] ok 19 - R1: Atom feed with bad feed-level updated still parses
  [Syndicate] ok 20 - R1: bad feed-level updated falls back to the entry timestamp
  [Syndicate] ok 21 - R1: timestamp-less Atom feed parses
  [Syndicate] ok 22 - R1: rendering a timestamp-less feed fails gracefully
  [Syndicate] ok 23 - R1: graceful message, not X::Temporal::OutOfRange
  [Syndicate] ok 24 - R3: non-Str title rejected
  [Syndicate] ok 25 - R3: graceful type message for title
  [Syndicate] ok 26 - R3: non-Str version rejected
  [Syndicate] ok 27 - R3: graceful type message for version
  [Syndicate] ok 28 - R3: non-Str item id rejected
  [Syndicate] ok 29 - R3: graceful type message for item id
  [Syndicate] ok 30 - R4: decimal ref without ; decodes
  [Syndicate] ok 31 - R4: decimal ref with ; still decodes
  [Syndicate] ok 32 - R4: hex ref without ; decodes
  [Syndicate] ok 33 - R4: named ref without ; still decodes
  [Syndicate] ok 34 - R4: entity-free text untouched
  [Syndicate] ok 35 - R5: rss091-feed without description fails
  [Syndicate] ok 36 - R5: failure names the missing description
  [Syndicate] ok 37 - R5: rss091-feed with description succeeds
  [Syndicate] ok 38 - R2: concurrent to-hash calls all return valid hashes
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/32-audit-round-15.rakutest
  [Syndicate] 1..28
  [Syndicate] ok 1 - R1: high surrogate stays literal
  [Syndicate] ok 2 - R1: low surrogate stays literal
  [Syndicate] ok 3 - R1: decimal surrogate stays literal
  [Syndicate] ok 4 - R1: max valid codepoint decodes
  [Syndicate] ok 5 - R1: out-of-range codepoint stays literal
  [Syndicate] ok 6 - R1: normal refs still decode
  [Syndicate] ok 7 - R1: feed with a surrogate ref keeps it as literal text
  [Syndicate] ok 8 - R1: to-hash string is UTF-8-encodable
  [Syndicate] ok 9 - R1: item text is UTF-8-encodable
  [Syndicate] ok 10 - R1: sibling item decoded normally
  [Syndicate] ok 11 - R2: no feed-level updated stored
  [Syndicate] ok 12 - R2: to-hash computes the newest entry updated
  [Syndicate] ok 13 - R2: XML emits the computed updated
  [Syndicate] ok 14 - R2: fully timestamp-less feed has no updated in to-hash
  [Syndicate] ok 15 - R2: rendering a fully timestamp-less feed fails
  [Syndicate] ok 16 - R2: failure is the documented graceful die
  [Syndicate] ok 17 - R3: Content-Type with space before ; accepted
  [Syndicate] ok 18 - R3: text/html with parameters still rejected
  [Syndicate] ok 19 - R4: space-separated HH:MM parses as midnight-second
  [Syndicate] ok 20 - R4: space-separated HH:MM with offset parses
  [Syndicate] ok 21 - R4: RFC 2822 date-only parses as midnight UTC
  [Syndicate] ok 22 - R4: HH:MM:SS form unchanged
  [Syndicate] ok 23 - R4: full RFC 2822 unchanged
  [Syndicate] ok 24 - R4: bare ISO date unchanged
  [Syndicate] ok 25 - R5: parse-feed-or-nil parses JSON Feed
  [Syndicate] ok 26 - R5: JSON Feed increments feeds-parsed
  [Syndicate] ok 27 - R5: non-feed records nothing
  [Syndicate] ok 28 - R5: non-feed did not increment feeds-parsed
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/33-audit-round-16.rakutest
  [Syndicate] 1..66
  [Syndicate] ok 1 - 2a: valueless <base href> yields no URL, no crash
  [Syndicate] ok 2 - 2a: valued <base href> still returned
  [Syndicate] ok 3 - 8: non-string home_page_url rejected
  [Syndicate] ok 4 - 8: home_page_url error names the field
  [Syndicate] ok 5 - 8: non-string description rejected
  [Syndicate] ok 6 - 8: description error names the field
  [Syndicate] ok 7 - 8: non-string generator rejected
  [Syndicate] ok 8 - 8: generator error names the field
  [Syndicate] ok 9 - 8: non-string feed_url rejected
  [Syndicate] ok 10 - 8: feed_url error names the field
  [Syndicate] ok 11 - 8: non-string user_comment rejected
  [Syndicate] ok 12 - 8: user_comment error names the field
  [Syndicate] ok 13 - 8: non-string next_url rejected
  [Syndicate] ok 14 - 8: next_url error names the field
  [Syndicate] ok 15 - 8: non-string icon rejected
  [Syndicate] ok 16 - 8: icon error names the field
  [Syndicate] ok 17 - 8: non-string favicon rejected
  [Syndicate] ok 18 - 8: favicon error names the field
  [Syndicate] ok 19 - 8: non-string locale rejected
  [Syndicate] ok 20 - 8: locale error names the field
  [Syndicate] ok 21 - 8: non-string language rejected when no locale
  [Syndicate] ok 22 - 8: language error names the field
  [Syndicate] ok 23 - 8: language used when locale absent
  [Syndicate] ok 24 - 8: feed_url parsed
  [Syndicate] ok 25 - 4: capital-X hex reference decodes
  [Syndicate] ok 26 - 4: lowercase-x hex reference still decodes
  [Syndicate] ok 27 - 4: surrogate hex reference stays literal
  [Syndicate] ok 28 - 4: decimal reference still decodes
  [Syndicate] ok 29 - 6: feed-format(0.0.92) is RSS2
  [Syndicate] ok 30 - 6: parse-feed accepts 0.92
  [Syndicate] ok 31 - 6: feed-format(0.0.93) is RSS2
  [Syndicate] ok 32 - 6: parse-feed accepts 0.93
  [Syndicate] ok 33 - 6: feed-format(0.0.94) is RSS2
  [Syndicate] ok 34 - 6: parse-feed accepts 0.94
  [Syndicate] ok 35 - 6: all three legacy versions accepted
  [Syndicate] ok 36 - 7: feed-format rejects empty suffix
  [Syndicate] ok 37 - 7: parse-feed-or-nil returns Nil for empty suffix
  [Syndicate] ok 38 - 7: proper version still detected
  [Syndicate] ok 39 - 9: dc-creators alone triggers the xmlns:dc declaration
  [Syndicate] ok 40 - 5: undeclared canonical prefix still matches
  [Syndicate] ok 41 - 5: no false positive when a different URI is actually bound
  [Syndicate] ok 42 - 11: invalid ttl not set on feed
  [Syndicate] ok 43 - 11: invalid ttl records no Stats error
  [Syndicate] ok 44 - 3: Atom element-form markup preserved
  [Syndicate] ok 45 - 3: Atom content flagged as markup
  [Syndicate] ok 46 - 3: Atom markup round-trip is byte-stable
  [Syndicate] ok 47 - 3: RSS element-form markup preserved
  [Syndicate] ok 48 - 3: RSS markup content stable across parse/regen/reparse
  [Syndicate] ok 49 - 3: RSS entity+element content decoded to markup
  [Syndicate] ok 50 - 3: RSS mixed content stable across parse/regen/reparse
  [Syndicate] ok 51 - 3: RSS inter-element whitespace stable across parse/regen/reparse
  [Syndicate] ok 52 - 3: entity-encoded content still decoded to plain text
  [Syndicate] ok 53 - 3: entity-encoded content stable (no double encoding)
  [Syndicate] ok 54 - 3: V1_0 element-form markup preserved
  [Syndicate] ok 55 - 3: V1_0 markup content stable across parse/regen/reparse
  [Syndicate] ok 56 - 13: title parsed
  [Syndicate] ok 57 - 13: link parsed
  [Syndicate] ok 58 - 13: description parsed
  [Syndicate] ok 59 - 13: author parsed
  [Syndicate] ok 60 - 13: both categories parsed
  [Syndicate] ok 61 - 13: comments parsed
  [Syndicate] ok 62 - 13: source parsed
  [Syndicate] ok 63 - 13: pubDate parsed
  [Syndicate] ok 64 - 13: guid parsed
  [Syndicate] ok 65 - 13: enclosure parsed
  [Syndicate] ok 66 - 13: content:encoded parsed
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/34-audit-round-17.rakutest
  [Syndicate] 1..56
  [Syndicate] ok 1 - 1: «Wed, 1 Jan 2020 00:00:00 UT» parses
  [Syndicate] ok 2 - 1: «Tue, 2 Feb 2021 12:00:00 GMT» parses
  [Syndicate] ok 3 - 1: «Wed, 1 Jan 2020 00:00:00 GMT» parses
  [Syndicate] ok 4 - 1: «Wed, 01 Jan 2020 10:00 +0000» parses
  [Syndicate] ok 5 - 1: «Sun, 08 Jul 2026 10:00:00+0000» parses
  [Syndicate] ok 6 - 1: «15 Jan 2024» parses
  [Syndicate] ok 7 - 1: «Mon, 15 Jan 2024 8:30:00 GMT» parses
  [Syndicate] ok 8 - 1: «Mon, 15 Jan 2024 8:30 AM EST» parses
  [Syndicate] ok 9 - 1: «Mon, 15 Jan 2024 10:00:00 +05:30» parses
  [Syndicate] ok 10 - 1: synthesized weekday is correct (15 Jan 2024 is a Monday)
  [Syndicate] ok 11 - 1: synthesized weekday is correct (29 Feb 2024 is a Thursday)
  [Syndicate] ok 12 - 1: bogus day still Nil
  [Syndicate] ok 13 - 1: bogus month-day still Nil
  [Syndicate] ok 14 - 1: space-separated ISO unaffected
  [Syndicate] ok 15 - 1: T-separated ISO with colon offset unaffected
  [Syndicate] ok 16 - 2: non-string url rejected
  [Syndicate] ok 17 - 2: url error is graceful and names the field
  [Syndicate] ok 18 - 2: non-string summary rejected
  [Syndicate] ok 19 - 2: summary error is graceful and names the field
  [Syndicate] ok 20 - 2: non-string content_html rejected
  [Syndicate] ok 21 - 2: content_html error is graceful and names the field
  [Syndicate] ok 22 - 2: non-string content_text rejected
  [Syndicate] ok 23 - 2: content_text error is graceful and names the field
  [Syndicate] ok 24 - 2: non-string external_url rejected
  [Syndicate] ok 25 - 2: external_url error is graceful and names the field
  [Syndicate] ok 26 - 2: non-string image rejected
  [Syndicate] ok 27 - 2: image error is graceful and names the field
  [Syndicate] ok 28 - 2: non-string banner_image rejected
  [Syndicate] ok 29 - 2: banner_image error is graceful and names the field
  [Syndicate] ok 30 - 2: non-string title rejected
  [Syndicate] ok 31 - 2: title error names the field
  [Syndicate] ok 32 - 2: non-string id rejected
  [Syndicate] ok 33 - 2: id falls back to url
  [Syndicate] ok 34 - 2: parse-feed propagates the graceful die
  [Syndicate] ok 35 - 2: parse-feed surfaces the graceful message, not X::TypeCheck
  [Syndicate] ok 36 - 2: parse-feed records the error
  [Syndicate] ok 37 - 5: RSS item to-hash has no active-ext key
  [Syndicate] ok 38 - 5: extension data still present
  [Syndicate] ok 39 - 5: item JSON is clean of active-ext
  [Syndicate] ok 40 - 6: good result
  [Syndicate] ok 41 - 6: good feeds-parsed delta
  [Syndicate] ok 42 - 6: good errors delta
  [Syndicate] ok 43 - 6: nochan result
  [Syndicate] ok 44 - 6: nochan feeds-parsed delta
  [Syndicate] ok 45 - 6: nochan errors delta
  [Syndicate] ok 46 - 6: html result
  [Syndicate] ok 47 - 6: html feeds-parsed delta
  [Syndicate] ok 48 - 6: html errors delta
  [Syndicate] ok 49 - V0_91: title
  [Syndicate] ok 50 - V0_91: link
  [Syndicate] ok 51 - V0_91: description
  [Syndicate] ok 52 - V0_91: guid -> id
  [Syndicate] ok 53 - V0_91: comments
  [Syndicate] ok 54 - V0_91: source
  [Syndicate] ok 55 - date_modified: parse path round-trips date_modified
  [Syndicate] ok 56 - date_modified: builder item with only updated emits no date_modified
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/35-convert.rakutest
  [Syndicate] 1..195
  [Syndicate] ok 1 - rss: title mapped
  [Syndicate] ok 2 - rss: link mapped
  [Syndicate] ok 3 - rss: description mapped
  [Syndicate] ok 4 - rss: copyright -> rights
  [Syndicate] ok 5 - rss: managingEditor -> author email
  [Syndicate] ok 6 - rss: lastBuildDate -> updated
  [Syndicate] ok 7 - rss: one entry
  [Syndicate] ok 8 - rss item: title
  [Syndicate] ok 9 - rss item: link
  [Syndicate] ok 10 - rss item: summary
  [Syndicate] ok 11 - rss item: guid -> id
  [Syndicate] ok 12 - rss item: author
  [Syndicate] ok 13 - rss item: categories
  [Syndicate] ok 14 - rss item: enclosure
  [Syndicate] ok 15 - rss item: content
  [Syndicate] ok 16 - rss091: title mapped
  [Syndicate] ok 17 - rss091: link mapped
  [Syndicate] ok 18 - rss091: description mapped
  [Syndicate] ok 19 - rss091: copyright -> rights
  [Syndicate] ok 20 - rss091: managingEditor -> author email
  [Syndicate] ok 21 - rss091: lastBuildDate -> updated
  [Syndicate] ok 22 - rss091: one entry
  [Syndicate] ok 23 - rss091 item: title
  [Syndicate] ok 24 - rss091 item: link
  [Syndicate] ok 25 - rss091 item: summary
  [Syndicate] ok 26 - rss091 item: id falls back to link
  [Syndicate] ok 27 - rss1: title mapped
  [Syndicate] ok 28 - rss1: link mapped
  [Syndicate] ok 29 - rss1: description mapped
  [Syndicate] ok 30 - rss1: about -> id
  [Syndicate] ok 31 - rss1: dc:subject -> feed categories
  [Syndicate] ok 32 - rss1: one entry
  [Syndicate] ok 33 - rss1 item: title
  [Syndicate] ok 34 - rss1 item: link
  [Syndicate] ok 35 - rss1 item: summary
  [Syndicate] ok 36 - rss1 item: about -> id
  [Syndicate] ok 37 - rss1 item: dc:date -> updated
  [Syndicate] ok 38 - rss1 item: dc:creator -> author
  [Syndicate] ok 39 - atom: title mapped
  [Syndicate] ok 40 - atom: primary alternate -> link
  [Syndicate] ok 41 - atom: subtitle -> description
  [Syndicate] ok 42 - atom: id mapped
  [Syndicate] ok 43 - atom: rights mapped
  [Syndicate] ok 44 - atom: icon mapped
  [Syndicate] ok 45 - atom: logo mapped
  [Syndicate] ok 46 - atom: updated mapped
  [Syndicate] ok 47 - atom: author name
  [Syndicate] ok 48 - atom: author email
  [Syndicate] ok 49 - atom: author uri
  [Syndicate] ok 50 - atom: feed categories
  [Syndicate] ok 51 - atom: link-self -> atom-self-link
  [Syndicate] ok 52 - atom: one entry
  [Syndicate] ok 53 - atom item: title
  [Syndicate] ok 54 - atom item: link
  [Syndicate] ok 55 - atom item: summary
  [Syndicate] ok 56 - atom item: id
  [Syndicate] ok 57 - atom item: content
  [Syndicate] ok 58 - atom item: published
  [Syndicate] ok 59 - atom item: author name
  [Syndicate] ok 60 - atom item: categories
  [Syndicate] ok 61 - json: title mapped
  [Syndicate] ok 62 - json: home_page_url -> link
  [Syndicate] ok 63 - json: description mapped
  [Syndicate] ok 64 - json: feed_url mapped
  [Syndicate] ok 65 - json: version mapped
  [Syndicate] ok 66 - json: icon mapped
  [Syndicate] ok 67 - json: author name
  [Syndicate] ok 68 - json: author url -> uri
  [Syndicate] ok 69 - json: one entry
  [Syndicate] ok 70 - json item: title
  [Syndicate] ok 71 - json item: url -> link
  [Syndicate] ok 72 - json item: summary
  [Syndicate] ok 73 - json item: id
  [Syndicate] ok 74 - json item: date_published -> published
  [Syndicate] ok 75 - json item: date_modified -> updated
  [Syndicate] ok 76 - json item: content_html -> content
  [Syndicate] ok 77 - json item: authors[0] -> author
  [Syndicate] ok 78 - json item: tags -> categories
  [Syndicate] ok 79 - rss -> RSS2: feed title survives
  [Syndicate] ok 80 - rss -> RSS2: has items
  [Syndicate] ok 81 - rss -> RSS2: first item title
  [Syndicate] ok 82 - rss -> RSS091: feed title survives
  [Syndicate] ok 83 - rss -> RSS091: has items
  [Syndicate] ok 84 - rss -> RSS091: first item title
  [Syndicate] ok 85 - rss -> RSS1: feed title survives
  [Syndicate] ok 86 - rss -> RSS1: has items
  [Syndicate] ok 87 - rss -> RSS1: first item title
  [Syndicate] ok 88 - rss -> Atom: feed title survives
  [Syndicate] ok 89 - rss -> Atom: has items
  [Syndicate] ok 90 - rss -> Atom: first item title
  [Syndicate] ok 91 - rss -> JSONFeedFmt: feed title survives
  [Syndicate] ok 92 - rss -> JSONFeedFmt: has items
  [Syndicate] ok 93 - rss -> JSONFeedFmt: first item title
  [Syndicate] ok 94 - atom -> RSS2: feed title survives
  [Syndicate] ok 95 - atom -> RSS2: has items
  [Syndicate] ok 96 - atom -> RSS2: first item title
  [Syndicate] ok 97 - atom -> RSS091: feed title survives
  [Syndicate] ok 98 - atom -> RSS091: has items
  [Syndicate] ok 99 - atom -> RSS091: first item title
  [Syndicate] ok 100 - atom -> RSS1: feed title survives
  [Syndicate] ok 101 - atom -> RSS1: has items
  [Syndicate] ok 102 - atom -> RSS1: first item title
  [Syndicate] ok 103 - atom -> Atom: feed title survives
  [Syndicate] ok 104 - atom -> Atom: has items
  [Syndicate] ok 105 - atom -> Atom: first item title
  [Syndicate] ok 106 - atom -> JSONFeedFmt: feed title survives
  [Syndicate] ok 107 - atom -> JSONFeedFmt: has items
  [Syndicate] ok 108 - atom -> JSONFeedFmt: first item title
  [Syndicate] ok 109 - rss091 -> RSS2: feed title survives
  [Syndicate] ok 110 - rss091 -> RSS2: has items
  [Syndicate] ok 111 - rss091 -> RSS2: first item title
  [Syndicate] ok 112 - rss091 -> RSS091: feed title survives
  [Syndicate] ok 113 - rss091 -> RSS091: has items
  [Syndicate] ok 114 - rss091 -> RSS091: first item title
  [Syndicate] ok 115 - rss091 -> RSS1: feed title survives
  [Syndicate] ok 116 - rss091 -> RSS1: has items
  [Syndicate] ok 117 - rss091 -> RSS1: first item title
  [Syndicate] ok 118 - rss091 -> Atom: feed title survives
  [Syndicate] ok 119 - rss091 -> Atom: has items
  [Syndicate] ok 120 - rss091 -> Atom: first item title
  [Syndicate] ok 121 - rss091 -> JSONFeedFmt: feed title survives
  [Syndicate] ok 122 - rss091 -> JSONFeedFmt: has items
  [Syndicate] ok 123 - rss091 -> JSONFeedFmt: first item title
  [Syndicate] ok 124 - rss1 -> RSS2: feed title survives
  [Syndicate] ok 125 - rss1 -> RSS2: has items
  [Syndicate] ok 126 - rss1 -> RSS2: first item title
  [Syndicate] ok 127 - rss1 -> RSS091: feed title survives
  [Syndicate] ok 128 - rss1 -> RSS091: has items
  [Syndicate] ok 129 - rss1 -> RSS091: first item title
  [Syndicate] ok 130 - rss1 -> RSS1: feed title survives
  [Syndicate] ok 131 - rss1 -> RSS1: has items
  [Syndicate] ok 132 - rss1 -> RSS1: first item title
  [Syndicate] ok 133 - rss1 -> Atom: feed title survives
  [Syndicate] ok 134 - rss1 -> Atom: has items
  [Syndicate] ok 135 - rss1 -> Atom: first item title
  [Syndicate] ok 136 - rss1 -> JSONFeedFmt: feed title survives
  [Syndicate] ok 137 - rss1 -> JSONFeedFmt: has items
  [Syndicate] ok 138 - rss1 -> JSONFeedFmt: first item title
  [Syndicate] ok 139 - json -> RSS2: feed title survives
  [Syndicate] ok 140 - json -> RSS2: has items
  [Syndicate] ok 141 - json -> RSS2: first item title
  [Syndicate] ok 142 - json -> RSS091: feed title survives
  [Syndicate] ok 143 - json -> RSS091: has items
  [Syndicate] ok 144 - json -> RSS091: first item title
  [Syndicate] ok 145 - json -> RSS1: feed title survives
  [Syndicate] ok 146 - json -> RSS1: has items
  [Syndicate] ok 147 - json -> RSS1: first item title
  [Syndicate] ok 148 - json -> Atom: feed title survives
  [Syndicate] ok 149 - json -> Atom: has items
  [Syndicate] ok 150 - json -> Atom: first item title
  [Syndicate] ok 151 - json -> JSONFeedFmt: feed title survives
  [Syndicate] ok 152 - json -> JSONFeedFmt: has items
  [Syndicate] ok 153 - json -> JSONFeedFmt: first item title
  [Syndicate] ok 154 - rss->atom: lastBuildDate -> feed updated
  [Syndicate] ok 155 - rss->atom: item pubDate -> entry updated
  [Syndicate] ok 156 - rss->atom: managingEditor -> author email
  [Syndicate] ok 157 - atom->rss: entry updated -> pubDate
  [Syndicate] ok 158 - atom->rss: feed updated -> lastBuildDate
  [Syndicate] ok 159 - atom->rss: author email -> managingEditor
  [Syndicate] ok 160 - atom->rss: feed categories survive
  [Syndicate] ok 161 - json->atom: content_html -> type=html
  [Syndicate] ok 162 - json->atom: tags -> category
  [Syndicate] ok 163 - json->atom: date_modified -> updated
  [Syndicate] ok 164 - json->atom: date_published -> published
  [Syndicate] ok 165 - json->rss: date_modified -> pubDate
  [Syndicate] ok 166 - json->rss: authors[0] name -> author
  [Syndicate] ok 167 - json->rss: tags -> category
  [Syndicate] ok 168 - json->rss: content_html -> content:encoded
  [Syndicate] ok 169 - rss->json: content:encoded -> content_html
  [Syndicate] ok 170 - rss->json: author -> authors[0]
  [Syndicate] ok 171 - rss->json: category -> tags
  [Syndicate] ok 172 - rss1->rss: dc:subject -> feed categories
  [Syndicate] ok 173 - rss1->rss: dc:creator -> item author
  [Syndicate] ok 174 - string target format is rejected (enum coercion fails)
  [Syndicate] ok 175 - coercion error names FeedFormat
  [Syndicate] ok 176 - enum target format accepted
  [Syndicate] ok 177 - atom without link -> rss dies
  [Syndicate] ok 178 - missing link error is clear
  [Syndicate] ok 179 - atom without subtitle -> rss dies
  [Syndicate] ok 180 - missing description error is clear
  [Syndicate] ok 181 - item without summary -> rss091 dies
  [Syndicate] ok 182 - missing item summary error is clear
  [Syndicate] ok 183 - enum RSS2 accepted
  [Syndicate] ok 184 - enum RSS1 accepted
  [Syndicate] ok 185 - enum RSS091 accepted
  [Syndicate] ok 186 - convert-to-rss emits RSS
  [Syndicate] ok 187 - convert-to-atom emits Atom
  [Syndicate] ok 188 - convert-to-json emits JSON
  [Syndicate] ok 189 - convert-to-rss1 emits RSS 1.0
  [Syndicate] Warning: RSS 0.91 does not support feed-level categories; 1 categories dropped
  [Syndicate]   in method rss091-feed at /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6/lib/Syndicate/Builder/Feed.rakumod (Syndicate::Builder::Feed) line 308
  [Syndicate] ok 190 - convert-to-rss091 emits RSS 0.91
  [Syndicate] ok 191 - convert-to-json result reparses
  [Syndicate] ok 192 - convert-to-atom result reparses
  [Syndicate] ok 193 - instance call returns a populated builder
  [Syndicate] ok 194 - instance call populates the receiver
  [Syndicate] ok 195 - type-object call creates a populated builder
  ===> Testing [OK] for Syndicate:ver<0.0.6>:auth<zef:sasha>
  ===> Installing: Syndicate:ver<0.0.6>:auth<zef:sasha>
  ===> Install [OK] for Syndicate:ver<0.0.6>:auth<zef:sasha>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 6min 484ms
               CPU time consumed: 6min 26.877s
                     Memory peak: 2.4G (swap: 284.4M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p281556-i310041.service; invocation ID: 3e31331af3244c1b9b9b9e94b19d3a2e
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Syndicate
  ===> Found: Syndicate:ver<0.0.6>:auth<zef:sasha> [via Zef::Repository::Ecosystems<fez>]
  [Syndicate] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788472695.281557.9643.675905510336/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz https://360.zef.pm/S/YN/SYNDICATE/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz
  ===> Fetching [OK]: Syndicate:ver<0.0.6>:auth<zef:sasha> to /home/coke/sandbox/blin/data/zef-data/tmp/1788472695.281557.9643.675905510336/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz
  [Syndicate] Command: tar -t -f ./37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz
  [Syndicate] Command: tar -xvf ./37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz -C ../37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz
  ===> Extraction [OK]: Syndicate to /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz
  ===> Testing: Syndicate:ver<0.0.6>:auth<zef:sasha>
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/00-basic.rakutest
  [Syndicate] 1..10
  [Syndicate] ok 1 - Syndicate module can be use-d ok
  [Syndicate] ok 2 - RSS::Item generates XML
  [Syndicate] ok 3 - RSS::Item Str contains item tag
  [Syndicate] ok 4 - RSS feed generates XML
  [Syndicate] ok 5 - RSS feed Str contains rss tag
  [Syndicate] ok 6 - RSS feed contains channel tag
  [Syndicate] ok 7 - RSS feed contains title text
  [Syndicate] ok 8 - RSS feed contains item tag
  [Syndicate] ok 9 - RSS::Item.new(Str) parses item XML
  [Syndicate] ok 10 - RSS::Item.new(Str) title
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/01-roundtrip.rakutest
  [Syndicate] 1..18
  [Syndicate] ok 1 - RSS output encodes & in title
  [Syndicate] ok 2 - RSS output encodes <> in title
  [Syndicate] ok 3 - RSS output encodes & in link
  [Syndicate] ok 4 - RSS output encodes <> in description
  [Syndicate] ok 5 - RSS output encodes item title
  [Syndicate] ok 6 - RSS entity roundtrip title
  [Syndicate] ok 7 - RSS entity roundtrip item title
  [Syndicate] ok 8 - RSS roundtrip item count
  [Syndicate] ok 9 - Atom self-link type preserved in output
  [Syndicate] ok 10 - Atom roundtrip title
  [Syndicate] ok 11 - Atom self-link type roundtrips
  [Syndicate] ok 12 - Atom roundtrip item count
  [Syndicate] ok 13 - RSS 0.91 roundtrip title
  [Syndicate] ok 14 - RSS 0.91 image roundtrip
  [Syndicate] ok 15 - RSS 0.91 textInput roundtrip
  [Syndicate] ok 16 - RSS 0.91 skipHours count
  [Syndicate] ok 17 - RSS 0.91 skipDays count
  [Syndicate] ok 18 - RSS 0.91 item count
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/02-parse.rakutest
  [Syndicate] 1..38
  [Syndicate] ok 1 - atom-full.xml detected as Atom
  [Syndicate] ok 2 - rss2-full.xml detected as RSS2
  [Syndicate] ok 3 - rss091-full.xml detected as RSS091
  [Syndicate] ok 4 - RSS without version -> RSS2
  [Syndicate] ok 5 - RSS version="2.0" -> RSS2
  [Syndicate] ok 6 - RSS version="0.91" -> RSS091
  [Syndicate] ok 7 - bare Atom -> Atom
  [Syndicate] ok 8 - jsonfeed-full.json detected as JSONFeedFmt
  [Syndicate] ok 9 - bare JSON -> JSONFeedFmt
  [Syndicate] ok 10 - parse-feed json returns JSONFeed
  [Syndicate] ok 11 - parse-feed atom returns Atom
  [Syndicate] ok 12 - parse-feed rss2 returns RSS
  [Syndicate] ok 13 - parse-feed rss091 returns V0_91
  [Syndicate] ok 14 - parse() atom returns Atom
  [Syndicate] ok 15 - parse() rss2 returns RSS
  [Syndicate] ok 16 - parse() rss091 returns V0_91
  [Syndicate] ok 17 - parse() json returns JSONFeed
  [Syndicate] ok 18 - parse() atom title
  [Syndicate] ok 19 - parse() rss2 title
  [Syndicate] ok 20 - parse() rss091 title
  [Syndicate] ok 21 - parse() json title
  [Syndicate] ok 22 - rss1-full.xml detected as RSS1
  [Syndicate] ok 23 - bare RSS1 -> RSS1
  [Syndicate] ok 24 - parse-feed rss1 returns V1_0
  [Syndicate] ok 25 - parse() rss1 returns V1_0
  [Syndicate] ok 26 - parse() rss1 title
  [Syndicate] ok 27 - empty string dies
  [Syndicate] ok 28 - whitespace-only dies
  [Syndicate] ok 29 - non-XML dies
  [Syndicate] ok 30 - unknown root element dies
  [Syndicate] ok 31 - feed-format is exported
  [Syndicate] ok 32 - parse-feed is exported
  [Syndicate] ok 33 - parse is exported from Syndicate
  [Syndicate] ok 34 - parse-file atom
  [Syndicate] ok 35 - parse-file rss2
  [Syndicate] ok 36 - parse-file rss1
  [Syndicate] ok 37 - parse-file jsonfeed IO::Path
  [Syndicate] ok 38 - parse-file nonexistent file dies
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/03-rss-parse.rakutest
  [Syndicate] 1..20
  [Syndicate] ok 1 - Parsed RSS 2.0 feed
  [Syndicate] ok 2 - Does Syndicate::Feed role
  [Syndicate] ok 3 - channel title
  [Syndicate] ok 4 - channel link
  [Syndicate] ok 5 - channel description
  [Syndicate] ok 6 - channel language
  [Syndicate] ok 7 - channel copyright
  [Syndicate] ok 8 - channel managingEditor
  [Syndicate] ok 9 - channel webMaster
  [Syndicate] ok 10 - channel category
  [Syndicate] ok 11 - channel generator
  [Syndicate] ok 12 - channel docs
  [Syndicate] ok 13 - channel ttl
  [Syndicate] ok 14 - pubDate is DateTime
  [Syndicate] ok 15 - pubDate year
  [Syndicate] ok 16 - pubDate month
  [Syndicate] ok 17 - pubDate day
  [Syndicate] ok 18 - dc:creator feed has 1 item
  [Syndicate] not ok 19 - dc:creator maps to author
  [Syndicate] # Failed test 'dc:creator maps to author'
  [Syndicate] # at t/03-rss-parse.rakutest line 47
  [Syndicate] # expected: 'Jane Writer'
  [Syndicate] #      got: (Str)
  [Syndicate] ok 20 - dc:creator item title preserved
  [Syndicate] # You failed 1 test of 20
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/04-rss091-parse.rakutest
  [Syndicate] 1..59
  [Syndicate] ok 1 - Parsed RSS 0.91 feed
  [Syndicate] ok 2 - Does Syndicate::Feed role
  [Syndicate] ok 3 - channel title
  [Syndicate] ok 4 - channel link
  [Syndicate] ok 5 - channel description
  [Syndicate] ok 6 - channel language
  [Syndicate] ok 7 - channel rating
  [Syndicate] ok 8 - channel copyright
  [Syndicate] ok 9 - channel managingEditor
  [Syndicate] ok 10 - channel webMaster
  [Syndicate] ok 11 - channel docs
  [Syndicate] ok 12 - pubDate is DateTime
  [Syndicate] ok 13 - pubDate year
  [Syndicate] ok 14 - pubDate month
  [Syndicate] ok 15 - pubDate day
  [Syndicate] ok 16 - lastBuildDate is DateTime
  [Syndicate] ok 17 - lastBuildDate year
  [Syndicate] ok 18 - image exists
  [Syndicate] ok 19 - image title
  [Syndicate] ok 20 - image url
  [Syndicate] ok 21 - image link
  [Syndicate] ok 22 - image width
  [Syndicate] ok 23 - image height
  [Syndicate] ok 24 - image description
  [Syndicate] ok 25 - textInput exists
  [Syndicate] ok 26 - textInput title
  [Syndicate] ok 27 - textInput description
  [Syndicate] ok 28 - textInput name
  [Syndicate] ok 29 - textInput link
  [Syndicate] ok 30 - skipHours count
  [Syndicate] ok 31 - skipHours first hour
  [Syndicate] ok 32 - skipHours second hour
  [Syndicate] ok 33 - skipDays count
  [Syndicate] ok 34 - skipDays first day
  [Syndicate] ok 35 - skipDays second day
  [Syndicate] ok 36 - item count
  [Syndicate] ok 37 - first item is V0_91::Item
  [Syndicate] ok 38 - first item title
  [Syndicate] ok 39 - first item link
  [Syndicate] ok 40 - first item description
  [Syndicate] ok 41 - second item title
  [Syndicate] ok 42 - second item link
  [Syndicate] ok 43 - second item description
  [Syndicate] ok 44 - third item title
  [Syndicate] ok 45 - third item description
  [Syndicate] ok 46 - items missing title/link/description are skipped
  [Syndicate] ok 47 - valid item still parsed
  [Syndicate] ok 48 - roundtrip title
  [Syndicate] ok 49 - roundtrip link
  [Syndicate] ok 50 - roundtrip description
  [Syndicate] ok 51 - roundtrip item count
  [Syndicate] ok 52 - roundtrip item title
  [Syndicate] ok 53 - roundtrip pubDate is DateTime
  [Syndicate] ok 54 - XML has rss root
  [Syndicate] ok 55 - XML has channel
  [Syndicate] ok 56 - XML has skipHours
  [Syndicate] ok 57 - XML has textInput
  [Syndicate] ok 58 - XML has image
  [Syndicate] ok 59 - XML has items
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/05-rss1-parse.rakutest
  [Syndicate] 1..32
  [Syndicate] ok 1 - Parsed RSS 1.0 feed
  [Syndicate] ok 2 - Does Syndicate::Feed role
  [Syndicate] ok 3 - channel title
  [Syndicate] ok 4 - channel link
  [Syndicate] ok 5 - channel description
  [Syndicate] ok 6 - channel about
  [Syndicate] ok 7 - image url
  [Syndicate] ok 8 - image title
  [Syndicate] ok 9 - image link
  [Syndicate] ok 10 - image about
  [Syndicate] ok 11 - two items
  [Syndicate] ok 12 - item is correct type
  [Syndicate] ok 13 - item 0 title
  [Syndicate] ok 14 - item 0 link
  [Syndicate] ok 15 - item 0 summary
  [Syndicate] ok 16 - item 0 about
  [Syndicate] ok 17 - item 1 title
  [Syndicate] ok 18 - item 1 link
  [Syndicate] ok 19 - Str roundtrip
  [Syndicate] ok 20 - roundtrip title matches
  [Syndicate] ok 21 - dc feed has 2 items
  [Syndicate] not ok 22 - dc:creator maps to author
  [Syndicate] ok 23 - dc:date maps to DateTime
  [Syndicate] # Failed test 'dc:creator maps to author'
  [Syndicate] # at t/05-rss1-parse.rakutest line 43
  [Syndicate] # expected: 'Alice Author'
  [Syndicate] #      got: (Str)
  [Syndicate] Cannot look up attributes in a DateTime type object. Did you forget a '.new'?
  [Syndicate]   in block <unit> at t/05-rss1-parse.rakutest line 45
  [Syndicate] # You planned 32 tests, but ran 23
  [Syndicate] # You failed 1 test of 23
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/06-atom-parse.rakutest
  [Syndicate] 1..55
  [Syndicate] ok 1 - Parsed Atom 1.0 feed
  [Syndicate] ok 2 - Does Syndicate::Feed role
  [Syndicate] ok 3 - feed title
  [Syndicate] ok 4 - feed id
  [Syndicate] ok 5 - feed subtitle
  [Syndicate] ok 6 - feed rights
  [Syndicate] ok 7 - feed generator
  [Syndicate] ok 8 - feed icon
  [Syndicate] ok 9 - feed logo
  [Syndicate] ok 10 - updated is DateTime
  [Syndicate] ok 11 - updated year
  [Syndicate] ok 12 - feed link (alternate)
  [Syndicate] ok 13 - feed link-self href
  [Syndicate] ok 14 - feed link-alternate href
  [Syndicate] ok 15 - feed author-detail name defined
  [Syndicate] ok 16 - feed author-detail name
  [Syndicate] ok 17 - feed author-detail email
  [Syndicate] ok 18 - feed author-detail uri
  [Syndicate] ok 19 - two categories
  [Syndicate] ok 20 - first category
  [Syndicate] ok 21 - second category
  [Syndicate] ok 22 - two entries
  [Syndicate] ok 23 - entry is Atom::Item
  [Syndicate] ok 24 - entry title
  [Syndicate] ok 25 - entry link
  [Syndicate] ok 26 - entry id
  [Syndicate] ok 27 - entry summary
  [Syndicate] ok 28 - entry content
  [Syndicate] ok 29 - entry content-type
  [Syndicate] ok 30 - entry published is DateTime
  [Syndicate] ok 31 - entry updated is DateTime
  [Syndicate] ok 32 - entry rights
  [Syndicate] ok 33 - entry author name
  [Syndicate] ok 34 - entry author email
  [Syndicate] ok 35 - entry has one category
  [Syndicate] ok 36 - entry category term
  [Syndicate] ok 37 - entry has one contributor
  [Syndicate] ok 38 - entry contributor name
  [Syndicate] ok 39 - entry source-feed title defined
  [Syndicate] ok 40 - entry source-feed title
  [Syndicate] ok 41 - entry source-feed link
  [Syndicate] ok 42 - entry source-feed updated is DateTime
  [Syndicate] ok 43 - roundtrip title
  [Syndicate] ok 44 - roundtrip rights
  [Syndicate] ok 45 - roundtrip generator
  [Syndicate] ok 46 - roundtrip icon
  [Syndicate] ok 47 - roundtrip logo
  [Syndicate] ok 48 - roundtrip author name
  [Syndicate] ok 49 - roundtrip 2 categories
  [Syndicate] ok 50 - roundtrip 2 entries
  [Syndicate] ok 51 - roundtrip entry title
  [Syndicate] ok 52 - roundtrip entry content
  [Syndicate] ok 53 - roundtrip entry content-type
  [Syndicate] ok 54 - roundtrip entry 1 category
  [Syndicate] ok 55 - roundtrip entry 1 contributor
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/07-jsonfeed-parse.rakutest
  [Syndicate] 1..63
  [Syndicate] ok 1 - Parsed JSON Feed
  [Syndicate] ok 2 - Does Syndicate::Feed role
  [Syndicate] ok 3 - feed title
  [Syndicate] ok 4 - feed link (home_page_url)
  [Syndicate] ok 5 - feed description
  [Syndicate] ok 6 - feed feed_url
  [Syndicate] ok 7 - feed user_comment
  [Syndicate] ok 8 - feed next_url
  [Syndicate] ok 9 - feed icon
  [Syndicate] ok 10 - feed favicon
  [Syndicate] ok 11 - feed language
  [Syndicate] ok 12 - feed expired is Bool
  [Syndicate] ok 13 - feed expired is false
  [Syndicate] ok 14 - feed author name
  [Syndicate] ok 15 - feed author url
  [Syndicate] ok 16 - feed author avatar
  [Syndicate] ok 17 - two entries
  [Syndicate] ok 18 - entry is JSONFeed::Item
  [Syndicate] ok 19 - entry title
  [Syndicate] ok 20 - entry link (url)
  [Syndicate] ok 21 - entry id
  [Syndicate] ok 22 - entry external_url
  [Syndicate] ok 23 - entry summary
  [Syndicate] ok 24 - entry content_html
  [Syndicate] ok 25 - entry content_text
  [Syndicate] ok 26 - entry image
  [Syndicate] ok 27 - entry banner_image
  [Syndicate] ok 28 - entry date_published is DateTime
  [Syndicate] ok 29 - entry date_published year
  [Syndicate] ok 30 - entry date_modified is DateTime
  [Syndicate] ok 31 - entry date_modified year
  [Syndicate] ok 32 - entry has one author
  [Syndicate] ok 33 - entry author name
  [Syndicate] ok 34 - entry author url
  [Syndicate] ok 35 - entry author avatar
  [Syndicate] ok 36 - entry has 2 tags
  [Syndicate] ok 37 - entry first tag
  [Syndicate] ok 38 - entry second tag
  [Syndicate] ok 39 - entry2 title
  [Syndicate] ok 40 - entry2 link
  [Syndicate] ok 41 - entry2 id
  [Syndicate] ok 42 - entry2 external_url is undefined
  [Syndicate] ok 43 - entry2 content_html is undefined
  [Syndicate] ok 44 - entry2 date_published is undefined
  [Syndicate] ok 45 - entry2 date_modified is DateTime
  [Syndicate] ok 46 - entry2 date_modified year
  [Syndicate] ok 47 - entry2 has no authors
  [Syndicate] ok 48 - entry2 has no tags
  [Syndicate] ok 49 - roundtrip title
  [Syndicate] ok 50 - roundtrip link
  [Syndicate] ok 51 - roundtrip description
  [Syndicate] ok 52 - roundtrip feed_url
  [Syndicate] ok 53 - roundtrip icon
  [Syndicate] ok 54 - roundtrip favicon
  [Syndicate] ok 55 - roundtrip language
  [Syndicate] ok 56 - roundtrip author name
  [Syndicate] ok 57 - roundtrip 2 entries
  [Syndicate] ok 58 - roundtrip entry1 title
  [Syndicate] ok 59 - roundtrip entry1 content_html
  [Syndicate] ok 60 - roundtrip entry1 2 tags
  [Syndicate] ok 61 - roundtrip entry1 1 author
  [Syndicate] ok 62 - roundtrip entry2 title
  [Syndicate] ok 63 - Str roundtrip lives
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/08-builder.rakutest
  [Syndicate] 1..140
  [Syndicate] ok 1 - Feed builder created
  [Syndicate] ok 2 - feed title get/set
  [Syndicate] ok 3 - feed link get/set
  [Syndicate] ok 4 - feed description get/set
  [Syndicate] ok 5 - feed id get/set
  [Syndicate] ok 6 - feed language get/set
  [Syndicate] ok 7 - feed rights get/set
  [Syndicate] ok 8 - feed generator get/set
  [Syndicate] ok 9 - feed icon get/set
  [Syndicate] ok 10 - feed logo get/set
  [Syndicate] ok 11 - feed author name
  [Syndicate] ok 12 - feed author email
  [Syndicate] ok 13 - feed has 2 categories
  [Syndicate] ok 14 - default generator value
  [Syndicate] ok 15 - entry created via add-entry
  [Syndicate] ok 16 - entry title get/set
  [Syndicate] ok 17 - entry link get/set
  [Syndicate] ok 18 - entry summary get/set
  [Syndicate] ok 19 - entry id get/set
  [Syndicate] ok 20 - entry updated is defined
  [Syndicate] ok 21 - feed has 2 entries
  [Syndicate] ok 22 - entry content get/set
  [Syndicate] ok 23 - rss-str generates output
  [Syndicate] ok 24 - RSS output has rss root
  [Syndicate] ok 25 - RSS output has channel
  [Syndicate] ok 26 - RSS output has feed title
  [Syndicate] ok 27 - RSS output has language
  [Syndicate] ok 28 - RSS output has copyright
  [Syndicate] ok 29 - RSS output has managingEditor
  [Syndicate] ok 30 - RSS output has generator
  [Syndicate] ok 31 - RSS output has items
  [Syndicate] ok 32 - atom-str generates output
  [Syndicate] ok 33 - Atom output has feed root
  [Syndicate] ok 34 - Atom output has feed title
  [Syndicate] ok 35 - Atom output has feed id
  [Syndicate] ok 36 - Atom output has subtitle
  [Syndicate] ok 37 - Atom output has author email (from entry)
  [Syndicate] ok 38 - Atom output has entries
  [Syndicate] ok 39 - Atom output has rights
  [Syndicate] ok 40 - Atom output has generator
  [Syndicate] ok 41 - Atom output has icon
  [Syndicate] ok 42 - Atom output has logo
  [Syndicate] ok 43 - Atom output has category
  [Syndicate] ok 44 - Atom output has second category
  [Syndicate] ok 45 - RSS roundtrip parsed
  [Syndicate] ok 46 - RSS roundtrip title
  [Syndicate] ok 47 - RSS roundtrip link
  [Syndicate] ok 48 - RSS roundtrip description
  [Syndicate] ok 49 - RSS roundtrip language
  [Syndicate] ok 50 - RSS roundtrip copyright
  [Syndicate] ok 51 - RSS roundtrip item count
  [Syndicate] ok 52 - RSS roundtrip first item title
  [Syndicate] ok 53 - RSS roundtrip second item title
  [Syndicate] ok 54 - RSS roundtrip pubDate is DateTime
  [Syndicate] ok 55 - Atom roundtrip parsed
  [Syndicate] ok 56 - Atom roundtrip title
  [Syndicate] ok 57 - Atom roundtrip id
  [Syndicate] ok 58 - Atom roundtrip subtitle
  [Syndicate] ok 59 - Atom roundtrip rights
  [Syndicate] ok 60 - Atom roundtrip generator
  [Syndicate] ok 61 - Atom roundtrip icon
  [Syndicate] ok 62 - Atom roundtrip logo
  [Syndicate] ok 63 - Atom roundtrip author name
  [Syndicate] ok 64 - Atom roundtrip author email
  [Syndicate] ok 65 - Atom roundtrip 2 categories
  [Syndicate] ok 66 - Atom roundtrip entry count
  [Syndicate] ok 67 - Atom roundtrip first entry title
  [Syndicate] ok 68 - Atom roundtrip second entry title
  [Syndicate] ok 69 - Atom roundtrip updated is DateTime
  [Syndicate] ok 70 - Atom output has content with type
  [Syndicate] ok 71 - Atom output has XHTML content body
  [Syndicate] ok 72 - content roundtrip body (RFC 4287 xhtml div wrapper)
  [Syndicate] ok 73 - content roundtrip type
  [Syndicate] ok 74 - empty RSS has root
  [Syndicate] ok 75 - empty RSS has title
  [Syndicate] ok 76 - empty Atom has root
  [Syndicate] ok 77 - empty Atom has title
  [Syndicate] ok 78 - rss091-str generates output
  [Syndicate] ok 79 - RSS 0.91 output has version 0.91
  [Syndicate] ok 80 - RSS 0.91 output has channel
  [Syndicate] ok 81 - RSS 0.91 output has feed title
  [Syndicate] ok 82 - RSS 0.91 output has language
  [Syndicate] ok 83 - RSS 0.91 output has copyright
  [Syndicate] ok 84 - RSS 0.91 output has managingEditor
  [Syndicate] ok 85 - RSS 0.91 output has items
  [Syndicate] ok 86 - rss091-feed returns V0_91
  [Syndicate] ok 87 - RSS 0.91 roundtrip parsed
  [Syndicate] ok 88 - RSS 0.91 roundtrip title
  [Syndicate] ok 89 - RSS 0.91 roundtrip link
  [Syndicate] ok 90 - RSS 0.91 roundtrip description
  [Syndicate] ok 91 - RSS 0.91 roundtrip language
  [Syndicate] ok 92 - RSS 0.91 roundtrip copyright
  [Syndicate] ok 93 - RSS 0.91 roundtrip item count
  [Syndicate] ok 94 - RSS 0.91 roundtrip first item title
  [Syndicate] ok 95 - RSS 0.91 roundtrip first item link
  [Syndicate] ok 96 - RSS 0.91 roundtrip first item description
  [Syndicate] ok 97 - empty RSS 0.91 has root
  [Syndicate] ok 98 - empty RSS 0.91 has title
  [Syndicate] ok 99 - rss1-str generates output
  [Syndicate] ok 100 - RSS 1.0 output has rdf:RDF root
  [Syndicate] ok 101 - RSS 1.0 output has channel
  [Syndicate] ok 102 - RSS 1.0 output has feed title
  [Syndicate] ok 103 - RSS 1.0 output has items
  [Syndicate] ok 104 - rss1-feed returns V1_0
  [Syndicate] ok 105 - RSS 1.0 roundtrip parsed
  [Syndicate] ok 106 - RSS 1.0 roundtrip title
  [Syndicate] ok 107 - RSS 1.0 roundtrip link
  [Syndicate] ok 108 - RSS 1.0 roundtrip description
  [Syndicate] ok 109 - RSS 1.0 roundtrip item count
  [Syndicate] ok 110 - RSS 1.0 roundtrip first item title
  [Syndicate] ok 111 - RSS 1.0 roundtrip first item link
  [Syndicate] ok 112 - RSS 1.0 roundtrip first item summary
  [Syndicate] not ok 113 - RSS 1.0 roundtrip first item author (dc:creator)
  [Syndicate] # Failed test 'RSS 1.0 roundtrip first item author (dc:creator)'
  [Syndicate] # at t/08-builder.rakutest line 242
  [Syndicate] # expected: 'Jane'
  [Syndicate] #      got: (Str)
  [Syndicate] ok 114 - RSS 1.0 output omits non-standard <author>
  [Syndicate] ok 115 - RSS 1.0 output omits non-standard <category>
  [Syndicate] not ok 116 - RSS 1.0 output carries author as dc:creator
  [Syndicate] # Failed test 'RSS 1.0 output carries author as dc:creator'
  [Syndicate] # at t/08-builder.rakutest line 248
  [Syndicate] # expected a match with: /'<dc:creator>Jane</dc:creator>'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rdf:RDF xmlns:dc=\"http://purl.org/dc/elements/1.1/\" xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns#\" xmlns=\"http://purl.org/rss/1.0/\"><channel rdf:about=\"http://example.com/feed\"><title>Test Builder Feed</title><link>http://example.com</link><description>A feed built with the builder API</description><generator>Syndicate Test</generator><dc:language>en</dc:language><dc:subject>Tech</dc:subject><dc:subject>News</dc:subject><items><rdf:Seq><rdf:li rdf:resource=\"urn:uuid:1111-1111\"/><rdf:li rdf:resource=\"urn:uuid:2222-2222\"/></rdf:Seq></items></channel><item rdf:about=\"urn:uuid:1111-1111\"><title>Entry One</title><link>http://example.com/1</link><description>First entry summary</description></item><item rdf:about=\"urn:uuid:2222-2222\"><title>Entry Two</title><link>http://example.com/2</link><description>Second entry</description></item></rdf:RDF>"
  [Syndicate] # Failed test 'RSS 1.0 output carries category as dc:subject'
  [Syndicate] # at t/08-builder.rakutest line 249
  [Syndicate] not ok 117 - RSS 1.0 output carries category as dc:subject
  [Syndicate] # expected a match with: /'<dc:subject>atom</dc:subject>'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rdf:RDF xmlns:dc=\"http://purl.org/dc/elements/1.1/\" xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns#\" xmlns=\"http://purl.org/rss/1.0/\"><channel rdf:about=\"http://example.com/feed\"><title>Test Builder Feed</title><link>http://example.com</link><description>A feed built with the builder API</description><generator>Syndicate Test</generator><dc:language>en</dc:language><dc:subject>Tech</dc:subject><dc:subject>News</dc:subject><items><rdf:Seq><rdf:li rdf:resource=\"urn:uuid:1111-1111\"/><rdf:li rdf:resource=\"urn:uuid:2222-2222\"/></rdf:Seq></items></channel><item rdf:about=\"urn:uuid:1111-1111\"><title>Entry One</title><link>http://example.com/1</link><description>First entry summary</description></item><item rdf:about=\"urn:uuid:2222-2222\"><title>Entry Two</title><link>http://example.com/2</link><description>Second entry</description></item></rdf:RDF>"
  [Syndicate] not ok 118 - RSS 1.0 dc:subject roundtrip
  [Syndicate] ok 119 - empty RSS 1.0 has root
  [Syndicate] ok 120 - empty RSS 1.0 has title
  [Syndicate] ok 121 - json-str generates output
  [Syndicate] ok 122 - json-str output is valid JSON
  [Syndicate] ok 123 - JSON output has feed title
  [Syndicate] ok 124 - JSON output has 2 items
  [Syndicate] ok 125 - JSON roundtrip parsed
  [Syndicate] ok 126 - JSON roundtrip title
  [Syndicate] ok 127 - JSON roundtrip item count
  [Syndicate] ok 128 - JSON roundtrip first item title
  [Syndicate] ok 129 - RSS 1.0 builder output declares xmlns:dc
  [Syndicate] not ok 130 - RSS 1.0 builder output has dc:creator
  [Syndicate] ok 131 - RSS builder output declares xmlns:content
  [Syndicate] ok 132 - RSS builder output has content:encoded
  [Syndicate] ok 133 - RSS 1.0 builder output has no pubDate
  [Syndicate] ok 134 - RSS 1.0 builder output has dc:date
  [Syndicate] # Failed test 'RSS 1.0 dc:subject roundtrip'
  [Syndicate] # at t/08-builder.rakutest line 250
  [Syndicate] # expected: 'atom'
  [Syndicate] #      got: ''
  [Syndicate] # Failed test 'RSS 1.0 builder output has dc:creator'
  [Syndicate] # at t/08-builder.rakutest line 291
  [Syndicate] # expected a match with: /'<dc:creator>Jane</dc:creator>'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rdf:RDF xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns#\" xmlns:dc=\"http://purl.org/dc/elements/1.1/\" xmlns=\"http://purl.org/rss/1.0/\"><channel rdf:about=\"http://example.com/needs\"><title>Needs Test</title><link>http://example.com/needs</link><description>Needs test</description><generator>Syndicate</generator><items><rdf:Seq><rdf:li rdf:resource=\"http://example.com/needs/1\"/></rdf:Seq></items></channel><item rdf:about=\"http://example.com/needs/1\"><title>Item</title><link>http://example.com/needs/1</link></item></rdf:RDF>"
  [Syndicate] Cannot look up attributes in a DateTime type object. Did you forget a '.new'?
  [Syndicate]   in block <unit> at t/08-builder.rakutest line 319
  [Syndicate] # You planned 140 tests, but ran 134
  [Syndicate] # You failed 5 tests of 134
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/09-discovery.rakutest
  [Syndicate] 1..61
  [Syndicate] ok 1 - absolute URL unchanged
  [Syndicate] ok 2 - root-relative URL
  [Syndicate] ok 3 - relative URL with trailing slash
  [Syndicate] ok 4 - relative URL without trailing slash
  [Syndicate] ok 5 - root-relative URL with path base
  [Syndicate] ok 6 - different origin https URL
  [Syndicate] ok 7 - protocol-relative URL
  [Syndicate] ok 8 - extract <base href>
  [Syndicate] ok 9 - no <base> tag returns Str
  [Syndicate] ok 10 - single-quoted base href
  [Syndicate] ok 11 - found 2 feed links
  [Syndicate] ok 12 - first feed is RSS
  [Syndicate] ok 13 - second feed is Atom
  [Syndicate] ok 14 - no feeds found when none present
  [Syndicate] ok 15 - found JSON feed link
  [Syndicate] ok 16 - JSON feed URL
  [Syndicate] ok 17 - found feed in multi-line HTML
  [Syndicate] ok 18 - multi-line feed URL
  [Syndicate] ok 19 - found feed with base href
  [Syndicate] ok 20 - base href affects URL resolution
  [Syndicate] ok 21 - found HTTPS feed link
  [Syndicate] ok 22 - HTTPS feed URL preserved
  [Syndicate] ok 23 - no feeds when rel is not alternate
  [Syndicate] ok 24 - single-quoted attributes work
  [Syndicate] ok 25 - single-quoted href
  [Syndicate] ok 26 - SSRF blocked: http://127.0.0.1/feed
  [Syndicate] ok 27 - SSRF blocked: http://127.1/feed
  [Syndicate] ok 28 - SSRF blocked: http://0x7f.1/feed
  [Syndicate] ok 29 - SSRF blocked: http://0177.0.0.1/feed
  [Syndicate] ok 30 - SSRF blocked: http://127.0.0.01/feed
  [Syndicate] ok 31 - SSRF blocked: http://0.0.0.0/feed
  [Syndicate] ok 32 - SSRF blocked: http://10.0.0.1/feed
  [Syndicate] ok 33 - SSRF blocked: http://192.168.1.1/feed
  [Syndicate] ok 34 - SSRF blocked: http://172.16.0.1/feed
  [Syndicate] ok 35 - SSRF blocked: http://169.254.0.1/feed
  [Syndicate] ok 36 - SSRF blocked: http://2130706433/feed
  [Syndicate] ok 37 - SSRF blocked: http://[::1]/feed
  [Syndicate] ok 38 - SSRF blocked: http://[::ffff:127.0.0.1]/feed
  [Syndicate] ok 39 - SSRF blocked: http://[::ffff:2130706433]/feed
  [Syndicate] ok 40 - SSRF blocked: http://[::ffff:7f00:1]/feed
  [Syndicate] ok 41 - SSRF blocked: http://[::ffff:10.0.0.1]/feed
  [Syndicate] ok 42 - SSRF allowed: http://8.8.8.8/feed
  [Syndicate] ok 43 - SSRF allowed: http://[::ffff:8.8.8.8]/feed
  [Syndicate] ok 44 - SSRF allowed: http://example.com/feed
  [Syndicate] ok 45 - SSRF allowed: http://01.example.com/feed
  [Syndicate] ok 46 - Content-Type with charset param accepted
  [Syndicate] ok 47 - Content-Type with multiple params accepted
  [Syndicate] ok 48 - missing Content-Type accepted
  [Syndicate] ok 49 - text/xml accepted
  [Syndicate] ok 50 - text/html rejected
  [Syndicate] ok 51 - bare href attribute skipped without crash
  [Syndicate] ok 52 - valid link found alongside bare href
  [Syndicate] ok 53 - bare rel attribute does not match alternate
  [Syndicate] ok 54 - SSRF blocked: http://[::127.0.0.1]/feed
  [Syndicate] ok 55 - SSRF blocked: http://[0:0:0:0:0:0:127.0.0.1]/feed
  [Syndicate] ok 56 - SSRF allowed: http://[::123.0.0.1]/feed
  [Syndicate] ok 57 - SSRF allowed: http://[2001:db8::1.2.3.4]/feed
  [Syndicate] ok 58 - Content-Length over MAX-FEED-SIZE rejected
  [Syndicate] ok 59 - body over MAX-FEED-SIZE rejected
  [Syndicate] ok 60 - custom duck-typed ua works
  [Syndicate] ok 61 - duck-typed ua fetch returns feed
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/10-media-rss.rakutest
  [Syndicate] 1..51
  [Syndicate] ok 1 - Parsed Media RSS feed
  [Syndicate] ok 2 - two items
  [Syndicate] ok 3 - item 0 title
  [Syndicate] ok 4 - item 0 link
  [Syndicate] ok 5 - item 0 description
  [Syndicate] not ok 6 - item 0 has 1 media:content
  [Syndicate] # Failed test 'item 0 has 1 media:content'
  [Syndicate] # at t/10-media-rss.rakutest line 21
  [Syndicate] # expected: '1'
  [Syndicate] #      got: '0'
  [Syndicate] not ok 7 - media:content url
  [Syndicate] # Failed test 'media:content url'
  [Syndicate] # at t/10-media-rss.rakutest line 22
  [Syndicate] # expected: 'http://example.com/video.mp4'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 8 - media:content type
  [Syndicate] # Failed test 'media:content type'
  [Syndicate] # at t/10-media-rss.rakutest line 23
  [Syndicate] # expected: 'video/mp4'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 9 - media:content medium
  [Syndicate] # Failed test 'media:content medium'
  [Syndicate] # at t/10-media-rss.rakutest line 24
  [Syndicate] # expected: 'video'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 10 - media:content duration
  [Syndicate] # Failed test 'media:content duration'
  [Syndicate] # at t/10-media-rss.rakutest line 25
  [Syndicate] # expected: '120'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 11 - media:content fileSize
  [Syndicate] # Failed test 'media:content fileSize'
  [Syndicate] # at t/10-media-rss.rakutest line 26
  [Syndicate] # expected: '1024000'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 12 - media:content width
  [Syndicate] # Failed test 'media:content width'
  [Syndicate] # at t/10-media-rss.rakutest line 27
  [Syndicate] # expected: '640'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 13 - media:content height
  [Syndicate] # Failed test 'media:content height'
  [Syndicate] # at t/10-media-rss.rakutest line 28
  [Syndicate] # expected: '480'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 14 - item 0 has 1 media:thumbnail
  [Syndicate] # Failed test 'item 0 has 1 media:thumbnail'
  [Syndicate] # at t/10-media-rss.rakutest line 30
  [Syndicate] # expected: '1'
  [Syndicate] #      got: '0'
  [Syndicate] not ok 15 - media:thumbnail url
  [Syndicate] # Failed test 'media:thumbnail url'
  [Syndicate] # at t/10-media-rss.rakutest line 31
  [Syndicate] # expected: 'http://example.com/thumb1.jpg'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 16 - media:thumbnail width
  [Syndicate] # Failed test 'media:thumbnail width'
  [Syndicate] # at t/10-media-rss.rakutest line 32
  [Syndicate] # expected: '320'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 17 - media:thumbnail height
  [Syndicate] # Failed test 'media:thumbnail height'
  [Syndicate] # at t/10-media-rss.rakutest line 33
  [Syndicate] # expected: '240'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 18 - media:thumbnail time
  [Syndicate] # Failed test 'media:thumbnail time'
  [Syndicate] # at t/10-media-rss.rakutest line 34
  [Syndicate] # expected: '01:23'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 19 - media:title
  [Syndicate] # Failed test 'media:title'
  [Syndicate] # at t/10-media-rss.rakutest line 36
  [Syndicate] # expected: 'Video: Syndication Explained'
  [Syndicate] #      got: (Str)
  [Syndicate] not ok 20 - media:description
  [Syndicate] # Failed test 'media:description'
  [Syndicate] # at t/10-media-rss.rakutest line 37
  [Syndicate] # expected: 'An in-depth look at feed syndication formats'
  [Syndicate] #      got: (Str)
  [Syndicate] ok 21 - item 1 title
  [Syndicate] ok 22 - item 1 link
  [Syndicate] not ok 23 - item 1 has 1 media:content
  [Syndicate] # Failed test 'item 1 has 1 media:content'
  [Syndicate] # at t/10-media-rss.rakutest line 44
  [Syndicate] # expected: '1'
  [Syndicate] #      got: '0'
  [Syndicate] not ok 24 - item 1 media:content url
  [Syndicate] # Failed test 'item 1 media:content url'
  [Syndicate] # at t/10-media-rss.rakutest line 45
  [Syndicate] # expected: 'http://example.com/audio.mp3'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 25 - item 1 media:content type
  [Syndicate] # Failed test 'item 1 media:content type'
  [Syndicate] # at t/10-media-rss.rakutest line 46
  [Syndicate] # expected: 'audio/mpeg'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 26 - item 1 media:content medium
  [Syndicate] # Failed test 'item 1 media:content medium'
  [Syndicate] # at t/10-media-rss.rakutest line 47
  [Syndicate] # expected: 'audio'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 27 - item 1 media:content duration
  [Syndicate] # Failed test 'item 1 media:content duration'
  [Syndicate] # at t/10-media-rss.rakutest line 48
  [Syndicate] # expected: '1800'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 28 - item 1 has 1 media:thumbnail
  [Syndicate] # Failed test 'item 1 has 1 media:thumbnail'
  [Syndicate] # at t/10-media-rss.rakutest line 50
  [Syndicate] # expected: '1'
  [Syndicate] #      got: '0'
  [Syndicate] not ok 29 - item 1 thumbnail url
  [Syndicate] # Failed test 'item 1 thumbnail url'
  [Syndicate] # at t/10-media-rss.rakutest line 51
  [Syndicate] # expected: 'http://example.com/thumb2.jpg'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 30 - roundtrip media:content count
  [Syndicate] # Failed test 'roundtrip media:content count'
  [Syndicate] # at t/10-media-rss.rakutest line 56
  [Syndicate] # expected: '1'
  [Syndicate] #      got: '0'
  [Syndicate] not ok 31 - roundtrip media:content url
  [Syndicate] # Failed test 'roundtrip media:content url'
  [Syndicate] # at t/10-media-rss.rakutest line 57
  [Syndicate] # expected: 'http://example.com/video.mp4'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 32 - roundtrip media:title
  [Syndicate] # Failed test 'roundtrip media:title'
  [Syndicate] # at t/10-media-rss.rakutest line 58
  [Syndicate] # expected: 'Video: Syndication Explained'
  [Syndicate] #      got: (Str)
  [Syndicate] ok 33 - Parsed HH:MM:SS Media RSS feed
  [Syndicate] ok 34 - 3 items in HH:MM:SS test feed
  [Syndicate] ok 35 - HH:MM:SS item title
  [Syndicate] not ok 36 - HH:MM:SS item has 1 media:content
  [Syndicate] # Failed test 'HH:MM:SS item has 1 media:content'
  [Syndicate] # at t/10-media-rss.rakutest line 70
  [Syndicate] # expected: '1'
  [Syndicate] #      got: '0'
  [Syndicate] not ok 37 - HH:MM:SS duration is defined
  [Syndicate] # Failed test 'HH:MM:SS duration is defined'
  [Syndicate] # at t/10-media-rss.rakutest line 71
  [Syndicate] not ok 38 - HH:MM:SS duration preserved as string
  [Syndicate] # Failed test 'HH:MM:SS duration preserved as string'
  [Syndicate] # at t/10-media-rss.rakutest line 72
  [Syndicate] # expected: '1:02:15'
  [Syndicate] #      got: (Any)
  [Syndicate] ok 39 - multi-content item title
  [Syndicate] not ok 40 - multi-content item has 3 media:content elements
  [Syndicate] # Failed test 'multi-content item has 3 media:content elements'
  [Syndicate] # at t/10-media-rss.rakutest line 77
  [Syndicate] # expected: '3'
  [Syndicate] #      got: '0'
  [Syndicate] not ok 41 - multi-content[0] url
  [Syndicate] # Failed test 'multi-content[0] url'
  [Syndicate] # at t/10-media-rss.rakutest line 78
  [Syndicate] # expected: 'http://example.com/video.mp4'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 42 - multi-content[0] duration
  [Syndicate] # Failed test 'multi-content[0] duration'
  [Syndicate] # at t/10-media-rss.rakutest line 79
  [Syndicate] # expected: '120'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 43 - multi-content[1] url
  [Syndicate] # Failed test 'multi-content[1] url'
  [Syndicate] # at t/10-media-rss.rakutest line 80
  [Syndicate] # expected: 'http://example.com/audio.mp3'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 44 - multi-content[1] duration
  [Syndicate] # Failed test 'multi-content[1] duration'
  [Syndicate] # at t/10-media-rss.rakutest line 81
  [Syndicate] # expected: '1800'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 45 - multi-content[2] url
  [Syndicate] # Failed test 'multi-content[2] url'
  [Syndicate] # at t/10-media-rss.rakutest line 82
  [Syndicate] # expected: 'http://example.com/thumb.jpg'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 46 - multi-content[2] medium
  [Syndicate] # Failed test 'multi-content[2] medium'
  [Syndicate] # at t/10-media-rss.rakutest line 83
  [Syndicate] # expected: 'image'
  [Syndicate] #      got: (Any)
  [Syndicate] ok 47 - HH:MM:SS roundtrip parsed
  [Syndicate] ok 48 - HH:MM:SS roundtrip item count
  [Syndicate] not ok 49 - HH:MM:SS roundtrip duration
  [Syndicate] # Failed test 'HH:MM:SS roundtrip duration'
  [Syndicate] # at t/10-media-rss.rakutest line 90
  [Syndicate] # expected: '1:02:15'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 50 - multi-content roundtrip count
  [Syndicate] # Failed test 'multi-content roundtrip count'
  [Syndicate] # at t/10-media-rss.rakutest line 91
  [Syndicate] # expected: '3'
  [Syndicate] #      got: '0'
  [Syndicate] # Subtest: Builder media-content carries medium and nested title/description
  [Syndicate]     not ok 1 - media:content emitted
  [Syndicate]     # Failed test 'media:content emitted'
  [Syndicate]     # at t/10-media-rss.rakutest line 112
  [Syndicate]     # Failed test 'media:content carries url'
  [Syndicate]     # at t/10-media-rss.rakutest line 113
  [Syndicate]     # Failed test 'media:content carries medium'
  [Syndicate]     # at t/10-media-rss.rakutest line 114
  [Syndicate]     # Failed test 'content-level media:title emitted'
  [Syndicate]     # at t/10-media-rss.rakutest line 115
  [Syndicate]     not ok 2 - media:content carries url
  [Syndicate]     not ok 3 - media:content carries medium
  [Syndicate]     not ok 4 - content-level media:title emitted
  [Syndicate]     not ok 5 - content-level media:description emitted
  [Syndicate]     # Failed test 'content-level media:description emitted'
  [Syndicate]     # at t/10-media-rss.rakutest line 116
  [Syndicate] Cannot look up attributes in a Hash type object. Did you forget a '.new'?
  [Syndicate]   in block <unit> at t/10-media-rss.rakutest line 119
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/11-itunes-podcast.rakutest
  [Syndicate] 1..33
  [Syndicate] ok 1 - Parsed iTunes podcast feed
  [Syndicate] ok 2 - channel itunes:author
  [Syndicate] ok 3 - channel itunes:summary
  [Syndicate] ok 4 - item 0 title
  [Syndicate] ok 5 - item 0 link
  [Syndicate] ok 6 - item 0 itunes:author
  [Syndicate] ok 7 - item 0 itunes:summary
  [Syndicate] ok 8 - item 0 itunes:duration
  [Syndicate] ok 9 - item 1 title
  [Syndicate] ok 10 - item 1 link
  [Syndicate] ok 11 - item 1 itunes:author
  [Syndicate] ok 12 - item 1 itunes:summary
  [Syndicate] ok 13 - item 1 itunes:duration
  [Syndicate] ok 14 - item 2 title
  [Syndicate] ok 15 - item 2 itunes:duration (seconds)
  [Syndicate] ok 16 - item 2 itunes:author is undefined
  [Syndicate] ok 17 - item 2 itunes:summary is undefined
  [Syndicate] ok 18 - Roundtripped feed parsed
  [Syndicate] ok 19 - roundtrip channel itunes:author
  [Syndicate] ok 20 - roundtrip channel itunes:summary
  [Syndicate] ok 21 - roundtrip item count
  [Syndicate] ok 22 - roundtrip item 0 itunes:author
  [Syndicate] ok 23 - roundtrip item 0 itunes:summary
  [Syndicate] ok 24 - roundtrip item 0 itunes:duration
  [Syndicate] ok 25 - roundtrip item 1 itunes:author
  [Syndicate] ok 26 - roundtrip item 1 itunes:duration
  [Syndicate] ok 27 - roundtrip item 2 itunes:duration (seconds)
  [Syndicate] ok 28 - XML output contains xmlns:itunes
  [Syndicate] ok 29 - XML output contains itunes:author
  [Syndicate] ok 30 - XML output contains itunes:summary
  [Syndicate] ok 31 - XML output contains itunes:duration
  [Syndicate] ok 32 - builder channel itunes:author
  [Syndicate] ok 33 - builder item title
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/12-concurrency.rakutest
  [Syndicate] 1..6
  [Syndicate] ok 1 - Stats class exists
  [Syndicate] ok 2 - starts at zero
  [Syndicate] ok 3 - items starts at zero
  [Syndicate] ok 4 - errors starts at zero
  [Syndicate] ok 5 - feeds-parsed = 10 after concurrent increments
  [Syndicate] ok 6 - items-parsed = 50 after concurrent increments
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/13-errors.rakutest
  [Syndicate] 1..16
  [Syndicate] ok 1 - empty input dies
  [Syndicate] ok 2 - whitespace-only input dies
  [Syndicate] ok 3 - unknown root element dies
  [Syndicate] ok 4 - garbage input dies
  [Syndicate] ok 5 - JSON without version key dies
  [Syndicate] ok 6 - parse-feed clarifies that valid JSON is not a JSON Feed
  [Syndicate] ok 7 - parse-feed keeps generic message for non-JSON input
  [Syndicate] ok 8 - wrong root element dies
  [Syndicate] ok 9 - no channel element dies
  [Syndicate] ok 10 - wrong RSS version dies
  [Syndicate] ok 11 - wrong item root element dies
  [Syndicate] ok 12 - wrong Atom entry root element dies
  [Syndicate] ok 13 - wrong Atom root element dies
  [Syndicate] ok 14 - invalid JSON dies
  [Syndicate] ok 15 - wrong RDF root element dies
  [Syndicate] ok 16 - all errors recorded by Stats
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/14-utils.rakutest
  [Syndicate] 1..27
  [Syndicate] ok 1 - encode &
  [Syndicate] ok 2 - encode <
  [Syndicate] ok 3 - encode Str returns Str
  [Syndicate] ok 4 - decode &amp;
  [Syndicate] ok 5 - decode &lt;
  [Syndicate] ok 6 - decode Str returns Str
  [Syndicate] ok 7 - add-element encodes value
  [Syndicate] ok 8 - add-element with Str appends nothing
  [Syndicate] ok 9 - get-text returns decoded text
  [Syndicate] ok 10 - get-text on missing element dies
  [Syndicate] ok 11 - get-text on empty element dies
  [Syndicate] ok 12 - get-text-optional returns text
  [Syndicate] ok 13 - get-text-optional on missing returns Str
  [Syndicate] ok 14 - parse-date RFC3339 returns DateTime
  [Syndicate] ok 15 - year correct
  [Syndicate] ok 16 - parse-date on empty dies
  [Syndicate] ok 17 - parse-date :optional valid returns DateTime
  [Syndicate] ok 18 - parse-date :optional invalid returns Nil
  [Syndicate] ok 19 - parse-date :optional empty returns Nil
  [Syndicate] ok 20 - AM/PM without seconds parses
  [Syndicate] ok 21 - AM hour preserved
  [Syndicate] ok 22 - missing seconds default to 0
  [Syndicate] ok 23 - AM/PM with seconds parses
  [Syndicate] ok 24 - PM hour converted to 24h
  [Syndicate] ok 25 - seconds preserved
  [Syndicate] ok 26 - 12 AM parses
  [Syndicate] ok 27 - 12 AM maps to midnight
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/15-extensions.rakutest
  [Syndicate] 1..6
  [Syndicate] ok 1 - run-parsers calls registered parse callbacks
  [Syndicate] ok 2 - run-parsers callback can modify %attrs
  [Syndicate] ok 3 - run-generators calls registered generate callbacks
  [Syndicate] ok 4 - run-generators callback can modify $xml
  [Syndicate] ok 5 - run-parsers catches dying callbacks
  [Syndicate] ok 6 - run-generators catches dying callbacks
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/16-ext-utils.rakutest
  [Syndicate] 1..19
  [Syndicate] ok 1 - DC: get-dc-text returns creator
  [Syndicate] ok 2 - DC: get-dc-text on missing returns Str
  [Syndicate] ok 3 - DC: get-dc-texts returns all subjects
  [Syndicate] ok 4 - DC: first dc:subject
  [Syndicate] ok 5 - DC: add-dc-declaration sets xmlns
  [Syndicate] ok 6 - DC: add-dc-element creates element with text
  [Syndicate] ok 7 - DC: add-dc-element with Str adds nothing
  [Syndicate] ok 8 - MRSS: get-media-text returns title
  [Syndicate] ok 9 - MRSS: get-media-text on missing returns Str
  [Syndicate] ok 10 - MRSS: get-media-contents count
  [Syndicate] ok 11 - MRSS: media:content url
  [Syndicate] ok 12 - MRSS: get-media-thumbnails count
  [Syndicate] ok 13 - MRSS: media:thumbnail url
  [Syndicate] ok 14 - IT: get-itunes-text returns author
  [Syndicate] ok 15 - IT: get-itunes-text returns summary
  [Syndicate] ok 16 - IT: get-itunes-duration returns duration
  [Syndicate] ok 17 - IT: get-itunes-text on missing returns Str
  [Syndicate] ok 18 - IT: add-itunes-declaration sets xmlns
  [Syndicate] ok 19 - IT: add-itunes-element creates element
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/17-dublin-core.rakutest
  [Syndicate] 1..12
  [Syndicate] ok 1 - Parsed RSS 2.0 with dc:date
  [Syndicate] ok 2 - 3 items parsed
  [Syndicate] ok 3 - item with dc:date only has DateTime updated
  [Syndicate] Cannot look up attributes in a DateTime type object. Did you forget a '.new'?
  [Syndicate]   in block <unit> at t/17-dublin-core.rakutest line 46
  [Syndicate] # You planned 12 tests, but ran 3
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/18-audit-regressions.rakutest
  [Syndicate] 1..30
  [Syndicate] ok 1 - RSS 1.0 CDATA item kept
  [Syndicate] ok 2 - RSS 1.0 CDATA item title
  [Syndicate] ok 3 - RSS 1.0 dc:subject CDATA captured
  [Syndicate] ok 4 - RSS 1.0 item with raw & < in CDATA kept
  [Syndicate] ok 5 - RSS 1.0 CDATA with raw & and < preserved
  [Syndicate] ok 6 - RSS 2.0 CDATA guid captured
  [Syndicate] ok 7 - RSS 0.91 CDATA skipHours captured
  [Syndicate] ok 8 - RSS 0.91 CDATA skipDays captured
  [Syndicate] not ok 9 - media:title CDATA captured
  [Syndicate] # Failed test 'media:title CDATA captured'
  [Syndicate] # at t/18-audit-regressions.rakutest line 69
  [Syndicate] # expected: 'Media & Title'
  [Syndicate] #      got: (Str)
  [Syndicate] not ok 10 - media:description CDATA captured
  [Syndicate] # Failed test 'media:description CDATA captured'
  [Syndicate] # at t/18-audit-regressions.rakutest line 70
  [Syndicate] # expected: 'Media <em>description</em>'
  [Syndicate] #      got: (Str)
  [Syndicate] ok 11 - itunes:summary CDATA captured
  [Syndicate] ok 12 - Atom CDATA content captured
  [Syndicate] ok 13 - direct Atom construction emits link rel=alternate
  [Syndicate] ok 14 - direct Atom construction emits link href
  [Syndicate] ok 15 - direct Atom construction emits author
  [Syndicate] ok 16 - builder atom output emits link rel=alternate
  [Syndicate] ok 17 - builder atom output emits link href
  [Syndicate] ok 18 - builder atom output emits author
  [Syndicate] ok 19 - JSON Feed numeric dates do not throw
  [Syndicate] ok 20 - numeric date_published ignored, not fatal
  [Syndicate] ok 21 - numeric date_modified ignored, not fatal
  [Syndicate] ok 22 - to-hash deep copy: tags cache intact
  [Syndicate] ok 23 - to-hash deep copy: authors cache intact
  [Syndicate] ok 24 - bare xhtml content wrapped in div
  [Syndicate] ok 25 - already-wrapped xhtml content not double-wrapped
  [Syndicate] ok 26 - multi-div xhtml parse keeps first child
  [Syndicate] ok 27 - multi-div xhtml parse keeps second child
  [Syndicate] ok 28 - multi-div xhtml output keeps first child
  [Syndicate] ok 29 - multi-div xhtml output keeps second child
  [Syndicate] ok 30 - multi-div xhtml roundtrips all children
  [Syndicate] # You failed 2 tests of 30
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/19-followup-audit.rakutest
  [Syndicate] 1..43
  [Syndicate] ok 1 - qualified Syndicate::Parse::parse-feed works
  [Syndicate] ok 2 - qualified parse-feed returns RSS
  [Syndicate] ok 3 - qualified Syndicate::Parse::feed-format works
  [Syndicate] ok 4 - qualified Syndicate::Parse::sanitize-input works
  [Syndicate] ok 5 - qualified Syndicate::Parse::parse-feed-with-format works
  [Syndicate] ok 6 - qualified Syndicate::Parse::parse-file works
  [Syndicate] ok 7 - qualified parse-file returns RSS
  [Syndicate] ok 8 - parse-rss works
  [Syndicate] ok 9 - parse-atom works
  [Syndicate] ok 10 - parse-json works
  [Syndicate] ok 11 - parse-rss1 works
  [Syndicate] ok 12 - parse-rss091 works
  [Syndicate] ok 13 - query-only ref keeps base path
  [Syndicate] ok 14 - fragment-only ref keeps base path
  [Syndicate] ok 15 - empty ref keeps base path
  [Syndicate] ok 16 - to-hash author hash not leaked
  [Syndicate] ok 17 - to-hash item hash not leaked
  [Syndicate] ok 18 - to-hash item tags not leaked
  [Syndicate] ok 19 - MediaRSS feed with non-numeric attrs parses
  [Syndicate] not ok 20 - non-numeric fileSize kept as string
  [Syndicate] # Failed test 'non-numeric fileSize kept as string'
  [Syndicate] # at t/19-followup-audit.rakutest line 96
  [Syndicate] # expected: 'abc'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 21 - numeric width parsed as Int
  [Syndicate] # Failed test 'numeric width parsed as Int'
  [Syndicate] # at t/19-followup-audit.rakutest line 97
  [Syndicate] # expected: '640'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 22 - non-numeric thumbnail width kept as string
  [Syndicate] # Failed test 'non-numeric thumbnail width kept as string'
  [Syndicate] # at t/19-followup-audit.rakutest line 98
  [Syndicate] # expected: 'big'
  [Syndicate] #      got: (Any)
  [Syndicate] ok 23 - SSRF blocked: http://[2002:7f00:1::]/feed
  [Syndicate] ok 24 - SSRF blocked: http://[2002:c0a8:1::]/feed
  [Syndicate] ok 25 - SSRF blocked: http://[2001:0:7f00:1::]/feed
  [Syndicate] ok 26 - SSRF blocked: http://[64:ff9b::7f00:1]/feed
  [Syndicate] ok 27 - SSRF blocked: http://[64:ff9b::c0a8:1]/feed
  [Syndicate] ok 28 - SSRF blocked: http://[::7f00:1]/feed
  [Syndicate] ok 29 - SSRF allowed: http://[2002:0808:0808::]/feed
  [Syndicate] ok 30 - SSRF allowed: http://[64:ff9b::0808:0808]/feed
  [Syndicate] ok 31 - SSRF allowed: http://[2001:db8::abcd]/feed
  [Syndicate] ok 32 - prefix bound to matching namespace-uri is active
  [Syndicate] ok 33 - prefix bound to wrong namespace-uri is inactive
  [Syndicate] ok 34 - unbound canonical prefix is active (lenient feeds)
  [Syndicate] ok 35 - extension registry restored after set-active tests
  [Syndicate] ok 36 - rel tokens other than 'alternate' do not prevent match
  [Syndicate] ok 37 - rel without alternate token excluded
  [Syndicate] ok 38 - empty feed category term skipped
  [Syndicate] ok 39 - empty entry category term skipped
  [Syndicate] ok 40 - no empty term attribute regenerated in output
  [Syndicate] ok 41 - JSONFeed tags must be an array
  [Syndicate] ok 42 - JSONFeed tags elements must be strings
  [Syndicate] ok 43 - valid JSONFeed tags accepted
  [Syndicate] # You failed 3 tests of 43
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/20-rss-common.rakutest
  [Syndicate] 1..16
  [Syndicate] ok 1 - RSS 2.0 parses item count
  [Syndicate] ok 2 - RSS 2.0 XML is cached (same object)
  [Syndicate] not ok 3 - RSS 2.0 regenerates dc declaration from item needs
  [Syndicate] # Failed test 'RSS 2.0 regenerates dc declaration from item needs'
  [Syndicate] # at t/20-rss-common.rakutest line 35
  [Syndicate] # expected a match with: / 'xmlns:dc' /
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rss version=\"2.0\" xmlns:content=\"http://purl.org/rss/1.0/modules/content/\"><channel><title>T</title><link>L</link><description>D</description><item><title>I</title><link>IL</link><content:encoded>\&lt;p\&gt;hi\&lt;/p\&gt;</content:encoded></item></channel></rss>"
  [Syndicate] not ok 4 - RSS 2.0 regenerates media declaration from item needs
  [Syndicate] # Failed test 'RSS 2.0 regenerates media declaration from item needs'
  [Syndicate] # at t/20-rss-common.rakutest line 36
  [Syndicate] # expected a match with: / 'xmlns:media' /
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rss version=\"2.0\" xmlns:content=\"http://purl.org/rss/1.0/modules/content/\"><channel><title>T</title><link>L</link><description>D</description><item><title>I</title><link>IL</link><content:encoded>\&lt;p\&gt;hi\&lt;/p\&gt;</content:encoded></item></channel></rss>"
  [Syndicate] ok 5 - RSS 2.0 regenerates content declaration from item needs
  [Syndicate] ok 6 - RSS 2.0 new(Str) error uses shared constructor message
  [Syndicate] ok 7 - RSS 0.91 parses item count
  [Syndicate] ok 8 - RSS 0.91 XML is cached (same object)
  [Syndicate] ok 9 - RSS 0.91 regenerates itunes declaration from item needs
  [Syndicate] ok 10 - RSS 0.91 new(Str) error uses shared constructor message
  [Syndicate] ok 11 - RSS 1.0 parses item count
  [Syndicate] ok 12 - RSS 1.0 XML is cached (same object)
  [Syndicate] ok 13 - RSS 1.0 regenerates dc declaration from categories
  [Syndicate] ok 14 - RSS 1.0 shared XML path builds rdf:RDF root
  [Syndicate] ok 15 - RSS 2.0 shared XML path builds rss root
  [Syndicate] ok 16 - RSS 1.0 new(Str) error uses shared constructor message
  [Syndicate] # You failed 2 tests of 16
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/21-entity-roundtrip.rakutest
  [Syndicate] 1..39
  [Syndicate] ok 1 - dc:language parses into language
  [Syndicate] ok 2 - dc:language-only feed regenerates dc declaration
  [Syndicate] ok 3 - dc:language element regenerated
  [Syndicate] not ok 4 - MediaRSS url decoded on parse
  [Syndicate] # Failed test 'MediaRSS url decoded on parse'
  [Syndicate] # at t/21-entity-roundtrip.rakutest line 47
  [Syndicate] # expected: 'http://e.com/?a=1&b=2'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 5 - MediaRSS type decoded on parse
  [Syndicate] # Failed test 'MediaRSS type decoded on parse'
  [Syndicate] # at t/21-entity-roundtrip.rakutest line 48
  [Syndicate] # expected: 'audio/mpeg&x'
  [Syndicate] #      got: (Any)
  [Syndicate] not ok 6 - MediaRSS url single-encoded on generate
  [Syndicate] # Failed test 'MediaRSS url single-encoded on generate'
  [Syndicate] # at t/21-entity-roundtrip.rakutest line 50
  [Syndicate] not ok 7 - MediaRSS type single-encoded on generate
  [Syndicate] # Failed test 'MediaRSS type single-encoded on generate'
  [Syndicate] # at t/21-entity-roundtrip.rakutest line 51
  [Syndicate] ok 8 - MediaRSS not double-encoded
  [Syndicate] ok 9 - atom:self href decoded on parse
  [Syndicate] ok 10 - atom:self href single-encoded on generate
  [Syndicate] ok 11 - channel rdf:about decoded on parse
  [Syndicate] ok 12 - item rdf:about decoded on parse
  [Syndicate] ok 13 - image rdf:about decoded on parse
  [Syndicate] ok 14 - channel rdf:about single-encoded on generate
  [Syndicate] ok 15 - item rdf:about single-encoded on generate
  [Syndicate] ok 16 - image rdf:about single-encoded on generate
  [Syndicate] ok 17 - source link href decoded on parse
  [Syndicate] ok 18 - source link href single-encoded on generate
  [Syndicate] ok 19 - feed category term decoded on parse
  [Syndicate] ok 20 - entry category term decoded on parse
  [Syndicate] ok 21 - feed category term single-encoded on generate
  [Syndicate] ok 22 - entry category term single-encoded on generate
  [Syndicate] ok 23 - user-constructed category term encoded on generate
  [Syndicate] ok 24 - link type decoded on parse
  [Syndicate] ok 25 - content type decoded on parse
  [Syndicate] ok 26 - link type single-encoded on generate
  [Syndicate] ok 27 - content type single-encoded on generate
  [Syndicate] ok 28 - empty JSON Feed to-hash includes items key
  [Syndicate] ok 29 - empty JSON Feed items is an empty array
  [Syndicate] ok 30 - empty JSON Feed to-json includes items: []
  [Syndicate] ok 31 - decimal character references decode
  [Syndicate] ok 32 - hexadecimal character references decode
  [Syndicate] ok 33 - encoded numeric reference stays literal (no double decode)
  [Syndicate] ok 34 - numeric reference roundtrips single-encoded
  [Syndicate] ok 35 - unknown named entity stays literal
  [Syndicate] ok 36 - out-of-range numeric reference stays literal
  [Syndicate] ok 37 - numeric references decoded on parse
  [Syndicate] ok 38 - numeric references single-encoded on generate
  [Syndicate] ok 39 - no double-encoded ampersand
  [Syndicate] # You failed 4 tests of 39
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/22-code-quality.rakutest
  [Syndicate] 1..10
  [Syndicate] ok 1 - skipDays normalizes day names
  [Syndicate] ok 2 - invalid skipDays value is skipped
  [Syndicate] ok 3 - all-invalid skipDays yields empty list
  [Syndicate] ok 4 - all-invalid skipDays feeds still parse
  [Syndicate] ok 5 - expired: true accepted
  [Syndicate] ok 6 - expired: false accepted
  [Syndicate] ok 7 - non-Bool expired dies
  [Syndicate] ok 8 - non-Bool expired dies with graceful message
  [Syndicate] ok 9 - rethrow-style constructors still record errors
  [Syndicate] ok 10 - normalized skipDays regenerated
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/23-audit-round-6.rakutest
  [Syndicate] 1..34
  [Syndicate] ok 1 - content:encoded found via URI-bound prefix
  [Syndicate] ok 2 - wrong-URI prefix does not match as content
  [Syndicate] ok 3 - default-namespace encoded element matches
  [Syndicate] ok 4 - space-separated ISO + EST parses
  [Syndicate] ok 5 - EST offset applied
  [Syndicate] ok 6 - space-separated ISO + numeric offset parses
  [Syndicate] ok 7 - numeric offset applied
  [Syndicate] ok 8 - space-separated ISO + colon offset parses
  [Syndicate] ok 9 - space-separated ISO without TZ parses as UTC
  [Syndicate] ok 10 - tz-less datetime treated as UTC
  [Syndicate] ok 11 - RFC 2822 dates still parse
  [Syndicate] ok 12 - RSS pubDate with space-separated ISO parses
  [Syndicate] ok 13 - RSS pubDate space-separated ISO offset applied
  [Syndicate] ok 14 - 0.91 item guid retained in object model
  [Syndicate] ok 15 - 0.91 item comments retained in object model
  [Syndicate] ok 16 - 0.91 item source retained in object model
  [Syndicate] not ok 17 - 0.91 item dc:creator author retained in object model
  [Syndicate] # Failed test '0.91 item dc:creator author retained in object model'
  [Syndicate] # at t/23-audit-round-6.rakutest line 95
  [Syndicate] # expected: 'Jane'
  [Syndicate] #      got: (Str)
  [Syndicate] ok 18 - 0.91 output omits guid
  [Syndicate] ok 19 - 0.91 output omits comments
  [Syndicate] ok 20 - 0.91 output omits enclosure
  [Syndicate] ok 21 - 0.91 output omits source
  [Syndicate] ok 22 - 0.91 output omits author
  [Syndicate] ok 23 - 0.91 output omits item pubDate
  [Syndicate] ok 24 - 0.91 output omits xmlns:dc declaration
  [Syndicate] ok 25 - 0.91 output omits dc:creator
  [Syndicate] ok 26 - 0.91 item regenerates only title, link, description
  [Syndicate] ok 27 - builder 0.91 item emits only title, link, description
  [Syndicate] ok 28 - builder 0.91 item omits author
  [Syndicate] ok 29 - builder 0.91 item omits comments
  [Syndicate] ok 30 - builder 0.91 item omits source
  [Syndicate] ok 31 - empty xhtml content parses to empty Str
  [Syndicate] ok 32 - empty xhtml content does not record an error
  [Syndicate] not ok 33 - Set.new active-ext default still runs generators
  [Syndicate] # Failed test 'Set.new active-ext default still runs generators'
  [Syndicate] # at t/23-audit-round-6.rakutest line 150
  [Syndicate] # expected a match with: /'<dc:creator>Jane</dc:creator>'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rdf:RDF xmlns:dc=\"http://purl.org/dc/elements/1.1/\" xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns#\" xmlns=\"http://purl.org/rss/1.0/\"><channel rdf:about=\"http://example.com/needs\"><title>Needs</title><link>http://example.com/needs</link><description>Needs test</description><generator>Syndicate</generator><items><rdf:Seq><rdf:li rdf:resource=\"http://example.com/needs/1\"/></rdf:Seq></items></channel><item rdf:about=\"http://example.com/needs/1\"><title>Item</title><link>http://example.com/needs/1</link></item></rdf:RDF>"
  [Syndicate] ok 34 - entries without updated share a single build timestamp
  [Syndicate] # You failed 2 tests of 34
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/24-date-offsets.rakutest
  [Syndicate] 1..43
  [Syndicate] ok 1 - ISO +05:30 parses
  [Syndicate] ok 2 - ISO +05:30 offset applied
  [Syndicate] ok 3 - ISO +05:30 stored as +05:30
  [Syndicate] ok 4 - ISO +0530 parses
  [Syndicate] ok 5 - ISO +0530 offset applied
  [Syndicate] ok 6 - space-separated ISO +05:30 parses
  [Syndicate] ok 7 - space-separated ISO +05:30 offset applied
  [Syndicate] ok 8 - RFC 2822 +0530 parses
  [Syndicate] ok 9 - RFC 2822 +0530 not mangled (was +05:18)
  [Syndicate] ok 10 - RFC 2822 +0530 stored as +05:30
  [Syndicate] ok 11 - RFC 2822 -0330 parses
  [Syndicate] ok 12 - RFC 2822 -0330 not mangled (was -03:18)
  [Syndicate] ok 13 - RFC 2822 -0330 stored as -03:30
  [Syndicate] ok 14 - IST abbreviation parses
  [Syndicate] ok 15 - half-hour abbreviation IST offset applied
  [Syndicate] ok 16 - whole-hour EST still correct
  [Syndicate] ok 17 - whole-hour -0500 still correct
  [Syndicate] ok 18 - explicit Z unaffected
  [Syndicate] ok 19 - Atom feed updated +05:30 applied
  [Syndicate] ok 20 - Atom entry updated +0530 applied
  [Syndicate] ok 21 - RSS pubDate RFC +0530 applied
  [Syndicate] ok 22 - JSON Feed date_published +0530 applied
  [Syndicate] ok 23 - JSON Feed date_modified -0330 applied
  [Syndicate] ok 24 - tz-less T-form parses
  [Syndicate] ok 25 - tz-less T-form treated as UTC
  [Syndicate] ok 26 - tz-less space-separated form parses
  [Syndicate] ok 27 - tz-less space-separated form treated as UTC
  [Syndicate] ok 28 - date-only still parses
  [Syndicate] ok 29 - date-only is midnight UTC
  [Syndicate] ok 30 - invalid ttl not set on feed
  [Syndicate] ok 31 - invalid ttl records no Stats error (optional metadata, feed parses fine)
  [Syndicate] ok 32 - valid ttl parses
  [Syndicate] ok 33 - &nbsp; decodes to non-breaking space
  [Syndicate] ok 34 - &mdash; decodes to em dash
  [Syndicate] ok 35 - &rsquo; decodes to right single quote
  [Syndicate] ok 36 - &ldquo; decodes to left double quote
  [Syndicate] ok 37 - &Aacute; decodes case-sensitively (Á)
  [Syndicate] ok 38 - &aacute; decodes case-sensitively (á)
  [Syndicate] ok 39 - uppercase &AMP; still decodes
  [Syndicate] ok 40 - uppercase &LT; still decodes
  [Syndicate] ok 41 - no double decode of named entities
  [Syndicate] ok 42 - unknown named entity stays literal
  [Syndicate] ok 43 - named entity roundtrips single-encoded
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/25-audit-round-8.rakutest
  [Syndicate] 1..47
  [Syndicate] ok 1 - B1: self-only feed has no $.link (no alternate)
  [Syndicate] ok 2 - B1: output emits no alternate link
  [Syndicate] ok 3 - B1: output keeps the self link
  [Syndicate] ok 4 - B1: self href preserved
  [Syndicate] ok 5 - B1: self link survives roundtrip
  [Syndicate] ok 6 - B2: RSS to-hash has copyright
  [Syndicate] ok 7 - B2: RSS to-hash has ttl
  [Syndicate] ok 8 - B2: RSS to-hash has pubDate
  [Syndicate] ok 9 - B2: RSS to-hash image includes width
  [Syndicate] ok 10 - B2: RSS to-hash has atom-self-link
  [Syndicate] ok 11 - B2: RSS to-hash omits categories when empty
  [Syndicate] ok 12 - B2: item to-hash has guid
  [Syndicate] ok 13 - B2: item to-hash has guid-is-permalink
  [Syndicate] ok 14 - B2: item to-hash has comments
  [Syndicate] ok 15 - B2: item to-hash has enclosure
  [Syndicate] ok 16 - B2: item to-hash has updated (pubDate)
  [Syndicate] ok 17 - B2: Atom to-hash has id
  [Syndicate] ok 18 - B2: Atom to-hash has updated
  [Syndicate] ok 19 - B2: Atom to-hash has subtitle
  [Syndicate] ok 20 - B2: Atom to-hash has icon
  [Syndicate] ok 21 - B2: Atom to-hash has logo
  [Syndicate] ok 22 - B2: Atom to-hash has rights
  [Syndicate] ok 23 - B2: Atom to-hash has author-detail
  [Syndicate] ok 24 - B2: Atom to-hash has contributors
  [Syndicate] ok 25 - B2: Atom to-hash has link-self
  [Syndicate] ok 26 - B2: Atom to-hash has link-alternate
  [Syndicate] ok 27 - B2: Atom item to-hash has content
  [Syndicate] ok 28 - B2: Atom item to-hash has content-type
  [Syndicate] ok 29 - B2: Atom item to-hash has published
  [Syndicate] ok 30 - B2: Atom item to-hash has contributors
  [Syndicate] ok 31 - B2: Atom item to-hash has categories
  [Syndicate] ok 32 - B4: JSON feed served as application/json fetches
  [Syndicate] ok 33 - B4: application/json with charset fetches
  [Syndicate] ok 34 - B5: skipHours keeps in-range hours, drops invalid
  [Syndicate] ok 35 - P2: non-numeric width leaves no key
  [Syndicate] ok 36 - P2: non-numeric height leaves no key
  [Syndicate] ok 37 - P2: other image fields intact
  [Syndicate] ok 38 - Q2: alt-prefix itunes:author parsed at feed level
  [Syndicate] ok 39 - Q2: alt-prefix itunes:summary parsed at feed level
  [Syndicate] ok 40 - Q2: alt-prefix itunes:summary parsed at item level
  [Syndicate] ok 41 - Q2: alt-prefix itunes:duration parsed (extension active)
  [Syndicate] not ok 42 - Q2: alt-prefix dc:creator parsed as author
  [Syndicate] # Failed test 'Q2: alt-prefix dc:creator parsed as author'
  [Syndicate] # at t/25-audit-round-8.rakutest line 183
  [Syndicate] # expected: 'Alt Creator'
  [Syndicate] #      got: (Str)
  [Syndicate] not ok 43 - Q2: alt-prefix dc:subject parsed
  [Syndicate] # Failed test 'Q2: alt-prefix dc:subject parsed'
  [Syndicate] # at t/25-audit-round-8.rakutest line 184
  [Syndicate] # expected: $("Alt Subj",)
  [Syndicate] #      got: $( )
  [Syndicate] ok 44 - Q4: builder feed categories returns a List
  [Syndicate] ok 45 - Q4: builder feed category value present
  [Syndicate] ok 46 - Q6: RSS 1.0 output has no <guid>
  [Syndicate] ok 47 - Q6: RSS 2.0 output still has <guid>
  [Syndicate] # You failed 2 tests of 47
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/26-audit-round-9.rakutest
  [Syndicate] 1..41
  [Syndicate] ok 1 - digit-named entities (frac12/sup2/frac34) decode
  [Syndicate] ok 2 - encoded digit-entity stays literal (no double decode)
  [Syndicate] ok 3 - unknown digit-named entity stays literal
  [Syndicate] ok 4 - RFC 2822 UT offset parses as UTC
  [Syndicate] ok 5 - tz-less RFC 2822 month-name date defaults to UTC
  [Syndicate] ok 6 - tz-less ISO shape still defaults to UTC
  [Syndicate] ok 7 - fragment-only ref keeps base query
  [Syndicate] ok 8 - empty ref keeps base query
  [Syndicate] ok 9 - query-only ref replaces base query
  [Syndicate] ok 10 - path ref drops base query
  [Syndicate] ok 11 - RSS 1.0 dc:subject via declared alt prefix
  [Syndicate] ok 12 - RSS 1.0 dc:subject via undeclared canonical prefix
  [Syndicate] ok 13 - undeclared itunes:author parsed at item level
  [Syndicate] ok 14 - undeclared itunes:duration parsed at item level
  [Syndicate] not ok 15 - undeclared dc:creator parsed at item level
  [Syndicate] # Failed test 'undeclared dc:creator parsed at item level'
  [Syndicate] # at t/26-audit-round-9.rakutest line 98
  [Syndicate] # expected: 'Jane'
  [Syndicate] #      got: (Str)
  [Syndicate] ok 16 - canonical prefix bound to wrong URI stays inactive
  [Syndicate] ok 17 - bare xhtml child normalized to div-wrapped form at parse
  [Syndicate] ok 18 - bare xhtml parse->regen->reparse is byte-stable
  [Syndicate] ok 19 - single xhtml div kept as-is at parse
  [Syndicate] ok 20 - div xhtml parse->regen->reparse is byte-stable
  [Syndicate] ok 21 - multi-div xhtml keeps all children at parse
  [Syndicate] ok 22 - parse-feed-or-nil returns parsed feed
  [Syndicate] ok 23 - parse-feed-or-nil returns Nil for HTML
  [Syndicate] ok 24 - parse-feed-or-nil returns Nil for garbage
  [Syndicate] ok 25 - parse-feed-or-nil records no error for non-feed input
  [Syndicate] ok 26 - items cache: author nested hash intact
  [Syndicate] ok 27 - items cache: tags array intact
  [Syndicate] ok 28 - items cache: author container replace isolated
  [Syndicate] ok 29 - items cache: tags container replace isolated
  [Syndicate] ok 30 - feed built without its own updated
  [Syndicate] ok 31 - Atom to-hash includes computed (entry-max) updated when feed updated unset
  [Syndicate] ok 32 - Atom XML emits the same computed updated
  [Syndicate] ok 33 - parse-file missing path raises friendly error
  [Syndicate] ok 34 - no per-item note() left in V0_91.rakumod
  [Syndicate] ok 35 - no per-item note() left in V1_0.rakumod
  [Syndicate] ok 36 - no per-item note() left in RSS.rakumod
  [Syndicate] ok 37 - extension callback failures are not noted
  [Syndicate] ok 38 - extension error counter retained
  [Syndicate] ok 39 - extension errors recorded in stats
  [Syndicate] ok 40 - no extension callback-failure notes remain
  [Syndicate] ok 41 - atom:link rel=self still parsed after redundant-check removal
  [Syndicate] # You failed 1 test of 41
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/27-audit-round-10.rakutest
  [Syndicate] 1..41
  [Syndicate] ok 1 - path+query ref replaces query
  [Syndicate] ok 2 - path+fragment ref drops base query
  [Syndicate] ok 3 - dot-relative ref
  [Syndicate] ok 4 - parent-relative ref
  [Syndicate] not ok 5 - alt prefix bound to MRSS URI parses as media:content
  [Syndicate] # Failed test 'alt prefix bound to MRSS URI parses as media:content'
  [Syndicate] # at t/27-audit-round-10.rakutest line 35
  [Syndicate] # expected: '1'
  [Syndicate] #      got: '0'
  [Syndicate] not ok 6 - undeclared canonical media: prefix parses leniently
  [Syndicate] # Failed test 'undeclared canonical media: prefix parses leniently'
  [Syndicate] # at t/27-audit-round-10.rakutest line 46
  [Syndicate] # expected: '1'
  [Syndicate] #      got: '0'
  [Syndicate] ok 7 - prefix bound to a wrong URI is never media:content
  [Syndicate] ok 8 - author preserved from parse
  [Syndicate] not ok 9 - dc:creator values stored
  [Syndicate] # Failed test 'dc:creator values stored'
  [Syndicate] # at t/27-audit-round-10.rakutest line 73
  [Syndicate] # expected: 'Creator@x.com'
  [Syndicate] #      got: ''
  [Syndicate] not ok 10 - dc:creator regenerated
  [Syndicate] # Failed test 'dc:creator regenerated'
  [Syndicate] # at t/27-audit-round-10.rakutest line 75
  [Syndicate] # expected a match with: /'<dc:creator>Creator@x.com</dc:creator>'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rss version=\"2.0\"><channel><title>T</title><link>http://e.com</link><description>D</description><item><title>I</title><link>http://e.com/i</link><description>D</description><author>real\@x.com</author></item></channel></rss>"
  [Syndicate] ok 11 - author preserved through round-trip
  [Syndicate] not ok 12 - dc:subject values stored
  [Syndicate] # Failed test 'dc:subject values stored'
  [Syndicate] # at t/27-audit-round-10.rakutest line 90
  [Syndicate] # expected: 'One|Two'
  [Syndicate] #      got: ''
  [Syndicate] not ok 13 - dc:subject 1 regenerated
  [Syndicate] # Failed test 'dc:subject 1 regenerated'
  [Syndicate] # at t/27-audit-round-10.rakutest line 92
  [Syndicate] # expected a match with: /'<dc:subject>One</dc:subject>'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rss version=\"2.0\"><channel><title>T</title><link>http://e.com</link><description>D</description><item><title>I</title><link>http://e.com/i</link><description>D</description></item></channel></rss>"
  [Syndicate] not ok 14 - dc:subject 2 regenerated
  [Syndicate] # Failed test 'dc:subject 2 regenerated'
  [Syndicate] # at t/27-audit-round-10.rakutest line 93
  [Syndicate] # expected a match with: /'<dc:subject>Two</dc:subject>'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rss version=\"2.0\"><channel><title>T</title><link>http://e.com</link><description>D</description><item><title>I</title><link>http://e.com/i</link><description>D</description></item></channel></rss>"
  [Syndicate] not ok 15 - xmlns:dc declared for subject-only item
  [Syndicate] # Failed test 'xmlns:dc declared for subject-only item'
  [Syndicate] # at t/27-audit-round-10.rakutest line 94
  [Syndicate] # expected a match with: /'xmlns:dc='/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rss version=\"2.0\"><channel><title>T</title><link>http://e.com</link><description>D</description><item><title>I</title><link>http://e.com/i</link><description>D</description></item></channel></rss>"
  [Syndicate] not ok 16 - dc:subject survives round-trip
  [Syndicate] # Failed test 'dc:subject survives round-trip'
  [Syndicate] # at t/27-audit-round-10.rakutest line 95
  [Syndicate] # expected: 'One|Two'
  [Syndicate] #      got: ''
  [Syndicate] ok 17 - plain <language> parsed as $.language
  [Syndicate] ok 18 - language regenerates as dc:language
  [Syndicate] ok 19 - xmlns:dc declared for dc:language
  [Syndicate] ok 20 - second to-hash unaffected by title mutation
  [Syndicate] not ok 21 - second to-hash unaffected by nested media mutation
  [Syndicate] # Failed test 'second to-hash unaffected by nested media mutation'
  [Syndicate] # at t/27-audit-round-10.rakutest line 131
  [Syndicate] # expected: 'http://e.com/v.mp4'
  [Syndicate] #      got: (Any)
  [Syndicate] ok 22 - mutation visible only in first result
  [Syndicate] ok 23 - third to-hash still pristine
  [Syndicate] ok 24 - failing extension parse is counted
  [Syndicate] ok 25 - failing extension parse is not noted to STDERR
  [Syndicate] ok 26 - missing semicolon tolerated
  [Syndicate] ok 27 - bare &amp decodes
  [Syndicate] ok 28 - bare digit-named entity decodes
  [Syndicate] ok 29 - encoded entity stays literal
  [Syndicate] ok 30 - greedy unknown name stays literal
  [Syndicate] ok 31 - ampersand without &name untouched
  [Syndicate] ok 32 - ampersand mid-word untouched
  [Syndicate] ok 33 - name terminated by space decodes
  [Syndicate] ok 34 - RSS 0.91 item dies without description
  [Syndicate] ok 35 - RSS 2.0 item dies without link
  [Syndicate] ok 36 - RSS 2.0 item dies without title
  [Syndicate] ok 37 - RSS 1.0 item dies without link
  [Syndicate] ok 38 - Atom item dies without title
  [Syndicate] ok 39 - JSON Feed item dies without title
  [Syndicate] ok 40 - RSS 2.0 title error message
  [Syndicate] ok 41 - RSS 2.0 link error message
  [Syndicate] # You failed 10 tests of 41
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/28-audit-round-11.rakutest
  [Syndicate] 1..60
  [Syndicate] ok 1 - B1: wrong-URI and bare unprefixed dc:subject rejected; URI-bound/default-ns matched
  [Syndicate] ok 2 - B1: exactly the namespace-correct dc:subject elements match
  [Syndicate] ok 3 - B1: media:content bound to a foreign URI is not media
  [Syndicate] ok 4 - B1: undeclared canonical media:thumbnail still matches (lenient)
  [Syndicate] ok 5 - B2: get-text-by-ns sees a prefix declared on the child element itself
  [Syndicate] ok 6 - B1: get-text-by-ns skips children bound to a wrong URI
  [Syndicate] ok 7 - B2: RSS item content:encoded picked up via child-declared prefix
  [Syndicate] ok 8 - B1: RSS item ignores content:encoded bound to a wrong URI
  [Syndicate] ok 9 - B1: RSS 1.0 parses with foreign-URI dc prefix
  [Syndicate] ok 10 - B1: wrong-URI dc:subject is not a channel category
  [Syndicate] ok 11 - B1: wrong-URI dc:language is ignored
  [Syndicate] ok 12 - B1 control: correct dc:subject becomes a category
  [Syndicate] ok 13 - B1 control: category value
  [Syndicate] ok 14 - B1 control: correct dc:language maps to language
  [Syndicate] ok 15 - B5: Atom feed parses despite one invalid entry
  [Syndicate] ok 16 - B5: valid entries retained, invalid skipped
  [Syndicate] ok 17 - B5: exactly one error recorded for the skipped entry
  [Syndicate] not ok 18 - B6: has-dc-date flag set from parsed dc:date
  [Syndicate] # Failed test 'B6: has-dc-date flag set from parsed dc:date'
  [Syndicate] # at t/28-audit-round-11.rakutest line 175
  [Syndicate] # expected: 'True'
  [Syndicate] #      got: 'False'
  [Syndicate] not ok 19 - B6: regenerated RSS 2.0 emits pubDate
  [Syndicate] # Failed test 'B6: regenerated RSS 2.0 emits pubDate'
  [Syndicate] # at t/28-audit-round-11.rakutest line 177
  [Syndicate] # expected a match with: /'<pubDate>'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rss version=\"2.0\"><channel><title>T</title><link>http://example.com</link><description>D</description><item><title>Item</title><link>http://example.com/1</link><description>d</description></item></channel></rss>"
  [Syndicate] not ok 20 - B6: regenerated RSS 2.0 keeps dc:date
  [Syndicate] # Failed test 'B6: regenerated RSS 2.0 keeps dc:date'
  [Syndicate] # at t/28-audit-round-11.rakutest line 178
  [Syndicate] # expected a match with: /'<dc:date>'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rss version=\"2.0\"><channel><title>T</title><link>http://example.com</link><description>D</description><item><title>Item</title><link>http://example.com/1</link><description>d</description></item></channel></rss>"
  [Syndicate] not ok 21 - B6: single dc:date, no duplicate
  [Syndicate] # Failed test 'B6: single dc:date, no duplicate'
  [Syndicate] # at t/28-audit-round-11.rakutest line 179
  [Syndicate] # expected: '1'
  [Syndicate] #      got: '0'
  [Syndicate] not ok 22 - B6: dc namespace declared on regeneration
  [Syndicate] # Failed test 'B6: dc namespace declared on regeneration'
  [Syndicate] # at t/28-audit-round-11.rakutest line 180
  [Syndicate] # expected a match with: /'xmlns:dc'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rss version=\"2.0\"><channel><title>T</title><link>http://example.com</link><description>D</description><item><title>Item</title><link>http://example.com/1</link><description>d</description></item></channel></rss>"
  [Syndicate] ok 23 - B6: builder RSS 2.0 emits pubDate
  [Syndicate] ok 24 - B6: builder RSS 2.0 emits no dc:date
  [Syndicate] ok 25 - B6: builder RSS 2.0 emits no dc namespace
  [Syndicate] not ok 26 - B6: RSS 1.0 dc:date regenerates exactly once
  [Syndicate] ok 27 - B6: RSS 1.0 emits no pubDate
  [Syndicate] not ok 28 - B6: RSS 1.0 dc namespace declared on regeneration
  [Syndicate] # Failed test 'B6: RSS 1.0 dc:date regenerates exactly once'
  [Syndicate] # at t/28-audit-round-11.rakutest line 213
  [Syndicate] # expected: '1'
  [Syndicate] #      got: '0'
  [Syndicate] # Failed test 'B6: RSS 1.0 dc namespace declared on regeneration'
  [Syndicate] # at t/28-audit-round-11.rakutest line 215
  [Syndicate] # expected a match with: /'xmlns:dc'/
  [Syndicate] #                   got: "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<rdf:RDF xmlns=\"http://purl.org/rss/1.0/\" xmlns:rdf=\"http://www.w3.org/1999/02/22-rdf-syntax-ns#\"><channel rdf:about=\"http://example.com\"><title>T</title><link>http://example.com</link><description>D</description><items><rdf:Seq><rdf:li rdf:resource=\"http://example.com/1\"/></rdf:Seq></items></channel><item rdf:about=\"http://example.com/1\"><title>Item</title><link>http://example.com/1</link><description>d</description></item></rdf:RDF>"
  [Syndicate] ok 29 - B3: mutating image in to-hash leaves the feed alone
  [Syndicate] ok 30 - B3: second to-hash is not corrupted
  [Syndicate] ok 31 - B3: Atom link-self not shared with to-hash
  [Syndicate] ok 32 - B3: Atom link-alternate not shared with to-hash
  [Syndicate] ok 33 - B3: Atom contributors not shared with to-hash
  [Syndicate] ok 34 - B3: second Atom to-hash is clean
  [Syndicate] ok 35 - B3: second Atom to-hash keeps contributors
  [Syndicate] ok 36 - B3: RSS 1.0 image not shared with to-hash
  [Syndicate] ok 37 - B4: no undefined values anywhere in RSS 2.0 to-hash
  [Syndicate] ok 38 - B4: absent enclosure length has no key (no null)
  [Syndicate] ok 39 - B4: enclosure url preserved
  [Syndicate] ok 40 - B4: RSS 2.0 to-json has no null
  [Syndicate] ok 41 - B4: to-json keeps enclosure url
  [Syndicate] ok 42 - B4: no undefined values in Atom to-hash
  [Syndicate] ok 43 - B4: absent author email has no key
  [Syndicate] ok 44 - B4: absent author uri has no key
  [Syndicate] ok 45 - B4: author name preserved
  [Syndicate] ok 46 - B4: Atom to-json has no null
  [Syndicate] ok 47 - B4: absent image description has no key
  [Syndicate] ok 48 - B4: image hash free of undefined values
  [Syndicate] ok 49 - B4: image-less-description to-json has no null
  [Syndicate] ok 50 - B7: image about is parsed
  [Syndicate] ok 51 - B7: degenerate image regenerates no dangling reference
  [Syndicate] ok 52 - B7 control: spec-correct image emits reference + element
  [Syndicate] ok 53 - sanitize keeps defined scalars
  [Syndicate] ok 54 - sanitize drops undefined scalars
  [Syndicate] ok 55 - sanitize recurses into hashes
  [Syndicate] ok 56 - sanitize keeps nested defined values
  [Syndicate] ok 57 - sanitize recurses into arrays
  [Syndicate] ok 58 - sanitize drops undefined array-element keys
  [Syndicate] ok 59 - sanitize output has no undefined values
  [Syndicate] ok 60 - sanitize returns a fresh clone
  [Syndicate] # You failed 7 tests of 60
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/29-audit-round-12.rakutest
  [Syndicate] 1..26
  [Syndicate] ok 1 - B1: V0_91 mutating image in to-hash leaves the feed alone
  [Syndicate] ok 2 - B1: V0_91 mutating skipHours in to-hash leaves the feed alone
  [Syndicate] ok 3 - B1: V0_91 mutating skipDays in to-hash leaves the feed alone
  [Syndicate] ok 4 - B2: Atom mutating categories in to-hash leaves the feed alone
  [Syndicate] ok 5 - B2: Atom entry categories round-trip unchanged
  [Syndicate] ok 6 - B3: builder item declares xmlns:content
  [Syndicate] ok 7 - B3: builder item emits content:encoded
  [Syndicate] ok 8 - B3: builder item declares xmlns:media
  [Syndicate] ok 9 - B3: builder item declares xmlns:itunes
  [Syndicate] ok 10 - B3: feed-embedded items stay byte-identical (no item-level xmlns)
  [Syndicate] ok 11 - B4: V1_0 direct construction emits dc:date (not pubDate)
  [Syndicate] ok 12 - B4: V1_0 direct construction emits no pubDate
  [Syndicate] ok 13 - B4: V0_91 direct construction emits no content:encoded
  [Syndicate] ok 14 - B4: V0_91 direct construction emits no pubDate
  [Syndicate] ok 15 - B4: V0_91 direct construction emits description
  [Syndicate] ok 16 - Q4: dc-only V1_0 builder item declares xmlns:dc
  [Syndicate] ok 17 - Q4: plain V1_0 builder item declares no namespaces
  [Syndicate] ok 18 - Q2: Atom to-hash updated matches XML updated
  [Syndicate] ok 19 - Q2: computed updated is the newest entry timestamp
  [Syndicate] Odd number of elements found where hash initializer expected:
  [Syndicate] Only saw: type object 'Any'
  [Syndicate]   in block <unit> at t/29-audit-round-12.rakutest line 142
  [Syndicate] # You planned 26 tests, but ran 19
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/30-audit-round-13.rakutest
  [Syndicate] 1..13
  [Syndicate] ok 1 - B1: to-hash uses the newest entry updated when it beats the feed updated
  [Syndicate] ok 2 - B1: to-hash updated matches XML updated when an entry is newer
  [Syndicate] ok 3 - B1: to-hash keeps the feed updated when it beats all entries
  [Syndicate] ok 4 - B2: standalone V1_0 item declares xmlns:rdf
  [Syndicate] ok 5 - B2: standalone V1_0 item emits rdf:about
  [Syndicate] ok 6 - B2: V1_0 item without about declares no namespaces
  [Syndicate] ok 7 - B2: builder V1_0 feed item still carries rdf:about
  [Syndicate] ok 8 - B2: builder V1_0 feed item stays namespace-bare (root declares rdf)
  [Syndicate] ok 9 - B3: foreign-namespace link rel=self is not captured
  [Syndicate] ok 10 - B3: foreign link is not re-emitted as atom:link
  [Syndicate] ok 11 - B3: atom-namespaced link rel=self is still parsed
  [Syndicate] ok 12 - B3: atom:link rel=self with empty href is not captured
  [Syndicate] ok 13 - B3: no empty atom:link is emitted
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/31-audit-round-14.rakutest
  [Syndicate] 1..38
  [Syndicate] ok 1 - R1: RSS 2.0 keeps all items despite bad item dates
  [Syndicate] ok 2 - R1: good item pubDate parsed
  [Syndicate] ok 3 - R1: bad pubDate item degrades to Nil
  [Syndicate] ok 4 - R1: structurally-invalid ISO date degrades to Nil
  [Syndicate] ok 5 - R1: bad channel pubDate degrades to Nil
  [Syndicate] ok 6 - R1: feed still parses with bad channel pubDate
  [Syndicate] ok 7 - R1: RSS 2.0 item with bad dc:date still parses
  [Syndicate] ok 8 - R1: bad dc:date degrades to Nil
  [Syndicate] ok 9 - R1: RSS 0.91 item with bad dc:date still parses
  [Syndicate] ok 10 - R1: 0.91 bad dc:date degrades to Nil
  [Syndicate] ok 11 - R1: RSS 1.0 item with bad dc:date still parses
  [Syndicate] ok 12 - R1: 1.0 bad dc:date degrades to Nil
  [Syndicate] ok 13 - R1: JSON Feed with bad item dates still parses
  [Syndicate] ok 14 - R1: bad date_published degrades to Nil
  [Syndicate] ok 15 - R1: bad date_modified degrades to Nil
  [Syndicate] ok 16 - R1: Atom skips entry with bad updated, keeps good one
  [Syndicate] ok 17 - R1: surviving Atom entry is the good one
  [Syndicate] ok 18 - R1: one error recorded for skipped entry
  [Syndicate] ok 19 - R1: Atom feed with bad feed-level updated still parses
  [Syndicate] ok 20 - R1: bad feed-level updated falls back to the entry timestamp
  [Syndicate] ok 21 - R1: timestamp-less Atom feed parses
  [Syndicate] ok 22 - R1: rendering a timestamp-less feed fails gracefully
  [Syndicate] ok 23 - R1: graceful message, not X::Temporal::OutOfRange
  [Syndicate] ok 24 - R3: non-Str title rejected
  [Syndicate] ok 25 - R3: graceful type message for title
  [Syndicate] ok 26 - R3: non-Str version rejected
  [Syndicate] ok 27 - R3: graceful type message for version
  [Syndicate] ok 28 - R3: non-Str item id rejected
  [Syndicate] ok 29 - R3: graceful type message for item id
  [Syndicate] ok 30 - R4: decimal ref without ; decodes
  [Syndicate] ok 31 - R4: decimal ref with ; still decodes
  [Syndicate] ok 32 - R4: hex ref without ; decodes
  [Syndicate] ok 33 - R4: named ref without ; still decodes
  [Syndicate] ok 34 - R4: entity-free text untouched
  [Syndicate] ok 35 - R5: rss091-feed without description fails
  [Syndicate] ok 36 - R5: failure names the missing description
  [Syndicate] ok 37 - R5: rss091-feed with description succeeds
  [Syndicate] ok 38 - R2: concurrent to-hash calls all return valid hashes
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/32-audit-round-15.rakutest
  [Syndicate] 1..28
  [Syndicate] ok 1 - R1: high surrogate stays literal
  [Syndicate] ok 2 - R1: low surrogate stays literal
  [Syndicate] ok 3 - R1: decimal surrogate stays literal
  [Syndicate] ok 4 - R1: max valid codepoint decodes
  [Syndicate] ok 5 - R1: out-of-range codepoint stays literal
  [Syndicate] ok 6 - R1: normal refs still decode
  [Syndicate] ok 7 - R1: feed with a surrogate ref keeps it as literal text
  [Syndicate] ok 8 - R1: to-hash string is UTF-8-encodable
  [Syndicate] ok 9 - R1: item text is UTF-8-encodable
  [Syndicate] ok 10 - R1: sibling item decoded normally
  [Syndicate] ok 11 - R2: no feed-level updated stored
  [Syndicate] ok 12 - R2: to-hash computes the newest entry updated
  [Syndicate] ok 13 - R2: XML emits the computed updated
  [Syndicate] ok 14 - R2: fully timestamp-less feed has no updated in to-hash
  [Syndicate] ok 15 - R2: rendering a fully timestamp-less feed fails
  [Syndicate] ok 16 - R2: failure is the documented graceful die
  [Syndicate] ok 17 - R3: Content-Type with space before ; accepted
  [Syndicate] ok 18 - R3: text/html with parameters still rejected
  [Syndicate] ok 19 - R4: space-separated HH:MM parses as midnight-second
  [Syndicate] ok 20 - R4: space-separated HH:MM with offset parses
  [Syndicate] ok 21 - R4: RFC 2822 date-only parses as midnight UTC
  [Syndicate] ok 22 - R4: HH:MM:SS form unchanged
  [Syndicate] ok 23 - R4: full RFC 2822 unchanged
  [Syndicate] ok 24 - R4: bare ISO date unchanged
  [Syndicate] ok 25 - R5: parse-feed-or-nil parses JSON Feed
  [Syndicate] ok 26 - R5: JSON Feed increments feeds-parsed
  [Syndicate] ok 27 - R5: non-feed records nothing
  [Syndicate] ok 28 - R5: non-feed did not increment feeds-parsed
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/33-audit-round-16.rakutest
  [Syndicate] 1..66
  [Syndicate] ok 1 - 2a: valueless <base href> yields no URL, no crash
  [Syndicate] ok 2 - 2a: valued <base href> still returned
  [Syndicate] ok 3 - 8: non-string home_page_url rejected
  [Syndicate] ok 4 - 8: home_page_url error names the field
  [Syndicate] ok 5 - 8: non-string description rejected
  [Syndicate] ok 6 - 8: description error names the field
  [Syndicate] ok 7 - 8: non-string generator rejected
  [Syndicate] ok 8 - 8: generator error names the field
  [Syndicate] ok 9 - 8: non-string feed_url rejected
  [Syndicate] ok 10 - 8: feed_url error names the field
  [Syndicate] ok 11 - 8: non-string user_comment rejected
  [Syndicate] ok 12 - 8: user_comment error names the field
  [Syndicate] ok 13 - 8: non-string next_url rejected
  [Syndicate] ok 14 - 8: next_url error names the field
  [Syndicate] ok 15 - 8: non-string icon rejected
  [Syndicate] ok 16 - 8: icon error names the field
  [Syndicate] ok 17 - 8: non-string favicon rejected
  [Syndicate] ok 18 - 8: favicon error names the field
  [Syndicate] ok 19 - 8: non-string locale rejected
  [Syndicate] ok 20 - 8: locale error names the field
  [Syndicate] ok 21 - 8: non-string language rejected when no locale
  [Syndicate] ok 22 - 8: language error names the field
  [Syndicate] ok 23 - 8: language used when locale absent
  [Syndicate] ok 24 - 8: feed_url parsed
  [Syndicate] ok 25 - 4: capital-X hex reference decodes
  [Syndicate] ok 26 - 4: lowercase-x hex reference still decodes
  [Syndicate] ok 27 - 4: surrogate hex reference stays literal
  [Syndicate] ok 28 - 4: decimal reference still decodes
  [Syndicate] ok 29 - 6: feed-format(0.0.92) is RSS2
  [Syndicate] ok 30 - 6: parse-feed accepts 0.92
  [Syndicate] ok 31 - 6: feed-format(0.0.93) is RSS2
  [Syndicate] ok 32 - 6: parse-feed accepts 0.93
  [Syndicate] ok 33 - 6: feed-format(0.0.94) is RSS2
  [Syndicate] ok 34 - 6: parse-feed accepts 0.94
  [Syndicate] ok 35 - 6: all three legacy versions accepted
  [Syndicate] ok 36 - 7: feed-format rejects empty suffix
  [Syndicate] ok 37 - 7: parse-feed-or-nil returns Nil for empty suffix
  [Syndicate] ok 38 - 7: proper version still detected
  [Syndicate] ok 39 - 9: dc-creators alone triggers the xmlns:dc declaration
  [Syndicate] ok 40 - 5: undeclared canonical prefix still matches
  [Syndicate] ok 41 - 5: no false positive when a different URI is actually bound
  [Syndicate] ok 42 - 11: invalid ttl not set on feed
  [Syndicate] ok 43 - 11: invalid ttl records no Stats error
  [Syndicate] ok 44 - 3: Atom element-form markup preserved
  [Syndicate] ok 45 - 3: Atom content flagged as markup
  [Syndicate] ok 46 - 3: Atom markup round-trip is byte-stable
  [Syndicate] ok 47 - 3: RSS element-form markup preserved
  [Syndicate] ok 48 - 3: RSS markup content stable across parse/regen/reparse
  [Syndicate] ok 49 - 3: RSS entity+element content decoded to markup
  [Syndicate] ok 50 - 3: RSS mixed content stable across parse/regen/reparse
  [Syndicate] ok 51 - 3: RSS inter-element whitespace stable across parse/regen/reparse
  [Syndicate] ok 52 - 3: entity-encoded content still decoded to plain text
  [Syndicate] ok 53 - 3: entity-encoded content stable (no double encoding)
  [Syndicate] ok 54 - 3: V1_0 element-form markup preserved
  [Syndicate] ok 55 - 3: V1_0 markup content stable across parse/regen/reparse
  [Syndicate] ok 56 - 13: title parsed
  [Syndicate] ok 57 - 13: link parsed
  [Syndicate] ok 58 - 13: description parsed
  [Syndicate] ok 59 - 13: author parsed
  [Syndicate] ok 60 - 13: both categories parsed
  [Syndicate] ok 61 - 13: comments parsed
  [Syndicate] ok 62 - 13: source parsed
  [Syndicate] ok 63 - 13: pubDate parsed
  [Syndicate] ok 64 - 13: guid parsed
  [Syndicate] ok 65 - 13: enclosure parsed
  [Syndicate] ok 66 - 13: content:encoded parsed
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/34-audit-round-17.rakutest
  [Syndicate] 1..56
  [Syndicate] ok 1 - 1: «Wed, 1 Jan 2020 00:00:00 UT» parses
  [Syndicate] ok 2 - 1: «Tue, 2 Feb 2021 12:00:00 GMT» parses
  [Syndicate] ok 3 - 1: «Wed, 1 Jan 2020 00:00:00 GMT» parses
  [Syndicate] ok 4 - 1: «Wed, 01 Jan 2020 10:00 +0000» parses
  [Syndicate] ok 5 - 1: «Sun, 08 Jul 2026 10:00:00+0000» parses
  [Syndicate] ok 6 - 1: «15 Jan 2024» parses
  [Syndicate] ok 7 - 1: «Mon, 15 Jan 2024 8:30:00 GMT» parses
  [Syndicate] ok 8 - 1: «Mon, 15 Jan 2024 8:30 AM EST» parses
  [Syndicate] ok 9 - 1: «Mon, 15 Jan 2024 10:00:00 +05:30» parses
  [Syndicate] ok 10 - 1: synthesized weekday is correct (15 Jan 2024 is a Monday)
  [Syndicate] ok 11 - 1: synthesized weekday is correct (29 Feb 2024 is a Thursday)
  [Syndicate] ok 12 - 1: bogus day still Nil
  [Syndicate] ok 13 - 1: bogus month-day still Nil
  [Syndicate] ok 14 - 1: space-separated ISO unaffected
  [Syndicate] ok 15 - 1: T-separated ISO with colon offset unaffected
  [Syndicate] ok 16 - 2: non-string url rejected
  [Syndicate] ok 17 - 2: url error is graceful and names the field
  [Syndicate] ok 18 - 2: non-string summary rejected
  [Syndicate] ok 19 - 2: summary error is graceful and names the field
  [Syndicate] ok 20 - 2: non-string content_html rejected
  [Syndicate] ok 21 - 2: content_html error is graceful and names the field
  [Syndicate] ok 22 - 2: non-string content_text rejected
  [Syndicate] ok 23 - 2: content_text error is graceful and names the field
  [Syndicate] ok 24 - 2: non-string external_url rejected
  [Syndicate] ok 25 - 2: external_url error is graceful and names the field
  [Syndicate] ok 26 - 2: non-string image rejected
  [Syndicate] ok 27 - 2: image error is graceful and names the field
  [Syndicate] ok 28 - 2: non-string banner_image rejected
  [Syndicate] ok 29 - 2: banner_image error is graceful and names the field
  [Syndicate] ok 30 - 2: non-string title rejected
  [Syndicate] ok 31 - 2: title error names the field
  [Syndicate] ok 32 - 2: non-string id rejected
  [Syndicate] ok 33 - 2: id falls back to url
  [Syndicate] ok 34 - 2: parse-feed propagates the graceful die
  [Syndicate] ok 35 - 2: parse-feed surfaces the graceful message, not X::TypeCheck
  [Syndicate] ok 36 - 2: parse-feed records the error
  [Syndicate] ok 37 - 5: RSS item to-hash has no active-ext key
  [Syndicate] Use of uninitialized value %h{'dc-creators'} of type Any in string context.
  [Syndicate] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Syndicate]   in block  at t/34-audit-round-17.rakutest line 88
  [Syndicate] not ok 38 - 5: extension data still present
  [Syndicate] # Failed test '5: extension data still present'
  [Syndicate] # at t/34-audit-round-17.rakutest line 88
  [Syndicate] # expected: 'Jane'
  [Syndicate] #      got: ''
  [Syndicate] ok 39 - 5: item JSON is clean of active-ext
  [Syndicate] ok 40 - 6: good result
  [Syndicate] ok 41 - 6: good feeds-parsed delta
  [Syndicate] ok 42 - 6: good errors delta
  [Syndicate] ok 43 - 6: nochan result
  [Syndicate] ok 44 - 6: nochan feeds-parsed delta
  [Syndicate] ok 45 - 6: nochan errors delta
  [Syndicate] ok 46 - 6: html result
  [Syndicate] ok 47 - 6: html feeds-parsed delta
  [Syndicate] ok 48 - 6: html errors delta
  [Syndicate] ok 49 - V0_91: title
  [Syndicate] ok 50 - V0_91: link
  [Syndicate] ok 51 - V0_91: description
  [Syndicate] ok 52 - V0_91: guid -> id
  [Syndicate] ok 53 - V0_91: comments
  [Syndicate] ok 54 - V0_91: source
  [Syndicate] ok 55 - date_modified: parse path round-trips date_modified
  [Syndicate] ok 56 - date_modified: builder item with only updated emits no date_modified
  [Syndicate] # You failed 1 test of 56
  [Syndicate] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6 t/35-convert.rakutest
  [Syndicate] 1..195
  [Syndicate] ok 1 - rss: title mapped
  [Syndicate] ok 2 - rss: link mapped
  [Syndicate] ok 3 - rss: description mapped
  [Syndicate] ok 4 - rss: copyright -> rights
  [Syndicate] ok 5 - rss: managingEditor -> author email
  [Syndicate] ok 6 - rss: lastBuildDate -> updated
  [Syndicate] ok 7 - rss: one entry
  [Syndicate] ok 8 - rss item: title
  [Syndicate] ok 9 - rss item: link
  [Syndicate] ok 10 - rss item: summary
  [Syndicate] ok 11 - rss item: guid -> id
  [Syndicate] ok 12 - rss item: author
  [Syndicate] ok 13 - rss item: categories
  [Syndicate] ok 14 - rss item: enclosure
  [Syndicate] ok 15 - rss item: content
  [Syndicate] ok 16 - rss091: title mapped
  [Syndicate] ok 17 - rss091: link mapped
  [Syndicate] ok 18 - rss091: description mapped
  [Syndicate] ok 19 - rss091: copyright -> rights
  [Syndicate] ok 20 - rss091: managingEditor -> author email
  [Syndicate] ok 21 - rss091: lastBuildDate -> updated
  [Syndicate] ok 22 - rss091: one entry
  [Syndicate] ok 23 - rss091 item: title
  [Syndicate] ok 24 - rss091 item: link
  [Syndicate] ok 25 - rss091 item: summary
  [Syndicate] ok 26 - rss091 item: id falls back to link
  [Syndicate] ok 27 - rss1: title mapped
  [Syndicate] ok 28 - rss1: link mapped
  [Syndicate] ok 29 - rss1: description mapped
  [Syndicate] ok 30 - rss1: about -> id
  [Syndicate] ok 31 - rss1: dc:subject -> feed categories
  [Syndicate] ok 32 - rss1: one entry
  [Syndicate] ok 33 - rss1 item: title
  [Syndicate] ok 34 - rss1 item: link
  [Syndicate] ok 35 - rss1 item: summary
  [Syndicate] ok 36 - rss1 item: about -> id
  [Syndicate] not ok 37 - rss1 item: dc:date -> updated
  [Syndicate] # Failed test 'rss1 item: dc:date -> updated'
  [Syndicate] # at t/35-convert.rakutest line 180
  [Syndicate] not ok 38 - rss1 item: dc:creator -> author
  [Syndicate] # Failed test 'rss1 item: dc:creator -> author'
  [Syndicate] # at t/35-convert.rakutest line 181
  [Syndicate] # expected: 'Jane'
  [Syndicate] #      got: (Str)
  [Syndicate] ok 39 - atom: title mapped
  [Syndicate] ok 40 - atom: primary alternate -> link
  [Syndicate] ok 41 - atom: subtitle -> description
  [Syndicate] ok 42 - atom: id mapped
  [Syndicate] ok 43 - atom: rights mapped
  [Syndicate] ok 44 - atom: icon mapped
  [Syndicate] ok 45 - atom: logo mapped
  [Syndicate] ok 46 - atom: updated mapped
  [Syndicate] ok 47 - atom: author name
  [Syndicate] ok 48 - atom: author email
  [Syndicate] ok 49 - atom: author uri
  [Syndicate] ok 50 - atom: feed categories
  [Syndicate] ok 51 - atom: link-self -> atom-self-link
  [Syndicate] ok 52 - atom: one entry
  [Syndicate] ok 53 - atom item: title
  [Syndicate] ok 54 - atom item: link
  [Syndicate] ok 55 - atom item: summary
  [Syndicate] ok 56 - atom item: id
  [Syndicate] ok 57 - atom item: content
  [Syndicate] ok 58 - atom item: published
  [Syndicate] ok 59 - atom item: author name
  [Syndicate] ok 60 - atom item: categories
  [Syndicate] ok 61 - json: title mapped
  [Syndicate] ok 62 - json: home_page_url -> link
  [Syndicate] ok 63 - json: description mapped
  [Syndicate] ok 64 - json: feed_url mapped
  [Syndicate] ok 65 - json: version mapped
  [Syndicate] ok 66 - json: icon mapped
  [Syndicate] ok 67 - json: author name
  [Syndicate] ok 68 - json: author url -> uri
  [Syndicate] ok 69 - json: one entry
  [Syndicate] ok 70 - json item: title
  [Syndicate] ok 71 - json item: url -> link
  [Syndicate] ok 72 - json item: summary
  [Syndicate] ok 73 - json item: id
  [Syndicate] ok 74 - json item: date_published -> published
  [Syndicate] ok 75 - json item: date_modified -> updated
  [Syndicate] ok 76 - json item: content_html -> content
  [Syndicate] ok 77 - json item: authors[0] -> author
  [Syndicate] ok 78 - json item: tags -> categories
  [Syndicate] ok 79 - json -> RSS2: feed title survives
  [Syndicate] ok 80 - json -> RSS2: has items
  [Syndicate] ok 81 - json -> RSS2: first item title
  [Syndicate] ok 82 - json -> RSS091: feed title survives
  [Syndicate] ok 83 - json -> RSS091: has items
  [Syndicate] ok 84 - json -> RSS091: first item title
  [Syndicate] ok 85 - json -> RSS1: feed title survives
  [Syndicate] ok 86 - json -> RSS1: has items
  [Syndicate] ok 87 - json -> RSS1: first item title
  [Syndicate] ok 88 - json -> Atom: feed title survives
  [Syndicate] ok 89 - json -> Atom: has items
  [Syndicate] ok 90 - json -> Atom: first item title
  [Syndicate] ok 91 - json -> JSONFeedFmt: feed title survives
  [Syndicate] ok 92 - json -> JSONFeedFmt: has items
  [Syndicate] ok 93 - json -> JSONFeedFmt: first item title
  [Syndicate] ok 94 - rss1 -> RSS2: feed title survives
  [Syndicate] ok 95 - rss1 -> RSS2: has items
  [Syndicate] ok 96 - rss1 -> RSS2: first item title
  [Syndicate] ok 97 - rss1 -> RSS091: feed title survives
  [Syndicate] ok 98 - rss1 -> RSS091: has items
  [Syndicate] ok 99 - rss1 -> RSS091: first item title
  [Syndicate] ok 100 - rss1 -> RSS1: feed title survives
  [Syndicate] ok 101 - rss1 -> RSS1: has items
  [Syndicate] ok 102 - rss1 -> RSS1: first item title
  [Syndicate] ok 103 - rss1 -> Atom: feed title survives
  [Syndicate] ok 104 - rss1 -> Atom: has items
  [Syndicate] ok 105 - rss1 -> Atom: first item title
  [Syndicate] ok 106 - rss1 -> JSONFeedFmt: feed title survives
  [Syndicate] ok 107 - rss1 -> JSONFeedFmt: has items
  [Syndicate] ok 108 - rss1 -> JSONFeedFmt: first item title
  [Syndicate] ok 109 - atom -> RSS2: feed title survives
  [Syndicate] ok 110 - atom -> RSS2: has items
  [Syndicate] ok 111 - atom -> RSS2: first item title
  [Syndicate] ok 112 - atom -> RSS091: feed title survives
  [Syndicate] ok 113 - atom -> RSS091: has items
  [Syndicate] ok 114 - atom -> RSS091: first item title
  [Syndicate] ok 115 - atom -> RSS1: feed title survives
  [Syndicate] ok 116 - atom -> RSS1: has items
  [Syndicate] ok 117 - atom -> RSS1: first item title
  [Syndicate] ok 118 - atom -> Atom: feed title survives
  [Syndicate] ok 119 - atom -> Atom: has items
  [Syndicate] ok 120 - atom -> Atom: first item title
  [Syndicate] ok 121 - atom -> JSONFeedFmt: feed title survives
  [Syndicate] ok 122 - atom -> JSONFeedFmt: has items
  [Syndicate] ok 123 - atom -> JSONFeedFmt: first item title
  [Syndicate] ok 124 - rss -> RSS2: feed title survives
  [Syndicate] ok 125 - rss -> RSS2: has items
  [Syndicate] ok 126 - rss -> RSS2: first item title
  [Syndicate] ok 127 - rss -> RSS091: feed title survives
  [Syndicate] ok 128 - rss -> RSS091: has items
  [Syndicate] ok 129 - rss -> RSS091: first item title
  [Syndicate] ok 130 - rss -> RSS1: feed title survives
  [Syndicate] ok 131 - rss -> RSS1: has items
  [Syndicate] ok 132 - rss -> RSS1: first item title
  [Syndicate] ok 133 - rss -> Atom: feed title survives
  [Syndicate] ok 134 - rss -> Atom: has items
  [Syndicate] ok 135 - rss -> Atom: first item title
  [Syndicate] ok 136 - rss -> JSONFeedFmt: feed title survives
  [Syndicate] ok 137 - rss -> JSONFeedFmt: has items
  [Syndicate] ok 138 - rss -> JSONFeedFmt: first item title
  [Syndicate] ok 139 - rss091 -> RSS2: feed title survives
  [Syndicate] ok 140 - rss091 -> RSS2: has items
  [Syndicate] ok 141 - rss091 -> RSS2: first item title
  [Syndicate] ok 142 - rss091 -> RSS091: feed title survives
  [Syndicate] ok 143 - rss091 -> RSS091: has items
  [Syndicate] ok 144 - rss091 -> RSS091: first item title
  [Syndicate] ok 145 - rss091 -> RSS1: feed title survives
  [Syndicate] ok 146 - rss091 -> RSS1: has items
  [Syndicate] ok 147 - rss091 -> RSS1: first item title
  [Syndicate] ok 148 - rss091 -> Atom: feed title survives
  [Syndicate] ok 149 - rss091 -> Atom: has items
  [Syndicate] ok 150 - rss091 -> Atom: first item title
  [Syndicate] ok 151 - rss091 -> JSONFeedFmt: feed title survives
  [Syndicate] ok 152 - rss091 -> JSONFeedFmt: has items
  [Syndicate] ok 153 - rss091 -> JSONFeedFmt: first item title
  [Syndicate] ok 154 - rss->atom: lastBuildDate -> feed updated
  [Syndicate] ok 155 - rss->atom: item pubDate -> entry updated
  [Syndicate] ok 156 - rss->atom: managingEditor -> author email
  [Syndicate] ok 157 - atom->rss: entry updated -> pubDate
  [Syndicate] ok 158 - atom->rss: feed updated -> lastBuildDate
  [Syndicate] ok 159 - atom->rss: author email -> managingEditor
  [Syndicate] ok 160 - atom->rss: feed categories survive
  [Syndicate] ok 161 - json->atom: content_html -> type=html
  [Syndicate] ok 162 - json->atom: tags -> category
  [Syndicate] ok 163 - json->atom: date_modified -> updated
  [Syndicate] ok 164 - json->atom: date_published -> published
  [Syndicate] ok 165 - json->rss: date_modified -> pubDate
  [Syndicate] ok 166 - json->rss: authors[0] name -> author
  [Syndicate] ok 167 - json->rss: tags -> category
  [Syndicate] ok 168 - json->rss: content_html -> content:encoded
  [Syndicate] ok 169 - rss->json: content:encoded -> content_html
  [Syndicate] ok 170 - rss->json: author -> authors[0]
  [Syndicate] ok 171 - rss->json: category -> tags
  [Syndicate] ok 172 - rss1->rss: dc:subject -> feed categories
  [Syndicate] not ok 173 - rss1->rss: dc:creator -> item author
  [Syndicate] # Failed test 'rss1->rss: dc:creator -> item author'
  [Syndicate] # at t/35-convert.rakutest line 299
  [Syndicate] # expected: 'Jane'
  [Syndicate] #      got: (Str)
  [Syndicate] ok 174 - string target format is rejected (enum coercion fails)
  [Syndicate] ok 175 - coercion error names FeedFormat
  [Syndicate] ok 176 - enum target format accepted
  [Syndicate] ok 177 - atom without link -> rss dies
  [Syndicate] ok 178 - missing link error is clear
  [Syndicate] ok 179 - atom without subtitle -> rss dies
  [Syndicate] ok 180 - missing description error is clear
  [Syndicate] ok 181 - item without summary -> rss091 dies
  [Syndicate] ok 182 - missing item summary error is clear
  [Syndicate] ok 183 - enum RSS2 accepted
  [Syndicate] ok 184 - enum RSS1 accepted
  [Syndicate] ok 185 - enum RSS091 accepted
  [Syndicate] ok 186 - convert-to-rss emits RSS
  [Syndicate] ok 187 - convert-to-atom emits Atom
  [Syndicate] ok 188 - convert-to-json emits JSON
  [Syndicate] ok 189 - convert-to-rss1 emits RSS 1.0
  [Syndicate] Warning: RSS 0.91 does not support feed-level categories; 1 categories dropped
  [Syndicate]   in method rss091-feed at /home/coke/sandbox/blin/data/zef-data/tmp/37de0e74a03acd7c7cbc2a6ec5876703c22c7a6c.tar.gz/Syndicate-0.0.6/lib/Syndicate/Builder/Feed.rakumod (Syndicate::Builder::Feed) line 308
  [Syndicate] ok 190 - convert-to-rss091 emits RSS 0.91
  [Syndicate] ok 191 - convert-to-json result reparses
  [Syndicate] ok 192 - convert-to-atom result reparses
  [Syndicate] ok 193 - instance call returns a populated builder
  [Syndicate] ok 194 - instance call populates the receiver
  [Syndicate] ok 195 - type-object call creates a populated builder
  [Syndicate] # You failed 3 tests of 195
  ===> Testing [FAIL]: Syndicate:ver<0.0.6>:auth<zef:sasha>
  [Syndicate] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Syndicate:ver<0.0.6>:auth<zef:sasha>
  ===> Install [OK] for Syndicate:ver<0.0.6>:auth<zef:sasha>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 6min 3.527s
               CPU time consumed: 6min 21.939s
                     Memory peak: 2.2G (swap: 509.6M)

  ```
  </details>
* [ ] [LLM::Character](https://raku.land/zef:apogee/LLM::Character) – Fail, Bisected: [fdc7d63](https://github.com/rakudo/rakudo/commit/fdc7d635717d90c06826668936cd708d30fd19c4)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p363663-i382689.service; invocation ID: 6ce0db8492a448b893e9d55e4df9eb81
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: LLM::Character
  ===> Found: LLM::Character:ver<0.2.3>:auth<zef:apogee> [via Zef::Repository::Ecosystems<fez>]
  [LLM::Character] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788474722.363664.354.543658155021/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz https://360.zef.pm/L/LM/LLM_CHARACTER/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  ===> Fetching [OK]: LLM::Character:ver<0.2.3>:auth<zef:apogee> to /home/coke/sandbox/blin/data/zef-data/tmp/1788474722.363664.354.543658155021/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  [LLM::Character] Command: tar -t -f ./f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  [LLM::Character] Command: tar -xvf ./f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz -C ../f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  ===> Extraction [OK]: LLM::Character to /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  ===> Testing: LLM::Character:ver<0.2.3>:auth<zef:apogee>
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/01-basic.rakutest
  [LLM::Character] ok 1 - replace me
  [LLM::Character] 1..1
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/02-minimal_lorebook.rakutest
  [LLM::Character] 1..29
  [LLM::Character] ok 1 - lorebook_minimal.json: lorebook is defined
  [LLM::Character] ok 2 - lorebook_minimal.json: is Lorebook
  [LLM::Character] ok 3 - lorebook_minimal.json: has entries
  [LLM::Character] ok 4 - lorebook_minimal.json: extensions defined
  [LLM::Character] ok 5 - lorebook_minimal.json: name is str or undefined
  [LLM::Character] ok 6 - lorebook_minimal.json: description is str or undefined
  [LLM::Character] ok 7 - lorebook_minimal.json: scan_depth is int or undefined
  [LLM::Character] ok 8 - lorebook_minimal.json: token_budget is int or undefined
  [LLM::Character] ok 9 - lorebook_minimal.json: recursive_scanning is bool or undefined
  [LLM::Character] ok 10 - lorebook_minimal.json: entry 0 is Entry
  [LLM::Character] ok 11 - lorebook_minimal.json: entry 0 has keys
  [LLM::Character] ok 12 - lorebook_minimal.json: entry 0 has content
  [LLM::Character] ok 13 - lorebook_minimal.json: entry 0 enabled is Bool
  [LLM::Character] ok 14 - lorebook_minimal.json: entry 0 insertion_order is Int
  [LLM::Character] ok 15 - lorebook_minimal.json: entry 0 use_regex is defined
  [LLM::Character] ok 16 - lorebook_minimal.json: entry 0 case_sensitive sane
  [LLM::Character] ok 17 - lorebook_minimal.json: entry 0 constant sane
  [LLM::Character] ok 18 - lorebook_minimal.json: entry 0 selective sane
  [LLM::Character] ok 19 - lorebook_minimal.json: entry 0 secondary_keys sane
  [LLM::Character] ok 20 - lorebook_minimal.json: entry 0 priority sane
  [LLM::Character] ok 21 - lorebook_minimal.json: entry 0 comment sane
  [LLM::Character] ok 22 - lorebook_minimal.json: entry 0 position sane
  [LLM::Character] ok 23 - lorebook_minimal.json: entry 0 extensions sane
  [LLM::Character] ok 24 - lorebook_minimal.json: correct first key
  [LLM::Character] ok 25 - lorebook_minimal.json: correct second key
  [LLM::Character] ok 26 - lorebook_minimal.json: correct content
  [LLM::Character] ok 27 - lorebook_minimal.json: correctly enabled
  [LLM::Character] ok 28 - lorebook_minimal.json: correct insertion order
  [LLM::Character] ok 29 - lorebook_minimal.json: regex disabled correctly
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/03-all_fields_lorebook.rakutest
  [LLM::Character] 1..49
  [LLM::Character] ok 1 - lorebook_valid.json: lorebook is defined
  [LLM::Character] ok 2 - lorebook_valid.json: is Lorebook
  [LLM::Character] ok 3 - lorebook_valid.json: has entries
  [LLM::Character] ok 4 - lorebook_valid.json: extensions defined
  [LLM::Character] ok 5 - lorebook_valid.json: name is str or undefined
  [LLM::Character] ok 6 - lorebook_valid.json: description is str or undefined
  [LLM::Character] ok 7 - lorebook_valid.json: scan_depth is int or undefined
  [LLM::Character] ok 8 - lorebook_valid.json: token_budget is int or undefined
  [LLM::Character] ok 9 - lorebook_valid.json: recursive_scanning is bool or undefined
  [LLM::Character] ok 10 - lorebook_valid.json: entry 0 is Entry
  [LLM::Character] ok 11 - lorebook_valid.json: entry 0 has keys
  [LLM::Character] ok 12 - lorebook_valid.json: entry 0 has content
  [LLM::Character] ok 13 - lorebook_valid.json: entry 0 enabled is Bool
  [LLM::Character] ok 14 - lorebook_valid.json: entry 0 insertion_order is Int
  [LLM::Character] ok 15 - lorebook_valid.json: entry 0 use_regex is defined
  [LLM::Character] ok 16 - lorebook_valid.json: entry 0 case_sensitive sane
  [LLM::Character] ok 17 - lorebook_valid.json: entry 0 constant sane
  [LLM::Character] ok 18 - lorebook_valid.json: entry 0 selective sane
  [LLM::Character] ok 19 - lorebook_valid.json: entry 0 secondary_keys sane
  [LLM::Character] ok 20 - lorebook_valid.json: entry 0 priority sane
  [LLM::Character] ok 21 - lorebook_valid.json: entry 0 comment sane
  [LLM::Character] ok 22 - lorebook_valid.json: entry 0 position sane
  [LLM::Character] ok 23 - lorebook_valid.json: entry 0 extensions sane
  [LLM::Character] ok 24 - lorebook_valid.json: correct lorebook name
  [LLM::Character] ok 25 - lorebook_valid.json: correct lorebook description
  [LLM::Character] ok 26 - lorebook_valid.json: correct scan depth
  [LLM::Character] ok 27 - lorebook_valid.json: correct token budget
  [LLM::Character] ok 28 - lorebook_valid.json: correct recursive scanning
  [LLM::Character] ok 29 - lorebook_valid.json: correct extension 'testString'
  [LLM::Character] ok 30 - lorebook_valid.json: correct extension 'testBool'
  [LLM::Character] ok 31 - lorebook_valid.json: correct extension 'testInt'
  [LLM::Character] ok 32 - lorebook_valid.json: correct first key
  [LLM::Character] ok 33 - lorebook_valid.json: correct second key
  [LLM::Character] ok 34 - lorebook_valid.json: correct content
  [LLM::Character] ok 35 - lorebook_valid.json: correct entry extension 'testString'
  [LLM::Character] ok 36 - lorebook_valid.json: correct entry extension 'testBool'
  [LLM::Character] ok 37 - lorebook_valid.json: correct entry extension 'testInt'
  [LLM::Character] ok 38 - lorebook_valid.json: correctly enabled
  [LLM::Character] ok 39 - lorebook_valid.json: correct insertion order
  [LLM::Character] ok 40 - lorebook_valid.json: correct case sensitive
  [LLM::Character] ok 41 - lorebook_valid.json: regex disabled correctly
  [LLM::Character] ok 42 - lorebook_valid.json: constant correctly false
  [LLM::Character] ok 43 - lorebook_valid.json: name correctly baz
  [LLM::Character] ok 44 - lorebook_valid.json: correct entry priority
  [LLM::Character] ok 45 - lorebook_valid.json: correct entry id
  [LLM::Character] ok 46 - lorebook.json: correct entry comment
  [LLM::Character] ok 47 - lorebook_valid.json: entry correctly set to selective
  [LLM::Character] ok 48 - lorebook_valid.json: correct entry secondary key
  [LLM::Character] ok 49 - lorebook_valid.json: correct entry position
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/04-enclosed_minimal_lorebook.rakutest
  [LLM::Character] 1..29
  [LLM::Character] ok 1 - lorebook_enclosed_minimal.json: lorebook is defined
  [LLM::Character] ok 2 - lorebook_enclosed_minimal.json: is Lorebook
  [LLM::Character] ok 3 - lorebook_enclosed_minimal.json: has entries
  [LLM::Character] ok 4 - lorebook_enclosed_minimal.json: extensions defined
  [LLM::Character] ok 5 - lorebook_enclosed_minimal.json: name is str or undefined
  [LLM::Character] ok 6 - lorebook_enclosed_minimal.json: description is str or undefined
  [LLM::Character] ok 7 - lorebook_enclosed_minimal.json: scan_depth is int or undefined
  [LLM::Character] ok 8 - lorebook_enclosed_minimal.json: token_budget is int or undefined
  [LLM::Character] ok 9 - lorebook_enclosed_minimal.json: recursive_scanning is bool or undefined
  [LLM::Character] ok 10 - lorebook_enclosed_minimal.json: entry 0 is Entry
  [LLM::Character] ok 11 - lorebook_enclosed_minimal.json: entry 0 has keys
  [LLM::Character] ok 12 - lorebook_enclosed_minimal.json: entry 0 has content
  [LLM::Character] ok 13 - lorebook_enclosed_minimal.json: entry 0 enabled is Bool
  [LLM::Character] ok 14 - lorebook_enclosed_minimal.json: entry 0 insertion_order is Int
  [LLM::Character] ok 15 - lorebook_enclosed_minimal.json: entry 0 use_regex is defined
  [LLM::Character] ok 16 - lorebook_enclosed_minimal.json: entry 0 case_sensitive sane
  [LLM::Character] ok 17 - lorebook_enclosed_minimal.json: entry 0 constant sane
  [LLM::Character] ok 18 - lorebook_enclosed_minimal.json: entry 0 selective sane
  [LLM::Character] ok 19 - lorebook_enclosed_minimal.json: entry 0 secondary_keys sane
  [LLM::Character] ok 20 - lorebook_enclosed_minimal.json: entry 0 priority sane
  [LLM::Character] ok 21 - lorebook_enclosed_minimal.json: entry 0 comment sane
  [LLM::Character] ok 22 - lorebook_enclosed_minimal.json: entry 0 position sane
  [LLM::Character] ok 23 - lorebook_enclosed_minimal.json: entry 0 extensions sane
  [LLM::Character] ok 24 - lorebook_enclosed_minimal.json: correct first key
  [LLM::Character] ok 25 - lorebook_enclosed_minimal.json: correct second key
  [LLM::Character] ok 26 - lorebook_enclosed_minimal.json: correct content
  [LLM::Character] ok 27 - lorebook_enclosed_minimal.json: correctly enabled
  [LLM::Character] ok 28 - lorebook_enclosed_minimal.json: correct insertion order
  [LLM::Character] ok 29 - lorebook_enclosed_minimal.json: regex disabled correctly
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/05-enclosed_all_fields_lorebook.rakutest
  [LLM::Character] 1..49
  [LLM::Character] ok 1 - lorebook_enclosed_valid.json: lorebook is defined
  [LLM::Character] ok 2 - lorebook_enclosed_valid.json: is Lorebook
  [LLM::Character] ok 3 - lorebook_enclosed_valid.json: has entries
  [LLM::Character] ok 4 - lorebook_enclosed_valid.json: extensions defined
  [LLM::Character] ok 5 - lorebook_enclosed_valid.json: name is str or undefined
  [LLM::Character] ok 6 - lorebook_enclosed_valid.json: description is str or undefined
  [LLM::Character] ok 7 - lorebook_enclosed_valid.json: scan_depth is int or undefined
  [LLM::Character] ok 8 - lorebook_enclosed_valid.json: token_budget is int or undefined
  [LLM::Character] ok 9 - lorebook_enclosed_valid.json: recursive_scanning is bool or undefined
  [LLM::Character] ok 10 - lorebook_enclosed_valid.json: entry 0 is Entry
  [LLM::Character] ok 11 - lorebook_enclosed_valid.json: entry 0 has keys
  [LLM::Character] ok 12 - lorebook_enclosed_valid.json: entry 0 has content
  [LLM::Character] ok 13 - lorebook_enclosed_valid.json: entry 0 enabled is Bool
  [LLM::Character] ok 14 - lorebook_enclosed_valid.json: entry 0 insertion_order is Int
  [LLM::Character] ok 15 - lorebook_enclosed_valid.json: entry 0 use_regex is defined
  [LLM::Character] ok 16 - lorebook_enclosed_valid.json: entry 0 case_sensitive sane
  [LLM::Character] ok 17 - lorebook_enclosed_valid.json: entry 0 constant sane
  [LLM::Character] ok 18 - lorebook_enclosed_valid.json: entry 0 selective sane
  [LLM::Character] ok 19 - lorebook_enclosed_valid.json: entry 0 secondary_keys sane
  [LLM::Character] ok 20 - lorebook_enclosed_valid.json: entry 0 priority sane
  [LLM::Character] ok 21 - lorebook_enclosed_valid.json: entry 0 comment sane
  [LLM::Character] ok 22 - lorebook_enclosed_valid.json: entry 0 position sane
  [LLM::Character] ok 23 - lorebook_enclosed_valid.json: entry 0 extensions sane
  [LLM::Character] ok 24 - lorebook_enclosed_valid.json: correct lorebook name
  [LLM::Character] ok 25 - lorebook_enclosed_valid.json: correct lorebook description
  [LLM::Character] ok 26 - lorebook_enclosed_valid.json: correct scan depth
  [LLM::Character] ok 27 - lorebook_enclosed_valid.json: correct token budget
  [LLM::Character] ok 28 - lorebook_enclosed_valid.json: correct recursive scanning
  [LLM::Character] ok 29 - lorebook_enclosed_valid.json: correct extension 'testString'
  [LLM::Character] ok 30 - lorebook_enclosed_valid.json: correct extension 'testBool'
  [LLM::Character] ok 31 - lorebook_enclosed_valid.json: correct extension 'testInt'
  [LLM::Character] ok 32 - lorebook_enclosed_valid.json: correct first key
  [LLM::Character] ok 33 - lorebook_enclosed_valid.json: correct second key
  [LLM::Character] ok 34 - lorebook_enclosed_valid.json: correct content
  [LLM::Character] ok 35 - lorebook_enclosed_valid.json: correct entry extension 'testString'
  [LLM::Character] ok 36 - lorebook_enclosed_valid.json: correct entry extension 'testBool'
  [LLM::Character] ok 37 - lorebook_enclosed_valid.json: correct entry extension 'testInt'
  [LLM::Character] ok 38 - lorebook_enclosed_valid.json: correctly enabled
  [LLM::Character] ok 39 - lorebook_enclosed_valid.json: correct insertion order
  [LLM::Character] ok 40 - lorebook_enclosed_valid.json: correct case sensitive
  [LLM::Character] ok 41 - lorebook_enclosed_valid.json: regex disabled correctly
  [LLM::Character] ok 42 - lorebook_enclosed_valid.json: constant correctly false
  [LLM::Character] ok 43 - lorebook_enclosed_valid.json: name correctly baz
  [LLM::Character] ok 44 - lorebook_enclosed_valid.json: correct entry priority
  [LLM::Character] ok 45 - lorebook_enclosed_valid.json: correct entry id
  [LLM::Character] ok 46 - lorebook.json: correct entry comment
  [LLM::Character] ok 47 - lorebook_enclosed_valid.json: entry correctly set to selective
  [LLM::Character] ok 48 - lorebook_enclosed_valid.json: correct entry secondary key
  [LLM::Character] ok 49 - lorebook_enclosed_valid.json: correct entry position
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/06-st_lorebook.rakutest
  [LLM::Character] 1..79
  [LLM::Character] ok 1 - st_lorebook.json: lorebook is defined
  [LLM::Character] ok 2 - st_lorebook.json: is Lorebook
  [LLM::Character] ok 3 - st_lorebook.json: has entries
  [LLM::Character] ok 4 - st_lorebook.json: extensions defined
  [LLM::Character] ok 5 - st_lorebook.json: name is str or undefined
  [LLM::Character] ok 6 - st_lorebook.json: description is str or undefined
  [LLM::Character] ok 7 - st_lorebook.json: scan_depth is int or undefined
  [LLM::Character] ok 8 - st_lorebook.json: token_budget is int or undefined
  [LLM::Character] ok 9 - st_lorebook.json: recursive_scanning is bool or undefined
  [LLM::Character] ok 10 - st_lorebook.json: entry 0 is Entry
  [LLM::Character] ok 11 - st_lorebook.json: entry 0 has keys or is constant
  [LLM::Character] ok 12 - st_lorebook.json: entry 0 has content
  [LLM::Character] ok 13 - st_lorebook.json: entry 0 enabled is Bool
  [LLM::Character] ok 14 - st_lorebook.json: entry 0 insertion_order is Int
  [LLM::Character] ok 15 - st_lorebook.json: entry 0 use_regex is defined
  [LLM::Character] ok 16 - st_lorebook.json: entry 0 case_sensitive sane
  [LLM::Character] ok 17 - st_lorebook.json: entry 0 constant sane
  [LLM::Character] ok 18 - st_lorebook.json: entry 0 selective sane
  [LLM::Character] ok 19 - st_lorebook.json: entry 0 secondary_keys sane
  [LLM::Character] ok 20 - st_lorebook.json: entry 0 priority sane
  [LLM::Character] ok 21 - st_lorebook.json: entry 0 comment sane
  [LLM::Character] ok 22 - st_lorebook.json: entry 0 position sane
  [LLM::Character] ok 23 - st_lorebook.json: entry 0 extensions sane
  [LLM::Character] ok 24 - st_lorebook.json: entry 1 is Entry
  [LLM::Character] ok 25 - st_lorebook.json: entry 1 has keys or is constant
  [LLM::Character] ok 26 - st_lorebook.json: entry 1 has content
  [LLM::Character] ok 27 - st_lorebook.json: entry 1 enabled is Bool
  [LLM::Character] ok 28 - st_lorebook.json: entry 1 insertion_order is Int
  [LLM::Character] ok 29 - st_lorebook.json: entry 1 use_regex is defined
  [LLM::Character] ok 30 - st_lorebook.json: entry 1 case_sensitive sane
  [LLM::Character] ok 31 - st_lorebook.json: entry 1 constant sane
  [LLM::Character] ok 32 - st_lorebook.json: entry 1 selective sane
  [LLM::Character] ok 33 - st_lorebook.json: entry 1 secondary_keys sane
  [LLM::Character] ok 34 - st_lorebook.json: entry 1 priority sane
  [LLM::Character] ok 35 - st_lorebook.json: entry 1 comment sane
  [LLM::Character] ok 36 - st_lorebook.json: entry 1 position sane
  [LLM::Character] ok 37 - st_lorebook.json: entry 1 extensions sane
  [LLM::Character] ok 38 - st_lorebook.json: entry 2 is Entry
  [LLM::Character] ok 39 - st_lorebook.json: entry 2 has keys or is constant
  [LLM::Character] ok 40 - st_lorebook.json: entry 2 has content
  [LLM::Character] ok 41 - st_lorebook.json: entry 2 enabled is Bool
  [LLM::Character] ok 42 - st_lorebook.json: entry 2 insertion_order is Int
  [LLM::Character] ok 43 - st_lorebook.json: entry 2 use_regex is defined
  [LLM::Character] ok 44 - st_lorebook.json: entry 2 case_sensitive sane
  [LLM::Character] ok 45 - st_lorebook.json: entry 2 constant sane
  [LLM::Character] ok 46 - st_lorebook.json: entry 2 selective sane
  [LLM::Character] ok 47 - st_lorebook.json: entry 2 secondary_keys sane
  [LLM::Character] ok 48 - st_lorebook.json: entry 2 priority sane
  [LLM::Character] ok 49 - st_lorebook.json: entry 2 comment sane
  [LLM::Character] ok 50 - st_lorebook.json: entry 2 position sane
  [LLM::Character] ok 51 - st_lorebook.json: entry 2 extensions sane
  [LLM::Character] ok 52 - st_lorebook.json: entry 3 is Entry
  [LLM::Character] ok 53 - st_lorebook.json: entry 3 has keys or is constant
  [LLM::Character] ok 54 - st_lorebook.json: entry 3 has content
  [LLM::Character] ok 55 - st_lorebook.json: entry 3 enabled is Bool
  [LLM::Character] ok 56 - st_lorebook.json: entry 3 insertion_order is Int
  [LLM::Character] ok 57 - st_lorebook.json: entry 3 use_regex is defined
  [LLM::Character] ok 58 - st_lorebook.json: entry 3 case_sensitive sane
  [LLM::Character] ok 59 - st_lorebook.json: entry 3 constant sane
  [LLM::Character] ok 60 - st_lorebook.json: entry 3 selective sane
  [LLM::Character] ok 61 - st_lorebook.json: entry 3 secondary_keys sane
  [LLM::Character] ok 62 - st_lorebook.json: entry 3 priority sane
  [LLM::Character] ok 63 - st_lorebook.json: entry 3 comment sane
  [LLM::Character] ok 64 - st_lorebook.json: entry 3 position sane
  [LLM::Character] ok 65 - st_lorebook.json: entry 3 extensions sane
  [LLM::Character] ok 66 - st_lorebook.json: entry 4 is Entry
  [LLM::Character] ok 67 - st_lorebook.json: entry 4 has keys or is constant
  [LLM::Character] ok 68 - st_lorebook.json: entry 4 has content
  [LLM::Character] ok 69 - st_lorebook.json: entry 4 enabled is Bool
  [LLM::Character] ok 70 - st_lorebook.json: entry 4 insertion_order is Int
  [LLM::Character] ok 71 - st_lorebook.json: entry 4 use_regex is defined
  [LLM::Character] ok 72 - st_lorebook.json: entry 4 case_sensitive sane
  [LLM::Character] ok 73 - st_lorebook.json: entry 4 constant sane
  [LLM::Character] ok 74 - st_lorebook.json: entry 4 selective sane
  [LLM::Character] ok 75 - st_lorebook.json: entry 4 secondary_keys sane
  [LLM::Character] ok 76 - st_lorebook.json: entry 4 priority sane
  [LLM::Character] ok 77 - st_lorebook.json: entry 4 comment sane
  [LLM::Character] ok 78 - st_lorebook.json: entry 4 position sane
  [LLM::Character] ok 79 - st_lorebook.json: entry 4 extensions sane
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/07-character_enclosed.rakutest
  [LLM::Character] 1..5
  [LLM::Character] ok 1 - Got a character card
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Correct description
  [LLM::Character] ok 4 - Extension talkativeness present
  [LLM::Character] ok 5 - Extension fav present
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/08-character_flat.rakutest
  [LLM::Character] 1..3
  [LLM::Character] ok 1 - Got a character card
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Correct description
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/09-character_with_book.rakutest
  [LLM::Character] 1..5
  [LLM::Character] ok 1 - Got a character card
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Lorebook is present
  [LLM::Character] ok 4 - One lorebook entry
  [LLM::Character] ok 5 - One asset present
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/10-main.rakutest
  [LLM::Character] 1..10
  [LLM::Character] ok 1 - correctly imports a lorebook
  [LLM::Character] ok 2 - correctly populates lorebook name
  [LLM::Character] ok 3 - correctly populates lorebook entry
  [LLM::Character] ok 4 - correctly imports a character
  [LLM::Character] ok 5 - correctly populates character name
  [LLM::Character] ok 6 - correctly populates character lorebook
  [LLM::Character] ok 7 - correctly populates lorebook keys
  [LLM::Character] ok 8 - correctly imports character from PNG
  [LLM::Character] ok 9 - correctly populates character name from PNG
  [LLM::Character] ok 10 - correctly populates first message from PNG
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/11-matcher-construction.rakutest
  [LLM::Character] 1..2
  [LLM::Character] # Subtest: Basic trie building
  [LLM::Character]     ok 1 - Root has 'f' child
  [LLM::Character]     ok 2 - 'f' node has 'o' child
  [LLM::Character]     ok 3 - 'f'→'o' has 'o' child
  [LLM::Character]     ok 4 - 'f'→'o' has 'a' child
  [LLM::Character]     ok 5 - 'foo' terminal node has one output
  [LLM::Character]     ok 6 - 'foo' entry output is correct
  [LLM::Character]     ok 7 - 'foal' entry output is correct
  [LLM::Character]     1..7
  [LLM::Character] ok 1 - Basic trie building
  [LLM::Character] # Subtest: Regex and constant handling
  [LLM::Character]     ok 1 - Constant entries list has 1
  [LLM::Character]     ok 2 - Constant entry uuid matches
  [LLM::Character]     ok 3 - Regex entries list has 2
  [LLM::Character]     ok 4 - Regex entry uuid matches
  [LLM::Character]     ok 5 - Regex was compiled
  [LLM::Character]     ok 6 - Regex matches
  [LLM::Character]     ok 7 - Regex with flags entry uuid matches
  [LLM::Character]     ok 8 - Regex with flags was compiled
  [LLM::Character]     ok 9 - Regex with flags is case-insensitive
  [LLM::Character]     1..9
  [LLM::Character] ok 2 - Regex and constant handling
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/12-matching.rakutest
  [LLM::Character] 1..12
  [LLM::Character] # Subtest: Single keyword match
  [LLM::Character]     ok 1 - Single match
  [LLM::Character]     ok 2 - UUID correct
  [LLM::Character]     1..2
  [LLM::Character] ok 1 - Single keyword match
  [LLM::Character] # Subtest: Multiple keywords, one pass
  [LLM::Character]     ok 1 - Both matches found
  [LLM::Character]     1..1
  [LLM::Character] ok 2 - Multiple keywords, one pass
  [LLM::Character] # Subtest: Case-insensitive key matches any case
  [LLM::Character]     ok 1 - Insensitive match (all upper)
  [LLM::Character]     ok 2 - Insensitive match (mixed)
  [LLM::Character]     ok 3 - No match on unrelated word
  [LLM::Character]     1..3
  [LLM::Character] ok 3 - Case-insensitive key matches any case
  [LLM::Character] # Subtest: Regex entry matches and respects flags
  [LLM::Character]     ok 1 - Regex matches start of line
  [LLM::Character]     ok 2 - Regex with /i matches
  [LLM::Character]     ok 3 - No regex match on non-bar/baz
  [LLM::Character]     1..3
  [LLM::Character] ok 4 - Regex entry matches and respects flags
  [LLM::Character] # Subtest: Constant entries always included
  [LLM::Character]     ok 1 - Only constant present when no match
  [LLM::Character]     ok 2 - Constant plus normal match
  [LLM::Character]     1..2
  [LLM::Character] ok 5 - Constant entries always included
  [LLM::Character] # Subtest: Selective entry: needs primary & secondary
  [LLM::Character]     ok 1 - Both keys present (fires)
  [LLM::Character]     ok 2 - Only primary, not selective
  [LLM::Character]     ok 3 - Only selective, not primary
  [LLM::Character]     1..3
  [LLM::Character] ok 6 - Selective entry: needs primary & secondary
  [LLM::Character] # Subtest: exclude_recursion: only pass 0
  [LLM::Character]     ok 1 - Matches on pass 0
  [LLM::Character]     ok 2 - Correct entry
  [LLM::Character]     1..2
  [LLM::Character] ok 7 - exclude_recursion: only pass 0
  [LLM::Character] # Subtest: delay_until_recursion: only pass > 0
  [LLM::Character]     ok 1 - delay_until_recursion only fires after pass 0
  [LLM::Character]     1..1
  [LLM::Character] ok 8 - delay_until_recursion: only pass > 0
  [LLM::Character] # Subtest: prevent_recursion: no content added for recursion
  [LLM::Character]     ok 1 - Second entry not matched due to prevent_recursion
  [LLM::Character]     1..1
  [LLM::Character] ok 9 - prevent_recursion: no content added for recursion
  [LLM::Character] # Subtest: Recursive matching up to scan_depth
  [LLM::Character]     ok 1 - All found through recursive scan
  [LLM::Character]     1..1
  [LLM::Character] ok 10 - Recursive matching up to scan_depth
  [LLM::Character] # Subtest: No duplicate matches
  [LLM::Character]     ok 1 - Entry matched only once
  [LLM::Character]     1..1
  [LLM::Character] ok 11 - No duplicate matches
  [LLM::Character] # Subtest: Edge cases
  [LLM::Character]     ok 1 - No match on empty haystack
  [LLM::Character]     ok 2 - No match on empty keys
  [LLM::Character]     ok 3 - No match if not enabled
  [LLM::Character]     ok 4 - Both 'foo' and 'food' matched
  [LLM::Character]     1..4
  [LLM::Character] ok 12 - Edge cases
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/13-export_character_json.rakutest
  [LLM::Character] 1..25
  [LLM::Character] ok 1 - Export produces output
  [LLM::Character] ok 2 - Correct spec
  [LLM::Character] ok 3 - Correct spec_version
  [LLM::Character] ok 4 - Has data key
  [LLM::Character] ok 5 - Correct name
  [LLM::Character] ok 6 - Correct description
  [LLM::Character] ok 7 - Correct first_mes
  [LLM::Character] ok 8 - Correct personality
  [LLM::Character] ok 9 - Correct scenario
  [LLM::Character] ok 10 - Correct mes_example
  [LLM::Character] ok 11 - Correct creator_notes
  [LLM::Character] ok 12 - Correct system_prompt
  [LLM::Character] ok 13 - Correct post_history_instructions
  [LLM::Character] ok 14 - Tags is empty array
  [LLM::Character] ok 15 - Alternate greetings is empty array
  [LLM::Character] ok 16 - Group only greetings is empty array
  [LLM::Character] ok 17 - character_book present
  [LLM::Character] ok 18 - One entry in character_book
  [LLM::Character] ok 19 - Entry keys correct
  [LLM::Character] ok 20 - Entry content correct
  [LLM::Character] ok 21 - One asset
  [LLM::Character] ok 22 - Asset type correct
  [LLM::Character] ok 23 - Asset uri correct
  [LLM::Character] ok 24 - Extension preserved
  [LLM::Character] ok 25 - Round-trip preserves name
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/14-export_lorebook_json.rakutest
  [LLM::Character] 1..27
  [LLM::Character] ok 1 - Export produces output
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Correct description
  [LLM::Character] ok 4 - Correct scan_depth
  [LLM::Character] ok 5 - Correct token_budget
  [LLM::Character] ok 6 - Correct recursive_scanning
  [LLM::Character] ok 7 - Extension testString preserved
  [LLM::Character] ok 8 - Extension testBool preserved
  [LLM::Character] ok 9 - Extension testInt preserved
  [LLM::Character] ok 10 - One entry
  [LLM::Character] ok 11 - Entry keys correct
  [LLM::Character] ok 12 - Entry content correct
  [LLM::Character] ok 13 - Entry enabled
  [LLM::Character] ok 14 - Entry insertion_order correct
  [LLM::Character] ok 15 - Entry case_sensitive correct
  [LLM::Character] ok 16 - Entry use_regex correct
  [LLM::Character] ok 17 - Entry constant correct
  [LLM::Character] ok 18 - Entry name correct
  [LLM::Character] ok 19 - Entry priority correct
  [LLM::Character] ok 20 - Entry id correct
  [LLM::Character] ok 21 - Entry comment correct
  [LLM::Character] ok 22 - Entry selective correct
  [LLM::Character] ok 23 - Entry secondary_keys correct
  [LLM::Character] ok 24 - Entry position correct
  [LLM::Character] ok 25 - Decorators prepended to content
  [LLM::Character] ok 26 - Round-trip preserves name
  [LLM::Character] ok 27 - Round-trip preserves entry content
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/15-export_lorebook_st.rakutest
  [LLM::Character] 1..22
  [LLM::Character] ok 1 - Export produces output
  [LLM::Character] ok 2 - Entries is a Hash
  [LLM::Character] ok 3 - All entry keys are strings
  [LLM::Character] ok 4 - Five entries
  [LLM::Character] ok 5 - Entry 0 exists
  [LLM::Character] ok 6 - uid field (renamed from id)
  [LLM::Character] ok 7 - key field is array (renamed from keys)
  [LLM::Character] ok 8 - keysecondary field is array (renamed from secondary_keys)
  [LLM::Character] ok 9 - order field (renamed from insertion_order)
  [LLM::Character] ok 10 - disable field (negated from enabled)
  [LLM::Character] ok 11 - position is int (before_char = 0)
  [LLM::Character] ok 12 - constant preserved
  [LLM::Character] ok 13 - comment preserved
  [LLM::Character] ok 14 - content preserved
  [LLM::Character] ok 15 - preventRecursion field present
  [LLM::Character] ok 16 - preventRecursion is true for entry 0
  [LLM::Character] ok 17 - preventRecursion is false for entry 3
  [LLM::Character] ok 18 - Entry 4 key array correct
  [LLM::Character] ok 19 - Entry 4 not constant
  [LLM::Character] ok 20 - Entry 4 content correct
  [LLM::Character] ok 21 - No keys field (should be key)
  [LLM::Character] ok 22 - No insertion_order field (should be order)
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/16-export_character_png.rakutest
  [LLM::Character] 1..9
  [LLM::Character] ok 1 - PNG export succeeds
  [LLM::Character] ok 2 - Output PNG file exists
  [LLM::Character] ok 3 - Output PNG file is not empty
  [LLM::Character] ok 4 - ccv3 tEXt chunk present
  [LLM::Character] ok 5 - chara tEXt chunk present
  [LLM::Character] ok 6 - Re-imported is a Card
  [LLM::Character] ok 7 - Round-trip preserves name
  [LLM::Character] ok 8 - Round-trip preserves description
  [LLM::Character] ok 9 - Round-trip preserves first_mes
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/17-export_main.rakutest
  [LLM::Character] 1..15
  [LLM::Character] ok 1 - export-character to JSON succeeds
  [LLM::Character] ok 2 - JSON file exists
  [LLM::Character] ok 3 - Exported JSON has CCv3 spec
  [LLM::Character] ok 4 - Exported JSON has correct name
  [LLM::Character] ok 5 - Round-trip JSON character name matches
  [LLM::Character] ok 6 - export-character-to-png succeeds
  [LLM::Character] ok 7 - PNG file exists
  [LLM::Character] ok 8 - Round-trip PNG character name matches
  [LLM::Character] ok 9 - export-lorebook ccv3 succeeds
  [LLM::Character] ok 10 - CCv3 lorebook file exists
  [LLM::Character] ok 11 - CCv3 lorebook name correct
  [LLM::Character] ok 12 - export-lorebook st succeeds
  [LLM::Character] ok 13 - ST lorebook file exists
  [LLM::Character] ok 14 - ST lorebook has Hash entries
  [LLM::Character] ok 15 - ST lorebook entry content correct
  ===> Testing [OK] for LLM::Character:ver<0.2.3>:auth<zef:apogee>
  ===> Installing: LLM::Character:ver<0.2.3>:auth<zef:apogee>
  ===> Install [OK] for LLM::Character:ver<0.2.3>:auth<zef:apogee>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 33.422s
               CPU time consumed: 1min 54.141s
                     Memory peak: 1.1G (swap: 62.2M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p357308-i358613.service; invocation ID: 669f6bc9f8434ecdb93c88f7af1b9160
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: LLM::Character
  ===> Found: LLM::Character:ver<0.2.3>:auth<zef:apogee> [via Zef::Repository::Ecosystems<fez>]
  [LLM::Character] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788474530.357313.1782.3010945348783/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz https://360.zef.pm/L/LM/LLM_CHARACTER/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  ===> Fetching [OK]: LLM::Character:ver<0.2.3>:auth<zef:apogee> to /home/coke/sandbox/blin/data/zef-data/tmp/1788474530.357313.1782.3010945348783/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  [LLM::Character] Command: tar -t -f ./f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  [LLM::Character] Command: tar -xvf ./f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz -C ../f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  ===> Extraction [OK]: LLM::Character to /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  ===> Testing: LLM::Character:ver<0.2.3>:auth<zef:apogee>
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/01-basic.rakutest
  [LLM::Character] ok 1 - replace me
  [LLM::Character] 1..1
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/02-minimal_lorebook.rakutest
  [LLM::Character] 1..29
  [LLM::Character] ok 1 - lorebook_minimal.json: lorebook is defined
  [LLM::Character] ok 2 - lorebook_minimal.json: is Lorebook
  [LLM::Character] ok 3 - lorebook_minimal.json: has entries
  [LLM::Character] ok 4 - lorebook_minimal.json: extensions defined
  [LLM::Character] ok 5 - lorebook_minimal.json: name is str or undefined
  [LLM::Character] ok 6 - lorebook_minimal.json: description is str or undefined
  [LLM::Character] ok 7 - lorebook_minimal.json: scan_depth is int or undefined
  [LLM::Character] ok 8 - lorebook_minimal.json: token_budget is int or undefined
  [LLM::Character] ok 9 - lorebook_minimal.json: recursive_scanning is bool or undefined
  [LLM::Character] ok 10 - lorebook_minimal.json: entry 0 is Entry
  [LLM::Character] ok 11 - lorebook_minimal.json: entry 0 has keys
  [LLM::Character] ok 12 - lorebook_minimal.json: entry 0 has content
  [LLM::Character] ok 13 - lorebook_minimal.json: entry 0 enabled is Bool
  [LLM::Character] ok 14 - lorebook_minimal.json: entry 0 insertion_order is Int
  [LLM::Character] ok 15 - lorebook_minimal.json: entry 0 use_regex is defined
  [LLM::Character] ok 16 - lorebook_minimal.json: entry 0 case_sensitive sane
  [LLM::Character] ok 17 - lorebook_minimal.json: entry 0 constant sane
  [LLM::Character] ok 18 - lorebook_minimal.json: entry 0 selective sane
  [LLM::Character] ok 19 - lorebook_minimal.json: entry 0 secondary_keys sane
  [LLM::Character] ok 20 - lorebook_minimal.json: entry 0 priority sane
  [LLM::Character] ok 21 - lorebook_minimal.json: entry 0 comment sane
  [LLM::Character] ok 22 - lorebook_minimal.json: entry 0 position sane
  [LLM::Character] ok 23 - lorebook_minimal.json: entry 0 extensions sane
  [LLM::Character] ok 24 - lorebook_minimal.json: correct first key
  [LLM::Character] ok 25 - lorebook_minimal.json: correct second key
  [LLM::Character] ok 26 - lorebook_minimal.json: correct content
  [LLM::Character] ok 27 - lorebook_minimal.json: correctly enabled
  [LLM::Character] ok 28 - lorebook_minimal.json: correct insertion order
  [LLM::Character] ok 29 - lorebook_minimal.json: regex disabled correctly
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/03-all_fields_lorebook.rakutest
  [LLM::Character] 1..49
  [LLM::Character] ok 1 - lorebook_valid.json: lorebook is defined
  [LLM::Character] ok 2 - lorebook_valid.json: is Lorebook
  [LLM::Character] ok 3 - lorebook_valid.json: has entries
  [LLM::Character] ok 4 - lorebook_valid.json: extensions defined
  [LLM::Character] ok 5 - lorebook_valid.json: name is str or undefined
  [LLM::Character] ok 6 - lorebook_valid.json: description is str or undefined
  [LLM::Character] ok 7 - lorebook_valid.json: scan_depth is int or undefined
  [LLM::Character] ok 8 - lorebook_valid.json: token_budget is int or undefined
  [LLM::Character] ok 9 - lorebook_valid.json: recursive_scanning is bool or undefined
  [LLM::Character] ok 10 - lorebook_valid.json: entry 0 is Entry
  [LLM::Character] ok 11 - lorebook_valid.json: entry 0 has keys
  [LLM::Character] ok 12 - lorebook_valid.json: entry 0 has content
  [LLM::Character] ok 13 - lorebook_valid.json: entry 0 enabled is Bool
  [LLM::Character] ok 14 - lorebook_valid.json: entry 0 insertion_order is Int
  [LLM::Character] ok 15 - lorebook_valid.json: entry 0 use_regex is defined
  [LLM::Character] ok 16 - lorebook_valid.json: entry 0 case_sensitive sane
  [LLM::Character] ok 17 - lorebook_valid.json: entry 0 constant sane
  [LLM::Character] ok 18 - lorebook_valid.json: entry 0 selective sane
  [LLM::Character] ok 19 - lorebook_valid.json: entry 0 secondary_keys sane
  [LLM::Character] ok 20 - lorebook_valid.json: entry 0 priority sane
  [LLM::Character] ok 21 - lorebook_valid.json: entry 0 comment sane
  [LLM::Character] ok 22 - lorebook_valid.json: entry 0 position sane
  [LLM::Character] ok 23 - lorebook_valid.json: entry 0 extensions sane
  [LLM::Character] ok 24 - lorebook_valid.json: correct lorebook name
  [LLM::Character] ok 25 - lorebook_valid.json: correct lorebook description
  [LLM::Character] ok 26 - lorebook_valid.json: correct scan depth
  [LLM::Character] ok 27 - lorebook_valid.json: correct token budget
  [LLM::Character] ok 28 - lorebook_valid.json: correct recursive scanning
  [LLM::Character] ok 29 - lorebook_valid.json: correct extension 'testString'
  [LLM::Character] ok 30 - lorebook_valid.json: correct extension 'testBool'
  [LLM::Character] ok 31 - lorebook_valid.json: correct extension 'testInt'
  [LLM::Character] ok 32 - lorebook_valid.json: correct first key
  [LLM::Character] ok 33 - lorebook_valid.json: correct second key
  [LLM::Character] ok 34 - lorebook_valid.json: correct content
  [LLM::Character] ok 35 - lorebook_valid.json: correct entry extension 'testString'
  [LLM::Character] ok 36 - lorebook_valid.json: correct entry extension 'testBool'
  [LLM::Character] ok 37 - lorebook_valid.json: correct entry extension 'testInt'
  [LLM::Character] ok 38 - lorebook_valid.json: correctly enabled
  [LLM::Character] ok 39 - lorebook_valid.json: correct insertion order
  [LLM::Character] ok 40 - lorebook_valid.json: correct case sensitive
  [LLM::Character] ok 41 - lorebook_valid.json: regex disabled correctly
  [LLM::Character] ok 42 - lorebook_valid.json: constant correctly false
  [LLM::Character] ok 43 - lorebook_valid.json: name correctly baz
  [LLM::Character] ok 44 - lorebook_valid.json: correct entry priority
  [LLM::Character] ok 45 - lorebook_valid.json: correct entry id
  [LLM::Character] ok 46 - lorebook.json: correct entry comment
  [LLM::Character] ok 47 - lorebook_valid.json: entry correctly set to selective
  [LLM::Character] ok 48 - lorebook_valid.json: correct entry secondary key
  [LLM::Character] ok 49 - lorebook_valid.json: correct entry position
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/04-enclosed_minimal_lorebook.rakutest
  [LLM::Character] 1..29
  [LLM::Character] ok 1 - lorebook_enclosed_minimal.json: lorebook is defined
  [LLM::Character] ok 2 - lorebook_enclosed_minimal.json: is Lorebook
  [LLM::Character] ok 3 - lorebook_enclosed_minimal.json: has entries
  [LLM::Character] ok 4 - lorebook_enclosed_minimal.json: extensions defined
  [LLM::Character] ok 5 - lorebook_enclosed_minimal.json: name is str or undefined
  [LLM::Character] ok 6 - lorebook_enclosed_minimal.json: description is str or undefined
  [LLM::Character] ok 7 - lorebook_enclosed_minimal.json: scan_depth is int or undefined
  [LLM::Character] ok 8 - lorebook_enclosed_minimal.json: token_budget is int or undefined
  [LLM::Character] ok 9 - lorebook_enclosed_minimal.json: recursive_scanning is bool or undefined
  [LLM::Character] ok 10 - lorebook_enclosed_minimal.json: entry 0 is Entry
  [LLM::Character] ok 11 - lorebook_enclosed_minimal.json: entry 0 has keys
  [LLM::Character] ok 12 - lorebook_enclosed_minimal.json: entry 0 has content
  [LLM::Character] ok 13 - lorebook_enclosed_minimal.json: entry 0 enabled is Bool
  [LLM::Character] ok 14 - lorebook_enclosed_minimal.json: entry 0 insertion_order is Int
  [LLM::Character] ok 15 - lorebook_enclosed_minimal.json: entry 0 use_regex is defined
  [LLM::Character] ok 16 - lorebook_enclosed_minimal.json: entry 0 case_sensitive sane
  [LLM::Character] ok 17 - lorebook_enclosed_minimal.json: entry 0 constant sane
  [LLM::Character] ok 18 - lorebook_enclosed_minimal.json: entry 0 selective sane
  [LLM::Character] ok 19 - lorebook_enclosed_minimal.json: entry 0 secondary_keys sane
  [LLM::Character] ok 20 - lorebook_enclosed_minimal.json: entry 0 priority sane
  [LLM::Character] ok 21 - lorebook_enclosed_minimal.json: entry 0 comment sane
  [LLM::Character] ok 22 - lorebook_enclosed_minimal.json: entry 0 position sane
  [LLM::Character] ok 23 - lorebook_enclosed_minimal.json: entry 0 extensions sane
  [LLM::Character] ok 24 - lorebook_enclosed_minimal.json: correct first key
  [LLM::Character] ok 25 - lorebook_enclosed_minimal.json: correct second key
  [LLM::Character] ok 26 - lorebook_enclosed_minimal.json: correct content
  [LLM::Character] ok 27 - lorebook_enclosed_minimal.json: correctly enabled
  [LLM::Character] ok 28 - lorebook_enclosed_minimal.json: correct insertion order
  [LLM::Character] ok 29 - lorebook_enclosed_minimal.json: regex disabled correctly
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/05-enclosed_all_fields_lorebook.rakutest
  [LLM::Character] 1..49
  [LLM::Character] ok 1 - lorebook_enclosed_valid.json: lorebook is defined
  [LLM::Character] ok 2 - lorebook_enclosed_valid.json: is Lorebook
  [LLM::Character] ok 3 - lorebook_enclosed_valid.json: has entries
  [LLM::Character] ok 4 - lorebook_enclosed_valid.json: extensions defined
  [LLM::Character] ok 5 - lorebook_enclosed_valid.json: name is str or undefined
  [LLM::Character] ok 6 - lorebook_enclosed_valid.json: description is str or undefined
  [LLM::Character] ok 7 - lorebook_enclosed_valid.json: scan_depth is int or undefined
  [LLM::Character] ok 8 - lorebook_enclosed_valid.json: token_budget is int or undefined
  [LLM::Character] ok 9 - lorebook_enclosed_valid.json: recursive_scanning is bool or undefined
  [LLM::Character] ok 10 - lorebook_enclosed_valid.json: entry 0 is Entry
  [LLM::Character] ok 11 - lorebook_enclosed_valid.json: entry 0 has keys
  [LLM::Character] ok 12 - lorebook_enclosed_valid.json: entry 0 has content
  [LLM::Character] ok 13 - lorebook_enclosed_valid.json: entry 0 enabled is Bool
  [LLM::Character] ok 14 - lorebook_enclosed_valid.json: entry 0 insertion_order is Int
  [LLM::Character] ok 15 - lorebook_enclosed_valid.json: entry 0 use_regex is defined
  [LLM::Character] ok 16 - lorebook_enclosed_valid.json: entry 0 case_sensitive sane
  [LLM::Character] ok 17 - lorebook_enclosed_valid.json: entry 0 constant sane
  [LLM::Character] ok 18 - lorebook_enclosed_valid.json: entry 0 selective sane
  [LLM::Character] ok 19 - lorebook_enclosed_valid.json: entry 0 secondary_keys sane
  [LLM::Character] ok 20 - lorebook_enclosed_valid.json: entry 0 priority sane
  [LLM::Character] ok 21 - lorebook_enclosed_valid.json: entry 0 comment sane
  [LLM::Character] ok 22 - lorebook_enclosed_valid.json: entry 0 position sane
  [LLM::Character] ok 23 - lorebook_enclosed_valid.json: entry 0 extensions sane
  [LLM::Character] ok 24 - lorebook_enclosed_valid.json: correct lorebook name
  [LLM::Character] ok 25 - lorebook_enclosed_valid.json: correct lorebook description
  [LLM::Character] ok 26 - lorebook_enclosed_valid.json: correct scan depth
  [LLM::Character] ok 27 - lorebook_enclosed_valid.json: correct token budget
  [LLM::Character] ok 28 - lorebook_enclosed_valid.json: correct recursive scanning
  [LLM::Character] ok 29 - lorebook_enclosed_valid.json: correct extension 'testString'
  [LLM::Character] ok 30 - lorebook_enclosed_valid.json: correct extension 'testBool'
  [LLM::Character] ok 31 - lorebook_enclosed_valid.json: correct extension 'testInt'
  [LLM::Character] ok 32 - lorebook_enclosed_valid.json: correct first key
  [LLM::Character] ok 33 - lorebook_enclosed_valid.json: correct second key
  [LLM::Character] ok 34 - lorebook_enclosed_valid.json: correct content
  [LLM::Character] ok 35 - lorebook_enclosed_valid.json: correct entry extension 'testString'
  [LLM::Character] ok 36 - lorebook_enclosed_valid.json: correct entry extension 'testBool'
  [LLM::Character] ok 37 - lorebook_enclosed_valid.json: correct entry extension 'testInt'
  [LLM::Character] ok 38 - lorebook_enclosed_valid.json: correctly enabled
  [LLM::Character] ok 39 - lorebook_enclosed_valid.json: correct insertion order
  [LLM::Character] ok 40 - lorebook_enclosed_valid.json: correct case sensitive
  [LLM::Character] ok 41 - lorebook_enclosed_valid.json: regex disabled correctly
  [LLM::Character] ok 42 - lorebook_enclosed_valid.json: constant correctly false
  [LLM::Character] ok 43 - lorebook_enclosed_valid.json: name correctly baz
  [LLM::Character] ok 44 - lorebook_enclosed_valid.json: correct entry priority
  [LLM::Character] ok 45 - lorebook_enclosed_valid.json: correct entry id
  [LLM::Character] ok 46 - lorebook.json: correct entry comment
  [LLM::Character] ok 47 - lorebook_enclosed_valid.json: entry correctly set to selective
  [LLM::Character] ok 48 - lorebook_enclosed_valid.json: correct entry secondary key
  [LLM::Character] ok 49 - lorebook_enclosed_valid.json: correct entry position
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/06-st_lorebook.rakutest
  [LLM::Character] 1..79
  [LLM::Character] ok 1 - st_lorebook.json: lorebook is defined
  [LLM::Character] ok 2 - st_lorebook.json: is Lorebook
  [LLM::Character] ok 3 - st_lorebook.json: has entries
  [LLM::Character] ok 4 - st_lorebook.json: extensions defined
  [LLM::Character] ok 5 - st_lorebook.json: name is str or undefined
  [LLM::Character] ok 6 - st_lorebook.json: description is str or undefined
  [LLM::Character] ok 7 - st_lorebook.json: scan_depth is int or undefined
  [LLM::Character] ok 8 - st_lorebook.json: token_budget is int or undefined
  [LLM::Character] ok 9 - st_lorebook.json: recursive_scanning is bool or undefined
  [LLM::Character] ok 10 - st_lorebook.json: entry 0 is Entry
  [LLM::Character] ok 11 - st_lorebook.json: entry 0 has keys or is constant
  [LLM::Character] ok 12 - st_lorebook.json: entry 0 has content
  [LLM::Character] ok 13 - st_lorebook.json: entry 0 enabled is Bool
  [LLM::Character] ok 14 - st_lorebook.json: entry 0 insertion_order is Int
  [LLM::Character] ok 15 - st_lorebook.json: entry 0 use_regex is defined
  [LLM::Character] ok 16 - st_lorebook.json: entry 0 case_sensitive sane
  [LLM::Character] ok 17 - st_lorebook.json: entry 0 constant sane
  [LLM::Character] ok 18 - st_lorebook.json: entry 0 selective sane
  [LLM::Character] ok 19 - st_lorebook.json: entry 0 secondary_keys sane
  [LLM::Character] ok 20 - st_lorebook.json: entry 0 priority sane
  [LLM::Character] ok 21 - st_lorebook.json: entry 0 comment sane
  [LLM::Character] ok 22 - st_lorebook.json: entry 0 position sane
  [LLM::Character] ok 23 - st_lorebook.json: entry 0 extensions sane
  [LLM::Character] ok 24 - st_lorebook.json: entry 1 is Entry
  [LLM::Character] ok 25 - st_lorebook.json: entry 1 has keys or is constant
  [LLM::Character] ok 26 - st_lorebook.json: entry 1 has content
  [LLM::Character] ok 27 - st_lorebook.json: entry 1 enabled is Bool
  [LLM::Character] ok 28 - st_lorebook.json: entry 1 insertion_order is Int
  [LLM::Character] ok 29 - st_lorebook.json: entry 1 use_regex is defined
  [LLM::Character] ok 30 - st_lorebook.json: entry 1 case_sensitive sane
  [LLM::Character] ok 31 - st_lorebook.json: entry 1 constant sane
  [LLM::Character] ok 32 - st_lorebook.json: entry 1 selective sane
  [LLM::Character] ok 33 - st_lorebook.json: entry 1 secondary_keys sane
  [LLM::Character] ok 34 - st_lorebook.json: entry 1 priority sane
  [LLM::Character] ok 35 - st_lorebook.json: entry 1 comment sane
  [LLM::Character] ok 36 - st_lorebook.json: entry 1 position sane
  [LLM::Character] ok 37 - st_lorebook.json: entry 1 extensions sane
  [LLM::Character] ok 38 - st_lorebook.json: entry 2 is Entry
  [LLM::Character] ok 39 - st_lorebook.json: entry 2 has keys or is constant
  [LLM::Character] ok 40 - st_lorebook.json: entry 2 has content
  [LLM::Character] ok 41 - st_lorebook.json: entry 2 enabled is Bool
  [LLM::Character] ok 42 - st_lorebook.json: entry 2 insertion_order is Int
  [LLM::Character] ok 43 - st_lorebook.json: entry 2 use_regex is defined
  [LLM::Character] ok 44 - st_lorebook.json: entry 2 case_sensitive sane
  [LLM::Character] ok 45 - st_lorebook.json: entry 2 constant sane
  [LLM::Character] ok 46 - st_lorebook.json: entry 2 selective sane
  [LLM::Character] ok 47 - st_lorebook.json: entry 2 secondary_keys sane
  [LLM::Character] ok 48 - st_lorebook.json: entry 2 priority sane
  [LLM::Character] ok 49 - st_lorebook.json: entry 2 comment sane
  [LLM::Character] ok 50 - st_lorebook.json: entry 2 position sane
  [LLM::Character] ok 51 - st_lorebook.json: entry 2 extensions sane
  [LLM::Character] ok 52 - st_lorebook.json: entry 3 is Entry
  [LLM::Character] ok 53 - st_lorebook.json: entry 3 has keys or is constant
  [LLM::Character] ok 54 - st_lorebook.json: entry 3 has content
  [LLM::Character] ok 55 - st_lorebook.json: entry 3 enabled is Bool
  [LLM::Character] ok 56 - st_lorebook.json: entry 3 insertion_order is Int
  [LLM::Character] ok 57 - st_lorebook.json: entry 3 use_regex is defined
  [LLM::Character] ok 58 - st_lorebook.json: entry 3 case_sensitive sane
  [LLM::Character] ok 59 - st_lorebook.json: entry 3 constant sane
  [LLM::Character] ok 60 - st_lorebook.json: entry 3 selective sane
  [LLM::Character] ok 61 - st_lorebook.json: entry 3 secondary_keys sane
  [LLM::Character] ok 62 - st_lorebook.json: entry 3 priority sane
  [LLM::Character] ok 63 - st_lorebook.json: entry 3 comment sane
  [LLM::Character] ok 64 - st_lorebook.json: entry 3 position sane
  [LLM::Character] ok 65 - st_lorebook.json: entry 3 extensions sane
  [LLM::Character] ok 66 - st_lorebook.json: entry 4 is Entry
  [LLM::Character] ok 67 - st_lorebook.json: entry 4 has keys or is constant
  [LLM::Character] ok 68 - st_lorebook.json: entry 4 has content
  [LLM::Character] ok 69 - st_lorebook.json: entry 4 enabled is Bool
  [LLM::Character] ok 70 - st_lorebook.json: entry 4 insertion_order is Int
  [LLM::Character] ok 71 - st_lorebook.json: entry 4 use_regex is defined
  [LLM::Character] ok 72 - st_lorebook.json: entry 4 case_sensitive sane
  [LLM::Character] ok 73 - st_lorebook.json: entry 4 constant sane
  [LLM::Character] ok 74 - st_lorebook.json: entry 4 selective sane
  [LLM::Character] ok 75 - st_lorebook.json: entry 4 secondary_keys sane
  [LLM::Character] ok 76 - st_lorebook.json: entry 4 priority sane
  [LLM::Character] ok 77 - st_lorebook.json: entry 4 comment sane
  [LLM::Character] ok 78 - st_lorebook.json: entry 4 position sane
  [LLM::Character] ok 79 - st_lorebook.json: entry 4 extensions sane
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/07-character_enclosed.rakutest
  [LLM::Character] 1..5
  [LLM::Character] ok 1 - Got a character card
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Correct description
  [LLM::Character] ok 4 - Extension talkativeness present
  [LLM::Character] ok 5 - Extension fav present
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/08-character_flat.rakutest
  [LLM::Character] 1..3
  [LLM::Character] ok 1 - Got a character card
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Correct description
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/09-character_with_book.rakutest
  [LLM::Character] 1..5
  [LLM::Character] ok 1 - Got a character card
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Lorebook is present
  [LLM::Character] ok 4 - One lorebook entry
  [LLM::Character] ok 5 - One asset present
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/10-main.rakutest
  [LLM::Character] 1..10
  [LLM::Character] ok 1 - correctly imports a lorebook
  [LLM::Character] ok 2 - correctly populates lorebook name
  [LLM::Character] ok 3 - correctly populates lorebook entry
  [LLM::Character] ok 4 - correctly imports a character
  [LLM::Character] ok 5 - correctly populates character name
  [LLM::Character] ok 6 - correctly populates character lorebook
  [LLM::Character] ok 7 - correctly populates lorebook keys
  [LLM::Character] ok 8 - correctly imports character from PNG
  [LLM::Character] ok 9 - correctly populates character name from PNG
  [LLM::Character] ok 10 - correctly populates first message from PNG
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/11-matcher-construction.rakutest
  [LLM::Character] 1..2
  [LLM::Character] # Subtest: Basic trie building
  [LLM::Character]     ok 1 - Root has 'f' child
  [LLM::Character]     ok 2 - 'f' node has 'o' child
  [LLM::Character]     ok 3 - 'f'→'o' has 'o' child
  [LLM::Character]     ok 4 - 'f'→'o' has 'a' child
  [LLM::Character]     ok 5 - 'foo' terminal node has one output
  [LLM::Character]     ok 6 - 'foo' entry output is correct
  [LLM::Character]     ok 7 - 'foal' entry output is correct
  [LLM::Character]     1..7
  [LLM::Character] ok 1 - Basic trie building
  [LLM::Character] # Subtest: Regex and constant handling
  [LLM::Character]     ok 1 - Constant entries list has 1
  [LLM::Character]     ok 2 - Constant entry uuid matches
  [LLM::Character]     ok 3 - Regex entries list has 2
  [LLM::Character]     ok 4 - Regex entry uuid matches
  [LLM::Character]     ok 5 - Regex was compiled
  [LLM::Character]     ok 6 - Regex matches
  [LLM::Character]     ok 7 - Regex with flags entry uuid matches
  [LLM::Character]     ok 8 - Regex with flags was compiled
  [LLM::Character]     ok 9 - Regex with flags is case-insensitive
  [LLM::Character]     1..9
  [LLM::Character] ok 2 - Regex and constant handling
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/12-matching.rakutest
  [LLM::Character] 1..12
  [LLM::Character] # Subtest: Single keyword match
  [LLM::Character]     ok 1 - Single match
  [LLM::Character]     ok 2 - UUID correct
  [LLM::Character]     1..2
  [LLM::Character] ok 1 - Single keyword match
  [LLM::Character] # Subtest: Multiple keywords, one pass
  [LLM::Character]     ok 1 - Both matches found
  [LLM::Character]     1..1
  [LLM::Character] ok 2 - Multiple keywords, one pass
  [LLM::Character] # Subtest: Case-insensitive key matches any case
  [LLM::Character]     ok 1 - Insensitive match (all upper)
  [LLM::Character]     ok 2 - Insensitive match (mixed)
  [LLM::Character]     ok 3 - No match on unrelated word
  [LLM::Character]     1..3
  [LLM::Character] ok 3 - Case-insensitive key matches any case
  [LLM::Character] # Subtest: Regex entry matches and respects flags
  [LLM::Character]     ok 1 - Regex matches start of line
  [LLM::Character]     ok 2 - Regex with /i matches
  [LLM::Character]     ok 3 - No regex match on non-bar/baz
  [LLM::Character]     1..3
  [LLM::Character] ok 4 - Regex entry matches and respects flags
  [LLM::Character] # Subtest: Constant entries always included
  [LLM::Character]     ok 1 - Only constant present when no match
  [LLM::Character]     ok 2 - Constant plus normal match
  [LLM::Character]     1..2
  [LLM::Character] ok 5 - Constant entries always included
  [LLM::Character] # Subtest: Selective entry: needs primary & secondary
  [LLM::Character]     ok 1 - Both keys present (fires)
  [LLM::Character]     ok 2 - Only primary, not selective
  [LLM::Character]     ok 3 - Only selective, not primary
  [LLM::Character]     1..3
  [LLM::Character] ok 6 - Selective entry: needs primary & secondary
  [LLM::Character] # Subtest: exclude_recursion: only pass 0
  [LLM::Character]     ok 1 - Matches on pass 0
  [LLM::Character]     ok 2 - Correct entry
  [LLM::Character]     1..2
  [LLM::Character] ok 7 - exclude_recursion: only pass 0
  [LLM::Character] # Subtest: delay_until_recursion: only pass > 0
  [LLM::Character]     ok 1 - delay_until_recursion only fires after pass 0
  [LLM::Character]     1..1
  [LLM::Character] ok 8 - delay_until_recursion: only pass > 0
  [LLM::Character] # Subtest: prevent_recursion: no content added for recursion
  [LLM::Character]     ok 1 - Second entry not matched due to prevent_recursion
  [LLM::Character]     1..1
  [LLM::Character] ok 9 - prevent_recursion: no content added for recursion
  [LLM::Character] # Subtest: Recursive matching up to scan_depth
  [LLM::Character]     ok 1 - All found through recursive scan
  [LLM::Character]     1..1
  [LLM::Character] ok 10 - Recursive matching up to scan_depth
  [LLM::Character] # Subtest: No duplicate matches
  [LLM::Character]     ok 1 - Entry matched only once
  [LLM::Character]     1..1
  [LLM::Character] ok 11 - No duplicate matches
  [LLM::Character] # Subtest: Edge cases
  [LLM::Character]     ok 1 - No match on empty haystack
  [LLM::Character]     ok 2 - No match on empty keys
  [LLM::Character]     ok 3 - No match if not enabled
  [LLM::Character]     ok 4 - Both 'foo' and 'food' matched
  [LLM::Character]     1..4
  [LLM::Character] ok 12 - Edge cases
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/13-export_character_json.rakutest
  [LLM::Character] 1..25
  [LLM::Character] ok 1 - Export produces output
  [LLM::Character] ok 2 - Correct spec
  [LLM::Character] ok 3 - Correct spec_version
  [LLM::Character] ok 4 - Has data key
  [LLM::Character] ok 5 - Correct name
  [LLM::Character] ok 6 - Correct description
  [LLM::Character] ok 7 - Correct first_mes
  [LLM::Character] ok 8 - Correct personality
  [LLM::Character] ok 9 - Correct scenario
  [LLM::Character] ok 10 - Correct mes_example
  [LLM::Character] ok 11 - Correct creator_notes
  [LLM::Character] ok 12 - Correct system_prompt
  [LLM::Character] ok 13 - Correct post_history_instructions
  [LLM::Character] ok 14 - Tags is empty array
  [LLM::Character] ok 15 - Alternate greetings is empty array
  [LLM::Character] ok 16 - Group only greetings is empty array
  [LLM::Character] ok 17 - character_book present
  [LLM::Character] ok 18 - One entry in character_book
  [LLM::Character] ok 19 - Entry keys correct
  [LLM::Character] ok 20 - Entry content correct
  [LLM::Character] ok 21 - One asset
  [LLM::Character] ok 22 - Asset type correct
  [LLM::Character] ok 23 - Asset uri correct
  [LLM::Character] ok 24 - Extension preserved
  [LLM::Character] ok 25 - Round-trip preserves name
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/14-export_lorebook_json.rakutest
  [LLM::Character] 1..27
  [LLM::Character] ok 1 - Export produces output
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Correct description
  [LLM::Character] ok 4 - Correct scan_depth
  [LLM::Character] ok 5 - Correct token_budget
  [LLM::Character] ok 6 - Correct recursive_scanning
  [LLM::Character] ok 7 - Extension testString preserved
  [LLM::Character] ok 8 - Extension testBool preserved
  [LLM::Character] ok 9 - Extension testInt preserved
  [LLM::Character] ok 10 - One entry
  [LLM::Character] ok 11 - Entry keys correct
  [LLM::Character] ok 12 - Entry content correct
  [LLM::Character] ok 13 - Entry enabled
  [LLM::Character] ok 14 - Entry insertion_order correct
  [LLM::Character] ok 15 - Entry case_sensitive correct
  [LLM::Character] ok 16 - Entry use_regex correct
  [LLM::Character] ok 17 - Entry constant correct
  [LLM::Character] ok 18 - Entry name correct
  [LLM::Character] ok 19 - Entry priority correct
  [LLM::Character] ok 20 - Entry id correct
  [LLM::Character] ok 21 - Entry comment correct
  [LLM::Character] ok 22 - Entry selective correct
  [LLM::Character] ok 23 - Entry secondary_keys correct
  [LLM::Character] ok 24 - Entry position correct
  [LLM::Character] ok 25 - Decorators prepended to content
  [LLM::Character] ok 26 - Round-trip preserves name
  [LLM::Character] ok 27 - Round-trip preserves entry content
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/15-export_lorebook_st.rakutest
  [LLM::Character] 1..22
  [LLM::Character] ok 1 - Export produces output
  [LLM::Character] ok 2 - Entries is a Hash
  [LLM::Character] ok 3 - All entry keys are strings
  [LLM::Character] ok 4 - Five entries
  [LLM::Character] ok 5 - Entry 0 exists
  [LLM::Character] ok 6 - uid field (renamed from id)
  [LLM::Character] ok 7 - key field is array (renamed from keys)
  [LLM::Character] ok 8 - keysecondary field is array (renamed from secondary_keys)
  [LLM::Character] ok 9 - order field (renamed from insertion_order)
  [LLM::Character] ok 10 - disable field (negated from enabled)
  [LLM::Character] ok 11 - position is int (before_char = 0)
  [LLM::Character] ok 12 - constant preserved
  [LLM::Character] ok 13 - comment preserved
  [LLM::Character] ok 14 - content preserved
  [LLM::Character] ok 15 - preventRecursion field present
  [LLM::Character] ok 16 - preventRecursion is true for entry 0
  [LLM::Character] ok 17 - preventRecursion is false for entry 3
  [LLM::Character] ok 18 - Entry 4 key array correct
  [LLM::Character] ok 19 - Entry 4 not constant
  [LLM::Character] ok 20 - Entry 4 content correct
  [LLM::Character] ok 21 - No keys field (should be key)
  [LLM::Character] ok 22 - No insertion_order field (should be order)
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/16-export_character_png.rakutest
  [LLM::Character] 1..9
  [LLM::Character] ok 1 - PNG export succeeds
  [LLM::Character] ok 2 - Output PNG file exists
  [LLM::Character] ok 3 - Output PNG file is not empty
  [LLM::Character] ok 4 - ccv3 tEXt chunk present
  [LLM::Character] not ok 5 - chara tEXt chunk present
  [LLM::Character] # Failed test 'chara tEXt chunk present'
  [LLM::Character] # at t/16-export_character_png.rakutest line 34
  [LLM::Character] ok 6 - Re-imported is a Card
  [LLM::Character] ok 7 - Round-trip preserves name
  [LLM::Character] ok 8 - Round-trip preserves description
  [LLM::Character] ok 9 - Round-trip preserves first_mes
  [LLM::Character] # You failed 1 test of 9
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/17-export_main.rakutest
  [LLM::Character] 1..15
  [LLM::Character] ok 1 - export-character to JSON succeeds
  [LLM::Character] ok 2 - JSON file exists
  [LLM::Character] ok 3 - Exported JSON has CCv3 spec
  [LLM::Character] ok 4 - Exported JSON has correct name
  [LLM::Character] ok 5 - Round-trip JSON character name matches
  [LLM::Character] ok 6 - export-character-to-png succeeds
  [LLM::Character] ok 7 - PNG file exists
  [LLM::Character] ok 8 - Round-trip PNG character name matches
  [LLM::Character] ok 9 - export-lorebook ccv3 succeeds
  [LLM::Character] ok 10 - CCv3 lorebook file exists
  [LLM::Character] ok 11 - CCv3 lorebook name correct
  [LLM::Character] ok 12 - export-lorebook st succeeds
  [LLM::Character] ok 13 - ST lorebook file exists
  [LLM::Character] ok 14 - ST lorebook has Hash entries
  [LLM::Character] ok 15 - ST lorebook entry content correct
  ===> Testing [FAIL]: LLM::Character:ver<0.2.3>:auth<zef:apogee>
  [LLM::Character] Failed to get passing tests, but continuing with --force-test
  ===> Installing: LLM::Character:ver<0.2.3>:auth<zef:apogee>
  ===> Install [OK] for LLM::Character:ver<0.2.3>:auth<zef:apogee>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 41.089s
               CPU time consumed: 2min 43.949s
                     Memory peak: 1.8G (swap: 140.6M)

  ```
  </details>
* [ ] [PDF::Combiner](https://raku.land/zef:tbrowder/PDF::Combiner) – Fail, Bisected: [fdc7d63](https://github.com/rakudo/rakudo/commit/fdc7d635717d90c06826668936cd708d30fd19c4)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p549248-i465930.service; invocation ID: 1a6511e8cd3146dba6859bcf47077e10
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: PDF::Combiner
  ===> Found: PDF::Combiner:ver<0.0.1>:auth<zef:tbrowder> [via Zef::Repository::Ecosystems<fez>]
  [PDF::Combiner] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788479478.549253.6276.483011155517/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz https://360.zef.pm/P/DF/PDF_COMBINER/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz
  ===> Fetching [OK]: PDF::Combiner:ver<0.0.1>:auth<zef:tbrowder> to /home/coke/sandbox/blin/data/zef-data/tmp/1788479478.549253.6276.483011155517/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz
  [PDF::Combiner] Command: tar -t -f ./634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz
  [PDF::Combiner] Command: tar -xvf ./634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz -C ../634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz
  ===> Extraction [OK]: PDF::Combiner to /home/coke/sandbox/blin/data/zef-data/tmp/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz
  ===> Testing: PDF::Combiner:ver<0.0.1>:auth<zef:tbrowder>
  [PDF::Combiner] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz/PDF-Combiner-0.0.1 t/0-basic.t
  [PDF::Combiner] ok 1 - replace me
  [PDF::Combiner] 1..1
  [PDF::Combiner] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz/PDF-Combiner-0.0.1 t/1-config-class.t
  [PDF::Combiner] ok 1 - The object is-a 'PDF::Subs::Config'
  [PDF::Combiner] ok 2 - test Config class and the config reading
  [PDF::Combiner] ok 3 - title first line
  [PDF::Combiner] ok 4 - title second line
  [PDF::Combiner] ok 5 - title last line
  [PDF::Combiner] ok 6 - 
  [PDF::Combiner] ok 7 - 
  [PDF::Combiner] ok 8 - text matches /'trip-to-israel.pdf'/
  [PDF::Combiner] ok 9 - expect numbers True
  [PDF::Combiner] 1..9
  ===> Testing [OK] for PDF::Combiner:ver<0.0.1>:auth<zef:tbrowder>
  ===> Installing: PDF::Combiner:ver<0.0.1>:auth<zef:tbrowder>
  ===> Install [OK] for PDF::Combiner:ver<0.0.1>:auth<zef:tbrowder>

  1 bin/ script [combine-pdfs] installed to:
  /tmp/8USO3uLYB5/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 5min 14.059s
               CPU time consumed: 5min 55.460s
                     Memory peak: 2.9G (swap: 124.1M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p532512-i546938.service; invocation ID: 4ef7254d09ec47919fd9f007f51174a4
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: PDF::Combiner
  ===> Found: PDF::Combiner:ver<0.0.1>:auth<zef:tbrowder> [via Zef::Repository::Ecosystems<fez>]
  [PDF::Combiner] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788478983.532530.7288.644913368823/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz https://360.zef.pm/P/DF/PDF_COMBINER/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz
  ===> Fetching [OK]: PDF::Combiner:ver<0.0.1>:auth<zef:tbrowder> to /home/coke/sandbox/blin/data/zef-data/tmp/1788478983.532530.7288.644913368823/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz
  [PDF::Combiner] Command: tar -t -f ./634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz
  [PDF::Combiner] Command: tar -xvf ./634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz -C ../634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz
  ===> Extraction [OK]: PDF::Combiner to /home/coke/sandbox/blin/data/zef-data/tmp/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz
  ===> Testing: PDF::Combiner:ver<0.0.1>:auth<zef:tbrowder>
  [PDF::Combiner] Command: /tmp/whateverable/rakudo-moar/fdc7d635717d90c06826668936cd708d30fd19c4/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/634e627329dd8420f20c73ef9e47a508cf2f5e62.tar.gz/PDF-Combiner-0.0.1 t/0-basic.t
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 7min 55.263s
               CPU time consumed: 6min 16.599s
                     Memory peak: 2G (swap: 1G)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| UnhandledException        |     1 | [Foo:: Foo](https://raku.land/github:AlexDaniel/Foo:: Foo) |
| Flapper                   |     3 | [DAWG](https://raku.land/zef:slavenskoj/DAWG) [IO::Handle::Rollover](https://raku.land/cpan:ATROXAPER/IO::Handle::Rollover) [Radamsa](https://raku.land//Radamsa) |
| Fail                      |     6 | [LLM::Character](https://raku.land/zef:apogee/LLM::Character) [PDF::Combiner](https://raku.land/zef:tbrowder/PDF::Combiner) [Sitemap](https://raku.land/zef:sasha/Sitemap) [Syndicate](https://raku.land/zef:sasha/Syndicate) [Text::Markdown::Discount](https://raku.land/github:hartenfels/Text::Markdown::Discount) [Uni63](https://raku.land//Uni63) |
| InstallableButUntested    |     9 | [HTTP::Server::Async](https://raku.land/zef:raku-community-modules/HTTP::Server::Async) [IO::Socket::Async::SSL](https://raku.land/zef:raku-community-modules/IO::Socket::Async::SSL) [IRC::Client](https://raku.land/zef:lizmat/IRC::Client) [Log::Minimal](https://raku.land//Log::Minimal) [Russian](https://raku.land/zef:slavenskoj/Russian) [Time::Duration](https://raku.land/zef:masukomi/Time::Duration) [Toaster](https://raku.land//Toaster) [Uzu](https://raku.land/cpan:SACOMO/Uzu) [Web::Scraper](https://raku.land/zef:tony-o/Web::Scraper) |
| ZefFailure                |    10 | [BDD::Behave](https://raku.land/zef:gdonald/BDD::Behave) [Cro::RPC::JSON](https://raku.land/zef:vrurg/Cro::RPC::JSON) [LLM::Data::Pipeline](https://raku.land/zef:apogee/LLM::Data::Pipeline) [ParaSeq](https://raku.land/zef:lizmat/ParaSeq) [Proc::ZMQed](https://raku.land/zef:antononcube/Proc::ZMQed) [TXN](https://raku.land//TXN) [TXN::Parser](https://raku.land//TXN::Parser) [TXN::Remarshal](https://raku.land//TXN::Remarshal) [Test::Time](https://raku.land/zef:FCO/Test::Time) [cro](https://raku.land/zef:cro/cro) |
| MissingDependency         |    11 | [App::Ebread](https://raku.land/zef:samy/App::Ebread) [App::Perl6LangServer](https://raku.land/cpan:AZAWAWI/App::Perl6LangServer) [Chemistry::Elements](https://raku.land/github:briandfoy/Chemistry::Elements) [DBIx::NamedQueries](https://raku.land/cpan:MZIESCHA/DBIx::NamedQueries) [Ethelia](https://raku.land/zef:knarkhov/Ethelia) [Learn::Raku::With](https://raku.land/zef:codesections/Learn::Raku::With) [META6::To::Man](https://raku.land/cpan:TBROWDER/META6::To::Man) [Pakku](https://raku.land/zef:hythm/Pakku) [Perl6::Tracer](https://raku.land/github:jaffa4/Perl6::Tracer) [Task::Galaxy](https://raku.land//Task::Galaxy) [Touch](https://raku.land/zef:rir/Touch) |
| CyclicDependency          |    47 | ⋯                         |
| AlwaysFail                |   728 | ⋯                         |
| OK                        |  1704 | ⋯                         |



This run started on 2026-09-04T00:27:54Z and finished in ≈4 hours.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
