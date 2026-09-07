[Blin](https://github.com/Raku/Blin) results between 2026.08 ([24e6e53](https://github.com/rakudo/rakudo/commit/24e6e5312f2868680413b0597aef8772f6b5bcea)) and HEAD ([b61226d](https://github.com/rakudo/rakudo/commit/b61226d8bc93d4c030870b48d18af2adfd3a0f6f)):

* [ ] [Needle::Compile](https://raku.land/zef:lizmat/Needle::Compile) – Fail, Bisected: [6ec3194](https://github.com/rakudo/rakudo/commit/6ec31943a47d15e58ada4e93e50eee43f91bb172)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2396698-i2395874.service; invocation ID: 26f27d505fd84a3ba061e3792a19624b
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Needle::Compile
  ===> Found: Needle::Compile:ver<0.0.12>:auth<zef:lizmat> [via Zef::Repository::Ecosystems<fez>]
  [Needle::Compile] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788816899.2396699.560.2071100376704/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz https://360.zef.pm/N/EE/NEEDLE_COMPILE/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz
  ===> Fetching [OK]: Needle::Compile:ver<0.0.12>:auth<zef:lizmat> to /home/coke/sandbox/blin/data/zef-data/tmp/1788816899.2396699.560.2071100376704/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz
  [Needle::Compile] Command: tar -t -f ./66794ae2eb541201a403c08d48e27de668b32db7.tar.gz
  [Needle::Compile] Command: tar -xvf ./66794ae2eb541201a403c08d48e27de668b32db7.tar.gz -C ../66794ae2eb541201a403c08d48e27de668b32db7.tar.gz
  ===> Extraction [OK]: Needle::Compile to /home/coke/sandbox/blin/data/zef-data/tmp/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz
  ===> Testing: Needle::Compile:ver<0.0.12>:auth<zef:lizmat>
  [Needle::Compile] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz/Needle-Compile-0.0.12 t/01-basic.rakutest
  [Needle::Compile] 1..36
  [Needle::Compile] ok 1 - did compile-needle get exported
  [Needle::Compile] ok 2 - did implicit2explicit get exported
  [Needle::Compile] ok 3 - did Type get exported
  [Needle::Compile] ok 4 - did StrType get exported
  [Needle::Compile] ok 5 - it's a string
  [Needle::Compile] ok 6 - it's a butted string
  [Needle::Compile] ok 7 - not a butted string
  [Needle::Compile] ok 8 - is 'foo' *NOT* acceptable
  [Needle::Compile] ok 9 - is 'and' acceptable
  [Needle::Compile] ok 10 - is 'auto' acceptable
  [Needle::Compile] ok 11 - is 'code' acceptable
  [Needle::Compile] ok 12 - is 'contains' acceptable
  [Needle::Compile] ok 13 - is 'ends-with' acceptable
  [Needle::Compile] ok 14 - is 'equal' acceptable
  [Needle::Compile] ok 15 - is 'file' acceptable
  [Needle::Compile] ok 16 - is 'json-path' acceptable
  [Needle::Compile] ok 17 - is 'not' acceptable
  [Needle::Compile] ok 18 - is 'regex' acceptable
  [Needle::Compile] ok 19 - is 'split' acceptable
  [Needle::Compile] ok 20 - is 'starts-with' acceptable
  [Needle::Compile] ok 21 - is 'words' acceptable
  [Needle::Compile] ok 22 - did 'foo' produce the correct explicit?
  [Needle::Compile] ok 23 - did '§foo' produce the correct explicit?
  [Needle::Compile] ok 24 - did '^foo' produce the correct explicit?
  [Needle::Compile] ok 25 - did 'foo$' produce the correct explicit?
  [Needle::Compile] ok 26 - did '^foo$' produce the correct explicit?
  [Needle::Compile] ok 27 - did 'url:foo' produce the correct explicit?
  [Needle::Compile] ok 28 - did 'file:foo' produce the correct explicit?
  [Needle::Compile] ok 29 - did 's:foo' produce the correct explicit?
  [Needle::Compile] ok 30 - did 'jp:foo' produce the correct explicit?
  [Needle::Compile] ok 31 - did '*.foo' produce the correct explicit?
  [Needle::Compile] ok 32 - did '{.foo}' produce the correct explicit?
  [Needle::Compile] ok 33 - did '/foo/' produce the correct explicit?
  [Needle::Compile] ok 34 - did '!foo' produce the correct explicit?
  [Needle::Compile] ok 35 - did '&foo' produce the correct explicit?
  [Needle::Compile] ok 36 - did we get an AST
  [Needle::Compile] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz/Needle-Compile-0.0.12 t/02-single.rakutest
  [Needle::Compile] 1..10
  [Needle::Compile] # Subtest: code: simple .subst
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - Testing ".subst(\"foo\", \"bar\")" but Type('code')
  [Needle::Compile]     ok 2 - 'foo' transformed ok
  [Needle::Compile]     ok 3 - Testing "\{.subst(\"foo\", \"bar\")}"
  [Needle::Compile]     ok 4 - 'foo' transformed ok
  [Needle::Compile]     ok 5 - Testing :code(".subst(\"foo\", \"bar\")")
  [Needle::Compile]     ok 6 - 'foo' transformed ok
  [Needle::Compile]     ok 7 - Testing "*.subst(\"foo\", \"bar\")"
  [Needle::Compile]     ok 8 - 'foo' transformed ok
  [Needle::Compile] ok 1 - code: simple .subst
  [Needle::Compile] # Subtest: code: simple .uc
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - Testing ".uc" but Type('code')
  [Needle::Compile]     ok 2 - 'foo' transformed ok
  [Needle::Compile]     ok 3 - Testing "\{.uc}"
  [Needle::Compile]     ok 4 - 'foo' transformed ok
  [Needle::Compile]     ok 5 - Testing :code(".uc")
  [Needle::Compile]     ok 6 - 'foo' transformed ok
  [Needle::Compile]     ok 7 - Testing "*.uc"
  [Needle::Compile]     ok 8 - 'foo' transformed ok
  [Needle::Compile] ok 2 - code: simple .uc
  [Needle::Compile] # Subtest: code: check availability of $*_
  [Needle::Compile]     1..6
  [Needle::Compile]     ok 1 - Testing "\$*_ eq \$_" but Type('code')
  [Needle::Compile]     ok 2 - 'foo' transformed ok
  [Needle::Compile]     ok 3 - Testing "\{\$*_ eq \$_}"
  [Needle::Compile]     ok 4 - 'foo' transformed ok
  [Needle::Compile]     ok 5 - Testing :code("\$*_ eq \$_")
  [Needle::Compile]     ok 6 - 'foo' transformed ok
  [Needle::Compile] ok 3 - code: check availability of $*_
  [Needle::Compile] # Subtest: code: check loading of Test module
  [Needle::Compile]     1..9
  [Needle::Compile]     ok 1 - Testing "is \$_, 42" but Type('code')
  [Needle::Compile]     ok 2 - 
  [Needle::Compile]     ok 3 - '42' transformed ok
  [Needle::Compile]     ok 4 - Testing "\{is \$_, 42}"
  [Needle::Compile]     ok 5 - 
  [Needle::Compile]     ok 6 - '42' transformed ok
  [Needle::Compile]     ok 7 - Testing :code("is \$_, 42")
  [Needle::Compile]     ok 8 - 
  [Needle::Compile]     ok 9 - '42' transformed ok
  [Needle::Compile] ok 4 - code: check loading of Test module
  [Needle::Compile] # Subtest: all named arguments for contains
  [Needle::Compile]     1..5
  [Needle::Compile]     # Subtest: contains: find simple 'foo'
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo"
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit 'infooout'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo")
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit 'infooout'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo")
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit 'infooout'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo" but Type('auto')
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit 'infooout'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo" but Type('auto'))
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit 'infooout'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo" but Type('auto'))
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit 'infooout'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit 'infooout'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo" but Type('contains'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit 'infooout'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo" but Type('contains'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit 'infooout'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit 'infooout'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit 'infooout'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit 'infooout'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".contains('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit 'infooout'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit 'infooout'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit 'infooout'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - hit 'infooout'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not hit 'infooout'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and hit 'infooout'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.contains('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit 'infooout'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.contains('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not hit 'infooout'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.contains('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and hit 'infooout'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.contains('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - hit 'infooout'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.contains('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not hit 'infooout'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.contains('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and hit 'infooout'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :auto("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - hit 'infooout'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:auto("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not hit 'infooout'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:auto("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and hit 'infooout'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :contains("foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - hit 'infooout'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:contains("foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not hit 'infooout'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:contains("foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and hit 'infooout'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - hit 'infooout'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not hit 'infooout'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and hit 'infooout'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".contains('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - hit 'infooout'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".contains('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not hit 'infooout'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".contains('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and hit 'infooout'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! hit 'infooout'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! hit 'infooout'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.contains('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! hit 'infooout'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.contains('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! hit 'infooout'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo"
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - returned 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - returned 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - returned 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - returned 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :contains("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - returned 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - returned 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 1 - contains: find simple 'foo'
  [Needle::Compile]     # Subtest: contains: find simple 'foo', :ignorecase, :ignorecase
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo"
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit 'infooout'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo")
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit 'infooout'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo")
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit 'infooout'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo" but Type('auto')
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit 'infooout'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo" but Type('auto'))
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit 'infooout'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo" but Type('auto'))
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit 'infooout'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit 'infooout'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo" but Type('contains'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit 'infooout'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo" but Type('contains'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit 'infooout'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit 'infooout'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit 'infooout'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit 'infooout'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".contains('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit 'infooout'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit 'infooout'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit 'infooout'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - hit 'infooout'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not hit 'infooout'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and hit 'infooout'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.contains('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit 'infooout'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.contains('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not hit 'infooout'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.contains('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and hit 'infooout'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.contains('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - hit 'infooout'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.contains('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not hit 'infooout'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.contains('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and hit 'infooout'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :auto("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - hit 'infooout'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:auto("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not hit 'infooout'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:auto("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and hit 'infooout'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :contains("foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - hit 'infooout'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:contains("foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not hit 'infooout'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:contains("foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and hit 'infooout'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - hit 'infooout'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not hit 'infooout'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and hit 'infooout'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".contains('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - hit 'infooout'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".contains('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not hit 'infooout'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".contains('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and hit 'infooout'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! hit 'infooout'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! hit 'infooout'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.contains('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! hit 'infooout'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.contains('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! hit 'infooout'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo"
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - returned 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - returned 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - returned 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - returned 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :contains("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - returned 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - returned 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 2 - contains: find simple 'foo', :ignorecase, :ignorecase
  [Needle::Compile]     # Subtest: contains: find simple 'foo', :ignoremark, :ignoremark
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo"
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit 'infooout'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo")
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit 'infooout'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo")
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit 'infooout'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo" but Type('auto')
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit 'infooout'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo" but Type('auto'))
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit 'infooout'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo" but Type('auto'))
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit 'infooout'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit 'infooout'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo" but Type('contains'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit 'infooout'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo" but Type('contains'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit 'infooout'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit 'infooout'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit 'infooout'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit 'infooout'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".contains('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit 'infooout'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit 'infooout'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit 'infooout'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - hit 'infooout'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not hit 'infooout'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and hit 'infooout'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.contains('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit 'infooout'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.contains('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not hit 'infooout'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.contains('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and hit 'infooout'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.contains('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - hit 'infooout'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.contains('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not hit 'infooout'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.contains('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and hit 'infooout'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :auto("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - hit 'infooout'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:auto("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not hit 'infooout'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:auto("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and hit 'infooout'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :contains("foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - hit 'infooout'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:contains("foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not hit 'infooout'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:contains("foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and hit 'infooout'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - hit 'infooout'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not hit 'infooout'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and hit 'infooout'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".contains('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - hit 'infooout'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".contains('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not hit 'infooout'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".contains('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and hit 'infooout'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! hit 'infooout'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! hit 'infooout'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.contains('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! hit 'infooout'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.contains('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! hit 'infooout'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo"
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - returned 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - returned 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - returned 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - returned 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :contains("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - returned 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - returned 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 3 - contains: find simple 'foo', :ignoremark, :ignoremark
  [Needle::Compile]     # Subtest: contains: find simple 'foo', :smartcase, :smartcase
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo"
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit 'infooout'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo")
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit 'infooout'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo")
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit 'infooout'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo" but Type('auto')
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit 'infooout'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo" but Type('auto'))
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit 'infooout'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo" but Type('auto'))
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit 'infooout'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit 'infooout'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo" but Type('contains'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit 'infooout'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo" but Type('contains'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit 'infooout'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit 'infooout'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit 'infooout'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit 'infooout'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".contains('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit 'infooout'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit 'infooout'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit 'infooout'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - hit 'infooout'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not hit 'infooout'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and hit 'infooout'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.contains('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit 'infooout'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.contains('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not hit 'infooout'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.contains('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and hit 'infooout'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.contains('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - hit 'infooout'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.contains('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not hit 'infooout'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.contains('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and hit 'infooout'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :auto("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - hit 'infooout'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:auto("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not hit 'infooout'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:auto("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and hit 'infooout'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :contains("foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - hit 'infooout'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:contains("foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not hit 'infooout'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:contains("foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and hit 'infooout'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - hit 'infooout'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not hit 'infooout'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and hit 'infooout'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".contains('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - hit 'infooout'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".contains('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not hit 'infooout'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".contains('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and hit 'infooout'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! hit 'infooout'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! hit 'infooout'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.contains('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! hit 'infooout'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.contains('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! hit 'infooout'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo"
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - returned 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - returned 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - returned 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - returned 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :contains("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - returned 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - returned 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 4 - contains: find simple 'foo', :smartcase, :smartcase
  [Needle::Compile]     # Subtest: contains: find simple 'foo', :smartmark, :smartmark
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo"
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit 'infooout'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo")
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit 'infooout'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo")
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit 'infooout'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo" but Type('auto')
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit 'infooout'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo" but Type('auto'))
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit 'infooout'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo" but Type('auto'))
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit 'infooout'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit 'infooout'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo" but Type('contains'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit 'infooout'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo" but Type('contains'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit 'infooout'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit 'infooout'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit 'infooout'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit 'infooout'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".contains('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit 'infooout'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit 'infooout'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit 'infooout'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - hit 'infooout'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not hit 'infooout'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and hit 'infooout'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.contains('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit 'infooout'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.contains('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not hit 'infooout'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.contains('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and hit 'infooout'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.contains('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - hit 'infooout'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.contains('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not hit 'infooout'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.contains('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and hit 'infooout'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :auto("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - hit 'infooout'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:auto("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not hit 'infooout'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:auto("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and hit 'infooout'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :contains("foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - hit 'infooout'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:contains("foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not hit 'infooout'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:contains("foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and hit 'infooout'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - hit 'infooout'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not hit 'infooout'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and hit 'infooout'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".contains('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - hit 'infooout'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".contains('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not hit 'infooout'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".contains('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and hit 'infooout'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! hit 'infooout'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! hit 'infooout'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.contains('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! hit 'infooout'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.contains('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! hit 'infooout'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo"
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - returned 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - returned 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - returned 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - returned 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :contains("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - returned 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - returned 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 5 - contains: find simple 'foo', :smartmark, :smartmark
  [Needle::Compile] ok 5 - all named arguments for contains
  [Needle::Compile] # Subtest: all named arguments for starts-with
  [Needle::Compile]     1..5
  [Needle::Compile]     # Subtest: starts-with: starts with simple 'foo'
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo" but Type('starts-with')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss ' foo'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('starts-with'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss ' foo'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('starts-with'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss ' foo'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "^foo"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss ' foo'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("^foo")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss ' foo'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("^foo")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss ' foo'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "^foo" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss ' foo'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("^foo" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss ' foo'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("^foo" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss ' foo'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "^foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss ' foo'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("^foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss ' foo'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("^foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss ' foo'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".starts-with('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss ' foo'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".starts-with('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss ' foo'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".starts-with('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss ' foo'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/^ foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss ' foo'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/^ foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss ' foo'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/^ foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss ' foo'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.starts-with('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss ' foo'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.starts-with('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss ' foo'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.starts-with('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss ' foo'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.starts-with('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss ' foo'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.starts-with('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss ' foo'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.starts-with('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss ' foo'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :starts-with("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss ' foo'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:starts-with("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss ' foo'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:starts-with("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss ' foo'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :auto("^foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - miss ' foo'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:auto("^foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not miss ' foo'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:auto("^foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and miss ' foo'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("^foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - miss ' foo'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("^foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not miss ' foo'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("^foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and miss ' foo'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".starts-with('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - miss ' foo'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".starts-with('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not miss ' foo'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".starts-with('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and miss ' foo'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!^foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! miss ' foo'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/^ foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! miss ' foo'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.starts-with('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! miss ' foo'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.starts-with('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! miss ' foo'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo" but Type('starts-with')
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - miss 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "^foo"
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - miss 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "^foo" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - miss 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/^ foo/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - miss 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :starts-with("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - miss 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("^foo")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - miss 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 1 - starts-with: starts with simple 'foo'
  [Needle::Compile]     # Subtest: starts-with: starts with simple 'foo', :ignorecase
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo" but Type('starts-with')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss ' foo'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('starts-with'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss ' foo'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('starts-with'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss ' foo'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "^foo"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss ' foo'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("^foo")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss ' foo'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("^foo")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss ' foo'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "^foo" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss ' foo'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("^foo" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss ' foo'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("^foo" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss ' foo'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "^foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss ' foo'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("^foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss ' foo'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("^foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss ' foo'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".starts-with('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss ' foo'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".starts-with('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss ' foo'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".starts-with('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss ' foo'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/^ foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss ' foo'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/^ foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss ' foo'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/^ foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss ' foo'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.starts-with('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss ' foo'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.starts-with('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss ' foo'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.starts-with('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss ' foo'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.starts-with('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss ' foo'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.starts-with('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss ' foo'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.starts-with('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss ' foo'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :starts-with("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss ' foo'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:starts-with("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss ' foo'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:starts-with("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss ' foo'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :auto("^foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - miss ' foo'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:auto("^foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not miss ' foo'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:auto("^foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and miss ' foo'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("^foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - miss ' foo'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("^foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not miss ' foo'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("^foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and miss ' foo'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".starts-with('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - miss ' foo'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".starts-with('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not miss ' foo'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".starts-with('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and miss ' foo'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!^foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! miss ' foo'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/^ foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! miss ' foo'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.starts-with('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! miss ' foo'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.starts-with('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! miss ' foo'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo" but Type('starts-with')
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - miss 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "^foo"
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - miss 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "^foo" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - miss 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/^ foo/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - miss 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :starts-with("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - miss 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("^foo")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - miss 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 2 - starts-with: starts with simple 'foo', :ignorecase
  [Needle::Compile]     # Subtest: starts-with: starts with simple 'foo', :ignoremark
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo" but Type('starts-with')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss ' foo'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('starts-with'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss ' foo'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('starts-with'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss ' foo'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "^foo"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss ' foo'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("^foo")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss ' foo'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("^foo")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss ' foo'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "^foo" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss ' foo'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("^foo" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss ' foo'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("^foo" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss ' foo'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "^foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss ' foo'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("^foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss ' foo'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("^foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss ' foo'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".starts-with('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss ' foo'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".starts-with('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss ' foo'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".starts-with('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss ' foo'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/^ foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss ' foo'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/^ foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss ' foo'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/^ foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss ' foo'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.starts-with('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss ' foo'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.starts-with('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss ' foo'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.starts-with('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss ' foo'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.starts-with('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss ' foo'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.starts-with('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss ' foo'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.starts-with('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss ' foo'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :starts-with("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss ' foo'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:starts-with("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss ' foo'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:starts-with("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss ' foo'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :auto("^foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - miss ' foo'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:auto("^foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not miss ' foo'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:auto("^foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and miss ' foo'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("^foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - miss ' foo'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("^foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not miss ' foo'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("^foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and miss ' foo'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".starts-with('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - miss ' foo'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".starts-with('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not miss ' foo'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".starts-with('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and miss ' foo'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!^foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! miss ' foo'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/^ foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! miss ' foo'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.starts-with('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! miss ' foo'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.starts-with('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! miss ' foo'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo" but Type('starts-with')
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - miss 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "^foo"
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - miss 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "^foo" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - miss 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/^ foo/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - miss 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :starts-with("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - miss 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("^foo")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - miss 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 3 - starts-with: starts with simple 'foo', :ignoremark
  [Needle::Compile]     # Subtest: starts-with: starts with simple 'foo', :smartcase
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo" but Type('starts-with')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss ' foo'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('starts-with'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss ' foo'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('starts-with'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss ' foo'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "^foo"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss ' foo'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("^foo")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss ' foo'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("^foo")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss ' foo'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "^foo" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss ' foo'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("^foo" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss ' foo'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("^foo" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss ' foo'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "^foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss ' foo'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("^foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss ' foo'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("^foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss ' foo'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".starts-with('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss ' foo'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".starts-with('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss ' foo'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".starts-with('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss ' foo'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/^ foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss ' foo'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/^ foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss ' foo'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/^ foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss ' foo'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.starts-with('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss ' foo'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.starts-with('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss ' foo'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.starts-with('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss ' foo'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.starts-with('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss ' foo'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.starts-with('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss ' foo'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.starts-with('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss ' foo'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :starts-with("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss ' foo'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:starts-with("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss ' foo'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:starts-with("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss ' foo'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :auto("^foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - miss ' foo'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:auto("^foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not miss ' foo'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:auto("^foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and miss ' foo'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("^foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - miss ' foo'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("^foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not miss ' foo'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("^foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and miss ' foo'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".starts-with('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - miss ' foo'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".starts-with('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not miss ' foo'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".starts-with('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and miss ' foo'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!^foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! miss ' foo'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/^ foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! miss ' foo'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.starts-with('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! miss ' foo'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.starts-with('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! miss ' foo'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo" but Type('starts-with')
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - miss 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "^foo"
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - miss 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "^foo" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - miss 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/^ foo/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - miss 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :starts-with("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - miss 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("^foo")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - miss 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 4 - starts-with: starts with simple 'foo', :smartcase
  [Needle::Compile]     # Subtest: starts-with: starts with simple 'foo', :smartmark
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo" but Type('starts-with')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss ' foo'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('starts-with'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss ' foo'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('starts-with'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss ' foo'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "^foo"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss ' foo'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("^foo")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss ' foo'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("^foo")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss ' foo'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "^foo" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss ' foo'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("^foo" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss ' foo'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("^foo" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss ' foo'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "^foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss ' foo'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("^foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss ' foo'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("^foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss ' foo'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".starts-with('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss ' foo'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".starts-with('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss ' foo'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".starts-with('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss ' foo'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/^ foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss ' foo'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/^ foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss ' foo'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/^ foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss ' foo'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.starts-with('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss ' foo'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.starts-with('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss ' foo'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.starts-with('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss ' foo'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.starts-with('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss ' foo'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.starts-with('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss ' foo'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.starts-with('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss ' foo'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :starts-with("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss ' foo'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:starts-with("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss ' foo'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:starts-with("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss ' foo'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :auto("^foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - miss ' foo'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:auto("^foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not miss ' foo'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:auto("^foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and miss ' foo'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("^foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - miss ' foo'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("^foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not miss ' foo'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("^foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and miss ' foo'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".starts-with('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - miss ' foo'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".starts-with('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not miss ' foo'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".starts-with('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and miss ' foo'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!^foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! miss ' foo'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/^ foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! miss ' foo'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.starts-with('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! miss ' foo'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.starts-with('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! miss ' foo'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo" but Type('starts-with')
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - miss 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "^foo"
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - miss 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "^foo" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - miss 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/^ foo/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - miss 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :starts-with("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - miss 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("^foo")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - miss 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 5 - starts-with: starts with simple 'foo', :smartmark
  [Needle::Compile] ok 6 - all named arguments for starts-with
  [Needle::Compile] # Subtest: all named arguments for ends-with
  [Needle::Compile]     1..5
  [Needle::Compile]     # Subtest: ends-with: ends with simple 'foo'
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo" but Type('ends-with')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss 'foo '
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('ends-with'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss 'foo '
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('ends-with'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss 'foo '
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo\$"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss 'foo '
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo\$")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss 'foo '
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo\$")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss 'foo '
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo\$" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss 'foo '
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo\$" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss 'foo '
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo\$" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss 'foo '
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo\$" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss 'foo '
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo\$" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss 'foo '
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo\$" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss 'foo '
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".ends-with('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss 'foo '
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".ends-with('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss 'foo '
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".ends-with('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss 'foo '
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo \$/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss 'foo '
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo \$/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss 'foo '
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo \$/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss 'foo '
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.ends-with('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss 'foo '
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.ends-with('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss 'foo '
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.ends-with('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss 'foo '
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.ends-with('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss 'foo '
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.ends-with('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss 'foo '
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.ends-with('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss 'foo '
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :ends-with("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss 'foo '
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:ends-with("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss 'foo '
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:ends-with("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss 'foo '
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :auto("foo\$")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - miss 'foo '
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:auto("foo\$"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not miss 'foo '
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:auto("foo\$"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and miss 'foo '
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :code(".ends-with('foo')")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - miss 'foo '
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:code(".ends-with('foo')"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not miss 'foo '
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:code(".ends-with('foo')"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and miss 'foo '
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :regex("foo\$")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - miss 'foo '
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:regex("foo\$"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not miss 'foo '
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:regex("foo\$"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and miss 'foo '
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo\$"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! miss 'foo '
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo \$/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! miss 'foo '
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.ends-with('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! miss 'foo '
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.ends-with('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! miss 'foo '
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo" but Type('ends-with')
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - miss 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo\$"
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - miss 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo\$" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - miss 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo \$/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - miss 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :ends-with("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - miss 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo\$")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - miss 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 1 - ends-with: ends with simple 'foo'
  [Needle::Compile]     # Subtest: ends-with: ends with simple 'foo', :ignorecase
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo" but Type('ends-with')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss 'foo '
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('ends-with'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss 'foo '
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('ends-with'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss 'foo '
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo\$"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss 'foo '
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo\$")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss 'foo '
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo\$")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss 'foo '
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo\$" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss 'foo '
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo\$" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss 'foo '
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo\$" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss 'foo '
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo\$" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss 'foo '
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo\$" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss 'foo '
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo\$" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss 'foo '
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".ends-with('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss 'foo '
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".ends-with('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss 'foo '
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".ends-with('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss 'foo '
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo \$/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss 'foo '
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo \$/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss 'foo '
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo \$/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss 'foo '
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.ends-with('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss 'foo '
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.ends-with('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss 'foo '
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.ends-with('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss 'foo '
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.ends-with('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss 'foo '
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.ends-with('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss 'foo '
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.ends-with('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss 'foo '
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :ends-with("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss 'foo '
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:ends-with("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss 'foo '
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:ends-with("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss 'foo '
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :auto("foo\$")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - miss 'foo '
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:auto("foo\$"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not miss 'foo '
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:auto("foo\$"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and miss 'foo '
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :code(".ends-with('foo')")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - miss 'foo '
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:code(".ends-with('foo')"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not miss 'foo '
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:code(".ends-with('foo')"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and miss 'foo '
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :regex("foo\$")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - miss 'foo '
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:regex("foo\$"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not miss 'foo '
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:regex("foo\$"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and miss 'foo '
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo\$"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! miss 'foo '
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo \$/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! miss 'foo '
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.ends-with('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! miss 'foo '
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.ends-with('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! miss 'foo '
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo" but Type('ends-with')
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - miss 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo\$"
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - miss 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo\$" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - miss 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo \$/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - miss 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :ends-with("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - miss 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo\$")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - miss 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 2 - ends-with: ends with simple 'foo', :ignorecase
  [Needle::Compile]     # Subtest: ends-with: ends with simple 'foo', :ignoremark
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo" but Type('ends-with')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss 'foo '
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('ends-with'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss 'foo '
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('ends-with'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss 'foo '
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo\$"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss 'foo '
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo\$")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss 'foo '
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo\$")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss 'foo '
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo\$" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss 'foo '
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo\$" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss 'foo '
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo\$" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss 'foo '
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo\$" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss 'foo '
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo\$" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss 'foo '
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo\$" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss 'foo '
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".ends-with('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss 'foo '
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".ends-with('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss 'foo '
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".ends-with('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss 'foo '
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo \$/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss 'foo '
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo \$/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss 'foo '
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo \$/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss 'foo '
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.ends-with('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss 'foo '
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.ends-with('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss 'foo '
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.ends-with('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss 'foo '
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.ends-with('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss 'foo '
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.ends-with('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss 'foo '
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.ends-with('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss 'foo '
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :ends-with("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss 'foo '
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:ends-with("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss 'foo '
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:ends-with("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss 'foo '
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :auto("foo\$")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - miss 'foo '
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:auto("foo\$"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not miss 'foo '
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:auto("foo\$"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and miss 'foo '
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :code(".ends-with('foo')")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - miss 'foo '
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:code(".ends-with('foo')"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not miss 'foo '
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:code(".ends-with('foo')"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and miss 'foo '
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :regex("foo\$")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - miss 'foo '
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:regex("foo\$"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not miss 'foo '
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:regex("foo\$"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and miss 'foo '
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo\$"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! miss 'foo '
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo \$/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! miss 'foo '
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.ends-with('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! miss 'foo '
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.ends-with('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! miss 'foo '
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo" but Type('ends-with')
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - miss 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo\$"
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - miss 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo\$" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - miss 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo \$/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - miss 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :ends-with("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - miss 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo\$")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - miss 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 3 - ends-with: ends with simple 'foo', :ignoremark
  [Needle::Compile]     # Subtest: ends-with: ends with simple 'foo', :smartcase
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo" but Type('ends-with')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss 'foo '
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('ends-with'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss 'foo '
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('ends-with'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss 'foo '
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo\$"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss 'foo '
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo\$")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss 'foo '
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo\$")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss 'foo '
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo\$" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss 'foo '
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo\$" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss 'foo '
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo\$" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss 'foo '
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo\$" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss 'foo '
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo\$" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss 'foo '
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo\$" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss 'foo '
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".ends-with('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss 'foo '
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".ends-with('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss 'foo '
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".ends-with('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss 'foo '
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo \$/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss 'foo '
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo \$/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss 'foo '
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo \$/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss 'foo '
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.ends-with('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss 'foo '
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.ends-with('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss 'foo '
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.ends-with('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss 'foo '
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.ends-with('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss 'foo '
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.ends-with('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss 'foo '
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.ends-with('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss 'foo '
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :ends-with("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss 'foo '
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:ends-with("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss 'foo '
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:ends-with("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss 'foo '
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :auto("foo\$")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - miss 'foo '
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:auto("foo\$"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not miss 'foo '
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:auto("foo\$"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and miss 'foo '
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :code(".ends-with('foo')")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - miss 'foo '
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:code(".ends-with('foo')"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not miss 'foo '
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:code(".ends-with('foo')"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and miss 'foo '
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :regex("foo\$")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - miss 'foo '
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:regex("foo\$"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not miss 'foo '
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:regex("foo\$"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and miss 'foo '
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo\$"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! miss 'foo '
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo \$/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! miss 'foo '
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.ends-with('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! miss 'foo '
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.ends-with('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! miss 'foo '
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo" but Type('ends-with')
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - miss 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo\$"
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - miss 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo\$" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - miss 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo \$/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - miss 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :ends-with("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - miss 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo\$")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - miss 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 4 - ends-with: ends with simple 'foo', :smartcase
  [Needle::Compile]     # Subtest: ends-with: ends with simple 'foo', :smartmark
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo" but Type('ends-with')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss 'foo '
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('ends-with'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss 'foo '
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('ends-with'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss 'foo '
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo\$"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss 'foo '
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo\$")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss 'foo '
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo\$")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss 'foo '
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo\$" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss 'foo '
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo\$" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss 'foo '
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo\$" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss 'foo '
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo\$" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss 'foo '
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo\$" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss 'foo '
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo\$" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss 'foo '
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".ends-with('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss 'foo '
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".ends-with('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss 'foo '
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".ends-with('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss 'foo '
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo \$/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss 'foo '
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo \$/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss 'foo '
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo \$/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss 'foo '
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.ends-with('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss 'foo '
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.ends-with('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss 'foo '
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.ends-with('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss 'foo '
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.ends-with('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss 'foo '
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.ends-with('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss 'foo '
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.ends-with('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss 'foo '
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :ends-with("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss 'foo '
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:ends-with("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss 'foo '
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:ends-with("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss 'foo '
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :auto("foo\$")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - miss 'foo '
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:auto("foo\$"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not miss 'foo '
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:auto("foo\$"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and miss 'foo '
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :code(".ends-with('foo')")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - miss 'foo '
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:code(".ends-with('foo')"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not miss 'foo '
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:code(".ends-with('foo')"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and miss 'foo '
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :regex("foo\$")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - miss 'foo '
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:regex("foo\$"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not miss 'foo '
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:regex("foo\$"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and miss 'foo '
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo\$"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! miss 'foo '
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo \$/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! miss 'foo '
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.ends-with('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! miss 'foo '
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.ends-with('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! miss 'foo '
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo" but Type('ends-with')
  [Needle::Compile]         ok 162 - returned 'foo'
  [Needle::Compile]         ok 163 - miss 'foo'
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo\$"
  [Needle::Compile]         ok 166 - returned 'foo'
  [Needle::Compile]         ok 167 - miss 'foo'
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo\$" but Type('regex')
  [Needle::Compile]         ok 170 - returned 'foo'
  [Needle::Compile]         ok 171 - miss 'foo'
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo \$/"
  [Needle::Compile]         ok 174 - returned 'foo'
  [Needle::Compile]         ok 175 - miss 'foo'
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :ends-with("foo")
  [Needle::Compile]         ok 178 - returned 'foo'
  [Needle::Compile]         ok 179 - miss 'foo'
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo\$")
  [Needle::Compile]         ok 182 - returned 'foo'
  [Needle::Compile]         ok 183 - miss 'foo'
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]     ok 5 - ends-with: ends with simple 'foo', :smartmark
  [Needle::Compile] ok 7 - all named arguments for ends-with
  [Needle::Compile] # Subtest: all named arguments for equal
  [Needle::Compile]     1..5
  [Needle::Compile]     # Subtest: equal: equal simple 'foo'
  [Needle::Compile]         1..128
  [Needle::Compile]         ok 1 - Testing "foo" but Type('equal')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss ' foo '
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('equal'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss ' foo '
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('equal'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss ' foo '
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "^foo\$"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss ' foo '
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("^foo\$")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss ' foo '
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("^foo\$")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss ' foo '
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "^foo\$" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss ' foo '
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("^foo\$" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss ' foo '
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("^foo\$" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss ' foo '
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "'foo' eq \$_" but Type('code')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss ' foo '
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("'foo' eq \$_" but Type('code'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss ' foo '
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("'foo' eq \$_" but Type('code'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss ' foo '
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing "/^ foo \$/"
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss ' foo '
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not("/^ foo \$/")
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss ' foo '
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and("/^ foo \$/")
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss ' foo '
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "\{'foo' eq \$_}"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss ' foo '
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("\{'foo' eq \$_}")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss ' foo '
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("\{'foo' eq \$_}")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss ' foo '
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing :auto("^foo\$")
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss ' foo '
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not(:auto("^foo\$"))
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss ' foo '
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and(:auto("^foo\$"))
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss ' foo '
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing :regex("^foo\$")
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss ' foo '
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not(:regex("^foo\$"))
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss ' foo '
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and(:regex("^foo\$"))
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss ' foo '
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :code("'foo' eq \$_")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss ' foo '
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:code("'foo' eq \$_"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss ' foo '
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:code("'foo' eq \$_"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss ' foo '
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing "!^foo\$"
  [Needle::Compile]         ok 110 - ! hit 'foo'
  [Needle::Compile]         ok 111 - ! miss ' foo '
  [Needle::Compile]         ok 112 - ! miss 'bar'
  [Needle::Compile]         ok 113 - Testing "!/^ foo \$/"
  [Needle::Compile]         ok 114 - ! hit 'foo'
  [Needle::Compile]         ok 115 - ! miss ' foo '
  [Needle::Compile]         ok 116 - ! miss 'bar'
  [Needle::Compile]         ok 117 - Testing "!\{'foo' eq \$_}"
  [Needle::Compile]         ok 118 - ! hit 'foo'
  [Needle::Compile]         ok 119 - ! miss ' foo '
  [Needle::Compile]         ok 120 - ! miss 'bar'
  [Needle::Compile]         ok 121 - Testing "/^ foo \$/"
  [Needle::Compile]         ok 122 - returned 'foo'
  [Needle::Compile]         ok 123 - miss 'foo'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :regex("^foo\$")
  [Needle::Compile]         ok 126 - returned 'foo'
  [Needle::Compile]         ok 127 - miss 'foo'
  [Needle::Compile]         ok 128 - miss 'bar'
  [Needle::Compile]     ok 1 - equal: equal simple 'foo'
  [Needle::Compile]     # Subtest: equal: equal simple 'foo', :ignorecase
  [Needle::Compile]         1..128
  [Needle::Compile]         ok 1 - Testing "foo" but Type('equal')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss ' foo '
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('equal'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss ' foo '
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('equal'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss ' foo '
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "^foo\$"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss ' foo '
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("^foo\$")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss ' foo '
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("^foo\$")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss ' foo '
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "^foo\$" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss ' foo '
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("^foo\$" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss ' foo '
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("^foo\$" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss ' foo '
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "'foo' eq \$_" but Type('code')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss ' foo '
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("'foo' eq \$_" but Type('code'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss ' foo '
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("'foo' eq \$_" but Type('code'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss ' foo '
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing "/^ foo \$/"
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss ' foo '
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not("/^ foo \$/")
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss ' foo '
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and("/^ foo \$/")
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss ' foo '
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "\{'foo' eq \$_}"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss ' foo '
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("\{'foo' eq \$_}")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss ' foo '
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("\{'foo' eq \$_}")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss ' foo '
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing :auto("^foo\$")
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss ' foo '
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not(:auto("^foo\$"))
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss ' foo '
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and(:auto("^foo\$"))
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss ' foo '
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing :regex("^foo\$")
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss ' foo '
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not(:regex("^foo\$"))
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss ' foo '
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and(:regex("^foo\$"))
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss ' foo '
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :code("'foo' eq \$_")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss ' foo '
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:code("'foo' eq \$_"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss ' foo '
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:code("'foo' eq \$_"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss ' foo '
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing "!^foo\$"
  [Needle::Compile]         ok 110 - ! hit 'foo'
  [Needle::Compile]         ok 111 - ! miss ' foo '
  [Needle::Compile]         ok 112 - ! miss 'bar'
  [Needle::Compile]         ok 113 - Testing "!/^ foo \$/"
  [Needle::Compile]         ok 114 - ! hit 'foo'
  [Needle::Compile]         ok 115 - ! miss ' foo '
  [Needle::Compile]         ok 116 - ! miss 'bar'
  [Needle::Compile]         ok 117 - Testing "!\{'foo' eq \$_}"
  [Needle::Compile]         ok 118 - ! hit 'foo'
  [Needle::Compile]         ok 119 - ! miss ' foo '
  [Needle::Compile]         ok 120 - ! miss 'bar'
  [Needle::Compile]         ok 121 - Testing "/^ foo \$/"
  [Needle::Compile]         ok 122 - returned 'foo'
  [Needle::Compile]         ok 123 - miss 'foo'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :regex("^foo\$")
  [Needle::Compile]         ok 126 - returned 'foo'
  [Needle::Compile]         ok 127 - miss 'foo'
  [Needle::Compile]         ok 128 - miss 'bar'
  [Needle::Compile]     ok 2 - equal: equal simple 'foo', :ignorecase
  [Needle::Compile]     # Subtest: equal: equal simple 'foo', :ignoremark
  [Needle::Compile]         1..128
  [Needle::Compile]         ok 1 - Testing "foo" but Type('equal')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss ' foo '
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('equal'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss ' foo '
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('equal'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss ' foo '
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "^foo\$"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss ' foo '
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("^foo\$")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss ' foo '
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("^foo\$")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss ' foo '
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "^foo\$" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss ' foo '
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("^foo\$" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss ' foo '
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("^foo\$" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss ' foo '
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "'foo' eq \$_" but Type('code')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss ' foo '
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("'foo' eq \$_" but Type('code'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss ' foo '
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("'foo' eq \$_" but Type('code'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss ' foo '
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing "/^ foo \$/"
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss ' foo '
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not("/^ foo \$/")
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss ' foo '
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and("/^ foo \$/")
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss ' foo '
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "\{'foo' eq \$_}"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss ' foo '
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("\{'foo' eq \$_}")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss ' foo '
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("\{'foo' eq \$_}")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss ' foo '
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing :auto("^foo\$")
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss ' foo '
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not(:auto("^foo\$"))
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss ' foo '
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and(:auto("^foo\$"))
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss ' foo '
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing :regex("^foo\$")
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss ' foo '
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not(:regex("^foo\$"))
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss ' foo '
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and(:regex("^foo\$"))
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss ' foo '
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :code("'foo' eq \$_")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss ' foo '
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:code("'foo' eq \$_"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss ' foo '
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:code("'foo' eq \$_"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss ' foo '
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing "!^foo\$"
  [Needle::Compile]         ok 110 - ! hit 'foo'
  [Needle::Compile]         ok 111 - ! miss ' foo '
  [Needle::Compile]         ok 112 - ! miss 'bar'
  [Needle::Compile]         ok 113 - Testing "!/^ foo \$/"
  [Needle::Compile]         ok 114 - ! hit 'foo'
  [Needle::Compile]         ok 115 - ! miss ' foo '
  [Needle::Compile]         ok 116 - ! miss 'bar'
  [Needle::Compile]         ok 117 - Testing "!\{'foo' eq \$_}"
  [Needle::Compile]         ok 118 - ! hit 'foo'
  [Needle::Compile]         ok 119 - ! miss ' foo '
  [Needle::Compile]         ok 120 - ! miss 'bar'
  [Needle::Compile]         ok 121 - Testing "/^ foo \$/"
  [Needle::Compile]         ok 122 - returned 'foo'
  [Needle::Compile]         ok 123 - miss 'foo'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :regex("^foo\$")
  [Needle::Compile]         ok 126 - returned 'foo'
  [Needle::Compile]         ok 127 - miss 'foo'
  [Needle::Compile]         ok 128 - miss 'bar'
  [Needle::Compile]     ok 3 - equal: equal simple 'foo', :ignoremark
  [Needle::Compile]     # Subtest: equal: equal simple 'foo', :smartcase
  [Needle::Compile]         1..128
  [Needle::Compile]         ok 1 - Testing "foo" but Type('equal')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss ' foo '
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('equal'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss ' foo '
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('equal'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss ' foo '
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "^foo\$"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss ' foo '
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("^foo\$")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss ' foo '
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("^foo\$")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss ' foo '
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "^foo\$" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss ' foo '
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("^foo\$" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss ' foo '
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("^foo\$" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss ' foo '
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "'foo' eq \$_" but Type('code')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss ' foo '
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("'foo' eq \$_" but Type('code'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss ' foo '
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("'foo' eq \$_" but Type('code'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss ' foo '
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing "/^ foo \$/"
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss ' foo '
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not("/^ foo \$/")
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss ' foo '
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and("/^ foo \$/")
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss ' foo '
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "\{'foo' eq \$_}"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss ' foo '
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("\{'foo' eq \$_}")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss ' foo '
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("\{'foo' eq \$_}")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss ' foo '
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing :auto("^foo\$")
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss ' foo '
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not(:auto("^foo\$"))
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss ' foo '
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and(:auto("^foo\$"))
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss ' foo '
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing :regex("^foo\$")
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss ' foo '
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not(:regex("^foo\$"))
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss ' foo '
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and(:regex("^foo\$"))
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss ' foo '
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :code("'foo' eq \$_")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss ' foo '
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:code("'foo' eq \$_"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss ' foo '
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:code("'foo' eq \$_"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss ' foo '
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing "!^foo\$"
  [Needle::Compile]         ok 110 - ! hit 'foo'
  [Needle::Compile]         ok 111 - ! miss ' foo '
  [Needle::Compile]         ok 112 - ! miss 'bar'
  [Needle::Compile]         ok 113 - Testing "!/^ foo \$/"
  [Needle::Compile]         ok 114 - ! hit 'foo'
  [Needle::Compile]         ok 115 - ! miss ' foo '
  [Needle::Compile]         ok 116 - ! miss 'bar'
  [Needle::Compile]         ok 117 - Testing "!\{'foo' eq \$_}"
  [Needle::Compile]         ok 118 - ! hit 'foo'
  [Needle::Compile]         ok 119 - ! miss ' foo '
  [Needle::Compile]         ok 120 - ! miss 'bar'
  [Needle::Compile]         ok 121 - Testing "/^ foo \$/"
  [Needle::Compile]         ok 122 - returned 'foo'
  [Needle::Compile]         ok 123 - miss 'foo'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :regex("^foo\$")
  [Needle::Compile]         ok 126 - returned 'foo'
  [Needle::Compile]         ok 127 - miss 'foo'
  [Needle::Compile]         ok 128 - miss 'bar'
  [Needle::Compile]     ok 4 - equal: equal simple 'foo', :smartcase
  [Needle::Compile]     # Subtest: equal: equal simple 'foo', :smartmark
  [Needle::Compile]         1..128
  [Needle::Compile]         ok 1 - Testing "foo" but Type('equal')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - miss ' foo '
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('equal'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not miss ' foo '
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('equal'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and miss ' foo '
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "^foo\$"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - miss ' foo '
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("^foo\$")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not miss ' foo '
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("^foo\$")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and miss ' foo '
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "^foo\$" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - miss ' foo '
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("^foo\$" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not miss ' foo '
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("^foo\$" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and miss ' foo '
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "'foo' eq \$_" but Type('code')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - miss ' foo '
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("'foo' eq \$_" but Type('code'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not miss ' foo '
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("'foo' eq \$_" but Type('code'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and miss ' foo '
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing "/^ foo \$/"
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - miss ' foo '
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not("/^ foo \$/")
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not miss ' foo '
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and("/^ foo \$/")
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and miss ' foo '
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "\{'foo' eq \$_}"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - miss ' foo '
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("\{'foo' eq \$_}")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not miss ' foo '
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("\{'foo' eq \$_}")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and miss ' foo '
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing :auto("^foo\$")
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - miss ' foo '
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not(:auto("^foo\$"))
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not miss ' foo '
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and(:auto("^foo\$"))
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and miss ' foo '
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing :regex("^foo\$")
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - miss ' foo '
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not(:regex("^foo\$"))
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not miss ' foo '
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and(:regex("^foo\$"))
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and miss ' foo '
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :code("'foo' eq \$_")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - miss ' foo '
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:code("'foo' eq \$_"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not miss ' foo '
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:code("'foo' eq \$_"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and miss ' foo '
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing "!^foo\$"
  [Needle::Compile]         ok 110 - ! hit 'foo'
  [Needle::Compile]         ok 111 - ! miss ' foo '
  [Needle::Compile]         ok 112 - ! miss 'bar'
  [Needle::Compile]         ok 113 - Testing "!/^ foo \$/"
  [Needle::Compile]         ok 114 - ! hit 'foo'
  [Needle::Compile]         ok 115 - ! miss ' foo '
  [Needle::Compile]         ok 116 - ! miss 'bar'
  [Needle::Compile]         ok 117 - Testing "!\{'foo' eq \$_}"
  [Needle::Compile]         ok 118 - ! hit 'foo'
  [Needle::Compile]         ok 119 - ! miss ' foo '
  [Needle::Compile]         ok 120 - ! miss 'bar'
  [Needle::Compile]         ok 121 - Testing "/^ foo \$/"
  [Needle::Compile]         ok 122 - returned 'foo'
  [Needle::Compile]         ok 123 - miss 'foo'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :regex("^foo\$")
  [Needle::Compile]         ok 126 - returned 'foo'
  [Needle::Compile]         ok 127 - miss 'foo'
  [Needle::Compile]         ok 128 - miss 'bar'
  [Needle::Compile]     ok 5 - equal: equal simple 'foo', :smartmark
  [Needle::Compile] ok 8 - all named arguments for equal
  [Needle::Compile] # Subtest: all named arguments for words
  [Needle::Compile]     1..5
  [Needle::Compile]     # Subtest: words: words simple 'foo'
  [Needle::Compile]         1..114
  [Needle::Compile]         ok 1 - Testing "foo" but Type('words')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit ' foo '
  [Needle::Compile]         ok 4 - hit ':foo:'
  [Needle::Compile]         ok 5 - miss 'oofooff'
  [Needle::Compile]         ok 6 - miss 'bar'
  [Needle::Compile]         ok 7 - Testing :not("foo" but Type('words'))
  [Needle::Compile]         ok 8 - not hit 'foo'
  [Needle::Compile]         ok 9 - not hit ' foo '
  [Needle::Compile]         ok 10 - not hit ':foo:'
  [Needle::Compile]         ok 11 - not miss 'oofooff'
  [Needle::Compile]         ok 12 - not miss 'bar'
  [Needle::Compile]         ok 13 - Testing :and("foo" but Type('words'))
  [Needle::Compile]         ok 14 - and hit 'foo'
  [Needle::Compile]         ok 15 - and hit ' foo '
  [Needle::Compile]         ok 16 - and hit ':foo:'
  [Needle::Compile]         ok 17 - and miss 'oofooff'
  [Needle::Compile]         ok 18 - and miss 'bar'
  [Needle::Compile]         ok 19 - Testing "§foo"
  [Needle::Compile]         ok 20 - hit 'foo'
  [Needle::Compile]         ok 21 - hit ' foo '
  [Needle::Compile]         ok 22 - hit ':foo:'
  [Needle::Compile]         ok 23 - miss 'oofooff'
  [Needle::Compile]         ok 24 - miss 'bar'
  [Needle::Compile]         ok 25 - Testing :not("§foo")
  [Needle::Compile]         ok 26 - not hit 'foo'
  [Needle::Compile]         ok 27 - not hit ' foo '
  [Needle::Compile]         ok 28 - not hit ':foo:'
  [Needle::Compile]         ok 29 - not miss 'oofooff'
  [Needle::Compile]         ok 30 - not miss 'bar'
  [Needle::Compile]         ok 31 - Testing :and("§foo")
  [Needle::Compile]         ok 32 - and hit 'foo'
  [Needle::Compile]         ok 33 - and hit ' foo '
  [Needle::Compile]         ok 34 - and hit ':foo:'
  [Needle::Compile]         ok 35 - and miss 'oofooff'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "§foo" but Type('auto')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit ' foo '
  [Needle::Compile]         ok 40 - hit ':foo:'
  [Needle::Compile]         ok 41 - miss 'oofooff'
  [Needle::Compile]         ok 42 - miss 'bar'
  [Needle::Compile]         ok 43 - Testing :not("§foo" but Type('auto'))
  [Needle::Compile]         ok 44 - not hit 'foo'
  [Needle::Compile]         ok 45 - not hit ' foo '
  [Needle::Compile]         ok 46 - not hit ':foo:'
  [Needle::Compile]         ok 47 - not miss 'oofooff'
  [Needle::Compile]         ok 48 - not miss 'bar'
  [Needle::Compile]         ok 49 - Testing :and("§foo" but Type('auto'))
  [Needle::Compile]         ok 50 - and hit 'foo'
  [Needle::Compile]         ok 51 - and hit ' foo '
  [Needle::Compile]         ok 52 - and hit ':foo:'
  [Needle::Compile]         ok 53 - and miss 'oofooff'
  [Needle::Compile]         ok 54 - and miss 'bar'
  [Needle::Compile]         ok 55 - Testing :words("foo")
  [Needle::Compile]         ok 56 - hit 'foo'
  [Needle::Compile]         ok 57 - hit ' foo '
  [Needle::Compile]         ok 58 - hit ':foo:'
  [Needle::Compile]         ok 59 - miss 'oofooff'
  [Needle::Compile]         ok 60 - miss 'bar'
  [Needle::Compile]         ok 61 - Testing :not(:words("foo"))
  [Needle::Compile]         ok 62 - not hit 'foo'
  [Needle::Compile]         ok 63 - not hit ' foo '
  [Needle::Compile]         ok 64 - not hit ':foo:'
  [Needle::Compile]         ok 65 - not miss 'oofooff'
  [Needle::Compile]         ok 66 - not miss 'bar'
  [Needle::Compile]         ok 67 - Testing :and(:words("foo"))
  [Needle::Compile]         ok 68 - and hit 'foo'
  [Needle::Compile]         ok 69 - and hit ' foo '
  [Needle::Compile]         ok 70 - and hit ':foo:'
  [Needle::Compile]         ok 71 - and miss 'oofooff'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing :auto("§foo")
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit ' foo '
  [Needle::Compile]         ok 76 - hit ':foo:'
  [Needle::Compile]         ok 77 - miss 'oofooff'
  [Needle::Compile]         ok 78 - miss 'bar'
  [Needle::Compile]         ok 79 - Testing :not(:auto("§foo"))
  [Needle::Compile]         ok 80 - not hit 'foo'
  [Needle::Compile]         ok 81 - not hit ' foo '
  [Needle::Compile]         ok 82 - not hit ':foo:'
  [Needle::Compile]         ok 83 - not miss 'oofooff'
  [Needle::Compile]         ok 84 - not miss 'bar'
  [Needle::Compile]         ok 85 - Testing :and(:auto("§foo"))
  [Needle::Compile]         ok 86 - and hit 'foo'
  [Needle::Compile]         ok 87 - and hit ' foo '
  [Needle::Compile]         ok 88 - and hit ':foo:'
  [Needle::Compile]         ok 89 - and miss 'oofooff'
  [Needle::Compile]         ok 90 - and miss 'bar'
  [Needle::Compile]         ok 91 - Testing "!§foo"
  [Needle::Compile]         ok 92 - ! hit 'foo'
  [Needle::Compile]         ok 93 - ! hit ' foo '
  [Needle::Compile]         ok 94 - ! hit ':foo:'
  [Needle::Compile]         ok 95 - ! miss 'oofooff'
  [Needle::Compile]         ok 96 - ! miss 'bar'
  [Needle::Compile]         ok 97 - Testing "foo" but Type('words')
  [Needle::Compile]         ok 98 - returned 'foo'
  [Needle::Compile]         ok 99 - returned ' foo '
  [Needle::Compile]         ok 100 - returned ':foo:'
  [Needle::Compile]         ok 101 - miss 'oofooff'
  [Needle::Compile]         ok 102 - miss 'bar'
  [Needle::Compile]         ok 103 - Testing "§foo"
  [Needle::Compile]         ok 104 - returned 'foo'
  [Needle::Compile]         ok 105 - returned ' foo '
  [Needle::Compile]         ok 106 - returned ':foo:'
  [Needle::Compile]         ok 107 - miss 'oofooff'
  [Needle::Compile]         ok 108 - miss 'bar'
  [Needle::Compile]         ok 109 - Testing :words("foo")
  [Needle::Compile]         ok 110 - returned 'foo'
  [Needle::Compile]         ok 111 - returned ' foo '
  [Needle::Compile]         ok 112 - returned ':foo:'
  [Needle::Compile]         ok 113 - miss 'oofooff'
  [Needle::Compile]         ok 114 - miss 'bar'
  [Needle::Compile]     ok 1 - words: words simple 'foo'
  [Needle::Compile]     # Subtest: words: words simple 'foo', :ignorecase
  [Needle::Compile]         1..114
  [Needle::Compile]         ok 1 - Testing "foo" but Type('words')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit ' foo '
  [Needle::Compile]         ok 4 - hit ':foo:'
  [Needle::Compile]         ok 5 - miss 'oofooff'
  [Needle::Compile]         ok 6 - miss 'bar'
  [Needle::Compile]         ok 7 - Testing :not("foo" but Type('words'))
  [Needle::Compile]         ok 8 - not hit 'foo'
  [Needle::Compile]         ok 9 - not hit ' foo '
  [Needle::Compile]         ok 10 - not hit ':foo:'
  [Needle::Compile]         ok 11 - not miss 'oofooff'
  [Needle::Compile]         ok 12 - not miss 'bar'
  [Needle::Compile]         ok 13 - Testing :and("foo" but Type('words'))
  [Needle::Compile]         ok 14 - and hit 'foo'
  [Needle::Compile]         ok 15 - and hit ' foo '
  [Needle::Compile]         ok 16 - and hit ':foo:'
  [Needle::Compile]         ok 17 - and miss 'oofooff'
  [Needle::Compile]         ok 18 - and miss 'bar'
  [Needle::Compile]         ok 19 - Testing "§foo"
  [Needle::Compile]         ok 20 - hit 'foo'
  [Needle::Compile]         ok 21 - hit ' foo '
  [Needle::Compile]         ok 22 - hit ':foo:'
  [Needle::Compile]         ok 23 - miss 'oofooff'
  [Needle::Compile]         ok 24 - miss 'bar'
  [Needle::Compile]         ok 25 - Testing :not("§foo")
  [Needle::Compile]         ok 26 - not hit 'foo'
  [Needle::Compile]         ok 27 - not hit ' foo '
  [Needle::Compile]         ok 28 - not hit ':foo:'
  [Needle::Compile]         ok 29 - not miss 'oofooff'
  [Needle::Compile]         ok 30 - not miss 'bar'
  [Needle::Compile]         ok 31 - Testing :and("§foo")
  [Needle::Compile]         ok 32 - and hit 'foo'
  [Needle::Compile]         ok 33 - and hit ' foo '
  [Needle::Compile]         ok 34 - and hit ':foo:'
  [Needle::Compile]         ok 35 - and miss 'oofooff'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "§foo" but Type('auto')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit ' foo '
  [Needle::Compile]         ok 40 - hit ':foo:'
  [Needle::Compile]         ok 41 - miss 'oofooff'
  [Needle::Compile]         ok 42 - miss 'bar'
  [Needle::Compile]         ok 43 - Testing :not("§foo" but Type('auto'))
  [Needle::Compile]         ok 44 - not hit 'foo'
  [Needle::Compile]         ok 45 - not hit ' foo '
  [Needle::Compile]         ok 46 - not hit ':foo:'
  [Needle::Compile]         ok 47 - not miss 'oofooff'
  [Needle::Compile]         ok 48 - not miss 'bar'
  [Needle::Compile]         ok 49 - Testing :and("§foo" but Type('auto'))
  [Needle::Compile]         ok 50 - and hit 'foo'
  [Needle::Compile]         ok 51 - and hit ' foo '
  [Needle::Compile]         ok 52 - and hit ':foo:'
  [Needle::Compile]         ok 53 - and miss 'oofooff'
  [Needle::Compile]         ok 54 - and miss 'bar'
  [Needle::Compile]         ok 55 - Testing :words("foo")
  [Needle::Compile]         ok 56 - hit 'foo'
  [Needle::Compile]         ok 57 - hit ' foo '
  [Needle::Compile]         ok 58 - hit ':foo:'
  [Needle::Compile]         ok 59 - miss 'oofooff'
  [Needle::Compile]         ok 60 - miss 'bar'
  [Needle::Compile]         ok 61 - Testing :not(:words("foo"))
  [Needle::Compile]         ok 62 - not hit 'foo'
  [Needle::Compile]         ok 63 - not hit ' foo '
  [Needle::Compile]         ok 64 - not hit ':foo:'
  [Needle::Compile]         ok 65 - not miss 'oofooff'
  [Needle::Compile]         ok 66 - not miss 'bar'
  [Needle::Compile]         ok 67 - Testing :and(:words("foo"))
  [Needle::Compile]         ok 68 - and hit 'foo'
  [Needle::Compile]         ok 69 - and hit ' foo '
  [Needle::Compile]         ok 70 - and hit ':foo:'
  [Needle::Compile]         ok 71 - and miss 'oofooff'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing :auto("§foo")
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit ' foo '
  [Needle::Compile]         ok 76 - hit ':foo:'
  [Needle::Compile]         ok 77 - miss 'oofooff'
  [Needle::Compile]         ok 78 - miss 'bar'
  [Needle::Compile]         ok 79 - Testing :not(:auto("§foo"))
  [Needle::Compile]         ok 80 - not hit 'foo'
  [Needle::Compile]         ok 81 - not hit ' foo '
  [Needle::Compile]         ok 82 - not hit ':foo:'
  [Needle::Compile]         ok 83 - not miss 'oofooff'
  [Needle::Compile]         ok 84 - not miss 'bar'
  [Needle::Compile]         ok 85 - Testing :and(:auto("§foo"))
  [Needle::Compile]         ok 86 - and hit 'foo'
  [Needle::Compile]         ok 87 - and hit ' foo '
  [Needle::Compile]         ok 88 - and hit ':foo:'
  [Needle::Compile]         ok 89 - and miss 'oofooff'
  [Needle::Compile]         ok 90 - and miss 'bar'
  [Needle::Compile]         ok 91 - Testing "!§foo"
  [Needle::Compile]         ok 92 - ! hit 'foo'
  [Needle::Compile]         ok 93 - ! hit ' foo '
  [Needle::Compile]         ok 94 - ! hit ':foo:'
  [Needle::Compile]         ok 95 - ! miss 'oofooff'
  [Needle::Compile]         ok 96 - ! miss 'bar'
  [Needle::Compile]         ok 97 - Testing "foo" but Type('words')
  [Needle::Compile]         ok 98 - returned 'foo'
  [Needle::Compile]         ok 99 - returned ' foo '
  [Needle::Compile]         ok 100 - returned ':foo:'
  [Needle::Compile]         ok 101 - miss 'oofooff'
  [Needle::Compile]         ok 102 - miss 'bar'
  [Needle::Compile]         ok 103 - Testing "§foo"
  [Needle::Compile]         ok 104 - returned 'foo'
  [Needle::Compile]         ok 105 - returned ' foo '
  [Needle::Compile]         ok 106 - returned ':foo:'
  [Needle::Compile]         ok 107 - miss 'oofooff'
  [Needle::Compile]         ok 108 - miss 'bar'
  [Needle::Compile]         ok 109 - Testing :words("foo")
  [Needle::Compile]         ok 110 - returned 'foo'
  [Needle::Compile]         ok 111 - returned ' foo '
  [Needle::Compile]         ok 112 - returned ':foo:'
  [Needle::Compile]         ok 113 - miss 'oofooff'
  [Needle::Compile]         ok 114 - miss 'bar'
  [Needle::Compile]     ok 2 - words: words simple 'foo', :ignorecase
  [Needle::Compile]     # Subtest: words: words simple 'foo', :ignoremark
  [Needle::Compile]         1..114
  [Needle::Compile]         ok 1 - Testing "foo" but Type('words')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit ' foo '
  [Needle::Compile]         ok 4 - hit ':foo:'
  [Needle::Compile]         ok 5 - miss 'oofooff'
  [Needle::Compile]         ok 6 - miss 'bar'
  [Needle::Compile]         ok 7 - Testing :not("foo" but Type('words'))
  [Needle::Compile]         ok 8 - not hit 'foo'
  [Needle::Compile]         ok 9 - not hit ' foo '
  [Needle::Compile]         ok 10 - not hit ':foo:'
  [Needle::Compile]         ok 11 - not miss 'oofooff'
  [Needle::Compile]         ok 12 - not miss 'bar'
  [Needle::Compile]         ok 13 - Testing :and("foo" but Type('words'))
  [Needle::Compile]         ok 14 - and hit 'foo'
  [Needle::Compile]         ok 15 - and hit ' foo '
  [Needle::Compile]         ok 16 - and hit ':foo:'
  [Needle::Compile]         ok 17 - and miss 'oofooff'
  [Needle::Compile]         ok 18 - and miss 'bar'
  [Needle::Compile]         ok 19 - Testing "§foo"
  [Needle::Compile]         ok 20 - hit 'foo'
  [Needle::Compile]         ok 21 - hit ' foo '
  [Needle::Compile]         ok 22 - hit ':foo:'
  [Needle::Compile]         ok 23 - miss 'oofooff'
  [Needle::Compile]         ok 24 - miss 'bar'
  [Needle::Compile]         ok 25 - Testing :not("§foo")
  [Needle::Compile]         ok 26 - not hit 'foo'
  [Needle::Compile]         ok 27 - not hit ' foo '
  [Needle::Compile]         ok 28 - not hit ':foo:'
  [Needle::Compile]         ok 29 - not miss 'oofooff'
  [Needle::Compile]         ok 30 - not miss 'bar'
  [Needle::Compile]         ok 31 - Testing :and("§foo")
  [Needle::Compile]         ok 32 - and hit 'foo'
  [Needle::Compile]         ok 33 - and hit ' foo '
  [Needle::Compile]         ok 34 - and hit ':foo:'
  [Needle::Compile]         ok 35 - and miss 'oofooff'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "§foo" but Type('auto')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit ' foo '
  [Needle::Compile]         ok 40 - hit ':foo:'
  [Needle::Compile]         ok 41 - miss 'oofooff'
  [Needle::Compile]         ok 42 - miss 'bar'
  [Needle::Compile]         ok 43 - Testing :not("§foo" but Type('auto'))
  [Needle::Compile]         ok 44 - not hit 'foo'
  [Needle::Compile]         ok 45 - not hit ' foo '
  [Needle::Compile]         ok 46 - not hit ':foo:'
  [Needle::Compile]         ok 47 - not miss 'oofooff'
  [Needle::Compile]         ok 48 - not miss 'bar'
  [Needle::Compile]         ok 49 - Testing :and("§foo" but Type('auto'))
  [Needle::Compile]         ok 50 - and hit 'foo'
  [Needle::Compile]         ok 51 - and hit ' foo '
  [Needle::Compile]         ok 52 - and hit ':foo:'
  [Needle::Compile]         ok 53 - and miss 'oofooff'
  [Needle::Compile]         ok 54 - and miss 'bar'
  [Needle::Compile]         ok 55 - Testing :words("foo")
  [Needle::Compile]         ok 56 - hit 'foo'
  [Needle::Compile]         ok 57 - hit ' foo '
  [Needle::Compile]         ok 58 - hit ':foo:'
  [Needle::Compile]         ok 59 - miss 'oofooff'
  [Needle::Compile]         ok 60 - miss 'bar'
  [Needle::Compile]         ok 61 - Testing :not(:words("foo"))
  [Needle::Compile]         ok 62 - not hit 'foo'
  [Needle::Compile]         ok 63 - not hit ' foo '
  [Needle::Compile]         ok 64 - not hit ':foo:'
  [Needle::Compile]         ok 65 - not miss 'oofooff'
  [Needle::Compile]         ok 66 - not miss 'bar'
  [Needle::Compile]         ok 67 - Testing :and(:words("foo"))
  [Needle::Compile]         ok 68 - and hit 'foo'
  [Needle::Compile]         ok 69 - and hit ' foo '
  [Needle::Compile]         ok 70 - and hit ':foo:'
  [Needle::Compile]         ok 71 - and miss 'oofooff'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing :auto("§foo")
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit ' foo '
  [Needle::Compile]         ok 76 - hit ':foo:'
  [Needle::Compile]         ok 77 - miss 'oofooff'
  [Needle::Compile]         ok 78 - miss 'bar'
  [Needle::Compile]         ok 79 - Testing :not(:auto("§foo"))
  [Needle::Compile]         ok 80 - not hit 'foo'
  [Needle::Compile]         ok 81 - not hit ' foo '
  [Needle::Compile]         ok 82 - not hit ':foo:'
  [Needle::Compile]         ok 83 - not miss 'oofooff'
  [Needle::Compile]         ok 84 - not miss 'bar'
  [Needle::Compile]         ok 85 - Testing :and(:auto("§foo"))
  [Needle::Compile]         ok 86 - and hit 'foo'
  [Needle::Compile]         ok 87 - and hit ' foo '
  [Needle::Compile]         ok 88 - and hit ':foo:'
  [Needle::Compile]         ok 89 - and miss 'oofooff'
  [Needle::Compile]         ok 90 - and miss 'bar'
  [Needle::Compile]         ok 91 - Testing "!§foo"
  [Needle::Compile]         ok 92 - ! hit 'foo'
  [Needle::Compile]         ok 93 - ! hit ' foo '
  [Needle::Compile]         ok 94 - ! hit ':foo:'
  [Needle::Compile]         ok 95 - ! miss 'oofooff'
  [Needle::Compile]         ok 96 - ! miss 'bar'
  [Needle::Compile]         ok 97 - Testing "foo" but Type('words')
  [Needle::Compile]         ok 98 - returned 'foo'
  [Needle::Compile]         ok 99 - returned ' foo '
  [Needle::Compile]         ok 100 - returned ':foo:'
  [Needle::Compile]         ok 101 - miss 'oofooff'
  [Needle::Compile]         ok 102 - miss 'bar'
  [Needle::Compile]         ok 103 - Testing "§foo"
  [Needle::Compile]         ok 104 - returned 'foo'
  [Needle::Compile]         ok 105 - returned ' foo '
  [Needle::Compile]         ok 106 - returned ':foo:'
  [Needle::Compile]         ok 107 - miss 'oofooff'
  [Needle::Compile]         ok 108 - miss 'bar'
  [Needle::Compile]         ok 109 - Testing :words("foo")
  [Needle::Compile]         ok 110 - returned 'foo'
  [Needle::Compile]         ok 111 - returned ' foo '
  [Needle::Compile]         ok 112 - returned ':foo:'
  [Needle::Compile]         ok 113 - miss 'oofooff'
  [Needle::Compile]         ok 114 - miss 'bar'
  [Needle::Compile]     ok 3 - words: words simple 'foo', :ignoremark
  [Needle::Compile]     # Subtest: words: words simple 'foo', :smartcase
  [Needle::Compile]         1..114
  [Needle::Compile]         ok 1 - Testing "foo" but Type('words')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit ' foo '
  [Needle::Compile]         ok 4 - hit ':foo:'
  [Needle::Compile]         ok 5 - miss 'oofooff'
  [Needle::Compile]         ok 6 - miss 'bar'
  [Needle::Compile]         ok 7 - Testing :not("foo" but Type('words'))
  [Needle::Compile]         ok 8 - not hit 'foo'
  [Needle::Compile]         ok 9 - not hit ' foo '
  [Needle::Compile]         ok 10 - not hit ':foo:'
  [Needle::Compile]         ok 11 - not miss 'oofooff'
  [Needle::Compile]         ok 12 - not miss 'bar'
  [Needle::Compile]         ok 13 - Testing :and("foo" but Type('words'))
  [Needle::Compile]         ok 14 - and hit 'foo'
  [Needle::Compile]         ok 15 - and hit ' foo '
  [Needle::Compile]         ok 16 - and hit ':foo:'
  [Needle::Compile]         ok 17 - and miss 'oofooff'
  [Needle::Compile]         ok 18 - and miss 'bar'
  [Needle::Compile]         ok 19 - Testing "§foo"
  [Needle::Compile]         ok 20 - hit 'foo'
  [Needle::Compile]         ok 21 - hit ' foo '
  [Needle::Compile]         ok 22 - hit ':foo:'
  [Needle::Compile]         ok 23 - miss 'oofooff'
  [Needle::Compile]         ok 24 - miss 'bar'
  [Needle::Compile]         ok 25 - Testing :not("§foo")
  [Needle::Compile]         ok 26 - not hit 'foo'
  [Needle::Compile]         ok 27 - not hit ' foo '
  [Needle::Compile]         ok 28 - not hit ':foo:'
  [Needle::Compile]         ok 29 - not miss 'oofooff'
  [Needle::Compile]         ok 30 - not miss 'bar'
  [Needle::Compile]         ok 31 - Testing :and("§foo")
  [Needle::Compile]         ok 32 - and hit 'foo'
  [Needle::Compile]         ok 33 - and hit ' foo '
  [Needle::Compile]         ok 34 - and hit ':foo:'
  [Needle::Compile]         ok 35 - and miss 'oofooff'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "§foo" but Type('auto')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit ' foo '
  [Needle::Compile]         ok 40 - hit ':foo:'
  [Needle::Compile]         ok 41 - miss 'oofooff'
  [Needle::Compile]         ok 42 - miss 'bar'
  [Needle::Compile]         ok 43 - Testing :not("§foo" but Type('auto'))
  [Needle::Compile]         ok 44 - not hit 'foo'
  [Needle::Compile]         ok 45 - not hit ' foo '
  [Needle::Compile]         ok 46 - not hit ':foo:'
  [Needle::Compile]         ok 47 - not miss 'oofooff'
  [Needle::Compile]         ok 48 - not miss 'bar'
  [Needle::Compile]         ok 49 - Testing :and("§foo" but Type('auto'))
  [Needle::Compile]         ok 50 - and hit 'foo'
  [Needle::Compile]         ok 51 - and hit ' foo '
  [Needle::Compile]         ok 52 - and hit ':foo:'
  [Needle::Compile]         ok 53 - and miss 'oofooff'
  [Needle::Compile]         ok 54 - and miss 'bar'
  [Needle::Compile]         ok 55 - Testing :words("foo")
  [Needle::Compile]         ok 56 - hit 'foo'
  [Needle::Compile]         ok 57 - hit ' foo '
  [Needle::Compile]         ok 58 - hit ':foo:'
  [Needle::Compile]         ok 59 - miss 'oofooff'
  [Needle::Compile]         ok 60 - miss 'bar'
  [Needle::Compile]         ok 61 - Testing :not(:words("foo"))
  [Needle::Compile]         ok 62 - not hit 'foo'
  [Needle::Compile]         ok 63 - not hit ' foo '
  [Needle::Compile]         ok 64 - not hit ':foo:'
  [Needle::Compile]         ok 65 - not miss 'oofooff'
  [Needle::Compile]         ok 66 - not miss 'bar'
  [Needle::Compile]         ok 67 - Testing :and(:words("foo"))
  [Needle::Compile]         ok 68 - and hit 'foo'
  [Needle::Compile]         ok 69 - and hit ' foo '
  [Needle::Compile]         ok 70 - and hit ':foo:'
  [Needle::Compile]         ok 71 - and miss 'oofooff'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing :auto("§foo")
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit ' foo '
  [Needle::Compile]         ok 76 - hit ':foo:'
  [Needle::Compile]         ok 77 - miss 'oofooff'
  [Needle::Compile]         ok 78 - miss 'bar'
  [Needle::Compile]         ok 79 - Testing :not(:auto("§foo"))
  [Needle::Compile]         ok 80 - not hit 'foo'
  [Needle::Compile]         ok 81 - not hit ' foo '
  [Needle::Compile]         ok 82 - not hit ':foo:'
  [Needle::Compile]         ok 83 - not miss 'oofooff'
  [Needle::Compile]         ok 84 - not miss 'bar'
  [Needle::Compile]         ok 85 - Testing :and(:auto("§foo"))
  [Needle::Compile]         ok 86 - and hit 'foo'
  [Needle::Compile]         ok 87 - and hit ' foo '
  [Needle::Compile]         ok 88 - and hit ':foo:'
  [Needle::Compile]         ok 89 - and miss 'oofooff'
  [Needle::Compile]         ok 90 - and miss 'bar'
  [Needle::Compile]         ok 91 - Testing "!§foo"
  [Needle::Compile]         ok 92 - ! hit 'foo'
  [Needle::Compile]         ok 93 - ! hit ' foo '
  [Needle::Compile]         ok 94 - ! hit ':foo:'
  [Needle::Compile]         ok 95 - ! miss 'oofooff'
  [Needle::Compile]         ok 96 - ! miss 'bar'
  [Needle::Compile]         ok 97 - Testing "foo" but Type('words')
  [Needle::Compile]         ok 98 - returned 'foo'
  [Needle::Compile]         ok 99 - returned ' foo '
  [Needle::Compile]         ok 100 - returned ':foo:'
  [Needle::Compile]         ok 101 - miss 'oofooff'
  [Needle::Compile]         ok 102 - miss 'bar'
  [Needle::Compile]         ok 103 - Testing "§foo"
  [Needle::Compile]         ok 104 - returned 'foo'
  [Needle::Compile]         ok 105 - returned ' foo '
  [Needle::Compile]         ok 106 - returned ':foo:'
  [Needle::Compile]         ok 107 - miss 'oofooff'
  [Needle::Compile]         ok 108 - miss 'bar'
  [Needle::Compile]         ok 109 - Testing :words("foo")
  [Needle::Compile]         ok 110 - returned 'foo'
  [Needle::Compile]         ok 111 - returned ' foo '
  [Needle::Compile]         ok 112 - returned ':foo:'
  [Needle::Compile]         ok 113 - miss 'oofooff'
  [Needle::Compile]         ok 114 - miss 'bar'
  [Needle::Compile]     ok 4 - words: words simple 'foo', :smartcase
  [Needle::Compile]     # Subtest: words: words simple 'foo', :smartmark
  [Needle::Compile]         1..114
  [Needle::Compile]         ok 1 - Testing "foo" but Type('words')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit ' foo '
  [Needle::Compile]         ok 4 - hit ':foo:'
  [Needle::Compile]         ok 5 - miss 'oofooff'
  [Needle::Compile]         ok 6 - miss 'bar'
  [Needle::Compile]         ok 7 - Testing :not("foo" but Type('words'))
  [Needle::Compile]         ok 8 - not hit 'foo'
  [Needle::Compile]         ok 9 - not hit ' foo '
  [Needle::Compile]         ok 10 - not hit ':foo:'
  [Needle::Compile]         ok 11 - not miss 'oofooff'
  [Needle::Compile]         ok 12 - not miss 'bar'
  [Needle::Compile]         ok 13 - Testing :and("foo" but Type('words'))
  [Needle::Compile]         ok 14 - and hit 'foo'
  [Needle::Compile]         ok 15 - and hit ' foo '
  [Needle::Compile]         ok 16 - and hit ':foo:'
  [Needle::Compile]         ok 17 - and miss 'oofooff'
  [Needle::Compile]         ok 18 - and miss 'bar'
  [Needle::Compile]         ok 19 - Testing "§foo"
  [Needle::Compile]         ok 20 - hit 'foo'
  [Needle::Compile]         ok 21 - hit ' foo '
  [Needle::Compile]         ok 22 - hit ':foo:'
  [Needle::Compile]         ok 23 - miss 'oofooff'
  [Needle::Compile]         ok 24 - miss 'bar'
  [Needle::Compile]         ok 25 - Testing :not("§foo")
  [Needle::Compile]         ok 26 - not hit 'foo'
  [Needle::Compile]         ok 27 - not hit ' foo '
  [Needle::Compile]         ok 28 - not hit ':foo:'
  [Needle::Compile]         ok 29 - not miss 'oofooff'
  [Needle::Compile]         ok 30 - not miss 'bar'
  [Needle::Compile]         ok 31 - Testing :and("§foo")
  [Needle::Compile]         ok 32 - and hit 'foo'
  [Needle::Compile]         ok 33 - and hit ' foo '
  [Needle::Compile]         ok 34 - and hit ':foo:'
  [Needle::Compile]         ok 35 - and miss 'oofooff'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "§foo" but Type('auto')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit ' foo '
  [Needle::Compile]         ok 40 - hit ':foo:'
  [Needle::Compile]         ok 41 - miss 'oofooff'
  [Needle::Compile]         ok 42 - miss 'bar'
  [Needle::Compile]         ok 43 - Testing :not("§foo" but Type('auto'))
  [Needle::Compile]         ok 44 - not hit 'foo'
  [Needle::Compile]         ok 45 - not hit ' foo '
  [Needle::Compile]         ok 46 - not hit ':foo:'
  [Needle::Compile]         ok 47 - not miss 'oofooff'
  [Needle::Compile]         ok 48 - not miss 'bar'
  [Needle::Compile]         ok 49 - Testing :and("§foo" but Type('auto'))
  [Needle::Compile]         ok 50 - and hit 'foo'
  [Needle::Compile]         ok 51 - and hit ' foo '
  [Needle::Compile]         ok 52 - and hit ':foo:'
  [Needle::Compile]         ok 53 - and miss 'oofooff'
  [Needle::Compile]         ok 54 - and miss 'bar'
  [Needle::Compile]         ok 55 - Testing :words("foo")
  [Needle::Compile]         ok 56 - hit 'foo'
  [Needle::Compile]         ok 57 - hit ' foo '
  [Needle::Compile]         ok 58 - hit ':foo:'
  [Needle::Compile]         ok 59 - miss 'oofooff'
  [Needle::Compile]         ok 60 - miss 'bar'
  [Needle::Compile]         ok 61 - Testing :not(:words("foo"))
  [Needle::Compile]         ok 62 - not hit 'foo'
  [Needle::Compile]         ok 63 - not hit ' foo '
  [Needle::Compile]         ok 64 - not hit ':foo:'
  [Needle::Compile]         ok 65 - not miss 'oofooff'
  [Needle::Compile]         ok 66 - not miss 'bar'
  [Needle::Compile]         ok 67 - Testing :and(:words("foo"))
  [Needle::Compile]         ok 68 - and hit 'foo'
  [Needle::Compile]         ok 69 - and hit ' foo '
  [Needle::Compile]         ok 70 - and hit ':foo:'
  [Needle::Compile]         ok 71 - and miss 'oofooff'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing :auto("§foo")
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit ' foo '
  [Needle::Compile]         ok 76 - hit ':foo:'
  [Needle::Compile]         ok 77 - miss 'oofooff'
  [Needle::Compile]         ok 78 - miss 'bar'
  [Needle::Compile]         ok 79 - Testing :not(:auto("§foo"))
  [Needle::Compile]         ok 80 - not hit 'foo'
  [Needle::Compile]         ok 81 - not hit ' foo '
  [Needle::Compile]         ok 82 - not hit ':foo:'
  [Needle::Compile]         ok 83 - not miss 'oofooff'
  [Needle::Compile]         ok 84 - not miss 'bar'
  [Needle::Compile]         ok 85 - Testing :and(:auto("§foo"))
  [Needle::Compile]         ok 86 - and hit 'foo'
  [Needle::Compile]         ok 87 - and hit ' foo '
  [Needle::Compile]         ok 88 - and hit ':foo:'
  [Needle::Compile]         ok 89 - and miss 'oofooff'
  [Needle::Compile]         ok 90 - and miss 'bar'
  [Needle::Compile]         ok 91 - Testing "!§foo"
  [Needle::Compile]         ok 92 - ! hit 'foo'
  [Needle::Compile]         ok 93 - ! hit ' foo '
  [Needle::Compile]         ok 94 - ! hit ':foo:'
  [Needle::Compile]         ok 95 - ! miss 'oofooff'
  [Needle::Compile]         ok 96 - ! miss 'bar'
  [Needle::Compile]         ok 97 - Testing "foo" but Type('words')
  [Needle::Compile]         ok 98 - returned 'foo'
  [Needle::Compile]         ok 99 - returned ' foo '
  [Needle::Compile]         ok 100 - returned ':foo:'
  [Needle::Compile]         ok 101 - miss 'oofooff'
  [Needle::Compile]         ok 102 - miss 'bar'
  [Needle::Compile]         ok 103 - Testing "§foo"
  [Needle::Compile]         ok 104 - returned 'foo'
  [Needle::Compile]         ok 105 - returned ' foo '
  [Needle::Compile]         ok 106 - returned ':foo:'
  [Needle::Compile]         ok 107 - miss 'oofooff'
  [Needle::Compile]         ok 108 - miss 'bar'
  [Needle::Compile]         ok 109 - Testing :words("foo")
  [Needle::Compile]         ok 110 - returned 'foo'
  [Needle::Compile]         ok 111 - returned ' foo '
  [Needle::Compile]         ok 112 - returned ':foo:'
  [Needle::Compile]         ok 113 - miss 'oofooff'
  [Needle::Compile]         ok 114 - miss 'bar'
  [Needle::Compile]     ok 5 - words: words simple 'foo', :smartmark
  [Needle::Compile] ok 9 - all named arguments for words
  [Needle::Compile] # Subtest: all named arguments for regex
  [Needle::Compile]     1..5
  [Needle::Compile]     # Subtest: regex: regex simple 'foo'
  [Needle::Compile]         1..76
  [Needle::Compile]         ok 1 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit ' foo '
  [Needle::Compile]         ok 4 - miss ':;!'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit ' foo '
  [Needle::Compile]         ok 8 - not miss ':;!'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit ' foo '
  [Needle::Compile]         ok 12 - and miss ':;!'
  [Needle::Compile]         ok 13 - Testing "/ foo /"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit ' foo '
  [Needle::Compile]         ok 16 - miss ':;!'
  [Needle::Compile]         ok 17 - Testing :not("/ foo /")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit ' foo '
  [Needle::Compile]         ok 20 - not miss ':;!'
  [Needle::Compile]         ok 21 - Testing :and("/ foo /")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit ' foo '
  [Needle::Compile]         ok 24 - and miss ':;!'
  [Needle::Compile]         ok 25 - Testing "/ foo /" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit ' foo '
  [Needle::Compile]         ok 28 - miss ':;!'
  [Needle::Compile]         ok 29 - Testing :not("/ foo /" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit ' foo '
  [Needle::Compile]         ok 32 - not miss ':;!'
  [Needle::Compile]         ok 33 - Testing :and("/ foo /" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit ' foo '
  [Needle::Compile]         ok 36 - and miss ':;!'
  [Needle::Compile]         ok 37 - Testing :regex("foo")
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit ' foo '
  [Needle::Compile]         ok 40 - miss ':;!'
  [Needle::Compile]         ok 41 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit ' foo '
  [Needle::Compile]         ok 44 - not miss ':;!'
  [Needle::Compile]         ok 45 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit ' foo '
  [Needle::Compile]         ok 48 - and miss ':;!'
  [Needle::Compile]         ok 49 - Testing :auto("/ foo /")
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit ' foo '
  [Needle::Compile]         ok 52 - miss ':;!'
  [Needle::Compile]         ok 53 - Testing :not(:auto("/ foo /"))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit ' foo '
  [Needle::Compile]         ok 56 - not miss ':;!'
  [Needle::Compile]         ok 57 - Testing :and(:auto("/ foo /"))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit ' foo '
  [Needle::Compile]         ok 60 - and miss ':;!'
  [Needle::Compile]         ok 61 - Testing "!/ foo /"
  [Needle::Compile]         ok 62 - ! hit 'foo'
  [Needle::Compile]         ok 63 - ! hit ' foo '
  [Needle::Compile]         ok 64 - ! miss ':;!'
  [Needle::Compile]         ok 65 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 66 - returned 'foo'
  [Needle::Compile]         ok 67 - returned 'foo'
  [Needle::Compile]         ok 68 - miss ':;!'
  [Needle::Compile]         ok 69 - Testing "/ foo /"
  [Needle::Compile]         ok 70 - returned 'foo'
  [Needle::Compile]         ok 71 - returned 'foo'
  [Needle::Compile]         ok 72 - miss ':;!'
  [Needle::Compile]         ok 73 - Testing :regex("foo")
  [Needle::Compile]         ok 74 - returned 'foo'
  [Needle::Compile]         ok 75 - returned 'foo'
  [Needle::Compile]         ok 76 - miss ':;!'
  [Needle::Compile]     ok 1 - regex: regex simple 'foo'
  [Needle::Compile]     # Subtest: regex: regex simple 'foo', :ignorecase
  [Needle::Compile]         1..76
  [Needle::Compile]         ok 1 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit ' foo '
  [Needle::Compile]         ok 4 - miss ':;!'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit ' foo '
  [Needle::Compile]         ok 8 - not miss ':;!'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit ' foo '
  [Needle::Compile]         ok 12 - and miss ':;!'
  [Needle::Compile]         ok 13 - Testing "/ foo /"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit ' foo '
  [Needle::Compile]         ok 16 - miss ':;!'
  [Needle::Compile]         ok 17 - Testing :not("/ foo /")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit ' foo '
  [Needle::Compile]         ok 20 - not miss ':;!'
  [Needle::Compile]         ok 21 - Testing :and("/ foo /")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit ' foo '
  [Needle::Compile]         ok 24 - and miss ':;!'
  [Needle::Compile]         ok 25 - Testing "/ foo /" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit ' foo '
  [Needle::Compile]         ok 28 - miss ':;!'
  [Needle::Compile]         ok 29 - Testing :not("/ foo /" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit ' foo '
  [Needle::Compile]         ok 32 - not miss ':;!'
  [Needle::Compile]         ok 33 - Testing :and("/ foo /" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit ' foo '
  [Needle::Compile]         ok 36 - and miss ':;!'
  [Needle::Compile]         ok 37 - Testing :regex("foo")
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit ' foo '
  [Needle::Compile]         ok 40 - miss ':;!'
  [Needle::Compile]         ok 41 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit ' foo '
  [Needle::Compile]         ok 44 - not miss ':;!'
  [Needle::Compile]         ok 45 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit ' foo '
  [Needle::Compile]         ok 48 - and miss ':;!'
  [Needle::Compile]         ok 49 - Testing :auto("/ foo /")
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit ' foo '
  [Needle::Compile]         ok 52 - miss ':;!'
  [Needle::Compile]         ok 53 - Testing :not(:auto("/ foo /"))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit ' foo '
  [Needle::Compile]         ok 56 - not miss ':;!'
  [Needle::Compile]         ok 57 - Testing :and(:auto("/ foo /"))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit ' foo '
  [Needle::Compile]         ok 60 - and miss ':;!'
  [Needle::Compile]         ok 61 - Testing "!/ foo /"
  [Needle::Compile]         ok 62 - ! hit 'foo'
  [Needle::Compile]         ok 63 - ! hit ' foo '
  [Needle::Compile]         ok 64 - ! miss ':;!'
  [Needle::Compile]         ok 65 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 66 - returned 'foo'
  [Needle::Compile]         ok 67 - returned 'foo'
  [Needle::Compile]         ok 68 - miss ':;!'
  [Needle::Compile]         ok 69 - Testing "/ foo /"
  [Needle::Compile]         ok 70 - returned 'foo'
  [Needle::Compile]         ok 71 - returned 'foo'
  [Needle::Compile]         ok 72 - miss ':;!'
  [Needle::Compile]         ok 73 - Testing :regex("foo")
  [Needle::Compile]         ok 74 - returned 'foo'
  [Needle::Compile]         ok 75 - returned 'foo'
  [Needle::Compile]         ok 76 - miss ':;!'
  [Needle::Compile]     ok 2 - regex: regex simple 'foo', :ignorecase
  [Needle::Compile]     # Subtest: regex: regex simple 'foo', :ignoremark
  [Needle::Compile]         1..76
  [Needle::Compile]         ok 1 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit ' foo '
  [Needle::Compile]         ok 4 - miss ':;!'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit ' foo '
  [Needle::Compile]         ok 8 - not miss ':;!'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit ' foo '
  [Needle::Compile]         ok 12 - and miss ':;!'
  [Needle::Compile]         ok 13 - Testing "/ foo /"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit ' foo '
  [Needle::Compile]         ok 16 - miss ':;!'
  [Needle::Compile]         ok 17 - Testing :not("/ foo /")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit ' foo '
  [Needle::Compile]         ok 20 - not miss ':;!'
  [Needle::Compile]         ok 21 - Testing :and("/ foo /")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit ' foo '
  [Needle::Compile]         ok 24 - and miss ':;!'
  [Needle::Compile]         ok 25 - Testing "/ foo /" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit ' foo '
  [Needle::Compile]         ok 28 - miss ':;!'
  [Needle::Compile]         ok 29 - Testing :not("/ foo /" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit ' foo '
  [Needle::Compile]         ok 32 - not miss ':;!'
  [Needle::Compile]         ok 33 - Testing :and("/ foo /" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit ' foo '
  [Needle::Compile]         ok 36 - and miss ':;!'
  [Needle::Compile]         ok 37 - Testing :regex("foo")
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit ' foo '
  [Needle::Compile]         ok 40 - miss ':;!'
  [Needle::Compile]         ok 41 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit ' foo '
  [Needle::Compile]         ok 44 - not miss ':;!'
  [Needle::Compile]         ok 45 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit ' foo '
  [Needle::Compile]         ok 48 - and miss ':;!'
  [Needle::Compile]         ok 49 - Testing :auto("/ foo /")
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit ' foo '
  [Needle::Compile]         ok 52 - miss ':;!'
  [Needle::Compile]         ok 53 - Testing :not(:auto("/ foo /"))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit ' foo '
  [Needle::Compile]         ok 56 - not miss ':;!'
  [Needle::Compile]         ok 57 - Testing :and(:auto("/ foo /"))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit ' foo '
  [Needle::Compile]         ok 60 - and miss ':;!'
  [Needle::Compile]         ok 61 - Testing "!/ foo /"
  [Needle::Compile]         ok 62 - ! hit 'foo'
  [Needle::Compile]         ok 63 - ! hit ' foo '
  [Needle::Compile]         ok 64 - ! miss ':;!'
  [Needle::Compile]         ok 65 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 66 - returned 'foo'
  [Needle::Compile]         ok 67 - returned 'foo'
  [Needle::Compile]         ok 68 - miss ':;!'
  [Needle::Compile]         ok 69 - Testing "/ foo /"
  [Needle::Compile]         ok 70 - returned 'foo'
  [Needle::Compile]         ok 71 - returned 'foo'
  [Needle::Compile]         ok 72 - miss ':;!'
  [Needle::Compile]         ok 73 - Testing :regex("foo")
  [Needle::Compile]         ok 74 - returned 'foo'
  [Needle::Compile]         ok 75 - returned 'foo'
  [Needle::Compile]         ok 76 - miss ':;!'
  [Needle::Compile]     ok 3 - regex: regex simple 'foo', :ignoremark
  [Needle::Compile]     # Subtest: regex: regex simple 'foo', :smartcase
  [Needle::Compile]         1..76
  [Needle::Compile]         ok 1 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit ' foo '
  [Needle::Compile]         ok 4 - miss ':;!'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit ' foo '
  [Needle::Compile]         ok 8 - not miss ':;!'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit ' foo '
  [Needle::Compile]         ok 12 - and miss ':;!'
  [Needle::Compile]         ok 13 - Testing "/ foo /"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit ' foo '
  [Needle::Compile]         ok 16 - miss ':;!'
  [Needle::Compile]         ok 17 - Testing :not("/ foo /")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit ' foo '
  [Needle::Compile]         ok 20 - not miss ':;!'
  [Needle::Compile]         ok 21 - Testing :and("/ foo /")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit ' foo '
  [Needle::Compile]         ok 24 - and miss ':;!'
  [Needle::Compile]         ok 25 - Testing "/ foo /" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit ' foo '
  [Needle::Compile]         ok 28 - miss ':;!'
  [Needle::Compile]         ok 29 - Testing :not("/ foo /" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit ' foo '
  [Needle::Compile]         ok 32 - not miss ':;!'
  [Needle::Compile]         ok 33 - Testing :and("/ foo /" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit ' foo '
  [Needle::Compile]         ok 36 - and miss ':;!'
  [Needle::Compile]         ok 37 - Testing :regex("foo")
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit ' foo '
  [Needle::Compile]         ok 40 - miss ':;!'
  [Needle::Compile]         ok 41 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit ' foo '
  [Needle::Compile]         ok 44 - not miss ':;!'
  [Needle::Compile]         ok 45 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit ' foo '
  [Needle::Compile]         ok 48 - and miss ':;!'
  [Needle::Compile]         ok 49 - Testing :auto("/ foo /")
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit ' foo '
  [Needle::Compile]         ok 52 - miss ':;!'
  [Needle::Compile]         ok 53 - Testing :not(:auto("/ foo /"))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit ' foo '
  [Needle::Compile]         ok 56 - not miss ':;!'
  [Needle::Compile]         ok 57 - Testing :and(:auto("/ foo /"))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit ' foo '
  [Needle::Compile]         ok 60 - and miss ':;!'
  [Needle::Compile]         ok 61 - Testing "!/ foo /"
  [Needle::Compile]         ok 62 - ! hit 'foo'
  [Needle::Compile]         ok 63 - ! hit ' foo '
  [Needle::Compile]         ok 64 - ! miss ':;!'
  [Needle::Compile]         ok 65 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 66 - returned 'foo'
  [Needle::Compile]         ok 67 - returned 'foo'
  [Needle::Compile]         ok 68 - miss ':;!'
  [Needle::Compile]         ok 69 - Testing "/ foo /"
  [Needle::Compile]         ok 70 - returned 'foo'
  [Needle::Compile]         ok 71 - returned 'foo'
  [Needle::Compile]         ok 72 - miss ':;!'
  [Needle::Compile]         ok 73 - Testing :regex("foo")
  [Needle::Compile]         ok 74 - returned 'foo'
  [Needle::Compile]         ok 75 - returned 'foo'
  [Needle::Compile]         ok 76 - miss ':;!'
  [Needle::Compile]     ok 4 - regex: regex simple 'foo', :smartcase
  [Needle::Compile]     # Subtest: regex: regex simple 'foo', :smartmark
  [Needle::Compile]         1..76
  [Needle::Compile]         ok 1 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit ' foo '
  [Needle::Compile]         ok 4 - miss ':;!'
  [Needle::Compile]         ok 5 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit ' foo '
  [Needle::Compile]         ok 8 - not miss ':;!'
  [Needle::Compile]         ok 9 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit ' foo '
  [Needle::Compile]         ok 12 - and miss ':;!'
  [Needle::Compile]         ok 13 - Testing "/ foo /"
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit ' foo '
  [Needle::Compile]         ok 16 - miss ':;!'
  [Needle::Compile]         ok 17 - Testing :not("/ foo /")
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit ' foo '
  [Needle::Compile]         ok 20 - not miss ':;!'
  [Needle::Compile]         ok 21 - Testing :and("/ foo /")
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit ' foo '
  [Needle::Compile]         ok 24 - and miss ':;!'
  [Needle::Compile]         ok 25 - Testing "/ foo /" but Type('auto')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit ' foo '
  [Needle::Compile]         ok 28 - miss ':;!'
  [Needle::Compile]         ok 29 - Testing :not("/ foo /" but Type('auto'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit ' foo '
  [Needle::Compile]         ok 32 - not miss ':;!'
  [Needle::Compile]         ok 33 - Testing :and("/ foo /" but Type('auto'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit ' foo '
  [Needle::Compile]         ok 36 - and miss ':;!'
  [Needle::Compile]         ok 37 - Testing :regex("foo")
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit ' foo '
  [Needle::Compile]         ok 40 - miss ':;!'
  [Needle::Compile]         ok 41 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit ' foo '
  [Needle::Compile]         ok 44 - not miss ':;!'
  [Needle::Compile]         ok 45 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit ' foo '
  [Needle::Compile]         ok 48 - and miss ':;!'
  [Needle::Compile]         ok 49 - Testing :auto("/ foo /")
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit ' foo '
  [Needle::Compile]         ok 52 - miss ':;!'
  [Needle::Compile]         ok 53 - Testing :not(:auto("/ foo /"))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit ' foo '
  [Needle::Compile]         ok 56 - not miss ':;!'
  [Needle::Compile]         ok 57 - Testing :and(:auto("/ foo /"))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit ' foo '
  [Needle::Compile]         ok 60 - and miss ':;!'
  [Needle::Compile]         ok 61 - Testing "!/ foo /"
  [Needle::Compile]         ok 62 - ! hit 'foo'
  [Needle::Compile]         ok 63 - ! hit ' foo '
  [Needle::Compile]         ok 64 - ! miss ':;!'
  [Needle::Compile]         ok 65 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 66 - returned 'foo'
  [Needle::Compile]         ok 67 - returned 'foo'
  [Needle::Compile]         ok 68 - miss ':;!'
  [Needle::Compile]         ok 69 - Testing "/ foo /"
  [Needle::Compile]         ok 70 - returned 'foo'
  [Needle::Compile]         ok 71 - returned 'foo'
  [Needle::Compile]         ok 72 - miss ':;!'
  [Needle::Compile]         ok 73 - Testing :regex("foo")
  [Needle::Compile]         ok 74 - returned 'foo'
  [Needle::Compile]         ok 75 - returned 'foo'
  [Needle::Compile]         ok 76 - miss ':;!'
  [Needle::Compile]     ok 5 - regex: regex simple 'foo', :smartmark
  [Needle::Compile] ok 10 - all named arguments for regex
  [Needle::Compile] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz/Needle-Compile-0.0.12 t/03-file.rakutest
  [Needle::Compile] 1..9
  [Needle::Compile] ok 1 - is it a Callable
  [Needle::Compile] ok 2 - matched "foo"
  [Needle::Compile] ok 3 - did not match "bar"
  [Needle::Compile] # Subtest: file: "file:t/always"
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched "foo"
  [Needle::Compile]     ok 3 - did not match "bar"
  [Needle::Compile]     1..3
  [Needle::Compile] ok 4 - file: "file:t/always"
  [Needle::Compile] # Subtest: file: "t/always" but Type('file')
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched "foo"
  [Needle::Compile]     ok 3 - did not match "bar"
  [Needle::Compile]     1..3
  [Needle::Compile] ok 5 - file: "t/always" but Type('file')
  [Needle::Compile] # Subtest: file: :file("t/always")
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched "foo"
  [Needle::Compile]     ok 3 - did not match "bar"
  [Needle::Compile]     1..3
  [Needle::Compile] ok 6 - file: :file("t/always")
  [Needle::Compile] # Subtest: not file: "!file:t/always"
  [Needle::Compile]     1..3
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - did not match "foo"
  [Needle::Compile]     ok 3 - matched "bar"
  [Needle::Compile] ok 7 - not file: "!file:t/always"
  [Needle::Compile] # Subtest: not file: :not("file:t/always")
  [Needle::Compile]     1..3
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - did not match "foo"
  [Needle::Compile]     ok 3 - matched "bar"
  [Needle::Compile] ok 8 - not file: :not("file:t/always")
  [Needle::Compile] # Subtest: not file: :not(:file("t/always"))
  [Needle::Compile]     1..3
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - did not match "foo"
  [Needle::Compile]     ok 3 - matched "bar"
  [Needle::Compile] ok 9 - not file: :not(:file("t/always"))
  [Needle::Compile] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz/Needle-Compile-0.0.12 t/04-multiple.rakutest
  [Needle::Compile] 1..16
  [Needle::Compile] # Subtest: or: $("foo", "§bar")
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 1 - or: $("foo", "§bar")
  [Needle::Compile] # Subtest: or: $("\&foo", "§bar")
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 2 - or: $("\&foo", "§bar")
  [Needle::Compile] # Subtest: or: $("foo" but Type('contains'), "bar" but Type('words'))
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 3 - or: $("foo" but Type('contains'), "bar" but Type('words'))
  [Needle::Compile] # Subtest: or: $(:contains("foo"), :words("bar"))
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 4 - or: $(:contains("foo"), :words("bar"))
  [Needle::Compile] # Subtest: or: "s:foo §bar"
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 5 - or: "s:foo §bar"
  [Needle::Compile] # Subtest: or: :split("foo §bar")
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 6 - or: :split("foo §bar")
  [Needle::Compile] # Subtest: or: "foo    §bar" but Type('split')
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 7 - or: "foo    §bar" but Type('split')
  [Needle::Compile] # Subtest: and: $("foo", "\&§bar")
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 8 - and: $("foo", "\&§bar")
  [Needle::Compile] # Subtest: and: $("foo" but Type('contains'), :and("bar" but Type('words')))
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 9 - and: $("foo" but Type('contains'), :and("bar" but Type('words')))
  [Needle::Compile] # Subtest: and: $(:contains("foo"), :and(:words("bar")))
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 10 - and: $(:contains("foo"), :and(:words("bar")))
  [Needle::Compile] # Subtest: and: $("foo" but Type('contains'), "\&§bar")
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 11 - and: $("foo" but Type('contains'), "\&§bar")
  [Needle::Compile] # Subtest: and: $("foo", "§bar" but Type('and'))
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 12 - and: $("foo", "§bar" but Type('and'))
  [Needle::Compile] # Subtest: and: $("\&foo", "§bar" but Type('and'))
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 13 - and: $("\&foo", "§bar" but Type('and'))
  [Needle::Compile] # Subtest: and: "s:foo \&§bar"
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 14 - and: "s:foo \&§bar"
  [Needle::Compile] # Subtest: and: :split("foo \&§bar")
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 15 - and: :split("foo \&§bar")
  [Needle::Compile] # Subtest: and: "foo    \&§bar" but Type('split')
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 16 - and: "foo    \&§bar" but Type('split')
  ===> Testing [OK] for Needle::Compile:ver<0.0.12>:auth<zef:lizmat>
  ===> Installing: Needle::Compile:ver<0.0.12>:auth<zef:lizmat>
  ===> Install [OK] for Needle::Compile:ver<0.0.12>:auth<zef:lizmat>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 35.208s
               CPU time consumed: 52.148s
                     Memory peak: 1.1G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2395408-i2413694.service; invocation ID: a2929a7a9e4c40d29459e45e473689f3
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Needle::Compile
  ===> Found: Needle::Compile:ver<0.0.12>:auth<zef:lizmat> [via Zef::Repository::Ecosystems<fez>]
  [Needle::Compile] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788816865.2395409.1535.9262231877146/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz https://360.zef.pm/N/EE/NEEDLE_COMPILE/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz
  ===> Fetching [OK]: Needle::Compile:ver<0.0.12>:auth<zef:lizmat> to /home/coke/sandbox/blin/data/zef-data/tmp/1788816865.2395409.1535.9262231877146/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz
  [Needle::Compile] Command: tar -t -f ./66794ae2eb541201a403c08d48e27de668b32db7.tar.gz
  [Needle::Compile] Command: tar -xvf ./66794ae2eb541201a403c08d48e27de668b32db7.tar.gz -C ../66794ae2eb541201a403c08d48e27de668b32db7.tar.gz
  ===> Extraction [OK]: Needle::Compile to /home/coke/sandbox/blin/data/zef-data/tmp/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz
  ===> Testing: Needle::Compile:ver<0.0.12>:auth<zef:lizmat>
  [Needle::Compile] Command: /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz/Needle-Compile-0.0.12 t/01-basic.rakutest
  [Needle::Compile] 1..36
  [Needle::Compile] ok 1 - did compile-needle get exported
  [Needle::Compile] ok 2 - did implicit2explicit get exported
  [Needle::Compile] ok 3 - did Type get exported
  [Needle::Compile] ok 4 - did StrType get exported
  [Needle::Compile] ok 5 - it's a string
  [Needle::Compile] ok 6 - it's a butted string
  [Needle::Compile] ok 7 - not a butted string
  [Needle::Compile] ok 8 - is 'foo' *NOT* acceptable
  [Needle::Compile] ok 9 - is 'and' acceptable
  [Needle::Compile] ok 10 - is 'auto' acceptable
  [Needle::Compile] ok 11 - is 'code' acceptable
  [Needle::Compile] ok 12 - is 'contains' acceptable
  [Needle::Compile] ok 13 - is 'ends-with' acceptable
  [Needle::Compile] ok 14 - is 'equal' acceptable
  [Needle::Compile] ok 15 - is 'file' acceptable
  [Needle::Compile] ok 16 - is 'json-path' acceptable
  [Needle::Compile] ok 17 - is 'not' acceptable
  [Needle::Compile] ok 18 - is 'regex' acceptable
  [Needle::Compile] ok 19 - is 'split' acceptable
  [Needle::Compile] ok 20 - is 'starts-with' acceptable
  [Needle::Compile] ok 21 - is 'words' acceptable
  [Needle::Compile] ok 22 - did 'foo' produce the correct explicit?
  [Needle::Compile] ok 23 - did '§foo' produce the correct explicit?
  [Needle::Compile] ok 24 - did '^foo' produce the correct explicit?
  [Needle::Compile] ok 25 - did 'foo$' produce the correct explicit?
  [Needle::Compile] ok 26 - did '^foo$' produce the correct explicit?
  [Needle::Compile] ok 27 - did 'url:foo' produce the correct explicit?
  [Needle::Compile] ok 28 - did 'file:foo' produce the correct explicit?
  [Needle::Compile] ok 29 - did 's:foo' produce the correct explicit?
  [Needle::Compile] ok 30 - did 'jp:foo' produce the correct explicit?
  [Needle::Compile] ok 31 - did '*.foo' produce the correct explicit?
  [Needle::Compile] ok 32 - did '{.foo}' produce the correct explicit?
  [Needle::Compile] ok 33 - did '/foo/' produce the correct explicit?
  [Needle::Compile] ok 34 - did '!foo' produce the correct explicit?
  [Needle::Compile] ok 35 - did '&foo' produce the correct explicit?
  [Needle::Compile] ok 36 - did we get an AST
  [Needle::Compile] Command: /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz/Needle-Compile-0.0.12 t/02-single.rakutest
  [Needle::Compile] 1..10
  [Needle::Compile] # Subtest: code: simple .subst
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - Testing ".subst(\"foo\", \"bar\")" but Type('code')
  [Needle::Compile]     ok 2 - 'foo' transformed ok
  [Needle::Compile]     ok 3 - Testing "\{.subst(\"foo\", \"bar\")}"
  [Needle::Compile]     ok 4 - 'foo' transformed ok
  [Needle::Compile]     ok 5 - Testing :code(".subst(\"foo\", \"bar\")")
  [Needle::Compile]     ok 6 - 'foo' transformed ok
  [Needle::Compile]     ok 7 - Testing "*.subst(\"foo\", \"bar\")"
  [Needle::Compile]     ok 8 - 'foo' transformed ok
  [Needle::Compile] ok 1 - code: simple .subst
  [Needle::Compile] # Subtest: code: simple .uc
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - Testing ".uc" but Type('code')
  [Needle::Compile]     ok 2 - 'foo' transformed ok
  [Needle::Compile]     ok 3 - Testing "\{.uc}"
  [Needle::Compile]     ok 4 - 'foo' transformed ok
  [Needle::Compile]     ok 5 - Testing :code(".uc")
  [Needle::Compile]     ok 6 - 'foo' transformed ok
  [Needle::Compile]     ok 7 - Testing "*.uc"
  [Needle::Compile]     ok 8 - 'foo' transformed ok
  [Needle::Compile] ok 2 - code: simple .uc
  [Needle::Compile] # Subtest: code: check availability of $*_
  [Needle::Compile]     1..6
  [Needle::Compile]     ok 1 - Testing "\$*_ eq \$_" but Type('code')
  [Needle::Compile]     ok 2 - 'foo' transformed ok
  [Needle::Compile]     ok 3 - Testing "\{\$*_ eq \$_}"
  [Needle::Compile]     ok 4 - 'foo' transformed ok
  [Needle::Compile]     ok 5 - Testing :code("\$*_ eq \$_")
  [Needle::Compile]     ok 6 - 'foo' transformed ok
  [Needle::Compile] ok 3 - code: check availability of $*_
  [Needle::Compile] # Subtest: code: check loading of Test module
  [Needle::Compile]     1..9
  [Needle::Compile]     ok 1 - Testing "is \$_, 42" but Type('code')
  [Needle::Compile]     ok 2 - 
  [Needle::Compile]     ok 3 - '42' transformed ok
  [Needle::Compile]     ok 4 - Testing "\{is \$_, 42}"
  [Needle::Compile]     ok 5 - 
  [Needle::Compile]     ok 6 - '42' transformed ok
  [Needle::Compile]     ok 7 - Testing :code("is \$_, 42")
  [Needle::Compile]     ok 8 - 
  [Needle::Compile]     ok 9 - '42' transformed ok
  [Needle::Compile] ok 4 - code: check loading of Test module
  [Needle::Compile] # Subtest: all named arguments for contains
  [Needle::Compile]     1..5
  [Needle::Compile]     # Subtest: contains: find simple 'foo'
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo"
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit 'infooout'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo")
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit 'infooout'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo")
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit 'infooout'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo" but Type('auto')
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit 'infooout'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo" but Type('auto'))
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit 'infooout'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo" but Type('auto'))
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit 'infooout'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit 'infooout'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo" but Type('contains'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit 'infooout'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo" but Type('contains'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit 'infooout'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit 'infooout'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit 'infooout'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit 'infooout'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".contains('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit 'infooout'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit 'infooout'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit 'infooout'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - hit 'infooout'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not hit 'infooout'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and hit 'infooout'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.contains('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit 'infooout'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.contains('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not hit 'infooout'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.contains('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and hit 'infooout'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.contains('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - hit 'infooout'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.contains('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not hit 'infooout'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.contains('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and hit 'infooout'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :auto("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - hit 'infooout'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:auto("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not hit 'infooout'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:auto("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and hit 'infooout'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :contains("foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - hit 'infooout'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:contains("foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not hit 'infooout'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:contains("foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and hit 'infooout'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - hit 'infooout'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not hit 'infooout'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and hit 'infooout'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".contains('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - hit 'infooout'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".contains('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not hit 'infooout'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".contains('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and hit 'infooout'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! hit 'infooout'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! hit 'infooout'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.contains('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! hit 'infooout'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.contains('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! hit 'infooout'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo"
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 162 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 163 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo" but Type('contains')
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 166 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 167 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo" but Type('regex')
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 170 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 171 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo/"
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 174 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 175 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :contains("foo")
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 178 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 179 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo")
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 182 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 183 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]         # You failed 12 tests of 184
  [Needle::Compile]     not ok 1 - contains: find simple 'foo'
  [Needle::Compile]     # Failed test 'contains: find simple 'foo''
  [Needle::Compile]     # at t/02-single.rakutest line 14
  [Needle::Compile]     # Subtest: contains: find simple 'foo', :ignorecase, :ignorecase
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo"
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit 'infooout'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo")
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit 'infooout'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo")
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit 'infooout'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo" but Type('auto')
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit 'infooout'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo" but Type('auto'))
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit 'infooout'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo" but Type('auto'))
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit 'infooout'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit 'infooout'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo" but Type('contains'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit 'infooout'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo" but Type('contains'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit 'infooout'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit 'infooout'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit 'infooout'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit 'infooout'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".contains('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit 'infooout'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit 'infooout'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit 'infooout'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - hit 'infooout'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not hit 'infooout'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and hit 'infooout'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.contains('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit 'infooout'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.contains('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not hit 'infooout'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.contains('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and hit 'infooout'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.contains('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - hit 'infooout'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.contains('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not hit 'infooout'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.contains('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and hit 'infooout'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :auto("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - hit 'infooout'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:auto("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not hit 'infooout'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:auto("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and hit 'infooout'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :contains("foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - hit 'infooout'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:contains("foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not hit 'infooout'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:contains("foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and hit 'infooout'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - hit 'infooout'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not hit 'infooout'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and hit 'infooout'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".contains('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - hit 'infooout'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".contains('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not hit 'infooout'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".contains('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and hit 'infooout'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! hit 'infooout'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! hit 'infooout'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.contains('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! hit 'infooout'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.contains('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! hit 'infooout'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo"
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 162 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 163 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo" but Type('contains')
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 166 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 167 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo" but Type('regex')
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 170 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 171 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo/"
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 174 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 175 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :contains("foo")
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 178 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 179 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo")
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 182 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 183 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]         # You failed 12 tests of 184
  [Needle::Compile]     not ok 2 - contains: find simple 'foo', :ignorecase, :ignorecase
  [Needle::Compile]     # Failed test 'contains: find simple 'foo', :ignorecase, :ignorecase'
  [Needle::Compile]     # at t/02-single.rakutest line 14
  [Needle::Compile]     # Subtest: contains: find simple 'foo', :ignoremark, :ignoremark
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo"
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit 'infooout'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo")
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit 'infooout'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo")
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit 'infooout'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo" but Type('auto')
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit 'infooout'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo" but Type('auto'))
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit 'infooout'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo" but Type('auto'))
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit 'infooout'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit 'infooout'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo" but Type('contains'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit 'infooout'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo" but Type('contains'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit 'infooout'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit 'infooout'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit 'infooout'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit 'infooout'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".contains('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit 'infooout'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit 'infooout'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit 'infooout'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - hit 'infooout'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not hit 'infooout'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and hit 'infooout'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.contains('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit 'infooout'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.contains('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not hit 'infooout'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.contains('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and hit 'infooout'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.contains('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - hit 'infooout'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.contains('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not hit 'infooout'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.contains('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and hit 'infooout'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :auto("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - hit 'infooout'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:auto("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not hit 'infooout'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:auto("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and hit 'infooout'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :contains("foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - hit 'infooout'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:contains("foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not hit 'infooout'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:contains("foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and hit 'infooout'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - hit 'infooout'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not hit 'infooout'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and hit 'infooout'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".contains('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - hit 'infooout'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".contains('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not hit 'infooout'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".contains('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and hit 'infooout'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! hit 'infooout'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! hit 'infooout'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.contains('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! hit 'infooout'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.contains('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! hit 'infooout'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo"
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 162 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 163 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo" but Type('contains')
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 166 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 167 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo" but Type('regex')
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 170 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 171 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo/"
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 174 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 175 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :contains("foo")
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 178 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 179 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo")
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 182 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 183 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]         # You failed 12 tests of 184
  [Needle::Compile]     not ok 3 - contains: find simple 'foo', :ignoremark, :ignoremark
  [Needle::Compile]     # Failed test 'contains: find simple 'foo', :ignoremark, :ignoremark'
  [Needle::Compile]     # at t/02-single.rakutest line 14
  [Needle::Compile]     # Subtest: contains: find simple 'foo', :smartcase, :smartcase
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo"
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit 'infooout'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo")
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit 'infooout'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo")
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit 'infooout'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo" but Type('auto')
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit 'infooout'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo" but Type('auto'))
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit 'infooout'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo" but Type('auto'))
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit 'infooout'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit 'infooout'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo" but Type('contains'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit 'infooout'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo" but Type('contains'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit 'infooout'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit 'infooout'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit 'infooout'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit 'infooout'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".contains('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit 'infooout'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit 'infooout'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit 'infooout'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - hit 'infooout'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not hit 'infooout'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and hit 'infooout'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.contains('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit 'infooout'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.contains('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not hit 'infooout'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.contains('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and hit 'infooout'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.contains('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - hit 'infooout'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.contains('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not hit 'infooout'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.contains('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and hit 'infooout'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :auto("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - hit 'infooout'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:auto("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not hit 'infooout'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:auto("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and hit 'infooout'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :contains("foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - hit 'infooout'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:contains("foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not hit 'infooout'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:contains("foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and hit 'infooout'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - hit 'infooout'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not hit 'infooout'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and hit 'infooout'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".contains('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - hit 'infooout'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".contains('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not hit 'infooout'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".contains('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and hit 'infooout'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! hit 'infooout'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! hit 'infooout'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.contains('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! hit 'infooout'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.contains('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! hit 'infooout'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo"
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 162 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 163 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo" but Type('contains')
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 166 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 167 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo" but Type('regex')
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 170 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 171 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo/"
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 174 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 175 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :contains("foo")
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 178 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 179 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo")
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 182 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 183 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]         # You failed 12 tests of 184
  [Needle::Compile]     not ok 4 - contains: find simple 'foo', :smartcase, :smartcase
  [Needle::Compile]     # Failed test 'contains: find simple 'foo', :smartcase, :smartcase'
  [Needle::Compile]     # at t/02-single.rakutest line 14
  [Needle::Compile]     # Subtest: contains: find simple 'foo', :smartmark, :smartmark
  [Needle::Compile]         1..184
  [Needle::Compile]         ok 1 - Testing "foo"
  [Needle::Compile]         ok 2 - hit 'foo'
  [Needle::Compile]         ok 3 - hit 'infooout'
  [Needle::Compile]         ok 4 - miss 'bar'
  [Needle::Compile]         ok 5 - Testing :not("foo")
  [Needle::Compile]         ok 6 - not hit 'foo'
  [Needle::Compile]         ok 7 - not hit 'infooout'
  [Needle::Compile]         ok 8 - not miss 'bar'
  [Needle::Compile]         ok 9 - Testing :and("foo")
  [Needle::Compile]         ok 10 - and hit 'foo'
  [Needle::Compile]         ok 11 - and hit 'infooout'
  [Needle::Compile]         ok 12 - and miss 'bar'
  [Needle::Compile]         ok 13 - Testing "foo" but Type('auto')
  [Needle::Compile]         ok 14 - hit 'foo'
  [Needle::Compile]         ok 15 - hit 'infooout'
  [Needle::Compile]         ok 16 - miss 'bar'
  [Needle::Compile]         ok 17 - Testing :not("foo" but Type('auto'))
  [Needle::Compile]         ok 18 - not hit 'foo'
  [Needle::Compile]         ok 19 - not hit 'infooout'
  [Needle::Compile]         ok 20 - not miss 'bar'
  [Needle::Compile]         ok 21 - Testing :and("foo" but Type('auto'))
  [Needle::Compile]         ok 22 - and hit 'foo'
  [Needle::Compile]         ok 23 - and hit 'infooout'
  [Needle::Compile]         ok 24 - and miss 'bar'
  [Needle::Compile]         ok 25 - Testing "foo" but Type('contains')
  [Needle::Compile]         ok 26 - hit 'foo'
  [Needle::Compile]         ok 27 - hit 'infooout'
  [Needle::Compile]         ok 28 - miss 'bar'
  [Needle::Compile]         ok 29 - Testing :not("foo" but Type('contains'))
  [Needle::Compile]         ok 30 - not hit 'foo'
  [Needle::Compile]         ok 31 - not hit 'infooout'
  [Needle::Compile]         ok 32 - not miss 'bar'
  [Needle::Compile]         ok 33 - Testing :and("foo" but Type('contains'))
  [Needle::Compile]         ok 34 - and hit 'foo'
  [Needle::Compile]         ok 35 - and hit 'infooout'
  [Needle::Compile]         ok 36 - and miss 'bar'
  [Needle::Compile]         ok 37 - Testing "foo" but Type('regex')
  [Needle::Compile]         ok 38 - hit 'foo'
  [Needle::Compile]         ok 39 - hit 'infooout'
  [Needle::Compile]         ok 40 - miss 'bar'
  [Needle::Compile]         ok 41 - Testing :not("foo" but Type('regex'))
  [Needle::Compile]         ok 42 - not hit 'foo'
  [Needle::Compile]         ok 43 - not hit 'infooout'
  [Needle::Compile]         ok 44 - not miss 'bar'
  [Needle::Compile]         ok 45 - Testing :and("foo" but Type('regex'))
  [Needle::Compile]         ok 46 - and hit 'foo'
  [Needle::Compile]         ok 47 - and hit 'infooout'
  [Needle::Compile]         ok 48 - and miss 'bar'
  [Needle::Compile]         ok 49 - Testing ".contains('foo')" but Type('code')
  [Needle::Compile]         ok 50 - hit 'foo'
  [Needle::Compile]         ok 51 - hit 'infooout'
  [Needle::Compile]         ok 52 - miss 'bar'
  [Needle::Compile]         ok 53 - Testing :not(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 54 - not hit 'foo'
  [Needle::Compile]         ok 55 - not hit 'infooout'
  [Needle::Compile]         ok 56 - not miss 'bar'
  [Needle::Compile]         ok 57 - Testing :and(".contains('foo')" but Type('code'))
  [Needle::Compile]         ok 58 - and hit 'foo'
  [Needle::Compile]         ok 59 - and hit 'infooout'
  [Needle::Compile]         ok 60 - and miss 'bar'
  [Needle::Compile]         ok 61 - Testing "/foo/"
  [Needle::Compile]         ok 62 - hit 'foo'
  [Needle::Compile]         ok 63 - hit 'infooout'
  [Needle::Compile]         ok 64 - miss 'bar'
  [Needle::Compile]         ok 65 - Testing :not("/foo/")
  [Needle::Compile]         ok 66 - not hit 'foo'
  [Needle::Compile]         ok 67 - not hit 'infooout'
  [Needle::Compile]         ok 68 - not miss 'bar'
  [Needle::Compile]         ok 69 - Testing :and("/foo/")
  [Needle::Compile]         ok 70 - and hit 'foo'
  [Needle::Compile]         ok 71 - and hit 'infooout'
  [Needle::Compile]         ok 72 - and miss 'bar'
  [Needle::Compile]         ok 73 - Testing "\{.contains('foo')}"
  [Needle::Compile]         ok 74 - hit 'foo'
  [Needle::Compile]         ok 75 - hit 'infooout'
  [Needle::Compile]         ok 76 - miss 'bar'
  [Needle::Compile]         ok 77 - Testing :not("\{.contains('foo')}")
  [Needle::Compile]         ok 78 - not hit 'foo'
  [Needle::Compile]         ok 79 - not hit 'infooout'
  [Needle::Compile]         ok 80 - not miss 'bar'
  [Needle::Compile]         ok 81 - Testing :and("\{.contains('foo')}")
  [Needle::Compile]         ok 82 - and hit 'foo'
  [Needle::Compile]         ok 83 - and hit 'infooout'
  [Needle::Compile]         ok 84 - and miss 'bar'
  [Needle::Compile]         ok 85 - Testing "*.contains('foo')"
  [Needle::Compile]         ok 86 - hit 'foo'
  [Needle::Compile]         ok 87 - hit 'infooout'
  [Needle::Compile]         ok 88 - miss 'bar'
  [Needle::Compile]         ok 89 - Testing :not("*.contains('foo')")
  [Needle::Compile]         ok 90 - not hit 'foo'
  [Needle::Compile]         ok 91 - not hit 'infooout'
  [Needle::Compile]         ok 92 - not miss 'bar'
  [Needle::Compile]         ok 93 - Testing :and("*.contains('foo')")
  [Needle::Compile]         ok 94 - and hit 'foo'
  [Needle::Compile]         ok 95 - and hit 'infooout'
  [Needle::Compile]         ok 96 - and miss 'bar'
  [Needle::Compile]         ok 97 - Testing :auto("foo")
  [Needle::Compile]         ok 98 - hit 'foo'
  [Needle::Compile]         ok 99 - hit 'infooout'
  [Needle::Compile]         ok 100 - miss 'bar'
  [Needle::Compile]         ok 101 - Testing :not(:auto("foo"))
  [Needle::Compile]         ok 102 - not hit 'foo'
  [Needle::Compile]         ok 103 - not hit 'infooout'
  [Needle::Compile]         ok 104 - not miss 'bar'
  [Needle::Compile]         ok 105 - Testing :and(:auto("foo"))
  [Needle::Compile]         ok 106 - and hit 'foo'
  [Needle::Compile]         ok 107 - and hit 'infooout'
  [Needle::Compile]         ok 108 - and miss 'bar'
  [Needle::Compile]         ok 109 - Testing :contains("foo")
  [Needle::Compile]         ok 110 - hit 'foo'
  [Needle::Compile]         ok 111 - hit 'infooout'
  [Needle::Compile]         ok 112 - miss 'bar'
  [Needle::Compile]         ok 113 - Testing :not(:contains("foo"))
  [Needle::Compile]         ok 114 - not hit 'foo'
  [Needle::Compile]         ok 115 - not hit 'infooout'
  [Needle::Compile]         ok 116 - not miss 'bar'
  [Needle::Compile]         ok 117 - Testing :and(:contains("foo"))
  [Needle::Compile]         ok 118 - and hit 'foo'
  [Needle::Compile]         ok 119 - and hit 'infooout'
  [Needle::Compile]         ok 120 - and miss 'bar'
  [Needle::Compile]         ok 121 - Testing :regex("foo")
  [Needle::Compile]         ok 122 - hit 'foo'
  [Needle::Compile]         ok 123 - hit 'infooout'
  [Needle::Compile]         ok 124 - miss 'bar'
  [Needle::Compile]         ok 125 - Testing :not(:regex("foo"))
  [Needle::Compile]         ok 126 - not hit 'foo'
  [Needle::Compile]         ok 127 - not hit 'infooout'
  [Needle::Compile]         ok 128 - not miss 'bar'
  [Needle::Compile]         ok 129 - Testing :and(:regex("foo"))
  [Needle::Compile]         ok 130 - and hit 'foo'
  [Needle::Compile]         ok 131 - and hit 'infooout'
  [Needle::Compile]         ok 132 - and miss 'bar'
  [Needle::Compile]         ok 133 - Testing :code(".contains('foo')")
  [Needle::Compile]         ok 134 - hit 'foo'
  [Needle::Compile]         ok 135 - hit 'infooout'
  [Needle::Compile]         ok 136 - miss 'bar'
  [Needle::Compile]         ok 137 - Testing :not(:code(".contains('foo')"))
  [Needle::Compile]         ok 138 - not hit 'foo'
  [Needle::Compile]         ok 139 - not hit 'infooout'
  [Needle::Compile]         ok 140 - not miss 'bar'
  [Needle::Compile]         ok 141 - Testing :and(:code(".contains('foo')"))
  [Needle::Compile]         ok 142 - and hit 'foo'
  [Needle::Compile]         ok 143 - and hit 'infooout'
  [Needle::Compile]         ok 144 - and miss 'bar'
  [Needle::Compile]         ok 145 - Testing "!foo"
  [Needle::Compile]         ok 146 - ! hit 'foo'
  [Needle::Compile]         ok 147 - ! hit 'infooout'
  [Needle::Compile]         ok 148 - ! miss 'bar'
  [Needle::Compile]         ok 149 - Testing "!/foo/"
  [Needle::Compile]         ok 150 - ! hit 'foo'
  [Needle::Compile]         ok 151 - ! hit 'infooout'
  [Needle::Compile]         ok 152 - ! miss 'bar'
  [Needle::Compile]         ok 153 - Testing "!\{.contains('foo')}"
  [Needle::Compile]         ok 154 - ! hit 'foo'
  [Needle::Compile]         ok 155 - ! hit 'infooout'
  [Needle::Compile]         ok 156 - ! miss 'bar'
  [Needle::Compile]         ok 157 - Testing "!*.contains('foo')"
  [Needle::Compile]         ok 158 - ! hit 'foo'
  [Needle::Compile]         ok 159 - ! hit 'infooout'
  [Needle::Compile]         ok 160 - ! miss 'bar'
  [Needle::Compile]         ok 161 - Testing "foo"
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 162 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 163 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 164 - miss 'bar'
  [Needle::Compile]         ok 165 - Testing "foo" but Type('contains')
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 166 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 167 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 168 - miss 'bar'
  [Needle::Compile]         ok 169 - Testing "foo" but Type('regex')
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 170 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 171 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 172 - miss 'bar'
  [Needle::Compile]         ok 173 - Testing "/foo/"
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 174 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 175 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 176 - miss 'bar'
  [Needle::Compile]         ok 177 - Testing :contains("foo")
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 178 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 179 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 180 - miss 'bar'
  [Needle::Compile]         ok 181 - Testing :regex("foo")
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 182 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile] Use of uninitialized value of type Any in string context.
  [Needle::Compile] Methods .^name, .raku, .gist, or .say can be used to stringify it to something meaningful.
  [Needle::Compile]   in sub _is_deeply at /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/share/perl6/core/sources/B7163A423E53679E5C263A8594641948ECB36A0A (Test) line 714
  [Needle::Compile]         not ok 183 - returned 'foo'
  [Needle::Compile]         # Failed test 'returned 'foo''
  [Needle::Compile]         # at t/02-single.rakutest line 14
  [Needle::Compile]         # expected: $(slip("foo",))
  [Needle::Compile]         #      got: $(slip("",))
  [Needle::Compile]         ok 184 - miss 'bar'
  [Needle::Compile]         # You failed 12 tests of 184
  [Needle::Compile]     not ok 5 - contains: find simple 'foo', :smartmark, :smartmark
  [Needle::Compile]     # Failed test 'contains: find simple 'foo', :smartmark, :smartmark'
  [Needle::Compile]     # at t/02-single.rakutest line 14
  [Needle::Compile]     # You failed 5 tests of 5
  [Needle::Compile] not ok 5 - all named arguments for contains
  [Needle::Compile] # Failed test 'all named arguments for contains'
  [Needle::Compile] # at t/02-single.rakutest line 14
  [Needle::Compile] # Test failed. Stopping test suite, because the RAKU_TEST_DIE_ON_FAIL
  [Needle::Compile] # environmental variable is set to a true value.
  [Needle::Compile] # You planned 10 tests, but ran 5
  [Needle::Compile] # You failed 1 test of 5
  [Needle::Compile] Command: /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz/Needle-Compile-0.0.12 t/03-file.rakutest
  [Needle::Compile] 1..9
  [Needle::Compile] ok 1 - is it a Callable
  [Needle::Compile] ok 2 - matched "foo"
  [Needle::Compile] ok 3 - did not match "bar"
  [Needle::Compile] # Subtest: file: "file:t/always"
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched "foo"
  [Needle::Compile]     ok 3 - did not match "bar"
  [Needle::Compile]     1..3
  [Needle::Compile] ok 4 - file: "file:t/always"
  [Needle::Compile] # Subtest: file: "t/always" but Type('file')
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched "foo"
  [Needle::Compile]     ok 3 - did not match "bar"
  [Needle::Compile]     1..3
  [Needle::Compile] ok 5 - file: "t/always" but Type('file')
  [Needle::Compile] # Subtest: file: :file("t/always")
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched "foo"
  [Needle::Compile]     ok 3 - did not match "bar"
  [Needle::Compile]     1..3
  [Needle::Compile] ok 6 - file: :file("t/always")
  [Needle::Compile] # Subtest: not file: "!file:t/always"
  [Needle::Compile]     1..3
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - did not match "foo"
  [Needle::Compile]     ok 3 - matched "bar"
  [Needle::Compile] ok 7 - not file: "!file:t/always"
  [Needle::Compile] # Subtest: not file: :not("file:t/always")
  [Needle::Compile]     1..3
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - did not match "foo"
  [Needle::Compile]     ok 3 - matched "bar"
  [Needle::Compile] ok 8 - not file: :not("file:t/always")
  [Needle::Compile] # Subtest: not file: :not(:file("t/always"))
  [Needle::Compile]     1..3
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - did not match "foo"
  [Needle::Compile]     ok 3 - matched "bar"
  [Needle::Compile] ok 9 - not file: :not(:file("t/always"))
  [Needle::Compile] Command: /tmp/whateverable/rakudo-moar/b61226d8bc93d4c030870b48d18af2adfd3a0f6f/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/66794ae2eb541201a403c08d48e27de668b32db7.tar.gz/Needle-Compile-0.0.12 t/04-multiple.rakutest
  [Needle::Compile] 1..16
  [Needle::Compile] # Subtest: or: $("foo", "§bar")
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 1 - or: $("foo", "§bar")
  [Needle::Compile] # Subtest: or: $("\&foo", "§bar")
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 2 - or: $("\&foo", "§bar")
  [Needle::Compile] # Subtest: or: $("foo" but Type('contains'), "bar" but Type('words'))
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 3 - or: $("foo" but Type('contains'), "bar" but Type('words'))
  [Needle::Compile] # Subtest: or: $(:contains("foo"), :words("bar"))
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 4 - or: $(:contains("foo"), :words("bar"))
  [Needle::Compile] # Subtest: or: "s:foo §bar"
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 5 - or: "s:foo §bar"
  [Needle::Compile] # Subtest: or: :split("foo §bar")
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 6 - or: :split("foo §bar")
  [Needle::Compile] # Subtest: or: "foo    §bar" but Type('split')
  [Needle::Compile]     1..7
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo'
  [Needle::Compile]     ok 3 - matched 'bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - matched 'ofoos'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile] ok 7 - or: "foo    §bar" but Type('split')
  [Needle::Compile] # Subtest: and: $("foo", "\&§bar")
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 8 - and: $("foo", "\&§bar")
  [Needle::Compile] # Subtest: and: $("foo" but Type('contains'), :and("bar" but Type('words')))
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 9 - and: $("foo" but Type('contains'), :and("bar" but Type('words')))
  [Needle::Compile] # Subtest: and: $(:contains("foo"), :and(:words("bar")))
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 10 - and: $(:contains("foo"), :and(:words("bar")))
  [Needle::Compile] # Subtest: and: $("foo" but Type('contains'), "\&§bar")
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 11 - and: $("foo" but Type('contains'), "\&§bar")
  [Needle::Compile] # Subtest: and: $("foo", "§bar" but Type('and'))
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 12 - and: $("foo", "§bar" but Type('and'))
  [Needle::Compile] # Subtest: and: $("\&foo", "§bar" but Type('and'))
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 13 - and: $("\&foo", "§bar" but Type('and'))
  [Needle::Compile] # Subtest: and: "s:foo \&§bar"
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 14 - and: "s:foo \&§bar"
  [Needle::Compile] # Subtest: and: :split("foo \&§bar")
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 15 - and: :split("foo \&§bar")
  [Needle::Compile] # Subtest: and: "foo    \&§bar" but Type('split')
  [Needle::Compile]     1..8
  [Needle::Compile]     ok 1 - is it a Callable
  [Needle::Compile]     ok 2 - matched 'foo bar'
  [Needle::Compile]     ok 3 - matched 'foozo bar'
  [Needle::Compile]     ok 4 - matched 'foo bar'
  [Needle::Compile]     ok 5 - did not match 'foo'
  [Needle::Compile]     ok 6 - did not match 'baz'
  [Needle::Compile]     ok 7 - did not match 'barra'
  [Needle::Compile]     ok 8 - did not match 'foo barra'
  [Needle::Compile] ok 16 - and: "foo    \&§bar" but Type('split')
  ===> Testing [FAIL]: Needle::Compile:ver<0.0.12>:auth<zef:lizmat>
  [Needle::Compile] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Needle::Compile:ver<0.0.12>:auth<zef:lizmat>
  ===> Install [OK] for Needle::Compile:ver<0.0.12>:auth<zef:lizmat>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 39.091s
               CPU time consumed: 59.257s
                     Memory peak: 1.1G (swap: 0B)

  ```
  </details>
* [ ] [File::Which](https://raku.land//File::Which) – Fail, Bisected: [b61226d](https://github.com/rakudo/rakudo/commit/b61226d8bc93d4c030870b48d18af2adfd3a0f6f)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2395465-i2449751.service; invocation ID: be6ff228095c4625a14abd2985e0a086
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: File::Which
  ===> Found: File::Which:ver<1.0.4> [via Zef::Repository::Ecosystems<rea>]
  [File::Which] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788816873.2395466.1894.152888773839/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/F/File%3A%3AWhich/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz
  ===> Fetching [OK]: File::Which:ver<1.0.4> to /home/coke/sandbox/blin/data/zef-data/tmp/1788816873.2395466.1894.152888773839/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz
  [File::Which] Command: tar -t -f ./File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz
  [File::Which] Command: tar -xvf ./File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz -C ../File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz
  ===> Extraction [OK]: File::Which to /home/coke/sandbox/blin/data/zef-data/tmp/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz
  ===> Testing: File::Which:ver<1.0.4>
  [File::Which] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz/raku-file-which-master t/00-load.rakutest
  [File::Which] 1..4
  [File::Which] ok 1 - File::Which::MacOSX module can be use-d ok
  [File::Which] ok 2 - File::Which::Unix module can be use-d ok
  [File::Which] ok 3 - File::Which::Win32 module can be use-d ok
  [File::Which] ok 4 - File::Which module can be use-d ok
  [File::Which] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz/raku-file-which-master t/01-which.rakutest
  [File::Which] 1..4
  [File::Which] ok 1 - 'use File::Which' worked!
  [File::Which] # Found raku at '/tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/raku'
  [File::Which] ok 2 - raku is found
  [File::Which] ok 3 - raku file exists
  [File::Which] ok 4 - raku and is an executable
  [File::Which] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz/raku-file-which-master t/02-win32.rakutest
  [File::Which] 1..10
  [File::Which] ok 1 - # SKIP Windows-only tests
  [File::Which] ok 2 - # SKIP Windows-only tests
  [File::Which] ok 3 - # SKIP Windows-only tests
  [File::Which] ok 4 - # SKIP Windows-only tests
  [File::Which] ok 5 - # SKIP Windows-only tests
  [File::Which] ok 6 - # SKIP Windows-only tests
  [File::Which] ok 7 - # SKIP Windows-only tests
  [File::Which] ok 8 - # SKIP Windows-only tests
  [File::Which] ok 9 - # SKIP Windows-only tests
  [File::Which] ok 10 - # SKIP Windows-only tests
  [File::Which] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz/raku-file-which-master t/03-export.rakutest
  [File::Which] 1..4
  [File::Which] ok 1 - 'use File::Which :whence' worked!
  [File::Which] # Found raku at '/tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/raku' using whence
  [File::Which] ok 2 - raku is found
  [File::Which] ok 3 - raku file exists
  [File::Which] ok 4 - raku and is an executable
  [File::Which] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz/raku-file-which-master t/04-simple.rakutest
  [File::Which] ok 1 - Null-length false result
  [File::Which] ok 2 - Positive length false result
  [File::Which] ok 3 - Found test-bin
  [File::Which] ok 4 - Check test3 for Unix
  [File::Which] 1..4
  [File::Which] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz/raku-file-which-master t/05-all.rakutest
  [File::Which] ok 1 - Found test-bin
  [File::Which] ok 2 - Found all
  [File::Which] ok 3 - Found at least one result
  [File::Which] ok 4 - Zero is defined
  [File::Which] ok 5 - Empty string
  [File::Which] 1..5
  [File::Which] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/File%3A%3AWhich%3Aver%3C1.0.4%3E%3Aauth%3Cgithub%3Aazawawi%3E.tar.gz/raku-file-which-master t/99-author-meta.rakutest
  [File::Which] 1..1
  [File::Which] ok 1 - # SKIP Skipping author test
  ===> Testing [OK] for File::Which:ver<1.0.4>
  ===> Installing: File::Which:ver<1.0.4>
  ===> Install [OK] for File::Which:ver<1.0.4>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 42.181s
               CPU time consumed: 59.598s
                     Memory peak: 1.4G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2393497-i2434460.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: File::Which
  No candidates found matching identity: File::Which
            Finished with result: exit-code
  Main processes terminated with: code=exited, status=255/EXCEPTION
                 Service runtime: 46.679s
               CPU time consumed: 1min 2.399s
                     Memory peak: 1G (swap: 0B)

  ```
  </details>
* [ ] [Getopt::Long](https://raku.land/cpan:LEONT/Getopt::Long) – Fail, Bisected: [b61226d](https://github.com/rakudo/rakudo/commit/b61226d8bc93d4c030870b48d18af2adfd3a0f6f)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2395345-i2461722.service; invocation ID: 0382c770d7254a98be58b78614a86e43
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Getopt::Long
  ===> Found: Getopt::Long:ver<0.4.2>:auth<cpan:LEONT> [via Zef::Repository::Ecosystems<rea>]
  [Getopt::Long] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1788816873.2395346.9000.049688294412/Getopt%3A%3ALong%3Aver%3C0.4.2%3E%3Aauth%3Ccpan%3ALEONT%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/Getopt%3A%3ALong/Getopt%3A%3ALong%3Aver%3C0.4.2%3E%3Aauth%3Ccpan%3ALEONT%3E.tar.gz
  ===> Fetching [OK]: Getopt::Long:ver<0.4.2>:auth<cpan:LEONT> to /home/coke/sandbox/blin/data/zef-data/tmp/1788816873.2395346.9000.049688294412/Getopt%3A%3ALong%3Aver%3C0.4.2%3E%3Aauth%3Ccpan%3ALEONT%3E.tar.gz
  [Getopt::Long] Command: tar -t -f ./Getopt%3A%3ALong%3Aver%3C0.4.2%3E%3Aauth%3Ccpan%3ALEONT%3E.tar.gz
  [Getopt::Long] Command: tar -xvf ./Getopt%3A%3ALong%3Aver%3C0.4.2%3E%3Aauth%3Ccpan%3ALEONT%3E.tar.gz -C ../Getopt%3A%3ALong%3Aver%3C0.4.2%3E%3Aauth%3Ccpan%3ALEONT%3E.tar.gz
  ===> Extraction [OK]: Getopt::Long to /home/coke/sandbox/blin/data/zef-data/tmp/Getopt%3A%3ALong%3Aver%3C0.4.2%3E%3Aauth%3Ccpan%3ALEONT%3E.tar.gz
  ===> Testing: Getopt::Long:ver<0.4.2>
  [Getopt::Long] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Getopt%3A%3ALong%3Aver%3C0.4.2%3E%3Aauth%3Ccpan%3ALEONT%3E.tar.gz/Getopt-Long-0.4.2 t/basic.rakutest
  [Getopt::Long] ok 1 - Common argument mix works
  [Getopt::Long] ok 2 - Common argument mix works (2)
  [Getopt::Long] ok 3 - Calling main (1) works
  [Getopt::Long] ok 4 - Short options work
  [Getopt::Long] ok 5 - Calling main (1) works
  [Getopt::Long] ok 6 - "--" terminates argument handling
  [Getopt::Long] ok 7 - Floating point arguments work
  [Getopt::Long] ok 8 - :i without argument works
  [Getopt::Long] ok 9 - :i with argument works
  [Getopt::Long] ok 10 - :1 without argument works
  [Getopt::Long] ok 11 - :1 with argument works
  [Getopt::Long] ok 12 - Counter adds up
  [Getopt::Long] ok 13 - Colon singles fine
  [Getopt::Long] ok 14 - Colon counter adds up
  [Getopt::Long] ok 15 - Parsing octal argument with "i"
  [Getopt::Long] ok 16 - Parsing negative octal argument with "i"
  [Getopt::Long] ok 17 - Parsing decimal argument with "i"
  [Getopt::Long] ok 18 - Negated arguments produce False
  [Getopt::Long] ok 19 - Bundling can be disabled
  [Getopt::Long] ok 20 - Repeat specifier works
  [Getopt::Long] ok 21 - Repeat specifier works with range
  [Getopt::Long] ok 22 - sub main1 is not quite a Sub
  [Getopt::Long] ok 23 - sub main1 is parsed
  [Getopt::Long] ok 24 - getopt trait works
  [Getopt::Long] ok 25 - negative argument detected
  [Getopt::Long] ok 26 - Pair arguments
  [Getopt::Long] ok 27 - Pair arguments
  [Getopt::Long] ok 28 - Repeat specifier works
  [Getopt::Long] ok 29 - :compat-singles appears to work
  [Getopt::Long] ok 30 - :compat-negation works
  [Getopt::Long] ok 31 - compat negation delivers a false value
  [Getopt::Long] ok 32 - compat negation delivers the correct string
  [Getopt::Long] ok 33 - Correctly parsed enum
  [Getopt::Long] ok 34 - Correctly parsed enum
  [Getopt::Long] ok 35 - Typed positionals work
  [Getopt::Long] ok 36 - Typed positionals work on multis as well
  [Getopt::Long] ok 37 - Can parse DateTime
  [Getopt::Long] ok 38 - Can parse Date
  [Getopt::Long] ok 39 - Can auto-abbreviate
  [Getopt::Long] ok 40 - Parse a custom parseable type
  [Getopt::Long] # Subtest: No conversion known for type Signature
  [Getopt::Long]     1..2
  [Getopt::Long]     ok 1 - code dies
  [Getopt::Long]     ok 2 - right exception type (Getopt::Long::Exception)
  [Getopt::Long] ok 41 - No conversion known for type Signature
  [Getopt::Long] ok 42 - Bundled options with arguments work
  [Getopt::Long] ok 43 - :!permute works
  [Getopt::Long] ok 44 - Custom converter works
  [Getopt::Long] ok 45 - 
  [Getopt::Long] 1..45
  ===> Testing [OK] for Getopt::Long:ver<0.4.2>
  ===> Installing: Getopt::Long:ver<0.4.2>
  ===> Install [OK] for Getopt::Long:ver<0.4.2>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 41.570s
               CPU time consumed: 57.899s
                     Memory peak: 1.2G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2393504-i2430259.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Getopt::Long
  No candidates found matching identity: Getopt::Long
            Finished with result: exit-code
  Main processes terminated with: code=exited, status=255/EXCEPTION
                 Service runtime: 44.320s
               CPU time consumed: 1min 2.280s
                     Memory peak: 1G (swap: 0B)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| Fail                      |     3 | [File::Which](https://raku.land//File::Which) [Getopt::Long](https://raku.land/cpan:LEONT/Getopt::Long) [Needle::Compile](https://raku.land/zef:lizmat/Needle::Compile) |
| OK                        |    35 | ⋯                         |



This run started on 2026-09-07T21:44:51Z and finished in 13 minutes.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
