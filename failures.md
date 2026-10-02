[Blin](https://github.com/Raku/Blin) results between 2026.09 ([9a94801](https://github.com/rakudo/rakudo/commit/9a94801c154543573d926e6258e062f3c3782635)) and 8de7894122 ([8de7894](https://github.com/rakudo/rakudo/commit/8de7894122c342cd22a95f6af91365eed57ec846)):

* [ ] [Injector](https://raku.land/zef:FCO/Injector) – Fail, Bisected: [f20534c](https://github.com/rakudo/rakudo/commit/f20534cb3a5df815e7c3b8ca08160bcb78f9d6c2)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p526251-i8918502.service; invocation ID: 8963a648392545b3ac66c53557d146e3
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Injector
  ===> Found: Injector:ver<0.0.1>:auth<zef:FCO> [via Zef::Repository::Ecosystems<fez>]
  [Injector] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1790947371.526252.5583.808281699001/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz https://360.zef.pm/I/NJ/INJECTOR/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  ===> Fetching [OK]: Injector:ver<0.0.1>:auth<zef:FCO> to /home/coke/sandbox/blin/data/zef-data/tmp/1790947371.526252.5583.808281699001/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  [Injector] Command: tar -t -f ./c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  [Injector] Command: tar -xvf ./c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz -C ../c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  ===> Extraction [OK]: Injector to /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  ===> Testing: Injector:ver<0.0.1>:auth<zef:FCO>
  [Injector] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1 t/02-test.rakutest
  [Injector] WARNING: unhandled Failure detected in DESTROY. If you meant to ignore it, you can mark it as handled by calling .Bool, .so, .not, or .defined methods. The Failure was:
  [Injector] No such symbol 'Test'
  [Injector]   in block <unit> at t/02-test.rakutest line 14
  [Injector]   in method IMPL-LOAD-MODULE at src/Raku/ast/statements.rakumod line 2547
  [Injector]   in any PERFORM-BEGIN at src/Raku/ast/statements.rakumod line 2813
  [Injector]   in any  at src/Raku/ast/begintime.rakumod line 21
  [Injector]   in method ensure-begin-performed at src/Raku/ast/begintime.rakumod line 18
  [Injector]   in any statement-control at /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/share/perl6/lib/Raku/Grammar.moarvm line 1
  [Injector] ok 1 - 
  [Injector] ok 2 - 
  [Injector] ok 3 - 
  [Injector] ok 4 - 
  [Injector] ok 5 - 
  [Injector] ok 6 - 
  [Injector] ok 7 - 
  [Injector] ok 8 - 
  [Injector] ok 9 - 
  [Injector] ok 10 - 
  [Injector] 1..10
  [Injector] Saw 1 occurrence of deprecated code.
  [Injector] ================================================================================
  [Injector] Method perl (from Mu) seen at:
  [Injector]   /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Storage.rakumod (Injector::Storage), lines 10,14
  [Injector] Please use raku instead.
  [Injector] --------------------------------------------------------------------------------
  [Injector] Please contact the author to have these occurrences of deprecated code
  [Injector] adapted, so that this message will disappear!
  ===> Testing [OK] for Injector:ver<0.0.1>:auth<zef:FCO>
  ===> Installing: Injector:ver<0.0.1>:auth<zef:FCO>
  ===> Install [OK] for Injector:ver<0.0.1>:auth<zef:FCO>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 22.214s
               CPU time consumed: 31.436s
                     Memory peak: 1.1G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p526131-i8850637.service; invocation ID: ff8c33c659f040d48a725b95e3f6ed59
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Injector
  ===> Found: Injector:ver<0.0.1>:auth<zef:FCO> [via Zef::Repository::Ecosystems<fez>]
  [Injector] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1790947351.526133.1061.059523232949/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz https://360.zef.pm/I/NJ/INJECTOR/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  ===> Fetching [OK]: Injector:ver<0.0.1>:auth<zef:FCO> to /home/coke/sandbox/blin/data/zef-data/tmp/1790947351.526133.1061.059523232949/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  [Injector] Command: tar -t -f ./c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  [Injector] Command: tar -xvf ./c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz -C ../c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  ===> Extraction [OK]: Injector to /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  ===> Testing: Injector:ver<0.0.1>:auth<zef:FCO>
  [Injector] Command: /tmp/whateverable/rakudo-moar/8de7894122c342cd22a95f6af91365eed57ec846/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1 t/02-test.rakutest
  [Injector] ===SORRY!=== Error while compiling t/02-test.rakutest
  [Injector] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Storage.rakumod (Injector::Storage)
  [Injector] multidimensional shaped hashes not yet implemented. Sorry.
  [Injector] at /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Storage.rakumod (Injector::Storage):5
  [Injector] ------> has <HERE>%!bind{Str:D; Str:D; Str:D};
  [Injector] at t/02-test.rakutest:4
  [Injector] ------> <BOL><HERE>use Injector;
  ===> Testing [FAIL]: Injector:ver<0.0.1>:auth<zef:FCO>
  [Injector] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Injector:ver<0.0.1>:auth<zef:FCO>
  ===> Install [FAIL] for Injector:ver<0.0.1>:auth<zef:FCO>: ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Injector_zef:FCO_0.0.1_0/sources/3676574614DBE24DDE0F241F908B877548574CDB (Injector::Storage)
  multidimensional shaped hashes not yet implemented. Sorry.
  at /home/coke/sandbox/blin/installed/Injector_zef:FCO_0.0.1_0/sources/3676574614DBE24DDE0F241F908B877548574CDB (Injector::Storage):5
  ------> has <HERE>%!bind{Str:D; Str:D; Str:D};

  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Injector_zef:FCO_0.0.1_0/sources/3676574614DBE24DDE0F241F908B877548574CDB (Injector::Storage)
  multidimensional shaped hashes not yet implemented. Sorry.
  at /home/coke/sandbox/blin/installed/Injector_zef:FCO_0.0.1_0/sources/3676574614DBE24DDE0F241F908B877548574CDB (Injector::Storage):5
  ------> has <HERE>%!bind{Str:D; Str:D; Str:D};

            Finished with result: exit-code
  Main processes terminated with: code=exited, status=1/FAILURE
                 Service runtime: 6.211s
               CPU time consumed: 6.981s
                     Memory peak: 1G (swap: 0B)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| Fail                      |     1 | [Injector](https://raku.land/zef:FCO/Injector) |
| AlwaysFail                |     4 | [JSON::Class](https://raku.land/zef:jonathanstowe/JSON::Class) [License::SPDX](https://raku.land/zef:jonathanstowe/License::SPDX) [META6](https://raku.land/zef:jonathanstowe/META6) [Test::META](https://raku.land/zef:jonathanstowe/Test::META) |
| OK                        |    53 | ⋯                         |



This run started on 2026-10-02T13:27:26Z and finished in 7 minutes.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
