[Blin](https://github.com/Raku/Blin) results between 2026.08 ([24e6e53](https://github.com/rakudo/rakudo/commit/24e6e5312f2868680413b0597aef8772f6b5bcea)) and 7a3abc5aba ([7a3abc5](https://github.com/rakudo/rakudo/commit/7a3abc5ababa5842e6346438d5e0675f2599ecb3)):

* [ ] [Terminal::UI](https://raku.land/zef:bduggan/Terminal::UI) – Fail, Bisected: [8464af2](https://github.com/rakudo/rakudo/commit/8464af23d703d9f86ace5d19ea4e2dd3e5f80ec5)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p950379-i983610.service; invocation ID: 1e6416db2c0e4de49e79d1deb9d0823c
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Terminal::UI
  ===> Found: Terminal::UI:ver<0.1.14>:auth<zef:bduggan> [via Zef::Repository::Ecosystems<fez>]
  [Terminal::UI] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789696276.950393.9515.921883805193/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz https://360.zef.pm/T/ER/TERMINAL_UI/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  ===> Fetching [OK]: Terminal::UI:ver<0.1.14>:auth<zef:bduggan> to /home/coke/sandbox/blin/data/zef-data/tmp/1789696276.950393.9515.921883805193/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  [Terminal::UI] Command: tar -t -f ./97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  [Terminal::UI] Command: tar -xvf ./97be0392703c0ef562b9092d0a52c2623157131c.tar.gz -C ../97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  ===> Extraction [OK]: Terminal::UI to /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  ===> Testing: Terminal::UI:ver<0.1.14>:auth<zef:bduggan>
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/00-basic.rakutest
  [Terminal::UI] 1..6
  [Terminal::UI] ok 1 - Terminal::UI module can be use-d ok
  [Terminal::UI] ok 2 - Terminal::UI::Screen module can be use-d ok
  [Terminal::UI] ok 3 - Terminal::UI::Frame module can be use-d ok
  [Terminal::UI] ok 4 - Terminal::UI::Pane module can be use-d ok
  [Terminal::UI] ok 5 - Terminal::UI::Input module can be use-d ok
  [Terminal::UI] ok 6 - Terminal::UI::Style module can be use-d ok
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/01-sizes.rakutest
  [Terminal::UI] 1..41
  [Terminal::UI] ok 1 - screen height
  [Terminal::UI] ok 2 - screen rows
  [Terminal::UI] ok 3 - top
  [Terminal::UI] ok 4 - height
  [Terminal::UI] ok 5 - height
  [Terminal::UI] ok 6 - frame width
  [Terminal::UI] ok 7 - pane top
  [Terminal::UI] ok 8 - pane height
  [Terminal::UI] ok 9 - pane left
  [Terminal::UI] ok 10 - pane width
  [Terminal::UI] ok 11 - full top is 1
  [Terminal::UI] ok 12 - full has screen rows
  [Terminal::UI] ok 13 - height 1
  [Terminal::UI] ok 14 - height 2
  [Terminal::UI] ok 15 - check is ok
  [Terminal::UI] ok 16 - divider
  [Terminal::UI] ok 17 - height 1
  [Terminal::UI] ok 18 - check is ok
  [Terminal::UI] ok 19 - height 1
  [Terminal::UI] ok 20 - height 2
  [Terminal::UI] ok 21 - height 3
  [Terminal::UI] ok 22 - check is ok
  [Terminal::UI] ok 23 - height 1
  [Terminal::UI] ok 24 - height 2
  [Terminal::UI] ok 25 - height 3
  [Terminal::UI] ok 26 - check is ok
  [Terminal::UI] ok 27 - height 1
  [Terminal::UI] ok 28 - height 2
  [Terminal::UI] ok 29 - height 3
  [Terminal::UI] ok 30 - check is ok
  [Terminal::UI] ok 31 - height 1
  [Terminal::UI] ok 32 - height 2
  [Terminal::UI] ok 33 - check is ok
  [Terminal::UI] ok 34 - height 1
  [Terminal::UI] ok 35 - height 2
  [Terminal::UI] ok 36 - height 3
  [Terminal::UI] ok 37 - check is ok
  [Terminal::UI] ok 38 - height 1
  [Terminal::UI] ok 39 - height 2
  [Terminal::UI] ok 40 - height 3
  [Terminal::UI] ok 41 - check is ok
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/02-screen.rakutest
  [Terminal::UI] ok 1 - rows
  [Terminal::UI] ok 2 - cols
  [Terminal::UI] 1..2
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/03-pane.rakutest
  [Terminal::UI] ok 1 - bottom
  [Terminal::UI] ok 2 - right
  [Terminal::UI] ok 3 - lines
  [Terminal::UI] ok 4 - two lines
  [Terminal::UI] ok 5 - scroll up
  [Terminal::UI] ok 6 - word wrap with indent
  [Terminal::UI] ok 7 - hard wrap with indent
  [Terminal::UI] ok 8 - word wrap with hang
  [Terminal::UI] 1..8
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/04-frame.rakutest
  [Terminal::UI] ok 1 - full
  [Terminal::UI] ok 2 - render
  [Terminal::UI] 1..2
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/05-style.rakutest
  [Terminal::UI] 1..2
  [Terminal::UI] ok 1 - set a value
  [Terminal::UI] ok 2 - singleton works
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/06-ui.rakutest
  [Terminal::UI] ok 1 - height
  [Terminal::UI] ok 2 - width
  [Terminal::UI] ok 3 - top
  [Terminal::UI] ok 4 - left
  [Terminal::UI] ok 5 - render
  [Terminal::UI] 1..5
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/07-alert.rakutest
  [Terminal::UI] ok 1 - initial screen
  [Terminal::UI] ok 2 - alert
  [Terminal::UI] ok 3 - dismissed
  [Terminal::UI] 1..3
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/08-resize.rakutest
  [Terminal::UI] 1..2
  [Terminal::UI] ok 1 - initial heights
  [Terminal::UI] ok 2 - resize
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/09-print.rakutest
  [Terminal::UI] 1..21
  [Terminal::UI] ok 1 - prints characters to line
  [Terminal::UI] ok 2 - newline moves to next line
  [Terminal::UI] ok 3 - carriage return resets to start of line
  [Terminal::UI] ok 4 - lines accumulate for scrollback
  [Terminal::UI] ok 5 - can access historical lines
  [Terminal::UI] ok 6 - escape sequences not stored in content
  [Terminal::UI] ok 7 - print writes to last line
  [Terminal::UI] ok 8 - first-visible updates when content exceeds height
  [Terminal::UI] ok 9 - string with newlines splits correctly
  [Terminal::UI] ok 10 - first line from batched string
  [Terminal::UI] ok 11 - third line from batched string
  [Terminal::UI] ok 12 - mixed string with carriage return
  [Terminal::UI] ok 13 - stream handles basic text
  [Terminal::UI] ok 14 - stream handles newlines
  [Terminal::UI] ok 15 - stream first line correct
  [Terminal::UI] ok 16 - stream filters ANSI sequences
  [Terminal::UI] ok 17 - put then print creates two lines
  [Terminal::UI] ok 18 - put creates first line
  [Terminal::UI] ok 19 - print goes to second line after put
  [Terminal::UI] ok 20 - two prints then put creates two lines
  [Terminal::UI] ok 21 - prints combine on same line, put adds new line
  ===> Testing [OK] for Terminal::UI:ver<0.1.14>:auth<zef:bduggan>
  ===> Installing: Terminal::UI:ver<0.1.14>:auth<zef:bduggan>
  ===> Install [OK] for Terminal::UI:ver<0.1.14>:auth<zef:bduggan>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 3min 7.819s
               CPU time consumed: 3min 11.355s
                     Memory peak: 1.6G (swap: 288.3M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p944314-i964340.service; invocation ID: e5b0090a38ea4522ad6283dec10f4e01
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Terminal::UI
  ===> Found: Terminal::UI:ver<0.1.14>:auth<zef:bduggan> [via Zef::Repository::Ecosystems<fez>]
  [Terminal::UI] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789696115.944321.9917.683746449433/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz https://360.zef.pm/T/ER/TERMINAL_UI/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  ===> Fetching [OK]: Terminal::UI:ver<0.1.14>:auth<zef:bduggan> to /home/coke/sandbox/blin/data/zef-data/tmp/1789696115.944321.9917.683746449433/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  [Terminal::UI] Command: tar -t -f ./97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  [Terminal::UI] Command: tar -xvf ./97be0392703c0ef562b9092d0a52c2623157131c.tar.gz -C ../97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  ===> Extraction [OK]: Terminal::UI to /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  ===> Testing: Terminal::UI:ver<0.1.14>:auth<zef:bduggan>
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/00-basic.rakutest
  [Terminal::UI] 1..6
  [Terminal::UI] ok 1 - Terminal::UI module can be use-d ok
  [Terminal::UI] ok 2 - Terminal::UI::Screen module can be use-d ok
  [Terminal::UI] ok 3 - Terminal::UI::Frame module can be use-d ok
  [Terminal::UI] ok 4 - Terminal::UI::Pane module can be use-d ok
  [Terminal::UI] ok 5 - Terminal::UI::Input module can be use-d ok
  [Terminal::UI] ok 6 - Terminal::UI::Style module can be use-d ok
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/01-sizes.rakutest
  [Terminal::UI] 1..41
  [Terminal::UI] ok 1 - screen height
  [Terminal::UI] ok 2 - screen rows
  [Terminal::UI] ok 3 - top
  [Terminal::UI] ok 4 - height
  [Terminal::UI] ok 5 - height
  [Terminal::UI] ok 6 - frame width
  [Terminal::UI] ok 7 - pane top
  [Terminal::UI] ok 8 - pane height
  [Terminal::UI] ok 9 - pane left
  [Terminal::UI] ok 10 - pane width
  [Terminal::UI] ok 11 - full top is 1
  [Terminal::UI] ok 12 - full has screen rows
  [Terminal::UI] ok 13 - height 1
  [Terminal::UI] ok 14 - height 2
  [Terminal::UI] ok 15 - check is ok
  [Terminal::UI] ok 16 - divider
  [Terminal::UI] ok 17 - height 1
  [Terminal::UI] ok 18 - check is ok
  [Terminal::UI] ok 19 - height 1
  [Terminal::UI] ok 20 - height 2
  [Terminal::UI] ok 21 - height 3
  [Terminal::UI] ok 22 - check is ok
  [Terminal::UI] ok 23 - height 1
  [Terminal::UI] ok 24 - height 2
  [Terminal::UI] ok 25 - height 3
  [Terminal::UI] ok 26 - check is ok
  [Terminal::UI] ok 27 - height 1
  [Terminal::UI] ok 28 - height 2
  [Terminal::UI] ok 29 - height 3
  [Terminal::UI] ok 30 - check is ok
  [Terminal::UI] ok 31 - height 1
  [Terminal::UI] ok 32 - height 2
  [Terminal::UI] ok 33 - check is ok
  [Terminal::UI] ok 34 - height 1
  [Terminal::UI] ok 35 - height 2
  [Terminal::UI] ok 36 - height 3
  [Terminal::UI] ok 37 - check is ok
  [Terminal::UI] ok 38 - height 1
  [Terminal::UI] ok 39 - height 2
  [Terminal::UI] ok 40 - height 3
  [Terminal::UI] ok 41 - check is ok
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/02-screen.rakutest
  [Terminal::UI] ok 1 - rows
  [Terminal::UI] ok 2 - cols
  [Terminal::UI] 1..2
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/03-pane.rakutest
  [Terminal::UI] ok 1 - bottom
  [Terminal::UI] ok 2 - right
  [Terminal::UI] ok 3 - lines
  [Terminal::UI] ok 4 - two lines
  [Terminal::UI] ok 5 - scroll up
  [Terminal::UI] ok 6 - word wrap with indent
  [Terminal::UI] ok 7 - hard wrap with indent
  [Terminal::UI] ok 8 - word wrap with hang
  [Terminal::UI] 1..8
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/04-frame.rakutest
  [Terminal::UI] ok 1 - full
  [Terminal::UI] ok 2 - render
  [Terminal::UI] 1..2
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/05-style.rakutest
  [Terminal::UI] 1..2
  [Terminal::UI] ok 1 - set a value
  [Terminal::UI] ok 2 - singleton works
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/06-ui.rakutest
  [Terminal::UI] ok 1 - height
  [Terminal::UI] ok 2 - width
  [Terminal::UI] ok 3 - top
  [Terminal::UI] ok 4 - left
  [Terminal::UI] ok 5 - render
  [Terminal::UI] 1..5
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/07-alert.rakutest
  [Terminal::UI] ok 1 - initial screen
  [Terminal::UI] not ok 2 - alert
  [Terminal::UI] # Failed test 'alert'
  [Terminal::UI] # at t/07-alert.rakutest line 45
  [Terminal::UI] # expected: '"╔══════════════════╗\n║Hello!            ║\n║w╔══════════════╗ ║\n║ ║   ¡ALERT!    ║ ║\n║ ╟──────────────╢ ║\n║ ╢      ok      ║ ║\n║ ╚══════════════╝ ║\n║                  ║\n║                  ║\n╚══════════════════╝\n"'
  [Terminal::UI] #      got: '"╔══════════════════╗\n║Hello!            ║\n║w╔══════════════╗ ║\n║ ║   ¡ALERT!    ║ ║\n║ ╟──────────────╢ ║\n║ ║      ok      ║ ║\n║ ╚══════════════╝ ║\n║                  ║\n║                  ║\n╚══════════════════╝\n"'
  [Terminal::UI] ok 3 - dismissed
  [Terminal::UI] 1..3
  [Terminal::UI] # You failed 1 test of 3
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/08-resize.rakutest
  [Terminal::UI] 1..2
  [Terminal::UI] ok 1 - initial heights
  [Terminal::UI] ok 2 - resize
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/09-print.rakutest
  [Terminal::UI] 1..21
  [Terminal::UI] ok 1 - prints characters to line
  [Terminal::UI] ok 2 - newline moves to next line
  [Terminal::UI] ok 3 - carriage return resets to start of line
  [Terminal::UI] ok 4 - lines accumulate for scrollback
  [Terminal::UI] ok 5 - can access historical lines
  [Terminal::UI] ok 6 - escape sequences not stored in content
  [Terminal::UI] ok 7 - print writes to last line
  [Terminal::UI] ok 8 - first-visible updates when content exceeds height
  [Terminal::UI] ok 9 - string with newlines splits correctly
  [Terminal::UI] ok 10 - first line from batched string
  [Terminal::UI] ok 11 - third line from batched string
  [Terminal::UI] ok 12 - mixed string with carriage return
  [Terminal::UI] ok 13 - stream handles basic text
  [Terminal::UI] ok 14 - stream handles newlines
  [Terminal::UI] ok 15 - stream first line correct
  [Terminal::UI] ok 16 - stream filters ANSI sequences
  [Terminal::UI] ok 17 - put then print creates two lines
  [Terminal::UI] ok 18 - put creates first line
  [Terminal::UI] ok 19 - print goes to second line after put
  [Terminal::UI] ok 20 - two prints then put creates two lines
  [Terminal::UI] ok 21 - prints combine on same line, put adds new line
  ===> Testing [FAIL]: Terminal::UI:ver<0.1.14>:auth<zef:bduggan>
  [Terminal::UI] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Terminal::UI:ver<0.1.14>:auth<zef:bduggan>
  ===> Install [OK] for Terminal::UI:ver<0.1.14>:auth<zef:bduggan>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 37.041s
               CPU time consumed: 2min 39.388s
                     Memory peak: 1.4G (swap: 187.5M)

  ```
  </details>
* [ ] [Polyglot::Regexen](https://raku.land/zef:guifa/Polyglot::Regexen) – Fail, Bisected: [aab0778](https://github.com/rakudo/rakudo/commit/aab0778725da5848824f07514c0ae355d972926a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p764673-i803064.service; invocation ID: f8d8741f0a4445968974dd58599c87fc
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Polyglot::Regexen
  ===> Found: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> [via Zef::Repository::Ecosystems<fez>]
  [Polyglot::Regexen] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789691379.764674.340.9944496280981/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz https://360.zef.pm/P/OL/POLYGLOT_REGEXEN/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Fetching [OK]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> to /home/coke/sandbox/blin/data/zef-data/tmp/1789691379.764674.340.9944496280981/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
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
                 Service runtime: 2min 9.334s
               CPU time consumed: 2min 23.673s
                     Memory peak: 1.6G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p760160-i724863.service; invocation ID: 31faaa72fccc4b27b9e59466bd8fcff1
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Polyglot::Regexen
  ===> Found: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> [via Zef::Repository::Ecosystems<fez>]
  [Polyglot::Regexen] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789691252.760162.9094.799066130821/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz https://360.zef.pm/P/OL/POLYGLOT_REGEXEN/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Fetching [OK]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> to /home/coke/sandbox/blin/data/zef-data/tmp/1789691252.760162.9094.799066130821/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  [Polyglot::Regexen] Command: tar -t -f ./17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  [Polyglot::Regexen] Command: tar -xvf ./17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz -C ../17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Extraction [OK]: Polyglot::Regexen to /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Testing: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/00-sanity.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] 1..1
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/01-literals.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/02-character-classes.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/03-alternation.rakutest
  [Polyglot::Regexen] ok 1 - Simple alternation, two terms
  [Polyglot::Regexen] ok 2 - Simple alternation, three terms
  [Polyglot::Regexen] 1..2
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/04-assertions.rakutest
  [Polyglot::Regexen] ok 1 - Simple lookahead
  [Polyglot::Regexen] ok 2 - Simple negative lookahead
  [Polyglot::Regexen] ok 3 - Simple lookbehind
  [Polyglot::Regexen] ok 4 - Simple negative lookbehind
  [Polyglot::Regexen] 1..4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/05-quantifiers.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/06-captures.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/07-unicode.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/08-modifiers.rakutest
  [Polyglot::Regexen] ok 1 - 
  [Polyglot::Regexen] ok 2 - 
  [Polyglot::Regexen] ok 3 - 
  [Polyglot::Regexen] ok 4 - 
  [Polyglot::Regexen] 1..4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/09-role.rakutest
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
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/10-usage.rakutest
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
                 Service runtime: 2min 16.251s
               CPU time consumed: 2min 23.895s
                     Memory peak: 1.5G (swap: 0B)

  ```
  </details>
* [ ] [GIO](https://raku.land/cpan:CBWOOD/GIO) – Fail, Bisected: [6357ccf](https://github.com/rakudo/rakudo/commit/6357ccf97f2c4b1dd1067bf4f50b6cdcfdb78373)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1259562-i1307805.service; invocation ID: ad82b994ed1b407c9a8c50da680af8d6
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: GIO
  ===> Found: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1> [via Zef::Repository::Ecosystems<rea>]
  [GIO] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789704621.1259563.8570.988910806222/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/GIO/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  ===> Fetching [OK]: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1> to /home/coke/sandbox/blin/data/zef-data/tmp/1789704621.1259563.8570.988910806222/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  [GIO] Command: tar -t -f ./GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  [GIO] Command: tar -xvf ./GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz -C ../GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  ===> Extraction [OK]: GIO to /home/coke/sandbox/blin/data/zef-data/tmp/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  ===> Testing: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1>
  [GIO] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz/GIO-0.0.4 t/01-modules.t
  [GIO] 1..294
  [GIO] ok 1 - GIO
  [GIO] ok 2 - GIO::AppInfoMonitor
  [GIO] ok 3 - GIO::Application
  [GIO] ok 4 - GIO::ApplicationCommandLine
  [GIO] ok 5 - GIO::BufferedInputStream
  [GIO] ok 6 - GIO::BufferedOutputStream
  [GIO] ok 7 - GIO::Builder
  [GIO] ok 8 - GIO::BytesIcon
  [GIO] ok 9 - GIO::Cancellable
  [GIO] ok 10 - GIO::CharsetConverter
  [GIO] ok 11 - GIO::ContentType
  [GIO] ok 12 - GIO::ConverterInputStream
  [GIO] ok 13 - GIO::ConverterOutputStream
  [GIO] ok 14 - GIO::Credentials
  [GIO] ok 15 - GIO::DBus::ActionGroup
  [GIO] ok 16 - GIO::DBus::Address
  [GIO] ok 17 - GIO::DBus::AuthObserver
  [GIO] ok 18 - GIO::DBus::Connection
  [GIO] ok 19 - GIO::DBus::Error
  [GIO] ok 20 - GIO::DBus::InterfaceSkeleton
  [GIO] ok 21 - GIO::DBus::Message
  [GIO] ok 22 - GIO::DBus::MethodInvocation
  [GIO] ok 23 - GIO::DBus::ObjectManagerClient
  [GIO] ok 24 - GIO::DBus::ObjectManagerServer
  [GIO] ok 25 - GIO::DBus::ObjectProxy
  [GIO] ok 26 - GIO::DBus::ObjectSkeleton
  [GIO] ok 27 - GIO::DBus::Proxy
  [GIO] ok 28 - GIO::DBus::Raw::Address
  [GIO] ok 29 - GIO::DBus::Raw::Connection
  [GIO] ok 30 - GIO::DBus::Raw::Error
  [GIO] ok 31 - GIO::DBus::Raw::Interface
  [GIO] ok 32 - GIO::DBus::Raw::InterfaceSkeleton
  [GIO] ok 33 - GIO::DBus::Raw::Message
  [GIO] ok 34 - GIO::DBus::Raw::MethodInvocation
  [GIO] ok 35 - GIO::DBus::Raw::ObjectManager
  [GIO] ok 36 - GIO::DBus::Raw::ObjectManagerClient
  [GIO] ok 37 - GIO::DBus::Raw::ObjectManagerServer
  [GIO] ok 38 - GIO::DBus::Raw::ObjectSkeleton
  [GIO] ok 39 - GIO::DBus::Raw::Proxy
  [GIO] ok 40 - GIO::DBus::Raw::Server
  [GIO] ok 41 - GIO::DBus::Raw::Subs
  [GIO] ok 42 - GIO::DBus::Raw::Types
  [GIO] ok 43 - GIO::DBus::Raw::Utils
  [GIO] ok 44 - GIO::DBus::Roles::Interface
  [GIO] ok 45 - GIO::DBus::Roles::Object
  [GIO] ok 46 - GIO::DBus::Roles::ObjectManager
  [GIO] ok 47 - GIO::DBus::Roles::Signals::AuthObserver
  [GIO] ok 48 - GIO::DBus::Roles::Signals::Connection
  [GIO] ok 49 - GIO::DBus::Roles::Signals::InterfaceSkeleton
  [GIO] ok 50 - GIO::DBus::Roles::Signals::Object
  [GIO] ok 51 - GIO::DBus::Roles::Signals::ObjectManager
  [GIO] ok 52 - GIO::DBus::Roles::Signals::ObjectManagerClient
  [GIO] ok 53 - GIO::DBus::Roles::Signals::ObjectSkeleton
  [GIO] ok 54 - GIO::DBus::Roles::Signals::Proxy
  [GIO] ok 55 - GIO::DBus::Roles::Signals::Server
  [GIO] ok 56 - GIO::DBus::Roles::SupplyCallback
  [GIO] ok 57 - GIO::DBus::Server
  [GIO] ok 58 - GIO::DBus::Utils
  [GIO] ok 59 - GIO::DataInputStream
  [GIO] ok 60 - GIO::DataOutputStream
  [GIO] ok 61 - GIO::DesktopAppInfo
  [GIO] ok 62 - GIO::Emblem
  [GIO] ok 63 - GIO::EmblemedIcon
  [GIO] ok 64 - GIO::Enums
  [GIO] ok 65 - GIO::FileAttributeInfoList
  [GIO] ok 66 - GIO::FileAttributeMatcher
  [GIO] ok 67 - GIO::FileEnumerator
  [GIO] ok 68 - GIO::FileIOStream
  [GIO] ok 69 - GIO::FileIcon
  [GIO] ok 70 - GIO::FileInfo
  [GIO] ok 71 - GIO::FileInputStream
  [GIO] ok 72 - GIO::FileMonitor
  [GIO] ok 73 - GIO::FileMonitor::Local
  [GIO] ok 74 - GIO::FileOutputStream
  [GIO] ok 75 - GIO::FilenameCompleter
  [GIO] ok 76 - GIO::FilterInputStream
  [GIO] ok 77 - GIO::FilterOutputStream
  [GIO] ok 78 - GIO::InetAddress
  [GIO] ok 79 - GIO::InetAddressMask
  [GIO] ok 80 - GIO::InetSocketAddress
  [GIO] ok 81 - GIO::InputStream
  [GIO] ok 82 - GIO::LaunchContext
  [GIO] ok 83 - GIO::ListStore
  [GIO] ok 84 - GIO::MemoryInputStream
  [GIO] ok 85 - GIO::MemoryOutputStream
  [GIO] ok 86 - GIO::Menu
  [GIO] ok 87 - GIO::MenuAttributeIter
  [GIO] ok 88 - GIO::MenuItem
  [GIO] ok 89 - GIO::MenuLinkIter
  [GIO] ok 90 - GIO::MenuModel
  [GIO] ok 91 - GIO::MiscTypes
  [GIO] ok 92 - GIO::MountOperation
  [GIO] ok 93 - GIO::NetworkAddress
  [GIO] ok 94 - GIO::NetworkService
  [GIO] ok 95 - GIO::Notification
  [GIO] ok 96 - GIO::OutputStream
  [GIO] ok 97 - GIO::Permission
  [GIO] ok 98 - GIO::PropertyAction
  [GIO] ok 99 - GIO::ProxyAddress
  [GIO] ok 100 - GIO::ProxyAddressEnumerator
  [GIO] ok 101 - GIO::Raw::Action
  [GIO] ok 102 - GIO::Raw::ActionGroup
  [GIO] ok 103 - GIO::Raw::AppInfo
  [GIO] ok 104 - GIO::Raw::Application
  [GIO] ok 105 - GIO::Raw::ApplicationCommandLine
  [GIO] ok 106 - GIO::Raw::AsyncInitable
  [GIO] ok 107 - GIO::Raw::AsyncResult
  [GIO] ok 108 - GIO::Raw::BufferedInputStream
  [GIO] ok 109 - GIO::Raw::BufferedOutputStream
  [GIO] ok 110 - GIO::Raw::Cancellable
  [GIO] ok 111 - GIO::Raw::CharsetConverter
  [GIO] ok 112 - GIO::Raw::ContentType
  [GIO] ok 113 - GIO::Raw::Credentials
  [GIO] ok 114 - GIO::Raw::DataInputStream
  [GIO] ok 115 - GIO::Raw::DataOutputStream
  [GIO] ok 116 - GIO::Raw::DatagramBased
  [GIO] ok 117 - GIO::Raw::Definitions
  [GIO] ok 118 - GIO::Raw::DesktopAppInfo
  [GIO] ok 119 - GIO::Raw::Distro
  [GIO] ok 120 - GIO::Raw::Drive
  [GIO] ok 121 - GIO::Raw::DtlsClientConnection
  [GIO] ok 122 - GIO::Raw::DtlsConnection
  [GIO] ok 123 - GIO::Raw::Emblem
  [GIO] ok 124 - GIO::Raw::EmblemedIcon
  [GIO] ok 125 - GIO::Raw::Enums
  [GIO] ok 126 - GIO::Raw::Exports
  [GIO] ok 127 - GIO::Raw::FileAttributeInfoList
  [GIO] ok 128 - GIO::Raw::FileAttributeTypes
  [GIO] ok 129 - GIO::Raw::FileEnumerator
  [GIO] ok 130 - GIO::Raw::FileIOStream
  [GIO] ok 131 - GIO::Raw::FileInfo
  [GIO] ok 132 - GIO::Raw::FileMonitor
  [GIO] ok 133 - GIO::Raw::FileMonitor::Local
  [GIO] ok 134 - GIO::Raw::FilenameCompleter
  [GIO] ok 135 - GIO::Raw::FilterInputStream
  [GIO] ok 136 - GIO::Raw::FilterOutputStream
  [GIO] ok 137 - GIO::Raw::GFile
  [GIO] ok 138 - GIO::Raw::Icon
  [GIO] ok 139 - GIO::Raw::InetAddress
  [GIO] ok 140 - GIO::Raw::InetAddressMask
  [GIO] ok 141 - GIO::Raw::InetSocketAddress
  [GIO] ok 142 - GIO::Raw::InputStream
  [GIO] ok 143 - GIO::Raw::ListModel
  [GIO] ok 144 - GIO::Raw::ListStore
  [GIO] ok 145 - GIO::Raw::MemoryInputStream
  [GIO] ok 146 - GIO::Raw::MemoryOutputStream
  [GIO] ok 147 - GIO::Raw::Menu
  [GIO] ok 148 - GIO::Raw::MenuModel
  [GIO] ok 149 - GIO::Raw::Mount
  [GIO] ok 150 - GIO::Raw::MountOperation
  [GIO] ok 151 - GIO::Raw::NetworkAddress
  [GIO] ok 152 - GIO::Raw::NetworkMonitor
  [GIO] ok 153 - GIO::Raw::NetworkService
  [GIO] ok 154 - GIO::Raw::Notification
  [GIO] ok 155 - GIO::Raw::OutputStream
  [GIO] ok 156 - GIO::Raw::Permission
  [GIO] ok 157 - GIO::Raw::PollableInputStream
  [GIO] ok 158 - GIO::Raw::PollableOutputStream
  [GIO] ok 159 - GIO::Raw::Proxy
  [GIO] ok 160 - GIO::Raw::ProxyAddress
  [GIO] ok 161 - GIO::Raw::ProxyResolver
  [GIO] ok 162 - GIO::Raw::Quarks
  [GIO] ok 163 - GIO::Raw::Resolver
  [GIO] ok 164 - GIO::Raw::Resource
  [GIO] ok 165 - GIO::Raw::Seekable
  [GIO] ok 166 - GIO::Raw::Settings
  [GIO] ok 167 - GIO::Raw::SettingsBackend
  [GIO] ok 168 - GIO::Raw::SettingsSchema
  [GIO] ok 169 - GIO::Raw::SimpleAction
  [GIO] ok 170 - GIO::Raw::SimpleActionGroup
  [GIO] ok 171 - GIO::Raw::SimpleAsyncResult
  [GIO] ok 172 - GIO::Raw::SimpleProxyResolver
  [GIO] ok 173 - GIO::Raw::Socket
  [GIO] ok 174 - GIO::Raw::SocketAddress
  [GIO] ok 175 - GIO::Raw::SocketClient
  [GIO] ok 176 - GIO::Raw::SocketConnection
  [GIO] ok 177 - GIO::Raw::SocketControlMessage
  [GIO] ok 178 - GIO::Raw::SocketListener
  [GIO] ok 179 - GIO::Raw::SocketService
  [GIO] ok 180 - GIO::Raw::SrvTarget
  [GIO] ok 181 - GIO::Raw::Stream
  [GIO] ok 182 - GIO::Raw::Structs
  [GIO] ok 183 - GIO::Raw::Subs
  [GIO] ok 184 - GIO::Raw::Task
  [GIO] ok 185 - GIO::Raw::ThemedIcon
  [GIO] ok 186 - GIO::Raw::TlsBackend
  [GIO] ok 187 - GIO::Raw::TlsCertificate
  [GIO] ok 188 - GIO::Raw::TlsClientConnection
  [GIO] ok 189 - GIO::Raw::TlsConnection
  [GIO] ok 190 - GIO::Raw::TlsDatabase
  [GIO] ok 191 - GIO::Raw::TlsInteraction
  [GIO] ok 192 - GIO::Raw::TlsPassword
  [GIO] ok 193 - GIO::Raw::Traps
  [GIO] ok 194 - GIO::Raw::Types
  [GIO] ok 195 - GIO::Raw::UnixConnection
  [GIO] ok 196 - GIO::Raw::UnixCredentialsMessage
  [GIO] ok 197 - GIO::Raw::UnixFDList
  [GIO] ok 198 - GIO::Raw::UnixFDMessage
  [GIO] ok 199 - GIO::Raw::UnixInputStream
  [GIO] ok 200 - GIO::Raw::UnixMounts
  [GIO] ok 201 - GIO::Raw::UnixOutputStream
  [GIO] ok 202 - GIO::Raw::UnixSocketAddress
  [GIO] ok 203 - GIO::Raw::VFS
  [GIO] ok 204 - GIO::Raw::Volume
  [GIO] ok 205 - GIO::Raw::VolumeMonitor
  [GIO] ok 206 - GIO::Resolver
  [GIO] ok 207 - GIO::Resource
  [GIO] ok 208 - GIO::Roles::Action
  [GIO] ok 209 - GIO::Roles::ActionGroup
  [GIO] ok 210 - GIO::Roles::ActionMap
  [GIO] ok 211 - GIO::Roles::AppInfo
  [GIO] ok 212 - GIO::Roles::AsyncInitable
  [GIO] ok 213 - GIO::Roles::AsyncResult
  [GIO] ok 214 - GIO::Roles::Converter
  [GIO] ok 215 - GIO::Roles::DTlsClientConnection
  [GIO] ok 216 - GIO::Roles::DTlsServerConnection
  [GIO] ok 217 - GIO::Roles::DatagramBased
  [GIO] ok 218 - GIO::Roles::Drive
  [GIO] ok 219 - GIO::Roles::DtlsConnection
  [GIO] ok 220 - GIO::Roles::FileDescriptorBased
  [GIO] ok 221 - GIO::Roles::GFile
  [GIO] ok 222 - GIO::Roles::Icon
  [GIO] ok 223 - GIO::Roles::Initable
  [GIO] ok 224 - GIO::Roles::ListModel
  [GIO] ok 225 - GIO::Roles::LoadableIcon
  [GIO] ok 226 - GIO::Roles::Mount
  [GIO] ok 227 - GIO::Roles::NetworkMonitor
  [GIO] ok 228 - GIO::Roles::NetworkMonitorBase
  [GIO] ok 229 - GIO::Roles::PollableInputStream
  [GIO] ok 230 - GIO::Roles::PollableOutputStream
  [GIO] ok 231 - GIO::Roles::Proxy
  [GIO] ok 232 - GIO::Roles::ProxyResolver
  [GIO] ok 233 - GIO::Roles::RemoteActionGroup
  [GIO] ok 234 - GIO::Roles::Seekable
  [GIO] ok 235 - GIO::Roles::Signals::ActionGroup
  [GIO] ok 236 - GIO::Roles::Signals::Application
  [GIO] ok 237 - GIO::Roles::Signals::DtlsConnection
  [GIO] ok 238 - GIO::Roles::Signals::FileMonitor
  [GIO] ok 239 - GIO::Roles::Signals::ListModel
  [GIO] ok 240 - GIO::Roles::Signals::MenuModel
  [GIO] ok 241 - GIO::Roles::Signals::MountOperation
  [GIO] ok 242 - GIO::Roles::Signals::NetworkMonitor
  [GIO] ok 243 - GIO::Roles::Signals::Settings
  [GIO] ok 244 - GIO::Roles::Signals::SocketListener
  [GIO] ok 245 - GIO::Roles::Signals::SocketService
  [GIO] ok 246 - GIO::Roles::Signals::ThreadedSocketService
  [GIO] ok 247 - GIO::Roles::Signals::TlsConnection
  [GIO] ok 248 - GIO::Roles::Signals::VolumeMonitor
  [GIO] ok 249 - GIO::Roles::SocketConnectable
  [GIO] ok 250 - GIO::Roles::TlsBackend
  [GIO] ok 251 - GIO::Roles::TlsClientConnection
  [GIO] ok 252 - GIO::Roles::TlsFileDatabase
  [GIO] ok 253 - GIO::Roles::TlsServerConnection
  [GIO] ok 254 - GIO::Roles::Volume
  [GIO] ok 255 - GIO::Settings
  [GIO] ok 256 - GIO::Settings::Backend
  [GIO] ok 257 - GIO::Settings::Schema
  [GIO] ok 258 - GIO::SimpleAction
  [GIO] ok 259 - GIO::SimpleActionGroup
  [GIO] ok 260 - GIO::SimplePermission
  [GIO] ok 261 - GIO::SimpleProxyResolver
  [GIO] ok 262 - GIO::Socket
  [GIO] ok 263 - GIO::SocketAddress
  [GIO] ok 264 - GIO::SocketAddressEnumerator
  [GIO] ok 265 - GIO::SocketClient
  [GIO] ok 266 - GIO::SocketConnection
  [GIO] ok 267 - GIO::SocketControlMessage
  [GIO] ok 268 - GIO::SocketListener
  [GIO] ok 269 - GIO::SocketService
  [GIO] ok 270 - GIO::SrvTarget
  [GIO] ok 271 - GIO::Stream
  [GIO] ok 272 - GIO::Task
  [GIO] ok 273 - GIO::TcpConnection
  [GIO] ok 274 - GIO::TcpWrapperConnection
  [GIO] ok 275 - GIO::ThemedIcon
  [GIO] ok 276 - GIO::ThreadedSocketService
  [GIO] ok 277 - GIO::TlsCertificate
  [GIO] ok 278 - GIO::TlsConnection
  [GIO] ok 279 - GIO::TlsDatabase
  [GIO] ok 280 - GIO::TlsInteraction
  [GIO] ok 281 - GIO::TlsPassword
  [GIO] ok 282 - GIO::TypeManifest
  [GIO] ok 283 - GIO::Unix::Connection
  [GIO] ok 284 - GIO::Unix::CredentialsMessage
  [GIO] ok 285 - GIO::Unix::FDList
  [GIO] ok 286 - GIO::Unix::FDMessage
  [GIO] ok 287 - GIO::Unix::InputStream
  [GIO] ok 288 - GIO::Unix::Mounts
  [GIO] ok 289 - GIO::Unix::OutputStream
  [GIO] ok 290 - GIO::Unix::SocketAddress
  [GIO] ok 291 - GIO::VFS
  [GIO] ok 292 - GIO::VolumeMonitor
  [GIO] ok 293 - GIO::ZlibCompressor
  [GIO] ok 294 - GIO::ZlibDecompressor
  ===> Testing [OK] for GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1>
  ===> Installing: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1>
  Potential difficulties:
      Declaring class 'GLib::Class::Object' inside an enclosing package of
      the same name silently replaces the package in the outer stash. This is
      legacy behavior specific to Raku 6.d and earlier; in Raku 6.e the same
      pattern installs the class as a nested package instead. Rewrite as 'unit
      class GLib::Class::Object;' in its own file (or otherwise avoid the
      package+same-named-class collision) to work the same way on either
      revision.
      at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/6CA058F1742AC15AF9A8D119F6535617F1C5EFF5 (GLib::Class::Object):103
      ------> class <HERE>GLib::Class::Object is export {
  ===> Install [OK] for GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 3min 39.581s
               CPU time consumed: 5min 2.989s
                     Memory peak: 4G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1259257-i1307749.service; invocation ID: 558be04a8d254ae68cc88a4c8c0c9761
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: GIO
  ===> Found: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1> [via Zef::Repository::Ecosystems<rea>]
  [GIO] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789704598.1259258.9978.078735028874/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/GIO/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  ===> Fetching [OK]: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1> to /home/coke/sandbox/blin/data/zef-data/tmp/1789704598.1259258.9978.078735028874/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  [GIO] Command: tar -t -f ./GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  [GIO] Command: tar -xvf ./GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz -C ../GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  ===> Extraction [OK]: GIO to /home/coke/sandbox/blin/data/zef-data/tmp/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  ===> Testing: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1>
  [GIO] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz/GIO-0.0.4 t/01-modules.t
  [GIO] 1..294
  [GIO] ok 1 - GIO
  [GIO] ok 2 - GIO::AppInfoMonitor
  [GIO] ok 3 - GIO::Application
  [GIO] ok 4 - GIO::ApplicationCommandLine
  [GIO] ok 5 - GIO::BufferedInputStream
  [GIO] ok 6 - GIO::BufferedOutputStream
  [GIO] ok 7 - GIO::Builder
  [GIO] ok 8 - GIO::BytesIcon
  [GIO] ok 9 - GIO::Cancellable
  [GIO] ok 10 - GIO::CharsetConverter
  [GIO] ok 11 - GIO::ContentType
  [GIO] ok 12 - GIO::ConverterInputStream
  [GIO] ok 13 - GIO::ConverterOutputStream
  [GIO] ok 14 - GIO::Credentials
  [GIO] ok 15 - GIO::DBus::ActionGroup
  [GIO] ok 16 - GIO::DBus::Address
  [GIO] ok 17 - GIO::DBus::AuthObserver
  [GIO] ok 18 - GIO::DBus::Connection
  [GIO] ok 19 - GIO::DBus::Error
  [GIO] ok 20 - GIO::DBus::InterfaceSkeleton
  [GIO] ok 21 - GIO::DBus::Message
  [GIO] ok 22 - GIO::DBus::MethodInvocation
  [GIO] ok 23 - GIO::DBus::ObjectManagerClient
  [GIO] ok 24 - GIO::DBus::ObjectManagerServer
  [GIO] ok 25 - GIO::DBus::ObjectProxy
  [GIO] ok 26 - GIO::DBus::ObjectSkeleton
  [GIO] ok 27 - GIO::DBus::Proxy
  [GIO] ok 28 - GIO::DBus::Raw::Address
  [GIO] ok 29 - GIO::DBus::Raw::Connection
  [GIO] ok 30 - GIO::DBus::Raw::Error
  [GIO] ok 31 - GIO::DBus::Raw::Interface
  [GIO] ok 32 - GIO::DBus::Raw::InterfaceSkeleton
  [GIO] ok 33 - GIO::DBus::Raw::Message
  [GIO] ok 34 - GIO::DBus::Raw::MethodInvocation
  [GIO] ok 35 - GIO::DBus::Raw::ObjectManager
  [GIO] ok 36 - GIO::DBus::Raw::ObjectManagerClient
  [GIO] ok 37 - GIO::DBus::Raw::ObjectManagerServer
  [GIO] ok 38 - GIO::DBus::Raw::ObjectSkeleton
  [GIO] ok 39 - GIO::DBus::Raw::Proxy
  [GIO] ok 40 - GIO::DBus::Raw::Server
  [GIO] ok 41 - GIO::DBus::Raw::Subs
  [GIO] ok 42 - GIO::DBus::Raw::Types
  [GIO] ok 43 - GIO::DBus::Raw::Utils
  [GIO] ok 44 - GIO::DBus::Roles::Interface
  [GIO] ok 45 - GIO::DBus::Roles::Object
  [GIO] ok 46 - GIO::DBus::Roles::ObjectManager
  [GIO] ok 47 - GIO::DBus::Roles::Signals::AuthObserver
  [GIO] ok 48 - GIO::DBus::Roles::Signals::Connection
  [GIO] ok 49 - GIO::DBus::Roles::Signals::InterfaceSkeleton
  [GIO] ok 50 - GIO::DBus::Roles::Signals::Object
  [GIO] ok 51 - GIO::DBus::Roles::Signals::ObjectManager
  [GIO] ok 52 - GIO::DBus::Roles::Signals::ObjectManagerClient
  [GIO] ok 53 - GIO::DBus::Roles::Signals::ObjectSkeleton
  [GIO] ok 54 - GIO::DBus::Roles::Signals::Proxy
  [GIO] ok 55 - GIO::DBus::Roles::Signals::Server
  [GIO] ok 56 - GIO::DBus::Roles::SupplyCallback
  [GIO] ok 57 - GIO::DBus::Server
  [GIO] ok 58 - GIO::DBus::Utils
  [GIO] ok 59 - GIO::DataInputStream
  [GIO] ok 60 - GIO::DataOutputStream
  [GIO] ok 61 - GIO::DesktopAppInfo
  [GIO] ok 62 - GIO::Emblem
  [GIO] ok 63 - GIO::EmblemedIcon
  [GIO] ok 64 - GIO::Enums
  [GIO] ok 65 - GIO::FileAttributeInfoList
  [GIO] ok 66 - GIO::FileAttributeMatcher
  [GIO] ok 67 - GIO::FileEnumerator
  [GIO] ok 68 - GIO::FileIOStream
  [GIO] ok 69 - GIO::FileIcon
  [GIO] ok 70 - GIO::FileInfo
  [GIO] ok 71 - GIO::FileInputStream
  [GIO] ok 72 - GIO::FileMonitor
  [GIO] ok 73 - GIO::FileMonitor::Local
  [GIO] ok 74 - GIO::FileOutputStream
  [GIO] ok 75 - GIO::FilenameCompleter
  [GIO] ok 76 - GIO::FilterInputStream
  [GIO] ok 77 - GIO::FilterOutputStream
  [GIO] ok 78 - GIO::InetAddress
  [GIO] ok 79 - GIO::InetAddressMask
  [GIO] ok 80 - GIO::InetSocketAddress
  [GIO] ok 81 - GIO::InputStream
  [GIO] ok 82 - GIO::LaunchContext
  [GIO] ok 83 - GIO::ListStore
  [GIO] ok 84 - GIO::MemoryInputStream
  [GIO] ok 85 - GIO::MemoryOutputStream
  [GIO] ok 86 - GIO::Menu
  [GIO] ok 87 - GIO::MenuAttributeIter
  [GIO] ok 88 - GIO::MenuItem
  [GIO] ok 89 - GIO::MenuLinkIter
  [GIO] ok 90 - GIO::MenuModel
  [GIO] ok 91 - GIO::MiscTypes
  [GIO] ok 92 - GIO::MountOperation
  [GIO] ok 93 - GIO::NetworkAddress
  [GIO] ok 94 - GIO::NetworkService
  [GIO] ok 95 - GIO::Notification
  [GIO] ok 96 - GIO::OutputStream
  [GIO] ok 97 - GIO::Permission
  [GIO] ok 98 - GIO::PropertyAction
  [GIO] ok 99 - GIO::ProxyAddress
  [GIO] ok 100 - GIO::ProxyAddressEnumerator
  [GIO] ok 101 - GIO::Raw::Action
  [GIO] ok 102 - GIO::Raw::ActionGroup
  [GIO] ok 103 - GIO::Raw::AppInfo
  [GIO] ok 104 - GIO::Raw::Application
  [GIO] ok 105 - GIO::Raw::ApplicationCommandLine
  [GIO] ok 106 - GIO::Raw::AsyncInitable
  [GIO] ok 107 - GIO::Raw::AsyncResult
  [GIO] ok 108 - GIO::Raw::BufferedInputStream
  [GIO] ok 109 - GIO::Raw::BufferedOutputStream
  [GIO] ok 110 - GIO::Raw::Cancellable
  [GIO] ok 111 - GIO::Raw::CharsetConverter
  [GIO] ok 112 - GIO::Raw::ContentType
  [GIO] ok 113 - GIO::Raw::Credentials
  [GIO] ok 114 - GIO::Raw::DataInputStream
  [GIO] ok 115 - GIO::Raw::DataOutputStream
  [GIO] ok 116 - GIO::Raw::DatagramBased
  [GIO] ok 117 - GIO::Raw::Definitions
  [GIO] ok 118 - GIO::Raw::DesktopAppInfo
  [GIO] ok 119 - GIO::Raw::Distro
  [GIO] ok 120 - GIO::Raw::Drive
  [GIO] ok 121 - GIO::Raw::DtlsClientConnection
  [GIO] ok 122 - GIO::Raw::DtlsConnection
  [GIO] ok 123 - GIO::Raw::Emblem
  [GIO] ok 124 - GIO::Raw::EmblemedIcon
  [GIO] ok 125 - GIO::Raw::Enums
  [GIO] ok 126 - GIO::Raw::Exports
  [GIO] ok 127 - GIO::Raw::FileAttributeInfoList
  [GIO] ok 128 - GIO::Raw::FileAttributeTypes
  [GIO] ok 129 - GIO::Raw::FileEnumerator
  [GIO] ok 130 - GIO::Raw::FileIOStream
  [GIO] ok 131 - GIO::Raw::FileInfo
  [GIO] ok 132 - GIO::Raw::FileMonitor
  [GIO] ok 133 - GIO::Raw::FileMonitor::Local
  [GIO] ok 134 - GIO::Raw::FilenameCompleter
  [GIO] ok 135 - GIO::Raw::FilterInputStream
  [GIO] ok 136 - GIO::Raw::FilterOutputStream
  [GIO] ok 137 - GIO::Raw::GFile
  [GIO] ok 138 - GIO::Raw::Icon
  [GIO] ok 139 - GIO::Raw::InetAddress
  [GIO] ok 140 - GIO::Raw::InetAddressMask
  [GIO] ok 141 - GIO::Raw::InetSocketAddress
  [GIO] ok 142 - GIO::Raw::InputStream
  [GIO] ok 143 - GIO::Raw::ListModel
  [GIO] ok 144 - GIO::Raw::ListStore
  [GIO] ok 145 - GIO::Raw::MemoryInputStream
  [GIO] ok 146 - GIO::Raw::MemoryOutputStream
  [GIO] ok 147 - GIO::Raw::Menu
  [GIO] ok 148 - GIO::Raw::MenuModel
  [GIO] ok 149 - GIO::Raw::Mount
  [GIO] ok 150 - GIO::Raw::MountOperation
  [GIO] ok 151 - GIO::Raw::NetworkAddress
  [GIO] ok 152 - GIO::Raw::NetworkMonitor
  [GIO] ok 153 - GIO::Raw::NetworkService
  [GIO] ok 154 - GIO::Raw::Notification
  [GIO] ok 155 - GIO::Raw::OutputStream
  [GIO] ok 156 - GIO::Raw::Permission
  [GIO] ok 157 - GIO::Raw::PollableInputStream
  [GIO] ok 158 - GIO::Raw::PollableOutputStream
  [GIO] ok 159 - GIO::Raw::Proxy
  [GIO] ok 160 - GIO::Raw::ProxyAddress
  [GIO] ok 161 - GIO::Raw::ProxyResolver
  [GIO] ok 162 - GIO::Raw::Quarks
  [GIO] ok 163 - GIO::Raw::Resolver
  [GIO] ok 164 - GIO::Raw::Resource
  [GIO] ok 165 - GIO::Raw::Seekable
  [GIO] ok 166 - GIO::Raw::Settings
  [GIO] ok 167 - GIO::Raw::SettingsBackend
  [GIO] ok 168 - GIO::Raw::SettingsSchema
  [GIO] ok 169 - GIO::Raw::SimpleAction
  [GIO] ok 170 - GIO::Raw::SimpleActionGroup
  [GIO] ok 171 - GIO::Raw::SimpleAsyncResult
  [GIO] ok 172 - GIO::Raw::SimpleProxyResolver
  [GIO] ok 173 - GIO::Raw::Socket
  [GIO] ok 174 - GIO::Raw::SocketAddress
  [GIO] ok 175 - GIO::Raw::SocketClient
  [GIO] ok 176 - GIO::Raw::SocketConnection
  [GIO] ok 177 - GIO::Raw::SocketControlMessage
  [GIO] ok 178 - GIO::Raw::SocketListener
  [GIO] ok 179 - GIO::Raw::SocketService
  [GIO] ok 180 - GIO::Raw::SrvTarget
  [GIO] ok 181 - GIO::Raw::Stream
  [GIO] ok 182 - GIO::Raw::Structs
  [GIO] ok 183 - GIO::Raw::Subs
  [GIO] ok 184 - GIO::Raw::Task
  [GIO] ok 185 - GIO::Raw::ThemedIcon
  [GIO] ok 186 - GIO::Raw::TlsBackend
  [GIO] ok 187 - GIO::Raw::TlsCertificate
  [GIO] ok 188 - GIO::Raw::TlsClientConnection
  [GIO] ok 189 - GIO::Raw::TlsConnection
  [GIO] ok 190 - GIO::Raw::TlsDatabase
  [GIO] ok 191 - GIO::Raw::TlsInteraction
  [GIO] ok 192 - GIO::Raw::TlsPassword
  [GIO] ok 193 - GIO::Raw::Traps
  [GIO] ok 194 - GIO::Raw::Types
  [GIO] ok 195 - GIO::Raw::UnixConnection
  [GIO] ok 196 - GIO::Raw::UnixCredentialsMessage
  [GIO] ok 197 - GIO::Raw::UnixFDList
  [GIO] ok 198 - GIO::Raw::UnixFDMessage
  [GIO] ok 199 - GIO::Raw::UnixInputStream
  [GIO] ok 200 - GIO::Raw::UnixMounts
  [GIO] ok 201 - GIO::Raw::UnixOutputStream
  [GIO] ok 202 - GIO::Raw::UnixSocketAddress
  [GIO] ok 203 - GIO::Raw::VFS
  [GIO] ok 204 - GIO::Raw::Volume
  [GIO] ok 205 - GIO::Raw::VolumeMonitor
  [GIO] ok 206 - GIO::Resolver
  [GIO] ok 207 - GIO::Resource
  [GIO] ok 208 - GIO::Roles::Action
  [GIO] ok 209 - GIO::Roles::ActionGroup
  [GIO] ok 210 - GIO::Roles::ActionMap
  [GIO] ok 211 - GIO::Roles::AppInfo
  [GIO] ok 212 - GIO::Roles::AsyncInitable
  [GIO] ok 213 - GIO::Roles::AsyncResult
  [GIO] ok 214 - GIO::Roles::Converter
  [GIO] ok 215 - GIO::Roles::DTlsClientConnection
  [GIO] ok 216 - GIO::Roles::DTlsServerConnection
  [GIO] ok 217 - GIO::Roles::DatagramBased
  [GIO] ok 218 - GIO::Roles::Drive
  [GIO] ok 219 - GIO::Roles::DtlsConnection
  [GIO] ok 220 - GIO::Roles::FileDescriptorBased
  [GIO] ok 221 - GIO::Roles::GFile
  [GIO] ok 222 - GIO::Roles::Icon
  [GIO] ok 223 - GIO::Roles::Initable
  [GIO] ok 224 - GIO::Roles::ListModel
  [GIO] ok 225 - GIO::Roles::LoadableIcon
  [GIO] ok 226 - GIO::Roles::Mount
  [GIO] ok 227 - GIO::Roles::NetworkMonitor
  [GIO] ok 228 - GIO::Roles::NetworkMonitorBase
  [GIO] ok 229 - GIO::Roles::PollableInputStream
  [GIO] ok 230 - GIO::Roles::PollableOutputStream
  [GIO] ok 231 - GIO::Roles::Proxy
  [GIO] ok 232 - GIO::Roles::ProxyResolver
  [GIO] ok 233 - GIO::Roles::RemoteActionGroup
  [GIO] ok 234 - GIO::Roles::Seekable
  [GIO] ok 235 - GIO::Roles::Signals::ActionGroup
  [GIO] ok 236 - GIO::Roles::Signals::Application
  [GIO] ok 237 - GIO::Roles::Signals::DtlsConnection
  [GIO] ok 238 - GIO::Roles::Signals::FileMonitor
  [GIO] ok 239 - GIO::Roles::Signals::ListModel
  [GIO] ok 240 - GIO::Roles::Signals::MenuModel
  [GIO] ok 241 - GIO::Roles::Signals::MountOperation
  [GIO] ok 242 - GIO::Roles::Signals::NetworkMonitor
  [GIO] ok 243 - GIO::Roles::Signals::Settings
  [GIO] ok 244 - GIO::Roles::Signals::SocketListener
  [GIO] ok 245 - GIO::Roles::Signals::SocketService
  [GIO] ok 246 - GIO::Roles::Signals::ThreadedSocketService
  [GIO] ok 247 - GIO::Roles::Signals::TlsConnection
  [GIO] ok 248 - GIO::Roles::Signals::VolumeMonitor
  [GIO] ok 249 - GIO::Roles::SocketConnectable
  [GIO] ok 250 - GIO::Roles::TlsBackend
  [GIO] ok 251 - GIO::Roles::TlsClientConnection
  [GIO] ok 252 - GIO::Roles::TlsFileDatabase
  [GIO] ok 253 - GIO::Roles::TlsServerConnection
  [GIO] ok 254 - GIO::Roles::Volume
  [GIO] ok 255 - GIO::Settings
  [GIO] ok 256 - GIO::Settings::Backend
  [GIO] ok 257 - GIO::Settings::Schema
  [GIO] ok 258 - GIO::SimpleAction
  [GIO] ok 259 - GIO::SimpleActionGroup
  [GIO] ok 260 - GIO::SimplePermission
  [GIO] ok 261 - GIO::SimpleProxyResolver
  [GIO] ok 262 - GIO::Socket
  [GIO] ok 263 - GIO::SocketAddress
  [GIO] ok 264 - GIO::SocketAddressEnumerator
  [GIO] ok 265 - GIO::SocketClient
  [GIO] ok 266 - GIO::SocketConnection
  [GIO] ok 267 - GIO::SocketControlMessage
  [GIO] ok 268 - GIO::SocketListener
  [GIO] ok 269 - GIO::SocketService
  [GIO] ok 270 - GIO::SrvTarget
  [GIO] ok 271 - GIO::Stream
  [GIO] ok 272 - GIO::Task
  [GIO] ok 273 - GIO::TcpConnection
  [GIO] ok 274 - GIO::TcpWrapperConnection
  [GIO] ok 275 - GIO::ThemedIcon
  [GIO] ok 276 - GIO::ThreadedSocketService
  [GIO] ok 277 - GIO::TlsCertificate
  [GIO] ok 278 - GIO::TlsConnection
  [GIO] ok 279 - GIO::TlsDatabase
  [GIO] ok 280 - GIO::TlsInteraction
  [GIO] ok 281 - GIO::TlsPassword
  [GIO] ok 282 - GIO::TypeManifest
  [GIO] ok 283 - GIO::Unix::Connection
  [GIO] ok 284 - GIO::Unix::CredentialsMessage
  [GIO] ok 285 - GIO::Unix::FDList
  [GIO] ok 286 - GIO::Unix::FDMessage
  [GIO] ok 287 - GIO::Unix::InputStream
  [GIO] ok 288 - GIO::Unix::Mounts
  [GIO] ok 289 - GIO::Unix::OutputStream
  [GIO] ok 290 - GIO::Unix::SocketAddress
  [GIO] ok 291 - GIO::VFS
  [GIO] ok 292 - GIO::VolumeMonitor
  [GIO] ok 293 - GIO::ZlibCompressor
  [GIO] ok 294 - GIO::ZlibDecompressor
  ===> Testing [OK] for GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1>
  ===> Installing: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1>
  ===> Install [FAIL] for GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1>: ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/52C01D560A2FDF37C89638F865165F50944209FE (GIO)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/B3DF2080E9C47497139F66F002DF654B59CC04A1 (GIO::AppInfoMonitor)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/ED0C5738485BD7549FE65E5169CC8CA5A9961294 (GIO::Raw::Types)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions)
  Can only use : as invocant marker in a signature after the first parameter
  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions):133
  ------>   method new (<HERE> :

  at /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/ED0C5738485BD7549FE65E5169CC8CA5A9961294 (GIO::Raw::Types):13

  at /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/B3DF2080E9C47497139F66F002DF654B59CC04A1 (GIO::AppInfoMonitor):5

  at /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/52C01D560A2FDF37C89638F865165F50944209FE (GIO):3

  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/52C01D560A2FDF37C89638F865165F50944209FE (GIO)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/B3DF2080E9C47497139F66F002DF654B59CC04A1 (GIO::AppInfoMonitor)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/ED0C5738485BD7549FE65E5169CC8CA5A9961294 (GIO::Raw::Types)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions)
  Can only use : as invocant marker in a signature after the first parameter
  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions):133
  ------>   method new (<HERE> :

  at /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/ED0C5738485BD7549FE65E5169CC8CA5A9961294 (GIO::Raw::Types):13

  at /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/B3DF2080E9C47497139F66F002DF654B59CC04A1 (GIO::AppInfoMonitor):5

  at /home/coke/sandbox/blin/installed/GIO_cpan:CBWOOD_0.0.4_1/sources/52C01D560A2FDF37C89638F865165F50944209FE (GIO):3

            Finished with result: exit-code
  Main processes terminated with: code=exited, status=1/FAILURE
                 Service runtime: 22.568s
               CPU time consumed: 28.574s
                     Memory peak: 2.2G (swap: 0B)

  ```
  </details>
* [ ] [GLib](https://raku.land/cpan:CBWOOD/GLib) – Fail, Bisected: [6357ccf](https://github.com/rakudo/rakudo/commit/6357ccf97f2c4b1dd1067bf4f50b6cdcfdb78373)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1134937-i1064134.service; invocation ID: 103febc063c341eea98c4bba052f59c4
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: GLib
  ===> Found: GLib:ver<0.0.11>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [GLib] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789701147.1134944.9188.913109196386/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/GLib/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: GLib:ver<0.0.11>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789701147.1134944.9188.913109196386/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
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
  Potential difficulties:
      Declaring class 'GLib::Class::Object' inside an enclosing package of
      the same name silently replaces the package in the outer stash. This is
      legacy behavior specific to Raku 6.d and earlier; in Raku 6.e the same
      pattern installs the class as a nested package instead. Rewrite as 'unit
      class GLib::Class::Object;' in its own file (or otherwise avoid the
      package+same-named-class collision) to work the same way on either
      revision.
      at /tmp/zXi1mSwCaD/sources/6CA058F1742AC15AF9A8D119F6535617F1C5EFF5 (GLib::Class::Object):103
      ------> class <HERE>GLib::Class::Object is export {
  ===> Install [OK] for GLib:ver<0.0.11>:auth<cpan:CBWOOD>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 16min 979ms
               CPU time consumed: 15min 15.665s
                     Memory peak: 2.3G (swap: 1.3G)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1128315-i1137166.service; invocation ID: 1306ba5213b34e47857a0f36fa91b306
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: GLib
  ===> Found: GLib:ver<0.0.11>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [GLib] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789700956.1128325.7774.788904124121/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/GLib/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: GLib:ver<0.0.11>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789700956.1128325.7774.788904124121/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [GLib] Command: tar -t -f ./GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [GLib] Command: tar -xvf ./GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz -C ../GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Extraction [OK]: GLib to /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Testing: GLib:ver<0.0.11>:auth<cpan:CBWOOD>
  [GLib] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/00-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs)
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions)
  [GLib] Can only use : as invocant marker in a signature after the first parameter
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions):133
  [GLib] ------>   method new (<HERE> :
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs):10
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00-struct-sizes.t:7
  [GLib] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/00b-class-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00b-class-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs)
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions)
  [GLib] Can only use : as invocant marker in a signature after the first parameter
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions):133
  [GLib] ------>   method new (<HERE> :
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs):10
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00b-class-struct-sizes.t:7
  [GLib] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/01-modules.t
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
  ===> Install [FAIL] for GLib:ver<0.0.11>:auth<cpan:CBWOOD>: ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/F0C9879CCDBF598DAF96BD37D9F1CE815D9D1FE3 (GLib)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/E460938D8BE5E569C3EC400A0BA8E44BE67D41D3 (GLib::Array)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/1EA21A570A7AEB653962EFCBE486E61D713CC8D2 (GLib::Raw::Types)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions)
  Can only use : as invocant marker in a signature after the first parameter
  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions):133
  ------>   method new (<HERE> :

  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/1EA21A570A7AEB653962EFCBE486E61D713CC8D2 (GLib::Raw::Types):10

  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/E460938D8BE5E569C3EC400A0BA8E44BE67D41D3 (GLib::Array):5

  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/F0C9879CCDBF598DAF96BD37D9F1CE815D9D1FE3 (GLib):1

  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/F0C9879CCDBF598DAF96BD37D9F1CE815D9D1FE3 (GLib)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/E460938D8BE5E569C3EC400A0BA8E44BE67D41D3 (GLib::Array)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/1EA21A570A7AEB653962EFCBE486E61D713CC8D2 (GLib::Raw::Types)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions)
  Can only use : as invocant marker in a signature after the first parameter
  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions):133
  ------>   method new (<HERE> :

  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/1EA21A570A7AEB653962EFCBE486E61D713CC8D2 (GLib::Raw::Types):10

  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/E460938D8BE5E569C3EC400A0BA8E44BE67D41D3 (GLib::Array):5

  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/F0C9879CCDBF598DAF96BD37D9F1CE815D9D1FE3 (GLib):1

            Finished with result: exit-code
  Main processes terminated with: code=exited, status=1/FAILURE
                 Service runtime: 2min 49.504s
               CPU time consumed: 2min 42.232s
                     Memory peak: 2.4G (swap: 324.6M)

  ```
  </details>
* [ ] [JSON::GLib::Node](https://raku.land/cpan:CBWOOD/JSON::GLib::Node) – Fail, Bisected: [6357ccf](https://github.com/rakudo/rakudo/commit/6357ccf97f2c4b1dd1067bf4f50b6cdcfdb78373)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1273930-i1261135.service; invocation ID: 95b57e40193f410f80b102c73cfa5715
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: JSON::GLib::Node
  ===> Found: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [JSON::GLib::Node] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789706480.1273931.9885.270775139752/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/J/JSON%3A%3AGLib%3A%3ANode/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789706480.1273931.9885.270775139752/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
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
  Potential difficulties:
      Declaring class 'GLib::Class::Object' inside an enclosing package of
      the same name silently replaces the package in the outer stash. This is
      legacy behavior specific to Raku 6.d and earlier; in Raku 6.e the same
      pattern installs the class as a nested package instead. Rewrite as 'unit
      class GLib::Class::Object;' in its own file (or otherwise avoid the
      package+same-named-class collision) to work the same way on either
      revision.
      at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/6CA058F1742AC15AF9A8D119F6535617F1C5EFF5 (GLib::Class::Object):103
      ------> class <HERE>GLib::Class::Object is export {
  ===> Install [OK] for JSON::GLib::Node:ver<0.0.1>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 44.034s
               CPU time consumed: 2min 27.692s
                     Memory peak: 3.1G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1273782-i1327913.service; invocation ID: 04011309cbe04caaa411422dfed57c9b
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: JSON::GLib::Node
  ===> Found: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [JSON::GLib::Node] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789706461.1273783.5383.203910326105/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/J/JSON%3A%3AGLib%3A%3ANode/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789706461.1273783.5383.203910326105/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [JSON::GLib::Node] Command: tar -t -f ./JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [JSON::GLib::Node] Command: tar -xvf ./JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz -C ../JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Extraction [OK]: JSON::GLib::Node to /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Testing: JSON::GLib::Node:ver<0.0.1>
  [JSON::GLib::Node] Command: /tmp/whateverable/rakudo-moar/7a3abc5ababa5842e6346438d5e0675f2599ecb3/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/JSON-GLib-Node-0.0.1 t/01-basic.t
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
  ===> Install [FAIL] for JSON::GLib::Node:ver<0.0.1>: ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/JSON::GLib::Node_cpan:CBWOOD_0.0.1_0/sources/3DC40796A7852D357A41C0C1D927A021704BCC8B (JSON::GLib::Array)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/0C336C09131938C526DC4C924AD2A0CDE35A600C (GLib::GList)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/1EA21A570A7AEB653962EFCBE486E61D713CC8D2 (GLib::Raw::Types)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions)
  Can only use : as invocant marker in a signature after the first parameter
  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions):133
  ------>   method new (<HERE> :

  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/1EA21A570A7AEB653962EFCBE486E61D713CC8D2 (GLib::Raw::Types):10

  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/0C336C09131938C526DC4C924AD2A0CDE35A600C (GLib::GList):6

  at /home/coke/sandbox/blin/installed/JSON::GLib::Node_cpan:CBWOOD_0.0.1_0/sources/3DC40796A7852D357A41C0C1D927A021704BCC8B (JSON::GLib::Array):7

  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/JSON::GLib::Node_cpan:CBWOOD_0.0.1_0/sources/3DC40796A7852D357A41C0C1D927A021704BCC8B (JSON::GLib::Array)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/0C336C09131938C526DC4C924AD2A0CDE35A600C (GLib::GList)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/1EA21A570A7AEB653962EFCBE486E61D713CC8D2 (GLib::Raw::Types)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions)
  Can only use : as invocant marker in a signature after the first parameter
  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/3E6796E3681A9E7317502A97903E4856F1C3F0B1 (GLib::Raw::Exceptions):133
  ------>   method new (<HERE> :

  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/1EA21A570A7AEB653962EFCBE486E61D713CC8D2 (GLib::Raw::Types):10

  at /home/coke/sandbox/blin/installed/GLib_cpan:CBWOOD_0.0.11_0/sources/0C336C09131938C526DC4C924AD2A0CDE35A600C (GLib::GList):6

  at /home/coke/sandbox/blin/installed/JSON::GLib::Node_cpan:CBWOOD_0.0.1_0/sources/3DC40796A7852D357A41C0C1D927A021704BCC8B (JSON::GLib::Array):7

            Finished with result: exit-code
  Main processes terminated with: code=exited, status=1/FAILURE
                 Service runtime: 19.699s
               CPU time consumed: 26.356s
                     Memory peak: 2.1G (swap: 0B)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| UnhandledException        |     1 | [Foo:: Foo](https://raku.land/github:AlexDaniel/Foo:: Foo) |
| Flapper                   |     1 | [Proc::Q](https://raku.land//Proc::Q) |
| Fail                      |     5 | [GIO](https://raku.land/cpan:CBWOOD/GIO) [GLib](https://raku.land/cpan:CBWOOD/GLib) [JSON::GLib::Node](https://raku.land/cpan:CBWOOD/JSON::GLib::Node) [Polyglot::Regexen](https://raku.land/zef:guifa/Polyglot::Regexen) [Terminal::UI](https://raku.land/zef:bduggan/Terminal::UI) |
| InstallableButUntested    |    10 | [HTTP::Server::Async](https://raku.land/zef:raku-community-modules/HTTP::Server::Async) [IO::Socket::Async::SSL](https://raku.land/zef:raku-community-modules/IO::Socket::Async::SSL) [IRC::Client](https://raku.land/zef:lizmat/IRC::Client) [Log::Minimal](https://raku.land//Log::Minimal) [Russian](https://raku.land/zef:slavenskoj/Russian) [Text::Markdown::Discount](https://raku.land/github:hartenfels/Text::Markdown::Discount) [Time::Duration](https://raku.land/zef:masukomi/Time::Duration) [Toaster](https://raku.land//Toaster) [Uzu](https://raku.land/cpan:SACOMO/Uzu) [Web::Scraper](https://raku.land/zef:tony-o/Web::Scraper) |
| MissingDependency         |    11 | [App::Ebread](https://raku.land/zef:samy/App::Ebread) [App::Perl6LangServer](https://raku.land/cpan:AZAWAWI/App::Perl6LangServer) [Chemistry::Elements](https://raku.land/github:briandfoy/Chemistry::Elements) [DBIx::NamedQueries](https://raku.land/cpan:MZIESCHA/DBIx::NamedQueries) [Ethelia](https://raku.land/zef:knarkhov/Ethelia) [Learn::Raku::With](https://raku.land/zef:codesections/Learn::Raku::With) [META6::To::Man](https://raku.land/cpan:TBROWDER/META6::To::Man) [Pakku](https://raku.land/zef:hythm/Pakku) [Perl6::Tracer](https://raku.land/github:jaffa4/Perl6::Tracer) [Task::Galaxy](https://raku.land//Task::Galaxy) [Touch](https://raku.land/zef:rir/Touch) |
| ZefFailure                |    13 | [BDD::Behave](https://raku.land/zef:gdonald/BDD::Behave) [Concurrent::BoundedChannel](https://raku.land/zef:raku-community-modules/Concurrent::BoundedChannel) [Cro::RPC::JSON](https://raku.land/zef:vrurg/Cro::RPC::JSON) [Cro::ZeroMQ](https://raku.land/cpan:JNTHN/Cro::ZeroMQ) [Gnome::Gtk4](https://raku.land/zef:martimm/Gnome::Gtk4) [ParaSeq](https://raku.land/zef:lizmat/ParaSeq) [Proc::ZMQed](https://raku.land/zef:antononcube/Proc::ZMQed) [Sitemap](https://raku.land/zef:sasha/Sitemap) [Syndicate](https://raku.land/zef:sasha/Syndicate) [TXN](https://raku.land//TXN) [TXN::Parser](https://raku.land//TXN::Parser) [TXN::Remarshal](https://raku.land//TXN::Remarshal) [cro](https://raku.land/zef:cro/cro) |
| CyclicDependency          |    48 | ⋯                         |
| AlwaysFail                |   781 | ⋯                         |
| OK                        |  1661 | ⋯                         |



This run started on 2026-09-18T04:54:25Z and finished in ≈5 hours.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
