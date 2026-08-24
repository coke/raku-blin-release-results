[Blin](https://github.com/Raku/Blin) results between 2026.08 ([24e6e53](https://github.com/rakudo/rakudo/commit/24e6e5312f2868680413b0597aef8772f6b5bcea)) and HEAD ([561c512](https://github.com/rakudo/rakudo/commit/561c5121dbf8d84c5ed815e7e57831707e58d713)):

* [ ] [Cro::HTTP::Test](https://raku.land/cpan:JNTHN/Cro::HTTP::Test) – Fail, Bisected: [adf522f](https://github.com/rakudo/rakudo/commit/adf522f2413c4f0746feecf84d7575595cc38b9c)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p482637-i510129.service; invocation ID: 87410f7d4b0e47b9bb373508945f4c7c
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Cro::HTTP::Test
  ===> Found: Cro::HTTP::Test:ver<0.8.1>:auth<cpan:JNTHN> [via Zef::Repository::Ecosystems<rea>]
  [Cro::HTTP::Test] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787606488.482641.5960.004132149692/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/C/Cro%3A%3AHTTP%3A%3ATest/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz
  ===> Fetching [OK]: Cro::HTTP::Test:ver<0.8.1>:auth<cpan:JNTHN> to /home/coke/sandbox/blin/data/zef-data/tmp/1787606488.482641.5960.004132149692/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz
  [Cro::HTTP::Test] Command: tar -t -f ./Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz
  [Cro::HTTP::Test] Command: tar -xvf ./Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz -C ../Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz
  ===> Extraction [OK]: Cro::HTTP::Test to /home/coke/sandbox/blin/data/zef-data/tmp/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz
  ===> Testing: Cro::HTTP::Test:ver<0.8.1>
  [Cro::HTTP::Test] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz/Cro-HTTP-Test t/checks.t
  [Cro::HTTP::Test] 1..20
  [Cro::HTTP::Test] # Subtest: GET /text
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 1 - GET /text
  [Cro::HTTP::Test] # Subtest: GET /text
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 2 - GET /text
  [Cro::HTTP::Test] # Subtest: GET /text
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 3 - GET /text
  [Cro::HTTP::Test] # Subtest: GET /text
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 4 - GET /text
  [Cro::HTTP::Test] # Subtest: GET /binary
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 5 - GET /binary
  [Cro::HTTP::Test] # Subtest: GET /binary
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 6 - GET /binary
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-foo header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 7 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-foo header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 8 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-foo header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 9 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-foo header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 10 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-foo header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 11 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-foo header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 12 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-bar header
  [Cro::HTTP::Test]     ok 2 - X-foo header
  [Cro::HTTP::Test]     1..2
  [Cro::HTTP::Test] ok 13 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-foo header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 14 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-foo header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 15 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-foo header
  [Cro::HTTP::Test]     ok 2 - X-bar header
  [Cro::HTTP::Test]     1..2
  [Cro::HTTP::Test] ok 16 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-bar header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 17 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-bar header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 18 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-bar header
  [Cro::HTTP::Test]     ok 2 - X-foo header
  [Cro::HTTP::Test]     1..2
  [Cro::HTTP::Test] ok 19 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - X-bar header
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 20 - GET /headers
  [Cro::HTTP::Test] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz/Cro-HTTP-Test t/fake-auth.t
  [Cro::HTTP::Test] 1..9
  [Cro::HTTP::Test] # Subtest: GET /public
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 1 - GET /public
  [Cro::HTTP::Test] # Subtest: GET /secret
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 2 - GET /secret
  [Cro::HTTP::Test] # Subtest: GET /admin
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 3 - GET /admin
  [Cro::HTTP::Test] # Subtest: GET /public
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 4 - GET /public
  [Cro::HTTP::Test] # Subtest: GET /secret
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 5 - GET /secret
  [Cro::HTTP::Test] # Subtest: GET /admin
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 6 - GET /admin
  [Cro::HTTP::Test] # Subtest: GET /public
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 7 - GET /public
  [Cro::HTTP::Test] # Subtest: GET /secret
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 8 - GET /secret
  [Cro::HTTP::Test] # Subtest: GET /admin
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 9 - GET /admin
  [Cro::HTTP::Test] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz/Cro-HTTP-Test t/fake-peer.t
  [Cro::HTTP::Test] # Subtest: GET /
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is recognized as a JSON one
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 1 - GET /
  [Cro::HTTP::Test] 1..1
  [Cro::HTTP::Test] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz/Cro-HTTP-Test t/http2.t
  [Cro::HTTP::Test] 1..4
  [Cro::HTTP::Test] # Subtest: GET /
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 1 - GET /
  [Cro::HTTP::Test] # Subtest: POST /add
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is recognized as a JSON one
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 2 - POST /add
  [Cro::HTTP::Test] # Subtest: POST /add
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 3 - POST /add
  [Cro::HTTP::Test] # Subtest: GET /add
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 4 - GET /add
  [Cro::HTTP::Test] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz/Cro-HTTP-Test t/synopsis.t
  [Cro::HTTP::Test] 1..4
  [Cro::HTTP::Test] # Subtest: GET /
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 1 - GET /
  [Cro::HTTP::Test] # Subtest: POST /add
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is recognized as a JSON one
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 2 - POST /add
  [Cro::HTTP::Test] # Subtest: POST /add
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 3 - POST /add
  [Cro::HTTP::Test] # Subtest: GET /add
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 4 - GET /add
  [Cro::HTTP::Test] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz/Cro-HTTP-Test t/test-given.t
  [Cro::HTTP::Test] 1..14
  [Cro::HTTP::Test] # Subtest: GET /cookies
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 1 - GET /cookies
  [Cro::HTTP::Test] # Subtest: GET /cookies
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 2 - GET /cookies
  [Cro::HTTP::Test] # Subtest: GET /cookies
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 3 - GET /cookies
  [Cro::HTTP::Test] # Subtest: GET /cookies
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 4 - GET /cookies
  [Cro::HTTP::Test] # Subtest: GET /cookies
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 5 - GET /cookies
  [Cro::HTTP::Test] # Subtest: GET /cookies
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 6 - GET /cookies
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 7 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 8 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 9 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 10 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 11 - GET /headers
  [Cro::HTTP::Test] # Subtest: GET /headers
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 12 - GET /headers
  [Cro::HTTP::Test] # Subtest: PUT /content
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 13 - PUT /content
  [Cro::HTTP::Test] # Subtest: PUT /content
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 14 - PUT /content
  [Cro::HTTP::Test] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz/Cro-HTTP-Test t/test-uri.t
  [Cro::HTTP::Test] 1..5
  [Cro::HTTP::Test] # Subtest: GET /
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is acceptable
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 1 - GET /
  [Cro::HTTP::Test] # Subtest: POST /add
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is recognized as a JSON one
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 2 - POST /add
  [Cro::HTTP::Test] # Subtest: POST /add
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     ok 2 - Content type is recognized as a JSON one
  [Cro::HTTP::Test]     ok 3 - Body is acceptable
  [Cro::HTTP::Test]     1..3
  [Cro::HTTP::Test] ok 3 - POST /add
  [Cro::HTTP::Test] # Subtest: POST /add
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 4 - POST /add
  [Cro::HTTP::Test] # Subtest: GET /add
  [Cro::HTTP::Test]     ok 1 - Status is acceptable
  [Cro::HTTP::Test]     1..1
  [Cro::HTTP::Test] ok 5 - GET /add
  ===> Testing [OK] for Cro::HTTP::Test:ver<0.8.1>
  ===> Installing: Cro::HTTP::Test:ver<0.8.1>
  ===> Install [OK] for Cro::HTTP::Test:ver<0.8.1>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 7min 34.896s
               CPU time consumed: 5min 23.608s
                     Memory peak: 2.2G (swap: 1.3G)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p475334-i512216.service; invocation ID: 657de9afac7d41579e52cce3a7a5859a
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Cro::HTTP::Test
  ===> Found: Cro::HTTP::Test:ver<0.8.1>:auth<cpan:JNTHN> [via Zef::Repository::Ecosystems<rea>]
  [Cro::HTTP::Test] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787606273.475347.5302.354247433723/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/C/Cro%3A%3AHTTP%3A%3ATest/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz
  ===> Fetching [OK]: Cro::HTTP::Test:ver<0.8.1>:auth<cpan:JNTHN> to /home/coke/sandbox/blin/data/zef-data/tmp/1787606273.475347.5302.354247433723/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz
  [Cro::HTTP::Test] Command: tar -t -f ./Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz
  [Cro::HTTP::Test] Command: tar -xvf ./Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz -C ../Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz
  ===> Extraction [OK]: Cro::HTTP::Test to /home/coke/sandbox/blin/data/zef-data/tmp/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz
  ===> Testing: Cro::HTTP::Test:ver<0.8.1>
  [Cro::HTTP::Test] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Cro%3A%3AHTTP%3A%3ATest%3Aver%3C0.8.1%3E%3Aauth%3Ccpan%3AJNTHN%3E.tar.gz/Cro-HTTP-Test t/checks.t
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 3min 23.147s
               CPU time consumed: 2min 38.950s
                     Memory peak: 2.1G (swap: 877.6M)

  ```
  </details>
* [ ] [API::USNavalObservatory](https://raku.land//API::USNavalObservatory) – Fail, Bisected: [af214e7](https://github.com/rakudo/rakudo/commit/af214e70ebc4f10a02dc3cd3b9f4bf5de0cae09a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p482142-i388230.service; invocation ID: 8f3abcf33a4a4c279bdd5195fb72a166
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: API::USNavalObservatory
  ===> Found: API::USNavalObservatory:ver<1.1.0> [via Zef::Repository::Ecosystems<rea>]
  [API::USNavalObservatory] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787606492.482153.1257.2326591501014/API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/A/API%3A%3AUSNavalObservatory/API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz
  ===> Fetching [OK]: API::USNavalObservatory:ver<1.1.0> to /home/coke/sandbox/blin/data/zef-data/tmp/1787606492.482153.1257.2326591501014/API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz
  [API::USNavalObservatory] Command: tar -t -f ./API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz
  [API::USNavalObservatory] Command: tar -xvf ./API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz -C ../API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz
  ===> Extraction [OK]: API::USNavalObservatory to /home/coke/sandbox/blin/data/zef-data/tmp/API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz
  ===> Testing: API::USNavalObservatory:ver<1.1.0>
  [API::USNavalObservatory] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz/API-USNavalObservatory-master t/10-travis.t
  [API::USNavalObservatory] ok 1 - 
  [API::USNavalObservatory] 1..1
  ===> Testing [OK] for API::USNavalObservatory:ver<1.1.0>
  ===> Installing: API::USNavalObservatory:ver<1.1.0>
  ===> Install [OK] for API::USNavalObservatory:ver<1.1.0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 7min 6.841s
               CPU time consumed: 4min 50.455s
                     Memory peak: 2.1G (swap: 1.3G)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p472484-i411942.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: API::USNavalObservatory
  ===> Found: API::USNavalObservatory:ver<1.1.0> [via Zef::Repository::Ecosystems<rea>]
  [API::USNavalObservatory] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787606177.472488.1777.2850302271427/API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/A/API%3A%3AUSNavalObservatory/API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz
  ===> Fetching [OK]: API::USNavalObservatory:ver<1.1.0> to /home/coke/sandbox/blin/data/zef-data/tmp/1787606177.472488.1777.2850302271427/API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz
  [API::USNavalObservatory] Command: tar -t -f ./API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz
  [API::USNavalObservatory] Command: tar -xvf ./API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz -C ../API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz
  ===> Extraction [OK]: API::USNavalObservatory to /home/coke/sandbox/blin/data/zef-data/tmp/API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz
  ===> Testing: API::USNavalObservatory:ver<1.1.0>
  [API::USNavalObservatory] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/API%3A%3AUSNavalObservatory%3Aver%3C1.1.0%3E%3Aauth%3Cgithub%3Acbk%3E.tar.gz/API-USNavalObservatory-master t/10-travis.t
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 4min 27.918s
               CPU time consumed: 3min 51.978s
                     Memory peak: 2.7G (swap: 1.2G)

  ```
  </details>
* [ ] [ADT](https://raku.land//ADT) – Fail, Bisected: [561c512](https://github.com/rakudo/rakudo/commit/561c5121dbf8d84c5ed815e7e57831707e58d713)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p151604-i98219.service; invocation ID: b97336996fe941ee93a1e0c529c2c538
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: ADT
  ===> Found: ADT:ver<0.5> [via Zef::Repository::Ecosystems<rea>]
  [ADT] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787597558.151606.6730.328237168096/ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/A/ADT/ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz
  ===> Fetching [OK]: ADT:ver<0.5> to /home/coke/sandbox/blin/data/zef-data/tmp/1787597558.151606.6730.328237168096/ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz
  [ADT] Command: tar -t -f ./ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz
  [ADT] Command: tar -xvf ./ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz -C ../ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz
  ===> Extraction [OK]: ADT to /home/coke/sandbox/blin/data/zef-data/tmp/ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz
  ===> Testing: ADT:ver<0.5>
  [ADT] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz/ADT-master t/01-tree.t
  [ADT] 1..7
  [ADT] ok 1 - evaling a construction gists out exactly the same again.
  [ADT] ok 2 - evaling a construction perls out exactly the same again.
  [ADT] ok 3 - positional args for constructors work, too
  [ADT] ok 4 - example treemaps work
  [ADT] ok 5 - smartmatch against container class
  [ADT] ok 6 - smartmatch against one constructor
  [ADT] ok 7 - smartmatch against another constructor
  [ADT] Saw 1 occurrence of deprecated code.
  [ADT] ================================================================================
  [ADT] Method perl (from Mu) seen at:
  [ADT]   /home/coke/sandbox/blin/data/zef-data/tmp/ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz/ADT-master/lib/ADT.pm6 (ADT), line 167
  [ADT] Please use raku instead.
  [ADT] --------------------------------------------------------------------------------
  [ADT] Please contact the author to have these occurrences of deprecated code
  [ADT] adapted, so that this message will disappear!
  [ADT] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz/ADT-master t/02-EXPORT.t
  [ADT] ok 1 - single ADT from EXPORT
  [ADT] ok 2 - single ADT from EXPORT number 2
  [ADT] ok 3 - two ADTs from EXPORT
  [ADT] 1..3
  [ADT] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz/ADT-master t/03-positional.t
  [ADT] 1..8
  [ADT] ok 1 - positional constructors
  [ADT] ok 2 - 
  [ADT] ok 3 - 
  [ADT] ok 4 - 
  [ADT] ok 5 - 
  [ADT] ok 6 - 
  [ADT] ok 7 - 
  [ADT] ok 8 - 
  [ADT] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ADT%3Aver%3C0.5%3E%3Aauth%3Cgithub%3Atimo%3E.tar.gz/ADT-master t/04-whitespace.t
  [ADT] 1..5
  [ADT] ok 1 - sanity
  [ADT] ok 2 - simple multiline
  [ADT] ok 3 - | on the first line, too
  [ADT] ok 4 - newline after comma
  [ADT] ok 5 - trailing comma
  ===> Testing [OK] for ADT:ver<0.5>
  ===> Installing: ADT:ver<0.5>
  ===> Install [OK] for ADT:ver<0.5>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 51.568s
               CPU time consumed: 1min 53.581s
                     Memory peak: 1.4G (swap: 29.2M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p148596-i129071.service; invocation ID: d32e2a4b6a384e828be4d2a33c1e729f
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: ADT
  No candidates found matching identity: ADT
            Finished with result: exit-code
  Main processes terminated with: code=exited, status=255/EXCEPTION
                 Service runtime: 1min 23.551s
               CPU time consumed: 1min 17.733s
                     Memory peak: 892.7M (swap: 92.7M)

  ```
  </details>
* [ ] [AI::NLP](https://raku.land/cpan:KOBOLDWIZ/AI::NLP) – Fail, Bisected: [561c512](https://github.com/rakudo/rakudo/commit/561c5121dbf8d84c5ed815e7e57831707e58d713)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p151621-i117043.service; invocation ID: 60d39f83d83f47388774dbb3e2697451
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: AI::NLP
  ===> Found: AI::NLP:ver<0.1.5>:auth<cpan:KOBOLDWIZ>:api<1> [via Zef::Repository::Ecosystems<rea>]
  [AI::NLP] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787597562.151628.9136.66781750732/AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/A/AI%3A%3ANLP/AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz
  ===> Fetching [OK]: AI::NLP:ver<0.1.5>:auth<cpan:KOBOLDWIZ>:api<1> to /home/coke/sandbox/blin/data/zef-data/tmp/1787597562.151628.9136.66781750732/AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz
  [AI::NLP] Command: tar -t -f ./AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz
  [AI::NLP] Command: tar -xvf ./AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz -C ../AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz
  ===> Extraction [OK]: AI::NLP to /home/coke/sandbox/blin/data/zef-data/tmp/AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz
  ===> Testing: AI::NLP:ver<0.1.5>:auth<CPAN:HOLYGHOST>:api<1>
  [AI::NLP] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/AI%3A%3ANLP%3Aver%3C0.1.5%3E%3Aauth%3Ccpan%3AKOBOLDWIZ%3E%3Aapi%3C1%3E.tar.gz/AI-NLP t/00-load.t
  [AI::NLP] 1..3
  [AI::NLP] ok 1 - AI::NLP::Matrix module can be use-d ok
  [AI::NLP] ok 2 - AI::NLP::Vector module can be use-d ok
  [AI::NLP] ok 3 - AI::NLP::BPPNet module can be use-d ok
  ===> Testing [OK] for AI::NLP:ver<0.1.5>:auth<CPAN:HOLYGHOST>:api<1>
  ===> Installing: AI::NLP:ver<0.1.5>:auth<CPAN:HOLYGHOST>:api<1>
  ===> Install [OK] for AI::NLP:ver<0.1.5>:auth<CPAN:HOLYGHOST>:api<1>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 52.630s
               CPU time consumed: 1min 51.854s
                     Memory peak: 1.4G (swap: 27.9M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p148603-i176938.service; invocation ID: 75308d7654a644538e4c8867886f72cb
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: AI::NLP
  No candidates found matching identity: AI::NLP
            Finished with result: exit-code
  Main processes terminated with: code=exited, status=255/EXCEPTION
                 Service runtime: 1min 23.898s
               CPU time consumed: 1min 19.113s
                     Memory peak: 846.3M (swap: 113.4M)

  ```
  </details>
* [ ] [FDF](https://raku.land/zef:dwarring/FDF) – Fail, Bisected: [561c512](https://github.com/rakudo/rakudo/commit/561c5121dbf8d84c5ed815e7e57831707e58d713)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p700230-i695873.service; invocation ID: 1b02dbb443394546b025714462e6e6c6
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: FDF
  ===> Found: FDF:ver<0.0.4>:auth<zef:dwarring> [via Zef::Repository::Ecosystems<fez>]
  [FDF] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787612763.700231.897.5377281151309/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz https://360.zef.pm/F/DF/FDF/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz
  ===> Fetching [OK]: FDF:ver<0.0.4>:auth<zef:dwarring> to /home/coke/sandbox/blin/data/zef-data/tmp/1787612763.700231.897.5377281151309/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz
  [FDF] Command: tar -t -f ./4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz
  [FDF] Command: tar -xvf ./4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz -C ../4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz
  ===> Extraction [OK]: FDF to /home/coke/sandbox/blin/data/zef-data/tmp/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz
  ===> Testing: FDF:ver<0.0.4>:auth<zef:dwarring>
  [FDF] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz/FDF-0.0.4 t/annots.t
  [FDF] ok 1 - open annots FDF - lives
  [FDF] ok 2 - number of annots
  [FDF] ok 3 - annot role
  [FDF] ok 4 - annot role role
  [FDF] ok 5 - annot.Page
  [FDF] ok 6 - annot.page-number
  [FDF] ok 7 - annot.Page
  [FDF] ok 8 - annot.page-number
  [FDF] 1..8
  [FDF] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz/FDF-0.0.4 t/create.t
  [FDF] ok 1 - create minimal
  [FDF] ok 2 - 
  [FDF] ok 3 - ID generated
  [FDF] ok 4 - created with two identical ID fields
  [FDF] ok 5 - first ID retained after updated
  [FDF] ok 6 - second ID changed after update
  [FDF] 1..6
  [FDF] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz/FDF-0.0.4 t/field-imports.t
  [FDF] 1..8
  [FDF] ok 1 - The object does role 'FDF::Field'
  [FDF] ok 2 - The object does role 'PDF::Field::Text'
  [FDF] ok 3 - PDF::Field.check()
  [FDF] ok 4 - FDF::Field.check()
  [FDF] ok 5 - 
  [FDF] ok 6 - export of T
  [FDF] ok 7 - export of V
  [FDF] ok 8 - export of Ff
  [FDF] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz/FDF-0.0.4 t/fields-exports.t
  [FDF] 1..11
  [FDF] ok 1 - The object does role 'FDF::Field'
  [FDF] ok 2 - The object does role 'PDF::Field::Text'
  [FDF] ok 3 - PDF::Field.check()
  [FDF] ok 4 - FDF::Field.check()
  [FDF] ok 5 - 
  [FDF] ok 6 - import of T
  [FDF] ok 7 - import of V
  [FDF] ok 8 - 
  [FDF] ok 9 - 
  [FDF] ok 10 - import of F
  [FDF] ok 11 - import of Ff
  [FDF] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz/FDF-0.0.4 t/fields.t
  [FDF] ok 1 - open annots FDF - lives
  [FDF] ok 2 - FDF.F
  [FDF] ok 3 - number of fields
  [FDF] ok 4 - field role
  [FDF] ok 5 - @fields[0].T
  [FDF] ok 6 - @fields[0].V
  [FDF] ok 7 - number of fields
  [FDF] ok 8 - field role
  [FDF] ok 9 - %fields<CheckBox>.T
  [FDF] ok 10 - %fields<CheckBox>.V
  [FDF] 1..10
  [FDF] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz/FDF-0.0.4 t/merge.t
  [FDF] ok 1 - 
  [FDF] ok 2 - 
  [FDF] ok 3 - 
  [FDF] ok 4 - 
  [FDF] 1..4
  [FDF] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz/FDF-0.0.4 t/open.t
  [FDF] ok 1 - loaded version
  [FDF] ok 2 - loaded type
  [FDF] ok 3 - root FDF object
  [FDF] ok 4 - $fdf<Root><FDF>
  [FDF] ok 5 - $fdf.Root.FDF
  [FDF] ok 6 - root does catalog
  [FDF] ok 7 - $fdf.FDF.F
  [FDF] ok 8 - $fdf<Root><FDF><Fields>
  [FDF] ok 9 - field item does field
  [FDF] ok 10 - $fdf.Root.FDF.Fields[0].T
  [FDF] 1..10
  ===> Testing [OK] for FDF:ver<0.0.4>:auth<zef:dwarring>
  ===> Installing: FDF:ver<0.0.4>:auth<zef:dwarring>
  ===> Install [OK] for FDF:ver<0.0.4>:auth<zef:dwarring>

  1 bin/ script [fdf-fields.raku] installed to:
  /tmp/tBG87IJdL6/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 10min 8.851s
               CPU time consumed: 7min 39.333s
                     Memory peak: 2.6G (swap: 1G)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p691807-i699739.service; invocation ID: 460912c15cc1496996d91ad17e758e6e
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: FDF
  ===> Found: FDF:ver<0.0.4>:auth<zef:dwarring> [via Zef::Repository::Ecosystems<fez>]
  [FDF] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787612433.691821.7846.259482797738/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz https://360.zef.pm/F/DF/FDF/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz
  ===> Fetching [OK]: FDF:ver<0.0.4>:auth<zef:dwarring> to /home/coke/sandbox/blin/data/zef-data/tmp/1787612433.691821.7846.259482797738/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz
  [FDF] Command: tar -t -f ./4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz
  [FDF] Command: tar -xvf ./4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz -C ../4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz
  ===> Extraction [OK]: FDF to /home/coke/sandbox/blin/data/zef-data/tmp/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz
  ===> Testing: FDF:ver<0.0.4>:auth<zef:dwarring>
  [FDF] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/4c0d33a9d26a9ee335c099369c9dec10efd5a706.tar.gz/FDF-0.0.4 t/annots.t
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 5min 43.707s
               CPU time consumed: 3min 10.399s
                     Memory peak: 2.4G (swap: 823.6M)

  ```
  </details>
* [ ] [LLM::Character](https://raku.land/zef:apogee/LLM::Character) – Fail, Bisected: [561c512](https://github.com/rakudo/rakudo/commit/561c5121dbf8d84c5ed815e7e57831707e58d713)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p498182-i424751.service; invocation ID: d3710fbbb5924816afbb30040a06e6b9
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: LLM::Character
  ===> Found: LLM::Character:ver<0.2.3>:auth<zef:apogee> [via Zef::Repository::Ecosystems<fez>]
  [LLM::Character] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787606915.498193.4789.421923385001/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz https://360.zef.pm/L/LM/LLM_CHARACTER/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  ===> Fetching [OK]: LLM::Character:ver<0.2.3>:auth<zef:apogee> to /home/coke/sandbox/blin/data/zef-data/tmp/1787606915.498193.4789.421923385001/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
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
                 Service runtime: 3min 4.276s
               CPU time consumed: 2min 53.970s
                     Memory peak: 1.7G (swap: 287M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p491010-i498960.service; invocation ID: d8aba33635584e3b82e3a1caf4acb9ac
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: LLM::Character
  ===> Found: LLM::Character:ver<0.2.3>:auth<zef:apogee> [via Zef::Repository::Ecosystems<fez>]
  [LLM::Character] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787606724.491011.7818.676657470257/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz https://360.zef.pm/L/LM/LLM_CHARACTER/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  ===> Fetching [OK]: LLM::Character:ver<0.2.3>:auth<zef:apogee> to /home/coke/sandbox/blin/data/zef-data/tmp/1787606724.491011.7818.676657470257/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  [LLM::Character] Command: tar -t -f ./f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  [LLM::Character] Command: tar -xvf ./f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz -C ../f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  ===> Extraction [OK]: LLM::Character to /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz
  ===> Testing: LLM::Character:ver<0.2.3>:auth<zef:apogee>
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/01-basic.rakutest
  [LLM::Character] ok 1 - replace me
  [LLM::Character] 1..1
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/02-minimal_lorebook.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/03-all_fields_lorebook.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/04-enclosed_minimal_lorebook.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/05-enclosed_all_fields_lorebook.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/06-st_lorebook.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/07-character_enclosed.rakutest
  [LLM::Character] 1..5
  [LLM::Character] ok 1 - Got a character card
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Correct description
  [LLM::Character] ok 4 - Extension talkativeness present
  [LLM::Character] ok 5 - Extension fav present
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/08-character_flat.rakutest
  [LLM::Character] 1..3
  [LLM::Character] ok 1 - Got a character card
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Correct description
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/09-character_with_book.rakutest
  [LLM::Character] 1..5
  [LLM::Character] ok 1 - Got a character card
  [LLM::Character] ok 2 - Correct name
  [LLM::Character] ok 3 - Lorebook is present
  [LLM::Character] ok 4 - One lorebook entry
  [LLM::Character] ok 5 - One asset present
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/10-main.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/11-matcher-construction.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/12-matching.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/13-export_character_json.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/14-export_lorebook_json.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/15-export_lorebook_st.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/16-export_character_png.rakutest
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
  [LLM::Character] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f594ebd569812d0ed2cd94f07155aef37438c3b9.tar.gz/LLM-Character-0.2.3 t/17-export_main.rakutest
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
                 Service runtime: 3min 19.814s
               CPU time consumed: 2min 36.316s
                     Memory peak: 1.7G (swap: 265.5M)

  ```
  </details>
* [ ] [MongoDB](https://raku.land/cpan:MARTIMM/MongoDB) – Fail, Bisected: [561c512](https://github.com/rakudo/rakudo/commit/561c5121dbf8d84c5ed815e7e57831707e58d713)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p579127-i614959.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: MongoDB
  ===> Found: MongoDB:ver<0.45.3>:auth<cpan:MARTIMM> [via Zef::Repository::Ecosystems<rea>]
  [MongoDB] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787609078.579128.1393.005203733354/MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/M/MongoDB/MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz
  ===> Fetching [OK]: MongoDB:ver<0.45.3>:auth<cpan:MARTIMM> to /home/coke/sandbox/blin/data/zef-data/tmp/1787609078.579128.1393.005203733354/MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz
  [MongoDB] Command: tar -t -f ./MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz
  [MongoDB] Command: tar -xvf ./MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz -C ../MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz
  ===> Extraction [OK]: MongoDB to /home/coke/sandbox/blin/data/zef-data/tmp/MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz
  ===> Testing: MongoDB:ver<0.45.3>:auth<cpan:MARTIMM>
  [MongoDB] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz/raku-mongodb-driver-0.45.3 t/MongoDB-Load-Test.rakutest
  [MongoDB] ok 1 - MongoDB
  [MongoDB] ok 2 - MongoDB::Client
  [MongoDB] ok 3 - MongoDB::Authenticate::Credential
  [MongoDB] ok 4 - MongoDB::Authenticate::Scram
  [MongoDB] ok 5 - MongoDB::Client
  [MongoDB] ok 6 - MongoDB::Collection
  [MongoDB] ok 7 - MongoDB::Cursor
  [MongoDB] ok 8 - MongoDB::Database
  [MongoDB] ok 9 - MongoDB::Header
  [MongoDB] ok 10 - MongoDB::HL::Collection
  [MongoDB] ok 11 - MongoDB::HL::Users
  [MongoDB] ok 12 - MongoDB::Log
  [MongoDB] ok 13 - MongoDB::ObserverEmitter
  [MongoDB] ok 14 - MongoDB::Server::Monitor
  [MongoDB] ok 15 - MongoDB::ServerPool::Server
  [MongoDB] ok 16 - MongoDB::ServerPool
  [MongoDB] ok 17 - MongoDB::SocketPool::Socket
  [MongoDB] ok 18 - MongoDB::SocketPool
  [MongoDB] ok 19 - MongoDB::Timer
  [MongoDB] ok 20 - MongoDB::Uri
  [MongoDB] ok 21 - MongoDB::Wire
  [MongoDB] 1..21
  ===> Testing [OK] for MongoDB:ver<0.45.3>:auth<cpan:MARTIMM>
  ===> Installing: MongoDB:ver<0.45.3>:auth<cpan:MARTIMM>
  ===> Install [OK] for MongoDB:ver<0.45.3>:auth<cpan:MARTIMM>

  4 bin/ scripts [mongodb-accounting.raku start-servers.raku make-replicaset.raku stop-servers.raku] installed to:
  /tmp/j_I7xt5LK2/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 6min 41.230s
               CPU time consumed: 5min 7.381s
                     Memory peak: 2.5G (swap: 1G)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p569226-i560034.service; invocation ID: 25b6e47a6fc24cfa8465879489c52be9
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: MongoDB
  ===> Found: MongoDB:ver<0.45.3>:auth<cpan:MARTIMM> [via Zef::Repository::Ecosystems<rea>]
  [MongoDB] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787608780.569229.985.2996026580585/MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/M/MongoDB/MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz
  ===> Fetching [OK]: MongoDB:ver<0.45.3>:auth<cpan:MARTIMM> to /home/coke/sandbox/blin/data/zef-data/tmp/1787608780.569229.985.2996026580585/MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz
  [MongoDB] Command: tar -t -f ./MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz
  [MongoDB] Command: tar -xvf ./MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz -C ../MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz
  ===> Extraction [OK]: MongoDB to /home/coke/sandbox/blin/data/zef-data/tmp/MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz
  ===> Testing: MongoDB:ver<0.45.3>:auth<cpan:MARTIMM>
  [MongoDB] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/MongoDB%3Aver%3C0.45.3%3E%3Aauth%3Ccpan%3AMARTIMM%3E.tar.gz/raku-mongodb-driver-0.45.3 t/MongoDB-Load-Test.rakutest
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 4min 43.997s
               CPU time consumed: 3min 14.400s
                     Memory peak: 2.4G (swap: 1.1G)

  ```
  </details>
* [ ] [PDF::API6](https://raku.land/zef:dwarring/PDF::API6) – Fail, Bisected: [561c512](https://github.com/rakudo/rakudo/commit/561c5121dbf8d84c5ed815e7e57831707e58d713)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p695280-i621415.service; invocation ID: 67800251b9c843a384965084586db39a
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: PDF::API6
  ===> Found: PDF::API6:ver<0.2.10>:auth<zef:dwarring> [via Zef::Repository::Ecosystems<fez>]
  [PDF::API6] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787612581.695301.3099.8923882796225/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz https://360.zef.pm/P/DF/PDF_API6/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz
  ===> Fetching [OK]: PDF::API6:ver<0.2.10>:auth<zef:dwarring> to /home/coke/sandbox/blin/data/zef-data/tmp/1787612581.695301.3099.8923882796225/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz
  [PDF::API6] Command: tar -t -f ./786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz
  [PDF::API6] Command: tar -xvf ./786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz -C ../786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz
  ===> Extraction [OK]: PDF::API6 to /home/coke/sandbox/blin/data/zef-data/tmp/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz
  ===> Testing: PDF::API6:ver<0.2.10>:auth<zef:dwarring>
  [PDF::API6] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz/PDF-API6-0.2.10 t/00-basic.t
  [PDF::API6] 1..9
  [PDF::API6] ok 1 - PDF default version
  [PDF::API6] ok 2 - set version
  [PDF::API6] ok 3 - PDF updated version
  [PDF::API6] ok 4 - set info field
  [PDF::API6] ok 5 - get info field
  [PDF::API6] ok 6 - set xmp metadata
  [PDF::API6] ok 7 - get xmp metadata
  [PDF::API6] ok 8 - invalid rotation
  [PDF::API6] ok 9 - 90 degree rotation
  [PDF::API6] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz/PDF-API6-0.2.10 t/01-readme.t
  [PDF::API6] 1..11
  [PDF::API6] ok 1 - code sample
  [PDF::API6] ok 2 - code sample
  [PDF::API6] ok 3 - code sample
  [PDF::API6] ok 4 - code sample
  [PDF::API6] ok 5 - code sample
  [PDF::API6] ok 6 - code sample
  [PDF::API6] ok 7 - code sample
  [PDF::API6] ok 8 - code sample
  [PDF::API6] ok 9 - code sample
  [PDF::API6] ok 10 - code sample
  [PDF::API6] ok 11 - code sample
  [PDF::API6] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz/PDF-API6-0.2.10 t/annotations.t
  [PDF::API6] 1..22
  [PDF::API6] ok 1 - 
  [PDF::API6] ok 2 - named destination added
  [PDF::API6] ok 3 - dest page dereference
  [PDF::API6] ok 4 - annot added to source page
  [PDF::API6] ok 5 - /P entry in annots
  [PDF::API6] ok 6 - construct link annot
  [PDF::API6] ok 7 - annot added to source page
  [PDF::API6] ok 8 - annot reference to destination page
  [PDF::API6] ok 9 - construct uri annot
  [PDF::API6] ok 10 - annot added to source page
  [PDF::API6] ok 11 - annot reference to URI
  [PDF::API6] ok 12 - construct file annot
  [PDF::API6] ok 13 - remote link added
  [PDF::API6] ok 14 - Goto annonation file
  [PDF::API6] ok 15 - Goto annonation page index
  [PDF::API6] ok 16 - Goto annonation fit
  [PDF::API6] ok 17 - construct text note annot
  [PDF::API6] ok 18 - text annot added
  [PDF::API6] ok 19 - Text note annotation
  [PDF::API6] ok 20 - construct styled uri annot
  [PDF::API6] ok 21 - setting of dashed border
  [PDF::API6] ok 22 - construct file attachment annot
  [PDF::API6] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz/PDF-API6-0.2.10 t/colors.t
  [PDF::API6] 1..17
  [PDF::API6] ok 1 - The object is-a 'PDF::ColorSpace::Separation'
  [PDF::API6] ok 2 - 
  [PDF::API6] ok 3 - 
  [PDF::API6] ok 4 - 
  [PDF::API6] ok 5 - The object is-a 'PDF::Function::Sampled'
  [PDF::API6] ok 6 - got separation function
  [PDF::API6] ok 7 - separation function takes 1 input
  [PDF::API6] ok 8 - separation function produces 4 outputs
  [PDF::API6] ok 9 - separation function calculation
  [PDF::API6] ok 10 - got device-n function
  [PDF::API6] ok 11 - device-n function takes 5 inputs
  [PDF::API6] ok 12 - device-n function produces 4 outputs
  [PDF::API6] ok 13 - device-n function calculation
  [PDF::API6] ok 14 - device-n function calculation
  [PDF::API6] ok 15 - device-n function calculation
  [PDF::API6] ok 16 - device-n function calculation
  [PDF::API6] ok 17 - device-n function calculation
  [PDF::API6] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz/PDF-API6-0.2.10 t/fields.t
  [PDF::API6] 1..29
  [PDF::API6] ok 1 - page annots
  [PDF::API6] ok 2 - page annots
  [PDF::API6] ok 3 - .Fields
  [PDF::API6] ok 4 - fields count
  [PDF::API6] ok 5 - .Fields
  [PDF::API6] ok 6 - field type
  [PDF::API6] ok 7 - .page
  [PDF::API6] ok 8 - .Rect
  [PDF::API6] ok 9 - .T
  [PDF::API6] ok 10 - .TU
  [PDF::API6] ok 11 - .V
  [PDF::API6] ok 12 - .key
  [PDF::API6] ok 13 - .value
  [PDF::API6] ok 14 - .default-value
  [PDF::API6] ok 15 - .MaxLen
  [PDF::API6] ok 16 - .DR
  [PDF::API6] ok 17 - .DA
  [PDF::API6] ok 18 - .appearance
  [PDF::API6] ok 19 - .appearance
  [PDF::API6] ok 20 - .apperance.N
  [PDF::API6] ok 21 - first field via page-1 annots
  [PDF::API6] ok 22 - choice field
  [PDF::API6] ok 23 - choice options
  [PDF::API6] ok 24 - choice first option
  [PDF::API6] ok 25 - Button field
  [PDF::API6] ok 26 - .AP
  [PDF::API6] ok 27 - .AP.N.Yes
  [PDF::API6] ok 28 - fields hash key count
  [PDF::API6] ok 29 - field hash lookup by .T
  [PDF::API6] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz/PDF-API6-0.2.10 t/outlines.t
  [PDF::API6] 1..3
  [PDF::API6] ok 1 - fit destination
  [PDF::API6] ok 2 - fit dest page ref
  [PDF::API6] ok 3 - destination fit
  [PDF::API6] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz/PDF-API6-0.2.10 t/preferences.t
  [PDF::API6] 1..17
  [PDF::API6] ok 1 - PageLayout
  [PDF::API6] ok 2 - PageMode
  [PDF::API6] ok 3 - viewer HideToolbar
  [PDF::API6] ok 4 - viewer non-full page-mode
  [PDF::API6] ok 5 - duplex
  [PDF::API6] ok 6 - viewer non-full page-mode
  [PDF::API6] ok 7 - OpenAction
  [PDF::API6] ok 8 - OpenAction elems
  [PDF::API6] ok 9 - OpenAction[0]
  [PDF::API6] ok 10 - OpenAction[1]
  [PDF::API6] ok 11 - .page-labels accessor
  [PDF::API6] ok 12 - .catalog.PageLabels
  [PDF::API6] ok 13 - $dest.key
  [PDF::API6] ok 14 - The object does role 'PDF::Destination[Str]'
  [PDF::API6] ok 15 - $dest.value.page
  [PDF::API6] ok 16 - $dest.value.fit
  [PDF::API6] ok 17 - .kids rw accessor
  ===> Testing [OK] for PDF::API6:ver<0.2.10>:auth<zef:dwarring>
  ===> Installing: PDF::API6:ver<0.2.10>:auth<zef:dwarring>
  ===> Install [OK] for PDF::API6:ver<0.2.10>:auth<zef:dwarring>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 13min 14.524s
               CPU time consumed: 9min 373ms
                     Memory peak: 2.3G (swap: 1.2G)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p691286-i687436.service; invocation ID: fa3db485cbbb4ee3a9307b7d1c3485d6
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: PDF::API6
  ===> Found: PDF::API6:ver<0.2.10>:auth<zef:dwarring> [via Zef::Repository::Ecosystems<fez>]
  [PDF::API6] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787612373.691290.8910.617588617099/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz https://360.zef.pm/P/DF/PDF_API6/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz
  ===> Fetching [OK]: PDF::API6:ver<0.2.10>:auth<zef:dwarring> to /home/coke/sandbox/blin/data/zef-data/tmp/1787612373.691290.8910.617588617099/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz
  [PDF::API6] Command: tar -t -f ./786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz
  [PDF::API6] Command: tar -xvf ./786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz -C ../786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz
  ===> Extraction [OK]: PDF::API6 to /home/coke/sandbox/blin/data/zef-data/tmp/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz
  ===> Testing: PDF::API6:ver<0.2.10>:auth<zef:dwarring>
  [PDF::API6] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/786604edc4f1f6a19770f68da8d74f02597ae2c4.tar.gz/PDF-API6-0.2.10 t/00-basic.t
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 2min 46.049s
               CPU time consumed: 1min 47.859s
                     Memory peak: 1.9G (swap: 242.4M)

  ```
  </details>
* [ ] [PDF::Font::Loader::CSS](https://raku.land/zef:dwarring/PDF::Font::Loader::CSS) – Fail, Bisected: [561c512](https://github.com/rakudo/rakudo/commit/561c5121dbf8d84c5ed815e7e57831707e58d713)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p695707-i690131.service; invocation ID: 320dee25d82340c2b66e52d11ec533a1
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: PDF::Font::Loader::CSS
  ===> Found: PDF::Font::Loader::CSS:ver<0.0.1>:auth<zef:dwarring> [via Zef::Repository::Ecosystems<fez>]
  [PDF::Font::Loader::CSS] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787612598.695708.3130.8323410973917/cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz https://360.zef.pm/P/DF/PDF_FONT_LOADER_CSS/cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz
  ===> Fetching [OK]: PDF::Font::Loader::CSS:ver<0.0.1>:auth<zef:dwarring> to /home/coke/sandbox/blin/data/zef-data/tmp/1787612598.695708.3130.8323410973917/cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz
  [PDF::Font::Loader::CSS] Command: tar -t -f ./cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz
  [PDF::Font::Loader::CSS] Command: tar -xvf ./cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz -C ../cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz
  ===> Extraction [OK]: PDF::Font::Loader::CSS to /home/coke/sandbox/blin/data/zef-data/tmp/cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz
  ===> Testing: PDF::Font::Loader::CSS:ver<0.0.1>:auth<zef:dwarring>
  [PDF::Font::Loader::CSS] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz/dist t/01basic.t
  [PDF::Font::Loader::CSS] 1..4
  [PDF::Font::Loader::CSS] ok 1 - 
  [PDF::Font::Loader::CSS] ok 2 - 
  [PDF::Font::Loader::CSS] ok 3 - The object is-a '"PDF::Font::Loader::FontObj"'
  [PDF::Font::Loader::CSS] ok 4 - 
  ===> Testing [OK] for PDF::Font::Loader::CSS:ver<0.0.1>:auth<zef:dwarring>
  ===> Installing: PDF::Font::Loader::CSS:ver<0.0.1>:auth<zef:dwarring>
  ===> Install [OK] for PDF::Font::Loader::CSS:ver<0.0.1>:auth<zef:dwarring>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 11min 57.786s
               CPU time consumed: 7min 42.555s
                     Memory peak: 2.3G (swap: 1G)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p689024-i605238.service; invocation ID: 5b0b9877930441c9af6275bbc4fc23c0
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: PDF::Font::Loader::CSS
  ===> Found: PDF::Font::Loader::CSS:ver<0.0.1>:auth<zef:dwarring> [via Zef::Repository::Ecosystems<fez>]
  [PDF::Font::Loader::CSS] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787612307.689036.4321.307628283928/cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz https://360.zef.pm/P/DF/PDF_FONT_LOADER_CSS/cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz
  ===> Fetching [OK]: PDF::Font::Loader::CSS:ver<0.0.1>:auth<zef:dwarring> to /home/coke/sandbox/blin/data/zef-data/tmp/1787612307.689036.4321.307628283928/cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz
  [PDF::Font::Loader::CSS] Command: tar -t -f ./cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz
  [PDF::Font::Loader::CSS] Command: tar -xvf ./cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz -C ../cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz
  ===> Extraction [OK]: PDF::Font::Loader::CSS to /home/coke/sandbox/blin/data/zef-data/tmp/cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz
  ===> Testing: PDF::Font::Loader::CSS:ver<0.0.1>:auth<zef:dwarring>
  [PDF::Font::Loader::CSS] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/cac2fa07550d5e0360360821bfc2b4b685bc5ead.tar.gz/dist t/01basic.t
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 4min 7.804s
               CPU time consumed: 2min 58.830s
                     Memory peak: 2.4G (swap: 1.1G)

  ```
  </details>
* [ ] [Slangify::Tutorial](https://raku.land/zef:librasteve/Slangify::Tutorial) – Fail, Bisected: [561c512](https://github.com/rakudo/rakudo/commit/561c5121dbf8d84c5ed815e7e57831707e58d713)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p659840-i584521.service; invocation ID: 7e4f0eb7ba864549a9f376ca7f1bd435
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Slangify::Tutorial
  ===> Found: Slangify::Tutorial:ver<0.0.1>:auth<zef:librasteve> [via Zef::Repository::Ecosystems<fez>]
  [Slangify::Tutorial] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787611432.659842.7113.424624255602/b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz https://360.zef.pm/S/LA/SLANGIFY_TUTORIAL/b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz
  ===> Fetching [OK]: Slangify::Tutorial:ver<0.0.1>:auth<zef:librasteve> to /home/coke/sandbox/blin/data/zef-data/tmp/1787611432.659842.7113.424624255602/b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz
  [Slangify::Tutorial] Command: tar -t -f ./b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz
  [Slangify::Tutorial] Command: tar -xvf ./b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz -C ../b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz
  ===> Extraction [OK]: Slangify::Tutorial to /home/coke/sandbox/blin/data/zef-data/tmp/b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz
  ===> Testing: Slangify::Tutorial:ver<0.0.1>:auth<zef:librasteve>
  [Slangify::Tutorial] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz/Slangify-Tutorial-0.0.1 t/01-basic.rakutest
  [Slangify::Tutorial] # Subtest: grammar parses canonical DSL line
  [Slangify::Tutorial]     ok 1 - grammar parses
  [Slangify::Tutorial]     ok 2 - name captured (quotes stripped)
  [Slangify::Tutorial]     ok 3 - party captured
  [Slangify::Tutorial]     ok 4 - time captured
  [Slangify::Tutorial]     ok 5 - restaurant captured (quotes stripped)
  [Slangify::Tutorial]     ok 6 - date captured
  [Slangify::Tutorial]     1..6
  [Slangify::Tutorial] ok 1 - grammar parses canonical DSL line
  [Slangify::Tutorial] # Subtest: name with title and last name
  [Slangify::Tutorial]     ok 1 - grammar parses
  [Slangify::Tutorial]     ok 2 - title + first + last captured
  [Slangify::Tutorial]     1..2
  [Slangify::Tutorial] ok 2 - name with title and last name
  [Slangify::Tutorial] # Subtest: name with middle name
  [Slangify::Tutorial]     ok 1 - grammar parses
  [Slangify::Tutorial]     ok 2 - first + middle + last captured
  [Slangify::Tutorial]     1..2
  [Slangify::Tutorial] ok 3 - name with middle name
  [Slangify::Tutorial] # Subtest: actions populate Booking from canonical DSL
  [Slangify::Tutorial]     ok 1 - parse succeeded
  [Slangify::Tutorial]     ok 2 - made a Booking
  [Slangify::Tutorial]     ok 3 - name
  [Slangify::Tutorial]     ok 4 - party coerced to Int
  [Slangify::Tutorial]     ok 5 - party is Int
  [Slangify::Tutorial]     ok 6 - time passes through as 24h
  [Slangify::Tutorial]     ok 7 - restaurant
  [Slangify::Tutorial]     ok 8 - date
  [Slangify::Tutorial]     1..8
  [Slangify::Tutorial] ok 4 - actions populate Booking from canonical DSL
  [Slangify::Tutorial] # Subtest: action-hash has all expected keys
  [Slangify::Tutorial]     ok 1 - name key
  [Slangify::Tutorial]     ok 2 - party key
  [Slangify::Tutorial]     ok 3 - time key
  [Slangify::Tutorial]     ok 4 - restaurant key
  [Slangify::Tutorial]     ok 5 - date key
  [Slangify::Tutorial]     1..5
  [Slangify::Tutorial] ok 5 - action-hash has all expected keys
  [Slangify::Tutorial] # Subtest: grammar rejects raw freeform text
  [Slangify::Tutorial]     ok 1 - freeform text does not parse
  [Slangify::Tutorial]     1..1
  [Slangify::Tutorial] ok 6 - grammar rejects raw freeform text
  [Slangify::Tutorial] # Subtest: various 24h times pass through unchanged
  [Slangify::Tutorial]     ok 1 - 00:00 parses
  [Slangify::Tutorial]     ok 2 - 00:00 passes through
  [Slangify::Tutorial]     ok 3 - 08:30 parses
  [Slangify::Tutorial]     ok 4 - 08:30 passes through
  [Slangify::Tutorial]     ok 5 - 12:00 parses
  [Slangify::Tutorial]     ok 6 - 12:00 passes through
  [Slangify::Tutorial]     ok 7 - 13:45 parses
  [Slangify::Tutorial]     ok 8 - 13:45 passes through
  [Slangify::Tutorial]     ok 9 - 19:30 parses
  [Slangify::Tutorial]     ok 10 - 19:30 passes through
  [Slangify::Tutorial]     ok 11 - 23:59 parses
  [Slangify::Tutorial]     ok 12 - 23:59 passes through
  [Slangify::Tutorial]     1..12
  [Slangify::Tutorial] ok 7 - various 24h times pass through unchanged
  [Slangify::Tutorial] # Subtest: multi-digit party size
  [Slangify::Tutorial]     ok 1 - parses large party
  [Slangify::Tutorial]     ok 2 - party 20
  [Slangify::Tutorial]     ok 3 - still Int
  [Slangify::Tutorial]     1..3
  [Slangify::Tutorial] ok 8 - multi-digit party size
  [Slangify::Tutorial] # Subtest: ISO date
  [Slangify::Tutorial]     ok 1 - parses ISO date
  [Slangify::Tutorial]     ok 2 - ISO date preserved
  [Slangify::Tutorial]     1..2
  [Slangify::Tutorial] ok 9 - ISO date
  [Slangify::Tutorial] # Subtest: JSON output via .raku has correct keys and types
  [Slangify::Tutorial]     ok 1 - name in JSON
  [Slangify::Tutorial]     ok 2 - party in JSON
  [Slangify::Tutorial]     ok 3 - time in JSON as 24h
  [Slangify::Tutorial]     ok 4 - restaurant in JSON
  [Slangify::Tutorial]     ok 5 - date in JSON
  [Slangify::Tutorial]     ok 6 - party is Int (not Str)
  [Slangify::Tutorial]     1..6
  [Slangify::Tutorial] ok 10 - JSON output via .raku has correct keys and types
  [Slangify::Tutorial] ok 11 - # SKIP OPENAI_API_KEY not set — skipping LLM integration test
  [Slangify::Tutorial] 1..11
  ===> Testing [OK] for Slangify::Tutorial:ver<0.0.1>:auth<zef:librasteve>
  ===> Installing: Slangify::Tutorial:ver<0.0.1>:auth<zef:librasteve>
  ===> Install [OK] for Slangify::Tutorial:ver<0.0.1>:auth<zef:librasteve>

  1 bin/ script [extract-booking] installed to:
  /tmp/ChKEefmOca/bin
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 5min 54.625s
               CPU time consumed: 3min 34.709s
                     Memory peak: 1.9G (swap: 762.7M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p651340-i624365.service; invocation ID: 6fba4176e5984a8ab74c69c7c9ee24ff
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Slangify::Tutorial
  ===> Found: Slangify::Tutorial:ver<0.0.1>:auth<zef:librasteve> [via Zef::Repository::Ecosystems<fez>]
  [Slangify::Tutorial] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1787611146.651345.9082.1469861275/b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz https://360.zef.pm/S/LA/SLANGIFY_TUTORIAL/b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz
  ===> Fetching [OK]: Slangify::Tutorial:ver<0.0.1>:auth<zef:librasteve> to /home/coke/sandbox/blin/data/zef-data/tmp/1787611146.651345.9082.1469861275/b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz
  [Slangify::Tutorial] Command: tar -t -f ./b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz
  [Slangify::Tutorial] Command: tar -xvf ./b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz -C ../b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz
  ===> Extraction [OK]: Slangify::Tutorial to /home/coke/sandbox/blin/data/zef-data/tmp/b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz
  ===> Testing: Slangify::Tutorial:ver<0.0.1>:auth<zef:librasteve>
  [Slangify::Tutorial] Command: /tmp/whateverable/rakudo-moar/561c5121dbf8d84c5ed815e7e57831707e58d713/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/b5e7f20a7b0819d2ceca5d19a1f9e8a68cf25f1a.tar.gz/Slangify-Tutorial-0.0.1 t/01-basic.rakutest
            Finished with result: oom-kill
  Main processes terminated with: code=killed, status=9/KILL
                 Service runtime: 4min 49.303s
               CPU time consumed: 3min 15.479s
                     Memory peak: 2G (swap: 807.1M)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| UnhandledException        |     1 | [Foo:: Foo](https://raku.land/github:AlexDaniel/Foo:: Foo) |
| InstallableButUntested    |     9 | [HTTP::Server::Async](https://raku.land/zef:raku-community-modules/HTTP::Server::Async) [IO::Socket::Async::SSL](https://raku.land/zef:raku-community-modules/IO::Socket::Async::SSL) [IRC::Client](https://raku.land/zef:lizmat/IRC::Client) [Log::Minimal](https://raku.land//Log::Minimal) [Russian](https://raku.land/zef:slavenskoj/Russian) [Time::Duration](https://raku.land/zef:masukomi/Time::Duration) [Toaster](https://raku.land//Toaster) [Uzu](https://raku.land/cpan:SACOMO/Uzu) [Web::Scraper](https://raku.land/zef:tony-o/Web::Scraper) |
| Fail                      |    10 | [ADT](https://raku.land//ADT) [AI::NLP](https://raku.land/cpan:KOBOLDWIZ/AI::NLP) [API::USNavalObservatory](https://raku.land//API::USNavalObservatory) [Cro::HTTP::Test](https://raku.land/cpan:JNTHN/Cro::HTTP::Test) [FDF](https://raku.land/zef:dwarring/FDF) [LLM::Character](https://raku.land/zef:apogee/LLM::Character) [MongoDB](https://raku.land/cpan:MARTIMM/MongoDB) [PDF::API6](https://raku.land/zef:dwarring/PDF::API6) [PDF::Font::Loader::CSS](https://raku.land/zef:dwarring/PDF::Font::Loader::CSS) [Slangify::Tutorial](https://raku.land/zef:librasteve/Slangify::Tutorial) |
| MissingDependency         |    11 | [App::Ebread](https://raku.land/zef:samy/App::Ebread) [App::Perl6LangServer](https://raku.land/cpan:AZAWAWI/App::Perl6LangServer) [Chemistry::Elements](https://raku.land/github:briandfoy/Chemistry::Elements) [DBIx::NamedQueries](https://raku.land/cpan:MZIESCHA/DBIx::NamedQueries) [Ethelia](https://raku.land/zef:knarkhov/Ethelia) [Learn::Raku::With](https://raku.land/zef:codesections/Learn::Raku::With) [META6::To::Man](https://raku.land/cpan:TBROWDER/META6::To::Man) [Pakku](https://raku.land/zef:hythm/Pakku) [Perl6::Tracer](https://raku.land/github:jaffa4/Perl6::Tracer) [Task::Galaxy](https://raku.land//Task::Galaxy) [Touch](https://raku.land/zef:rir/Touch) |
| ZefFailure                |    13 | [App::snippet](https://raku.land/github:araraloren/App::snippet) [BDD::Behave](https://raku.land/zef:gdonald/BDD::Behave) [Concurrent::BoundedChannel](https://raku.land/zef:raku-community-modules/Concurrent::BoundedChannel) [Cro::RPC::JSON](https://raku.land/zef:vrurg/Cro::RPC::JSON) [Gnome::Gtk4](https://raku.land/zef:martimm/Gnome::Gtk4) [Jupyter::Kernel](https://raku.land/zef:bduggan/Jupyter::Kernel) [ORM::ActiveRecord](https://raku.land/zef:gdonald/ORM::ActiveRecord) [ParaSeq](https://raku.land/zef:lizmat/ParaSeq) [Proc::ZMQed](https://raku.land/zef:antononcube/Proc::ZMQed) [TXN](https://raku.land//TXN) [TXN::Parser](https://raku.land//TXN::Parser) [TXN::Remarshal](https://raku.land//TXN::Remarshal) [cro](https://raku.land/zef:cro/cro) |
| CyclicDependency          |    46 | ⋯                         |
| AlwaysFail                |   730 | ⋯                         |
| OK                        |  1693 | ⋯                         |



This run started on 2026-08-24T23:35:12Z and finished in ≈4 hours.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
