[Blin](https://github.com/Raku/Blin) results between 2026.07 ([d53a85f](https://github.com/rakudo/rakudo/commit/d53a85f9deeffbaba941e1cd1f86149a797b2b09)) and HEAD ([0930c6f](https://github.com/rakudo/rakudo/commit/0930c6faccb75cafcc61cfede63063d4c4e18cc2)):

* [ ] [Text::Markdown::Discount](https://raku.land/github:hartenfels/Text::Markdown::Discount) – Fail, Bisected: [60357e5](https://github.com/rakudo/rakudo/commit/60357e53b2a5dc1a32afaf5689da96a7bd19aeab) [96c7630](https://github.com/rakudo/rakudo/commit/96c7630c322fee7de2a769a53fd78575289b7ee5) [a0962b7](https://github.com/rakudo/rakudo/commit/a0962b746121fbb2f882ce422d159eba3721bf81) [c78d52e](https://github.com/rakudo/rakudo/commit/c78d52e39dc8f06acff714615207bd4119aec24a) [4fb0b00](https://github.com/rakudo/rakudo/commit/4fb0b00cdaef6c7dee9744ec8350654e6954dee8)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3485540-i3465036.service; invocation ID: d1a990ec033f46f4a41c6d491c7af6b9
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Text::Markdown::Discount
  ===> Found: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels> [via Zef::Repository::Ecosystems<rea>]
  [Text::Markdown::Discount] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787155192.3485541.6014.320939961205/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/T/Text%3A%3AMarkdown%3A%3ADiscount/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Fetching [OK]: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels> to /home/coke/sandbox/blin/data/zef-data/tmp/1787155192.3485541.6014.320939961205/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  [Text::Markdown::Discount] Command: tar -t -f ./Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  [Text::Markdown::Discount] Command: tar -xvf ./Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz -C ../Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Extraction [OK]: Text::Markdown::Discount to /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Testing: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/01_lib.t
  [Text::Markdown::Discount] # markdown_version: NativeCall::Types::Pointer[int8]<6530649002656>
  [Text::Markdown::Discount] ok 1 - libmarkdown is installed
  [Text::Markdown::Discount] 1..1
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/02_make-flags.t
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
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/03_interna.t
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
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/04_markdown.t
  [Text::Markdown::Discount] ok 1 - string to string
  [Text::Markdown::Discount] ok 2 - file to string
  [Text::Markdown::Discount] ok 3 - string to file
  [Text::Markdown::Discount] ok 4 - file to file
  [Text::Markdown::Discount] ok 5 - HTML conversion ()
  [Text::Markdown::Discount] ok 6 - HTML conversion (nolinks)
  [Text::Markdown::Discount] ok 7 - HTML conversion (nohtml)
  [Text::Markdown::Discount] ok 8 - HTML conversion (nolinks nohtml)
  [Text::Markdown::Discount] 1..8
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/05_dump.t
  [Text::Markdown::Discount] ok 1 - LINKS IMAGE
  [Text::Markdown::Discount] ok 2 - !LINKS IMAGE
  [Text::Markdown::Discount] ok 3 - LINKS !IMAGE
  [Text::Markdown::Discount] ok 4 - !LINKS !IMAGE
  [Text::Markdown::Discount] 1..4
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/06_headers.t
  [Text::Markdown::Discount] ok 1 - 
  [Text::Markdown::Discount] ok 2 - 
  [Text::Markdown::Discount] ok 3 - 
  [Text::Markdown::Discount] ok 4 - 
  [Text::Markdown::Discount] ok 5 - 
  [Text::Markdown::Discount] ok 6 - 
  [Text::Markdown::Discount] ok 7 - 
  [Text::Markdown::Discount] ok 8 - 
  [Text::Markdown::Discount] 1..8
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/07_meta.t
  [Text::Markdown::Discount] 1..1
  [Text::Markdown::Discount] ok 1 - # SKIP Skipping author test
  ===> Testing [OK] for Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  ===> Installing: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  ===> Install [OK] for Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 18.192s
               CPU time consumed: 2min 14.857s
                     Memory peak: 1.1G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3480944-i3551363.service; invocation ID: 817a8a4691584b6693c64bc32341cc0b
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Text::Markdown::Discount
  ===> Found: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels> [via Zef::Repository::Ecosystems<rea>]
  [Text::Markdown::Discount] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787155052.3480954.3976.3870412084843/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/T/Text%3A%3AMarkdown%3A%3ADiscount/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Fetching [OK]: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels> to /home/coke/sandbox/blin/data/zef-data/tmp/1787155052.3480954.3976.3870412084843/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  [Text::Markdown::Discount] Command: tar -t -f ./Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  [Text::Markdown::Discount] Command: tar -xvf ./Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz -C ../Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Extraction [OK]: Text::Markdown::Discount to /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz
  ===> Testing: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/01_lib.t
  [Text::Markdown::Discount] # markdown_version: NativeCall::Types::Pointer[int8]<4466256037920>
  [Text::Markdown::Discount] ok 1 - libmarkdown is installed
  [Text::Markdown::Discount] 1..1
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/02_make-flags.t
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
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/03_interna.t
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
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/04_markdown.t
  [Text::Markdown::Discount] ok 1 - string to string
  [Text::Markdown::Discount] ok 2 - file to string
  [Text::Markdown::Discount] ok 3 - string to file
  [Text::Markdown::Discount] ok 4 - file to file
  [Text::Markdown::Discount] ok 5 - HTML conversion ()
  [Text::Markdown::Discount] ok 6 - HTML conversion (nolinks)
  [Text::Markdown::Discount] ok 7 - HTML conversion (nohtml)
  [Text::Markdown::Discount] ok 8 - HTML conversion (nohtml nolinks)
  [Text::Markdown::Discount] 1..8
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/05_dump.t
  [Text::Markdown::Discount] ok 1 - LINKS IMAGE
  [Text::Markdown::Discount] ok 2 - !LINKS IMAGE
  [Text::Markdown::Discount] ok 3 - LINKS !IMAGE
  [Text::Markdown::Discount] ok 4 - !LINKS !IMAGE
  [Text::Markdown::Discount] 1..4
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/06_headers.t
  [Text::Markdown::Discount] ok 1 - 
  [Text::Markdown::Discount] ok 2 - 
  [Text::Markdown::Discount] ok 3 - 
  [Text::Markdown::Discount] ok 4 - 
  [Text::Markdown::Discount] ok 5 - 
  [Text::Markdown::Discount] ok 6 - 
  [Text::Markdown::Discount] ok 7 - 
  [Text::Markdown::Discount] ok 8 - 
  [Text::Markdown::Discount] 1..8
  [Text::Markdown::Discount] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Text%3A%3AMarkdown%3A%3ADiscount%3Aver%3C0.3.0%3E%3Aauth%3Cgithub%3Ahartenfels%3E.tar.gz/Text-Markdown-Discount-master t/07_meta.t
  [Text::Markdown::Discount] 1..1
  [Text::Markdown::Discount] ok 1 - # SKIP Skipping author test
  ===> Testing [FAIL]: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  [Text::Markdown::Discount] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
  ===> Install [OK] for Text::Markdown::Discount:ver<0.3.0>:auth<github:hartenfels>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 103ms
               CPU time consumed: 2min 5.705s
                     Memory peak: 1.4G (swap: 0B)

  ```
  </details>
* [ ] [Net::BGP](https://raku.land/zef:jmaslak/Net::BGP) – Fail, Bisected: [9cf4f2d](https://github.com/rakudo/rakudo/commit/9cf4f2d2412f6d0b8ba6864d26fb6b1f791fb05e)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3783749-i3846251.service; invocation ID: b6d3a7fbd16b497bb3f0db20956bd879
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Net::BGP
  ===> Found: Net::BGP:ver<0.9.0>:auth<zef:jmaslak> [via Zef::Repository::Ecosystems<fez>]
  [Net::BGP] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787163406.3783755.548.9513686980341/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz https://360.zef.pm/N/ET/NET_BGP/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  ===> Fetching [OK]: Net::BGP:ver<0.9.0>:auth<zef:jmaslak> to /home/coke/sandbox/blin/data/zef-data/tmp/1787163406.3783755.548.9513686980341/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
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
  [Net::BGP] # Listening on port 52359
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
  [Net::BGP] # Listening on port 35057
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
  [Net::BGP] # Listening on port 34973
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
  [Net::BGP] # Listening on port 34813
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

  2 bin/ scripts [bgpmon.p6 bgpmon.rakudoc] installed to:
  /tmp/UPpYP1beuD/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 3min 32.142s
               CPU time consumed: 3min 19.897s
                     Memory peak: 904.5M (swap: 198.4M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3761140-i3781221.service; invocation ID: 88422fb9716d471ca2c4e1a3482894e3
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Net::BGP
  ===> Found: Net::BGP:ver<0.9.0>:auth<zef:jmaslak> [via Zef::Repository::Ecosystems<fez>]
  [Net::BGP] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787162786.3761144.3582.9540377158296/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz https://360.zef.pm/N/ET/NET_BGP/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  ===> Fetching [OK]: Net::BGP:ver<0.9.0>:auth<zef:jmaslak> to /home/coke/sandbox/blin/data/zef-data/tmp/1787162786.3761144.3582.9540377158296/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  [Net::BGP] Command: tar -t -f ./b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  [Net::BGP] Command: tar -xvf ./b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz -C ../b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  ===> Extraction [OK]: Net::BGP to /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz
  ===> Testing: Net::BGP:ver<0.9.0>:auth<zef:jmaslak>
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/00-conversions.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/01-ip-test.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/02-as-list.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/03-afi-safi.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/10-linux-socket.t
  [Net::BGP] KERNEL Name: linux
  [Net::BGP] # Subtest: Basic Server
  [Net::BGP]     ok 1 - sock is proper type
  [Net::BGP]     ok 2 - sock is defined
  [Net::BGP]     ok 3 - bound port does not die
  [Net::BGP]     ok 4 - bound port in proper range
  [Net::BGP] # Listening on port 50905
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
  [Net::BGP] # Listening on port 39593
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
  [Net::BGP]   in sub subtest at /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/share/perl6/core/sources/9679FFF98FD116E36E6DD591E772F79FDAE0B05E (Test) line 430
  [Net::BGP]   in sub subtest at /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/share/perl6/core/sources/9679FFF98FD116E36E6DD591E772F79FDAE0B05E (Test) line 418
  [Net::BGP]   in block <unit> at t/10-linux-socket.t line 109
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/11-socket.t
  [Net::BGP] # Subtest: Basic Server - Native OS
  [Net::BGP]     ok 1 - sock is defined
  [Net::BGP]     ok 2 - connections is a Supply
  [Net::BGP]     ok 3 - bound port promise is kept
  [Net::BGP]     ok 4 - bound port does not die
  [Net::BGP]     ok 5 - bound port in proper range
  [Net::BGP] # Listening on port 38517
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
  [Net::BGP] # Listening on port 43847
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/30-basic.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/31-conn-open-close-event.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/32-Command-Dead-Child.t
  [Net::BGP] ok 1 - Created Net::BGP::Command::Dead-Child Class
  [Net::BGP] ok 2 - Proper Dead-Child command
  [Net::BGP] ok 3 - Payload is correct
  [Net::BGP] 1..3
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/50-messages.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/51-bgp-messages-from-hash.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/52-bgp-messages-raw.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/53-Open-With-Multiple-CapOpts.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/54-Update-Failure.t
  [Net::BGP] ok 1 - BGP message is defined
  [Net::BGP] ok 2 - Message type is correct
  [Net::BGP] ok 3 - Message code is correct
  [Net::BGP] ok 4 - NLRI right
  [Net::BGP] ok 5 - right number of path elems
  [Net::BGP] ok 6 - No NLRI6 Elements
  [Net::BGP] ok 7 - Aggregator ASN correct
  [Net::BGP] ok 8 - Aggregator IP correct
  [Net::BGP] 1..8
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/55-bgp-notification-raw.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/56-bgp-invalid-marker.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/57-bgp-open-bad-asn.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/58-as4-update.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/60-Path-Attributes.t
  [Net::BGP] # Subtest: Extended-Community
  [Net::BGP]     ok 1 - Created Path Attribute
  [Net::BGP]     ok 2 - From Hash capability correct
  [Net::BGP]     ok 3 - From RAW capability correct
  [Net::BGP]     ok 4 - Route type is correct
  [Net::BGP]     1..4
  [Net::BGP] ok 1 - Extended-Community
  [Net::BGP] 1..1
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/70-peer-object.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/80-Validator-Aggregation.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/81-Validator-AS-Path.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/90-basic-bgp.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/91-send-update.t
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
  [Net::BGP] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b2acc52958f570b9100f1f523aeae0d1bdade510.tar.gz/Net-BGP-0.9.0 t/95-bgpmon.t
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
                 Service runtime: 10min 13.876s
               CPU time consumed: 9min 53.545s
                     Memory peak: 3.5G (swap: 831.6M)

  ```
  </details>
* [ ] [AI::NLP](https://raku.land/cpan:KOBOLDWIZ/AI::NLP) – Fail, Bisected: [0930c6f](https://github.com/rakudo/rakudo/commit/0930c6faccb75cafcc61cfede63063d4c4e18cc2)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3362719-i3264230.service; invocation ID: 459bee1e101740c6be2b22b153bc54f5
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: AI::NLP
  ===> Found: AI::NLP:ver<0.1.5>:auth<cpan:KOBOLDWIZ>:api<1> [via Zef::Repository::Ecosystems<rea>]
  [AI::NLP] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787151601.3362721.2719.0626659507943/AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/A/AI%3A%3ANLP/AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz
  ===> Fetching [OK]: AI::NLP:ver<0.1.5>:auth<cpan:KOBOLDWIZ>:api<1> to /home/coke/sandbox/blin/data/zef-data/tmp/1787151601.3362721.2719.0626659507943/AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz
  [AI::NLP] Command: tar -t -f ./AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz
  [AI::NLP] Command: tar -xvf ./AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz -C ../AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz
  ===> Extraction [OK]: AI::NLP to /home/coke/sandbox/blin/data/zef-data/tmp/AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz
  ===> Testing: AI::NLP:ver<0.1.5>:auth<CPAN:HOLYGHOST>:api<1>
  [AI::NLP] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz/AI-NLP t/00-load.t
  [AI::NLP] 1..3
  [AI::NLP] ok 1 - AI::NLP::Matrix module can be use-d ok
  [AI::NLP] ok 2 - AI::NLP::Vector module can be use-d ok
  [AI::NLP] ok 3 - AI::NLP::BPPNet module can be use-d ok
  ===> Testing [OK] for AI::NLP:ver<0.1.5>:auth<CPAN:HOLYGHOST>:api<1>
  ===> Installing: AI::NLP:ver<0.1.5>:auth<CPAN:HOLYGHOST>:api<1>
  ===> Install [OK] for AI::NLP:ver<0.1.5>:auth<CPAN:HOLYGHOST>:api<1>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 4.364s
               CPU time consumed: 1min 58.857s
                     Memory peak: 1.3G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3359694-i3416202.service; invocation ID: 74e0e1348564494d9778733b26619f6d
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: AI::NLP
  No candidates found matching identity: AI::NLP
            Finished with result: exit-code
  Main processes terminated with: code=exited, status=255/EXCEPTION
                 Service runtime: 1min 26.700s
               CPU time consumed: 1min 21.674s
                     Memory peak: 864.6M (swap: 114.1M)

  ```
  </details>
* [ ] [Acme::Cow](https://raku.land//Acme::Cow) – Fail, Bisected: [0930c6f](https://github.com/rakudo/rakudo/commit/0930c6faccb75cafcc61cfede63063d4c4e18cc2)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3363549-i3400829.service; invocation ID: 67a54e3ec63f433b83466ff95bf74bd4
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Acme::Cow
  ===> Found: Acme::Cow:ver<0.0.5>:auth<zef:lizmat> [via Zef::Repository::Ecosystems<fez>]
  [Acme::Cow] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787151596.3363551.3258.607247327946/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz https://360.zef.pm/A/CM/ACME_COW/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz
  ===> Fetching [OK]: Acme::Cow:ver<0.0.5>:auth<zef:lizmat> to /home/coke/sandbox/blin/data/zef-data/tmp/1787151596.3363551.3258.607247327946/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz
  [Acme::Cow] Command: tar -t -f ./b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz
  [Acme::Cow] Command: tar -xvf ./b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz -C ../b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz
  ===> Extraction [OK]: Acme::Cow to /home/coke/sandbox/blin/data/zef-data/tmp/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz
  ===> Testing: Acme::Cow:ver<0.0.5>:auth<zef:lizmat>
  [Acme::Cow] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz/Acme-Cow-0.0.5 t/balloon.t
  [Acme::Cow] 1..20
  [Acme::Cow] ok 1 - 
  [Acme::Cow] ok 2 - 
  [Acme::Cow] ok 3 - 
  [Acme::Cow] ok 4 - 
  [Acme::Cow] ok 5 - 
  [Acme::Cow] ok 6 - 
  [Acme::Cow]  _____
  [Acme::Cow] < Hi. >
  [Acme::Cow]  -----
  [Acme::Cow] ok 7 - 
  [Acme::Cow] ok 8 - 
  [Acme::Cow] ok 9 - 
  [Acme::Cow] ok 10 - 
  [Acme::Cow] ok 11 - 
  [Acme::Cow]        ______
  [Acme::Cow]       (  Hi. )
  [Acme::Cow]        ------
  [Acme::Cow] ok 12 - 
  [Acme::Cow] ok 13 - 
  [Acme::Cow] ok 14 - 
  [Acme::Cow] ok 15 - 
  [Acme::Cow] ok 16 - 
  [Acme::Cow] ok 17 - 
  [Acme::Cow] ok 18 - 
  [Acme::Cow] ok 19 - 
  [Acme::Cow] ok 20 - 
  [Acme::Cow]  ___________________________________________
  [Acme::Cow] / A limerick packs laughs anatomical        \
  [Acme::Cow] | Into space that is quite economical.      |
  [Acme::Cow] |         But the good ones I've seen       |
  [Acme::Cow] |         So seldom are clean               |
  [Acme::Cow] \ And the clean ones so seldom are comical. /
  [Acme::Cow]  -------------------------------------------
  [Acme::Cow] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz/Acme-Cow-0.0.5 t/cow.t
  [Acme::Cow] 1..30
  [Acme::Cow] ok 1 - 
  [Acme::Cow] ok 2 - 
  [Acme::Cow] ok 3 - 
  [Acme::Cow] ok 4 - 
  [Acme::Cow] ok 5 - 
  [Acme::Cow] ok 6 - 
  [Acme::Cow] ok 7 - 
  [Acme::Cow] ok 8 - 
  [Acme::Cow] ok 9 - 
  [Acme::Cow] ok 10 - 
  [Acme::Cow]  _____
  [Acme::Cow] < Hi. >
  [Acme::Cow]  -----
  [Acme::Cow]         \   ^__^
  [Acme::Cow]          \  (oo)\_______
  [Acme::Cow]             (__)\       )\/\
  [Acme::Cow]                 ||----w |
  [Acme::Cow]                 ||     ||
  [Acme::Cow] ok 11 - 
  [Acme::Cow] ok 12 - 
  [Acme::Cow] ok 13 - 
  [Acme::Cow] ok 14 - 
  [Acme::Cow] ok 15 - 
  [Acme::Cow] ok 16 - 
  [Acme::Cow] ok 17 - 
  [Acme::Cow] ok 18 - 
  [Acme::Cow] ok 19 - 
  [Acme::Cow] ok 20 - 
  [Acme::Cow]  _____
  [Acme::Cow] ( Hi. )
  [Acme::Cow]  -----
  [Acme::Cow]         o   ^__^
  [Acme::Cow]          o  (oo)\_______
  [Acme::Cow]             (__)\       )\/\
  [Acme::Cow]                 ||----w |
  [Acme::Cow]                 ||     ||
  [Acme::Cow] ok 21 - 
  [Acme::Cow] ok 22 - 
  [Acme::Cow] ok 23 - 
  [Acme::Cow] ok 24 - 
  [Acme::Cow] ok 25 - 
  [Acme::Cow] ok 26 - 
  [Acme::Cow] ok 27 - 
  [Acme::Cow] ok 28 - 
  [Acme::Cow] ok 29 - 
  [Acme::Cow] ok 30 - 
  [Acme::Cow]  ______
  [Acme::Cow] (  Hi. )
  [Acme::Cow]  ------
  [Acme::Cow]         o   ^__^
  [Acme::Cow]          o  (oo)\_______
  [Acme::Cow]             (__)\       )\/\
  [Acme::Cow]                 ||----w |
  [Acme::Cow]                 ||     ||
  [Acme::Cow] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz/Acme-Cow-0.0.5 t/file.t
  [Acme::Cow] 1..16
  [Acme::Cow] ok 1 - 
  [Acme::Cow] ok 2 - 
  [Acme::Cow] ok 3 - 
  [Acme::Cow] ok 4 - 
  [Acme::Cow] ok 5 - 
  [Acme::Cow] ok 6 - 
  [Acme::Cow] ok 7 - 
  [Acme::Cow] ok 8 - 
  [Acme::Cow] ok 9 - 
  [Acme::Cow] ok 10 - 
  [Acme::Cow] ok 11 - 
  [Acme::Cow] ok 12 - 
  [Acme::Cow] ok 13 - 
  [Acme::Cow] ok 14 - 
  [Acme::Cow] ok 15 - 
  [Acme::Cow] ok 16 - 
  [Acme::Cow]  __________
  [Acme::Cow] < Bwahaha! >
  [Acme::Cow]  ----------
  [Acme::Cow]     \
  [Acme::Cow]      \
  [Acme::Cow]                                    .::!!!!!!!:.
  [Acme::Cow]   .!!!!!:.                        .:!!!!!!!!!!!!
  [Acme::Cow]   ~~~~!!!!!!.                 .:!!!!!!!!!UWWW$$$ 
  [Acme::Cow]       :$$NWX!!:           .:!!!!!!XUWW$$$$$$$$$P 
  [Acme::Cow]       $$$$$##WX!:      .<!!!!UW$$$$"  $$$$$$$$# 
  [Acme::Cow]       $$$$$  $$$UX   :!!UW$$$$$$$$$   4$$$$$* 
  [Acme::Cow]       ^$$$B  $$$$     $$$$$$$$$$$$   d$$R" 
  [Acme::Cow]         "*$bd$$$$      '*$$$$$$$$$$$o+#" 
  [Acme::Cow]              """"          """"""" 
  [Acme::Cow] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz/Acme-Cow-0.0.5 t/pm.t
  [Acme::Cow] 1..12
  [Acme::Cow] ok 1 - 
  [Acme::Cow] ok 2 - 
  [Acme::Cow] ok 3 - 
  [Acme::Cow] ok 4 - 
  [Acme::Cow] ok 5 - 
  [Acme::Cow] ok 6 - 
  [Acme::Cow] ok 7 - 
  [Acme::Cow] ok 8 - 
  [Acme::Cow] ok 9 - 
  [Acme::Cow] ok 10 - 
  [Acme::Cow] ok 11 - 
  [Acme::Cow] ok 12 - 
  [Acme::Cow]                                                _____
  [Acme::Cow]                                               < Hi. >
  [Acme::Cow]                                                -----
  [Acme::Cow]                                               /
  [Acme::Cow]                                             /
  [Acme::Cow]           oO)-.                       .-(Oo
  [Acme::Cow]          /__  _\                     /_  __\
  [Acme::Cow]          \  \(  |     ()~()         |  )/  /
  [Acme::Cow]           \__|\ |    (-___-)        | /|__/
  [Acme::Cow]           '  '--'    ==`-'==        '--'  '
  ===> Testing [OK] for Acme::Cow:ver<0.0.5>:auth<zef:lizmat>
  ===> Installing: Acme::Cow:ver<0.0.5>:auth<zef:lizmat>
  ===> Install [OK] for Acme::Cow:ver<0.0.5>:auth<zef:lizmat>

  3 bin/ scripts [cowthink cowpm cowsay] installed to:
  /tmp/j3SCdT5Zmu/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 54.293s
               CPU time consumed: 1min 49.917s
                     Memory peak: 807.4M (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3359827-i3400699.service; invocation ID: 8d08f59439f340f6bb4d800bb0ec618b
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Acme::Cow
  ===> Found: Acme::Cow:ver<0.0.5>:auth<zef:lizmat> [via Zef::Repository::Ecosystems<fez>]
  [Acme::Cow] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787151485.3359834.2557.6001221286547/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz https://360.zef.pm/A/CM/ACME_COW/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz
  ===> Fetching [OK]: Acme::Cow:ver<0.0.5>:auth<zef:lizmat> to /home/coke/sandbox/blin/data/zef-data/tmp/1787151485.3359834.2557.6001221286547/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz
  [Acme::Cow] Command: tar -t -f ./b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz
  [Acme::Cow] Command: tar -xvf ./b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz -C ../b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz
  ===> Extraction [OK]: Acme::Cow to /home/coke/sandbox/blin/data/zef-data/tmp/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz
  ===> Testing: Acme::Cow:ver<0.0.5>:auth<zef:lizmat>
  [Acme::Cow] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz/Acme-Cow-0.0.5 t/balloon.t
  [Acme::Cow] 1..20
  [Acme::Cow] ok 1 - 
  [Acme::Cow] ok 2 - 
  [Acme::Cow] ok 3 - 
  [Acme::Cow] ok 4 - 
  [Acme::Cow] ok 5 - 
  [Acme::Cow] ok 6 - 
  [Acme::Cow]  _____
  [Acme::Cow] < Hi. >
  [Acme::Cow]  -----
  [Acme::Cow] ok 7 - 
  [Acme::Cow] ok 8 - 
  [Acme::Cow] ok 9 - 
  [Acme::Cow] ok 10 - 
  [Acme::Cow] ok 11 - 
  [Acme::Cow]        ______
  [Acme::Cow]       (  Hi. )
  [Acme::Cow]        ------
  [Acme::Cow] ok 12 - 
  [Acme::Cow] ok 13 - 
  [Acme::Cow] ok 14 - 
  [Acme::Cow] ok 15 - 
  [Acme::Cow] ok 16 - 
  [Acme::Cow] ok 17 - 
  [Acme::Cow] ok 18 - 
  [Acme::Cow] ok 19 - 
  [Acme::Cow] ok 20 - 
  [Acme::Cow]  ___________________________________________
  [Acme::Cow] / A limerick packs laughs anatomical        \
  [Acme::Cow] | Into space that is quite economical.      |
  [Acme::Cow] |         But the good ones I've seen       |
  [Acme::Cow] |         So seldom are clean               |
  [Acme::Cow] \ And the clean ones so seldom are comical. /
  [Acme::Cow]  -------------------------------------------
  [Acme::Cow] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz/Acme-Cow-0.0.5 t/cow.t
  [Acme::Cow] 1..30
  [Acme::Cow] ok 1 - 
  [Acme::Cow] ok 2 - 
  [Acme::Cow] ok 3 - 
  [Acme::Cow] ok 4 - 
  [Acme::Cow] ok 5 - 
  [Acme::Cow] ok 6 - 
  [Acme::Cow] ok 7 - 
  [Acme::Cow] ok 8 - 
  [Acme::Cow] ok 9 - 
  [Acme::Cow] ok 10 - 
  [Acme::Cow]  _____
  [Acme::Cow] < Hi. >
  [Acme::Cow]  -----
  [Acme::Cow]         \   ^__^
  [Acme::Cow]          \  (oo)\_______
  [Acme::Cow]             (__)\       )\/\
  [Acme::Cow]                 ||----w |
  [Acme::Cow]                 ||     ||
  [Acme::Cow] ok 11 - 
  [Acme::Cow] ok 12 - 
  [Acme::Cow] ok 13 - 
  [Acme::Cow] ok 14 - 
  [Acme::Cow] ok 15 - 
  [Acme::Cow] ok 16 - 
  [Acme::Cow] ok 17 - 
  [Acme::Cow] ok 18 - 
  [Acme::Cow] ok 19 - 
  [Acme::Cow] ok 20 - 
  [Acme::Cow]  _____
  [Acme::Cow] ( Hi. )
  [Acme::Cow]  -----
  [Acme::Cow]         o   ^__^
  [Acme::Cow]          o  (oo)\_______
  [Acme::Cow]             (__)\       )\/\
  [Acme::Cow]                 ||----w |
  [Acme::Cow]                 ||     ||
  [Acme::Cow] ok 21 - 
  [Acme::Cow] ok 22 - 
  [Acme::Cow] ok 23 - 
  [Acme::Cow] ok 24 - 
  [Acme::Cow] ok 25 - 
  [Acme::Cow] ok 26 - 
  [Acme::Cow] ok 27 - 
  [Acme::Cow] ok 28 - 
  [Acme::Cow] ok 29 - 
  [Acme::Cow] ok 30 - 
  [Acme::Cow]  ______
  [Acme::Cow] (  Hi. )
  [Acme::Cow]  ------
  [Acme::Cow]         o   ^__^
  [Acme::Cow]          o  (oo)\_______
  [Acme::Cow]             (__)\       )\/\
  [Acme::Cow]                 ||----w |
  [Acme::Cow]                 ||     ||
  [Acme::Cow] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz/Acme-Cow-0.0.5 t/file.t
  [Acme::Cow] 1..16
  [Acme::Cow] ok 1 - 
  [Acme::Cow] ok 2 - 
  [Acme::Cow] ok 3 - 
  [Acme::Cow] ok 4 - 
  [Acme::Cow] ok 5 - 
  [Acme::Cow] ok 6 - 
  [Acme::Cow] ok 7 - 
  [Acme::Cow] ok 8 - 
  [Acme::Cow] ok 9 - 
  [Acme::Cow] ok 10 - 
  [Acme::Cow] ok 11 - 
  [Acme::Cow] ok 12 - 
  [Acme::Cow] ok 13 - 
  [Acme::Cow] ok 14 - 
  [Acme::Cow] ok 15 - 
  [Acme::Cow] ok 16 - 
  [Acme::Cow]  __________
  [Acme::Cow] < Bwahaha! >
  [Acme::Cow]  ----------
  [Acme::Cow]     \
  [Acme::Cow]      \
  [Acme::Cow]                                    .::!!!!!!!:.
  [Acme::Cow]   .!!!!!:.                        .:!!!!!!!!!!!!
  [Acme::Cow]   ~~~~!!!!!!.                 .:!!!!!!!!!UWWW$$$ 
  [Acme::Cow]       :$$NWX!!:           .:!!!!!!XUWW$$$$$$$$$P 
  [Acme::Cow]       $$$$$##WX!:      .<!!!!UW$$$$"  $$$$$$$$# 
  [Acme::Cow]       $$$$$  $$$UX   :!!UW$$$$$$$$$   4$$$$$* 
  [Acme::Cow]       ^$$$B  $$$$     $$$$$$$$$$$$   d$$R" 
  [Acme::Cow]         "*$bd$$$$      '*$$$$$$$$$$$o+#" 
  [Acme::Cow]              """"          """"""" 
  [Acme::Cow] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b1518cbf636e7ad3fba4fd6300c97f48d4a91523.tar.gz/Acme-Cow-0.0.5 t/pm.t
  ===> Testing [FAIL]: Acme::Cow:ver<0.0.5>:auth<zef:lizmat>
  [Acme::Cow] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Acme::Cow:ver<0.0.5>:auth<zef:lizmat>
  ===> Install [OK] for Acme::Cow:ver<0.0.5>:auth<zef:lizmat>

  3 bin/ scripts [cowsay cowpm cowthink] installed to:
  /home/coke/sandbox/blin/installed/Acme::Cow__0.2_0/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 39.956s
               CPU time consumed: 1min 34.597s
                     Memory peak: 1G (swap: 135M)

  ```
  </details>
* [ ] [Cro::WebSocket](https://raku.land/zef:cro/Cro::WebSocket) – Fail, Bisected: [0930c6f](https://github.com/rakudo/rakudo/commit/0930c6faccb75cafcc61cfede63063d4c4e18cc2)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3688819-i3700689.service; invocation ID: 1650882417b544df8c585220c46805c8
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Cro::WebSocket
  ===> Found: Cro::WebSocket:ver<0.8.10>:auth<zef:cro>:api<0> [via Zef::Repository::Ecosystems<fez>]
  [Cro::WebSocket] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787160759.3688825.702.6862569460212/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz https://360.zef.pm/C/RO/CRO_WEBSOCKET/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz
  ===> Fetching [OK]: Cro::WebSocket:ver<0.8.10>:auth<zef:cro>:api<0> to /home/coke/sandbox/blin/data/zef-data/tmp/1787160759.3688825.702.6862569460212/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz
  [Cro::WebSocket] Command: tar -t -f ./ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz
  [Cro::WebSocket] Command: tar -xvf ./ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz -C ../ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz
  ===> Extraction [OK]: Cro::WebSocket to /home/coke/sandbox/blin/data/zef-data/tmp/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz
  ===> Testing: Cro::WebSocket:ver<0.8.10>:auth<zef:cro>:api<0>
  [Cro::WebSocket] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz/dist t/http-router-websocket.rakutest
  [Cro::WebSocket] # Subtest: Connection is not upgraded, 400 Bad Request
  [Cro::WebSocket]     1..2
  [Cro::WebSocket]     ok 1 - code dies
  [Cro::WebSocket]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::WebSocket] ok 1 - Connection is not upgraded, 400 Bad Request
  [Cro::WebSocket] ok 2 - All expected responses were received
  [Cro::WebSocket] ok 3 - Got first message response
  [Cro::WebSocket] ok 4 - Got second message response
  [Cro::WebSocket] ok 5 - Got third message response
  [Cro::WebSocket] ok 6 - Get back valid JSON from websocket endpoint with JSON parser/serializer endpoint
  [Cro::WebSocket] ok 7 - Expected data returned (1)
  [Cro::WebSocket] ok 8 - Expected data returned (2)
  [Cro::WebSocket] ok 9 - Expected data returned (3)
  [Cro::WebSocket] ok 10 - Get back valid JSON from websocket endpoint that uses :json
  [Cro::WebSocket] ok 11 - Expected data returned (1)
  [Cro::WebSocket] ok 12 - Expected data returned (2)
  [Cro::WebSocket] ok 13 - Expected data returned (3)
  [Cro::WebSocket] 1..13
  [Cro::WebSocket] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz/dist t/websocket-frame-parser.rakutest
  [Cro::WebSocket] ok 1 - WebSocket frame parser is a transform
  [Cro::WebSocket] ok 2 - WebSocket frame parser consumes TCP messages
  [Cro::WebSocket] ok 3 - WebSocket frame parser produces Frames
  [Cro::WebSocket] ok 4 - Hello
  [Cro::WebSocket] ok 5 - check 1
  [Cro::WebSocket] ok 6 - check 2
  [Cro::WebSocket] ok 7 - check 3
  [Cro::WebSocket] ok 8 - Masked Hello
  [Cro::WebSocket] ok 9 - check 1
  [Cro::WebSocket] ok 10 - check 2
  [Cro::WebSocket] ok 11 - check 3
  [Cro::WebSocket] ok 12 - Hel
  [Cro::WebSocket] ok 13 - check 1
  [Cro::WebSocket] ok 14 - check 2
  [Cro::WebSocket] ok 15 - check 3
  [Cro::WebSocket] ok 16 - lo
  [Cro::WebSocket] ok 17 - check 1
  [Cro::WebSocket] ok 18 - check 2
  [Cro::WebSocket] ok 19 - check 3
  [Cro::WebSocket] ok 20 - Unmasked ping request
  [Cro::WebSocket] ok 21 - check 1
  [Cro::WebSocket] ok 22 - check 2
  [Cro::WebSocket] ok 23 - check 3
  [Cro::WebSocket] ok 24 - Empty unmasked ping response
  [Cro::WebSocket] ok 25 - check 1
  [Cro::WebSocket] ok 26 - check 2
  [Cro::WebSocket] ok 27 - check 3
  [Cro::WebSocket] ok 28 - Masked ping response
  [Cro::WebSocket] ok 29 - check 1
  [Cro::WebSocket] ok 30 - check 2
  [Cro::WebSocket] ok 31 - check 3
  [Cro::WebSocket] ok 32 - Masked ping response
  [Cro::WebSocket] ok 33 - check 1
  [Cro::WebSocket] ok 34 - check 2
  [Cro::WebSocket] ok 35 - check 3
  [Cro::WebSocket] ok 36 - 256 bytes binary message in a single unmasked frame
  [Cro::WebSocket] ok 37 - check 1
  [Cro::WebSocket] ok 38 - check 2
  [Cro::WebSocket] ok 39 - check 3
  [Cro::WebSocket] ok 40 - 256 bytes binary message in a single unmasked frame
  [Cro::WebSocket] ok 41 - check 1
  [Cro::WebSocket] ok 42 - check 2
  [Cro::WebSocket] ok 43 - check 3
  [Cro::WebSocket] ok 44 - 32 KiB binary message in a single unmasked frame
  [Cro::WebSocket] ok 45 - check 1
  [Cro::WebSocket] ok 46 - check 2
  [Cro::WebSocket] ok 47 - check 3
  [Cro::WebSocket] ok 48 - 32 KiB binary message in a single unmasked frame
  [Cro::WebSocket] ok 49 - check 1
  [Cro::WebSocket] ok 50 - check 2
  [Cro::WebSocket] ok 51 - check 3
  [Cro::WebSocket] ok 52 - 64 KiB binary message in a single unmasked frame
  [Cro::WebSocket] ok 53 - check 1
  [Cro::WebSocket] ok 54 - check 2
  [Cro::WebSocket] ok 55 - 64 KiB binary message in a single unmasked frame
  [Cro::WebSocket] ok 56 - check 1
  [Cro::WebSocket] ok 57 - check 2
  [Cro::WebSocket] 1..57
  [Cro::WebSocket] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz/dist t/websocket-frame-serializer.rakutest
  [Cro::WebSocket] ok 1 - WebSocket frame serializer is a transform
  [Cro::WebSocket] ok 2 - WebSocket frame serializer consumes TCP messages
  [Cro::WebSocket] ok 3 - WebSocket frame serializer produces Frames
  [Cro::WebSocket] # Subtest: Hello text frame
  [Cro::WebSocket]     ok 1 - fin flag
  [Cro::WebSocket]     ok 2 - opcode
  [Cro::WebSocket]     ok 3 - payload type
  [Cro::WebSocket]     ok 4 - payload contents
  [Cro::WebSocket]     1..4
  [Cro::WebSocket] ok 4 - Hello text frame
  [Cro::WebSocket] # Subtest: Masked Hello
  [Cro::WebSocket]     ok 1 - fin flag
  [Cro::WebSocket]     ok 2 - opcode
  [Cro::WebSocket]     ok 3 - payload type
  [Cro::WebSocket]     ok 4 - payload contents
  [Cro::WebSocket]     1..4
  [Cro::WebSocket] ok 5 - Masked Hello
  [Cro::WebSocket] # Subtest: Hel
  [Cro::WebSocket]     ok 1 - fin flag
  [Cro::WebSocket]     ok 2 - opcode
  [Cro::WebSocket]     ok 3 - payload type
  [Cro::WebSocket]     ok 4 - payload contents
  [Cro::WebSocket]     1..4
  [Cro::WebSocket] ok 6 - Hel
  [Cro::WebSocket] # Subtest: lo
  [Cro::WebSocket]     ok 1 - fin flag
  [Cro::WebSocket]     ok 2 - opcode
  [Cro::WebSocket]     ok 3 - payload type
  [Cro::WebSocket]     ok 4 - payload contents
  [Cro::WebSocket]     1..4
  [Cro::WebSocket] ok 7 - lo
  [Cro::WebSocket] # Subtest: Unmasked ping request
  [Cro::WebSocket]     ok 1 - fin flag
  [Cro::WebSocket]     ok 2 - opcode
  [Cro::WebSocket]     ok 3 - payload type
  [Cro::WebSocket]     ok 4 - payload contents
  [Cro::WebSocket]     1..4
  [Cro::WebSocket] ok 8 - Unmasked ping request
  [Cro::WebSocket] # Subtest: Masked ping response
  [Cro::WebSocket]     ok 1 - fin flag
  [Cro::WebSocket]     ok 2 - opcode
  [Cro::WebSocket]     ok 3 - payload type
  [Cro::WebSocket]     ok 4 - payload contents
  [Cro::WebSocket]     1..4
  [Cro::WebSocket] ok 9 - Masked ping response
  [Cro::WebSocket] # Subtest: 256 bytes binary message in a single unmasked frame
  [Cro::WebSocket]     ok 1 - fin flag
  [Cro::WebSocket]     ok 2 - opcode
  [Cro::WebSocket]     ok 3 - payload type
  [Cro::WebSocket]     ok 4 - payload contents
  [Cro::WebSocket]     1..4
  [Cro::WebSocket] ok 10 - 256 bytes binary message in a single unmasked frame
  [Cro::WebSocket] # Subtest: 32 KiB binary message in a single unmasked frame
  [Cro::WebSocket]     ok 1 - fin flag
  [Cro::WebSocket]     ok 2 - opcode
  [Cro::WebSocket]     ok 3 - payload type
  [Cro::WebSocket]     ok 4 - payload contents
  [Cro::WebSocket]     1..4
  [Cro::WebSocket] ok 11 - 32 KiB binary message in a single unmasked frame
  [Cro::WebSocket] # Subtest: 64 KiB binary message in a single unmasked frame
  [Cro::WebSocket]     ok 1 - fin flag
  [Cro::WebSocket]     ok 2 - opcode
  [Cro::WebSocket]     ok 3 - payload type
  [Cro::WebSocket]     ok 4 - payload contents
  [Cro::WebSocket]     1..4
  [Cro::WebSocket] ok 12 - 64 KiB binary message in a single unmasked frame
  [Cro::WebSocket] 1..12
  [Cro::WebSocket] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz/dist t/websocket-handler.rakutest
  [Cro::WebSocket] ok 1 - 
  [Cro::WebSocket] ok 2 - 
  [Cro::WebSocket] ok 3 - 
  [Cro::WebSocket] ok 4 - Close code is 1000
  [Cro::WebSocket] 1..4
  [Cro::WebSocket] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz/dist t/websocket-message-parser.rakutest
  [Cro::WebSocket] ok 1 - Hello
  [Cro::WebSocket] ok 2 - check 1
  [Cro::WebSocket] ok 3 - check 2
  [Cro::WebSocket] ok 4 - check 3
  [Cro::WebSocket] ok 5 - Splitted Hello
  [Cro::WebSocket] ok 6 - check 1
  [Cro::WebSocket] ok 7 - check 2
  [Cro::WebSocket] ok 8 - check 3
  [Cro::WebSocket] ok 9 - Unmasked ping request
  [Cro::WebSocket] ok 10 - check 1
  [Cro::WebSocket] ok 11 - check 2
  [Cro::WebSocket] ok 12 - check 3
  [Cro::WebSocket] ok 13 - Splitted big data package
  [Cro::WebSocket] ok 14 - check 1
  [Cro::WebSocket] ok 15 - check 2
  [Cro::WebSocket] ok 16 - check 3
  [Cro::WebSocket] 1..16
  [Cro::WebSocket] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz/dist t/websocket-message-serializer.rakutest
  [Cro::WebSocket] ok 1 - check 1
  [Cro::WebSocket] ok 2 - check 2
  [Cro::WebSocket] ok 3 - check 3
  [Cro::WebSocket] ok 4 - Hello
  [Cro::WebSocket] ok 5 - check 1
  [Cro::WebSocket] ok 6 - check 2
  [Cro::WebSocket] ok 7 - check 3
  [Cro::WebSocket] ok 8 - check 1
  [Cro::WebSocket] ok 9 - check 2
  [Cro::WebSocket] ok 10 - check 3
  [Cro::WebSocket] ok 11 - check 1
  [Cro::WebSocket] ok 12 - check 2
  [Cro::WebSocket] ok 13 - check 3
  [Cro::WebSocket] ok 14 - Splitted hello
  [Cro::WebSocket] ok 15 - check 1
  [Cro::WebSocket] ok 16 - Control message
  [Cro::WebSocket] ok 17 - check 1
  [Cro::WebSocket] ok 18 - check 2
  [Cro::WebSocket] ok 19 - check 3
  [Cro::WebSocket] ok 20 - check 1
  [Cro::WebSocket] ok 21 - check 2
  [Cro::WebSocket] ok 22 - check 3
  [Cro::WebSocket] ok 23 - check 1
  [Cro::WebSocket] ok 24 - check 2
  [Cro::WebSocket] ok 25 - check 3
  [Cro::WebSocket] ok 26 - check 1
  [Cro::WebSocket] ok 27 - check 2
  [Cro::WebSocket] ok 28 - check 3
  [Cro::WebSocket] ok 29 - Control message in-between
  [Cro::WebSocket] 1..29
  [Cro::WebSocket] Command: /tmp/whateverable/rakudo-moar/d53a85f9deeffbaba941e1cd1f86149a797b2b09/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz/dist t/websocket-message.rakutest
  [Cro::WebSocket] ok 1 - Is text
  [Cro::WebSocket] ok 2 - Is data
  [Cro::WebSocket] ok 3 - Body is passed
  [Cro::WebSocket] ok 4 - Is binary
  [Cro::WebSocket] ok 5 - Is data
  [Cro::WebSocket] # Subtest: Binary message cannot have body-text called on it
  [Cro::WebSocket]     1..2
  [Cro::WebSocket]     ok 1 - code dies
  [Cro::WebSocket]     ok 2 - right exception type (X::Cro::BodyNotText)
  [Cro::WebSocket] ok 6 - Binary message cannot have body-text called on it
  [Cro::WebSocket] ok 7 - Body can be get as blob
  [Cro::WebSocket] ok 8 - Checked 0
  [Cro::WebSocket] ok 9 - Checked 1
  [Cro::WebSocket] ok 10 - Checked 2
  [Cro::WebSocket] 1..10
  ===> Testing [OK] for Cro::WebSocket:ver<0.8.10>:auth<zef:cro>:api<0>
  ===> Installing: Cro::WebSocket:ver<0.8.10>:auth<zef:cro>:api<0>
  ===> Install [OK] for Cro::WebSocket:ver<0.8.10>:auth<zef:cro>:api<0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 7min 39.262s
               CPU time consumed: 6min 32.631s
                     Memory peak: 1.6G (swap: 716.5M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3683270-i3720392.service; invocation ID: 94c21c100f894f2d9c3fe598c638b295
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Cro::WebSocket
  ===> Found: Cro::WebSocket:ver<0.8.10>:auth<zef:cro>:api<0> [via Zef::Repository::Ecosystems<fez>]
  [Cro::WebSocket] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787160550.3683273.3435.949446076914/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz https://360.zef.pm/C/RO/CRO_WEBSOCKET/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz
  ===> Fetching [OK]: Cro::WebSocket:ver<0.8.10>:auth<zef:cro>:api<0> to /home/coke/sandbox/blin/data/zef-data/tmp/1787160550.3683273.3435.949446076914/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz
  [Cro::WebSocket] Command: tar -t -f ./ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz
  [Cro::WebSocket] Command: tar -xvf ./ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz -C ../ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz
  ===> Extraction [OK]: Cro::WebSocket to /home/coke/sandbox/blin/data/zef-data/tmp/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz
  ===> Testing: Cro::WebSocket:ver<0.8.10>:auth<zef:cro>:api<0>
  [Cro::WebSocket] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ed1f2481248f53caafc607573edd72b2f1402e58.tar.gz/dist t/http-router-websocket.rakutest
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 2min 45.771s
               CPU time consumed: 2min 15.876s
                     Memory peak: 1.6G (swap: 576.3M)

  ```
  </details>
* [ ] [Debugging::Tool](https://raku.land/zef:lucs/Debugging::Tool) – Fail, Bisected: [1a08ca7](https://github.com/rakudo/rakudo/commit/1a08ca762010ff035c3ee106c842464a68d301e6)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3756668-i3653415.service; invocation ID: 1505fb17344b48a1ab5f18c19fc7e1d9
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Debugging::Tool
  ===> Found: Debugging::Tool:ver<0.3.1>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [Debugging::Tool] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787162669.3756670.2981.349591125786/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz https://360.zef.pm/D/EB/DEBUGGING_TOOL/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  ===> Fetching [OK]: Debugging::Tool:ver<0.3.1>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1787162669.3756670.2981.349591125786/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
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
                 Service runtime: 4min 19.124s
               CPU time consumed: 3min 49.034s
                     Memory peak: 869.2M (swap: 378.8M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3753066-i3739071.service; invocation ID: a6ef9db461854f6db02c6abeedb5053c
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Debugging::Tool
  ===> Found: Debugging::Tool:ver<0.3.1>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [Debugging::Tool] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787162537.3753079.6718.990884617504/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz https://360.zef.pm/D/EB/DEBUGGING_TOOL/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  ===> Fetching [OK]: Debugging::Tool:ver<0.3.1>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1787162537.3753079.6718.990884617504/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  [Debugging::Tool] Command: tar -t -f ./e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  [Debugging::Tool] Command: tar -xvf ./e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz -C ../e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  ===> Extraction [OK]: Debugging::Tool to /home/coke/sandbox/blin/data/zef-data/tmp/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz
  ===> Testing: Debugging::Tool:ver<0.3.1>:auth<zef:lucs>
  [Debugging::Tool] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/e785d3b09ae5b82f75a0448ae088e73f464a5f0b.tar.gz t/all.rakutest
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
                 Service runtime: 1min 54.320s
               CPU time consumed: 1min 56.898s
                     Memory peak: 1.3G (swap: 115.5M)

  ```
  </details>
* [ ] [File::TreeBuilder](https://raku.land/zef:lucs/File::TreeBuilder) – Fail, Bisected: [1a08ca7](https://github.com/rakudo/rakudo/commit/1a08ca762010ff035c3ee106c842464a68d301e6)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3757053-i3777936.service; invocation ID: beb7f9b6d6f147d9827ee6fcbf2c4051
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: File::TreeBuilder
  ===> Found: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [File::TreeBuilder] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787162676.3757060.2737.7080011062526/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz https://360.zef.pm/F/IL/FILE_TREEBUILDER/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  ===> Fetching [OK]: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1787162676.3757060.2737.7080011062526/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
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
                 Service runtime: 2min 6.824s
               CPU time consumed: 1min 51.207s
                     Memory peak: 823.4M (swap: 133.7M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3753126-i3801566.service; invocation ID: 356d7d59d8464d3487194125f90434e8
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: File::TreeBuilder
  ===> Found: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [File::TreeBuilder] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787162543.3753129.13.12011407766267/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz https://360.zef.pm/F/IL/FILE_TREEBUILDER/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  ===> Fetching [OK]: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1787162543.3753129.13.12011407766267/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  [File::TreeBuilder] Command: tar -t -f ./29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  [File::TreeBuilder] Command: tar -xvf ./29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz -C ../29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  ===> Extraction [OK]: File::TreeBuilder to /home/coke/sandbox/blin/data/zef-data/tmp/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz
  ===> Testing: File::TreeBuilder:ver<0.2.0>:auth<zef:lucs>
  [File::TreeBuilder] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/29dc69fda1a8a9bdb41aa2be428f22387b221cbe.tar.gz t/main.rakutest
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
                 Service runtime: 2min 1.675s
               CPU time consumed: 2min 2.471s
                     Memory peak: 1.3G (swap: 117M)

  ```
  </details>
* [ ] [MIDI::Make](https://raku.land/zef:pelevesque/MIDI::Make) – Fail, Bisected: [1a08ca7](https://github.com/rakudo/rakudo/commit/1a08ca762010ff035c3ee106c842464a68d301e6)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3757208-i3781132.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: MIDI::Make
  ===> Found: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0> [via Zef::Repository::Ecosystems<fez>]
  [MIDI::Make] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787162683.3757211.8601.679606497471/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz https://360.zef.pm/M/ID/MIDI_MAKE/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  ===> Fetching [OK]: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0> to /home/coke/sandbox/blin/data/zef-data/tmp/1787162683.3757211.8601.679606497471/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
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
                 Service runtime: 2min 14.430s
               CPU time consumed: 1min 55.032s
                     Memory peak: 766.8M (swap: 148.7M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3753393-i3801576.service; invocation ID: e0b0fce6fa6d4c13addc2ee439c8db33
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: MIDI::Make
  ===> Found: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0> [via Zef::Repository::Ecosystems<fez>]
  [MIDI::Make] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787162545.3753396.5430.68188473931/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz https://360.zef.pm/M/ID/MIDI_MAKE/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  ===> Fetching [OK]: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0> to /home/coke/sandbox/blin/data/zef-data/tmp/1787162545.3753396.5430.68188473931/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  [MIDI::Make] Command: tar -t -f ./b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  [MIDI::Make] Command: tar -xvf ./b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz -C ../b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  ===> Extraction [OK]: MIDI::Make to /home/coke/sandbox/blin/data/zef-data/tmp/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz
  ===> Testing: MIDI::Make:ver<0.11.0>:auth<zef:pelevesque>:api<1.0>
  [MIDI::Make] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b3ef75d1f30caf73071db445133800001bfcbd60.tar.gz t/all.rakutest
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
                 Service runtime: 1min 56.437s
               CPU time consumed: 1min 58.546s
                     Memory peak: 1.3G (swap: 143M)

  ```
  </details>
* [ ] [Test::Selector](https://raku.land/zef:lucs/Test::Selector) – Fail, Bisected: [1a08ca7](https://github.com/rakudo/rakudo/commit/1a08ca762010ff035c3ee106c842464a68d301e6)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p3609509-i3662810.service; invocation ID: aa97e6e64f364fc3bb416c7b15edabf8
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Test::Selector
  ===> Found: Test::Selector:ver<0.4.1>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [Test::Selector] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787158611.3609512.6836.074455878941/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz https://360.zef.pm/T/ES/TEST_SELECTOR/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  ===> Fetching [OK]: Test::Selector:ver<0.4.1>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1787158611.3609512.6836.074455878941/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
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
  /tmp/40JjwZfHzC/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 14.811s
               CPU time consumed: 2min 11.922s
                     Memory peak: 891.6M (swap: 32M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p3601026-i3629793.service; invocation ID: 7a4d4e8ae57e46cd9407990e84846498
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Test::Selector
  ===> Found: Test::Selector:ver<0.4.1>:auth<zef:lucs> [via Zef::Repository::Ecosystems<fez>]
  [Test::Selector] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787158403.3601028.5880.338292162452/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz https://360.zef.pm/T/ES/TEST_SELECTOR/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  ===> Fetching [OK]: Test::Selector:ver<0.4.1>:auth<zef:lucs> to /home/coke/sandbox/blin/data/zef-data/tmp/1787158403.3601028.5880.338292162452/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  [Test::Selector] Command: tar -t -f ./6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  [Test::Selector] Command: tar -xvf ./6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz -C ../6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  ===> Extraction [OK]: Test::Selector to /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz
  ===> Testing: Test::Selector:ver<0.4.1>:auth<zef:lucs>
  [Test::Selector] Command: /tmp/whateverable/rakudo-moar/0930c6faccb75cafcc61cfede63063d4c4e18cc2/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz t/all.rakutest
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
  [Test::Selector] # Failed test 't_ignore-test Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] not ok 3 - t_ignore-test Err okay.
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/yAgr3vDIeg
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/yAgr3vDIeg:3'
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
  [Test::Selector] not ok 5 - t_glob_prob Err okay.
  [Test::Selector] # Failed test 't_glob_prob Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/UI1RQPqAu9
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/UI1RQPqAu9:3'
  [Test::Selector] not ok 6 - t_char-range Out okay.
  [Test::Selector] # Failed test 't_char-range Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # N1d
  [Test::Selector] #    # N1b
  [Test::Selector] #    # N1ba
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] # Failed test 't_char-range Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] not ok 7 - t_char-range Err okay.
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/UVsrhfmqDk
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/UVsrhfmqDk:3'
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
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/wPQ2d12x3m
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/wPQ2d12x3m:3'
  [Test::Selector] not ok 10 - t_skip-non-match Out okay.
  [Test::Selector] # Failed test 't_skip-non-match Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 11 - t_skip-non-match Err okay.
  [Test::Selector] # Failed test 't_skip-non-match Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/IwgE0f4GXr
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/IwgE0f4GXr:3'
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
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/8JTz2MTAw0
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/8JTz2MTAw0:3'
  [Test::Selector] not ok 14 - t_var-test-id Out okay.
  [Test::Selector] # Failed test 't_var-test-id Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a3b
  [Test::Selector] # ok 1 - 42 is true.
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 15 - t_var-test-id Err okay.
  [Test::Selector] # Failed test 't_var-test-id Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/vMNYzr7QPO
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/vMNYzr7QPO:3'
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
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/leBkjFj9LM
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/leBkjFj9LM:3'
  [Test::Selector] not ok 18 - t_matchall_dflt Out okay.
  [Test::Selector] # Failed test 't_matchall_dflt Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a5
  [Test::Selector] # ok 1 - 42 is true.
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] # Failed test 't_matchall_dflt Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/AaicqyhGZM
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/AaicqyhGZM:3'
  [Test::Selector] not ok 19 - t_matchall_dflt Err okay.
  [Test::Selector] not ok 20 - t_no-match Out okay.
  [Test::Selector] # Failed test 't_no-match Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 21 - t_no-match Err okay.
  [Test::Selector] # Failed test 't_no-match Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/AieP8O0O_2
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/AieP8O0O_2:3'
  [Test::Selector] not ok 22 - t_list Out okay.
  [Test::Selector] # Failed test 't_list Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: 'a7
  [Test::Selector] # b1
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 23 - t_list Err okay.
  [Test::Selector] # Failed test 't_list Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/gVvPZdH4NY
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/gVvPZdH4NY:3'
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
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/9O9pH_02_G
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/9O9pH_02_G:3'
  [Test::Selector] not ok 26 - t_list-subset2 Out okay.
  [Test::Selector] # Failed test 't_list-subset2 Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: 'b3
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 27 - t_list-subset2 Err okay.
  [Test::Selector] # Failed test 't_list-subset2 Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/f7fLREM_6P
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/f7fLREM_6P:3'
  [Test::Selector] not ok 28 - t_list-subset3 Out okay.
  [Test::Selector] # Failed test 't_list-subset3 Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: 'b3b
  [Test::Selector] # b5b
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 29 - t_list-subset3 Err okay.
  [Test::Selector] # Failed test 't_list-subset3 Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/Vpvm_V2AAj
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/Vpvm_V2AAj:3'
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
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/MWeIjsPUPv
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/MWeIjsPUPv:3'
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
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/15FO6jbqZb
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/15FO6jbqZb:3'
  [Test::Selector] not ok 34 - t_diff-sub-name3 Out okay.
  [Test::Selector] not ok 35 - t_diff-sub-name3 Err okay.
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
  [Test::Selector] # Failed test 't_diff-sub-name3 Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/KboyEfFhhy
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/KboyEfFhhy:3'
  [Test::Selector] not ok 36 - t_list-subset4 Out okay.
  [Test::Selector] not ok 37 - t_list-subset4 Err okay.
  [Test::Selector] # Failed test 't_list-subset4 Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: 'a1
  [Test::Selector] # __a2
  [Test::Selector] # _a3
  [Test::Selector] # a4
  [Test::Selector] # 1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] # Failed test 't_list-subset4 Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/GN_elGOgR9
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/GN_elGOgR9:3'
  [Test::Selector] not ok 38 - t_run-subset Out okay.
  [Test::Selector] # Failed test 't_run-subset Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '   # a1
  [Test::Selector] #    # _a3 : skipped
  [Test::Selector] #    # a4
  [Test::Selector] # ok 1 - Four
  [Test::Selector] # 1..1'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 39 - t_run-subset Err okay.
  [Test::Selector] # Failed test 't_run-subset Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: ''
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/RRVrc4zqcr
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/RRVrc4zqcr:3'
  [Test::Selector] not ok 40 - t_bad_action Out okay.
  [Test::Selector] # Failed test 't_bad_action Out okay.'
  [Test::Selector] # at t/all.rakutest line 74
  [Test::Selector] # expected: '1..0'
  [Test::Selector] #      got: ''
  [Test::Selector] not ok 41 - t_bad_action Err okay.
  [Test::Selector] # Failed test 't_bad_action Err okay.'
  [Test::Selector] # at t/all.rakutest line 75
  [Test::Selector] # expected: 'Moo'
  [Test::Selector] #      got: '===SORRY!=== Error while compiling /tmp/VVudPoTzXq
  [Test::Selector] # ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector)
  [Test::Selector] # No unspace allowed in regex; if you meant to match the literal
  [Test::Selector] # character, please enclose in single quotes (' ') or use a backslashed
  [Test::Selector] # form like \x20.
  [Test::Selector] # at /home/coke/sandbox/blin/data/zef-data/tmp/6d1ca6b4c6990bb293ba310faaca1e4400a6674b.tar.gz/lib/Test/Selector.rakumod (Test::Selector):614
  [Test::Selector] # ------>                     / ^ \s* ok \ <HERE>/ ||
  [Test::Selector] # 
  [Test::Selector] # at /tmp/VVudPoTzXq:3'
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
                 Service runtime: 3min 14.309s
               CPU time consumed: 3min 22.483s
                     Memory peak: 1.5G (swap: 128M)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| UnhandledException        |     1 | [Foo:: Foo](https://raku.land/github:AlexDaniel/Foo:: Foo) |
| InstallableButUntested    |     9 | [HTTP::Server::Async](https://raku.land/zef:raku-community-modules/HTTP::Server::Async) [IO::Socket::Async::SSL](https://raku.land/zef:raku-community-modules/IO::Socket::Async::SSL) [IRC::Client](https://raku.land/zef:lizmat/IRC::Client) [Log::Minimal](https://raku.land//Log::Minimal) [Russian](https://raku.land/zef:slavenskoj/Russian) [Time::Duration](https://raku.land/zef:masukomi/Time::Duration) [Toaster](https://raku.land//Toaster) [Uzu](https://raku.land/cpan:SACOMO/Uzu) [Web::Scraper](https://raku.land/zef:tony-o/Web::Scraper) |
| Fail                      |     9 | [AI::NLP](https://raku.land/cpan:KOBOLDWIZ/AI::NLP) [Acme::Cow](https://raku.land//Acme::Cow) [Cro::WebSocket](https://raku.land/zef:cro/Cro::WebSocket) [Debugging::Tool](https://raku.land/zef:lucs/Debugging::Tool) [File::TreeBuilder](https://raku.land/zef:lucs/File::TreeBuilder) [MIDI::Make](https://raku.land/zef:pelevesque/MIDI::Make) [Net::BGP](https://raku.land/zef:jmaslak/Net::BGP) [Test::Selector](https://raku.land/zef:lucs/Test::Selector) [Text::Markdown::Discount](https://raku.land/github:hartenfels/Text::Markdown::Discount) |
| ZefFailure                |    11 | [BDD::Behave](https://raku.land/zef:gdonald/BDD::Behave) [Cro::ZeroMQ](https://raku.land/cpan:JNTHN/Cro::ZeroMQ) [Gnome::Gtk4](https://raku.land/zef:martimm/Gnome::Gtk4) [JSON::Stream](https://raku.land//JSON::Stream) [ParaSeq](https://raku.land/zef:lizmat/ParaSeq) [Proc::ZMQed](https://raku.land/zef:antononcube/Proc::ZMQed) [TXN](https://raku.land//TXN) [TXN::Parser](https://raku.land//TXN::Parser) [TXN::Remarshal](https://raku.land//TXN::Remarshal) [Test::Time](https://raku.land/zef:FCO/Test::Time) [cro](https://raku.land/zef:cro/cro) |
| MissingDependency         |    11 | [App::Ebread](https://raku.land/zef:samy/App::Ebread) [App::Perl6LangServer](https://raku.land/cpan:AZAWAWI/App::Perl6LangServer) [Chemistry::Elements](https://raku.land/github:briandfoy/Chemistry::Elements) [DBIx::NamedQueries](https://raku.land/cpan:MZIESCHA/DBIx::NamedQueries) [Ethelia](https://raku.land/zef:knarkhov/Ethelia) [Learn::Raku::With](https://raku.land/zef:codesections/Learn::Raku::With) [META6::To::Man](https://raku.land/cpan:TBROWDER/META6::To::Man) [Pakku](https://raku.land/zef:hythm/Pakku) [Perl6::Tracer](https://raku.land/github:jaffa4/Perl6::Tracer) [Task::Galaxy](https://raku.land//Task::Galaxy) [Touch](https://raku.land/zef:rir/Touch) |
| CyclicDependency          |    46 | ⋯                         |
| AlwaysFail                |   727 | ⋯                         |
| OK                        |  1695 | ⋯                         |



This run started on 2026-08-19T19:30:39Z and finished in ≈4 hours.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
