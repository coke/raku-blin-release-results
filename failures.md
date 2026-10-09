[Blin](https://github.com/Raku/Blin) results between 2026.09 ([9a94801](https://github.com/rakudo/rakudo/commit/9a94801c154543573d926e6258e062f3c3782635)) and 6a3feeac14 ([6a3feea](https://github.com/rakudo/rakudo/commit/6a3feeac1482cb1d2b41634e3e06a69e4c806c49)):

* [ ] [Intl::CLDR](https://raku.land/zef:guifa/Intl::CLDR) – Fail, Bisected: [74b7282](https://github.com/rakudo/rakudo/commit/74b7282e15d984563c3c8ba082d64a6aa01fd198)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2762419-i15405426.service; invocation ID: b45c3f5ad6e54e60972eb5d4308319e5
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Intl::CLDR
  ===> Found: Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1> [via Zef::Repository::Ecosystems<fez>]
  [Intl::CLDR] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1791561051.2762420.8054.89998974179/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz https://360.zef.pm/I/NT/INTL_CLDR/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz
  ===> Fetching [OK]: Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1> to /home/coke/sandbox/blin/data/zef-data/tmp/1791561051.2762420.8054.89998974179/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz
  [Intl::CLDR] Command: tar -t -f ./c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz
  [Intl::CLDR] Command: tar -xvf ./c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz -C ../c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz
  ===> Extraction [OK]: Intl::CLDR to /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz
  ===> Testing: Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1>
  [Intl::CLDR] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist t/00-sanity.rakutest
  [Intl::CLDR] Potential difficulties:
  [Intl::CLDR]     Missing declarand for trailing declarator doc
  [Intl::CLDR]     at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/MonthPatternWidth.rakumod (Intl::CLDR::Types::MonthPatternWidth):8
  [Intl::CLDR]     ------> p>; #= The 'standardAfterLeap' from CLDR<HERE><EOL>
  [Intl::CLDR] Potential difficulties:
  [Intl::CLDR]     Missing declarand for trailing declarator doc
  [Intl::CLDR]     at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Dates.rakumod (Intl::CLDR::Types::Dates):15
  [Intl::CLDR]     ------> he timezone data for the date collection<HERE><EOL>
  [Intl::CLDR] Potential difficulties:
  [Intl::CLDR]     Missing declarand for trailing declarator doc
  [Intl::CLDR]     at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SymbolSet.rakumod (Intl::CLDR::Types::SymbolSet):13
  [Intl::CLDR]     ------> -scientific (e.g. superscript) exponents<HERE><EOL>
  [Intl::CLDR] ok 1 - 
  [Intl::CLDR] 1..1
  [Intl::CLDR] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist t/01-spot-check.rakutest
  [Intl::CLDR] # Subtest: Characters
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     1..2
  [Intl::CLDR] ok 1 - Characters
  [Intl::CLDR] # Subtest: Context transforms
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     ok 3 - 
  [Intl::CLDR]     1..3
  [Intl::CLDR] ok 2 - Context transforms
  [Intl::CLDR] # Subtest: Dates
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     ok 3 - 
  [Intl::CLDR]     ok 4 - 
  [Intl::CLDR]     ok 5 - 
  [Intl::CLDR]     ok 6 - 
  [Intl::CLDR]     ok 7 - 
  [Intl::CLDR]     ok 8 - 
  [Intl::CLDR]     ok 9 - 
  [Intl::CLDR]     ok 10 - 
  [Intl::CLDR]     ok 11 - 
  [Intl::CLDR]     ok 12 - 
  [Intl::CLDR]     ok 13 - 
  [Intl::CLDR]     ok 14 - 
  [Intl::CLDR]     ok 15 - 
  [Intl::CLDR]     ok 16 - 
  [Intl::CLDR]     ok 17 - 
  [Intl::CLDR]     1..17
  [Intl::CLDR] ok 3 - Dates
  [Intl::CLDR] # Subtest: Delimiters
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     1..2
  [Intl::CLDR] ok 4 - Delimiters
  [Intl::CLDR] # Subtest: Grammar
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     ok 3 - 
  [Intl::CLDR]     ok 4 - 
  [Intl::CLDR]     ok 5 - 
  [Intl::CLDR]     1..5
  [Intl::CLDR] ok 5 - Grammar
  [Intl::CLDR] # Subtest: Layout
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     1..2
  [Intl::CLDR] ok 6 - Layout
  [Intl::CLDR] # Subtest: List patterns
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     ok 3 - 
  [Intl::CLDR]     1..3
  [Intl::CLDR] ok 7 - List patterns
  [Intl::CLDR] # Subtest: Locale display names
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     ok 3 - 
  [Intl::CLDR]     ok 4 - 
  [Intl::CLDR]     ok 5 - 
  [Intl::CLDR]     ok 6 - 
  [Intl::CLDR]     1..6
  [Intl::CLDR] ok 8 - Locale display names
  [Intl::CLDR] # Subtest: Numbers
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     ok 3 - 
  [Intl::CLDR]     ok 4 - 
  [Intl::CLDR]     ok 5 - 
  [Intl::CLDR]     ok 6 - 
  [Intl::CLDR]     ok 7 - 
  [Intl::CLDR]     ok 8 - 
  [Intl::CLDR]     ok 9 - 
  [Intl::CLDR]     ok 10 - 
  [Intl::CLDR]     1..10
  [Intl::CLDR] ok 9 - Numbers
  [Intl::CLDR] # Subtest: POSIX
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     1..2
  [Intl::CLDR] ok 10 - POSIX
  [Intl::CLDR] # Subtest: Units
  [Intl::CLDR]     ok 1 - 
  [Intl::CLDR]     ok 2 - 
  [Intl::CLDR]     ok 3 - 
  [Intl::CLDR]     ok 4 - 
  [Intl::CLDR]     1..4
  [Intl::CLDR] ok 11 - Units
  [Intl::CLDR] 1..11
  [Intl::CLDR] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist t/99-load-time-test.rakutest
  [Intl::CLDR] 1..0
  ===> Testing [OK] for Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1>
  ===> Installing: Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /tmp/5JIgRjCPA4/sources/F0936CD30D560BBC40876E240F88BB712D8BF4D3 (Intl::CLDR::Types::MonthPatternWidth):8
      ------> p>; #= The 'standardAfterLeap' from CLDR<HERE><EOL>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /tmp/5JIgRjCPA4/sources/73695ACE1F4120D98623C4EFFC45D81D97053054 (Intl::CLDR::Types::Dates):15
      ------> he timezone data for the date collection<HERE><EOL>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /tmp/5JIgRjCPA4/sources/6ED7C380C0F85D5EAC6021572DDA3E7DF5C42E52 (Intl::CLDR::Types::SymbolSet):13
      ------> -scientific (e.g. superscript) exponents<HERE><EOL>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::LanguageTag_zef:guifa_0.12.7_0/sources/02BCD182A9AF97E6BA19D1AEEC5654DFC6960B7D (Intl::LanguageTag::BCP47):665
      ------> s to use as a filter (generally shorter)<HERE><EOL>
  ===> Install [OK] for Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 58.134s
               CPU time consumed: 2min 52.359s
                     Memory peak: 4G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2760020-i15353188.service; invocation ID: dc22c24b78794a5da494a926ff935499
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Intl::CLDR
  ===> Found: Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1> [via Zef::Repository::Ecosystems<fez>]
  [Intl::CLDR] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1791560934.2760021.3762.2530073912285/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz https://360.zef.pm/I/NT/INTL_CLDR/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz
  ===> Fetching [OK]: Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1> to /home/coke/sandbox/blin/data/zef-data/tmp/1791560934.2760021.3762.2530073912285/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz
  [Intl::CLDR] Command: tar -t -f ./c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz
  [Intl::CLDR] Command: tar -xvf ./c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz -C ../c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz
  ===> Extraction [OK]: Intl::CLDR to /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz
  ===> Testing: Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1>
  [Intl::CLDR] Command: /tmp/whateverable/rakudo-moar/6a3feeac1482cb1d2b41634e3e06a69e4c806c49/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist t/00-sanity.rakutest
  [Intl::CLDR] ===SORRY!=== Error while compiling t/00-sanity.rakutest
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR.rakumod (Intl::CLDR)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Database.rakumod (Intl::CLDR::Types::Database)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Languages.rakumod (Intl::CLDR::Types::Languages)
  [Intl::CLDR] Potential difficulties:
  [Intl::CLDR]     Missing declarand for trailing declarator doc
  [Intl::CLDR]     at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/MonthPatternWidth.rakumod (Intl::CLDR::Types::MonthPatternWidth):8
  [Intl::CLDR]     ------> p>; #= The 'standardAfterLeap' from CLDR<HERE><EOL>
  [Intl::CLDR] Potential difficulties:
  [Intl::CLDR]     Missing declarand for trailing declarator doc
  [Intl::CLDR]     at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Dates.rakumod (Intl::CLDR::Types::Dates):15
  [Intl::CLDR]     ------> he timezone data for the date collection<HERE><EOL>
  [Intl::CLDR] Potential difficulties:
  [Intl::CLDR]     Missing declarand for trailing declarator doc
  [Intl::CLDR]     at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SymbolSet.rakumod (Intl::CLDR::Types::SymbolSet):13
  [Intl::CLDR]     ------> -scientific (e.g. superscript) exponents<HERE><EOL>
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Language.rakumod (Intl::CLDR::Types::Language)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Units.rakumod (Intl::CLDR::Types::Units)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnits.rakumod (Intl::CLDR::Types::SimpleUnits)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnitSet.rakumod (Intl::CLDR::Types::SimpleUnitSet)
  [Intl::CLDR] This type cannot unbox to a native string: P6opaque, Int
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnitSet.rakumod (Intl::CLDR::Types::SimpleUnitSet):4
  [Intl::CLDR] ------>     <HERE>use Intl::CLDR::Enums;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnits.rakumod (Intl::CLDR::Types::SimpleUnits):8
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnitSet;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Units.rakumod (Intl::CLDR::Types::Units):6
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnits;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Language.rakumod (Intl::CLDR::Types::Language):15
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::Units;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Languages.rakumod (Intl::CLDR::Types::Languages):4
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::Language;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Database.rakumod (Intl::CLDR::Types::Database):3
  [Intl::CLDR] ------>     <HERE>use Intl::CLDR::Types::Languages;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR.rakumod (Intl::CLDR):31
  [Intl::CLDR] ------>     <HERE>use Intl::CLDR::Types::Database;
  [Intl::CLDR] at t/00-sanity.rakutest:2
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR:auth<zef:guifa>;
  [Intl::CLDR] Command: /tmp/whateverable/rakudo-moar/6a3feeac1482cb1d2b41634e3e06a69e4c806c49/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist t/01-spot-check.rakutest
  [Intl::CLDR] ===SORRY!=== Error while compiling t/01-spot-check.rakutest
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR.rakumod (Intl::CLDR)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Database.rakumod (Intl::CLDR::Types::Database)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Languages.rakumod (Intl::CLDR::Types::Languages)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Language.rakumod (Intl::CLDR::Types::Language)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Units.rakumod (Intl::CLDR::Types::Units)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnits.rakumod (Intl::CLDR::Types::SimpleUnits)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnitSet.rakumod (Intl::CLDR::Types::SimpleUnitSet)
  [Intl::CLDR] This type cannot unbox to a native string: P6opaque, Int
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnitSet.rakumod (Intl::CLDR::Types::SimpleUnitSet):4
  [Intl::CLDR] ------>     <HERE>use Intl::CLDR::Enums;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnits.rakumod (Intl::CLDR::Types::SimpleUnits):8
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnitSet;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Units.rakumod (Intl::CLDR::Types::Units):6
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnits;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Language.rakumod (Intl::CLDR::Types::Language):15
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::Units;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Languages.rakumod (Intl::CLDR::Types::Languages):4
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::Language;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Database.rakumod (Intl::CLDR::Types::Database):3
  [Intl::CLDR] ------>     <HERE>use Intl::CLDR::Types::Languages;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR.rakumod (Intl::CLDR):31
  [Intl::CLDR] ------>     <HERE>use Intl::CLDR::Types::Database;
  [Intl::CLDR] at t/01-spot-check.rakutest:16
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR:auth<zef:guifa>;
  [Intl::CLDR] Command: /tmp/whateverable/rakudo-moar/6a3feeac1482cb1d2b41634e3e06a69e4c806c49/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist t/99-load-time-test.rakutest
  [Intl::CLDR] ===SORRY!=== Error while compiling t/99-load-time-test.rakutest
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR.rakumod (Intl::CLDR)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Database.rakumod (Intl::CLDR::Types::Database)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Languages.rakumod (Intl::CLDR::Types::Languages)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Language.rakumod (Intl::CLDR::Types::Language)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Units.rakumod (Intl::CLDR::Types::Units)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnits.rakumod (Intl::CLDR::Types::SimpleUnits)
  [Intl::CLDR] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnitSet.rakumod (Intl::CLDR::Types::SimpleUnitSet)
  [Intl::CLDR] This type cannot unbox to a native string: P6opaque, Int
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnitSet.rakumod (Intl::CLDR::Types::SimpleUnitSet):4
  [Intl::CLDR] ------>     <HERE>use Intl::CLDR::Enums;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/SimpleUnits.rakumod (Intl::CLDR::Types::SimpleUnits):8
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnitSet;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Units.rakumod (Intl::CLDR::Types::Units):6
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnits;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Language.rakumod (Intl::CLDR::Types::Language):15
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::Units;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Languages.rakumod (Intl::CLDR::Types::Languages):4
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR::Types::Language;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR/Types/Database.rakumod (Intl::CLDR::Types::Database):3
  [Intl::CLDR] ------>     <HERE>use Intl::CLDR::Types::Languages;
  [Intl::CLDR] at /home/coke/sandbox/blin/data/zef-data/tmp/c355ab0803985ce7b3d01ecc3a525c13eb26f881.tar.gz/dist/lib/Intl/CLDR.rakumod (Intl::CLDR):31
  [Intl::CLDR] ------>     <HERE>use Intl::CLDR::Types::Database;
  [Intl::CLDR] at t/99-load-time-test.rakutest:1
  [Intl::CLDR] ------> <BOL><HERE>use Intl::CLDR:auth<zef:guifa>;
  ===> Testing [FAIL]: Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1>
  [Intl::CLDR] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1>
  ===> Install [FAIL] for Intl::CLDR:ver<0.7.6>:auth<zef:guifa>:api<1>: ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/2D64AB7F840DBC1187A48A651516D851331602DA (Intl::CLDR)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/983C26B86287DA3FF695AA2FBF5F0DD2D70F4DC6 (Intl::CLDR::Types::Database)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/202601A191D2EB4FD96D1F154320EEB3E311A9C4 (Intl::CLDR::Types::Languages)
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/F0936CD30D560BBC40876E240F88BB712D8BF4D3 (Intl::CLDR::Types::MonthPatternWidth):8
      ------> p>; #= The 'standardAfterLeap' from CLDR<HERE><EOL>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/73695ACE1F4120D98623C4EFFC45D81D97053054 (Intl::CLDR::Types::Dates):15
      ------> he timezone data for the date collection<HERE><EOL>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/6ED7C380C0F85D5EAC6021572DDA3E7DF5C42E52 (Intl::CLDR::Types::SymbolSet):13
      ------> -scientific (e.g. superscript) exponents<HERE><EOL>
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/7B5ABC9367F8DD6813475C416AB192F71A78B276 (Intl::CLDR::Types::Language)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/276219BCFD79C8B10BB4F20F7A14A5F56CA4B355 (Intl::CLDR::Types::Units)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/716C26AB03A4E6BA0D2FCB27543389D42730167C (Intl::CLDR::Types::SimpleUnits)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/191C8E803D779AFE6049DD4B613FB10C004EC0AA (Intl::CLDR::Types::SimpleUnitSet)
  This type cannot unbox to a native string: P6opaque, Int
  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/191C8E803D779AFE6049DD4B613FB10C004EC0AA (Intl::CLDR::Types::SimpleUnitSet):4
  ------>     <HERE>use Intl::CLDR::Enums;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/716C26AB03A4E6BA0D2FCB27543389D42730167C (Intl::CLDR::Types::SimpleUnits):8
  ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnitSet;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/276219BCFD79C8B10BB4F20F7A14A5F56CA4B355 (Intl::CLDR::Types::Units):6
  ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnits;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/7B5ABC9367F8DD6813475C416AB192F71A78B276 (Intl::CLDR::Types::Language):15
  ------> <BOL><HERE>use Intl::CLDR::Types::Units;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/202601A191D2EB4FD96D1F154320EEB3E311A9C4 (Intl::CLDR::Types::Languages):4
  ------> <BOL><HERE>use Intl::CLDR::Types::Language;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/983C26B86287DA3FF695AA2FBF5F0DD2D70F4DC6 (Intl::CLDR::Types::Database):3
  ------>     <HERE>use Intl::CLDR::Types::Languages;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/2D64AB7F840DBC1187A48A651516D851331602DA (Intl::CLDR):31
  ------>     <HERE>use Intl::CLDR::Types::Database;

  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/2D64AB7F840DBC1187A48A651516D851331602DA (Intl::CLDR)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/983C26B86287DA3FF695AA2FBF5F0DD2D70F4DC6 (Intl::CLDR::Types::Database)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/202601A191D2EB4FD96D1F154320EEB3E311A9C4 (Intl::CLDR::Types::Languages)
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/F0936CD30D560BBC40876E240F88BB712D8BF4D3 (Intl::CLDR::Types::MonthPatternWidth):8
      ------> p>; #= The 'standardAfterLeap' from CLDR<HERE><EOL>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/73695ACE1F4120D98623C4EFFC45D81D97053054 (Intl::CLDR::Types::Dates):15
      ------> he timezone data for the date collection<HERE><EOL>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/6ED7C380C0F85D5EAC6021572DDA3E7DF5C42E52 (Intl::CLDR::Types::SymbolSet):13
      ------> -scientific (e.g. superscript) exponents<HERE><EOL>
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/7B5ABC9367F8DD6813475C416AB192F71A78B276 (Intl::CLDR::Types::Language)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/276219BCFD79C8B10BB4F20F7A14A5F56CA4B355 (Intl::CLDR::Types::Units)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/716C26AB03A4E6BA0D2FCB27543389D42730167C (Intl::CLDR::Types::SimpleUnits)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/191C8E803D779AFE6049DD4B613FB10C004EC0AA (Intl::CLDR::Types::SimpleUnitSet)
  This type cannot unbox to a native string: P6opaque, Int
  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/191C8E803D779AFE6049DD4B613FB10C004EC0AA (Intl::CLDR::Types::SimpleUnitSet):4
  ------>     <HERE>use Intl::CLDR::Enums;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/716C26AB03A4E6BA0D2FCB27543389D42730167C (Intl::CLDR::Types::SimpleUnits):8
  ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnitSet;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/276219BCFD79C8B10BB4F20F7A14A5F56CA4B355 (Intl::CLDR::Types::Units):6
  ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnits;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/7B5ABC9367F8DD6813475C416AB192F71A78B276 (Intl::CLDR::Types::Language):15
  ------> <BOL><HERE>use Intl::CLDR::Types::Units;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/202601A191D2EB4FD96D1F154320EEB3E311A9C4 (Intl::CLDR::Types::Languages):4
  ------> <BOL><HERE>use Intl::CLDR::Types::Language;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/983C26B86287DA3FF695AA2FBF5F0DD2D70F4DC6 (Intl::CLDR::Types::Database):3
  ------>     <HERE>use Intl::CLDR::Types::Languages;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/2D64AB7F840DBC1187A48A651516D851331602DA (Intl::CLDR):31
  ------>     <HERE>use Intl::CLDR::Types::Database;

            Finished with result: exit-code
  Main processes terminated with: code=exited, status=1/FAILURE
                 Service runtime: 1min 40.918s
               CPU time consumed: 2min 22.971s
                     Memory peak: 4.3G (swap: 0B)

  ```
  </details>
* [ ] [Intl::Number::Plural](https://raku.land/github:alabamenhu/Intl::Number::Plural) – Fail, Bisected: [74b7282](https://github.com/rakudo/rakudo/commit/74b7282e15d984563c3c8ba082d64a6aa01fd198)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2780114-i15410248.service; invocation ID: 7c37b6b4ad644d029c47b7b7070b37ea
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Intl::Number::Plural
  ===> Found: Intl::Number::Plural:ver<0.5.4>:auth<github:alabamenhu> [via Zef::Repository::Ecosystems<rea>]
  [Intl::Number::Plural] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1791562086.2780115.4900.43100256619/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/I/Intl%3A%3ANumber%3A%3APlural/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Fetching [OK]: Intl::Number::Plural:ver<0.5.4>:auth<github:alabamenhu> to /home/coke/sandbox/blin/data/zef-data/tmp/1791562086.2780115.4900.43100256619/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  [Intl::Number::Plural] Command: tar -t -f ./Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  [Intl::Number::Plural] Command: tar -xvf ./Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz -C ../Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Extraction [OK]: Intl::Number::Plural to /home/coke/sandbox/blin/data/zef-data/tmp/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Testing: Intl::Number::Plural:ver<0.5.4>:auth<git:alabamenhu>
  [Intl::Number::Plural] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz/IntlNumberPlural-main t/00-sanity.t
  [Intl::Number::Plural] Potential difficulties:
  [Intl::Number::Plural]     Missing declarand for trailing declarator doc
  [Intl::Number::Plural]     at /home/coke/sandbox/blin/installed/Intl::LanguageTag_zef:guifa_0.12.7_0/sources/02BCD182A9AF97E6BA19D1AEEC5654DFC6960B7D (Intl::LanguageTag::BCP47):665
  [Intl::Number::Plural]     ------> s to use as a filter (generally shorter)<HERE><EOL>
  [Intl::Number::Plural] ⎡ The module Intl::UserLanguage has been renamed to User::Language. ⎤
  [Intl::Number::Plural] ⎢ Please use this name in the future. If you received this message  ⎥
  [Intl::Number::Plural] ⎢ without having explicitly used the module, please contact the     ⎥
  [Intl::Number::Plural] ⎢ author whose module called this to have them update accordingly.  ⎥
  [Intl::Number::Plural] ⎢                                                                   ⎥
  [Intl::Number::Plural] ⎢ Please be aware that fallback languages are not supported when    ⎥
  [Intl::Number::Plural] ⎢ calling by the old name for compile time reasons                  ⎥
  [Intl::Number::Plural] ⎢                                                                   ⎥
  [Intl::Number::Plural] ⎢ You may dismiss this by setting the environment variable          ⎥
  [Intl::Number::Plural] ⎢ RAKU_USER_LANGUAGE_NAMECHANGE_WARNING to OFF. Updates after 2024  ⎥
  [Intl::Number::Plural] ⎣ will no longer provide under the old name.                        ⎦
  [Intl::Number::Plural] Potential difficulties:
  [Intl::Number::Plural]     Missing declarand for trailing declarator doc
  [Intl::Number::Plural]     at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/F0936CD30D560BBC40876E240F88BB712D8BF4D3 (Intl::CLDR::Types::MonthPatternWidth):8
  [Intl::Number::Plural]     ------> p>; #= The 'standardAfterLeap' from CLDR<HERE><EOL>
  [Intl::Number::Plural] Potential difficulties:
  [Intl::Number::Plural]     Missing declarand for trailing declarator doc
  [Intl::Number::Plural]     at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/73695ACE1F4120D98623C4EFFC45D81D97053054 (Intl::CLDR::Types::Dates):15
  [Intl::Number::Plural]     ------> he timezone data for the date collection<HERE><EOL>
  [Intl::Number::Plural] Potential difficulties:
  [Intl::Number::Plural]     Missing declarand for trailing declarator doc
  [Intl::Number::Plural]     at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/6ED7C380C0F85D5EAC6021572DDA3E7DF5C42E52 (Intl::CLDR::Types::SymbolSet):13
  [Intl::Number::Plural]     ------> -scientific (e.g. superscript) exponents<HERE><EOL>
  [Intl::Number::Plural] 1..0
  ===> Testing [OK] for Intl::Number::Plural:ver<0.5.4>:auth<git:alabamenhu>
  ===> Installing: Intl::Number::Plural:ver<0.5.4>:auth<git:alabamenhu>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::LanguageTag_zef:guifa_0.12.7_0/sources/02BCD182A9AF97E6BA19D1AEEC5654DFC6960B7D (Intl::LanguageTag::BCP47):665
      ------> s to use as a filter (generally shorter)<HERE><EOL>
  ⎡ The module Intl::UserLanguage has been renamed to User::Language. ⎤
  ⎢ Please use this name in the future. If you received this message  ⎥
  ⎢ without having explicitly used the module, please contact the     ⎥
  ⎢ author whose module called this to have them update accordingly.  ⎥
  ⎢                                                                   ⎥
  ⎢ Please be aware that fallback languages are not supported when    ⎥
  ⎢ calling by the old name for compile time reasons                  ⎥
  ⎢                                                                   ⎥
  ⎢ You may dismiss this by setting the environment variable          ⎥
  ⎢ RAKU_USER_LANGUAGE_NAMECHANGE_WARNING to OFF. Updates after 2024  ⎥
  ⎣ will no longer provide under the old name.                        ⎦
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/F0936CD30D560BBC40876E240F88BB712D8BF4D3 (Intl::CLDR::Types::MonthPatternWidth):8
      ------> p>; #= The 'standardAfterLeap' from CLDR<HERE><EOL>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/73695ACE1F4120D98623C4EFFC45D81D97053054 (Intl::CLDR::Types::Dates):15
      ------> he timezone data for the date collection<HERE><EOL>
  Potential difficulties:
      Missing declarand for trailing declarator doc
      at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/6ED7C380C0F85D5EAC6021572DDA3E7DF5C42E52 (Intl::CLDR::Types::SymbolSet):13
      ------> -scientific (e.g. superscript) exponents<HERE><EOL>
  ===> Install [OK] for Intl::Number::Plural:ver<0.5.4>:auth<git:alabamenhu>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 30.950s
               CPU time consumed: 2min 13.322s
                     Memory peak: 3.5G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2779945-i15422012.service; invocation ID: b68c6ceddf324a8c82053e92c323423b
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Intl::Number::Plural
  ===> Found: Intl::Number::Plural:ver<0.5.4>:auth<github:alabamenhu> [via Zef::Repository::Ecosystems<rea>]
  [Intl::Number::Plural] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1791562062.2779946.4048.9450169429974/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/I/Intl%3A%3ANumber%3A%3APlural/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Fetching [OK]: Intl::Number::Plural:ver<0.5.4>:auth<github:alabamenhu> to /home/coke/sandbox/blin/data/zef-data/tmp/1791562062.2779946.4048.9450169429974/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  [Intl::Number::Plural] Command: tar -t -f ./Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  [Intl::Number::Plural] Command: tar -xvf ./Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz -C ../Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Extraction [OK]: Intl::Number::Plural to /home/coke/sandbox/blin/data/zef-data/tmp/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz
  ===> Testing: Intl::Number::Plural:ver<0.5.4>:auth<git:alabamenhu>
  [Intl::Number::Plural] Command: /tmp/whateverable/rakudo-moar/6a3feeac1482cb1d2b41634e3e06a69e4c806c49/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz/IntlNumberPlural-main t/00-sanity.t
  [Intl::Number::Plural] ===SORRY!=== Error while compiling t/00-sanity.t
  [Intl::Number::Plural] ⎡ The module Intl::UserLanguage has been renamed to User::Language. ⎤
  [Intl::Number::Plural] ⎢ Please use this name in the future. If you received this message  ⎥
  [Intl::Number::Plural] ⎢ without having explicitly used the module, please contact the     ⎥
  [Intl::Number::Plural] ⎢ author whose module called this to have them update accordingly.  ⎥
  [Intl::Number::Plural] ⎢                                                                   ⎥
  [Intl::Number::Plural] ⎢ Please be aware that fallback languages are not supported when    ⎥
  [Intl::Number::Plural] ⎢ calling by the old name for compile time reasons                  ⎥
  [Intl::Number::Plural] ⎢                                                                   ⎥
  [Intl::Number::Plural] ⎢ You may dismiss this by setting the environment variable          ⎥
  [Intl::Number::Plural] ⎢ RAKU_USER_LANGUAGE_NAMECHANGE_WARNING to OFF. Updates after 2024  ⎥
  [Intl::Number::Plural] ⎣ will no longer provide under the old name.                        ⎦
  [Intl::Number::Plural] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz/IntlNumberPlural-main/lib/Intl/Number/Plural.pm6 (Intl::Number::Plural)
  [Intl::Number::Plural] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/2D64AB7F840DBC1187A48A651516D851331602DA (Intl::CLDR)
  [Intl::Number::Plural] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/983C26B86287DA3FF695AA2FBF5F0DD2D70F4DC6 (Intl::CLDR::Types::Database)
  [Intl::Number::Plural] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/202601A191D2EB4FD96D1F154320EEB3E311A9C4 (Intl::CLDR::Types::Languages)
  [Intl::Number::Plural] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/7B5ABC9367F8DD6813475C416AB192F71A78B276 (Intl::CLDR::Types::Language)
  [Intl::Number::Plural] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/276219BCFD79C8B10BB4F20F7A14A5F56CA4B355 (Intl::CLDR::Types::Units)
  [Intl::Number::Plural] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/716C26AB03A4E6BA0D2FCB27543389D42730167C (Intl::CLDR::Types::SimpleUnits)
  [Intl::Number::Plural] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/191C8E803D779AFE6049DD4B613FB10C004EC0AA (Intl::CLDR::Types::SimpleUnitSet)
  [Intl::Number::Plural] This type cannot unbox to a native string: P6opaque, Int
  [Intl::Number::Plural] at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/191C8E803D779AFE6049DD4B613FB10C004EC0AA (Intl::CLDR::Types::SimpleUnitSet):4
  [Intl::Number::Plural] ------>     <HERE>use Intl::CLDR::Enums;
  [Intl::Number::Plural] at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/716C26AB03A4E6BA0D2FCB27543389D42730167C (Intl::CLDR::Types::SimpleUnits):8
  [Intl::Number::Plural] ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnitSet;
  [Intl::Number::Plural] at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/276219BCFD79C8B10BB4F20F7A14A5F56CA4B355 (Intl::CLDR::Types::Units):6
  [Intl::Number::Plural] ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnits;
  [Intl::Number::Plural] at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/7B5ABC9367F8DD6813475C416AB192F71A78B276 (Intl::CLDR::Types::Language):15
  [Intl::Number::Plural] ------> <BOL><HERE>use Intl::CLDR::Types::Units;
  [Intl::Number::Plural] at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/202601A191D2EB4FD96D1F154320EEB3E311A9C4 (Intl::CLDR::Types::Languages):4
  [Intl::Number::Plural] ------> <BOL><HERE>use Intl::CLDR::Types::Language;
  [Intl::Number::Plural] at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/983C26B86287DA3FF695AA2FBF5F0DD2D70F4DC6 (Intl::CLDR::Types::Database):3
  [Intl::Number::Plural] ------>     <HERE>use Intl::CLDR::Types::Languages;
  [Intl::Number::Plural] at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/2D64AB7F840DBC1187A48A651516D851331602DA (Intl::CLDR):31
  [Intl::Number::Plural] ------>     <HERE>use Intl::CLDR::Types::Database;
  [Intl::Number::Plural] at /home/coke/sandbox/blin/data/zef-data/tmp/Intl%3A%3ANumber%3A%3APlural%3Aver%3C0.5.4%3E%3Aauth%3Cgithub%3Aalabamenhu%3E.tar.gz/IntlNumberPlural-main/lib/Intl/Number/Plural.pm6 (Intl::Number::Plural):4
  [Intl::Number::Plural] ------> <BOL><HERE>use Intl::CLDR;
  [Intl::Number::Plural] at t/00-sanity.t:1
  [Intl::Number::Plural] ------> <BOL><HERE>use Intl::Number::Plural;
  ===> Testing [FAIL]: Intl::Number::Plural:ver<0.5.4>:auth<git:alabamenhu>
  [Intl::Number::Plural] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Intl::Number::Plural:ver<0.5.4>:auth<git:alabamenhu>
  ===> Install [FAIL] for Intl::Number::Plural:ver<0.5.4>:auth<git:alabamenhu>: ⎡ The module Intl::UserLanguage has been renamed to User::Language. ⎤
  ⎢ Please use this name in the future. If you received this message  ⎥
  ⎢ without having explicitly used the module, please contact the     ⎥
  ⎢ author whose module called this to have them update accordingly.  ⎥
  ⎢                                                                   ⎥
  ⎢ Please be aware that fallback languages are not supported when    ⎥
  ⎢ calling by the old name for compile time reasons                  ⎥
  ⎢                                                                   ⎥
  ⎢ You may dismiss this by setting the environment variable          ⎥
  ⎢ RAKU_USER_LANGUAGE_NAMECHANGE_WARNING to OFF. Updates after 2024  ⎥
  ⎣ will no longer provide under the old name.                        ⎦
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::Number::Plural_github:alabamenhu_0.5.4_0/sources/9F5F1EE9CB750282977EDC77049DC45738CEBB55 (Intl::Number::Plural)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/2D64AB7F840DBC1187A48A651516D851331602DA (Intl::CLDR)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/983C26B86287DA3FF695AA2FBF5F0DD2D70F4DC6 (Intl::CLDR::Types::Database)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/202601A191D2EB4FD96D1F154320EEB3E311A9C4 (Intl::CLDR::Types::Languages)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/7B5ABC9367F8DD6813475C416AB192F71A78B276 (Intl::CLDR::Types::Language)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/276219BCFD79C8B10BB4F20F7A14A5F56CA4B355 (Intl::CLDR::Types::Units)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/716C26AB03A4E6BA0D2FCB27543389D42730167C (Intl::CLDR::Types::SimpleUnits)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/191C8E803D779AFE6049DD4B613FB10C004EC0AA (Intl::CLDR::Types::SimpleUnitSet)
  This type cannot unbox to a native string: P6opaque, Int
  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/191C8E803D779AFE6049DD4B613FB10C004EC0AA (Intl::CLDR::Types::SimpleUnitSet):4
  ------>     <HERE>use Intl::CLDR::Enums;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/716C26AB03A4E6BA0D2FCB27543389D42730167C (Intl::CLDR::Types::SimpleUnits):8
  ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnitSet;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/276219BCFD79C8B10BB4F20F7A14A5F56CA4B355 (Intl::CLDR::Types::Units):6
  ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnits;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/7B5ABC9367F8DD6813475C416AB192F71A78B276 (Intl::CLDR::Types::Language):15
  ------> <BOL><HERE>use Intl::CLDR::Types::Units;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/202601A191D2EB4FD96D1F154320EEB3E311A9C4 (Intl::CLDR::Types::Languages):4
  ------> <BOL><HERE>use Intl::CLDR::Types::Language;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/983C26B86287DA3FF695AA2FBF5F0DD2D70F4DC6 (Intl::CLDR::Types::Database):3
  ------>     <HERE>use Intl::CLDR::Types::Languages;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/2D64AB7F840DBC1187A48A651516D851331602DA (Intl::CLDR):31
  ------>     <HERE>use Intl::CLDR::Types::Database;

  at /home/coke/sandbox/blin/installed/Intl::Number::Plural_github:alabamenhu_0.5.4_0/sources/9F5F1EE9CB750282977EDC77049DC45738CEBB55 (Intl::Number::Plural):4
  ------> <BOL><HERE>use Intl::CLDR;

  ⎡ The module Intl::UserLanguage has been renamed to User::Language. ⎤
  ⎢ Please use this name in the future. If you received this message  ⎥
  ⎢ without having explicitly used the module, please contact the     ⎥
  ⎢ author whose module called this to have them update accordingly.  ⎥
  ⎢                                                                   ⎥
  ⎢ Please be aware that fallback languages are not supported when    ⎥
  ⎢ calling by the old name for compile time reasons                  ⎥
  ⎢                                                                   ⎥
  ⎢ You may dismiss this by setting the environment variable          ⎥
  ⎢ RAKU_USER_LANGUAGE_NAMECHANGE_WARNING to OFF. Updates after 2024  ⎥
  ⎣ will no longer provide under the old name.                        ⎦
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::Number::Plural_github:alabamenhu_0.5.4_0/sources/9F5F1EE9CB750282977EDC77049DC45738CEBB55 (Intl::Number::Plural)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/2D64AB7F840DBC1187A48A651516D851331602DA (Intl::CLDR)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/983C26B86287DA3FF695AA2FBF5F0DD2D70F4DC6 (Intl::CLDR::Types::Database)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/202601A191D2EB4FD96D1F154320EEB3E311A9C4 (Intl::CLDR::Types::Languages)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/7B5ABC9367F8DD6813475C416AB192F71A78B276 (Intl::CLDR::Types::Language)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/276219BCFD79C8B10BB4F20F7A14A5F56CA4B355 (Intl::CLDR::Types::Units)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/716C26AB03A4E6BA0D2FCB27543389D42730167C (Intl::CLDR::Types::SimpleUnits)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/191C8E803D779AFE6049DD4B613FB10C004EC0AA (Intl::CLDR::Types::SimpleUnitSet)
  This type cannot unbox to a native string: P6opaque, Int
  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/191C8E803D779AFE6049DD4B613FB10C004EC0AA (Intl::CLDR::Types::SimpleUnitSet):4
  ------>     <HERE>use Intl::CLDR::Enums;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/716C26AB03A4E6BA0D2FCB27543389D42730167C (Intl::CLDR::Types::SimpleUnits):8
  ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnitSet;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/276219BCFD79C8B10BB4F20F7A14A5F56CA4B355 (Intl::CLDR::Types::Units):6
  ------> <BOL><HERE>use Intl::CLDR::Types::SimpleUnits;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/7B5ABC9367F8DD6813475C416AB192F71A78B276 (Intl::CLDR::Types::Language):15
  ------> <BOL><HERE>use Intl::CLDR::Types::Units;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/202601A191D2EB4FD96D1F154320EEB3E311A9C4 (Intl::CLDR::Types::Languages):4
  ------> <BOL><HERE>use Intl::CLDR::Types::Language;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/983C26B86287DA3FF695AA2FBF5F0DD2D70F4DC6 (Intl::CLDR::Types::Database):3
  ------>     <HERE>use Intl::CLDR::Types::Languages;

  at /home/coke/sandbox/blin/installed/Intl::CLDR_zef:guifa_0.7.6_1/sources/2D64AB7F840DBC1187A48A651516D851331602DA (Intl::CLDR):31
  ------>     <HERE>use Intl::CLDR::Types::Database;

  at /home/coke/sandbox/blin/installed/Intl::Number::Plural_github:alabamenhu_0.5.4_0/sources/9F5F1EE9CB750282977EDC77049DC45738CEBB55 (Intl::Number::Plural):4
  ------> <BOL><HERE>use Intl::CLDR;

            Finished with result: exit-code
  Main processes terminated with: code=exited, status=1/FAILURE
                 Service runtime: 11.237s
               CPU time consumed: 13.665s
                     Memory peak: 2.6G (swap: 0B)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| Fail                      |     2 | [Intl::CLDR](https://raku.land/zef:guifa/Intl::CLDR) [Intl::Number::Plural](https://raku.land/github:alabamenhu/Intl::Number::Plural) |
| AlwaysFail                |     7 | [BDD::Behave](https://raku.land/zef:gdonald/BDD::Behave) [Intl::LanguageTag](https://raku.land/zef:guifa/Intl::LanguageTag) [JSON::Class](https://raku.land/zef:jonathanstowe/JSON::Class) [License::SPDX](https://raku.land/zef:jonathanstowe/License::SPDX) [META6](https://raku.land/zef:jonathanstowe/META6) [Test::META](https://raku.land/zef:jonathanstowe/Test::META) [User::Language](https://raku.land/zef:guifa/User::Language) |
| OK                        |    60 | ⋯                         |



This run started on 2026-10-09T16:21:30Z and finished in 35 minutes.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
