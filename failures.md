[Blin](https://github.com/Raku/Blin) results between 2026.09 ([9a94801](https://github.com/rakudo/rakudo/commit/9a94801c154543573d926e6258e062f3c3782635)) and 69f2b375f4 ([69f2b37](https://github.com/rakudo/rakudo/commit/69f2b375f4c4f187d2ea00f9603c88f104486bfc)):

* [ ] [Crust::Middleware::Syslog](https://raku.land//Crust::Middleware::Syslog) – Fail, Bisected: [69f2b37](https://github.com/rakudo/rakudo/commit/69f2b375f4c4f187d2ea00f9603c88f104486bfc)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2705570-i6916426.service; invocation ID: d382de583da2443cba3d9f56c611b186
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Crust::Middleware::Syslog
  ===> Found: Crust::Middleware::Syslog:ver<1.0.0> [via Zef::Repository::Ecosystems<rea>]
  [Crust::Middleware::Syslog] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1790704328.2705571.6783.542134108621/Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/C/Crust%3A%3AMiddleware%3A%3ASyslog/Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz
  ===> Fetching [OK]: Crust::Middleware::Syslog:ver<1.0.0> to /home/coke/sandbox/blin/data/zef-data/tmp/1790704328.2705571.6783.542134108621/Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz
  [Crust::Middleware::Syslog] Command: tar -t -f ./Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz
  [Crust::Middleware::Syslog] Command: tar -xvf ./Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz -C ../Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz
  ===> Extraction [OK]: Crust::Middleware::Syslog to /home/coke/sandbox/blin/data/zef-data/tmp/Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz
  ===> Testing: Crust::Middleware::Syslog:ver<1.0.0>
  [Crust::Middleware::Syslog] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz/P6-Crust-Middleware-Syslog-master t/01-basic.t
  [Crust::Middleware::Syslog] 1..1
  [Crust::Middleware::Syslog] ok 1 - able to load
  ===> Testing [OK] for Crust::Middleware::Syslog:ver<1.0.0>
  ===> Installing: Crust::Middleware::Syslog:ver<1.0.0>
  ===> Install [OK] for Crust::Middleware::Syslog:ver<1.0.0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 4min 39.077s
               CPU time consumed: 2min 18.135s
                     Memory peak: 1.2G (swap: 514.5M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2701295-i6778621.service; invocation ID: 25da769bc67042d7817f094ddf4cd9e2
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Crust::Middleware::Syslog
  ===> Found: Crust::Middleware::Syslog:ver<1.0.0> [via Zef::Repository::Ecosystems<rea>]
  [Crust::Middleware::Syslog] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1790704062.2701330.64.91904683489702/Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/C/Crust%3A%3AMiddleware%3A%3ASyslog/Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz
  ===> Fetching [OK]: Crust::Middleware::Syslog:ver<1.0.0> to /home/coke/sandbox/blin/data/zef-data/tmp/1790704062.2701330.64.91904683489702/Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz
  [Crust::Middleware::Syslog] Command: tar -t -f ./Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz
  [Crust::Middleware::Syslog] Command: tar -xvf ./Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz -C ../Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz
  ===> Extraction [OK]: Crust::Middleware::Syslog to /home/coke/sandbox/blin/data/zef-data/tmp/Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz
  ===> Testing: Crust::Middleware::Syslog:ver<1.0.0>
  [Crust::Middleware::Syslog] Command: /tmp/whateverable/rakudo-moar/69f2b375f4c4f187d2ea00f9603c88f104486bfc/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Crust%3A%3AMiddleware%3A%3ASyslog%3Aver%3C1.0.0%3E%3Aauth%3Cgithub%3Aretupmoca%3E.tar.gz/P6-Crust-Middleware-Syslog-master t/01-basic.t
  [Crust::Middleware::Syslog] 1..1
  [Crust::Middleware::Syslog] ok 1 - able to load
  ===> Testing [OK] for Crust::Middleware::Syslog:ver<1.0.0>
  ===> Installing: Crust::Middleware::Syslog:ver<1.0.0>
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 5min 34.959s
               CPU time consumed: 2min 3.998s
                     Memory peak: 1G (swap: 418.9M)

  ```
  </details>
* [ ] [Mux](https://raku.land/zef:tony-o/Mux) – Fail, Bisected: [69f2b37](https://github.com/rakudo/rakudo/commit/69f2b375f4c4f187d2ea00f9603c88f104486bfc)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2258804-i6368617.service; invocation ID: 4b04ecfab2814d658d228e0db2e702d4
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Mux
  ===> Found: Mux:ver<0.0.4>:auth<zef:tony-o> [via Zef::Repository::Ecosystems<fez>]
  [Mux] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1790690069.2258808.867.7974444318381/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz https://360.zef.pm/M/UX/MUX/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz
  ===> Fetching [OK]: Mux:ver<0.0.4>:auth<zef:tony-o> to /home/coke/sandbox/blin/data/zef-data/tmp/1790690069.2258808.867.7974444318381/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz
  [Mux] Command: tar -t -f ./0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz
  [Mux] Command: tar -xvf ./0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz -C ../0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz
  ===> Extraction [OK]: Mux to /home/coke/sandbox/blin/data/zef-data/tmp/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz
  ===> Testing: Mux:ver<0.0.4>:auth<zef:tony-o>
  [Mux] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz t/01-full.t
  [Mux] 1..9
  [Mux] ok 1 - correct emission
  [Mux] ok 2 - correct emission
  [Mux] ok 3 - correct emission
  [Mux] ok 4 - correct emission
  [Mux] ok 5 - correct emission
  [Mux] ok 6 - should not receive more values than channels during sleeping
  [Mux] ok 7 - correct emission
  [Mux] ok 8 - correct emission
  [Mux] ok 9 - correct emission
  [Mux] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz t/02-good-drain.t
  [Mux] 1..7
  [Mux] ==> DEMUX 1
  [Mux] ok 1 - correct emission (got: 1, expected: 1)
  [Mux] ==> DEMUX 1
  [Mux] ok 2 - correct emission (got: 1, expected: 1)
  [Mux] ==> drain !fed
  [Mux] ok 3 - should have one more expecting in drain
  [Mux] ==> DEMUX 1
  [Mux] ok 4 - correct emission (got: 1, expected: 1)
  [Mux] ==> drain fed
  [Mux] ok 5 - should have no more expecting in drain
  [Mux] ==> drain fed
  [Mux] ok 6 - should have no more expecting in drain
  [Mux] ==> blocked
  [Mux] ok 7 - should not be expecting anything else at end
  ===> Testing [OK] for Mux:ver<0.0.4>:auth<zef:tony-o>
  ===> Installing: Mux:ver<0.0.4>:auth<zef:tony-o>
  ===> Install [OK] for Mux:ver<0.0.4>:auth<zef:tony-o>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 25.839s
               CPU time consumed: 1min 54.734s
                     Memory peak: 953.9M (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2254386-i6488690.service; invocation ID: ec24ca084abd4e9eb6f86cb8ab474aa3
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Mux
  ===> Found: Mux:ver<0.0.4>:auth<zef:tony-o> [via Zef::Repository::Ecosystems<fez>]
  [Mux] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1790689922.2254387.619.7314993200321/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz https://360.zef.pm/M/UX/MUX/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz
  ===> Fetching [OK]: Mux:ver<0.0.4>:auth<zef:tony-o> to /home/coke/sandbox/blin/data/zef-data/tmp/1790689922.2254387.619.7314993200321/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz
  [Mux] Command: tar -t -f ./0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz
  [Mux] Command: tar -xvf ./0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz -C ../0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz
  ===> Extraction [OK]: Mux to /home/coke/sandbox/blin/data/zef-data/tmp/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz
  ===> Testing: Mux:ver<0.0.4>:auth<zef:tony-o>
  [Mux] Command: /tmp/whateverable/rakudo-moar/69f2b375f4c4f187d2ea00f9603c88f104486bfc/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz t/01-full.t
  [Mux] 1..9
  [Mux] not ok 2 - correct emission
  [Mux] not ok 2 - correct emission
  [Mux] # Failed test 'correct emission'
  [Mux] # at t/01-full.t line 15
  [Mux] # Failed test 'correct emission'
  [Mux] # at t/01-full.t line 15
  [Mux] # expected: '1'
  [Mux] #      got: '10'
  [Mux] # expected: '10'
  [Mux] #      got: '1'
  [Mux] ok 3 - correct emission
  [Mux] ok 4 - correct emission
  [Mux] ok 5 - correct emission
  [Mux] ok 6 - should not receive more values than channels during sleeping
  [Mux] ok 7 - correct emission
  [Mux] ok 8 - correct emission
  [Mux] ok 9 - correct emission
  [Mux] # You failed 2 tests of 9
  [Mux] Command: /tmp/whateverable/rakudo-moar/69f2b375f4c4f187d2ea00f9603c88f104486bfc/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0d1f727bc7e85bccaccf3e8b3c380f307037eb39.tar.gz t/02-good-drain.t
  [Mux] 1..7
  [Mux] ==> DEMUX 1
  [Mux] ok 1 - correct emission (got: 1, expected: 1)
  [Mux] ==> DEMUX 1
  [Mux] ok 2 - correct emission (got: 1, expected: 1)
  [Mux] ==> drain !fed
  [Mux] ok 3 - should have one more expecting in drain
  [Mux] ==> DEMUX 1
  [Mux] ok 4 - correct emission (got: 1, expected: 1)
  [Mux] ==> drain fed
  [Mux] ok 5 - should have no more expecting in drain
  [Mux] ==> drain fed
  [Mux] ok 6 - should have no more expecting in drain
  [Mux] ==> blocked
  [Mux] ok 7 - should not be expecting anything else at end
  ===> Testing [FAIL]: Mux:ver<0.0.4>:auth<zef:tony-o>
  [Mux] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Mux:ver<0.0.4>:auth<zef:tony-o>
  ===> Install [OK] for Mux:ver<0.0.4>:auth<zef:tony-o>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 20.130s
               CPU time consumed: 1min 45.493s
                     Memory peak: 1012.8M (swap: 0B)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| UnhandledException        |     1 | [Foo:: Foo](https://raku.land/github:AlexDaniel/Foo:: Foo) |
| Fail                      |     2 | [Crust::Middleware::Syslog](https://raku.land//Crust::Middleware::Syslog) [Mux](https://raku.land/zef:tony-o/Mux) |
| Flapper                   |     3 | [FastCGI::NativeCall](https://raku.land/zef:jonathanstowe/FastCGI::NativeCall) [Math::NIntegrate](https://raku.land/zef:antononcube/Math::NIntegrate) [Net::DNS](https://raku.land/zef:rbt/Net::DNS) |
| MissingDependency         |    11 | [App::Ebread](https://raku.land/zef:samy/App::Ebread) [App::Perl6LangServer](https://raku.land/cpan:AZAWAWI/App::Perl6LangServer) [Chemistry::Elements](https://raku.land/github:briandfoy/Chemistry::Elements) [DBIx::NamedQueries](https://raku.land/cpan:MZIESCHA/DBIx::NamedQueries) [Ethelia](https://raku.land/zef:knarkhov/Ethelia) [Learn::Raku::With](https://raku.land/zef:codesections/Learn::Raku::With) [META6::To::Man](https://raku.land/cpan:TBROWDER/META6::To::Man) [Pakku](https://raku.land/zef:hythm/Pakku) [Perl6::Tracer](https://raku.land/github:jaffa4/Perl6::Tracer) [Task::Galaxy](https://raku.land//Task::Galaxy) [Touch](https://raku.land/zef:rir/Touch) |
| InstallableButUntested    |    13 | [Control::Bail](https://raku.land//Control::Bail) [HTTP::Server::Async](https://raku.land/zef:raku-community-modules/HTTP::Server::Async) [IO::Socket::Async::SSL](https://raku.land/zef:raku-community-modules/IO::Socket::Async::SSL) [IRC::Client](https://raku.land/zef:lizmat/IRC::Client) [Log::Minimal](https://raku.land//Log::Minimal) [P5__DATA__](https://raku.land/cpan:ELIZABETH/P5__DATA__) [Russian](https://raku.land/zef:slavenskoj/Russian) [Sustenance](https://raku.land//Sustenance) [Text::Markdown::Discount](https://raku.land/github:hartenfels/Text::Markdown::Discount) [Time::Duration](https://raku.land/zef:masukomi/Time::Duration) [Toaster](https://raku.land//Toaster) [Uzu](https://raku.land/cpan:SACOMO/Uzu) [Web::Scraper](https://raku.land/zef:tony-o/Web::Scraper) |
| ZefFailure                |    14 | [BDD::Behave](https://raku.land/zef:gdonald/BDD::Behave) [Cro::ZeroMQ](https://raku.land/cpan:JNTHN/Cro::ZeroMQ) [Net::BGP](https://raku.land/zef:jmaslak/Net::BGP) [ORM::ActiveRecord](https://raku.land/zef:gdonald/ORM::ActiveRecord) [PDF::Class](https://raku.land/zef:dwarring/PDF::Class) [ParaSeq](https://raku.land/zef:lizmat/ParaSeq) [Proc::ZMQed](https://raku.land/zef:antononcube/Proc::ZMQed) [Sitemap](https://raku.land/zef:sasha/Sitemap) [Syndicate](https://raku.land/zef:sasha/Syndicate) [TXN](https://raku.land//TXN) [TXN::Parser](https://raku.land//TXN::Parser) [TXN::Remarshal](https://raku.land//TXN::Remarshal) [UNIX::Daemonize](https://raku.land//UNIX::Daemonize) [WAT](https://raku.land/zef:nige123/WAT) |
| CyclicDependency          |    48 | ⋯                         |
| AlwaysFail                |   821 | ⋯                         |
| OK                        |  1625 | ⋯                         |



This run started on 2026-09-29T18:31:43Z and finished in ≈5 hours.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
