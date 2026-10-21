[Blin](https://github.com/Raku/Blin) results between 2026.09 ([9a94801](https://github.com/rakudo/rakudo/commit/9a94801c154543573d926e6258e062f3c3782635)) and aa1262d242 ([aa1262d](https://github.com/rakudo/rakudo/commit/aa1262d24269fcbc10e6ef7039d91f05bde64b04)):

* [ ] [Injector](https://raku.land/zef:FCO/Injector) – Fail, Bisected: [f20534c](https://github.com/rakudo/rakudo/commit/f20534cb3a5df815e7c3b8ca08160bcb78f9d6c2)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1411485-i1454965.service; invocation ID: ab67eafb81f14fe6a8feeb1413645e13
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Injector
  ===> Found: Injector:ver<0.0.1>:auth<zef:FCO> [via Zef::Repository::Ecosystems<fez>]
  [Injector] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549574.1411486.4479.459708259898/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz https://360.zef.pm/I/NJ/INJECTOR/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  ===> Fetching [OK]: Injector:ver<0.0.1>:auth<zef:FCO> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549574.1411486.4479.459708259898/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
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
                 Service runtime: 30.989s
               CPU time consumed: 44.045s
                     Memory peak: 1.1G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1411130-i1406523.service; invocation ID: 3fbd9c5b61c84ce7b5d99205ed4a7fec
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Injector
  ===> Found: Injector:ver<0.0.1>:auth<zef:FCO> [via Zef::Repository::Ecosystems<fez>]
  [Injector] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549542.1411132.4024.3361219580374/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz https://360.zef.pm/I/NJ/INJECTOR/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  ===> Fetching [OK]: Injector:ver<0.0.1>:auth<zef:FCO> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549542.1411132.4024.3361219580374/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  [Injector] Command: tar -t -f ./c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  [Injector] Command: tar -xvf ./c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz -C ../c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  ===> Extraction [OK]: Injector to /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz
  ===> Testing: Injector:ver<0.0.1>:auth<zef:FCO>
  [Injector] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1 t/02-test.rakutest
  [Injector] WARNING: unhandled Failure detected in DESTROY. If you meant to ignore it, you can mark it as handled by calling .Bool, .so, .not, or .defined methods. The Failure was:
  [Injector] No such symbol 'Test'
  [Injector]   in block <unit> at t/02-test.rakutest line 14
  [Injector]   in method IMPL-LOAD-MODULE at src/Raku/ast/statements.rakumod line 2557
  [Injector]   in any PERFORM-BEGIN at src/Raku/ast/statements.rakumod line 2823
  [Injector]   in any  at src/Raku/ast/begintime.rakumod line 22
  [Injector]   in method ensure-begin-performed at src/Raku/ast/begintime.rakumod line 18
  [Injector]   in any statement-control at /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/share/perl6/lib/Raku/Grammar.moarvm line 1
  [Injector] Method 'r' must be implemented by Rand because it is required by roles: Rand.
  [Injector]   in method instantiate at /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Bind.rakumod (Injector::Bind) line 23
  [Injector]   in method get-obj at /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Bind/Instance.rakumod (Injector::Bind::Instance) line 5
  [Injector]   in method  at /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Injected/Attribute.rakumod (Injector::Injected::Attribute) line 13
  [Injector]   in method  at /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Injected/Attribute.rakumod (Injector::Injected::Attribute) line 19
  [Injector]   in method instantiate at /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Bind.rakumod (Injector::Bind) line 23
  [Injector]   in method get-obj at /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Bind/Singleton.rakumod (Injector::Bind::Singleton) line 5
  [Injector]   in block  at /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Injected/Variable.rakumod (Injector::Injected::Variable) line 11
  [Injector]   in block <unit> at t/02-test.rakutest line 1
  [Injector] Saw 1 occurrence of deprecated code.
  [Injector] ================================================================================
  [Injector] Method perl (from Mu) seen at:
  [Injector]   /home/coke/sandbox/blin/data/zef-data/tmp/c5d8945aa0ebdfc89690d16f8841360faffe4299.tar.gz/Injector-0.0.1/lib/Injector/Storage.rakumod (Injector::Storage), lines 10,14
  [Injector] Please use raku instead.
  [Injector] --------------------------------------------------------------------------------
  [Injector] Please contact the author to have these occurrences of deprecated code
  [Injector] adapted, so that this message will disappear!
  ===> Testing [FAIL]: Injector:ver<0.0.1>:auth<zef:FCO>
  [Injector] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Injector:ver<0.0.1>:auth<zef:FCO>
  ===> Install [OK] for Injector:ver<0.0.1>:auth<zef:FCO>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 11.929s
               CPU time consumed: 15.116s
                     Memory peak: 1.1G (swap: 0B)

  ```
  </details>
* [ ] [BinaryHeap](https://raku.land/zef:dumarchie/BinaryHeap) – Fail, Bisected: [afee7d8](https://github.com/rakudo/rakudo/commit/afee7d8d3197b7a093355d98a90f6f86d8bda32a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1405402-i1424234.service; invocation ID: 4989dccb31e9419d928ddd7729eddac2
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: BinaryHeap
  ===> Found: BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2> [via Zef::Repository::Ecosystems<fez>]
  [BinaryHeap] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549409.1405403.2601.7497283815715/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz https://360.zef.pm/B/IN/BINARYHEAP/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz
  ===> Fetching [OK]: BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549409.1405403.2601.7497283815715/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz
  [BinaryHeap] Command: tar -t -f ./114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz
  [BinaryHeap] Command: tar -xvf ./114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz -C ../114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz
  ===> Extraction [OK]: BinaryHeap to /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz
  ===> Testing: BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2>
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/00-meta.rakutest
  [BinaryHeap] 1..1
  [BinaryHeap] ok 1 - # SKIP Skipping author test
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/01-binaryheap.rakutest
  [BinaryHeap] 1..9
  [BinaryHeap] # Subtest: uninitialized $heap
  [BinaryHeap]     ok 1 - $heap.Bool
  [BinaryHeap]     ok 2 - $heap.of
  [BinaryHeap]     ok 3 - $heap.top
  [BinaryHeap]     ok 4 - $heap.values
  [BinaryHeap]     ok 5 - $heap has not been autovivified
  [BinaryHeap]     ok 6 - $heap.elems
  [BinaryHeap]     ok 7 - $heap has been autovivified
  [BinaryHeap]     1..7
  [BinaryHeap] ok 1 - uninitialized $heap
  [BinaryHeap] # Subtest: create a heap
  [BinaryHeap]     # Subtest: create an empty heap
  [BinaryHeap]         ok 1 - MinHeap.new
  [BinaryHeap]         ok 2 - .Bool
  [BinaryHeap]         ok 3 - .top
  [BinaryHeap]         ok 4 - .values
  [BinaryHeap]         ok 5 - .elems
  [BinaryHeap]         1..5
  [BinaryHeap]     ok 1 - create an empty heap
  [BinaryHeap]     # Subtest: create a heap from a single value
  [BinaryHeap]         ok 1 - MinHeap.new(Mu)
  [BinaryHeap]         ok 2 - .Bool
  [BinaryHeap]         ok 3 - .top
  [BinaryHeap]         ok 4 - .values
  [BinaryHeap]         ok 5 - .elems
  [BinaryHeap]         1..5
  [BinaryHeap]     ok 2 - create a heap from a single value
  [BinaryHeap]     # Subtest: create a heap from a list of values
  [BinaryHeap]         ok 1 - MinHeap.new(values)
  [BinaryHeap]         ok 2 - .values
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 3 - create a heap from a list of values
  [BinaryHeap]     # Subtest: create a heap from an itemized Slip
  [BinaryHeap]         ok 1 - MinHeap.new($slip)
  [BinaryHeap]         ok 2 - .values
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 4 - create a heap from an itemized Slip
  [BinaryHeap]     1..4
  [BinaryHeap] ok 2 - create a heap
  [BinaryHeap] # Subtest: push onto a heap
  [BinaryHeap]     # Subtest: push a single value onto an empty heap
  [BinaryHeap]         ok 1 - .push(Mu) returns the heap
  [BinaryHeap]         ok 2 - heap includes the provided value
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 1 - push a single value onto an empty heap
  [BinaryHeap]     # Subtest: push multiple values onto a heap
  [BinaryHeap]         ok 1 - .push(2, 19, 7, 3, 1, 100) returns the heap
  [BinaryHeap]         ok 2 - heap includes the provided values
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 2 - push multiple values onto a heap
  [BinaryHeap]     # Subtest: push a Slip onto a heap
  [BinaryHeap]         ok 1 - .push($slip) returns the heap
  [BinaryHeap]         ok 2 - heap includes the elements of the provided Slip
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 3 - push a Slip onto a heap
  [BinaryHeap]     1..3
  [BinaryHeap] ok 3 - push onto a heap
  [BinaryHeap] # Subtest: replace the top of a heap
  [BinaryHeap]     # Subtest: replace into an empty heap
  [BinaryHeap]         ok 1 - .replace(value) returns Nil
  [BinaryHeap]         ok 2 - heap contains the provided value
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 1 - replace into an empty heap
  [BinaryHeap]     # Subtest: replace the top of a non-empty heap with a Slip
  [BinaryHeap]         ok 1 - .replace($slip) returns the original top
  [BinaryHeap]         ok 2 - new top is the provided Slip
  [BinaryHeap]         1..2
  [BinaryHeap]     ok 2 - replace the top of a non-empty heap with a Slip
  [BinaryHeap]     # Subtest: sift down a lower-precedence value
  [BinaryHeap]         ok 1 - .replace(value) returns the original top
  [BinaryHeap]         ok 2 - heap contains the provided value instead
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 3 - sift down a lower-precedence value
  [BinaryHeap]     1..3
  [BinaryHeap] ok 4 - replace the top of a heap
  [BinaryHeap] # Subtest: pop a value from a heap
  [BinaryHeap]     # Subtest: pop from an uninitialized heap
  [BinaryHeap]         1..2
  [BinaryHeap]         ok 1 - code returned a Failure
  [BinaryHeap]         # Subtest: Failure threw when sunk
  [BinaryHeap]             1..4
  [BinaryHeap]             ok 1 - code dies
  [BinaryHeap]             ok 2 - right exception type (X::Cannot::Empty)
  [BinaryHeap]             ok 3 - .action matches pop
  [BinaryHeap]             ok 4 - .what matches BinaryHeap::MinHeap
  [BinaryHeap]         ok 2 - Failure threw when sunk
  [BinaryHeap]     ok 1 - pop from an uninitialized heap
  [BinaryHeap]     # Subtest: pop from an empty heap
  [BinaryHeap]         1..2
  [BinaryHeap]         ok 1 - code returned a Failure
  [BinaryHeap]         # Subtest: Failure threw when sunk
  [BinaryHeap]             1..4
  [BinaryHeap]             ok 1 - code dies
  [BinaryHeap]             ok 2 - right exception type (X::Cannot::Empty)
  [BinaryHeap]             ok 3 - .action matches pop
  [BinaryHeap]             ok 4 - .what matches BinaryHeap::MinHeap
  [BinaryHeap]         ok 2 - Failure threw when sunk
  [BinaryHeap]     ok 2 - pop from an empty heap
  [BinaryHeap]     # Subtest: pop from a heap containing a single value
  [BinaryHeap]         ok 1 - .pop returns the top
  [BinaryHeap]         ok 2 - heap is empty
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 3 - pop from a heap containing a single value
  [BinaryHeap]     # Subtest: pop from a heap containing multiple values
  [BinaryHeap]         ok 1 - .pop returns the original top
  [BinaryHeap]         ok 2 - heap no longer contains the original top
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 4 - pop from a heap containing multiple values
  [BinaryHeap]     1..4
  [BinaryHeap] ok 5 - pop a value from a heap
  [BinaryHeap] # Subtest: extract values from a heap
  [BinaryHeap]     # Subtest: extract all values
  [BinaryHeap]         ok 1 - MinHeap.extract() returns an empty Seq
  [BinaryHeap]         ok 2 - MinHeap.new(values).extract returns a Seq
  [BinaryHeap]         ok 3 - the heap is not modified if the Seq did not generate any values
  [BinaryHeap]         ok 4 - .elems
  [BinaryHeap]         ok 5 - the Seq generates all heap elements in non-decreasing order
  [BinaryHeap]         ok 6 - the heap is empty when the Seq is exhausted
  [BinaryHeap]         ok 7 - .elems
  [BinaryHeap]         1..7
  [BinaryHeap]     ok 1 - extract all values
  [BinaryHeap]     # Subtest: extract n values
  [BinaryHeap]         ok 1 - MaxHeap.extract(n) returns an empty Seq
  [BinaryHeap]         ok 2 - MaxHeap.new(values).extract(n) returns a Seq
  [BinaryHeap]         ok 3 - the heap is not modified if the Seq did not generate any values
  [BinaryHeap]         ok 4 - .elems
  [BinaryHeap]         ok 5 - the Seq generates n elements in non-increasing order
  [BinaryHeap]         ok 6 - the elements are removed from the heap
  [BinaryHeap]         ok 7 - .elems
  [BinaryHeap]         1..7
  [BinaryHeap]     ok 2 - extract n values
  [BinaryHeap]     1..2
  [BinaryHeap] ok 6 - extract values from a heap
  [BinaryHeap] # Subtest: push-pop
  [BinaryHeap]     ok 1 - MinHeap.push-pop(Mu) returns the provided value
  [BinaryHeap]     # Subtest: push-pop when heap instance is empty
  [BinaryHeap]         ok 1 - .push-pop(Mu) returns the provided value
  [BinaryHeap]         ok 2 - heap remains empty
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 2 - push-pop when heap instance is empty
  [BinaryHeap]     # Subtest: push-pop when provided value precedes top
  [BinaryHeap]         ok 1 - .push-pop(value) returns the provided value
  [BinaryHeap]         ok 2 - heap remains the same
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 3 - push-pop when provided value precedes top
  [BinaryHeap]     # Subtest: push-pop when top precedes provided value
  [BinaryHeap]         ok 1 - .push-pop(value) returns the old top
  [BinaryHeap]         ok 2 - heap contains the provided value instead
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 4 - push-pop when top precedes provided value
  [BinaryHeap]     1..4
  [BinaryHeap] ok 7 - push-pop
  [BinaryHeap] # Subtest: clone
  [BinaryHeap]     ok 1 - .clone returns a heap storing the same values
  [BinaryHeap]     ok 2 - .elems
  [BinaryHeap]     ok 3 - the values are stored in a distinct array
  [BinaryHeap]     ok 4 - .elems
  [BinaryHeap]     1..4
  [BinaryHeap] ok 8 - clone
  [BinaryHeap] # Subtest: heapify
  [BinaryHeap]     ok 1 - .new(@array, :in-place) constrains the type of values on the heap
  [BinaryHeap]     ok 2 - ... and puts the elements of the provieded @array in heap order
  [BinaryHeap]     ok 3 - the return value is a heap
  [BinaryHeap]     ok 4 - the heap is based on the @array
  [BinaryHeap]     ok 5 - .elems
  [BinaryHeap]     # Subtest: replace top with value of invalid type
  [BinaryHeap]         ok 1 - .replace(value) dies
  [BinaryHeap]         ok 2 - the heap is not modified
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 6 - replace top with value of invalid type
  [BinaryHeap]     ok 7 - .clone maintains the type constraint of the heap
  [BinaryHeap]     1..7
  [BinaryHeap] ok 9 - heapify
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/02-autovivify.rakutest
  [BinaryHeap] 1..3
  [BinaryHeap] # Subtest: Push onto an uninitialized MaxHeap
  [BinaryHeap]     ok 1 - $heap.push(|values)
  [BinaryHeap]     ok 2 - .values
  [BinaryHeap]     1..2
  [BinaryHeap] ok 1 - Push onto an uninitialized MaxHeap
  [BinaryHeap] # Subtest: Push onto an uninitialized MinHeap
  [BinaryHeap]     ok 1 - $heap.push(|values)
  [BinaryHeap]     ok 2 - .values
  [BinaryHeap]     1..2
  [BinaryHeap] ok 2 - Push onto an uninitialized MinHeap
  [BinaryHeap] # Subtest: Replace the top of an uninitialized heap
  [BinaryHeap]     ok 1 - $heap.replace(new) returns Nil
  [BinaryHeap]     ok 2 - .values
  [BinaryHeap]     1..2
  [BinaryHeap] ok 3 - Replace the top of an uninitialized heap
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/03-exports.rakutest
  [BinaryHeap] 1..7
  [BinaryHeap] # Subtest: infix eqv
  [BinaryHeap]     ok 1 - MaxHeap.new(42) eqv MaxHeap.new(42)
  [BinaryHeap]     ok 2 - MaxHeap.new(42) !eqv MinHeap.new(42)
  [BinaryHeap]     1..2
  [BinaryHeap] ok 1 - infix eqv
  [BinaryHeap] # Subtest: can't import symbols that are not exported
  [BinaryHeap]     1..3
  [BinaryHeap]     ok 1 - 'use BinaryHeap <Foo &heapify>' died
  [BinaryHeap]     ok 2 - right exception type (Exception)
  [BinaryHeap]     ok 3 - .message matches Trying to import from 'BinaryHeap', but the following symbols are not exported: Foo, &heapify
  [BinaryHeap] ok 2 - can't import symbols that are not exported
  [BinaryHeap] ok 3 - imported &heapsort is an alias for &BinaryHeap::heapsort
  [BinaryHeap] # Subtest: heapsort
  [BinaryHeap]     ok 1 - heapsort(@array) returns the array
  [BinaryHeap]     ok 2 - the array elements are sorted in ascending order
  [BinaryHeap]     1..2
  [BinaryHeap] ok 4 - heapsort
  [BinaryHeap] # Subtest: reverse heapsort
  [BinaryHeap]     ok 1 - heapsort(@array, :reverse) returns the array
  [BinaryHeap]     ok 2 - the array elements are sorted in descending order
  [BinaryHeap]     1..2
  [BinaryHeap] ok 5 - reverse heapsort
  [BinaryHeap] # Subtest: heapsort with custom comparator
  [BinaryHeap]     ok 1 - heapsort({$^b cmp $^a}, @array) returns the array
  [BinaryHeap]     ok 2 - the array elements are put in descending order
  [BinaryHeap]     1..2
  [BinaryHeap] ok 6 - heapsort with custom comparator
  [BinaryHeap] # Subtest: reverse heapsort with custom comparator
  [BinaryHeap]     ok 1 - heapsort({$^b cmp $^a}, @array, :reverse) returns the array
  [BinaryHeap]     ok 2 - the array elements are put in ascending order
  [BinaryHeap]     1..2
  [BinaryHeap] ok 7 - reverse heapsort with custom comparator
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/04-factories.rakutest
  [BinaryHeap] 1..3
  [BinaryHeap] # Subtest: imports
  [BinaryHeap]     ok 1 - imported &max-heap is short for &BinaryHeap::max-heap
  [BinaryHeap]     ok 2 - imported &min-heap is short for &BinaryHeap::min-heap
  [BinaryHeap]     1..2
  [BinaryHeap] ok 1 - imports
  [BinaryHeap] ok 2 - max-heap(*.value <=> *.value, @values)
  [BinaryHeap] ok 3 - min-heap(*.value <=> *.value, @values)
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/05-representation.rakutest
  [BinaryHeap] 1..6
  [BinaryHeap] ok 1 - BinaryHeap::MinHeap.new.gist
  [BinaryHeap] ok 2 - BinaryHeap::MinHeap.new.raku
  [BinaryHeap] ok 3 - BinaryHeap::MinHeap.new(1, 2, 3).gist
  [BinaryHeap] ok 4 - BinaryHeap::MinHeap.new(1, 2, 3).raku
  [BinaryHeap] ok 5 - BinaryHeap::MinHeap.new(1, 3, 2).gist
  [BinaryHeap] ok 6 - BinaryHeap::MinHeap.new(1, 3, 2).raku
  ===> Testing [OK] for BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2>
  ===> Installing: BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2>
  ===> Install [OK] for BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 48.915s
               CPU time consumed: 1min 9.449s
                     Memory peak: 999.5M (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1404958-i1466792.service; invocation ID: e4188edad94c477fb7871e7f7b9b4b4a
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: BinaryHeap
  ===> Found: BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2> [via Zef::Repository::Ecosystems<fez>]
  [BinaryHeap] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549362.1404961.1958.92375421848/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz https://360.zef.pm/B/IN/BINARYHEAP/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz
  ===> Fetching [OK]: BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549362.1404961.1958.92375421848/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz
  [BinaryHeap] Command: tar -t -f ./114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz
  [BinaryHeap] Command: tar -xvf ./114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz -C ../114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz
  ===> Extraction [OK]: BinaryHeap to /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz
  ===> Testing: BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2>
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/00-meta.rakutest
  [BinaryHeap] 1..1
  [BinaryHeap] ok 1 - # SKIP Skipping author test
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/01-binaryheap.rakutest
  [BinaryHeap] 1..9
  [BinaryHeap] # Subtest: uninitialized $heap
  [BinaryHeap]     ok 1 - $heap.Bool
  [BinaryHeap]     ok 2 - $heap.of
  [BinaryHeap]     ok 3 - $heap.top
  [BinaryHeap]     ok 4 - $heap.values
  [BinaryHeap]     ok 5 - $heap has not been autovivified
  [BinaryHeap]     ok 6 - $heap.elems
  [BinaryHeap]     ok 7 - $heap has been autovivified
  [BinaryHeap]     1..7
  [BinaryHeap] ok 1 - uninitialized $heap
  [BinaryHeap] # Subtest: create a heap
  [BinaryHeap]     # Subtest: create an empty heap
  [BinaryHeap]         ok 1 - MinHeap.new
  [BinaryHeap]         ok 2 - .Bool
  [BinaryHeap]         ok 3 - .top
  [BinaryHeap]         ok 4 - .values
  [BinaryHeap]         ok 5 - .elems
  [BinaryHeap]         1..5
  [BinaryHeap]     ok 1 - create an empty heap
  [BinaryHeap]     # Subtest: create a heap from a single value
  [BinaryHeap]         ok 1 - MinHeap.new(Mu)
  [BinaryHeap]         ok 2 - .Bool
  [BinaryHeap]         ok 3 - .top
  [BinaryHeap]         ok 4 - .values
  [BinaryHeap]         ok 5 - .elems
  [BinaryHeap]         1..5
  [BinaryHeap]     ok 2 - create a heap from a single value
  [BinaryHeap]     # Subtest: create a heap from a list of values
  [BinaryHeap]         ok 1 - MinHeap.new(values)
  [BinaryHeap]         ok 2 - .values
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 3 - create a heap from a list of values
  [BinaryHeap]     # Subtest: create a heap from an itemized Slip
  [BinaryHeap]         ok 1 - MinHeap.new($slip)
  [BinaryHeap]         ok 2 - .values
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 4 - create a heap from an itemized Slip
  [BinaryHeap]     1..4
  [BinaryHeap] ok 2 - create a heap
  [BinaryHeap] # Subtest: push onto a heap
  [BinaryHeap]     # Subtest: push a single value onto an empty heap
  [BinaryHeap]         ok 1 - .push(Mu) returns the heap
  [BinaryHeap]         ok 2 - heap includes the provided value
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 1 - push a single value onto an empty heap
  [BinaryHeap]     # Subtest: push multiple values onto a heap
  [BinaryHeap]         ok 1 - .push(2, 19, 7, 3, 1, 100) returns the heap
  [BinaryHeap]         ok 2 - heap includes the provided values
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 2 - push multiple values onto a heap
  [BinaryHeap]     # Subtest: push a Slip onto a heap
  [BinaryHeap]         ok 1 - .push($slip) returns the heap
  [BinaryHeap]         ok 2 - heap includes the elements of the provided Slip
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 3 - push a Slip onto a heap
  [BinaryHeap]     1..3
  [BinaryHeap] ok 3 - push onto a heap
  [BinaryHeap] # Subtest: replace the top of a heap
  [BinaryHeap]     # Subtest: replace into an empty heap
  [BinaryHeap]         ok 1 - .replace(value) returns Nil
  [BinaryHeap]         ok 2 - heap contains the provided value
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 1 - replace into an empty heap
  [BinaryHeap]     # Subtest: replace the top of a non-empty heap with a Slip
  [BinaryHeap]         ok 1 - .replace($slip) returns the original top
  [BinaryHeap]         ok 2 - new top is the provided Slip
  [BinaryHeap]         1..2
  [BinaryHeap]     ok 2 - replace the top of a non-empty heap with a Slip
  [BinaryHeap]     # Subtest: sift down a lower-precedence value
  [BinaryHeap]         ok 1 - .replace(value) returns the original top
  [BinaryHeap]         ok 2 - heap contains the provided value instead
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 3 - sift down a lower-precedence value
  [BinaryHeap]     1..3
  [BinaryHeap] ok 4 - replace the top of a heap
  [BinaryHeap] # Subtest: pop a value from a heap
  [BinaryHeap]     # Subtest: pop from an uninitialized heap
  [BinaryHeap]         1..2
  [BinaryHeap]         ok 1 - code returned a Failure
  [BinaryHeap]         # Subtest: Failure threw when sunk
  [BinaryHeap]             1..4
  [BinaryHeap]             ok 1 - code dies
  [BinaryHeap]             ok 2 - right exception type (X::Cannot::Empty)
  [BinaryHeap]             ok 3 - .action matches pop
  [BinaryHeap]             ok 4 - .what matches BinaryHeap::MinHeap
  [BinaryHeap]         ok 2 - Failure threw when sunk
  [BinaryHeap]     ok 1 - pop from an uninitialized heap
  [BinaryHeap]     # Subtest: pop from an empty heap
  [BinaryHeap]         1..2
  [BinaryHeap]         ok 1 - code returned a Failure
  [BinaryHeap]         # Subtest: Failure threw when sunk
  [BinaryHeap]             1..4
  [BinaryHeap]             ok 1 - code dies
  [BinaryHeap]             ok 2 - right exception type (X::Cannot::Empty)
  [BinaryHeap]             ok 3 - .action matches pop
  [BinaryHeap]             ok 4 - .what matches BinaryHeap::MinHeap
  [BinaryHeap]         ok 2 - Failure threw when sunk
  [BinaryHeap]     ok 2 - pop from an empty heap
  [BinaryHeap]     # Subtest: pop from a heap containing a single value
  [BinaryHeap]         ok 1 - .pop returns the top
  [BinaryHeap]         ok 2 - heap is empty
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 3 - pop from a heap containing a single value
  [BinaryHeap]     # Subtest: pop from a heap containing multiple values
  [BinaryHeap]         ok 1 - .pop returns the original top
  [BinaryHeap]         ok 2 - heap no longer contains the original top
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 4 - pop from a heap containing multiple values
  [BinaryHeap]     1..4
  [BinaryHeap] ok 5 - pop a value from a heap
  [BinaryHeap] # Subtest: extract values from a heap
  [BinaryHeap]     # Subtest: extract all values
  [BinaryHeap]         ok 1 - MinHeap.extract() returns an empty Seq
  [BinaryHeap]         ok 2 - MinHeap.new(values).extract returns a Seq
  [BinaryHeap]         ok 3 - the heap is not modified if the Seq did not generate any values
  [BinaryHeap]         ok 4 - .elems
  [BinaryHeap]         ok 5 - the Seq generates all heap elements in non-decreasing order
  [BinaryHeap]         ok 6 - the heap is empty when the Seq is exhausted
  [BinaryHeap]         ok 7 - .elems
  [BinaryHeap]         1..7
  [BinaryHeap]     ok 1 - extract all values
  [BinaryHeap]     # Subtest: extract n values
  [BinaryHeap]         ok 1 - MaxHeap.extract(n) returns an empty Seq
  [BinaryHeap]         ok 2 - MaxHeap.new(values).extract(n) returns a Seq
  [BinaryHeap]         ok 3 - the heap is not modified if the Seq did not generate any values
  [BinaryHeap]         ok 4 - .elems
  [BinaryHeap]         ok 5 - the Seq generates n elements in non-increasing order
  [BinaryHeap]         ok 6 - the elements are removed from the heap
  [BinaryHeap]         ok 7 - .elems
  [BinaryHeap]         1..7
  [BinaryHeap]     ok 2 - extract n values
  [BinaryHeap]     1..2
  [BinaryHeap] ok 6 - extract values from a heap
  [BinaryHeap] # Subtest: push-pop
  [BinaryHeap]     ok 1 - MinHeap.push-pop(Mu) returns the provided value
  [BinaryHeap]     # Subtest: push-pop when heap instance is empty
  [BinaryHeap]         ok 1 - .push-pop(Mu) returns the provided value
  [BinaryHeap]         ok 2 - heap remains empty
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 2 - push-pop when heap instance is empty
  [BinaryHeap]     # Subtest: push-pop when provided value precedes top
  [BinaryHeap]         ok 1 - .push-pop(value) returns the provided value
  [BinaryHeap]         ok 2 - heap remains the same
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 3 - push-pop when provided value precedes top
  [BinaryHeap]     # Subtest: push-pop when top precedes provided value
  [BinaryHeap]         ok 1 - .push-pop(value) returns the old top
  [BinaryHeap]         ok 2 - heap contains the provided value instead
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 4 - push-pop when top precedes provided value
  [BinaryHeap]     1..4
  [BinaryHeap] ok 7 - push-pop
  [BinaryHeap] # Subtest: clone
  [BinaryHeap]     ok 1 - .clone returns a heap storing the same values
  [BinaryHeap]     ok 2 - .elems
  [BinaryHeap]     ok 3 - the values are stored in a distinct array
  [BinaryHeap]     ok 4 - .elems
  [BinaryHeap]     1..4
  [BinaryHeap] ok 8 - clone
  [BinaryHeap] # Subtest: heapify
  [BinaryHeap]     ok 1 - .new(@array, :in-place) constrains the type of values on the heap
  [BinaryHeap]     ok 2 - ... and puts the elements of the provieded @array in heap order
  [BinaryHeap]     ok 3 - the return value is a heap
  [BinaryHeap]     ok 4 - the heap is based on the @array
  [BinaryHeap]     ok 5 - .elems
  [BinaryHeap]     # Subtest: replace top with value of invalid type
  [BinaryHeap]         ok 1 - .replace(value) dies
  [BinaryHeap]         ok 2 - the heap is not modified
  [BinaryHeap]         ok 3 - .elems
  [BinaryHeap]         1..3
  [BinaryHeap]     ok 6 - replace top with value of invalid type
  [BinaryHeap]     ok 7 - .clone maintains the type constraint of the heap
  [BinaryHeap]     1..7
  [BinaryHeap] ok 9 - heapify
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/02-autovivify.rakutest
  [BinaryHeap] 1..3
  [BinaryHeap] # Subtest: Push onto an uninitialized MaxHeap
  [BinaryHeap]     ok 1 - $heap.push(|values)
  [BinaryHeap]     ok 2 - .values
  [BinaryHeap]     1..2
  [BinaryHeap] ok 1 - Push onto an uninitialized MaxHeap
  [BinaryHeap] # Subtest: Push onto an uninitialized MinHeap
  [BinaryHeap]     ok 1 - $heap.push(|values)
  [BinaryHeap]     ok 2 - .values
  [BinaryHeap]     1..2
  [BinaryHeap] ok 2 - Push onto an uninitialized MinHeap
  [BinaryHeap] # Subtest: Replace the top of an uninitialized heap
  [BinaryHeap]     ok 1 - $heap.replace(new) returns Nil
  [BinaryHeap]     ok 2 - .values
  [BinaryHeap]     1..2
  [BinaryHeap] ok 3 - Replace the top of an uninitialized heap
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/03-exports.rakutest
  [BinaryHeap] 1..7
  [BinaryHeap] # Subtest: infix eqv
  [BinaryHeap]     ok 1 - MaxHeap.new(42) eqv MaxHeap.new(42)
  [BinaryHeap]     ok 2 - MaxHeap.new(42) !eqv MinHeap.new(42)
  [BinaryHeap]     1..2
  [BinaryHeap] ok 1 - infix eqv
  [BinaryHeap] # Subtest: can't import symbols that are not exported
  [BinaryHeap]     1..3
  [BinaryHeap]     ok 1 - 'use BinaryHeap <Foo &heapify>' died
  [BinaryHeap]     ok 2 - right exception type (Exception)
  [BinaryHeap]     ok 3 - .message matches Trying to import from 'BinaryHeap', but the following symbols are not exported: Foo, &heapify
  [BinaryHeap] ok 2 - can't import symbols that are not exported
  [BinaryHeap] ok 3 - imported &heapsort is an alias for &BinaryHeap::heapsort
  [BinaryHeap] # Subtest: heapsort
  [BinaryHeap]     ok 1 - heapsort(@array) returns the array
  [BinaryHeap]     ok 2 - the array elements are sorted in ascending order
  [BinaryHeap]     1..2
  [BinaryHeap] ok 4 - heapsort
  [BinaryHeap] # Subtest: reverse heapsort
  [BinaryHeap]     ok 1 - heapsort(@array, :reverse) returns the array
  [BinaryHeap]     ok 2 - the array elements are sorted in descending order
  [BinaryHeap]     1..2
  [BinaryHeap] ok 5 - reverse heapsort
  [BinaryHeap] # Subtest: heapsort with custom comparator
  [BinaryHeap]     ok 1 - heapsort({$^b cmp $^a}, @array) returns the array
  [BinaryHeap]     ok 2 - the array elements are put in descending order
  [BinaryHeap]     1..2
  [BinaryHeap] ok 6 - heapsort with custom comparator
  [BinaryHeap] # Subtest: reverse heapsort with custom comparator
  [BinaryHeap]     ok 1 - heapsort({$^b cmp $^a}, @array, :reverse) returns the array
  [BinaryHeap]     ok 2 - the array elements are put in ascending order
  [BinaryHeap]     1..2
  [BinaryHeap] ok 7 - reverse heapsort with custom comparator
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/04-factories.rakutest
  [BinaryHeap] 1..3
  [BinaryHeap] # Subtest: imports
  [BinaryHeap]     ok 1 - imported &max-heap is short for &BinaryHeap::max-heap
  [BinaryHeap]     ok 2 - imported &min-heap is short for &BinaryHeap::min-heap
  [BinaryHeap]     1..2
  [BinaryHeap] ok 1 - imports
  [BinaryHeap] not ok 2 - max-heap(*.value <=> *.value, @values)
  [BinaryHeap] # Failed test 'max-heap(*.value <=> *.value, @values)'
  [BinaryHeap] # at t/04-factories.rakutest line 24
  [BinaryHeap] # expected: (:baz(4), :foobar(3), :bar(2), :foo(1))
  [BinaryHeap] #  matcher: 'infix:<eqv>'
  [BinaryHeap] #      got: (:baz(4), :foobar(3), :bar(2), :foo(1)).Seq
  [BinaryHeap] not ok 3 - min-heap(*.value <=> *.value, @values)
  [BinaryHeap] # Failed test 'min-heap(*.value <=> *.value, @values)'
  [BinaryHeap] # at t/04-factories.rakutest line 30
  [BinaryHeap] # expected: (:foo(1), :bar(2), :foobar(3), :baz(4))
  [BinaryHeap] #  matcher: 'infix:<eqv>'
  [BinaryHeap] #      got: (:foo(1), :bar(2), :foobar(3), :baz(4)).Seq
  [BinaryHeap] # You failed 2 tests of 3
  [BinaryHeap] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/114b644c9e7e88c0b7d575d1c31010fcf80b6aef.tar.gz t/05-representation.rakutest
  [BinaryHeap] 1..6
  [BinaryHeap] ok 1 - BinaryHeap::MinHeap.new.gist
  [BinaryHeap] ok 2 - BinaryHeap::MinHeap.new.raku
  [BinaryHeap] ok 3 - BinaryHeap::MinHeap.new(1, 2, 3).gist
  [BinaryHeap] ok 4 - BinaryHeap::MinHeap.new(1, 2, 3).raku
  [BinaryHeap] ok 5 - BinaryHeap::MinHeap.new(1, 3, 2).gist
  [BinaryHeap] ok 6 - BinaryHeap::MinHeap.new(1, 3, 2).raku
  ===> Testing [FAIL]: BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2>
  [BinaryHeap] Failed to get passing tests, but continuing with --force-test
  ===> Installing: BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2>
  ===> Install [OK] for BinaryHeap:ver<2.0.3>:auth<zef:dumarchie>:api<2>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 14.757s
               CPU time consumed: 9.265s
                     Memory peak: 1G (swap: 0B)

  ```
  </details>
* [ ] [CSS::Properties](https://raku.land/zef:dwarring/CSS::Properties) – Fail, Bisected: [afee7d8](https://github.com/rakudo/rakudo/commit/afee7d8d3197b7a093355d98a90f6f86d8bda32a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1414100-i1463843.service; invocation ID: 0fbbbfbdaaf543e58441e6aa67ee6347
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: CSS::Properties
  ===> Found: CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10> [via Zef::Repository::Ecosystems<fez>]
  [CSS::Properties] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549664.1414101.6590.106843499697/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz https://360.zef.pm/C/SS/CSS_PROPERTIES/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz
  ===> Fetching [OK]: CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549664.1414101.6590.106843499697/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz
  [CSS::Properties] Command: tar -t -f ./59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz
  [CSS::Properties] Command: tar -xvf ./59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz -C ../59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz
  ===> Extraction [OK]: CSS::Properties to /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz
  ===> Testing: CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10>
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/00-readme.t
  [CSS::Properties] 1..12
  [CSS::Properties] ok 1 - code sample
  [CSS::Properties] dropping unknown CSS1 property azimuth
  [CSS::Properties] ok 2 - code sample
  [CSS::Properties] ok 3 - code sample
  [CSS::Properties] ok 4 - code sample
  [CSS::Properties] ok 5 - code sample
  [CSS::Properties] ok 6 - code sample
  [CSS::Properties] ok 7 - code sample
  [CSS::Properties] ok 8 - code sample
  [CSS::Properties] ok 9 - code sample
  [CSS::Properties] ok 10 - code sample
  [CSS::Properties] ok 11 - code sample
  [CSS::Properties] ok 12 - code sample
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/01-property-basic.t
  [CSS::Properties] 1..21
  [CSS::Properties] ok 1 - $prop.name
  [CSS::Properties] ok 2 - $prop.box
  [CSS::Properties] ok 3 - $prop.inherit
  [CSS::Properties] ok 4 - $prop.synopsis
  [CSS::Properties] ok 5 - $prop.default
  [CSS::Properties] ok 6 - missing edges detected
  [CSS::Properties] ok 7 - $prop.name
  [CSS::Properties] ok 8 - $prop.box
  [CSS::Properties] ok 9 - $prop.inherit
  [CSS::Properties] ok 10 - $prop.synopsis
  [CSS::Properties] ok 11 - $prop.top.name
  [CSS::Properties] ok 12 - declared property
  [CSS::Properties] ok 13 - defaulted property
  [CSS::Properties] ok 14 - write
  [CSS::Properties] ok 15 - write
  [CSS::Properties] ok 16 - copy/write
  [CSS::Properties] ok 17 - 
  [CSS::Properties] ok 18 - 
  [CSS::Properties] ok 19 - 
  [CSS::Properties] ok 20 - 
  [CSS::Properties] ok 21 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/02-style-basic.t
  [CSS::Properties] 1..15
  [CSS::Properties] ok 1 - 
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - 
  [CSS::Properties] ok 7 - 
  [CSS::Properties] ok 8 - important property
  [CSS::Properties] ok 9 - unimportant property
  [CSS::Properties] ok 10 - 
  [CSS::Properties] ok 11 - 
  [CSS::Properties] ok 12 - 
  [CSS::Properties] ok 13 - 
  [CSS::Properties] ok 14 - 
  [CSS::Properties] ok 15 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/ast.t
  [CSS::Properties] 1..4
  [CSS::Properties] ok 1 - ast
  [CSS::Properties] ok 2 - style unoptimized
  [CSS::Properties] ok 3 - ast
  [CSS::Properties] ok 4 - style optimized
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/at-font-face.t
  [CSS::Properties] 1..30
  [CSS::Properties] ok 1 - 
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - 
  [CSS::Properties] ok 7 - 
  [CSS::Properties] ok 8 - 
  [CSS::Properties] ok 9 - 
  [CSS::Properties] ok 10 - 
  [CSS::Properties] ok 11 - 
  [CSS::Properties] ok 12 - 
  [CSS::Properties] ok 13 - 
  [CSS::Properties] ok 14 - 
  [CSS::Properties] ok 15 - 
  [CSS::Properties] ok 16 - 
  [CSS::Properties] ok 17 - 
  [CSS::Properties] ok 18 - 
  [CSS::Properties] ok 19 - 
  [CSS::Properties] ok 20 - 
  [CSS::Properties] ok 21 - 
  [CSS::Properties] ok 22 - 
  [CSS::Properties] ok 23 - 
  [CSS::Properties] ok 24 - 
  [CSS::Properties] ok 25 - 
  [CSS::Properties] ok 26 - 
  [CSS::Properties] ok 27 - 
  [CSS::Properties] ok 28 - 
  [CSS::Properties] ok 29 - 
  [CSS::Properties] ok 30 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/box-fonts.t
  [CSS::Properties] 1..5
  [CSS::Properties] # Subtest: basic
  [CSS::Properties]     1..9
  [CSS::Properties]     ok 1 - em
  [CSS::Properties]     ok 2 - ex
  [CSS::Properties]     ok 3 - font-style
  [CSS::Properties]     ok 4 - font-weight
  [CSS::Properties]     ok 5 - font-family
  [CSS::Properties]     ok 6 - line-height
  [CSS::Properties]     ok 7 - font-stretch
  [CSS::Properties]     ok 8 - measuring unit
  [CSS::Properties]     ok 9 - $font.Str
  [CSS::Properties] ok 1 - basic
  [CSS::Properties] # Subtest: measure
  [CSS::Properties]     1..9
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - measure numeric
  [CSS::Properties]     ok 5 - measure percentage font-size
  [CSS::Properties]     ok 6 - measure percentage font-size
  [CSS::Properties]     ok 7 - measure percentage font-size
  [CSS::Properties]     ok 8 - measure named font-size
  [CSS::Properties]     ok 9 - measure named font-size
  [CSS::Properties] ok 2 - measure
  [CSS::Properties] # Subtest: patterns
  [CSS::Properties]     1..3
  [CSS::Properties]     ok 1 - fontconfig-pattern
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - fontconfig-pattern
  [CSS::Properties] ok 3 - patterns
  [CSS::Properties] # Subtest: match basic
  [CSS::Properties]     1..2
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties] ok 4 - match basic
  [CSS::Properties] # Subtest: match styles
  [CSS::Properties]     1..6
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     ok 6 - 
  [CSS::Properties] ok 5 - match styles
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/box-measure.t
  [CSS::Properties] 1..19
  [CSS::Properties] ok 1 - default units
  [CSS::Properties] ok 2 - .Array
  [CSS::Properties] ok 3 - .padding
  [CSS::Properties] ok 4 - .border
  [CSS::Properties] ok 5 - .margin
  [CSS::Properties] ok 6 - .width
  [CSS::Properties] ok 7 - .height
  [CSS::Properties] ok 8 - .width("padding")
  [CSS::Properties] ok 9 - .height("padding")
  [CSS::Properties] ok 10 - .padding-XXX
  [CSS::Properties] ok 11 - .border-XXX
  [CSS::Properties] ok 12 - .margin-XXX
  [CSS::Properties] ok 13 - .border-width
  [CSS::Properties] ok 14 - .border-height
  [CSS::Properties] ok 15 - 
  [CSS::Properties] ok 16 - changed units
  [CSS::Properties] ok 17 - .Array
  [CSS::Properties] ok 18 - .padding
  [CSS::Properties] ok 19 - adjusted .margin
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/box.t
  [CSS::Properties] 1..20
  [CSS::Properties] ok 1 - .Array
  [CSS::Properties] ok 2 - .padding
  [CSS::Properties] ok 3 - .border
  [CSS::Properties] ok 4 - .margin
  [CSS::Properties] ok 5 - .width
  [CSS::Properties] ok 6 - .height
  [CSS::Properties] ok 7 - .width("padding")
  [CSS::Properties] ok 8 - .height("padding")
  [CSS::Properties] ok 9 - .padding-XXX
  [CSS::Properties] ok 10 - .border-XXX
  [CSS::Properties] ok 11 - .margin-XXX
  [CSS::Properties] ok 12 - .border-width
  [CSS::Properties] ok 13 - .border-height
  [CSS::Properties] ok 14 - .translate
  [CSS::Properties] ok 15 - translate padding
  [CSS::Properties] ok 16 - .move
  [CSS::Properties] ok 17 - move padding
  [CSS::Properties] ok 18 - .resize
  [CSS::Properties] ok 19 - illegal initial size
  [CSS::Properties] not ok 20 - illegal resize # TODO reimplement resize checks
  [CSS::Properties] # Failed test 'illegal resize'
  [CSS::Properties] # at t/box.t line 52
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/calc.t
  [CSS::Properties] 1..4
  [CSS::Properties] # Subtest: font-size
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     1..3
  [CSS::Properties] ok 1 - font-size
  [CSS::Properties] # Subtest: basic arithmetic
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     1..4
  [CSS::Properties] ok 2 - basic arithmetic
  [CSS::Properties] # Subtest: associativety/precedence
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     ok 7 - 
  [CSS::Properties]     1..7
  [CSS::Properties] ok 3 - associativety/precedence
  [CSS::Properties] # Subtest: div/minus
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     1..4
  [CSS::Properties] ok 4 - div/minus
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/colors.t
  [CSS::Properties] 1..33
  [CSS::Properties] ok 1 - :values constructor
  [CSS::Properties] ok 2 - :values constructor
  [CSS::Properties] ok 3 - serialization
  [CSS::Properties] ok 4 - :values constructor
  [CSS::Properties] ok 5 - :values constructor
  [CSS::Properties] ok 6 - :values constructor
  [CSS::Properties] ok 7 - serialization
  [CSS::Properties] ok 8 - :values constructor
  [CSS::Properties] ok 9 - :values constructor
  [CSS::Properties] ok 10 - :values constructor
  [CSS::Properties] ok 11 - :values constructor
  [CSS::Properties] ok 12 - serialization
  [CSS::Properties] ok 13 - :values constructor
  [CSS::Properties] ok 14 - :values constructor
  [CSS::Properties] ok 15 - :values constructor
  [CSS::Properties] ok 16 - serialization
  [CSS::Properties] ok 17 - :values constructor
  [CSS::Properties] ok 18 - :values constructor
  [CSS::Properties] ok 19 - :values constructor
  [CSS::Properties] ok 20 - serialization
  [CSS::Properties] ok 21 - :values constructor
  [CSS::Properties] ok 22 - :values constructor
  [CSS::Properties] ok 23 - :values constructor
  [CSS::Properties] ok 24 - serialization
  [CSS::Properties] ok 25 - :values constructor
  [CSS::Properties] ok 26 - :values constructor
  [CSS::Properties] ok 27 - :values constructor
  [CSS::Properties] ok 28 - serialization
  [CSS::Properties] ok 29 - border-*-color default
  [CSS::Properties] ok 30 - border-*-color default
  [CSS::Properties] ok 31 - border-*-color default
  [CSS::Properties] ok 32 - color assignment
  [CSS::Properties] ok 33 - color assigment
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/css-fonts.t
  [CSS::Properties] 1..4
  [CSS::Properties] # Subtest: props
  [CSS::Properties]     ok 1 - font-style
  [CSS::Properties]     ok 2 - font-weight
  [CSS::Properties]     ok 3 - font-family
  [CSS::Properties]     ok 4 - font-size
  [CSS::Properties]     ok 5 - line-height
  [CSS::Properties]     1..5
  [CSS::Properties] ok 1 - props
  [CSS::Properties] # Subtest: serialization
  [CSS::Properties]     1..33
  [CSS::Properties]     ok 1 - serialization
  [CSS::Properties]     ok 2 - (empty)
  [CSS::Properties]     ok 3 - font-family
  [CSS::Properties]     ok 4 - line-height
  [CSS::Properties]     ok 5 - font-family line-height
  [CSS::Properties]     ok 6 - font-size
  [CSS::Properties]     ok 7 - font-family font-size
  [CSS::Properties]     ok 8 - font-size line-height
  [CSS::Properties]     ok 9 - font-family font-size line-height
  [CSS::Properties]     ok 10 - font-weight
  [CSS::Properties]     ok 11 - font-family font-weight
  [CSS::Properties]     ok 12 - font-weight line-height
  [CSS::Properties]     ok 13 - font-family font-weight line-height
  [CSS::Properties]     ok 14 - font-size font-weight
  [CSS::Properties]     ok 15 - font-family font-size font-weight
  [CSS::Properties]     ok 16 - font-size font-weight line-height
  [CSS::Properties]     ok 17 - font-family font-size font-weight line-height
  [CSS::Properties]     ok 18 - font-style
  [CSS::Properties]     ok 19 - font-family font-style
  [CSS::Properties]     ok 20 - font-style line-height
  [CSS::Properties]     ok 21 - font-family font-style line-height
  [CSS::Properties]     ok 22 - font-size font-style
  [CSS::Properties]     ok 23 - font-family font-size font-style
  [CSS::Properties]     ok 24 - font-size font-style line-height
  [CSS::Properties]     ok 25 - font-family font-size font-style line-height
  [CSS::Properties]     ok 26 - font-style font-weight
  [CSS::Properties]     ok 27 - font-family font-style font-weight
  [CSS::Properties]     ok 28 - font-style font-weight line-height
  [CSS::Properties]     ok 29 - font-family font-style font-weight line-height
  [CSS::Properties]     ok 30 - font-size font-style font-weight
  [CSS::Properties]     ok 31 - font-family font-size font-style font-weight
  [CSS::Properties]     ok 32 - font-size font-style font-weight line-height
  [CSS::Properties]     ok 33 - font-family font-size font-style font-weight line-height
  [CSS::Properties] ok 2 - serialization
  [CSS::Properties] # Subtest: issue#23
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     1..1
  [CSS::Properties] ok 3 - issue \#23
  [CSS::Properties] # Subtest: change em
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     1..2
  [CSS::Properties] ok 4 - change em
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/declarations.t
  [CSS::Properties] 1..47
  [CSS::Properties] ok 1 - :values constructor
  [CSS::Properties] ok 2 - box property
  [CSS::Properties] ok 3 - edges property
  [CSS::Properties] ok 4 - simple property
  [CSS::Properties] ok 5 - margin-left is a margin edge
  [CSS::Properties] ok 6 - default azimuth
  [CSS::Properties] ok 7 - default azimuth
  [CSS::Properties] ok 8 - default margin
  [CSS::Properties] ok 9 - default margin-left
  [CSS::Properties] ok 10 - default margin left type
  [CSS::Properties] ok 11 - default background-color
  [CSS::Properties] ok 12 - default background-color
  [CSS::Properties] ok 13 - basic css rewritten
  [CSS::Properties] ok 14 - default background position
  [CSS::Properties] ok 15 - list parse
  [CSS::Properties] ok 16 - list parse
  [CSS::Properties] ok 17 - list parse
  [CSS::Properties] ok 18 - background-color reset
  [CSS::Properties] ok 19 - background-color reset
  [CSS::Properties] ok 20 - updated margin-right value
  [CSS::Properties] ok 21 - updated margin-right units
  [CSS::Properties] ok 22 - updated margin-right units
  [CSS::Properties] ok 23 - updated margin
  [CSS::Properties] ok 24 - measured margin
  [CSS::Properties] ok 25 - reset margin
  [CSS::Properties] ok 26 - reset margin-left
  [CSS::Properties] ok 27 - named and rgb colors
  [CSS::Properties] ok 28 - 
  [CSS::Properties] ok 29 - border-color string coercement
  [CSS::Properties] ok 30 - border-color reset
  [CSS::Properties] ok 31 - struct str assignment
  [CSS::Properties] ok 32 - border top
  [CSS::Properties] ok 33 - border top width
  [CSS::Properties] ok 34 - border top width
  [CSS::Properties] ok 35 - border top color
  [CSS::Properties] ok 36 - border top color
  [CSS::Properties] ok 37 - struct hash assignment
  [CSS::Properties] ok 38 - border top width
  [CSS::Properties] ok 39 - border top color
  [CSS::Properties] ok 40 - border top color
  [CSS::Properties] ok 41 - border top color
  [CSS::Properties] ok 42 - reset border top width
  [CSS::Properties] ok 43 - reset border top color
  [CSS::Properties] ok 44 - info on a container property
  [CSS::Properties] ok 45 - default text-align
  [CSS::Properties] ok 46 - default text-align (direction rtl)
  [CSS::Properties] ok 47 - updated text-direction
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/errors.t
  [CSS::Properties] 1..6
  [CSS::Properties] ok 1 - 
  [CSS::Properties] unable to parse CSS3 property 'width: 2furlongs;'
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] unable to parse CSS3 property 'width: foo(42);'
  [CSS::Properties] ok 5 - 
  [CSS::Properties] expected type of length, got number: calc(42)
  [CSS::Properties] ok 6 - 
  [CSS::Properties] unable to evaluate expression: calc(2em + 3hz)
  [CSS::Properties] skipping: 'foo'
  [CSS::Properties] usage: calc( <calc-sum> )
  [CSS::Properties] unable to evaluate expression: calc('foo')
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/extend.t
  [CSS::Properties] 1..22
  [CSS::Properties] ok 1 - info.name
  [CSS::Properties] ok 2 - info.synopsis
  [CSS::Properties] ok 3 - info.default
  [CSS::Properties] ok 4 - info.name
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - info.default
  [CSS::Properties] ok 7 - coercer called
  [CSS::Properties] ok 8 - 
  [CSS::Properties] ok 9 - The object is-a 'Int'
  [CSS::Properties] ok 10 - property set
  [CSS::Properties] ok 11 - coercer called
  [CSS::Properties] ok 12 - property get
  [CSS::Properties] ok 13 - properties
  [CSS::Properties] ok 14 - serialization
  [CSS::Properties] ok 15 - serialization (default)
  [CSS::Properties] ok 16 - reserialization
  [CSS::Properties] ok 17 - 
  [CSS::Properties] ok 18 - 
  [CSS::Properties] ok 19 - case insensitivity
  [CSS::Properties] # Subtest: parse
  [CSS::Properties]     ok 1 - coercer called
  [CSS::Properties]     ok 2 - coercer called
  [CSS::Properties]     ok 3 - serialization
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - The object is-a 'Int'
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     1..6
  [CSS::Properties] ok 20 - parse
  [CSS::Properties] # Subtest: invalid
  [CSS::Properties]     ok 1 - serialization
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - The object is-a 'Int'
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     1..4
  [CSS::Properties] ok 21 - invalid
  [CSS::Properties] # Subtest: any
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     1..5
  [CSS::Properties] ok 22 - any
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/important.t
  [CSS::Properties] 1..14
  [CSS::Properties] ok 1 - 
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - importance setter
  [CSS::Properties] ok 7 - importance setter - box
  [CSS::Properties] ok 8 - importance setter - box
  [CSS::Properties] ok 9 - 
  [CSS::Properties] ok 10 - 
  [CSS::Properties] ok 11 - 
  [CSS::Properties] ok 12 - 
  [CSS::Properties] ok 13 - 
  [CSS::Properties] ok 14 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/inherit.t
  [CSS::Properties] 1..23
  [CSS::Properties] ok 1 - 
  [CSS::Properties] ok 2 - overridden value
  [CSS::Properties] ok 3 - overridden value
  [CSS::Properties] ok 4 - 'initial'
  [CSS::Properties] ok 5 - 'initial'
  [CSS::Properties] ok 6 - 'inherit'
  [CSS::Properties] ok 7 - 'inherit'
  [CSS::Properties] ok 8 - color inherit metadata
  [CSS::Properties] ok 9 - inherited property
  [CSS::Properties] ok 10 - margin-bottom inherit metadata
  [CSS::Properties] ok 11 - non-inhertiable property
  [CSS::Properties] ok 12 - inherited box value
  [CSS::Properties] ok 13 - inherited value
  [CSS::Properties] ok 14 - initial box value
  [CSS::Properties] ok 15 - inherited !important property
  [CSS::Properties] ok 16 - !important is not inherited
  [CSS::Properties] ok 17 - inherit from object
  [CSS::Properties] ok 18 - inherit from string
  [CSS::Properties] # Subtest: font-size inheritance
  [CSS::Properties]     ok 1 - inherit absolute font-size
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - inheritance of relative font-size
  [CSS::Properties]     ok 4 - relative font-size inheritance
  [CSS::Properties]     ok 5 - inherited font size measurement
  [CSS::Properties]     ok 6 - computed font size measurement
  [CSS::Properties]     ok 7 - relative font size measurement
  [CSS::Properties]     ok 8 - relative font size measurement
  [CSS::Properties]     1..8
  [CSS::Properties] ok 19 - font-size inheritance
  [CSS::Properties] # Subtest: inherit+clone
  [CSS::Properties]     ok 1 - speech-rate inherit metadata
  [CSS::Properties]     ok 2 - cloned css
  [CSS::Properties]     ok 3 - cloned css
  [CSS::Properties]     ok 4 - cloned+inherited css
  [CSS::Properties]     ok 5 - inherited+cloned css
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     ok 7 - 
  [CSS::Properties]     ok 8 - 
  [CSS::Properties]     ok 9 - original css
  [CSS::Properties]     1..9
  [CSS::Properties] ok 20 - inherit+clone
  [CSS::Properties] # Subtest: issue#11 inheritence
  [CSS::Properties]     1..2
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties] ok 21 - issue \#11 inheritence
  [CSS::Properties] # Subtest: early inheritence
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     1..3
  [CSS::Properties] ok 22 - early inheritence
  [CSS::Properties] # Subtest: late inheritance
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     1..4
  [CSS::Properties] ok 23 - late inheritance
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/measure.t
  [CSS::Properties] 1..34
  [CSS::Properties] ok 1 - $css.measure($.viewport-width)
  [CSS::Properties] ok 2 - $css.measure($.viewport-height)
  [CSS::Properties] ok 3 - default units
  [CSS::Properties] ok 4 - $css.measure(pt)
  [CSS::Properties] ok 5 - $css.measure(px)
  [CSS::Properties] ok 6 - $css.measure(pc)
  [CSS::Properties] ok 7 - $css.measure(em)
  [CSS::Properties] ok 8 - $css.measure(ex)
  [CSS::Properties] ok 9 - $css.measure(vw)
  [CSS::Properties] ok 10 - $css.measure(vh)
  [CSS::Properties] ok 11 - $css.measure("thin")
  [CSS::Properties] ok 12 - $css.measure("medium")
  [CSS::Properties] ok 13 - $css.measure(:font-size<medium>)
  [CSS::Properties] ok 14 - $css.measure("thick")
  [CSS::Properties] ok 15 - $css.measure("x-large")
  [CSS::Properties] ok 16 - $css.measure("smaller")
  [CSS::Properties] # Subtest: font-size
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     ok 7 - 
  [CSS::Properties]     ok 8 - 
  [CSS::Properties]     ok 9 - 
  [CSS::Properties]     ok 10 - 
  [CSS::Properties]     ok 11 - 
  [CSS::Properties]     ok 12 - 
  [CSS::Properties]     ok 13 - 
  [CSS::Properties]     ok 14 - 
  [CSS::Properties]     1..14
  [CSS::Properties] ok 17 - font-size
  [CSS::Properties] # Subtest: font-weight
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     ok 7 - 
  [CSS::Properties]     ok 8 - 
  [CSS::Properties]     ok 9 - 
  [CSS::Properties]     ok 10 - 
  [CSS::Properties]     ok 11 - 
  [CSS::Properties]     ok 12 - 
  [CSS::Properties]     ok 13 - 
  [CSS::Properties]     1..13
  [CSS::Properties] ok 18 - font-weight
  [CSS::Properties] ok 19 - 
  [CSS::Properties] ok 20 - 
  [CSS::Properties] ok 21 - 
  [CSS::Properties] ok 22 - changed units
  [CSS::Properties] ok 23 - $css.measure(in)
  [CSS::Properties] ok 24 - $css.measure(in)
  [CSS::Properties] ok 25 - $css.measure(in)
  [CSS::Properties] ok 26 - 
  [CSS::Properties] ok 27 - 
  [CSS::Properties] ok 28 - 
  [CSS::Properties] ok 29 - 
  [CSS::Properties] ok 30 - 
  [CSS::Properties] ok 31 - 
  [CSS::Properties] ok 32 - 
  [CSS::Properties] # Subtest: simple background-position
  [CSS::Properties]     ok 1 - measure background-position
  [CSS::Properties]     ok 2 - measure background-position: 10% 20%
  [CSS::Properties]     ok 3 - measure background-position: center 100%
  [CSS::Properties]     ok 4 - measure background-position: 10pt 20pt
  [CSS::Properties]     1..4
  [CSS::Properties] ok 33 - simple background-position
  [CSS::Properties] ok 34 - # SKIP multi-layer background-position
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/modules.t
  [CSS::Properties] 1..5
  [CSS::Properties] ok 1 - azimuth is unknown in CSS1
  [CSS::Properties] ok 2 - azimuth is known in CSS21
  [CSS::Properties] ok 3 - azimuth is known in CSS3
  [CSS::Properties] dropping unknown @fontface property azimuth
  [CSS::Properties] ok 4 - src is known in @font-face
  [CSS::Properties] ok 5 - azimuth is unknown in @font-face
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/optimize.t
  [CSS::Properties] 1..16
  [CSS::Properties] ok 1 - optimised ast border:1px solid red;
  [CSS::Properties] ok 2 - optimised via CSS::Properties border:1px solid red;
  [CSS::Properties] ok 3 - optimised ast border-width:5pt 5px 5in 5mm;
  [CSS::Properties] ok 4 - optimised via CSS::Properties border-width:5pt 5px 5in 5mm;
  [CSS::Properties] ok 5 - optimised ast border-top:5px!important;
  [CSS::Properties] ok 6 - optimised via CSS::Properties border-top:5px!important;
  [CSS::Properties] ok 7 - optimised ast border:5pt solid; border-color:red green blue yellow;
  [CSS::Properties] ok 8 - optimised via CSS::Properties border:5pt solid; border-color:red green blue yellow;
  [CSS::Properties] ok 9 - optimised ast font-family:times; font-size:inherit; font-weight:inherit;
  [CSS::Properties] ok 10 - optimised via CSS::Properties font-family:times; font-size:inherit; font-weight:inherit;
  [CSS::Properties] ok 11 - optimised ast background:no-repeat 50% 75%;
  [CSS::Properties] ok 12 - optimised via CSS::Properties background:no-repeat 50% 75%; # TODO CSS Properties backgrounds
  [CSS::Properties] ok 13 - optimised ast font:1.1em/1.3 Verdana, Arial, sans-serif;
  [CSS::Properties] ok 14 - optimised via CSS::Properties font:1.1em/1.3 Verdana, Arial, sans-serif;
  [CSS::Properties] ok 15 - optimised ast list-style:circle;
  [CSS::Properties] ok 16 - optimised via CSS::Properties list-style:circle;
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/page-box.t
  [CSS::Properties] 1..19
  [CSS::Properties] ok 1 - 
  [CSS::Properties] ok 2 - .Array
  [CSS::Properties] ok 3 - .Array
  [CSS::Properties] ok 4 - css
  [CSS::Properties] ok 5 - .margin (mm)
  [CSS::Properties] ok 6 - .margin (pt)
  [CSS::Properties] ok 7 - .border
  [CSS::Properties] ok 8 - .padding
  [CSS::Properties] ok 9 - .content
  [CSS::Properties] ok 10 - .margin auto
  [CSS::Properties] ok 11 - .border auto
  [CSS::Properties] ok 12 - .padding auto
  [CSS::Properties] ok 13 - .content auto
  [CSS::Properties] ok 14 - .margin auto
  [CSS::Properties] ok 15 - .border auto
  [CSS::Properties] ok 16 - .padding auto
  [CSS::Properties] ok 17 - .content auto (mm)
  [CSS::Properties] ok 18 - .content auto (pt)
  [CSS::Properties] ok 19 - auto/min/max
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/svg-properties.t
  [CSS::Properties] ok 1 - alignment-baseline:after-edge;
  [CSS::Properties] ok 2 - baseline-shift:super;
  [CSS::Properties] ok 3 - baseline-shift:1.5em;
  [CSS::Properties] ok 4 - baseline-shift:1.5em; - type
  [CSS::Properties] ok 5 - baseline-shift:4%;
  [CSS::Properties] ok 6 - baseline-shift:4%; - type
  [CSS::Properties] ok 7 - color:red;
  [CSS::Properties] ok 8 - color:rgb(10%,20,30);
  [CSS::Properties] ok 9 - color:rgb(10%,20,30); - type
  [CSS::Properties] ok 10 - color-interpolation:sRGB;
  [CSS::Properties] ok 11 - color-interpolation:Srgb;
  [CSS::Properties] ok 12 - color-interpolation:lInearRgB;
  [CSS::Properties] ok 13 - color-rendering:optimizeSpeed;
  [CSS::Properties] ok 14 - direction:ltr;
  [CSS::Properties] ok 15 - direction:rtl;
  [CSS::Properties] ok 16 - display:table-cell;
  [CSS::Properties] ok 17 - dominant-baseline:hanging;
  [CSS::Properties] ok 18 - fill:rgb(10,20,10%);
  [CSS::Properties] ok 19 - fill-opacity:0.75;
  [CSS::Properties] ok 20 - fill-opacity:75%;
  [CSS::Properties] ok 21 - fill-rule:evenOdD;
  [CSS::Properties] ok 22 - font-variant:small-Caps;
  [CSS::Properties] ok 23 - glyph-orientation-vertical:45deg;
  [CSS::Properties] ok 24 - glyph-orientation-vertical:7;
  [CSS::Properties] ok 25 - image-rendering:optimizeQuality;
  [CSS::Properties] ok 26 - line-height:90%;
  [CSS::Properties] ok 27 - line-height:normal;
  [CSS::Properties] ok 28 - line-height:42;
  [CSS::Properties] ok 29 - marker-start:none;
  [CSS::Properties] ok 30 - marker-start:url('http://www.example.com/pinkish.gif');
  [CSS::Properties] ok 31 - marker-mid:none;
  [CSS::Properties] ok 32 - marker-end:none;
  [CSS::Properties] ok 33 - marker:url('http://www.example.com/greenish.gif') url('http://www.example.com/pinkish.gif');
  [CSS::Properties] ok 34 - opacity:0.75;
  [CSS::Properties] ok 35 - opacity:75%;
  [CSS::Properties] ok 36 - overflow:hidden;
  [CSS::Properties] ok 37 - paint-order:fill stroke;
  [CSS::Properties] ok 38 - shape-rendering:crispEdges;
  [CSS::Properties] ok 39 - stop-opacity:0.75;
  [CSS::Properties] ok 40 - stop-opacity:75%;
  [CSS::Properties] ok 41 - stroke:none;
  [CSS::Properties] ok 42 - stroke:black;
  [CSS::Properties] ok 43 - stroke-dasharray:20, 10;
  [CSS::Properties] ok 44 - stroke-dasharray:em, 2em;
  [CSS::Properties] ok 45 - stroke-dashoffset:3em;
  [CSS::Properties] ok 46 - stroke-linecap:round;
  [CSS::Properties] ok 47 - stroke-linejoin:bevel;
  [CSS::Properties] ok 48 - stroke-opacity:0.75;
  [CSS::Properties] ok 49 - stroke-opacity:75%;
  [CSS::Properties] ok 50 - stroke-width:0.1em;
  [CSS::Properties] ok 51 - stroke-width:2.5;
  [CSS::Properties] ok 52 - stroke-miterlimit:5;
  [CSS::Properties] ok 53 - text-anchor:middle;
  [CSS::Properties] ok 54 - text-decoration:underline blink;
  [CSS::Properties] ok 55 - text-rendering:geometricPrecision;
  [CSS::Properties] ok 56 - visibility:hidden;
  [CSS::Properties] ok 57 - white-space:pre;
  [CSS::Properties] ok 58 - writing-mode:rl-tb;
  [CSS::Properties] 1..58
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/threads.t
  [CSS::Properties] 1..4
  [CSS::Properties] ok 1 - basic
  [CSS::Properties] ok 2 - info
  [CSS::Properties] ok 3 - no property name errors
  [CSS::Properties] ok 4 - mixed modules
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/units.t
  [CSS::Properties] ok 1 - pt + pt
  [CSS::Properties] ok 2 - pt + pt
  [CSS::Properties] ok 3 - gist
  [CSS::Properties] ok 4 - pt += pt
  [CSS::Properties] ok 5 - pt += pt
  [CSS::Properties] ok 6 - pt + mm
  [CSS::Properties] ok 7 - pt + mm
  [CSS::Properties] ok 8 - pt + mm
  [CSS::Properties] ok 9 - pt - in
  [CSS::Properties] ok 10 - pt + in
  [CSS::Properties] ok 11 - pt +css in
  [CSS::Properties] ok 12 - pt + px
  [CSS::Properties] ok 13 - pt + pc
  [CSS::Properties] ok 14 - pt - pc
  [CSS::Properties] ok 15 - pt -css pc
  [CSS::Properties] ok 16 - ms to s
  [CSS::Properties] ok 17 - hz to khz
  [CSS::Properties] ok 18 - turn to deg
  [CSS::Properties] ok 19 - turn to rad
  [CSS::Properties] ok 20 - px to pt
  [CSS::Properties] ok 21 - dpi to dpcm
  [CSS::Properties] ok 22 - dppx to dpi
  [CSS::Properties] 1..22
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/vivify.t
  [CSS::Properties] 1..6
  [CSS::Properties] ok 1 - vivifed-name
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/write.t
  [CSS::Properties] 1..25
  [CSS::Properties] ok 1 - unoptimized edge property
  [CSS::Properties] ok 2 - edge property
  [CSS::Properties] ok 3 - consolidation of edge properties
  [CSS::Properties] ok 4 - consolidation of edge properties
  [CSS::Properties] ok 5 - optimized properties
  [CSS::Properties] ok 6 - edge unoptimized
  [CSS::Properties] ok 7 - edge optimized
  [CSS::Properties] ok 8 - compound edge
  [CSS::Properties] ok 9 - compound edge - unoptimized
  [CSS::Properties] ok 10 - compound edge - re-optimized
  [CSS::Properties] ok 11 - compound edge - partial optimization
  [CSS::Properties] ok 12 - optimization of default values
  [CSS::Properties] ok 13 - 
  [CSS::Properties] ok 14 - 
  [CSS::Properties] ok 15 - 
  [CSS::Properties] ok 16 - 
  [CSS::Properties] ok 17 - 
  [CSS::Properties] ok 18 - 
  [CSS::Properties] ok 19 - 
  [CSS::Properties] ok 20 - 
  [CSS::Properties] ok 21 - 
  [CSS::Properties] ok 22 - 
  [CSS::Properties] ok 23 - 
  [CSS::Properties] ok 24 - 
  [CSS::Properties] ok 25 - 
  ===> Testing [OK] for CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10>
  ===> Installing: CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10>
  ===> Install [OK] for CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 52.674s
               CPU time consumed: 4min 17.864s
                     Memory peak: 2.3G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1411667-i1459597.service; invocation ID: 331ad2f6dc954b6faf9b15d7545d9493
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: CSS::Properties
  ===> Found: CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10> [via Zef::Repository::Ecosystems<fez>]
  [CSS::Properties] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549561.1411668.3501.6858366407146/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz https://360.zef.pm/C/SS/CSS_PROPERTIES/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz
  ===> Fetching [OK]: CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549561.1411668.3501.6858366407146/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz
  [CSS::Properties] Command: tar -t -f ./59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz
  [CSS::Properties] Command: tar -xvf ./59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz -C ../59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz
  ===> Extraction [OK]: CSS::Properties to /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz
  ===> Testing: CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10>
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/00-readme.t
  [CSS::Properties] 1..12
  [CSS::Properties] ok 1 - code sample
  [CSS::Properties] dropping unknown CSS1 property azimuth
  [CSS::Properties] ok 2 - code sample
  [CSS::Properties] ok 3 - code sample
  [CSS::Properties] ok 4 - code sample
  [CSS::Properties] ok 5 - code sample
  [CSS::Properties] ok 6 - code sample
  [CSS::Properties] ok 7 - code sample
  [CSS::Properties] ok 8 - code sample
  [CSS::Properties] ok 9 - code sample
  [CSS::Properties] ok 10 - code sample
  [CSS::Properties] ok 11 - code sample
  [CSS::Properties] ok 12 - code sample
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/01-property-basic.t
  [CSS::Properties] 1..21
  [CSS::Properties] ok 1 - $prop.name
  [CSS::Properties] ok 2 - $prop.box
  [CSS::Properties] ok 3 - $prop.inherit
  [CSS::Properties] ok 4 - $prop.synopsis
  [CSS::Properties] ok 5 - $prop.default
  [CSS::Properties] ok 6 - missing edges detected
  [CSS::Properties] ok 7 - $prop.name
  [CSS::Properties] ok 8 - $prop.box
  [CSS::Properties] ok 9 - $prop.inherit
  [CSS::Properties] ok 10 - $prop.synopsis
  [CSS::Properties] ok 11 - $prop.top.name
  [CSS::Properties] ok 12 - declared property
  [CSS::Properties] ok 13 - defaulted property
  [CSS::Properties] ok 14 - write
  [CSS::Properties] ok 15 - write
  [CSS::Properties] ok 16 - copy/write
  [CSS::Properties] ok 17 - 
  [CSS::Properties] ok 18 - 
  [CSS::Properties] ok 19 - 
  [CSS::Properties] ok 20 - 
  [CSS::Properties] ok 21 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/02-style-basic.t
  [CSS::Properties] 1..15
  [CSS::Properties] ok 1 - 
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - 
  [CSS::Properties] ok 7 - 
  [CSS::Properties] ok 8 - important property
  [CSS::Properties] ok 9 - unimportant property
  [CSS::Properties] ok 10 - 
  [CSS::Properties] ok 11 - 
  [CSS::Properties] ok 12 - 
  [CSS::Properties] ok 13 - 
  [CSS::Properties] ok 14 - 
  [CSS::Properties] ok 15 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/ast.t
  [CSS::Properties] 1..4
  [CSS::Properties] ok 1 - ast
  [CSS::Properties] ok 2 - style unoptimized
  [CSS::Properties] ok 3 - ast
  [CSS::Properties] ok 4 - style optimized
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/at-font-face.t
  [CSS::Properties] 1..30
  [CSS::Properties] ok 1 - 
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - 
  [CSS::Properties] ok 7 - 
  [CSS::Properties] ok 8 - 
  [CSS::Properties] ok 9 - 
  [CSS::Properties] ok 10 - 
  [CSS::Properties] ok 11 - 
  [CSS::Properties] ok 12 - 
  [CSS::Properties] ok 13 - 
  [CSS::Properties] ok 14 - 
  [CSS::Properties] ok 15 - 
  [CSS::Properties] ok 16 - 
  [CSS::Properties] ok 17 - 
  [CSS::Properties] ok 18 - 
  [CSS::Properties] ok 19 - 
  [CSS::Properties] ok 20 - 
  [CSS::Properties] ok 21 - 
  [CSS::Properties] ok 22 - 
  [CSS::Properties] ok 23 - 
  [CSS::Properties] ok 24 - 
  [CSS::Properties] ok 25 - 
  [CSS::Properties] ok 26 - 
  [CSS::Properties] ok 27 - 
  [CSS::Properties] ok 28 - 
  [CSS::Properties] ok 29 - 
  [CSS::Properties] ok 30 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/box-fonts.t
  [CSS::Properties] 1..5
  [CSS::Properties] # Subtest: basic
  [CSS::Properties]     1..9
  [CSS::Properties]     ok 1 - em
  [CSS::Properties]     ok 2 - ex
  [CSS::Properties]     ok 3 - font-style
  [CSS::Properties]     ok 4 - font-weight
  [CSS::Properties]     ok 5 - font-family
  [CSS::Properties]     ok 6 - line-height
  [CSS::Properties]     ok 7 - font-stretch
  [CSS::Properties]     ok 8 - measuring unit
  [CSS::Properties]     ok 9 - $font.Str
  [CSS::Properties] ok 1 - basic
  [CSS::Properties] # Subtest: measure
  [CSS::Properties]     1..9
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - measure numeric
  [CSS::Properties]     ok 5 - measure percentage font-size
  [CSS::Properties]     ok 6 - measure percentage font-size
  [CSS::Properties]     ok 7 - measure percentage font-size
  [CSS::Properties]     ok 8 - measure named font-size
  [CSS::Properties]     ok 9 - measure named font-size
  [CSS::Properties] ok 2 - measure
  [CSS::Properties] # Subtest: patterns
  [CSS::Properties]     1..3
  [CSS::Properties]     ok 1 - fontconfig-pattern
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - fontconfig-pattern
  [CSS::Properties] ok 3 - patterns
  [CSS::Properties] # Subtest: match basic
  [CSS::Properties]     1..2
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties] ok 4 - match basic
  [CSS::Properties] # Subtest: match styles
  [CSS::Properties]     1..6
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     ok 6 - 
  [CSS::Properties] ok 5 - match styles
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/box-measure.t
  [CSS::Properties] 1..19
  [CSS::Properties] ok 1 - default units
  [CSS::Properties] ok 2 - .Array
  [CSS::Properties] ok 3 - .padding
  [CSS::Properties] ok 4 - .border
  [CSS::Properties] ok 5 - .margin
  [CSS::Properties] ok 6 - .width
  [CSS::Properties] ok 7 - .height
  [CSS::Properties] ok 8 - .width("padding")
  [CSS::Properties] ok 9 - .height("padding")
  [CSS::Properties] ok 10 - .padding-XXX
  [CSS::Properties] ok 11 - .border-XXX
  [CSS::Properties] ok 12 - .margin-XXX
  [CSS::Properties] ok 13 - .border-width
  [CSS::Properties] ok 14 - .border-height
  [CSS::Properties] ok 15 - 
  [CSS::Properties] ok 16 - changed units
  [CSS::Properties] ok 17 - .Array
  [CSS::Properties] ok 18 - .padding
  [CSS::Properties] ok 19 - adjusted .margin
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/box.t
  [CSS::Properties] 1..20
  [CSS::Properties] ok 1 - .Array
  [CSS::Properties] ok 2 - .padding
  [CSS::Properties] ok 3 - .border
  [CSS::Properties] ok 4 - .margin
  [CSS::Properties] ok 5 - .width
  [CSS::Properties] ok 6 - .height
  [CSS::Properties] ok 7 - .width("padding")
  [CSS::Properties] ok 8 - .height("padding")
  [CSS::Properties] ok 9 - .padding-XXX
  [CSS::Properties] ok 10 - .border-XXX
  [CSS::Properties] ok 11 - .margin-XXX
  [CSS::Properties] ok 12 - .border-width
  [CSS::Properties] ok 13 - .border-height
  [CSS::Properties] ok 14 - .translate
  [CSS::Properties] ok 15 - translate padding
  [CSS::Properties] ok 16 - .move
  [CSS::Properties] ok 17 - move padding
  [CSS::Properties] ok 18 - .resize
  [CSS::Properties] ok 19 - illegal initial size
  [CSS::Properties] not ok 20 - illegal resize # TODO reimplement resize checks
  [CSS::Properties] # Failed test 'illegal resize'
  [CSS::Properties] # at t/box.t line 52
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/calc.t
  [CSS::Properties] 1..4
  [CSS::Properties] # Subtest: font-size
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     1..3
  [CSS::Properties] ok 1 - font-size
  [CSS::Properties] # Subtest: basic arithmetic
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     1..4
  [CSS::Properties] ok 2 - basic arithmetic
  [CSS::Properties] # Subtest: associativety/precedence
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     ok 7 - 
  [CSS::Properties]     1..7
  [CSS::Properties] ok 3 - associativety/precedence
  [CSS::Properties] # Subtest: div/minus
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     1..4
  [CSS::Properties] ok 4 - div/minus
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/colors.t
  [CSS::Properties] 1..33
  [CSS::Properties] ok 1 - :values constructor
  [CSS::Properties] ok 2 - :values constructor
  [CSS::Properties] ok 3 - serialization
  [CSS::Properties] ok 4 - :values constructor
  [CSS::Properties] ok 5 - :values constructor
  [CSS::Properties] ok 6 - :values constructor
  [CSS::Properties] ok 7 - serialization
  [CSS::Properties] ok 8 - :values constructor
  [CSS::Properties] ok 9 - :values constructor
  [CSS::Properties] ok 10 - :values constructor
  [CSS::Properties] ok 11 - :values constructor
  [CSS::Properties] ok 12 - serialization
  [CSS::Properties] ok 13 - :values constructor
  [CSS::Properties] ok 14 - :values constructor
  [CSS::Properties] ok 15 - :values constructor
  [CSS::Properties] ok 16 - serialization
  [CSS::Properties] ok 17 - :values constructor
  [CSS::Properties] ok 18 - :values constructor
  [CSS::Properties] ok 19 - :values constructor
  [CSS::Properties] ok 20 - serialization
  [CSS::Properties] ok 21 - :values constructor
  [CSS::Properties] ok 22 - :values constructor
  [CSS::Properties] ok 23 - :values constructor
  [CSS::Properties] ok 24 - serialization
  [CSS::Properties] ok 25 - :values constructor
  [CSS::Properties] ok 26 - :values constructor
  [CSS::Properties] ok 27 - :values constructor
  [CSS::Properties] ok 28 - serialization
  [CSS::Properties] ok 29 - border-*-color default
  [CSS::Properties] ok 30 - border-*-color default
  [CSS::Properties] ok 31 - border-*-color default
  [CSS::Properties] ok 32 - color assignment
  [CSS::Properties] ok 33 - color assigment
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/css-fonts.t
  [CSS::Properties] 1..4
  [CSS::Properties] # Subtest: props
  [CSS::Properties]     ok 1 - font-style
  [CSS::Properties]     ok 2 - font-weight
  [CSS::Properties]     ok 3 - font-family
  [CSS::Properties]     ok 4 - font-size
  [CSS::Properties]     ok 5 - line-height
  [CSS::Properties]     1..5
  [CSS::Properties] ok 1 - props
  [CSS::Properties] # Subtest: serialization
  [CSS::Properties]     1..33
  [CSS::Properties]     ok 1 - serialization
  [CSS::Properties]     ok 2 - (empty)
  [CSS::Properties]     ok 3 - font-family
  [CSS::Properties]     ok 4 - line-height
  [CSS::Properties]     ok 5 - font-family line-height
  [CSS::Properties]     ok 6 - font-size
  [CSS::Properties]     ok 7 - font-family font-size
  [CSS::Properties]     ok 8 - font-size line-height
  [CSS::Properties]     ok 9 - font-family font-size line-height
  [CSS::Properties]     ok 10 - font-weight
  [CSS::Properties]     ok 11 - font-family font-weight
  [CSS::Properties]     ok 12 - font-weight line-height
  [CSS::Properties]     ok 13 - font-family font-weight line-height
  [CSS::Properties]     ok 14 - font-size font-weight
  [CSS::Properties]     ok 15 - font-family font-size font-weight
  [CSS::Properties]     ok 16 - font-size font-weight line-height
  [CSS::Properties]     ok 17 - font-family font-size font-weight line-height
  [CSS::Properties]     ok 18 - font-style
  [CSS::Properties]     ok 19 - font-family font-style
  [CSS::Properties]     ok 20 - font-style line-height
  [CSS::Properties]     ok 21 - font-family font-style line-height
  [CSS::Properties]     ok 22 - font-size font-style
  [CSS::Properties]     ok 23 - font-family font-size font-style
  [CSS::Properties]     ok 24 - font-size font-style line-height
  [CSS::Properties]     ok 25 - font-family font-size font-style line-height
  [CSS::Properties]     ok 26 - font-style font-weight
  [CSS::Properties]     ok 27 - font-family font-style font-weight
  [CSS::Properties]     ok 28 - font-style font-weight line-height
  [CSS::Properties]     ok 29 - font-family font-style font-weight line-height
  [CSS::Properties]     ok 30 - font-size font-style font-weight
  [CSS::Properties]     ok 31 - font-family font-size font-style font-weight
  [CSS::Properties]     ok 32 - font-size font-style font-weight line-height
  [CSS::Properties]     ok 33 - font-family font-size font-style font-weight line-height
  [CSS::Properties] ok 2 - serialization
  [CSS::Properties] # Subtest: issue#23
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     1..1
  [CSS::Properties] ok 3 - issue \#23
  [CSS::Properties] # Subtest: change em
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     1..2
  [CSS::Properties] ok 4 - change em
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/declarations.t
  [CSS::Properties] 1..47
  [CSS::Properties] ok 1 - :values constructor
  [CSS::Properties] ok 2 - box property
  [CSS::Properties] ok 3 - edges property
  [CSS::Properties] ok 4 - simple property
  [CSS::Properties] ok 5 - margin-left is a margin edge
  [CSS::Properties] ok 6 - default azimuth
  [CSS::Properties] ok 7 - default azimuth
  [CSS::Properties] ok 8 - default margin
  [CSS::Properties] ok 9 - default margin-left
  [CSS::Properties] ok 10 - default margin left type
  [CSS::Properties] ok 11 - default background-color
  [CSS::Properties] ok 12 - default background-color
  [CSS::Properties] ok 13 - basic css rewritten
  [CSS::Properties] ok 14 - default background position
  [CSS::Properties] ok 15 - list parse
  [CSS::Properties] ok 16 - list parse
  [CSS::Properties] ok 17 - list parse
  [CSS::Properties] ok 18 - background-color reset
  [CSS::Properties] ok 19 - background-color reset
  [CSS::Properties] ok 20 - updated margin-right value
  [CSS::Properties] ok 21 - updated margin-right units
  [CSS::Properties] ok 22 - updated margin-right units
  [CSS::Properties] ok 23 - updated margin
  [CSS::Properties] ok 24 - measured margin
  [CSS::Properties] ok 25 - reset margin
  [CSS::Properties] ok 26 - reset margin-left
  [CSS::Properties] ok 27 - named and rgb colors
  [CSS::Properties] ok 28 - 
  [CSS::Properties] ok 29 - border-color string coercement
  [CSS::Properties] ok 30 - border-color reset
  [CSS::Properties] ok 31 - struct str assignment
  [CSS::Properties] ok 32 - border top
  [CSS::Properties] ok 33 - border top width
  [CSS::Properties] ok 34 - border top width
  [CSS::Properties] ok 35 - border top color
  [CSS::Properties] ok 36 - border top color
  [CSS::Properties] ok 37 - struct hash assignment
  [CSS::Properties] ok 38 - border top width
  [CSS::Properties] ok 39 - border top color
  [CSS::Properties] ok 40 - border top color
  [CSS::Properties] ok 41 - border top color
  [CSS::Properties] ok 42 - reset border top width
  [CSS::Properties] ok 43 - reset border top color
  [CSS::Properties] ok 44 - info on a container property
  [CSS::Properties] ok 45 - default text-align
  [CSS::Properties] ok 46 - default text-align (direction rtl)
  [CSS::Properties] ok 47 - updated text-direction
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/errors.t
  [CSS::Properties] 1..6
  [CSS::Properties] ok 1 - 
  [CSS::Properties] unable to parse CSS3 property 'width: 2furlongs;'
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] unable to parse CSS3 property 'width: foo(42);'
  [CSS::Properties] ok 5 - 
  [CSS::Properties] expected type of length, got number: calc(42)
  [CSS::Properties] ok 6 - 
  [CSS::Properties] unable to evaluate expression: calc(2em + 3hz)
  [CSS::Properties] skipping: 'foo'
  [CSS::Properties] usage: calc( <calc-sum> )
  [CSS::Properties] unable to evaluate expression: calc('foo')
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/extend.t
  [CSS::Properties] 1..22
  [CSS::Properties] ok 1 - info.name
  [CSS::Properties] ok 2 - info.synopsis
  [CSS::Properties] ok 3 - info.default
  [CSS::Properties] ok 4 - info.name
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - info.default
  [CSS::Properties] ok 7 - coercer called
  [CSS::Properties] ok 8 - 
  [CSS::Properties] ok 9 - The object is-a 'Int'
  [CSS::Properties] ok 10 - property set
  [CSS::Properties] ok 11 - coercer called
  [CSS::Properties] ok 12 - property get
  [CSS::Properties] ok 13 - properties
  [CSS::Properties] ok 14 - serialization
  [CSS::Properties] ok 15 - serialization (default)
  [CSS::Properties] ok 16 - reserialization
  [CSS::Properties] ok 17 - 
  [CSS::Properties] ok 18 - 
  [CSS::Properties] ok 19 - case insensitivity
  [CSS::Properties] # Subtest: parse
  [CSS::Properties]     ok 1 - coercer called
  [CSS::Properties]     ok 2 - coercer called
  [CSS::Properties]     ok 3 - serialization
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - The object is-a 'Int'
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     1..6
  [CSS::Properties] ok 20 - parse
  [CSS::Properties] # Subtest: invalid
  [CSS::Properties]     ok 1 - serialization
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - The object is-a 'Int'
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     1..4
  [CSS::Properties] ok 21 - invalid
  [CSS::Properties] # Subtest: any
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     1..5
  [CSS::Properties] ok 22 - any
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/important.t
  [CSS::Properties] 1..14
  [CSS::Properties] ok 1 - 
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - importance setter
  [CSS::Properties] ok 7 - importance setter - box
  [CSS::Properties] ok 8 - importance setter - box
  [CSS::Properties] ok 9 - 
  [CSS::Properties] ok 10 - 
  [CSS::Properties] ok 11 - 
  [CSS::Properties] ok 12 - 
  [CSS::Properties] ok 13 - 
  [CSS::Properties] ok 14 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/inherit.t
  [CSS::Properties] 1..23
  [CSS::Properties] Type check failed for return value; expected Seq but got List (("color",))
  [CSS::Properties]   in method inherited at /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10/lib/CSS/Properties.rakumod (CSS::Properties) line 443
  [CSS::Properties]   in block <unit> at t/inherit.t line 8
  [CSS::Properties] # You planned 23 tests, but ran 0
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/measure.t
  [CSS::Properties] 1..34
  [CSS::Properties] ok 1 - $css.measure($.viewport-width)
  [CSS::Properties] ok 2 - $css.measure($.viewport-height)
  [CSS::Properties] ok 3 - default units
  [CSS::Properties] ok 4 - $css.measure(pt)
  [CSS::Properties] ok 5 - $css.measure(px)
  [CSS::Properties] ok 6 - $css.measure(pc)
  [CSS::Properties] ok 7 - $css.measure(em)
  [CSS::Properties] ok 8 - $css.measure(ex)
  [CSS::Properties] ok 9 - $css.measure(vw)
  [CSS::Properties] ok 10 - $css.measure(vh)
  [CSS::Properties] ok 11 - $css.measure("thin")
  [CSS::Properties] ok 12 - $css.measure("medium")
  [CSS::Properties] ok 13 - $css.measure(:font-size<medium>)
  [CSS::Properties] ok 14 - $css.measure("thick")
  [CSS::Properties] ok 15 - $css.measure("x-large")
  [CSS::Properties] ok 16 - $css.measure("smaller")
  [CSS::Properties] # Subtest: font-size
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     ok 7 - 
  [CSS::Properties]     ok 8 - 
  [CSS::Properties]     ok 9 - 
  [CSS::Properties]     ok 10 - 
  [CSS::Properties]     ok 11 - 
  [CSS::Properties]     ok 12 - 
  [CSS::Properties]     ok 13 - 
  [CSS::Properties]     ok 14 - 
  [CSS::Properties]     1..14
  [CSS::Properties] ok 17 - font-size
  [CSS::Properties] # Subtest: font-weight
  [CSS::Properties]     ok 1 - 
  [CSS::Properties]     ok 2 - 
  [CSS::Properties]     ok 3 - 
  [CSS::Properties]     ok 4 - 
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     ok 7 - 
  [CSS::Properties]     ok 8 - 
  [CSS::Properties]     ok 9 - 
  [CSS::Properties]     ok 10 - 
  [CSS::Properties]     ok 11 - 
  [CSS::Properties]     ok 12 - 
  [CSS::Properties]     ok 13 - 
  [CSS::Properties]     1..13
  [CSS::Properties] ok 18 - font-weight
  [CSS::Properties] ok 19 - 
  [CSS::Properties] ok 20 - 
  [CSS::Properties] ok 21 - 
  [CSS::Properties] ok 22 - changed units
  [CSS::Properties] ok 23 - $css.measure(in)
  [CSS::Properties] ok 24 - $css.measure(in)
  [CSS::Properties] ok 25 - $css.measure(in)
  [CSS::Properties] ok 26 - 
  [CSS::Properties] ok 27 - 
  [CSS::Properties] ok 28 - 
  [CSS::Properties] ok 29 - 
  [CSS::Properties] ok 30 - 
  [CSS::Properties] ok 31 - 
  [CSS::Properties] ok 32 - 
  [CSS::Properties] # Subtest: simple background-position
  [CSS::Properties]     ok 1 - measure background-position
  [CSS::Properties]     ok 2 - measure background-position: 10% 20%
  [CSS::Properties]     ok 3 - measure background-position: center 100%
  [CSS::Properties]     ok 4 - measure background-position: 10pt 20pt
  [CSS::Properties]     1..4
  [CSS::Properties] ok 33 - simple background-position
  [CSS::Properties] ok 34 - # SKIP multi-layer background-position
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/modules.t
  [CSS::Properties] 1..5
  [CSS::Properties] ok 1 - azimuth is unknown in CSS1
  [CSS::Properties] ok 2 - azimuth is known in CSS21
  [CSS::Properties] ok 3 - azimuth is known in CSS3
  [CSS::Properties] dropping unknown @fontface property azimuth
  [CSS::Properties] ok 4 - src is known in @font-face
  [CSS::Properties] ok 5 - azimuth is unknown in @font-face
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/optimize.t
  [CSS::Properties] 1..16
  [CSS::Properties] ok 1 - optimised ast border:1px solid red;
  [CSS::Properties] ok 2 - optimised via CSS::Properties border:1px solid red;
  [CSS::Properties] ok 3 - optimised ast border-width:5pt 5px 5in 5mm;
  [CSS::Properties] ok 4 - optimised via CSS::Properties border-width:5pt 5px 5in 5mm;
  [CSS::Properties] ok 5 - optimised ast border-top:5px!important;
  [CSS::Properties] ok 6 - optimised via CSS::Properties border-top:5px!important;
  [CSS::Properties] ok 7 - optimised ast border:5pt solid; border-color:red green blue yellow;
  [CSS::Properties] ok 8 - optimised via CSS::Properties border:5pt solid; border-color:red green blue yellow;
  [CSS::Properties] ok 9 - optimised ast font-family:times; font-size:inherit; font-weight:inherit;
  [CSS::Properties] ok 10 - optimised via CSS::Properties font-family:times; font-size:inherit; font-weight:inherit;
  [CSS::Properties] ok 11 - optimised ast background:no-repeat 50% 75%;
  [CSS::Properties] ok 12 - optimised via CSS::Properties background:no-repeat 50% 75%; # TODO CSS Properties backgrounds
  [CSS::Properties] ok 13 - optimised ast font:1.1em/1.3 Verdana, Arial, sans-serif;
  [CSS::Properties] ok 14 - optimised via CSS::Properties font:1.1em/1.3 Verdana, Arial, sans-serif;
  [CSS::Properties] ok 15 - optimised ast list-style:circle;
  [CSS::Properties] ok 16 - optimised via CSS::Properties list-style:circle;
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/page-box.t
  [CSS::Properties] 1..19
  [CSS::Properties] ok 1 - 
  [CSS::Properties] ok 2 - .Array
  [CSS::Properties] ok 3 - .Array
  [CSS::Properties] ok 4 - css
  [CSS::Properties] ok 5 - .margin (mm)
  [CSS::Properties] ok 6 - .margin (pt)
  [CSS::Properties] ok 7 - .border
  [CSS::Properties] ok 8 - .padding
  [CSS::Properties] ok 9 - .content
  [CSS::Properties] ok 10 - .margin auto
  [CSS::Properties] ok 11 - .border auto
  [CSS::Properties] ok 12 - .padding auto
  [CSS::Properties] ok 13 - .content auto
  [CSS::Properties] ok 14 - .margin auto
  [CSS::Properties] ok 15 - .border auto
  [CSS::Properties] ok 16 - .padding auto
  [CSS::Properties] ok 17 - .content auto (mm)
  [CSS::Properties] ok 18 - .content auto (pt)
  [CSS::Properties] ok 19 - auto/min/max
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/svg-properties.t
  [CSS::Properties] ok 1 - alignment-baseline:after-edge;
  [CSS::Properties] ok 2 - baseline-shift:super;
  [CSS::Properties] ok 3 - baseline-shift:1.5em;
  [CSS::Properties] ok 4 - baseline-shift:1.5em; - type
  [CSS::Properties] ok 5 - baseline-shift:4%;
  [CSS::Properties] ok 6 - baseline-shift:4%; - type
  [CSS::Properties] ok 7 - color:red;
  [CSS::Properties] ok 8 - color:rgb(10%,20,30);
  [CSS::Properties] ok 9 - color:rgb(10%,20,30); - type
  [CSS::Properties] ok 10 - color-interpolation:sRGB;
  [CSS::Properties] ok 11 - color-interpolation:Srgb;
  [CSS::Properties] ok 12 - color-interpolation:lInearRgB;
  [CSS::Properties] ok 13 - color-rendering:optimizeSpeed;
  [CSS::Properties] ok 14 - direction:ltr;
  [CSS::Properties] ok 15 - direction:rtl;
  [CSS::Properties] ok 16 - display:table-cell;
  [CSS::Properties] ok 17 - dominant-baseline:hanging;
  [CSS::Properties] ok 18 - fill:rgb(10,20,10%);
  [CSS::Properties] ok 19 - fill-opacity:0.75;
  [CSS::Properties] ok 20 - fill-opacity:75%;
  [CSS::Properties] ok 21 - fill-rule:evenOdD;
  [CSS::Properties] ok 22 - font-variant:small-Caps;
  [CSS::Properties] ok 23 - glyph-orientation-vertical:45deg;
  [CSS::Properties] ok 24 - glyph-orientation-vertical:7;
  [CSS::Properties] ok 25 - image-rendering:optimizeQuality;
  [CSS::Properties] ok 26 - line-height:90%;
  [CSS::Properties] ok 27 - line-height:normal;
  [CSS::Properties] ok 28 - line-height:42;
  [CSS::Properties] ok 29 - marker-start:none;
  [CSS::Properties] ok 30 - marker-start:url('http://www.example.com/pinkish.gif');
  [CSS::Properties] ok 31 - marker-mid:none;
  [CSS::Properties] ok 32 - marker-end:none;
  [CSS::Properties] ok 33 - marker:url('http://www.example.com/greenish.gif') url('http://www.example.com/pinkish.gif');
  [CSS::Properties] ok 34 - opacity:0.75;
  [CSS::Properties] ok 35 - opacity:75%;
  [CSS::Properties] ok 36 - overflow:hidden;
  [CSS::Properties] ok 37 - paint-order:fill stroke;
  [CSS::Properties] ok 38 - shape-rendering:crispEdges;
  [CSS::Properties] ok 39 - stop-opacity:0.75;
  [CSS::Properties] ok 40 - stop-opacity:75%;
  [CSS::Properties] ok 41 - stroke:none;
  [CSS::Properties] ok 42 - stroke:black;
  [CSS::Properties] ok 43 - stroke-dasharray:20, 10;
  [CSS::Properties] ok 44 - stroke-dasharray:em, 2em;
  [CSS::Properties] ok 45 - stroke-dashoffset:3em;
  [CSS::Properties] ok 46 - stroke-linecap:round;
  [CSS::Properties] ok 47 - stroke-linejoin:bevel;
  [CSS::Properties] ok 48 - stroke-opacity:0.75;
  [CSS::Properties] ok 49 - stroke-opacity:75%;
  [CSS::Properties] ok 50 - stroke-width:0.1em;
  [CSS::Properties] ok 51 - stroke-width:2.5;
  [CSS::Properties] ok 52 - stroke-miterlimit:5;
  [CSS::Properties] ok 53 - text-anchor:middle;
  [CSS::Properties] ok 54 - text-decoration:underline blink;
  [CSS::Properties] ok 55 - text-rendering:geometricPrecision;
  [CSS::Properties] ok 56 - visibility:hidden;
  [CSS::Properties] ok 57 - white-space:pre;
  [CSS::Properties] ok 58 - writing-mode:rl-tb;
  [CSS::Properties] 1..58
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/threads.t
  [CSS::Properties] 1..4
  [CSS::Properties] ok 1 - basic
  [CSS::Properties] ok 2 - info
  [CSS::Properties] ok 3 - no property name errors
  [CSS::Properties] ok 4 - mixed modules
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/units.t
  [CSS::Properties] ok 1 - pt + pt
  [CSS::Properties] ok 2 - pt + pt
  [CSS::Properties] ok 3 - gist
  [CSS::Properties] ok 4 - pt += pt
  [CSS::Properties] ok 5 - pt += pt
  [CSS::Properties] ok 6 - pt + mm
  [CSS::Properties] ok 7 - pt + mm
  [CSS::Properties] ok 8 - pt + mm
  [CSS::Properties] ok 9 - pt - in
  [CSS::Properties] ok 10 - pt + in
  [CSS::Properties] ok 11 - pt +css in
  [CSS::Properties] ok 12 - pt + px
  [CSS::Properties] ok 13 - pt + pc
  [CSS::Properties] ok 14 - pt - pc
  [CSS::Properties] ok 15 - pt -css pc
  [CSS::Properties] ok 16 - ms to s
  [CSS::Properties] ok 17 - hz to khz
  [CSS::Properties] ok 18 - turn to deg
  [CSS::Properties] ok 19 - turn to rad
  [CSS::Properties] ok 20 - px to pt
  [CSS::Properties] ok 21 - dpi to dpcm
  [CSS::Properties] ok 22 - dppx to dpi
  [CSS::Properties] 1..22
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/vivify.t
  [CSS::Properties] 1..6
  [CSS::Properties] ok 1 - vivifed-name
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/59b8ade5cbce66afbec75dc6ef92da9de3d7f1f0.tar.gz/CSS-Properties-0.10.10 t/write.t
  [CSS::Properties] 1..25
  [CSS::Properties] ok 1 - unoptimized edge property
  [CSS::Properties] ok 2 - edge property
  [CSS::Properties] ok 3 - consolidation of edge properties
  [CSS::Properties] ok 4 - consolidation of edge properties
  [CSS::Properties] ok 5 - optimized properties
  [CSS::Properties] ok 6 - edge unoptimized
  [CSS::Properties] ok 7 - edge optimized
  [CSS::Properties] ok 8 - compound edge
  [CSS::Properties] ok 9 - compound edge - unoptimized
  [CSS::Properties] ok 10 - compound edge - re-optimized
  [CSS::Properties] ok 11 - compound edge - partial optimization
  [CSS::Properties] ok 12 - optimization of default values
  [CSS::Properties] ok 13 - 
  [CSS::Properties] ok 14 - 
  [CSS::Properties] ok 15 - 
  [CSS::Properties] ok 16 - 
  [CSS::Properties] ok 17 - 
  [CSS::Properties] ok 18 - 
  [CSS::Properties] ok 19 - 
  [CSS::Properties] ok 20 - 
  [CSS::Properties] ok 21 - 
  [CSS::Properties] ok 22 - 
  [CSS::Properties] ok 23 - 
  [CSS::Properties] ok 24 - 
  [CSS::Properties] ok 25 - 
  ===> Testing [FAIL]: CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10>
  [CSS::Properties] Failed to get passing tests, but continuing with --force-test
  ===> Installing: CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10>
  ===> Install [OK] for CSS::Properties:ver<0.10.10>:auth<zef:dwarring>:api<0.10>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 22.049s
               CPU time consumed: 1min 59.501s
                     Memory peak: 2.1G (swap: 0B)

  ```
  </details>
* [ ] [Commands](https://raku.land/zef:lizmat/Commands) – Fail, Bisected: [afee7d8](https://github.com/rakudo/rakudo/commit/afee7d8d3197b7a093355d98a90f6f86d8bda32a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1405990-i1314487.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Commands
  ===> Found: Commands:ver<0.0.9>:auth<zef:lizmat> [via Zef::Repository::Ecosystems<fez>]
  [Commands] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549421.1405991.6257.687257759389/c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz https://360.zef.pm/C/OM/COMMANDS/c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz
  ===> Fetching [OK]: Commands:ver<0.0.9>:auth<zef:lizmat> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549421.1405991.6257.687257759389/c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz
  [Commands] Command: tar -t -f ./c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz
  [Commands] Command: tar -xvf ./c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz -C ../c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz
  ===> Extraction [OK]: Commands to /home/coke/sandbox/blin/data/zef-data/tmp/c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz
  ===> Testing: Commands:ver<0.0.9>:auth<zef:lizmat>
  [Commands] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz/Commands-0.0.9 t/01-basic.rakutest
  [Commands] 1..38
  [Commands] ok 1 - check primaries
  [Commands] ok 2 - check aliases
  [Commands] # Subtest: command: ''
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 3 - command: ''
  [Commands] # Subtest: command: 'quit foo'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 4 - command: 'quit foo'
  [Commands] # Subtest: command: 'quit'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 5 - command: 'quit'
  [Commands] # Subtest: command: 'qui'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 6 - command: 'qui'
  [Commands] # Subtest: command: 'qu'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 7 - command: 'qu'
  [Commands] # Subtest: command: 'q'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 8 - command: 'q'
  [Commands] # Subtest: command: 'exit foo'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 9 - command: 'exit foo'
  [Commands] # Subtest: command: 'exit'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 10 - command: 'exit'
  [Commands] # Subtest: command: 'exi'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 11 - command: 'exi'
  [Commands] # Subtest: command: 'ex'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 12 - command: 'ex'
  [Commands] # Subtest: command: 'e'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 13 - command: 'e'
  [Commands] # Subtest: command: 'release   all'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 14 - command: 'release   all'
  [Commands] # Subtest: command: 'r  all'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 15 - command: 'r  all'
  [Commands] # Subtest: command: 'release   42'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 16 - command: 'release   42'
  [Commands] # Subtest: command: 'rel  42'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 17 - command: 'rel  42'
  [Commands] # Subtest: command: 'red'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 18 - command: 'red'
  [Commands] # Subtest: command: 'shout hello  there'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 19 - command: 'shout hello  there'
  [Commands] # Subtest: command: 's     hello  there'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 20 - command: 's     hello  there'
  [Commands] # Subtest: command: 'bt'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 21 - command: 'bt'
  [Commands] # Subtest: command: 'help'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 22 - command: 'help'
  [Commands] # Subtest: command: 'help q'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 23 - command: 'help q'
  [Commands] # Subtest: command: 'help exit'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 24 - command: 'help exit'
  [Commands] # Subtest: command: 'help shout'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 25 - command: 'help shout'
  [Commands] # Subtest: command: 'help foo bar'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 26 - command: 'help foo bar'
  [Commands] # Subtest: command: '  foo  '
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 27 - command: '  foo  '
  [Commands] # Subtest: command: 'my $a = 666'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 28 - command: 'my $a = 666'
  [Commands] # Subtest: command: 'my $a = 666 ; $a'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 29 - command: 'my $a = 666 ; $a'
  [Commands] # Subtest: command: 'b'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 30 - command: 'b'
  [Commands] # Subtest: command: 'r  foo  bar'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 31 - command: 'r  foo  bar'
  [Commands] ok 32 - 's' resolved to 'shout'
  [Commands] ok 33 - 'sh' resolved to 'shout'
  [Commands] ok 34 - 'sho' resolved to 'shout'
  [Commands] ok 35 - 'shou' resolved to 'shout'
  [Commands] ok 36 - 'shout' resolved to 'shout'
  [Commands] ok 37 - 're' did not resolve as it is ambiguous
  [Commands] ok 38 - 'xxx' did not resolve as it is unknown
  ===> Testing [OK] for Commands:ver<0.0.9>:auth<zef:lizmat>
  ===> Installing: Commands:ver<0.0.9>:auth<zef:lizmat>
  ===> Install [OK] for Commands:ver<0.0.9>:auth<zef:lizmat>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 39.935s
               CPU time consumed: 56.981s
                     Memory peak: 1010.4M (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1404963-i1466794.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Commands
  ===> Found: Commands:ver<0.0.9>:auth<zef:lizmat> [via Zef::Repository::Ecosystems<fez>]
  [Commands] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549378.1404969.1.4838552223006563/c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz https://360.zef.pm/C/OM/COMMANDS/c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz
  ===> Fetching [OK]: Commands:ver<0.0.9>:auth<zef:lizmat> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549378.1404969.1.4838552223006563/c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz
  [Commands] Command: tar -t -f ./c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz
  [Commands] Command: tar -xvf ./c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz -C ../c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz
  ===> Extraction [OK]: Commands to /home/coke/sandbox/blin/data/zef-data/tmp/c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz
  ===> Testing: Commands:ver<0.0.9>:auth<zef:lizmat>
  [Commands] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/c9ace000d285202c1fd51c86eb457ebbe5f1f70e.tar.gz/Commands-0.0.9 t/01-basic.rakutest
  [Commands] 1..38
  [Commands] not ok 1 - check primaries
  [Commands] # Failed test 'check primaries'
  [Commands] # at t/01-basic.rakutest line 65
  [Commands] # expected: $("bt", "exit", "help", "quit", "red", "release", "release all", "shout")
  [Commands] #      got: $["bt", "exit", "help", "quit", "red", "release", "release all", "shout"]
  [Commands] ok 2 - check aliases
  [Commands] # Subtest: command: ''
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 3 - command: ''
  [Commands] # Subtest: command: 'quit foo'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 4 - command: 'quit foo'
  [Commands] # Subtest: command: 'quit'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 5 - command: 'quit'
  [Commands] # Subtest: command: 'qui'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 6 - command: 'qui'
  [Commands] # Subtest: command: 'qu'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 7 - command: 'qu'
  [Commands] # Subtest: command: 'q'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 8 - command: 'q'
  [Commands] # Subtest: command: 'exit foo'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 9 - command: 'exit foo'
  [Commands] # Subtest: command: 'exit'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 10 - command: 'exit'
  [Commands] # Subtest: command: 'exi'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 11 - command: 'exi'
  [Commands] # Subtest: command: 'ex'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 12 - command: 'ex'
  [Commands] # Subtest: command: 'e'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 13 - command: 'e'
  [Commands] # Subtest: command: 'release   all'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 14 - command: 'release   all'
  [Commands] # Subtest: command: 'r  all'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 15 - command: 'r  all'
  [Commands] # Subtest: command: 'release   42'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 16 - command: 'release   42'
  [Commands] # Subtest: command: 'rel  42'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 17 - command: 'rel  42'
  [Commands] # Subtest: command: 'red'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 18 - command: 'red'
  [Commands] # Subtest: command: 'shout hello  there'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 19 - command: 'shout hello  there'
  [Commands] # Subtest: command: 's     hello  there'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 20 - command: 's     hello  there'
  [Commands] # Subtest: command: 'bt'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 21 - command: 'bt'
  [Commands] # Subtest: command: 'help'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 22 - command: 'help'
  [Commands] # Subtest: command: 'help q'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 23 - command: 'help q'
  [Commands] # Subtest: command: 'help exit'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 24 - command: 'help exit'
  [Commands] # Subtest: command: 'help shout'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 25 - command: 'help shout'
  [Commands] # Subtest: command: 'help foo bar'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 26 - command: 'help foo bar'
  [Commands] # Subtest: command: '  foo  '
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 27 - command: '  foo  '
  [Commands] # Subtest: command: 'my $a = 666'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 28 - command: 'my $a = 666'
  [Commands] # Subtest: command: 'my $a = 666 ; $a'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 29 - command: 'my $a = 666 ; $a'
  [Commands] # Subtest: command: 'b'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 30 - command: 'b'
  [Commands] # Subtest: command: 'r  foo  bar'
  [Commands]     1..3
  [Commands]     ok 1 - out
  [Commands]     ok 2 - err
  [Commands]     ok 3 - sys
  [Commands] ok 31 - command: 'r  foo  bar'
  [Commands] ok 32 - 's' resolved to 'shout'
  [Commands] ok 33 - 'sh' resolved to 'shout'
  [Commands] ok 34 - 'sho' resolved to 'shout'
  [Commands] ok 35 - 'shou' resolved to 'shout'
  [Commands] ok 36 - 'shout' resolved to 'shout'
  [Commands] ok 37 - 're' did not resolve as it is ambiguous
  [Commands] ok 38 - 'xxx' did not resolve as it is unknown
  [Commands] # You failed 1 test of 38
  ===> Testing [FAIL]: Commands:ver<0.0.9>:auth<zef:lizmat>
  [Commands] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Commands:ver<0.0.9>:auth<zef:lizmat>
  ===> Install [OK] for Commands:ver<0.0.9>:auth<zef:lizmat>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 29.741s
               CPU time consumed: 13.130s
                     Memory peak: 936.4M (swap: 0B)

  ```
  </details>
* [ ] [Cro::HTTP](https://raku.land/zef:cro/Cro::HTTP) – Fail, Bisected: [afee7d8](https://github.com/rakudo/rakudo/commit/afee7d8d3197b7a093355d98a90f6f86d8bda32a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1413163-i1374480.service; invocation ID: b78429a9529e4d65b3a56d913d29545d
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Cro::HTTP
  ===> Found: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0> [via Zef::Repository::Ecosystems<fez>]
  [Cro::HTTP] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549634.1413164.7011.082490384439/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz https://360.zef.pm/C/RO/CRO_HTTP/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Fetching [OK]: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549634.1413164.7011.082490384439/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  [Cro::HTTP] Command: tar -t -f ./3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  [Cro::HTTP] Command: tar -xvf ./3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz -C ../3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Extraction [OK]: Cro::HTTP to /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Testing: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0>
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-basic-with-session.rakutest
  [Cro::HTTP] ok 1 - Username is set after basic authentication
  [Cro::HTTP] # Subtest: 401 when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6174479822656) ... }
  [Cro::HTTP] ok 2 - 401 when wrong credentials are passed
  [Cro::HTTP] # Subtest: WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6174479823088) ... }
  [Cro::HTTP] ok 3 - WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP] # Subtest: Request without credentials returns 401
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6174479823160) ... }
  [Cro::HTTP] ok 4 - Request without credentials returns 401
  [Cro::HTTP] # Subtest: Request without credentials has WWW-Authenticate header
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6174479823232) ... }
  [Cro::HTTP] ok 5 - Request without credentials has WWW-Authenticate header
  [Cro::HTTP] 1..5
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-basic.rakutest
  [Cro::HTTP] ok 1 - Username is set after basic authentication
  [Cro::HTTP] # Subtest: 401 when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|5606172436968) ... }
  [Cro::HTTP] ok 2 - 401 when wrong credentials are passed
  [Cro::HTTP] # Subtest: WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|5606172437400) ... }
  [Cro::HTTP] ok 3 - WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP] # Subtest: Request without credentials returns 401
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|5606172437472) ... }
  [Cro::HTTP] ok 4 - Request without credentials returns 401
  [Cro::HTTP] # Subtest: Request without credentials has WWW-Authenticate header
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|5606172437544) ... }
  [Cro::HTTP] ok 5 - Request without credentials has WWW-Authenticate header
  [Cro::HTTP] 1..5
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-webtoken-bearer.rakutest
  [Cro::HTTP] ok 1 - Username is correct
  [Cro::HTTP] ok 2 - Expired token is not passed
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-webtoken-cookie.rakutest
  [Cro::HTTP] ok 1 - Token is set to cookies
  [Cro::HTTP] ok 2 - Username is correct
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-cookie.rakutest
  [Cro::HTTP] ok 1 - Correct cookie names are into the subset
  [Cro::HTTP] ok 2 - Empty cookie name is now allowed
  [Cro::HTTP] ok 3 - No parens allowed in a cookie
  [Cro::HTTP] ok 4 - Cookie octet can be wrapped in double quotes
  [Cro::HTTP] # Subtest: Incorrect symbols are outside of CookieName subset
  [Cro::HTTP]     ok 1 - 
  [Cro::HTTP]     ok 2 - 
  [Cro::HTTP]     ok 3 - 
  [Cro::HTTP]     ok 4 - 
  [Cro::HTTP]     ok 5 - 
  [Cro::HTTP]     ok 6 - 
  [Cro::HTTP]     ok 7 - 
  [Cro::HTTP]     ok 8 - 
  [Cro::HTTP]     ok 9 - 
  [Cro::HTTP]     ok 10 - 
  [Cro::HTTP]     ok 11 - 
  [Cro::HTTP]     ok 12 - 
  [Cro::HTTP]     ok 13 - 
  [Cro::HTTP]     ok 14 - 
  [Cro::HTTP]     ok 15 - 
  [Cro::HTTP]     ok 16 - 
  [Cro::HTTP]     ok 17 - 
  [Cro::HTTP]     ok 18 - 
  [Cro::HTTP]     ok 19 - 
  [Cro::HTTP]     ok 20 - 
  [Cro::HTTP]     ok 21 - 
  [Cro::HTTP]     ok 22 - 
  [Cro::HTTP]     ok 23 - 
  [Cro::HTTP]     ok 24 - 
  [Cro::HTTP]     ok 25 - 
  [Cro::HTTP]     ok 26 - 
  [Cro::HTTP]     ok 27 - 
  [Cro::HTTP]     ok 28 - 
  [Cro::HTTP]     ok 29 - 
  [Cro::HTTP]     ok 30 - 
  [Cro::HTTP]     ok 31 - 
  [Cro::HTTP]     ok 32 - 
  [Cro::HTTP]     ok 33 - 
  [Cro::HTTP]     ok 34 - 
  [Cro::HTTP]     ok 35 - 
  [Cro::HTTP]     ok 36 - 
  [Cro::HTTP]     ok 37 - 
  [Cro::HTTP]     ok 38 - 
  [Cro::HTTP]     ok 39 - 
  [Cro::HTTP]     ok 40 - 
  [Cro::HTTP]     ok 41 - 
  [Cro::HTTP]     ok 42 - 
  [Cro::HTTP]     ok 43 - 
  [Cro::HTTP]     ok 44 - 
  [Cro::HTTP]     ok 45 - 
  [Cro::HTTP]     ok 46 - 
  [Cro::HTTP]     ok 47 - 
  [Cro::HTTP]     ok 48 - 
  [Cro::HTTP]     ok 49 - 
  [Cro::HTTP]     ok 50 - 
  [Cro::HTTP]     ok 51 - 
  [Cro::HTTP]     1..51
  [Cro::HTTP] ok 5 - Incorrect symbols are outside of CookieName subset
  [Cro::HTTP] ok 6 - Correct cookie values are into the subset
  [Cro::HTTP] ok 7 - Empty cookie value is allowed
  [Cro::HTTP] # Subtest: Incorrect symbols are outside of CookieValue subset
  [Cro::HTTP]     ok 1 - 
  [Cro::HTTP]     ok 2 - 
  [Cro::HTTP]     ok 3 - 
  [Cro::HTTP]     ok 4 - 
  [Cro::HTTP]     ok 5 - 
  [Cro::HTTP]     1..5
  [Cro::HTTP] ok 8 - Incorrect symbols are outside of CookieValue subset
  [Cro::HTTP] ok 9 - Correct domain name works
  [Cro::HTTP] ok 10 - Incorrect domain name with bad character
  [Cro::HTTP] ok 11 - Empty domain name cannot be created
  [Cro::HTTP] ok 12 - Domain name cannot contain spaces
  [Cro::HTTP] ok 13 - Set-Cookie string 1 parses
  [Cro::HTTP] ok 14 - Set-Cookie string 2 parses
  [Cro::HTTP] ok 15 - Set-Cookie string 3 parses
  [Cro::HTTP] ok 16 - Set-Cookie ala buggy Tomcat (missing space); we tolerate this
  [Cro::HTTP] ok 17 - Cookie cannot be created with no arguments
  [Cro::HTTP] ok 18 - Cookie cannot be created without value
  [Cro::HTTP] ok 19 - Cookie cannot be created without name
  [Cro::HTTP] ok 20 - Cookie can be created
  [Cro::HTTP] ok 21 - New is read only
  [Cro::HTTP] ok 22 - Value is read only
  [Cro::HTTP] ok 23 - Expires is read only
  [Cro::HTTP] ok 24 - Max-age is read only
  [Cro::HTTP] ok 25 - Domain is read only
  [Cro::HTTP] ok 26 - Path is read only
  [Cro::HTTP] ok 27 - Secure is read only
  [Cro::HTTP] ok 28 - Http-only is read only
  [Cro::HTTP] ok 29 - SameSite is read only
  [Cro::HTTP] ok 30 - Set cookie 1 works
  [Cro::HTTP] ok 31 - Cookie 1 works
  [Cro::HTTP] ok 32 - Cookie 1 can be parsed
  [Cro::HTTP] ok 33 - Set cookie 2 works
  [Cro::HTTP] ok 34 - Cookie 2 works
  [Cro::HTTP] ok 35 - Cookie 2 can be parsed
  [Cro::HTTP] ok 36 - Set cookie 3 works
  [Cro::HTTP] ok 37 - Cookie 3 works
  [Cro::HTTP] ok 38 - Cookie 3 can be parsed
  [Cro::HTTP] ok 39 - Set cookie 4 works
  [Cro::HTTP] ok 40 - Cookie 4 works
  [Cro::HTTP] ok 41 - Cookie 4 can be parsed
  [Cro::HTTP] ok 42 - Invalid SameSite value discarded
  [Cro::HTTP] ok 43 - Valid SameSite value cookie 0 can be parsed
  [Cro::HTTP] ok 44 - Valid SameSite value cookie 1 can be parsed
  [Cro::HTTP] ok 45 - Valid SameSite value cookie 2 can be parsed
  [Cro::HTTP] ok 46 - Correct path after extension
  [Cro::HTTP] ok 47 - Secure parsed after extension
  [Cro::HTTP] ok 48 - Extensions are parsed and extracted also
  [Cro::HTTP] ok 49 - Correct cookie name when illegal whitespace in value
  [Cro::HTTP] ok 50 - Cookie value parsed up to illegal whitespace
  [Cro::HTTP] ok 51 - Recovered to parse path after illegal cookie value
  [Cro::HTTP] 1..51
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-cookiejar.rakutest
  [Cro::HTTP] ok 1 - Empty cookie jar contents returns empty list
  [Cro::HTTP] ok 2 - Empty cookie jar contents with uri returns empty list
  [Cro::HTTP] ok 3 - Two cookies were added
  [Cro::HTTP] ok 4 - Cookie addition is neutral
  [Cro::HTTP] ok 5 - Cookie with bad domain was not added
  [Cro::HTTP] ok 6 - Uri-based check
  [Cro::HTTP] ok 7 - Good cookies are here
  [Cro::HTTP] ok 8 - Clear for absent url leaves jar untouched
  [Cro::HTTP] ok 9 - Clear for absent url with existing cookie name leaves jar untouched
  [Cro::HTTP] ok 10 - One cookie was removed
  [Cro::HTTP] ok 11 - All cookies from correct domain were removed
  [Cro::HTTP] ok 12 - Call to clear clears cookie jar
  [Cro::HTTP] ok 13 - Cookie with duration was added successfully
  [Cro::HTTP] ok 14 - Creation time is preserved during cookie update
  [Cro::HTTP] ok 15 - Cookie was deleted on negative-time cookie addition
  [Cro::HTTP] ok 16 - Cookies are added for sub-domains
  [Cro::HTTP] ok 17 - Rejected for incorrect sub-domain
  [Cro::HTTP] ok 18 - Header was added
  [Cro::HTTP] ok 19 - Set string is correct
  [Cro::HTTP] ok 20 - A single cookie was added, successfully
  [Cro::HTTP] ok 21 - Added cookie has correct name
  [Cro::HTTP] ok 22 - Added cookie has correct value
  [Cro::HTTP] ok 23 - Added cookie has proper domain
  [Cro::HTTP] ok 24 - Added cookie has proper path
  [Cro::HTTP] ok 25 - Cookie has proper expiration time
  [Cro::HTTP] ok 26 - A second cookie was added successfully
  [Cro::HTTP] ok 27 - New cookie is not persistent
  [Cro::HTTP] ok 28 - New cookie has expected expiration time with no max-age set
  [Cro::HTTP] ok 29 - First cookie was added to request
  [Cro::HTTP] ok 30 - Second cookie was added to request
  [Cro::HTTP] 1..30
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-log-file.rakutest
  [Cro::HTTP] ok 1 - Correct responses logged
  [Cro::HTTP] ok 2 - Error responses logged
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-middleware.rakutest
  [Cro::HTTP] # Subtest: Request and response middleware written using a transform
  [Cro::HTTP]     ok 1 - Header was set
  [Cro::HTTP]     ok 2 - Target was processed
  [Cro::HTTP]     ok 3 - after works with before
  [Cro::HTTP]     ok 4 - before works with after
  [Cro::HTTP]     1..4
  [Cro::HTTP] ok 1 - Request and response middleware written using a transform
  [Cro::HTTP] # Subtest: Request and response middleware written using a Cro::HTTP::Middleware roles
  [Cro::HTTP]     ok 1 - Header was set
  [Cro::HTTP]     ok 2 - Target was processed
  [Cro::HTTP]     ok 3 - after works with before
  [Cro::HTTP]     ok 4 - before works with after
  [Cro::HTTP]     ok 5 - Request middleware works with before-matched in route block
  [Cro::HTTP]     ok 6 - Response middleware works with after-matched in route block
  [Cro::HTTP]     1..6
  [Cro::HTTP] ok 2 - Request and response middleware written using a Cro::HTTP::Middleware roles
  [Cro::HTTP] # Subtest: Conditional response middleware using Cro::HTTP::Middleware::Conditional
  [Cro::HTTP]     # Subtest: Got 403 response from middleware when no auth header
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6496884230272) ... }
  [Cro::HTTP]     ok 1 - Got 403 response from middleware when no auth header
  [Cro::HTTP]     ok 2 - Got 200 normal response with an auth header
  [Cro::HTTP]     # Subtest: Got 403 response from middleware when no auth header (before-matched in router)
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6496885154168) ... }
  [Cro::HTTP]     ok 3 - Got 403 response from middleware when no auth header (before-matched in router)
  [Cro::HTTP]     ok 4 - Got 200 normal response with an auth header (before-matched in router)
  [Cro::HTTP]     # Subtest: Got 403 response from middleware when no auth header (before-matched + include in router)
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6496885157696) ... }
  [Cro::HTTP]     ok 5 - Got 403 response from middleware when no auth header (before-matched + include in router)
  [Cro::HTTP]     ok 6 - Got 200 normal response with an auth header (before-matched + include in router)
  [Cro::HTTP]     1..6
  [Cro::HTTP] ok 3 - Conditional response middleware using Cro::HTTP::Middleware::Conditional
  [Cro::HTTP] # Subtest: Request/response middleware using Cro::HTTP::Middleware::RequestResponse
  [Cro::HTTP]     ok 1 - Got 200 response on first request
  [Cro::HTTP]     ok 2 - Response part added header
  [Cro::HTTP]     ok 3 - Expected body
  [Cro::HTTP]     ok 4 - Got 200 response on second request
  [Cro::HTTP]     ok 5 - Response part did not run on early response
  [Cro::HTTP]     ok 6 - Got cached body
  [Cro::HTTP]     ok 7 - Got 200 response on first request (before-matched in router)
  [Cro::HTTP]     ok 8 - Response part added header (before-matched in router)
  [Cro::HTTP]     ok 9 - Expected body (before-matched in router)
  [Cro::HTTP]     ok 10 - Got 200 response on second request (before-matched in router)
  [Cro::HTTP]     ok 11 - Response part did not run on early response (before-matched in router)
  [Cro::HTTP]     ok 12 - Got cached body (before-matched in router)
  [Cro::HTTP]     ok 13 - Got 200 response on first request (before-matched + include in router)
  [Cro::HTTP]     ok 14 - Response part added header (before-matched + include in router)
  [Cro::HTTP]     ok 15 - Expected body (before-matched + include in router)
  [Cro::HTTP]     ok 16 - Got 200 response on second request (before-matched + include in router)
  [Cro::HTTP]     ok 17 - Response part did not run on early response (before-matched + include in router)
  [Cro::HTTP]     ok 18 - Got cached body (before-matched + include in router)
  [Cro::HTTP]     1..18
  [Cro::HTTP] ok 4 - Request/response middleware using Cro::HTTP::Middleware::RequestResponse
  [Cro::HTTP] # Subtest: Byte-level middleware, before/after request is parsed
  [Cro::HTTP]     ok 1 - before-parse works
  [Cro::HTTP]     ok 2 - after-serialize works
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 5 - Byte-level middleware, before/after request is parsed
  [Cro::HTTP] # Subtest: Interaction of middleware written as Cro::Transform with HTTP router
  [Cro::HTTP]     ok 1 - per-route after-matched middleware for regular request works
  [Cro::HTTP]     ok 2 - per-route before-matched middleware for regular request works
  [Cro::HTTP]     ok 3 - per-route after-matched middleware for delegated request works
  [Cro::HTTP]     ok 4 - per-route before-matched middleware for delegated request works
  [Cro::HTTP]     ok 5 - per-route after-matched middleware for includee works
  [Cro::HTTP]     ok 6 - per-route before-matched middleware for includee works
  [Cro::HTTP]     ok 7 - per-route after-matched middleware for includee works
  [Cro::HTTP]     ok 8 - per-route before-matched middleware for includee works
  [Cro::HTTP]     ok 9 - per-route block before-matched middleware works
  [Cro::HTTP]     ok 10 - per-route block after-matched middleware works
  [Cro::HTTP]     ok 11 - Cannot use wrong typed Transformer as a middleware
  [Cro::HTTP]     1..11
  [Cro::HTTP] ok 6 - Interaction of middleware written as Cro::Transform with HTTP router
  [Cro::HTTP] # Subtest: Conditional response in block form of before-matched in router
  [Cro::HTTP]     # Subtest: Block form of before-matched in router can produce an early response
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6496910394568) ... }
  [Cro::HTTP]     ok 1 - Block form of before-matched in router can produce an early response
  [Cro::HTTP]     ok 2 - Block form of before-matched not producing a response also works
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 7 - Conditional response in block form of before-matched in router
  [Cro::HTTP] ok 8 - before-matched applies even to delegate done before it
  [Cro::HTTP] ok 9 - after-matched applies even to delegate done after it
  [Cro::HTTP] ok 10 - before-matched applies even to a route before it
  [Cro::HTTP] ok 11 - after-matched middleware applies even to a route before it
  [Cro::HTTP] ok 12 - Dies when no matched rule
  [Cro::HTTP] ok 13 - before block was executed
  [Cro::HTTP] ok 14 - before-matched block was not executed
  [Cro::HTTP] ok 15 - after block was executed
  [Cro::HTTP] ok 16 - after-matched block was not executed
  [Cro::HTTP] ok 17 - before and after is run from block definition
  [Cro::HTTP] ok 18 - before and after is run from class definition
  [Cro::HTTP] ok 19 - before and after is run from RequestResponse(Pair) definition
  [Cro::HTTP] ok 20 - Auth middleware is applied
  [Cro::HTTP] ok 21 - Auth middleware is applied 2
  [Cro::HTTP] ok 22 - After middleware is applied
  [Cro::HTTP] # Subtest: Better exception message when user tries to include route with before/after
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::AdHoc)
  [Cro::HTTP]     ok 3 - .message matches /'delegate'/
  [Cro::HTTP] ok 23 - Better exception message when user tries to include route with before/after
  [Cro::HTTP] ok 24 - delegate does not cause an exception
  [Cro::HTTP] 1..24
  [Cro::HTTP] Saw 1 occurrence of deprecated code.
  [Cro::HTTP] ================================================================================
  [Cro::HTTP] Method perl (from Mu) seen at:
  [Cro::HTTP]   /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist/lib/Cro/HTTP/Router.rakumod (Cro::HTTP::Router), line 1335
  [Cro::HTTP] Please use raku instead.
  [Cro::HTTP] --------------------------------------------------------------------------------
  [Cro::HTTP] Please contact the author to have these occurrences of deprecated code
  [Cro::HTTP] adapted, so that this message will disappear!
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-rawbodyparserselector.rakutest
  [Cro::HTTP] ok 1 - got the correct 'Cro::HTTP::RawBodyParser'
  [Cro::HTTP] ok 2 - No content-length or transfer-encoding
  [Cro::HTTP] ok 3 - got the correct 'Cro::HTTP::RawBodyParser'
  [Cro::HTTP] ok 4 - Content-Length
  [Cro::HTTP] ok 5 - got the correct 'Cro::HTTP::RawBodyParser'
  [Cro::HTTP] ok 6 - Chunked transfer encoding
  [Cro::HTTP] ok 7 - got the correct 'Cro::HTTP::RawBodyParser'
  [Cro::HTTP] ok 8 - Identity transfer encoding - no content-length
  [Cro::HTTP] ok 9 - got the correct 'Cro::HTTP::RawBodyParser'
  [Cro::HTTP] ok 10 - Identity transfer encoding - with content-length
  [Cro::HTTP] 1..10
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request-parser.rakutest
  [Cro::HTTP] ok 1 - HTTP request parser is a transform
  [Cro::HTTP] ok 2 - HTTP request parser consumes TCP messages
  [Cro::HTTP] ok 3 - HTTP request parser produces HTTP requests
  [Cro::HTTP] ok 4 - Malformed request line - only verb
  [Cro::HTTP] ok 5 - check 1
  [Cro::HTTP] ok 6 - Malformed request line - no version
  [Cro::HTTP] ok 7 - check 1
  [Cro::HTTP] ok 8 - Malformed request line - utter crap
  [Cro::HTTP] ok 9 - check 1
  [Cro::HTTP] ok 10 - Malformed HTTP version (1)
  [Cro::HTTP] ok 11 - check 1
  [Cro::HTTP] ok 12 - Malformed HTTP version (2)
  [Cro::HTTP] ok 13 - check 1
  [Cro::HTTP] ok 14 - Malformed HTTP version (3)
  [Cro::HTTP] ok 15 - check 1
  [Cro::HTTP] ok 16 - Malformed HTTP version (4)
  [Cro::HTTP] ok 17 - check 1
  [Cro::HTTP] ok 18 - Malformed HTTP version (5)
  [Cro::HTTP] ok 19 - check 1
  [Cro::HTTP] ok 20 - Unimplemented HTTP version
  [Cro::HTTP] ok 21 - check 1
  [Cro::HTTP] ok 22 - Simple GET request with no headers
  [Cro::HTTP] ok 23 - check 1
  [Cro::HTTP] ok 24 - check 2
  [Cro::HTTP] ok 25 - check 3
  [Cro::HTTP] ok 26 - Simple HEAD request with no headers
  [Cro::HTTP] ok 27 - check 1
  [Cro::HTTP] ok 28 - check 2
  [Cro::HTTP] ok 29 - check 3
  [Cro::HTTP] ok 30 - Simple POST request with no headers
  [Cro::HTTP] ok 31 - check 1
  [Cro::HTTP] ok 32 - check 2
  [Cro::HTTP] ok 33 - check 3
  [Cro::HTTP] ok 34 - Simple PUT request with no headers
  [Cro::HTTP] ok 35 - check 1
  [Cro::HTTP] ok 36 - check 2
  [Cro::HTTP] ok 37 - check 3
  [Cro::HTTP] ok 38 - Simple DELETE request with no headers
  [Cro::HTTP] ok 39 - check 1
  [Cro::HTTP] ok 40 - check 2
  [Cro::HTTP] ok 41 - check 3
  [Cro::HTTP] ok 42 - Simple OPTIONS request with no headers
  [Cro::HTTP] ok 43 - check 1
  [Cro::HTTP] ok 44 - check 2
  [Cro::HTTP] ok 45 - check 3
  [Cro::HTTP] ok 46 - The TRACE method, as it is not implemented by default
  [Cro::HTTP] ok 47 - check 1
  [Cro::HTTP] ok 48 - Simple PATCH request with no headers
  [Cro::HTTP] ok 49 - check 1
  [Cro::HTTP] ok 50 - check 2
  [Cro::HTTP] ok 51 - check 3
  [Cro::HTTP] ok 52 - The TRACE method, as it is not implemented by default
  [Cro::HTTP] ok 53 - check 1
  [Cro::HTTP] ok 54 - The TRACE method if included in allowed-methods
  [Cro::HTTP] ok 55 - check 1
  [Cro::HTTP] ok 56 - check 2
  [Cro::HTTP] ok 57 - check 3
  [Cro::HTTP] ok 58 - PUT when it is not included in the allowed methods
  [Cro::HTTP] ok 59 - check 1
  [Cro::HTTP] ok 60 - An empty line before the request line
  [Cro::HTTP] ok 61 - check 1
  [Cro::HTTP] ok 62 - check 2
  [Cro::HTTP] ok 63 - check 3
  [Cro::HTTP] ok 64 - A few empty lines before the request line
  [Cro::HTTP] ok 65 - check 1
  [Cro::HTTP] ok 66 - check 2
  [Cro::HTTP] ok 67 - check 3
  [Cro::HTTP] ok 68 - Host header
  [Cro::HTTP] ok 69 - check 1
  [Cro::HTTP] ok 70 - check 2
  [Cro::HTTP] ok 71 - check 3
  [Cro::HTTP] ok 72 - check 4
  [Cro::HTTP] ok 73 - check 5
  [Cro::HTTP] ok 74 - check 6
  [Cro::HTTP] ok 75 - check 7
  [Cro::HTTP] ok 76 - Host header with no whitespace
  [Cro::HTTP] ok 77 - check 1
  [Cro::HTTP] ok 78 - check 2
  [Cro::HTTP] ok 79 - check 3
  [Cro::HTTP] ok 80 - check 4
  [Cro::HTTP] ok 81 - check 5
  [Cro::HTTP] ok 82 - check 6
  [Cro::HTTP] ok 83 - check 7
  [Cro::HTTP] ok 84 - Host header with trailing whitespace
  [Cro::HTTP] ok 85 - check 1
  [Cro::HTTP] ok 86 - check 2
  [Cro::HTTP] ok 87 - check 3
  [Cro::HTTP] ok 88 - check 4
  [Cro::HTTP] ok 89 - check 5
  [Cro::HTTP] ok 90 - check 6
  [Cro::HTTP] ok 91 - check 7
  [Cro::HTTP] ok 92 - Host header with tab before and after value
  [Cro::HTTP] ok 93 - check 1
  [Cro::HTTP] ok 94 - check 2
  [Cro::HTTP] ok 95 - check 3
  [Cro::HTTP] ok 96 - check 4
  [Cro::HTTP] ok 97 - check 5
  [Cro::HTTP] ok 98 - check 6
  [Cro::HTTP] ok 99 - check 7
  [Cro::HTTP] ok 100 - Header with insane but actually totally legit name
  [Cro::HTTP] ok 101 - check 1
  [Cro::HTTP] ok 102 - check 2
  [Cro::HTTP] ok 103 - check 3
  [Cro::HTTP] ok 104 - check 4
  [Cro::HTTP] ok 105 - check 5
  [Cro::HTTP] ok 106 - check 6
  [Cro::HTTP] ok 107 - check 7
  [Cro::HTTP] ok 108 - Not allowed " in header
  [Cro::HTTP] ok 109 - check 1
  [Cro::HTTP] ok 110 - Not allowed ( in header
  [Cro::HTTP] ok 111 - check 1
  [Cro::HTTP] ok 112 - Not allowed ) in header
  [Cro::HTTP] ok 113 - check 1
  [Cro::HTTP] ok 114 - Not allowed [ in header
  [Cro::HTTP] ok 115 - check 1
  [Cro::HTTP] ok 116 - Not allowed ] in header
  [Cro::HTTP] ok 117 - check 1
  [Cro::HTTP] ok 118 - Not allowed { in header
  [Cro::HTTP] ok 119 - check 1
  [Cro::HTTP] ok 120 - Not allowed } in header
  [Cro::HTTP] ok 121 - check 1
  [Cro::HTTP] ok 122 - Not allowed @ in header
  [Cro::HTTP] ok 123 - check 1
  [Cro::HTTP] ok 124 - Not allowed \ in header
  [Cro::HTTP] ok 125 - check 1
  [Cro::HTTP] ok 126 - Not allowed / in header
  [Cro::HTTP] ok 127 - check 1
  [Cro::HTTP] ok 128 - Not allowed < in header
  [Cro::HTTP] ok 129 - check 1
  [Cro::HTTP] ok 130 - Not allowed > in header
  [Cro::HTTP] ok 131 - check 1
  [Cro::HTTP] ok 132 - Not allowed , in header
  [Cro::HTTP] ok 133 - check 1
  [Cro::HTTP] ok 134 - Not allowed ; in header
  [Cro::HTTP] ok 135 - check 1
  [Cro::HTTP] ok 136 - Header with empty field
  [Cro::HTTP] ok 137 - check 1
  [Cro::HTTP] ok 138 - check 2
  [Cro::HTTP] ok 139 - check 3
  [Cro::HTTP] ok 140 - check 4
  [Cro::HTTP] ok 141 - check 5
  [Cro::HTTP] ok 142 - check 6
  [Cro::HTTP] ok 143 - check 7
  [Cro::HTTP] ok 144 - Field value can be any printable char including latin-1 range
  [Cro::HTTP] ok 145 - check 1
  [Cro::HTTP] ok 146 - check 2
  [Cro::HTTP] ok 147 - check 3
  [Cro::HTTP] ok 148 - check 4
  [Cro::HTTP] ok 149 - check 5
  [Cro::HTTP] ok 150 - check 6
  [Cro::HTTP] ok 151 - check 7
  [Cro::HTTP] ok 152 - Field values may have whitespace in them
  [Cro::HTTP] ok 153 - check 1
  [Cro::HTTP] ok 154 - check 2
  [Cro::HTTP] ok 155 - check 3
  [Cro::HTTP] ok 156 - check 4
  [Cro::HTTP] ok 157 - check 5
  [Cro::HTTP] ok 158 - check 6
  [Cro::HTTP] ok 159 - check 7
  [Cro::HTTP] ok 160 - Whitespace after field name ignored
  [Cro::HTTP] ok 161 - check 1
  [Cro::HTTP] ok 162 - check 2
  [Cro::HTTP] ok 163 - check 3
  [Cro::HTTP] ok 164 - check 4
  [Cro::HTTP] ok 165 - check 5
  [Cro::HTTP] ok 166 - check 6
  [Cro::HTTP] ok 167 - check 7
  [Cro::HTTP] ok 168 - Control chars other than space/tab not allowed (0)
  [Cro::HTTP] ok 169 - check 1
  [Cro::HTTP] ok 170 - Control chars other than space/tab not allowed (1)
  [Cro::HTTP] ok 171 - check 1
  [Cro::HTTP] ok 172 - Request with multiple headers (example from RFC)
  [Cro::HTTP] ok 173 - check 1
  [Cro::HTTP] ok 174 - check 2
  [Cro::HTTP] ok 175 - check 3
  [Cro::HTTP] ok 176 - check 4
  [Cro::HTTP] ok 177 - check 5
  [Cro::HTTP] ok 178 - check 6
  [Cro::HTTP] ok 179 - check 7
  [Cro::HTTP] ok 180 - check 8
  [Cro::HTTP] ok 181 - check 9
  [Cro::HTTP] ok 182 - check 10
  [Cro::HTTP] ok 183 - check 11
  [Cro::HTTP] ok 184 - check 12
  [Cro::HTTP] ok 185 - check 13
  [Cro::HTTP] ok 186 - Request path and path segments for /hello.txt
  [Cro::HTTP] ok 187 - check 1
  [Cro::HTTP] ok 188 - check 2
  [Cro::HTTP] ok 189 - Request path and path segments for /oh/my/path
  [Cro::HTTP] ok 190 - check 1
  [Cro::HTTP] ok 191 - check 2
  [Cro::HTTP] ok 192 - Query strings are parsed and accessible
  [Cro::HTTP] ok 193 - check 1
  [Cro::HTTP] ok 194 - check 2
  [Cro::HTTP] ok 195 - check 3
  [Cro::HTTP] ok 196 - check 4
  [Cro::HTTP] ok 197 - check 5
  [Cro::HTTP] ok 198 - check 6
  [Cro::HTTP] ok 199 - check 7
  [Cro::HTTP] ok 200 - Query strings with empty values
  [Cro::HTTP] ok 201 - check 1
  [Cro::HTTP] ok 202 - check 2
  [Cro::HTTP] ok 203 - check 3
  [Cro::HTTP] ok 204 - check 4
  [Cro::HTTP] ok 205 - check 5
  [Cro::HTTP] ok 206 - check 6
  [Cro::HTTP] ok 207 - check 7
  [Cro::HTTP] ok 208 - Query string keys and values that are encoded
  [Cro::HTTP] ok 209 - check 1
  [Cro::HTTP] ok 210 - check 2
  [Cro::HTTP] ok 211 - check 3
  [Cro::HTTP] ok 212 - check 4
  [Cro::HTTP] ok 213 - check 5
  [Cro::HTTP] ok 214 - check 6
  [Cro::HTTP] ok 215 - check 7
  [Cro::HTTP] ok 216 - Query strings with multiple values for the same key
  [Cro::HTTP] ok 217 - check 1
  [Cro::HTTP] ok 218 - check 2
  [Cro::HTTP] ok 219 - check 3
  [Cro::HTTP] ok 220 - check 4
  [Cro::HTTP] ok 221 - check 5
  [Cro::HTTP] ok 222 - check 6
  [Cro::HTTP] ok 223 - check 7
  [Cro::HTTP] ok 224 - check 8
  [Cro::HTTP] ok 225 - check 9
  [Cro::HTTP] ok 226 - Request with body, length specified by content-length
  [Cro::HTTP] ok 227 - check 1
  [Cro::HTTP] ok 228 - check 2
  [Cro::HTTP] ok 229 - check 3
  [Cro::HTTP] ok 230 - Request with body, sent with chunked encoding
  [Cro::HTTP] ok 231 - check 1
  [Cro::HTTP] ok 232 - check 2
  [Cro::HTTP] ok 233 - check 3
  [Cro::HTTP] ok 234 - A text/whatever request with body
  [Cro::HTTP] ok 235 - text/whatever gives string body
  [Cro::HTTP] ok 236 - Body contains the correct value
  [Cro::HTTP] ok 237 - A unknown/foo request with body
  [Cro::HTTP] ok 238 - unknown/foo .body gives Blob
  [Cro::HTTP] ok 239 - Blob has correct content
  [Cro::HTTP] ok 240 - Basic case of application/x-www-form-urlencoded
  [Cro::HTTP] ok 241 - .pairs returns ordered pairs from the decoded body
  [Cro::HTTP] ok 242 - .list returns ordered pairs from the decoded body
  [Cro::HTTP] ok 243 - .hash returns hash of the decoded body
  [Cro::HTTP] ok 244 - Can index associatively (1)
  [Cro::HTTP] ok 245 - Can index associatively (2)
  [Cro::HTTP] ok 246 - Can index associatively (3)
  [Cro::HTTP] ok 247 - Can index associatively with :exists (1)
  [Cro::HTTP] ok 248 - Can index associatively with :exists (2)
  [Cro::HTTP] ok 249 - Can index associatively with :exists (3)
  [Cro::HTTP] ok 250 - Multiple entries with same name in application/x-www-form-urlencoded
  [Cro::HTTP] ok 251 - .pairs returns ordered pairs, with multiple values in place
  [Cro::HTTP] ok 252 - .list returns ordered pairs, with muliplte values in place
  [Cro::HTTP] ok 253 - .hash gives back Hash with 3 elements
  [Cro::HTTP] ok 254 - Get back a HTTP multi-value (1)
  [Cro::HTTP] ok 255 - Get back a HTTP multi-value (2)
  [Cro::HTTP] ok 256 - Stringifying multi-value is correct (1)
  [Cro::HTTP] ok 257 - Stringifying multi-value is correct (2)
  [Cro::HTTP] ok 258 - Indexing multi-value is correct (1)
  [Cro::HTTP] ok 259 - Indexing multi-value is correct (2)
  [Cro::HTTP] ok 260 - When only one value with the name, get back a Str
  [Cro::HTTP] ok 261 - Value is correct
  [Cro::HTTP] ok 262 - Hash-indexing body gives HTTP multi-value (1)
  [Cro::HTTP] ok 263 - Hash-indexing body gives HTTP multi-value (2)
  [Cro::HTTP] ok 264 - Except when only one value for the name, then it is Str
  [Cro::HTTP] ok 265 - Charset present in content-type header field after application/x-www-form-urlencoded
  [Cro::HTTP] ok 266 - WWWUrlEncode prasers works correct with charset in content-type
  [Cro::HTTP] ok 267 - WWWFormUrlEncoded with empty body
  [Cro::HTTP] ok 268 - test `with message.content-type` returns Boolean
  [Cro::HTTP] ok 269 - Basic %-encoded things in an application/x-www-form-urlencoded
  [Cro::HTTP] ok 270 - %-encoded values in ASCII range handled correctly
  [Cro::HTTP] ok 271 - %-encoded non-ASCII is utf-8 by default in  application/x-www-form-urlencoded
  [Cro::HTTP] ok 272 - %-encoded values default to UTF-8 decoding
  [Cro::HTTP] ok 273 - Can pick default encoding for application/x-www-form-urlencoded
  [Cro::HTTP] ok 274 - 
  [Cro::HTTP] ok 275 - 
  [Cro::HTTP] ok 276 - %-encoded values handled correctly when default set to latin-1
  [Cro::HTTP] ok 277 - 
  [Cro::HTTP] ok 278 - 
  [Cro::HTTP] ok 279 - Respects encoding set by _charset_ in application/x-www-form-urlencoded
  [Cro::HTTP] ok 280 - %-encoded values decoded as latin-1 as set in _charset_
  [Cro::HTTP] ok 281 - A _charset_ in application/x-www-form-urlencoded overrides configured default
  [Cro::HTTP] ok 282 - Values were decoded as utf-8, not latin-1 default, due to _charset_
  [Cro::HTTP] ok 283 - No errors on keys with empty value or missing value
  [Cro::HTTP] ok 284 - 
  [Cro::HTTP] ok 285 - Simple multipart/form-data
  [Cro::HTTP] ok 286 - First part has 1 header
  [Cro::HTTP] ok 287 - First part header name correct
  [Cro::HTTP] ok 288 - First part header value correct
  [Cro::HTTP] ok 289 - First part has a content-type that is a Cro::MediaType
  [Cro::HTTP] ok 290 - First part has default text type
  [Cro::HTTP] ok 291 - First part has default plain subtype
  [Cro::HTTP] ok 292 - First part has correct field name
  [Cro::HTTP] ok 293 - First part has correct body blob
  [Cro::HTTP] ok 294 - First part has correct body text
  [Cro::HTTP] ok 295 - First part has correct body
  [Cro::HTTP] ok 296 - Second part has 1 header
  [Cro::HTTP] ok 297 - Second part header name correct
  [Cro::HTTP] ok 298 - Second part header value correct
  [Cro::HTTP] ok 299 - Second part has correct field name
  [Cro::HTTP] ok 300 - Second part has a content-type that is a Cro::MediaType
  [Cro::HTTP] ok 301 - Second part has default text type
  [Cro::HTTP] ok 302 - Second part has default plain subtype
  [Cro::HTTP] ok 303 - Second part has correct body blob
  [Cro::HTTP] ok 304 - Second part has correct body text
  [Cro::HTTP] ok 305 - Second part has correct body
  [Cro::HTTP] ok 306 - A multipart/form-data with a file upload
  [Cro::HTTP] ok 307 - Have 2 parts
  [Cro::HTTP] ok 308 - First part has 1 header
  [Cro::HTTP] ok 309 - First part header name correct
  [Cro::HTTP] ok 310 - First part header value correct
  [Cro::HTTP] ok 311 - First part has a content-type that is a Cro::MediaType
  [Cro::HTTP] ok 312 - First part has default text type
  [Cro::HTTP] ok 313 - First part has default plain subtype
  [Cro::HTTP] ok 314 - First part has correct field name
  [Cro::HTTP] ok 315 - First part has no filename
  [Cro::HTTP] ok 316 - First part has correct body text
  [Cro::HTTP] ok 317 - First part has correct body
  [Cro::HTTP] ok 318 - Second part has 2 headers
  [Cro::HTTP] ok 319 - First header name correct
  [Cro::HTTP] ok 320 - First header value correct
  [Cro::HTTP] ok 321 - Second header name correct
  [Cro::HTTP] ok 322 - Second header value correct
  [Cro::HTTP] ok 323 - Second part has a content-type that is a Cro::MediaType
  [Cro::HTTP] ok 324 - Second part has image media type
  [Cro::HTTP] ok 325 - Second part has gif media subtype
  [Cro::HTTP] ok 326 - Second part has correct field name
  [Cro::HTTP] ok 327 - Second part has correct filename
  [Cro::HTTP] ok 328 - Second part has correct body blob
  [Cro::HTTP] ok 329 - Second part has correct body
  [Cro::HTTP] ok 330 - An application/json request decodes JSON body
  [Cro::HTTP] ok 331 - .body of application/json with object gives Hash
  [Cro::HTTP] ok 332 - JSON was correctly decoded
  [Cro::HTTP] ok 333 - An media type with the +json suffix decodes JSON body
  [Cro::HTTP] ok 334 - .body of application/vnd.my-org+json with object gives Hash
  [Cro::HTTP] ok 335 - JSON was correctly decoded
  [Cro::HTTP] ok 336 - check first 1
  [Cro::HTTP] ok 337 - check second 1
  [Cro::HTTP] ok 338 - Two separate packages are parsed
  [Cro::HTTP] ok 339 - check first 1
  [Cro::HTTP] ok 340 - check second 1
  [Cro::HTTP] ok 341 - Two separate packages are parsed, RequestLine in the first
  [Cro::HTTP] ok 342 - check first 1
  [Cro::HTTP] ok 343 - check second 1
  [Cro::HTTP] ok 344 - Two separate packages are parsed, RequestLine and part of header in the first
  [Cro::HTTP] 1..344
  [Cro::HTTP] Saw 1 occurrence of deprecated code.
  [Cro::HTTP] ================================================================================
  [Cro::HTTP] Method perl (from Mu) seen at:
  [Cro::HTTP]   /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist/lib/Cro/HTTP/Body.rakumod (Cro::HTTP::Body), line 38
  [Cro::HTTP] Please use raku instead.
  [Cro::HTTP] --------------------------------------------------------------------------------
  [Cro::HTTP] Please contact the author to have these occurrences of deprecated code
  [Cro::HTTP] adapted, so that this message will disappear!
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request-serializer.rakutest
  [Cro::HTTP] ok 1 - Basic request with no Host header uses HTTP/1.0
  [Cro::HTTP] ok 2 - Basic request with Host header uses HTTP/1.1
  [Cro::HTTP] ok 3 - Basic request with blob body adds application/octet-stream and length
  [Cro::HTTP] ok 4 - Basic request with blob body does not replace existing content-type
  [Cro::HTTP] ok 5 - Basic request with string body adds text/plain and length
  [Cro::HTTP] ok 6 - Basic request with string body does not replace existing content-type
  [Cro::HTTP] ok 7 - application/json content serializes Hash to JSON
  [Cro::HTTP] ok 8 - application/json content serializes Array to JSON
  [Cro::HTTP] ok 9 - Media type with +json suffix also serializes JSON
  [Cro::HTTP] ok 10 - application/x-www-form-urlencoded with list of pairs
  [Cro::HTTP] ok 11 - application/x-www-form-urlencoded with ASCII things needing escaping
  [Cro::HTTP] ok 12 - application/x-www-form-urlencoded with ASCII things needing escaping
  [Cro::HTTP] ok 13 - application/x-www-form-urlencoded with hash
  [Cro::HTTP] ok 14 - application/x-www-form-urlencoded with body object
  [Cro::HTTP] ok 15 - application/x-www-form-urlencoded body object implies header
  [Cro::HTTP] ok 16 - multipart/form-data with list of pairs
  [Cro::HTTP] ok 17 - multipart/form-data with filename and extra header
  [Cro::HTTP] 1..17
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request.rakutest
  [Cro::HTTP] # Subtest: Request missing method and target throws on .Str
  [Cro::HTTP]     1..2
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Request::Incomplete)
  [Cro::HTTP] ok 1 - Request missing method and target throws on .Str
  [Cro::HTTP] # Subtest: Request missing target throws on .Str
  [Cro::HTTP]     1..2
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Request::Incomplete)
  [Cro::HTTP] ok 2 - Request missing target throws on .Str
  [Cro::HTTP] # Subtest: Request missing method throws on .Str
  [Cro::HTTP]     1..2
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Request::Incomplete)
  [Cro::HTTP] ok 3 - Request missing method throws on .Str
  [Cro::HTTP] ok 4 - Can serialize simple request built with accessors (HTTP/1.0 with no Host)
  [Cro::HTTP] ok 5 - Can serialize simple request with method/target in constructor (HTTP/1.0 with no Host)
  [Cro::HTTP] ok 6 - Lowercase method not allowed
  [Cro::HTTP] ok 7 - Mixed case method not allowed
  [Cro::HTTP] ok 8 - Method with space not allowed
  [Cro::HTTP] ok 9 - Target with space in not allowed
  [Cro::HTTP] ok 10 - Target with newline in not allowed
  [Cro::HTTP] ok 11 - Target with control char not allowed
  [Cro::HTTP] ok 12 - Target with non-Latin-1 characters not allowed
  [Cro::HTTP] ok 13 - Request with Host header will use HTTP/1.1
  [Cro::HTTP] ok 14 - Request header constructed with single-arg append-header overload works
  [Cro::HTTP] ok 15 - Refuses to add request header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 16 - Refuses to add request header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 17 - Refuses to add request header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 18 - Refuses to add request header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 19 - Refuses to add request header with illegal name containing " (single-arg)
  [Cro::HTTP] ok 20 - Refuses to add request header with illegal name containing ( (single-arg)
  [Cro::HTTP] ok 21 - Refuses to add request header with illegal name containing ) (single-arg)
  [Cro::HTTP] ok 22 - Refuses to add request header with illegal name containing [ (single-arg)
  [Cro::HTTP] ok 23 - Refuses to add request header with illegal name containing ] (single-arg)
  [Cro::HTTP] ok 24 - Refuses to add request header with illegal name containing { (single-arg)
  [Cro::HTTP] ok 25 - Refuses to add request header with illegal name containing } (single-arg)
  [Cro::HTTP] ok 26 - Refuses to add request header with illegal name containing @ (single-arg)
  [Cro::HTTP] ok 27 - Refuses to add request header with illegal name containing \ (single-arg)
  [Cro::HTTP] ok 28 - Refuses to add request header with illegal name containing / (single-arg)
  [Cro::HTTP] ok 29 - Refuses to add request header with illegal name containing < (single-arg)
  [Cro::HTTP] ok 30 - Refuses to add request header with illegal name containing > (single-arg)
  [Cro::HTTP] ok 31 - Refuses to add request header with illegal name containing , (single-arg)
  [Cro::HTTP] ok 32 - Refuses to add request header with illegal name containing ; (single-arg)
  [Cro::HTTP] ok 33 - Utterly crazy but valid header can be added (single-arg)
  [Cro::HTTP] ok 34 - Request header constructed with two-arg append-header overload works
  [Cro::HTTP] ok 35 - Refuses to add request header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 36 - Refuses to add request header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 37 - Refuses to add request header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 38 - Refuses to add request header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 39 - Refuses to add request header with illegal name containing " (two-arg)
  [Cro::HTTP] ok 40 - Refuses to add request header with illegal name containing ( (two-arg)
  [Cro::HTTP] ok 41 - Refuses to add request header with illegal name containing ) (two-arg)
  [Cro::HTTP] ok 42 - Refuses to add request header with illegal name containing [ (two-arg)
  [Cro::HTTP] ok 43 - Refuses to add request header with illegal name containing ] (two-arg)
  [Cro::HTTP] ok 44 - Refuses to add request header with illegal name containing { (two-arg)
  [Cro::HTTP] ok 45 - Refuses to add request header with illegal name containing } (two-arg)
  [Cro::HTTP] ok 46 - Refuses to add request header with illegal name containing @ (two-arg)
  [Cro::HTTP] ok 47 - Refuses to add request header with illegal name containing \ (two-arg)
  [Cro::HTTP] ok 48 - Refuses to add request header with illegal name containing / (two-arg)
  [Cro::HTTP] ok 49 - Refuses to add request header with illegal name containing < (two-arg)
  [Cro::HTTP] ok 50 - Refuses to add request header with illegal name containing > (two-arg)
  [Cro::HTTP] ok 51 - Refuses to add request header with illegal name containing , (two-arg)
  [Cro::HTTP] ok 52 - Refuses to add request header with illegal name containing ; (two-arg)
  [Cro::HTTP] ok 53 - Utterly crazy but valid header can be added (two-arg)
  [Cro::HTTP] ok 54 - has-header returns True on header we have
  [Cro::HTTP] ok 55 - has-header is not case-sensitive (1)
  [Cro::HTTP] ok 56 - has-header is not case-sensitive (2)
  [Cro::HTTP] ok 57 - has-header returns False on header we do not have
  [Cro::HTTP] ok 58 - header method fetches a header
  [Cro::HTTP] ok 59 - header method is not case sensitive (1)
  [Cro::HTTP] ok 60 - header method is not case sensitive (2)
  [Cro::HTTP] ok 61 - when there are multiple headers with the name, the value comma-joins them
  [Cro::HTTP] ok 62 - header we do not have returns Nil
  [Cro::HTTP] ok 63 - header-list method returns a List of one header for Host
  [Cro::HTTP] ok 64 - header-list method works case-insensitively
  [Cro::HTTP] ok 65 - header-list method returns a list of values when there are multiple headers
  [Cro::HTTP] ok 66 - header-list methods returns an empty list when no header of the requested name
  [Cro::HTTP] ok 67 - Removing single Host header returns 1
  [Cro::HTTP] ok 68 - Host header was really removed
  [Cro::HTTP] ok 69 - Removing 2 accept-language headers returns 2
  [Cro::HTTP] ok 70 - Headers really removed
  [Cro::HTTP] ok 71 - Removing single header matched by predicate works
  [Cro::HTTP] ok 72 - Header identified by predicate was really removed
  [Cro::HTTP] ok 73 - Removing an exact header returns 1
  [Cro::HTTP] ok 74 - Headers really removed
  [Cro::HTTP] ok 75 - 
  [Cro::HTTP] ok 76 - content-type method returns a Cro::MediaType when there is a content-type header
  [Cro::HTTP] ok 77 - Correct type
  [Cro::HTTP] ok 78 - Correct subtype
  [Cro::HTTP] ok 79 - Correct parameters list
  [Cro::HTTP] ok 80 - content-type returns Nil when no header
  [Cro::HTTP] ok 81 - has-cookie on non-existent cookie returns False
  [Cro::HTTP] ok 82 - cookie-value on non-existent cookie returns Nil
  [Cro::HTTP] ok 83 - cookie-hash returns empty hash when cookies not set
  [Cro::HTTP] ok 84 - Can add cookie
  [Cro::HTTP] ok 85 - has-cookie on added cookie returns True
  [Cro::HTTP] ok 86 - cookie-value on added cookie returns correct value
  [Cro::HTTP] ok 87 - cookie-hash returns correct result
  [Cro::HTTP] ok 88 - Can update cookie
  [Cro::HTTP] ok 89 - has-cookie on updated cookie returns True
  [Cro::HTTP] ok 90 - cookie-value on updated cookie returns correct value
  [Cro::HTTP] ok 91 - Can remove cookie
  [Cro::HTTP] ok 92 - Removed cookie is removed
  [Cro::HTTP] ok 93 - Empty names are not permitted
  [Cro::HTTP] ok 94 - Cookie header looks good
  [Cro::HTTP] ok 95 - lang cookie header should not be parsed for HTTP 1.1
  [Cro::HTTP] ok 96 - lang cookie header should be parsed for HTTP 2
  [Cro::HTTP] ok 97 - Can cope with trailing ; in cookie line
  [Cro::HTTP] ok 98 - Target is set
  [Cro::HTTP] ok 99 - original-target equals target
  [Cro::HTTP] ok 100 - original-path path equals target
  [Cro::HTTP] ok 101 - original-path-segments are equal to target segments
  [Cro::HTTP] ok 102 - target on stripped request changes
  [Cro::HTTP] ok 103 - original-target preserves
  [Cro::HTTP] ok 104 - original-path preserves
  [Cro::HTTP] ok 105 - original-path-segments are preserved
  [Cro::HTTP] ok 106 - target on second stripped request changes
  [Cro::HTTP] ok 107 - original-target preserves
  [Cro::HTTP] ok 108 - original-path preserves
  [Cro::HTTP] ok 109 - original-path-segments are preserved
  [Cro::HTTP] 1..109
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response-parser.rakutest
  [Cro::HTTP] ok 1 - HTTP response parser is a transform
  [Cro::HTTP] ok 2 - HTTP response parser consumes TCP messages
  [Cro::HTTP] ok 3 - HTTP respose parser produces HTTP responses
  [Cro::HTTP] ok 4 - Simple 204 no content response
  [Cro::HTTP] ok 5 - check 1
  [Cro::HTTP] ok 6 - check 2
  [Cro::HTTP] ok 7 - Malformed status line - only version
  [Cro::HTTP] ok 8 - Malformed status line - missing space after status code
  [Cro::HTTP] ok 9 - Simple 204 no content response with empty reason
  [Cro::HTTP] ok 10 - check 1
  [Cro::HTTP] ok 11 - check 2
  [Cro::HTTP] ok 12 - Malformed status line - code is only one digit
  [Cro::HTTP] ok 13 - Malformed status line - code is only two digits
  [Cro::HTTP] ok 14 - Malformed status line - code is four digits
  [Cro::HTTP] ok 15 - Minor version other than 1 OK (1)
  [Cro::HTTP] ok 16 - check 1
  [Cro::HTTP] ok 17 - check 2
  [Cro::HTTP] ok 18 - Minor version other than 1 OK (2)
  [Cro::HTTP] ok 19 - check 1
  [Cro::HTTP] ok 20 - check 2
  [Cro::HTTP] ok 21 - Invalid major version (1)
  [Cro::HTTP] ok 22 - Invalid major version (2)
  [Cro::HTTP] ok 23 - Double-digit minor version
  [Cro::HTTP] ok 24 - All non-controls allowed in reason
  [Cro::HTTP] ok 25 - check 1
  [Cro::HTTP] ok 26 - check 2
  [Cro::HTTP] ok 27 - Control chars in reason (0)
  [Cro::HTTP] ok 28 - Control chars in reason (1)
  [Cro::HTTP] ok 29 - Single simple header
  [Cro::HTTP] ok 30 - check 1
  [Cro::HTTP] ok 31 - check 2
  [Cro::HTTP] ok 32 - check 3
  [Cro::HTTP] ok 33 - check 4
  [Cro::HTTP] ok 34 - check 5
  [Cro::HTTP] ok 35 - Single header without whitespace
  [Cro::HTTP] ok 36 - check 1
  [Cro::HTTP] ok 37 - check 2
  [Cro::HTTP] ok 38 - check 3
  [Cro::HTTP] ok 39 - check 4
  [Cro::HTTP] ok 40 - check 5
  [Cro::HTTP] ok 41 - Single header with trailing whitespace
  [Cro::HTTP] ok 42 - check 1
  [Cro::HTTP] ok 43 - check 2
  [Cro::HTTP] ok 44 - check 3
  [Cro::HTTP] ok 45 - check 4
  [Cro::HTTP] ok 46 - check 5
  [Cro::HTTP] ok 47 - Host header with tab before and after value
  [Cro::HTTP] ok 48 - check 1
  [Cro::HTTP] ok 49 - check 2
  [Cro::HTTP] ok 50 - check 3
  [Cro::HTTP] ok 51 - check 4
  [Cro::HTTP] ok 52 - check 5
  [Cro::HTTP] ok 53 - Header with insane but actually totally legit name
  [Cro::HTTP] ok 54 - check 1
  [Cro::HTTP] ok 55 - check 2
  [Cro::HTTP] ok 56 - check 3
  [Cro::HTTP] ok 57 - check 4
  [Cro::HTTP] ok 58 - check 5
  [Cro::HTTP] ok 59 - Not allowed " in header name
  [Cro::HTTP] ok 60 - Not allowed ( in header name
  [Cro::HTTP] ok 61 - Not allowed ) in header name
  [Cro::HTTP] ok 62 - Not allowed [ in header name
  [Cro::HTTP] ok 63 - Not allowed ] in header name
  [Cro::HTTP] ok 64 - Not allowed { in header name
  [Cro::HTTP] ok 65 - Not allowed } in header name
  [Cro::HTTP] ok 66 - Not allowed @ in header name
  [Cro::HTTP] ok 67 - Not allowed \ in header name
  [Cro::HTTP] ok 68 - Not allowed / in header name
  [Cro::HTTP] ok 69 - Not allowed < in header name
  [Cro::HTTP] ok 70 - Not allowed > in header name
  [Cro::HTTP] ok 71 - Not allowed , in header name
  [Cro::HTTP] ok 72 - Not allowed ; in header name
  [Cro::HTTP] ok 73 - Header field value can be any printable char including latin-1 range
  [Cro::HTTP] ok 74 - check 1
  [Cro::HTTP] ok 75 - check 2
  [Cro::HTTP] ok 76 - check 3
  [Cro::HTTP] ok 77 - check 4
  [Cro::HTTP] ok 78 - check 5
  [Cro::HTTP] ok 79 - check 6
  [Cro::HTTP] ok 80 - Single header with whitespace in value
  [Cro::HTTP] ok 81 - check 1
  [Cro::HTTP] ok 82 - check 2
  [Cro::HTTP] ok 83 - check 3
  [Cro::HTTP] ok 84 - check 4
  [Cro::HTTP] ok 85 - check 5
  [Cro::HTTP] ok 86 - Response with multiple headers and content-length body (example from RFC)
  [Cro::HTTP] ok 87 - check 1
  [Cro::HTTP] ok 88 - check 2
  [Cro::HTTP] ok 89 - check 3
  [Cro::HTTP] ok 90 - check 4
  [Cro::HTTP] ok 91 - check 5
  [Cro::HTTP] ok 92 - check 6
  [Cro::HTTP] ok 93 - check 7
  [Cro::HTTP] ok 94 - check 8
  [Cro::HTTP] ok 95 - check 9
  [Cro::HTTP] ok 96 - check 10
  [Cro::HTTP] ok 97 - check 11
  [Cro::HTTP] ok 98 - check 12
  [Cro::HTTP] ok 99 - check 13
  [Cro::HTTP] ok 100 - check 14
  [Cro::HTTP] ok 101 - check 15
  [Cro::HTTP] ok 102 - check 16
  [Cro::HTTP] ok 103 - check 17
  [Cro::HTTP] ok 104 - check 18
  [Cro::HTTP] ok 105 - check 19
  [Cro::HTTP] ok 106 - check 20
  [Cro::HTTP] ok 107 - Response with body terminated by close of connection
  [Cro::HTTP] ok 108 - check 1
  [Cro::HTTP] ok 109 - check 2
  [Cro::HTTP] ok 110 - check 3
  [Cro::HTTP] ok 111 - check 4
  [Cro::HTTP] ok 112 - Connection close with incomplete body throws
  [Cro::HTTP] ok 113 - check 1
  [Cro::HTTP] ok 114 - check 2
  [Cro::HTTP] ok 115 - check 3
  [Cro::HTTP] ok 116 - check 4
  [Cro::HTTP] ok 117 - Response with chunked encoding
  [Cro::HTTP] ok 118 - check 1
  [Cro::HTTP] ok 119 - check 2
  [Cro::HTTP] ok 120 - check 3
  [Cro::HTTP] ok 121 - check 4
  [Cro::HTTP] ok 122 - A text/whatever response has Str .body
  [Cro::HTTP] ok 123 - check 1
  [Cro::HTTP] ok 124 - A unknown/foo response has Blob .body
  [Cro::HTTP] ok 125 - check 1
  [Cro::HTTP] ok 126 - charset in content-type is respected by body-text
  [Cro::HTTP] ok 127 - check 1
  [Cro::HTTP] ok 128 - check 2
  [Cro::HTTP] ok 129 - check 3
  [Cro::HTTP] ok 130 - check 4
  [Cro::HTTP] ok 131 - A UTF-8 BOM is respected and stripped
  [Cro::HTTP] ok 132 - check 1
  [Cro::HTTP] ok 133 - check 2
  [Cro::HTTP] ok 134 - check 3
  [Cro::HTTP] ok 135 - check 4
  [Cro::HTTP] ok 136 - A UTF-16 LE BOM is respected and stripped
  [Cro::HTTP] ok 137 - check 1
  [Cro::HTTP] ok 138 - check 2
  [Cro::HTTP] ok 139 - check 3
  [Cro::HTTP] ok 140 - check 4
  [Cro::HTTP] ok 141 - A UTF-16 BE BOM is respected and stripped
  [Cro::HTTP] ok 142 - check 1
  [Cro::HTTP] ok 143 - check 2
  [Cro::HTTP] ok 144 - check 3
  [Cro::HTTP] ok 145 - check 4
  [Cro::HTTP] ok 146 - With not other indications, and it utf-8 fails, decode as latin-1
  [Cro::HTTP] ok 147 - check 1
  [Cro::HTTP] ok 148 - check 2
  [Cro::HTTP] ok 149 - check 3
  [Cro::HTTP] ok 150 - check 4
  [Cro::HTTP] ok 151 - An application/json response decodes JSON body
  [Cro::HTTP] ok 152 - .body of application/json with object gives Hash
  [Cro::HTTP] ok 153 - JSON was correctly decoded
  [Cro::HTTP] ok 154 - A media type with the +json suffix decodes JSON body
  [Cro::HTTP] ok 155 - .body of application/vnd.my-org+json with object gives Hash
  [Cro::HTTP] ok 156 - JSON was correctly decoded
  [Cro::HTTP] 1..156
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response-serializer.rakutest
  [Cro::HTTP] ok 1 - Basic 204 status response serialized correctly
  [Cro::HTTP] ok 2 - 200 response with body readily available emits Content-length
  [Cro::HTTP] ok 3 - 200 response with streaming body does chunked encoding
  [Cro::HTTP] ok 4 - Chunked encoding not messed up by empty blobs
  [Cro::HTTP] ok 5 - application/json encodes Hash as JSON
  [Cro::HTTP] ok 6 - application/json encodes Array as JSON
  [Cro::HTTP] ok 7 - application/vnd.foobar+json encodes Hash as JSON
  [Cro::HTTP] 1..7
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response.rakutest
  [Cro::HTTP] ok 1 - Unconfigured HTTP response is HTTP/1.1 and 204 status
  [Cro::HTTP] ok 2 - Setting status in constructor includes it in the response
  [Cro::HTTP] ok 3 - Setting status and version in constructor includes it in the response
  [Cro::HTTP] ok 4 - Setting status and version attributes includes them in the response
  [Cro::HTTP] ok 5 - Status of 10 is invalid
  [Cro::HTTP] ok 6 - Status of 99 is invalid
  [Cro::HTTP] ok 7 - Status of 1000 is invalid
  [Cro::HTTP] ok 8 - Status of 4004 is invalid
  [Cro::HTTP] ok 9 - Headers are included in the response
  [Cro::HTTP] ok 10 - has-header returns True on header we have
  [Cro::HTTP] ok 11 - has-header is not case-sensitive (1)
  [Cro::HTTP] ok 12 - has-header is not case-sensitive (2)
  [Cro::HTTP] ok 13 - has-header returns False on header we do not have
  [Cro::HTTP] ok 14 - header method fetches a header
  [Cro::HTTP] ok 15 - header method is not case sensitive (1)
  [Cro::HTTP] ok 16 - header method is not case sensitive (2)
  [Cro::HTTP] ok 17 - header method returns Nil on header we do not have
  [Cro::HTTP] ok 18 - Refuses to add response header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 19 - Refuses to add response header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 20 - Refuses to add response header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 21 - Refuses to add response header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 22 - Refuses to add response header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 23 - Refuses to add response header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 24 - Refuses to add response header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 25 - Refuses to add response header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 26 - Refuses to add response header with illegal name containing " (single-arg)
  [Cro::HTTP] ok 27 - Refuses to add response header with illegal name containing ( (single-arg)
  [Cro::HTTP] ok 28 - Refuses to add response header with illegal name containing ) (single-arg)
  [Cro::HTTP] ok 29 - Refuses to add response header with illegal name containing [ (single-arg)
  [Cro::HTTP] ok 30 - Refuses to add response header with illegal name containing ] (single-arg)
  [Cro::HTTP] ok 31 - Refuses to add response header with illegal name containing { (single-arg)
  [Cro::HTTP] ok 32 - Refuses to add response header with illegal name containing } (single-arg)
  [Cro::HTTP] ok 33 - Refuses to add response header with illegal name containing @ (single-arg)
  [Cro::HTTP] ok 34 - Refuses to add response header with illegal name containing \ (single-arg)
  [Cro::HTTP] ok 35 - Refuses to add response header with illegal name containing / (single-arg)
  [Cro::HTTP] ok 36 - Refuses to add response header with illegal name containing < (single-arg)
  [Cro::HTTP] ok 37 - Refuses to add response header with illegal name containing > (single-arg)
  [Cro::HTTP] ok 38 - Refuses to add response header with illegal name containing , (single-arg)
  [Cro::HTTP] ok 39 - Refuses to add response header with illegal name containing ; (single-arg)
  [Cro::HTTP] ok 40 - Refuses to add response header with illegal name containing " (two-arg)
  [Cro::HTTP] ok 41 - Refuses to add response header with illegal name containing ( (two-arg)
  [Cro::HTTP] ok 42 - Refuses to add response header with illegal name containing ) (two-arg)
  [Cro::HTTP] ok 43 - Refuses to add response header with illegal name containing [ (two-arg)
  [Cro::HTTP] ok 44 - Refuses to add response header with illegal name containing ] (two-arg)
  [Cro::HTTP] ok 45 - Refuses to add response header with illegal name containing { (two-arg)
  [Cro::HTTP] ok 46 - Refuses to add response header with illegal name containing } (two-arg)
  [Cro::HTTP] ok 47 - Refuses to add response header with illegal name containing @ (two-arg)
  [Cro::HTTP] ok 48 - Refuses to add response header with illegal name containing \ (two-arg)
  [Cro::HTTP] ok 49 - Refuses to add response header with illegal name containing / (two-arg)
  [Cro::HTTP] ok 50 - Refuses to add response header with illegal name containing < (two-arg)
  [Cro::HTTP] ok 51 - Refuses to add response header with illegal name containing > (two-arg)
  [Cro::HTTP] ok 52 - Refuses to add response header with illegal name containing , (two-arg)
  [Cro::HTTP] ok 53 - Refuses to add response header with illegal name containing ; (two-arg)
  [Cro::HTTP] ok 54 - Utterly crazy but valid header can be added (single-arg)
  [Cro::HTTP] ok 55 - Utterly crazy but valid header can be added (two-arg)
  [Cro::HTTP] ok 56 - Can set body
  [Cro::HTTP] ok 57 - Default status code when body set is 200, not 204
  [Cro::HTTP] ok 58 - Can set correct cookie
  [Cro::HTTP] ok 59 - Cookie header is set
  [Cro::HTTP] ok 60 - Cookie cannot be set twice
  [Cro::HTTP] ok 61 - Cookie header is set for two cookies
  [Cro::HTTP] ok 62 - Cookie header is set for a complex cookie
  [Cro::HTTP] ok 63 - Cookies are returned from .cookies call
  [Cro::HTTP] ok 64 - All cookies are returned
  [Cro::HTTP] 1..64
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router-named-urls.t
  [Cro::HTTP] ok 1 - Escaped named param
  [Cro::HTTP] ok 2 - Escaped positional
  [Cro::HTTP] ok 3 - Non-path related parameters were not counted
  [Cro::HTTP] ok 4 - Auth parameter is ignored when creating uri
  [Cro::HTTP] ok 5 - Parameter with type that does Auth is ignored when creating uri
  [Cro::HTTP] ok 6 - GET option to multi method named endpoint
  [Cro::HTTP] ok 7 - POST option to multi method named endpoint
  [Cro::HTTP] ok 8 - PUT option to multi method named endpoint
  [Cro::HTTP] ok 9 - DELETE option to multi method named endpoint
  [Cro::HTTP] ok 10 - No named urls
  [Cro::HTTP] ok 11 - No named urls with a prefix
  [Cro::HTTP] ok 12 - Basic call of a generator by a qualified name is correct
  [Cro::HTTP] # Subtest: did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::DuplicateLinkName)
  [Cro::HTTP]     ok 3 - .message matches Conflicting link name: home
  [Cro::HTTP] ok 13 - did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP] # Subtest: did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::DuplicateLinkName)
  [Cro::HTTP]     ok 3 - .message matches Conflicting link name: main.home
  [Cro::HTTP] ok 14 - did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP] ok 15 - URL is generated correctly
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Not enough arguments
  [Cro::HTTP] ok 16 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Extraneous arguments
  [Cro::HTTP] ok 17 - did we throws-like Exception?
  [Cro::HTTP] ok 18 - 
  [Cro::HTTP] ok 19 - 
  [Cro::HTTP] ok 20 - 
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Extraneous arguments
  [Cro::HTTP] ok 21 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Extraneous named arguments: c.
  [Cro::HTTP] ok 22 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Extraneous named arguments: c.
  [Cro::HTTP] ok 23 - did we throws-like Exception?
  [Cro::HTTP] ok 24 - 
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Missing named arguments: b.
  [Cro::HTTP] ok 25 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Missing named arguments: a.
  [Cro::HTTP] ok 26 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Extraneous arguments
  [Cro::HTTP] ok 27 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Missing named arguments: a, b. Extraneous named arguments: c.
  [Cro::HTTP] ok 28 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Missing named arguments: b. Extraneous named arguments: c.
  [Cro::HTTP] ok 29 - did we throws-like Exception?
  [Cro::HTTP] ok 30 - 
  [Cro::HTTP] ok 31 - 
  [Cro::HTTP] ok 32 - Splat with no args at all
  [Cro::HTTP] ok 33 - Splat with no named args
  [Cro::HTTP] ok 34 - Splat with no pos args
  [Cro::HTTP] ok 35 - Splat with both types of args
  [Cro::HTTP] ok 36 - Conflict check is per-route block 1
  [Cro::HTTP] ok 37 - Conflict check is per-route block 2
  [Cro::HTTP] ok 38 - Conflict check is by route name
  [Cro::HTTP] # Subtest: did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::DuplicateLinkName)
  [Cro::HTTP]     ok 3 - .message matches Conflicting link name: foo.home
  [Cro::HTTP] ok 39 - did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP] 1..39
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router-plugin.rakutest
  [Cro::HTTP] # Subtest: router-plugin-add-config throws outside of route block
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInRouteBlock)
  [Cro::HTTP]     ok 3 - .what matches add-message
  [Cro::HTTP] ok 1 - router-plugin-add-config throws outside of route block
  [Cro::HTTP] ok 2 - Can add plugin configuration to the route block
  [Cro::HTTP] ok 3 - Got expected error from add-message
  [Cro::HTTP] # Subtest: Access to configuration with single level route block
  [Cro::HTTP]     ok 1 - Got a response
  [Cro::HTTP]     ok 2 - Local configuration was available in route handler
  [Cro::HTTP]     ok 3 - Got a response
  [Cro::HTTP]     ok 4 - All configuration was available in route handler
  [Cro::HTTP]     1..4
  [Cro::HTTP] ok 4 - Access to configuration with single level route block
  [Cro::HTTP] # Subtest: Access to configuration with include
  [Cro::HTTP]     ok 1 - Got a response
  [Cro::HTTP]     ok 2 - Local configuration in included route handler not affected by outer
  [Cro::HTTP]     ok 3 - Got a response
  [Cro::HTTP]     ok 4 - Outer configuration in included router handler available if requested
  [Cro::HTTP]     ok 5 - Got a response
  [Cro::HTTP]     ok 6 - Inner route block configuration does not leak into outer local configuration
  [Cro::HTTP]     ok 7 - Got a response
  [Cro::HTTP]     ok 8 - Inner route block configuration does not leak into outer configuration
  [Cro::HTTP]     1..8
  [Cro::HTTP] ok 5 - Access to configuration with include
  [Cro::HTTP] # Subtest: Access to configuration in before block
  [Cro::HTTP]     ok 1 - Got a response
  [Cro::HTTP]     ok 2 - Got 200 when before middleware ran and did not produce response
  [Cro::HTTP]     ok 3 - Got a response
  [Cro::HTTP]     ok 4 - Got 404 when before middleware ran and changed response
  [Cro::HTTP]     1..4
  [Cro::HTTP] ok 6 - Access to configuration in before block
  [Cro::HTTP] # Subtest: Access to configuration in after block
  [Cro::HTTP]     ok 1 - Got a response
  [Cro::HTTP]     ok 2 - Got 200 when after middleware ran and did not change response
  [Cro::HTTP]     ok 3 - Got a response
  [Cro::HTTP]     ok 4 - Got 404 when after middleware ran and changed response
  [Cro::HTTP]     1..4
  [Cro::HTTP] ok 7 - Access to configuration in after block
  [Cro::HTTP] 1..7
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router.rakutest
  [Cro::HTTP] ok 1 - Route block with no routes gives back a Cro::Transform
  [Cro::HTTP] ok 2 - Empty route set gives a response
  [Cro::HTTP] ok 3 - Status code from empty route set is 404
  [Cro::HTTP] ok 4 - No matching route gets a HTTP response
  [Cro::HTTP] ok 5 - Status code uri is invalid is 400
  [Cro::HTTP] # Subtest: Can only use request term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches request
  [Cro::HTTP] ok 6 - Can only use request term inside of a handler
  [Cro::HTTP] # Subtest: Can only use response term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches response
  [Cro::HTTP] ok 7 - Can only use response term inside of a handler
  [Cro::HTTP] # Subtest: Can only use created term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches created
  [Cro::HTTP] ok 8 - Can only use created term inside of a handler
  [Cro::HTTP] # Subtest: Can only use not-found term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches not-found
  [Cro::HTTP] ok 9 - Can only use not-found term inside of a handler
  [Cro::HTTP] # Subtest: Can only use forbidden term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches forbidden
  [Cro::HTTP] ok 10 - Can only use forbidden term inside of a handler
  [Cro::HTTP] # Subtest: Can only use redirect term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches redirected
  [Cro::HTTP] ok 11 - Can only use redirect term inside of a handler
  [Cro::HTTP] # Subtest: Can only use conflict term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches conflict
  [Cro::HTTP] ok 12 - Can only use conflict term inside of a handler
  [Cro::HTTP] # Subtest: Can only use i'm-a-teapot term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches i'm-a-teapot
  [Cro::HTTP] ok 13 - Can only use i'm-a-teapot term inside of a handler
  [Cro::HTTP] # Subtest: Can only use bad-request term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches bad-request
  [Cro::HTTP] ok 14 - Can only use bad-request term inside of a handler
  [Cro::HTTP] ok 15 - Route block with routes gives back a Cro::Transform
  [Cro::HTTP] ok 16 - Route set routes / correctly
  [Cro::HTTP] ok 17 - Got 200 response
  [Cro::HTTP] ok 18 - Got expected header
  [Cro::HTTP] ok 19 - Got expected body
  [Cro::HTTP] ok 20 - Route set routes /about correctly
  [Cro::HTTP] ok 21 - Got 200 response
  [Cro::HTTP] ok 22 - Got expected header
  [Cro::HTTP] ok 23 - Got expected body
  [Cro::HTTP] ok 24 - Route set routes /company/careers correctly
  [Cro::HTTP] ok 25 - Got 200 response
  [Cro::HTTP] ok 26 - Got expected header
  [Cro::HTTP] ok 27 - Got expected body
  [Cro::HTTP] ok 28 - No matching route gets a HTTP response
  [Cro::HTTP] ok 29 - Status code when no matching route is 404
  [Cro::HTTP] ok 30 - Route set routes GET
  [Cro::HTTP] ok 31 - Got 200 response
  [Cro::HTTP] ok 32 - Got expected header
  [Cro::HTTP] ok 33 - Got expected body
  [Cro::HTTP] ok 34 - Route set routes POST
  [Cro::HTTP] ok 35 - Got 201 response
  [Cro::HTTP] ok 36 - Got expected header
  [Cro::HTTP] ok 37 - Got expected body
  [Cro::HTTP] ok 38 - Route set routes PUT
  [Cro::HTTP] ok 39 - Got 204 response
  [Cro::HTTP] ok 40 - Route set routes DELETE
  [Cro::HTTP] ok 41 - Got 200 response
  [Cro::HTTP] ok 42 - Got expected header
  [Cro::HTTP] ok 43 - Got expected body
  [Cro::HTTP] ok 44 - Route set routes PATCH
  [Cro::HTTP] ok 45 - Got 200 response
  [Cro::HTTP] ok 46 - Got expected header
  [Cro::HTTP] ok 47 - Got expected body
  [Cro::HTTP] ok 48 - Mu variable at end handled correctly
  [Cro::HTTP] ok 49 - Any variable at end handled correctly
  [Cro::HTTP] ok 50 - Str variable at end handled correctly
  [Cro::HTTP] ok 51 - Longest literal prefix wins
  [Cro::HTTP] ok 52 - Str variable in middle of literals handled correctly
  [Cro::HTTP] ok 53 - Having both Str and Int variables handled correctly
  [Cro::HTTP] ok 54 - Int may have a sign
  [Cro::HTTP] ok 55 - Slurpy handled correctly (empty case)
  [Cro::HTTP] ok 56 - Slurpy handled correctly (one segment case)
  [Cro::HTTP] ok 57 - Slurpy handled correctly (two segment case)
  [Cro::HTTP] ok 58 - Slurpy handled correctly (three segment case)
  [Cro::HTTP] ok 59 - Optional segment handled correctly (no argument)
  [Cro::HTTP] ok 60 - Optional segment handled correctly (argument)
  [Cro::HTTP] ok 61 - Two optional segments handled correctly (none passed)
  [Cro::HTTP] ok 62 - Two optional segments handled correctly (one passed)
  [Cro::HTTP] ok 63 - Two optional segments handled correctly (two passed)
  [Cro::HTTP] ok 64 - Two query string parameters, neither passed (explicit is query)
  [Cro::HTTP] ok 65 - Two query string parameters, first passed (explicit is query)
  [Cro::HTTP] ok 66 - Two query string parameters, second passed (explicit is query)
  [Cro::HTTP] ok 67 - Two query string parameters, both passed (explicit is query)
  [Cro::HTTP] ok 68 - Two header parameters, one for a non-present header
  [Cro::HTTP] ok 69 - Two header parameters, both present
  [Cro::HTTP] ok 70 - Header parameters are case-insensitive
  [Cro::HTTP] ok 71 - Required query parameter selects correct route (1)
  [Cro::HTTP] ok 72 - Required query parameter selects correct route (2)
  [Cro::HTTP] ok 73 - First winning route with required query items wins
  [Cro::HTTP] ok 74 - Route with named array of query parameters works
  [Cro::HTTP] ok 75 - Route with named array of headers works
  [Cro::HTTP] ok 76 - Correct route picked when there are required headers
  [Cro::HTTP] ok 77 - Route with named array of headers works
  [Cro::HTTP] ok 78 - Route with named hash of headers works
  [Cro::HTTP] ok 79 - Route with required Int named arg for query parameter works
  [Cro::HTTP] ok 80 - Route with optional Int named arg for query parameter works when passed
  [Cro::HTTP] ok 81 - Route with optional Int named arg for query parameter works when not passed
  [Cro::HTTP] ok 82 - Route with optional UInt named arg for query parameter works when passed
  [Cro::HTTP] ok 83 - Route with optional UInt named arg for query parameter doesn't match negative values
  [Cro::HTTP] ok 84 - Route for positional int8 works
  [Cro::HTTP] ok 85 - 
  [Cro::HTTP] ok 86 - Lower border for positional int8 route works
  [Cro::HTTP] ok 87 - 
  [Cro::HTTP] ok 88 - Upper border for positional int8 route works
  [Cro::HTTP] ok 89 - Route for positional uint8 works
  [Cro::HTTP] ok 90 - 
  [Cro::HTTP] ok 91 - Lower border for positional uint8 route works
  [Cro::HTTP] ok 92 - 
  [Cro::HTTP] ok 93 - Upper border for positional uint8 route works
  [Cro::HTTP] ok 94 - Route for positional int16 works
  [Cro::HTTP] ok 95 - 
  [Cro::HTTP] ok 96 - Lower border for positional int16 route works
  [Cro::HTTP] ok 97 - 
  [Cro::HTTP] ok 98 - Upper border for positional int16 route works
  [Cro::HTTP] ok 99 - Route for positional uint16 works
  [Cro::HTTP] ok 100 - 
  [Cro::HTTP] ok 101 - Lower border for positional uint16 route works
  [Cro::HTTP] ok 102 - 
  [Cro::HTTP] ok 103 - Upper border for positional uint16 route works
  [Cro::HTTP] ok 104 - Route for positional int32 works
  [Cro::HTTP] ok 105 - 
  [Cro::HTTP] ok 106 - Lower border for positional int32 route works
  [Cro::HTTP] ok 107 - 
  [Cro::HTTP] ok 108 - Upper border for positional int32 route works
  [Cro::HTTP] ok 109 - Route for positional  uint32 works
  [Cro::HTTP] ok 110 - 
  [Cro::HTTP] ok 111 - Lower border for positional uint32 route works
  [Cro::HTTP] ok 112 - 
  [Cro::HTTP] ok 113 - Upper border for positional uint32 route works
  [Cro::HTTP] ok 114 - Route for positional int64 works
  [Cro::HTTP] ok 115 - 
  [Cro::HTTP] ok 116 - Lower border for positional int64 route works
  [Cro::HTTP] ok 117 - 
  [Cro::HTTP] ok 118 - Upper border for positional int64 route works
  [Cro::HTTP] ok 119 - Route for positional uint64 works
  [Cro::HTTP] ok 120 - 
  [Cro::HTTP] ok 121 - Lower border for positional uint64 route works
  [Cro::HTTP] ok 122 - 
  [Cro::HTTP] ok 123 - Upper border for positional uint64 route works
  [Cro::HTTP] ok 124 - Route with optional named int8 works
  [Cro::HTTP] ok 125 - Route for named int8 works
  [Cro::HTTP] ok 126 - 
  [Cro::HTTP] ok 127 - Lower border for named int8 route works
  [Cro::HTTP] ok 128 - 
  [Cro::HTTP] ok 129 - Upper border for named int8 route works
  [Cro::HTTP] ok 130 - Route with optional named uint8 works
  [Cro::HTTP] ok 131 - Route for named uint8 works
  [Cro::HTTP] ok 132 - 
  [Cro::HTTP] ok 133 - Lower border for named uint8 route works
  [Cro::HTTP] ok 134 - 
  [Cro::HTTP] ok 135 - Upper border for named uint8 route works
  [Cro::HTTP] ok 136 - Route with optional named int16 works
  [Cro::HTTP] ok 137 - Route for named int16 works
  [Cro::HTTP] ok 138 - 
  [Cro::HTTP] ok 139 - Lower border for named int16 route works
  [Cro::HTTP] ok 140 - 
  [Cro::HTTP] ok 141 - Upper border for named int16 route works
  [Cro::HTTP] ok 142 - Route with optional named uint16 works
  [Cro::HTTP] ok 143 - Route for named uint16 works
  [Cro::HTTP] ok 144 - 
  [Cro::HTTP] ok 145 - Lower border for named uint16 route works
  [Cro::HTTP] ok 146 - 
  [Cro::HTTP] ok 147 - Upper border for named uint16 route works
  [Cro::HTTP] ok 148 - Route with optional named int32 works
  [Cro::HTTP] ok 149 - Route for named int32 works
  [Cro::HTTP] ok 150 - 
  [Cro::HTTP] ok 151 - Lower border for named int32 route works
  [Cro::HTTP] ok 152 - 
  [Cro::HTTP] ok 153 - Upper border for named int32 route works
  [Cro::HTTP] ok 154 - Route with optional named uint32 works
  [Cro::HTTP] ok 155 - Route for named uint32 works
  [Cro::HTTP] ok 156 - 
  [Cro::HTTP] ok 157 - Lower border for named uint32 route works
  [Cro::HTTP] ok 158 - 
  [Cro::HTTP] ok 159 - Upper border for named uint32 route works
  [Cro::HTTP] ok 160 - Route with optional named int64 works
  [Cro::HTTP] ok 161 - Route for named int64 works
  [Cro::HTTP] ok 162 - 
  [Cro::HTTP] ok 163 - Lower border for named int64 route works
  [Cro::HTTP] ok 164 - 
  [Cro::HTTP] ok 165 - Upper border for named int64 route works
  [Cro::HTTP] ok 166 - Route with optional named uint64 works
  [Cro::HTTP] ok 167 - Route for named uint64 works
  [Cro::HTTP] ok 168 - 
  [Cro::HTTP] ok 169 - Lower border for named uint64 route works
  [Cro::HTTP] ok 170 - 
  [Cro::HTTP] ok 171 - Upper border for named uint64 route works
  [Cro::HTTP] ok 172 - Segment constrained by Str-base subset type matches when it should
  [Cro::HTTP] ok 173 - Segment constrained by Int-base subset type matches when it should
  [Cro::HTTP] ok 174 - Segment constrained by where clause matches when it should
  [Cro::HTTP] ok 175 - Segment of type Int constrained by where clause matches when it should
  [Cro::HTTP] ok 176 - Slurpy segment with where clause matches when it could
  [Cro::HTTP] ok 177 - Non-matching segment gives 404 error (subset, Str)
  [Cro::HTTP] ok 178 - Non-matching segment gives 404 error (subset, Int)
  [Cro::HTTP] ok 179 - Non-matching segment gives 404 error (where, Str)
  [Cro::HTTP] ok 180 - Non-matching segment gives 404 error (where, Int)
  [Cro::HTTP] ok 181 - Non-matching where clause on slurpy gives 404 error
  [Cro::HTTP] ok 182 - Required unpack constrained by Str-base subset type works
  [Cro::HTTP] ok 183 - Optional unpack constrained by Str-base subset type works (provided)
  [Cro::HTTP] ok 184 - Optional unpack constrained by Str-base subset type works (not provided)
  [Cro::HTTP] ok 185 - Required unpack constrained by Int-base subset type works
  [Cro::HTTP] ok 186 - Optional unpack constrained by Int-base subset type works (provided)
  [Cro::HTTP] ok 187 - Optional unpack constrained by Int-base subset type works (not provided)
  [Cro::HTTP] ok 188 - Required unpack untyped with where constraint works
  [Cro::HTTP] ok 189 - Required unpack of type Int with where constraint works
  [Cro::HTTP] ok 190 - Missing unpack gives 400 error (subset, Str)
  [Cro::HTTP] ok 191 - Non-matching unpack gives 400 error (subset, Str)
  [Cro::HTTP] ok 192 - Non-matching optional unpack gives 400 error (subset, Str)
  [Cro::HTTP] ok 193 - Missing unpack gives 400 error (subset, Int)
  [Cro::HTTP] ok 194 - Non-matching unpack gives 400 error (subset, Int)
  [Cro::HTTP] ok 195 - Non-matching optional unpack gives 400 error (subset, Int)
  [Cro::HTTP] ok 196 - Missing unpack gives 400 error (where, Str)
  [Cro::HTTP] ok 197 - Non-matching unpack gives 400 error (where, Str)
  [Cro::HTTP] ok 198 - Missing unpack gives 400 error (where, Int)
  [Cro::HTTP] ok 199 - Non-matching unpack gives 400 error (where, Int)
  [Cro::HTTP] ok 200 - URL that matches on segments but not method is 405
  [Cro::HTTP] ok 201 - URL that matches on segments but not method is 405
  [Cro::HTTP] ok 202 - URL that matches on segments but not method is 405
  [Cro::HTTP] ok 203 - Simple binary content response has 200 status
  [Cro::HTTP] ok 204 - Correct content-type set
  [Cro::HTTP] ok 205 - Got expected body
  [Cro::HTTP] ok 206 - Simple text content response has 200 status
  [Cro::HTTP] ok 207 - Correct content-type set including charset
  [Cro::HTTP] ok 208 - Got expected body
  [Cro::HTTP] ok 209 - Simple JSON content response has 200 status
  [Cro::HTTP] ok 210 - Got two Link headers
  [Cro::HTTP] ok 211 - Got expected link header value (1)
  [Cro::HTTP] ok 212 - Got expected link header value (2)
  [Cro::HTTP] ok 213 - Correct content-type set including charset
  [Cro::HTTP] ok 214 - Got expected body
  [Cro::HTTP] ok 215 - created + content response has 201 status
  [Cro::HTTP] ok 216 - Location header is set
  [Cro::HTTP] ok 217 - Correct content-type set including charset
  [Cro::HTTP] ok 218 - Got expected body
  [Cro::HTTP] ok 219 - created response has 201 status
  [Cro::HTTP] ok 220 - Location header is set
  [Cro::HTTP] ok 221 - Correct content-type set including charset
  [Cro::HTTP] ok 222 - Got expected body
  [Cro::HTTP] ok 223 - Str content with :enc<ISO-8859-1> has 200 response
  [Cro::HTTP] ok 224 - Correct content-type with charset=ISO-8859-1
  [Cro::HTTP] ok 225 - Got expected body
  [Cro::HTTP] ok 226 - Error routine not found sanity (1) - status
  [Cro::HTTP] ok 227 - Error routine not found sanity (1) - content type
  [Cro::HTTP] ok 228 - Error routine not found sanity (1) - body
  [Cro::HTTP] ok 229 - Error routine not found (1) - status
  [Cro::HTTP] ok 230 - Error routine not found (1) - content type
  [Cro::HTTP] ok 231 - Error routine not found (1) - body
  [Cro::HTTP] ok 232 - Error routine not found sanity (2) - status
  [Cro::HTTP] ok 233 - Error routine not found sanity (2) - content type
  [Cro::HTTP] ok 234 - Error routine not found sanity (2) - body
  [Cro::HTTP] ok 235 - Error routine not found (2) - status
  [Cro::HTTP] ok 236 - Error routine not found (2) - content type
  [Cro::HTTP] ok 237 - Error routine not found (2) - body
  [Cro::HTTP] ok 238 - Error routine bad request sanity (1) - status
  [Cro::HTTP] ok 239 - Error routine bad request sanity (1) - content type
  [Cro::HTTP] ok 240 - Error routine bad request sanity (1) - body
  [Cro::HTTP] ok 241 - Error routine bad request (1) - status
  [Cro::HTTP] ok 242 - Error routine bad request (1) - content type
  [Cro::HTTP] ok 243 - Error routine bad request (1) - body
  [Cro::HTTP] ok 244 - Error routine bad request sanity (2) - status
  [Cro::HTTP] ok 245 - Error routine bad request sanity (2) - content type
  [Cro::HTTP] ok 246 - Error routine bad request sanity (2) - body
  [Cro::HTTP] ok 247 - Error routine bad request (2) - status
  [Cro::HTTP] ok 248 - Error routine bad request (2) - content type
  [Cro::HTTP] ok 249 - Error routine bad request (2) - body
  [Cro::HTTP] ok 250 - Error routine forbidden sanity (1) - status
  [Cro::HTTP] ok 251 - Error routine forbidden sanity (1) - content type
  [Cro::HTTP] ok 252 - Error routine forbidden sanity (1) - body
  [Cro::HTTP] ok 253 - Error routine forbidden (1) - status
  [Cro::HTTP] ok 254 - Error routine forbidden (1) - content type
  [Cro::HTTP] ok 255 - Error routine forbidden (1) - body
  [Cro::HTTP] ok 256 - Error routine forbidden sanity (2) - status
  [Cro::HTTP] ok 257 - Error routine forbidden sanity (2) - content type
  [Cro::HTTP] ok 258 - Error routine forbidden sanity (2) - body
  [Cro::HTTP] ok 259 - Error routine forbidden (2) - status
  [Cro::HTTP] ok 260 - Error routine forbidden (2) - content type
  [Cro::HTTP] ok 261 - Error routine forbidden (2) - body
  [Cro::HTTP] ok 262 - Error routine conflict sanity (1) - status
  [Cro::HTTP] ok 263 - Error routine conflict sanity (1) - content type
  [Cro::HTTP] ok 264 - Error routine conflict sanity (1) - body
  [Cro::HTTP] ok 265 - Error routine conflict (1) - status
  [Cro::HTTP] ok 266 - Error routine conflict (1) - content type
  [Cro::HTTP] ok 267 - Error routine conflict (1) - body
  [Cro::HTTP] ok 268 - Error routine conflict sanity (2) - status
  [Cro::HTTP] ok 269 - Error routine conflict sanity (2) - content type
  [Cro::HTTP] ok 270 - Error routine conflict sanity (2) - body
  [Cro::HTTP] ok 271 - Error routine conflict (2) - status
  [Cro::HTTP] ok 272 - Error routine conflict (2) - content type
  [Cro::HTTP] ok 273 - Error routine conflict (2) - body
  [Cro::HTTP] ok 274 - Error routine i'm-a-teapot sanity (1) - status
  [Cro::HTTP] ok 275 - Error routine i'm-a-teapot sanity (1) - content type
  [Cro::HTTP] ok 276 - Error routine i'm-a-teapot sanity (1) - body
  [Cro::HTTP] ok 277 - Error routine i'm-a-teapot (1) - status
  [Cro::HTTP] ok 278 - Error routine i'm-a-teapot (1) - content type
  [Cro::HTTP] ok 279 - Error routine i'm-a-teapot (1) - body
  [Cro::HTTP] ok 280 - Error routine i'm-a-teapot sanity (2) - status
  [Cro::HTTP] ok 281 - Error routine i'm-a-teapot sanity (2) - content type
  [Cro::HTTP] ok 282 - Error routine i'm-a-teapot sanity (2) - body
  [Cro::HTTP] ok 283 - Error routine i'm-a-teapot (2) - status
  [Cro::HTTP] ok 284 - Error routine i'm-a-teapot (2) - content type
  [Cro::HTTP] ok 285 - Error routine i'm-a-teapot (2) - body
  [Cro::HTTP] ok 286 - Temporary redirect (1) - status
  [Cro::HTTP] ok 287 - Temporary redirect (1) - content type
  [Cro::HTTP] ok 288 - Temporary redirect (1) - location
  [Cro::HTTP] ok 289 - Temporary redirect (1) - body
  [Cro::HTTP] ok 290 - Temporary redirect (2) - status
  [Cro::HTTP] ok 291 - Temporary redirect (2) - content type
  [Cro::HTTP] ok 292 - Temporary redirect (2) - location
  [Cro::HTTP] ok 293 - Temporary redirect (2) - body
  [Cro::HTTP] ok 294 - Temporary redirect (3) - status
  [Cro::HTTP] ok 295 - Temporary redirect (3) - content type
  [Cro::HTTP] ok 296 - Temporary redirect (3) - location
  [Cro::HTTP] ok 297 - Temporary redirect (3) - body
  [Cro::HTTP] ok 298 - Temporary redirect (4) - status
  [Cro::HTTP] ok 299 - Temporary redirect (4) - content type
  [Cro::HTTP] ok 300 - Temporary redirect (4) - location
  [Cro::HTTP] ok 301 - Temporary redirect (4) - body
  [Cro::HTTP] ok 302 - Permanent redirect (1) - status
  [Cro::HTTP] ok 303 - Permanent redirect (1) - content type
  [Cro::HTTP] ok 304 - Permanent redirect (1) - location
  [Cro::HTTP] ok 305 - Permanent redirect (1) - body
  [Cro::HTTP] ok 306 - Permanent redirect (2) - status
  [Cro::HTTP] ok 307 - Permanent redirect (2) - content type
  [Cro::HTTP] ok 308 - Permanent redirect (2) - location
  [Cro::HTTP] ok 309 - Permanent redirect (2) - body
  [Cro::HTTP] ok 310 - See other redirect (1) - status
  [Cro::HTTP] ok 311 - See other redirect (1) - content type
  [Cro::HTTP] ok 312 - See other redirect (1) - location
  [Cro::HTTP] ok 313 - See other redirect (1) - body
  [Cro::HTTP] ok 314 - See other redirect (2) - status
  [Cro::HTTP] ok 315 - See other redirect (2) - content type
  [Cro::HTTP] ok 316 - See other redirect (2) - location
  [Cro::HTTP] ok 317 - See other redirect (2) - body
  [Cro::HTTP] ok 318 - Can use request inside of a handler
  [Cro::HTTP] ok 319 - request-body-blob passed a block invokes it with the body blob
  [Cro::HTTP] ok 320 - request-body-text passed a block invokes it with the body text
  [Cro::HTTP] ok 321 - request-body passed a block invokes it with the body object
  [Cro::HTTP] ok 322 - request-body passed a pair invokes block when content type matches
  [Cro::HTTP] ok 323 - When no body match, get bad request response
  [Cro::HTTP] ok 324 - request-body passed a list chooses first Pair if there is a match
  [Cro::HTTP] ok 325 - request-body passed a list chooses second Pair if there is a match
  [Cro::HTTP] ok 326 - request-body passed a list chooses final block if no earlier pairs match
  [Cro::HTTP] ok 327 - request-body matches by signature (Pair case)
  [Cro::HTTP] ok 328 - request-body matches by signature (Block case)
  [Cro::HTTP] ok 329 - body-parser installs a new body parser and it is used
  [Cro::HTTP] ok 330 - body-parser leaves existing body parsers in place
  [Cro::HTTP] ok 331 - body-serializer prepends a new body serializer and it is used
  [Cro::HTTP] ok 332 - body-serializer does not prevent default serializers being found
  [Cro::HTTP] ok 333 - Optional cookie route matches without cookie
  [Cro::HTTP] ok 334 - Status is good
  [Cro::HTTP] ok 335 - Optional cookie route matches with cookie
  [Cro::HTTP] ok 336 - Status is good
  [Cro::HTTP] ok 337 - Request without needed cookie was rejected
  [Cro::HTTP] ok 338 - Bad request to access page without needed cookie
  [Cro::HTTP] ok 339 - Request with required cookie works correctly
  [Cro::HTTP] ok 340 - Status is good
  [Cro::HTTP] ok 341 - Cookie hash works correctly
  [Cro::HTTP] ok 342 - Status is good
  [Cro::HTTP] ok 343 - 
  [Cro::HTTP] ok 344 - Got plain cookie
  [Cro::HTTP] ok 345 - Cookie is here
  [Cro::HTTP] ok 346 - 
  [Cro::HTTP] ok 347 - Status is good
  [Cro::HTTP] ok 348 - Complex cookie is here
  [Cro::HTTP] ok 349 - Static index is fine
  [Cro::HTTP] ok 350 - Static sets correct status code
  [Cro::HTTP] ok 351 - Files with long path work
  [Cro::HTTP] ok 352 - Good status
  [Cro::HTTP] ok 353 - 404 for static works
  [Cro::HTTP] ok 354 - 403 for static works
  [Cro::HTTP] ok 355 - Content-type was setted correctly
  [Cro::HTTP] ok 356 - Custom extension works
  [Cro::HTTP] ok 357 - 200 for static works
  [Cro::HTTP] ok 358 - Cache-Control header is set
  [Cro::HTTP] ok 359 - max-age is added
  [Cro::HTTP] ok 360 - public directive is added
  [Cro::HTTP] ok 361 - multipart/form-data is handled with destructuring
  [Cro::HTTP] ok 362 - urlencoded is handled with destructuring
  [Cro::HTTP] ok 363 - json is handled with destructuring
  [Cro::HTTP] ok 364 - request.uri reconstructs full request URI
  [Cro::HTTP] ok 365 - Basic include: after (outer)
  [Cro::HTTP] ok 366 - Basic include: empty route (include)
  [Cro::HTTP] ok 367 - Basic include: some parts (include)
  [Cro::HTTP] ok 368 - Basic include: before (outer)
  [Cro::HTTP] ok 369 - include and body-parser: body parser in include works in include
  [Cro::HTTP] ok 370 - include and body-parser: outer body parser visible in include
  [Cro::HTTP] ok 371 - include and body-parser: body parser in include does not leak out
  [Cro::HTTP] ok 372 - include and body-parser: outer has outer body parser
  [Cro::HTTP] ok 373 - Basic include: route 1B
  [Cro::HTTP] ok 374 - Basic include: route 1B
  [Cro::HTTP] ok 375 - Basic include: route 2B
  [Cro::HTTP] ok 376 - Basic include: route 1B
  [Cro::HTTP] ok 377 - Basic include: route 2A
  [Cro::HTTP] ok 378 - Basic include: route 2B
  [Cro::HTTP] ok 379 - Basic include: route 2A
  [Cro::HTTP] ok 380 - Basic include: route 1A
  [Cro::HTTP] ok 381 - Basic include: route 2B
  [Cro::HTTP] ok 382 - Basic include: route 1B
  [Cro::HTTP] ok 383 - Basic include: route 1A
  [Cro::HTTP] ok 384 - Basic include: route 2A
  [Cro::HTTP] ok 385 - Basic include: route 1A
  [Cro::HTTP] ok 386 - Basic include: route 1A
  [Cro::HTTP] ok 387 - Basic include: route 2A
  [Cro::HTTP] ok 388 - Basic include: route 2B
  [Cro::HTTP] ok 389 - Basic delegation: delegated transform simple
  [Cro::HTTP] ok 390 - Basic delegation: delegated transform multi part
  [Cro::HTTP] ok 391 - Basic delegation: delegated transform and second
  [Cro::HTTP] ok 392 - Basic delegation: delegated transform first
  [Cro::HTTP] ok 393 - Delegation: Home
  [Cro::HTTP] ok 394 - Delegation: / and /category
  [Cro::HTTP] ok 395 - Delegation: Path
  [Cro::HTTP] ok 396 - Delegation: Slash
  [Cro::HTTP] ok 397 - Delegation: /item and /proxy/item
  [Cro::HTTP] ok 398 - Delegation: /item/1 and /proxy/item/1
  [Cro::HTTP] ok 399 - Can match URL segments with encoded bits (/a%2Bplus)
  [Cro::HTTP] ok 400 - Can match URL segments with encoded bits (/encoded%2Fslash)
  [Cro::HTTP] ok 401 - Can pass query argument without path components (/?value=1)
  [Cro::HTTP] ok 402 - Can pass query arguments with slurpy path signature (/?value=1)
  [Cro::HTTP] ok 403 - Can pass query arguments with slurpy path signature (/x?value=1)
  [Cro::HTTP] ok 404 - Get value from index
  [Cro::HTTP] ok 405 - Static sets correct status code
  [Cro::HTTP] ok 406 - static indexes order check, 1
  [Cro::HTTP] ok 407 - Good status
  [Cro::HTTP] ok 408 - static indexes order check, 2
  [Cro::HTTP] ok 409 - Good status
  [Cro::HTTP] ok 410 - No candidate served with empty indexes
  [Cro::HTTP] ok 411 - Indexes with mime-types returns good status
  [Cro::HTTP] ok 412 - Indexes with mime-types returns proper content-type
  [Cro::HTTP] ok 413 - Get index.html from resources
  [Cro::HTTP] ok 414 - resource sets correct status code
  [Cro::HTTP] ok 415 - resource sets correct content-type
  [Cro::HTTP] ok 416 - Get folder/test.txt from resources
  [Cro::HTTP] ok 417 - Good status
  [Cro::HTTP] ok 418 - Good content-type
  [Cro::HTTP] ok 419 - Get <folder test.txt> from resources
  [Cro::HTTP] ok 420 - Good status
  [Cro::HTTP] ok 421 - Good content-type
  [Cro::HTTP] ok 422 - indexes in a folder of resources
  [Cro::HTTP] ok 423 - Good status
  [Cro::HTTP] ok 424 - Good content-type
  [Cro::HTTP] ok 425 - indexes in root of resources, 1
  [Cro::HTTP] ok 426 - Good status
  [Cro::HTTP] ok 427 - Good content-type
  [Cro::HTTP] ok 428 - indexes in root of resources, 2
  [Cro::HTTP] ok 429 - Good status
  [Cro::HTTP] ok 430 - Good content-type
  [Cro::HTTP] ok 431 - The extension point for other plugins wanting to use resources works
  [Cro::HTTP] ok 432 - Good content-type
  [Cro::HTTP] ok 433 - Around block was called
  [Cro::HTTP] ok 434 - Around block can send response
  [Cro::HTTP] ok 435 - Handler works normally with around block(s)
  [Cro::HTTP] ok 436 - Handler works normally with around block(s)
  [Cro::HTTP] ok 437 - The around blocks are called in top-to-bottom order
  [Cro::HTTP] ok 438 - Content-type header set by content replaces any existing one
  [Cro::HTTP] ok 439 - Recieved proper status for the case where a capture cannot be unpacked for whatever reason
  [Cro::HTTP] 1..439
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-session-inmemory.rakutest
  [Cro::HTTP] ok 1 - Request with no session cookie gets fresh state (1)
  [Cro::HTTP] ok 2 - Request with no session cookie gets fresh state (2)
  [Cro::HTTP] ok 3 - Session cookie being sent makes state work (request 1)
  [Cro::HTTP] ok 4 - Session cookie being sent makes state work (request 2)
  [Cro::HTTP] ok 5 - Session cookie being sent makes state work (request 3)
  [Cro::HTTP] ok 6 - Session cookie being sent makes state work (request 4)
  [Cro::HTTP] ok 7 - Session cookie being sent makes state work (request 5)
  [Cro::HTTP] ok 8 - No session confusion with concurrent clients (A)
  [Cro::HTTP] ok 9 - No session confusion with concurrent clients (B)
  [Cro::HTTP] ok 10 - New session for expiration test (sanity check)
  [Cro::HTTP] ok 11 - Request before expiration is OK
  [Cro::HTTP] ok 12 - A use of the session bumps its expiration
  [Cro::HTTP] ok 13 - Session expires appropriately
  [Cro::HTTP] 1..13
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-session-persistent.rakutest
  [Cro::HTTP] ok 1 - Request with no session cookie gets fresh state (1)
  [Cro::HTTP] ok 2 - Request with no session cookie gets fresh state (2)
  [Cro::HTTP] ok 3 - Session cookie being sent makes state work (request 1)
  [Cro::HTTP] ok 4 - Session cookie being sent makes state work (request 2)
  [Cro::HTTP] ok 5 - Session cookie being sent makes state work (request 3)
  [Cro::HTTP] ok 6 - Session cookie being sent makes state work (request 4)
  [Cro::HTTP] ok 7 - Session cookie being sent makes state work (request 5)
  [Cro::HTTP] ok 8 - No session confusion with concurrent clients (A)
  [Cro::HTTP] ok 9 - No session confusion with concurrent clients (B)
  [Cro::HTTP] ok 10 - New session for expiration test (sanity check)
  [Cro::HTTP] ok 11 - Request before expiration is OK
  [Cro::HTTP] ok 12 - A use of the session bumps its expiration
  [Cro::HTTP] ok 13 - Session expires appropriately
  [Cro::HTTP] ok 14 - Logging
  [Cro::HTTP] ok 15 - New session for route 1
  [Cro::HTTP] ok 16 - Using old session for route 2
  [Cro::HTTP] ok 17 - New session for route 1
  [Cro::HTTP] ok 18 - Logging
  [Cro::HTTP] ok 19 - Using old session for route 2
  [Cro::HTTP] 1..19
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame-parser.rakutest
  [Cro::HTTP] ok 1 - HTTP2 frame parser is a transform
  [Cro::HTTP] ok 2 - HTTP2 frame parser consumes TCP messages
  [Cro::HTTP] ok 3 - HTTP2 frame parser produces HTTP2 frames
  [Cro::HTTP] ok 4 - DATA Frame length cannot be less than padding length
  [Cro::HTTP] ok 5 - Empty DATA frame
  [Cro::HTTP] ok 6 - Empty DATA frame is serialized back
  [Cro::HTTP] ok 7 - DATA frame without padding
  [Cro::HTTP] ok 8 - DATA frame without padding is serialized back
  [Cro::HTTP] ok 9 - DATA frame with zero padding
  [Cro::HTTP] ok 10 - DATA frame with zero padding is serialized back
  [Cro::HTTP] ok 11 - DATA frame with padding
  [Cro::HTTP] ok 12 - DATA frame with padding is serialized back
  [Cro::HTTP] ok 13 - HEADERS Frame length cannot be less than padding length
  [Cro::HTTP] ok 14 - Empty HEADERS frame
  [Cro::HTTP] ok 15 - Empty HEADERS frame is serialized back
  [Cro::HTTP] ok 16 - HEADERS frame without padding
  [Cro::HTTP] ok 17 - HEADERS frame without padding is serialized back
  [Cro::HTTP] ok 18 - HEADERS frame with zero padding
  [Cro::HTTP] ok 19 - HEADERS frame with zero padding is serialized back
  [Cro::HTTP] ok 20 - PRIORITY Frame length is always 5 bytes
  [Cro::HTTP] ok 21 - RST_STREAM Frame length is always 4 bytes
  [Cro::HTTP] ok 22 - Ack SETTINGS Frame length is always 0
  [Cro::HTTP] ok 23 - SETTINGS Frame length is always divisible by 6
  [Cro::HTTP] ok 24 - SETTINGS Frame length is always divisible by 6
  [Cro::HTTP] ok 25 - WindowIncrement Frame length is always 4
  [Cro::HTTP] ok 26 - SETTINGS frame with zero content is emitted correctly
  [Cro::HTTP] 1..26
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame-serializer.rakutest
  [Cro::HTTP] ok 1 - HTTP2 frame serializer is a transform
  [Cro::HTTP] ok 2 - HTTP2 frame serializer consumes HTTP2 frames
  [Cro::HTTP] ok 3 - HTTP2 frame serializer produces TCP messages
  [Cro::HTTP] ok 4 - Simple data frame
  [Cro::HTTP] ok 5 - Simple data frame is parsed back
  [Cro::HTTP] ok 6 - Simple data frame with padding
  [Cro::HTTP] ok 7 - Simple data frame with padding is parsed back
  [Cro::HTTP] ok 8 - Simple headers frame
  [Cro::HTTP] ok 9 - Simple headers frame is parsed back
  [Cro::HTTP] ok 10 - Simple headers frame with padding
  [Cro::HTTP] ok 11 - Simple headers frame with padding is parsed back
  [Cro::HTTP] ok 12 - Simple priority frame
  [Cro::HTTP] ok 13 - Simple priority frame is parsed back
  [Cro::HTTP] ok 14 - Simple RstStream frame
  [Cro::HTTP] ok 15 - Simple RstStream frame is parsed back
  [Cro::HTTP] ok 16 - RstStream frame with a custom error treats it as INTERNAL_ERROR
  [Cro::HTTP] ok 17 - RstStream frame with a custom error treats it as INTERNAL_ERROR is parsed back
  [Cro::HTTP] ok 18 - Simple Settings frame
  [Cro::HTTP] ok 19 - Settings frame is successful
  [Cro::HTTP] ok 20 - Simple PushPromise frame
  [Cro::HTTP] ok 21 - Simple PushPromise frame is parsed back
  [Cro::HTTP] ok 22 - PushPromise frame with padding
  [Cro::HTTP] ok 23 - PushPromise frame with padding is parsed back
  [Cro::HTTP] ok 24 - Simple Ping frame
  [Cro::HTTP] ok 25 - Ping frame is successful
  [Cro::HTTP] ok 26 - Ping payload cannot be more than 8 bytes
  [Cro::HTTP] ok 27 - Simple GoAway frame
  [Cro::HTTP] ok 28 - Simple GoAway frame is parsed back
  [Cro::HTTP] ok 29 - GoAway frame with a custom error treats it as INTERNAL_ERROR
  [Cro::HTTP] ok 30 - GoAway frame with a custom error treats it as INTERNAL_ERROR is parsed back
  [Cro::HTTP] ok 31 - Simple WindowUpdate frame
  [Cro::HTTP] ok 32 - Simple WindowUpdate frame is parsed back
  [Cro::HTTP] ok 33 - Simple Continuation frame
  [Cro::HTTP] ok 34 - Simple Continuation frame is parsed back
  [Cro::HTTP] ok 35 - 
  [Cro::HTTP] ok 36 - 
  [Cro::HTTP] ok 37 - 
  [Cro::HTTP] ok 38 - 
  [Cro::HTTP] ok 39 - Too long Headers frame is splitted
  [Cro::HTTP] ok 40 - 
  [Cro::HTTP] ok 41 - 
  [Cro::HTTP] ok 42 - 
  [Cro::HTTP] ok 43 - 
  [Cro::HTTP] ok 44 - Too long Data frame is splitted
  [Cro::HTTP] 1..44
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame.rakutest
  [Cro::HTTP] ok 1 - DATA frame stream identifier cannot be 0
  [Cro::HTTP] ok 2 - HEADERS frame stream identifier cannot be 0
  [Cro::HTTP] ok 3 - PRIORITY frame stream identifier cannot be 0
  [Cro::HTTP] ok 4 - Settings stream-identifier cannot be non-zero
  [Cro::HTTP] ok 5 - PUSH_PROMISE frame stream identifier cannot be 0
  [Cro::HTTP] ok 6 - Ping stream-identifier cannot be non-zero
  [Cro::HTTP] ok 7 - GOAWAY Frame stream-identifier cannot be non-zero
  [Cro::HTTP] 1..7
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-request-parser.rakutest
  [Cro::HTTP] ok 1 - check 1
  [Cro::HTTP] ok 2 - check 2
  [Cro::HTTP] ok 3 - check 3
  [Cro::HTTP] ok 4 - check 4
  [Cro::HTTP] ok 5 - check 5
  [Cro::HTTP] ok 6 - Headers
  [Cro::HTTP] ok 7 - check 1
  [Cro::HTTP] ok 8 - check 2
  [Cro::HTTP] ok 9 - check 3
  [Cro::HTTP] ok 10 - check 4
  [Cro::HTTP] ok 11 - check 5
  [Cro::HTTP] ok 12 - check 6
  [Cro::HTTP] ok 13 - Headers + Continuation
  [Cro::HTTP] ok 14 - check 1
  [Cro::HTTP] ok 15 - check 2
  [Cro::HTTP] ok 16 - check 3
  [Cro::HTTP] ok 17 - check 4
  [Cro::HTTP] ok 18 - Headers + Data
  [Cro::HTTP] ok 19 - check 1
  [Cro::HTTP] ok 20 - check 2
  [Cro::HTTP] ok 21 - check 3
  [Cro::HTTP] ok 22 - check 4
  [Cro::HTTP] ok 23 - check 5
  [Cro::HTTP] ok 24 - check 6
  [Cro::HTTP] ok 25 - check 7
  [Cro::HTTP] ok 26 - Headers + Continuation + Data
  [Cro::HTTP] ok 27 - check 1
  [Cro::HTTP] ok 28 - check 2
  [Cro::HTTP] ok 29 - check 3
  [Cro::HTTP] ok 30 - check 4
  [Cro::HTTP] ok 31 - check 5
  [Cro::HTTP] ok 32 - check 6
  [Cro::HTTP] ok 33 - check 7
  [Cro::HTTP] ok 34 - check 8
  [Cro::HTTP] ok 35 - Headers + Continuation + Data + Headers
  [Cro::HTTP] ok 36 - check 1
  [Cro::HTTP] ok 37 - check 2
  [Cro::HTTP] ok 38 - check 3
  [Cro::HTTP] ok 39 - check 4
  [Cro::HTTP] ok 40 - check 1
  [Cro::HTTP] ok 41 - check 2
  [Cro::HTTP] ok 42 - check 3
  [Cro::HTTP] ok 43 - Header1 + Header2 + Data1
  [Cro::HTTP] ok 44 - check 1
  [Cro::HTTP] ok 45 - check 2
  [Cro::HTTP] ok 46 - check 3
  [Cro::HTTP] ok 47 - check 4
  [Cro::HTTP] ok 48 - check 1
  [Cro::HTTP] ok 49 - check 2
  [Cro::HTTP] ok 50 - check 3
  [Cro::HTTP] ok 51 - check 4
  [Cro::HTTP] ok 52 - Header1 + Header2 + Data1 + Data2
  [Cro::HTTP] ok 53 - check 1
  [Cro::HTTP] ok 54 - check 2
  [Cro::HTTP] ok 55 - check 3
  [Cro::HTTP] ok 56 - check 1
  [Cro::HTTP] ok 57 - check 2
  [Cro::HTTP] ok 58 - check 3
  [Cro::HTTP] ok 59 - check 4
  [Cro::HTTP] ok 60 - Header1 + Continuation1 + Header2 + Data1
  [Cro::HTTP] # Subtest: Unfinished header cannot be interrupted
  [Cro::HTTP]     1..2
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP2::Error)
  [Cro::HTTP] ok 61 - Unfinished header cannot be interrupted
  [Cro::HTTP] 1..61
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-request-serializer.rakutest
  [Cro::HTTP] ok 1 - check 1
  [Cro::HTTP] ok 2 - check 2
  [Cro::HTTP] ok 3 - check 3
  [Cro::HTTP] ok 4 - check 4
  [Cro::HTTP] ok 5 - Header
  [Cro::HTTP] ok 6 - check 1
  [Cro::HTTP] ok 7 - check 2
  [Cro::HTTP] ok 8 - check 3
  [Cro::HTTP] ok 9 - check 4
  [Cro::HTTP] ok 10 - check 1
  [Cro::HTTP] ok 11 - check 2
  [Cro::HTTP] ok 12 - check 3
  [Cro::HTTP] ok 13 - check 4
  [Cro::HTTP] ok 14 - Header + Data
  [Cro::HTTP] ok 15 - check 1
  [Cro::HTTP] ok 16 - check 2
  [Cro::HTTP] ok 17 - check 3
  [Cro::HTTP] ok 18 - check 4
  [Cro::HTTP] ok 19 - check 1
  [Cro::HTTP] ok 20 - check 2
  [Cro::HTTP] ok 21 - check 3
  [Cro::HTTP] ok 22 - check 4
  [Cro::HTTP] ok 23 - check 1
  [Cro::HTTP] ok 24 - check 2
  [Cro::HTTP] ok 25 - check 3
  [Cro::HTTP] ok 26 - check 4
  [Cro::HTTP] ok 27 - Header + Data with unknown Content-Length
  [Cro::HTTP] ok 28 - round-trip: method
  [Cro::HTTP] ok 29 - round-trip: target
  [Cro::HTTP] ok 30 - round-trip: content-length header present and correct
  [Cro::HTTP] ok 31 - round-trip: body text
  [Cro::HTTP] ok 32 - POST with set-body round-trips correctly over HTTP/2
  [Cro::HTTP] 1..32
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-response-parser.rakutest
  [Cro::HTTP] ok 1 - check 1
  [Cro::HTTP] ok 2 - check 2
  [Cro::HTTP] ok 3 - check 3
  [Cro::HTTP] ok 4 - Headers
  [Cro::HTTP] ok 5 - check 1
  [Cro::HTTP] ok 6 - check 2
  [Cro::HTTP] ok 7 - check 3
  [Cro::HTTP] ok 8 - check 4
  [Cro::HTTP] ok 9 - Headers + Data
  [Cro::HTTP] 1..9
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-response-serializer.rakutest
  [Cro::HTTP] ok 1 - check 1
  [Cro::HTTP] ok 2 - check 2
  [Cro::HTTP] ok 3 - check 3
  [Cro::HTTP] ok 4 - check 4
  [Cro::HTTP] ok 5 - Header
  [Cro::HTTP] ok 6 - check 1
  [Cro::HTTP] ok 7 - check 2
  [Cro::HTTP] ok 8 - check 3
  [Cro::HTTP] ok 9 - check 4
  [Cro::HTTP] ok 10 - check 1
  [Cro::HTTP] ok 11 - check 2
  [Cro::HTTP] ok 12 - check 3
  [Cro::HTTP] ok 13 - check 4
  [Cro::HTTP] ok 14 - Header + Data
  [Cro::HTTP] ok 15 - check 1
  [Cro::HTTP] ok 16 - check 2
  [Cro::HTTP] ok 17 - check 3
  [Cro::HTTP] ok 18 - check 4
  [Cro::HTTP] ok 19 - check 1
  [Cro::HTTP] ok 20 - check 2
  [Cro::HTTP] ok 21 - check 3
  [Cro::HTTP] ok 22 - check 4
  [Cro::HTTP] ok 23 - check 1
  [Cro::HTTP] ok 24 - check 2
  [Cro::HTTP] ok 25 - check 3
  [Cro::HTTP] ok 26 - check 4
  [Cro::HTTP] ok 27 - Header + Data - Content-Length unspecified
  [Cro::HTTP] ok 28 - Too small body throws
  [Cro::HTTP] ok 29 - Too big body throws
  [Cro::HTTP] 1..29
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/router-auth.rakutest
  [Cro::HTTP] # Subtest: Auth parameter with type that implements Cro::HTTP::Auth
  [Cro::HTTP]     ok 1 - Can request / successfully with non-logged-in, non-admin
  [Cro::HTTP]     ok 2 - Get the authorization object
  [Cro::HTTP]     ok 3 - Request to /page when not logged in is 401
  [Cro::HTTP]     ok 4 - Request to /admin when not logged in is 401
  [Cro::HTTP]     ok 5 - Can request / successfully with logged-in, non-admin
  [Cro::HTTP]     ok 6 - Get the authorization object
  [Cro::HTTP]     ok 7 - Can request /page successfully with logged-in, non-admin
  [Cro::HTTP]     ok 8 - Got expected body
  [Cro::HTTP]     ok 9 - Request to /admin when not an admin is 401
  [Cro::HTTP]     ok 10 - Can request / successfully with logged-in admin
  [Cro::HTTP]     ok 11 - Get the authorization object
  [Cro::HTTP]     ok 12 - Can request /page successfully with logged-in admin
  [Cro::HTTP]     ok 13 - Got expected body
  [Cro::HTTP]     ok 14 - Can request /admin successfully with logged-in admin
  [Cro::HTTP]     ok 15 - Got expected body
  [Cro::HTTP]     1..15
  [Cro::HTTP] ok 1 - Auth parameter with type that implements Cro::HTTP::Auth
  [Cro::HTTP] # Subtest: Auth parameter marked with is auth trait, not doing Cro::HTTP::Auth
  [Cro::HTTP]     ok 1 - Can request / successfully with non-logged-in, non-admin
  [Cro::HTTP]     ok 2 - Get the authorization object
  [Cro::HTTP]     ok 3 - Request to /page when not logged in is 401
  [Cro::HTTP]     ok 4 - Request to /admin when not logged in is 401
  [Cro::HTTP]     ok 5 - Can request / successfully with logged-in, non-admin
  [Cro::HTTP]     ok 6 - Get the authorization object
  [Cro::HTTP]     ok 7 - Can request /page successfully with logged-in, non-admin
  [Cro::HTTP]     ok 8 - Got expected body
  [Cro::HTTP]     ok 9 - Request to /admin when not an admin is 401
  [Cro::HTTP]     ok 10 - Can request / successfully with logged-in admin
  [Cro::HTTP]     ok 11 - Get the authorization object
  [Cro::HTTP]     ok 12 - Can request /page successfully with logged-in admin
  [Cro::HTTP]     ok 13 - Got expected body
  [Cro::HTTP]     ok 14 - Can request /admin successfully with logged-in admin
  [Cro::HTTP]     ok 15 - Got expected body
  [Cro::HTTP]     1..15
  [Cro::HTTP] ok 2 - Auth parameter marked with is auth trait, not doing Cro::HTTP::Auth
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/uri-http.rakutest
  [Cro::HTTP] ok 1 - A single / request target
  [Cro::HTTP] ok 2 - Check 1
  [Cro::HTTP] ok 3 - Check 2
  [Cro::HTTP] ok 4 - Check 3
  [Cro::HTTP] ok 5 - Check 4
  [Cro::HTTP] ok 6 - Check 5
  [Cro::HTTP] ok 7 - Check 6
  [Cro::HTTP] ok 8 - A single /foo/bar.html request target
  [Cro::HTTP] ok 9 - Check 1
  [Cro::HTTP] ok 10 - Check 2
  [Cro::HTTP] ok 11 - Check 3
  [Cro::HTTP] # Subtest: Basic query string additions as pair arguemnts
  [Cro::HTTP]     ok 1 - Path was retained correctly
  [Cro::HTTP]     ok 2 - Query string correctly appended
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 12 - Basic query string additions as pair arguemnts
  [Cro::HTTP] # Subtest: Basic query string additions as named arguments
  [Cro::HTTP]     ok 1 - Path was retained correctly
  [Cro::HTTP]     ok 2 - Query string correctly appended
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 13 - Basic query string additions as named arguments
  [Cro::HTTP] # Subtest: Basic query string additions retain what was originally there
  [Cro::HTTP]     ok 1 - Path was retained correctly
  [Cro::HTTP]     ok 2 - Existing query string values were retained
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 14 - Basic query string additions retain what was originally there
  [Cro::HTTP] # Subtest: Query string keys and values are encoded
  [Cro::HTTP]     ok 1 - Path was retained correctly
  [Cro::HTTP]     ok 2 - Correct encoding
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 15 - Query string keys and values are encoded
  [Cro::HTTP] ok 16 - + signs in query string decoded correctly
  [Cro::HTTP] 1..16
  ===> Testing [OK] for Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0>
  ===> Installing: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0>
  ===> Install [OK] for Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 3min 33.930s
               CPU time consumed: 5min 17.618s
                     Memory peak: 2.7G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1408802-i1418567.service; invocation ID: af7a11a1dbe74919a6957329c419559f
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Cro::HTTP
  ===> Found: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0> [via Zef::Repository::Ecosystems<fez>]
  [Cro::HTTP] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549467.1408803.1758.2992810740018/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz https://360.zef.pm/C/RO/CRO_HTTP/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Fetching [OK]: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549467.1408803.1758.2992810740018/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  [Cro::HTTP] Command: tar -t -f ./3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  [Cro::HTTP] Command: tar -xvf ./3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz -C ../3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Extraction [OK]: Cro::HTTP to /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Testing: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0>
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-basic-with-session.rakutest
  [Cro::HTTP] ok 1 - Username is set after basic authentication
  [Cro::HTTP] # Subtest: 401 when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|5431991559880) ... }
  [Cro::HTTP] ok 2 - 401 when wrong credentials are passed
  [Cro::HTTP] # Subtest: WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|5431991560312) ... }
  [Cro::HTTP] ok 3 - WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP] # Subtest: Request without credentials returns 401
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|5431991560384) ... }
  [Cro::HTTP] ok 4 - Request without credentials returns 401
  [Cro::HTTP] # Subtest: Request without credentials has WWW-Authenticate header
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|5432117618472) ... }
  [Cro::HTTP] ok 5 - Request without credentials has WWW-Authenticate header
  [Cro::HTTP] 1..5
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-basic.rakutest
  [Cro::HTTP] ok 1 - Username is set after basic authentication
  [Cro::HTTP] # Subtest: 401 when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4852874393880) ... }
  [Cro::HTTP] ok 2 - 401 when wrong credentials are passed
  [Cro::HTTP] # Subtest: WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4852874394312) ... }
  [Cro::HTTP] ok 3 - WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP] # Subtest: Request without credentials returns 401
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4852874394384) ... }
  [Cro::HTTP] ok 4 - Request without credentials returns 401
  [Cro::HTTP] # Subtest: Request without credentials has WWW-Authenticate header
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4852874394456) ... }
  [Cro::HTTP] ok 5 - Request without credentials has WWW-Authenticate header
  [Cro::HTTP] 1..5
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-webtoken-bearer.rakutest
  [Cro::HTTP] ok 1 - Username is correct
  [Cro::HTTP] ok 2 - Expired token is not passed
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-webtoken-cookie.rakutest
  [Cro::HTTP] ok 1 - Token is set to cookies
  [Cro::HTTP] ok 2 - Username is correct
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-cookie.rakutest
  [Cro::HTTP] ok 1 - Correct cookie names are into the subset
  [Cro::HTTP] ok 2 - Empty cookie name is now allowed
  [Cro::HTTP] ok 3 - No parens allowed in a cookie
  [Cro::HTTP] ok 4 - Cookie octet can be wrapped in double quotes
  [Cro::HTTP] # Subtest: Incorrect symbols are outside of CookieName subset
  [Cro::HTTP]     ok 1 - 
  [Cro::HTTP]     ok 2 - 
  [Cro::HTTP]     ok 3 - 
  [Cro::HTTP]     ok 4 - 
  [Cro::HTTP]     ok 5 - 
  [Cro::HTTP]     ok 6 - 
  [Cro::HTTP]     ok 7 - 
  [Cro::HTTP]     ok 8 - 
  [Cro::HTTP]     ok 9 - 
  [Cro::HTTP]     ok 10 - 
  [Cro::HTTP]     ok 11 - 
  [Cro::HTTP]     ok 12 - 
  [Cro::HTTP]     ok 13 - 
  [Cro::HTTP]     ok 14 - 
  [Cro::HTTP]     ok 15 - 
  [Cro::HTTP]     ok 16 - 
  [Cro::HTTP]     ok 17 - 
  [Cro::HTTP]     ok 18 - 
  [Cro::HTTP]     ok 19 - 
  [Cro::HTTP]     ok 20 - 
  [Cro::HTTP]     ok 21 - 
  [Cro::HTTP]     ok 22 - 
  [Cro::HTTP]     ok 23 - 
  [Cro::HTTP]     ok 24 - 
  [Cro::HTTP]     ok 25 - 
  [Cro::HTTP]     ok 26 - 
  [Cro::HTTP]     ok 27 - 
  [Cro::HTTP]     ok 28 - 
  [Cro::HTTP]     ok 29 - 
  [Cro::HTTP]     ok 30 - 
  [Cro::HTTP]     ok 31 - 
  [Cro::HTTP]     ok 32 - 
  [Cro::HTTP]     ok 33 - 
  [Cro::HTTP]     ok 34 - 
  [Cro::HTTP]     ok 35 - 
  [Cro::HTTP]     ok 36 - 
  [Cro::HTTP]     ok 37 - 
  [Cro::HTTP]     ok 38 - 
  [Cro::HTTP]     ok 39 - 
  [Cro::HTTP]     ok 40 - 
  [Cro::HTTP]     ok 41 - 
  [Cro::HTTP]     ok 42 - 
  [Cro::HTTP]     ok 43 - 
  [Cro::HTTP]     ok 44 - 
  [Cro::HTTP]     ok 45 - 
  [Cro::HTTP]     ok 46 - 
  [Cro::HTTP]     ok 47 - 
  [Cro::HTTP]     ok 48 - 
  [Cro::HTTP]     ok 49 - 
  [Cro::HTTP]     ok 50 - 
  [Cro::HTTP]     ok 51 - 
  [Cro::HTTP]     1..51
  [Cro::HTTP] ok 5 - Incorrect symbols are outside of CookieName subset
  [Cro::HTTP] ok 6 - Correct cookie values are into the subset
  [Cro::HTTP] ok 7 - Empty cookie value is allowed
  [Cro::HTTP] # Subtest: Incorrect symbols are outside of CookieValue subset
  [Cro::HTTP]     ok 1 - 
  [Cro::HTTP]     ok 2 - 
  [Cro::HTTP]     ok 3 - 
  [Cro::HTTP]     ok 4 - 
  [Cro::HTTP]     ok 5 - 
  [Cro::HTTP]     1..5
  [Cro::HTTP] ok 8 - Incorrect symbols are outside of CookieValue subset
  [Cro::HTTP] ok 9 - Correct domain name works
  [Cro::HTTP] ok 10 - Incorrect domain name with bad character
  [Cro::HTTP] ok 11 - Empty domain name cannot be created
  [Cro::HTTP] ok 12 - Domain name cannot contain spaces
  [Cro::HTTP] ok 13 - Set-Cookie string 1 parses
  [Cro::HTTP] ok 14 - Set-Cookie string 2 parses
  [Cro::HTTP] ok 15 - Set-Cookie string 3 parses
  [Cro::HTTP] ok 16 - Set-Cookie ala buggy Tomcat (missing space); we tolerate this
  [Cro::HTTP] ok 17 - Cookie cannot be created with no arguments
  [Cro::HTTP] ok 18 - Cookie cannot be created without value
  [Cro::HTTP] ok 19 - Cookie cannot be created without name
  [Cro::HTTP] ok 20 - Cookie can be created
  [Cro::HTTP] ok 21 - New is read only
  [Cro::HTTP] ok 22 - Value is read only
  [Cro::HTTP] ok 23 - Expires is read only
  [Cro::HTTP] ok 24 - Max-age is read only
  [Cro::HTTP] ok 25 - Domain is read only
  [Cro::HTTP] ok 26 - Path is read only
  [Cro::HTTP] ok 27 - Secure is read only
  [Cro::HTTP] ok 28 - Http-only is read only
  [Cro::HTTP] ok 29 - SameSite is read only
  [Cro::HTTP] ok 30 - Set cookie 1 works
  [Cro::HTTP] ok 31 - Cookie 1 works
  [Cro::HTTP] ok 32 - Cookie 1 can be parsed
  [Cro::HTTP] ok 33 - Set cookie 2 works
  [Cro::HTTP] ok 34 - Cookie 2 works
  [Cro::HTTP] ok 35 - Cookie 2 can be parsed
  [Cro::HTTP] ok 36 - Set cookie 3 works
  [Cro::HTTP] ok 37 - Cookie 3 works
  [Cro::HTTP] ok 38 - Cookie 3 can be parsed
  [Cro::HTTP] ok 39 - Set cookie 4 works
  [Cro::HTTP] ok 40 - Cookie 4 works
  [Cro::HTTP] ok 41 - Cookie 4 can be parsed
  [Cro::HTTP] ok 42 - Invalid SameSite value discarded
  [Cro::HTTP] ok 43 - Valid SameSite value cookie 0 can be parsed
  [Cro::HTTP] ok 44 - Valid SameSite value cookie 1 can be parsed
  [Cro::HTTP] ok 45 - Valid SameSite value cookie 2 can be parsed
  [Cro::HTTP] ok 46 - Correct path after extension
  [Cro::HTTP] ok 47 - Secure parsed after extension
  [Cro::HTTP] ok 48 - Extensions are parsed and extracted also
  [Cro::HTTP] ok 49 - Correct cookie name when illegal whitespace in value
  [Cro::HTTP] ok 50 - Cookie value parsed up to illegal whitespace
  [Cro::HTTP] ok 51 - Recovered to parse path after illegal cookie value
  [Cro::HTTP] 1..51
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-cookiejar.rakutest
  [Cro::HTTP] ok 1 - Empty cookie jar contents returns empty list
  [Cro::HTTP] ok 2 - Empty cookie jar contents with uri returns empty list
  [Cro::HTTP] ok 3 - Two cookies were added
  [Cro::HTTP] ok 4 - Cookie addition is neutral
  [Cro::HTTP] ok 5 - Cookie with bad domain was not added
  [Cro::HTTP] ok 6 - Uri-based check
  [Cro::HTTP] ok 7 - Good cookies are here
  [Cro::HTTP] ok 8 - Clear for absent url leaves jar untouched
  [Cro::HTTP] ok 9 - Clear for absent url with existing cookie name leaves jar untouched
  [Cro::HTTP] ok 10 - One cookie was removed
  [Cro::HTTP] ok 11 - All cookies from correct domain were removed
  [Cro::HTTP] ok 12 - Call to clear clears cookie jar
  [Cro::HTTP] ok 13 - Cookie with duration was added successfully
  [Cro::HTTP] ok 14 - Creation time is preserved during cookie update
  [Cro::HTTP] ok 15 - Cookie was deleted on negative-time cookie addition
  [Cro::HTTP] ok 16 - Cookies are added for sub-domains
  [Cro::HTTP] ok 17 - Rejected for incorrect sub-domain
  [Cro::HTTP] ok 18 - Header was added
  [Cro::HTTP] ok 19 - Set string is correct
  [Cro::HTTP] ok 20 - A single cookie was added, successfully
  [Cro::HTTP] ok 21 - Added cookie has correct name
  [Cro::HTTP] ok 22 - Added cookie has correct value
  [Cro::HTTP] ok 23 - Added cookie has proper domain
  [Cro::HTTP] ok 24 - Added cookie has proper path
  [Cro::HTTP] ok 25 - Cookie has proper expiration time
  [Cro::HTTP] ok 26 - A second cookie was added successfully
  [Cro::HTTP] ok 27 - New cookie is not persistent
  [Cro::HTTP] ok 28 - New cookie has expected expiration time with no max-age set
  [Cro::HTTP] ok 29 - First cookie was added to request
  [Cro::HTTP] ok 30 - Second cookie was added to request
  [Cro::HTTP] 1..30
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-log-file.rakutest
  [Cro::HTTP] ok 1 - Correct responses logged
  [Cro::HTTP] ok 2 - Error responses logged
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-middleware.rakutest
  [Cro::HTTP] # Subtest: Request and response middleware written using a transform
  [Cro::HTTP]     ok 1 - Header was set
  [Cro::HTTP]     ok 2 - Target was processed
  [Cro::HTTP]     ok 3 - after works with before
  [Cro::HTTP]     ok 4 - before works with after
  [Cro::HTTP]     1..4
  [Cro::HTTP] ok 1 - Request and response middleware written using a transform
  [Cro::HTTP] # Subtest: Request and response middleware written using a Cro::HTTP::Middleware roles
  [Cro::HTTP]     ok 1 - Header was set
  [Cro::HTTP]     ok 2 - Target was processed
  [Cro::HTTP]     ok 3 - after works with before
  [Cro::HTTP]     ok 4 - before works with after
  [Cro::HTTP]     ok 5 - Request middleware works with before-matched in route block
  [Cro::HTTP]     ok 6 - Response middleware works with after-matched in route block
  [Cro::HTTP]     1..6
  [Cro::HTTP] ok 2 - Request and response middleware written using a Cro::HTTP::Middleware roles
  [Cro::HTTP] # Subtest: Conditional response middleware using Cro::HTTP::Middleware::Conditional
  [Cro::HTTP]     # Subtest: Got 403 response from middleware when no auth header
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4753684463056) ... }
  [Cro::HTTP]     ok 1 - Got 403 response from middleware when no auth header
  [Cro::HTTP]     ok 2 - Got 200 normal response with an auth header
  [Cro::HTTP]     # Subtest: Got 403 response from middleware when no auth header (before-matched in router)
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4753581036256) ... }
  [Cro::HTTP]     ok 3 - Got 403 response from middleware when no auth header (before-matched in router)
  [Cro::HTTP]     ok 4 - Got 200 normal response with an auth header (before-matched in router)
  [Cro::HTTP]     # Subtest: Got 403 response from middleware when no auth header (before-matched + include in router)
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4753581040864) ... }
  [Cro::HTTP]     ok 5 - Got 403 response from middleware when no auth header (before-matched + include in router)
  [Cro::HTTP]     ok 6 - Got 200 normal response with an auth header (before-matched + include in router)
  [Cro::HTTP]     1..6
  [Cro::HTTP] ok 3 - Conditional response middleware using Cro::HTTP::Middleware::Conditional
  [Cro::HTTP] # Subtest: Request/response middleware using Cro::HTTP::Middleware::RequestResponse
  [Cro::HTTP]     ok 1 - Got 200 response on first request
  [Cro::HTTP]     ok 2 - Response part added header
  [Cro::HTTP]     ok 3 - Expected body
  [Cro::HTTP]     ok 4 - Got 200 response on second request
  [Cro::HTTP]     ok 5 - Response part did not run on early response
  [Cro::HTTP]     ok 6 - Got cached body
  [Cro::HTTP]     ok 7 - Got 200 response on first request (before-matched in router)
  [Cro::HTTP]     ok 8 - Response part added header (before-matched in router)
  [Cro::HTTP]     ok 9 - Expected body (before-matched in router)
  [Cro::HTTP]     ok 10 - Got 200 response on second request (before-matched in router)
  [Cro::HTTP]     ok 11 - Response part did not run on early response (before-matched in router)
  [Cro::HTTP]     ok 12 - Got cached body (before-matched in router)
  [Cro::HTTP]     ok 13 - Got 200 response on first request (before-matched + include in router)
  [Cro::HTTP]     ok 14 - Response part added header (before-matched + include in router)
  [Cro::HTTP]     ok 15 - Expected body (before-matched + include in router)
  [Cro::HTTP]     ok 16 - Got 200 response on second request (before-matched + include in router)
  [Cro::HTTP]     ok 17 - Response part did not run on early response (before-matched + include in router)
  [Cro::HTTP]     ok 18 - Got cached body (before-matched + include in router)
  [Cro::HTTP]     1..18
  [Cro::HTTP] ok 4 - Request/response middleware using Cro::HTTP::Middleware::RequestResponse
  [Cro::HTTP] # Subtest: Byte-level middleware, before/after request is parsed
  [Cro::HTTP]     ok 1 - before-parse works
  [Cro::HTTP]     ok 2 - after-serialize works
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 5 - Byte-level middleware, before/after request is parsed
  [Cro::HTTP] # Subtest: Interaction of middleware written as Cro::Transform with HTTP router
  [Cro::HTTP]     ok 1 - per-route after-matched middleware for regular request works
  [Cro::HTTP]     ok 2 - per-route before-matched middleware for regular request works
  [Cro::HTTP]     ok 3 - per-route after-matched middleware for delegated request works
  [Cro::HTTP]     ok 4 - per-route before-matched middleware for delegated request works
  [Cro::HTTP]     ok 5 - per-route after-matched middleware for includee works
  [Cro::HTTP]     ok 6 - per-route before-matched middleware for includee works
  [Cro::HTTP]     ok 7 - per-route after-matched middleware for includee works
  [Cro::HTTP]     ok 8 - per-route before-matched middleware for includee works
  [Cro::HTTP]     ok 9 - per-route block before-matched middleware works
  [Cro::HTTP]     ok 10 - per-route block after-matched middleware works
  [Cro::HTTP]     ok 11 - Cannot use wrong typed Transformer as a middleware
  [Cro::HTTP]     1..11
  [Cro::HTTP] ok 6 - Interaction of middleware written as Cro::Transform with HTTP router
  [Cro::HTTP] # Subtest: Conditional response in block form of before-matched in router
  [Cro::HTTP]     # Subtest: Block form of before-matched in router can produce an early response
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4753736259768) ... }
  [Cro::HTTP]     ok 1 - Block form of before-matched in router can produce an early response
  [Cro::HTTP]     ok 2 - Block form of before-matched not producing a response also works
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 7 - Conditional response in block form of before-matched in router
  [Cro::HTTP] ok 8 - before-matched applies even to delegate done before it
  [Cro::HTTP] ok 9 - after-matched applies even to delegate done after it
  [Cro::HTTP] ok 10 - before-matched applies even to a route before it
  [Cro::HTTP] ok 11 - after-matched middleware applies even to a route before it
  [Cro::HTTP] ok 12 - Dies when no matched rule
  [Cro::HTTP] ok 13 - before block was executed
  [Cro::HTTP] ok 14 - before-matched block was not executed
  [Cro::HTTP] ok 15 - after block was executed
  [Cro::HTTP] ok 16 - after-matched block was not executed
  [Cro::HTTP] ok 17 - before and after is run from block definition
  [Cro::HTTP] ok 18 - before and after is run from class definition
  [Cro::HTTP] ok 19 - before and after is run from RequestResponse(Pair) definition
  [Cro::HTTP] ok 20 - Auth middleware is applied
  [Cro::HTTP] ok 21 - Auth middleware is applied 2
  [Cro::HTTP] ok 22 - After middleware is applied
  [Cro::HTTP] # Subtest: Better exception message when user tries to include route with before/after
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::AdHoc)
  [Cro::HTTP]     ok 3 - .message matches /'delegate'/
  [Cro::HTTP] ok 23 - Better exception message when user tries to include route with before/after
  [Cro::HTTP] ok 24 - delegate does not cause an exception
  [Cro::HTTP] 1..24
  [Cro::HTTP] Saw 1 occurrence of deprecated code.
  [Cro::HTTP] ================================================================================
  [Cro::HTTP] Method perl (from Mu) seen at:
  [Cro::HTTP]   /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist/lib/Cro/HTTP/Router.rakumod (Cro::HTTP::Router), line 1335
  [Cro::HTTP] Please use raku instead.
  [Cro::HTTP] --------------------------------------------------------------------------------
  [Cro::HTTP] Please contact the author to have these occurrences of deprecated code
  [Cro::HTTP] adapted, so that this message will disappear!
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-rawbodyparserselector.rakutest
  [Cro::HTTP] ok 1 - got the correct 'Cro::HTTP::RawBodyParser'
  [Cro::HTTP] ok 2 - No content-length or transfer-encoding
  [Cro::HTTP] ok 3 - got the correct 'Cro::HTTP::RawBodyParser'
  [Cro::HTTP] ok 4 - Content-Length
  [Cro::HTTP] ok 5 - got the correct 'Cro::HTTP::RawBodyParser'
  [Cro::HTTP] ok 6 - Chunked transfer encoding
  [Cro::HTTP] ok 7 - got the correct 'Cro::HTTP::RawBodyParser'
  [Cro::HTTP] ok 8 - Identity transfer encoding - no content-length
  [Cro::HTTP] ok 9 - got the correct 'Cro::HTTP::RawBodyParser'
  [Cro::HTTP] ok 10 - Identity transfer encoding - with content-length
  [Cro::HTTP] 1..10
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request-parser.rakutest
  [Cro::HTTP] ok 1 - HTTP request parser is a transform
  [Cro::HTTP] ok 2 - HTTP request parser consumes TCP messages
  [Cro::HTTP] ok 3 - HTTP request parser produces HTTP requests
  [Cro::HTTP] ok 4 - Malformed request line - only verb
  [Cro::HTTP] ok 5 - check 1
  [Cro::HTTP] ok 6 - Malformed request line - no version
  [Cro::HTTP] ok 7 - check 1
  [Cro::HTTP] ok 8 - Malformed request line - utter crap
  [Cro::HTTP] ok 9 - check 1
  [Cro::HTTP] ok 10 - Malformed HTTP version (1)
  [Cro::HTTP] ok 11 - check 1
  [Cro::HTTP] ok 12 - Malformed HTTP version (2)
  [Cro::HTTP] ok 13 - check 1
  [Cro::HTTP] ok 14 - Malformed HTTP version (3)
  [Cro::HTTP] ok 15 - check 1
  [Cro::HTTP] ok 16 - Malformed HTTP version (4)
  [Cro::HTTP] ok 17 - check 1
  [Cro::HTTP] ok 18 - Malformed HTTP version (5)
  [Cro::HTTP] ok 19 - check 1
  [Cro::HTTP] ok 20 - Unimplemented HTTP version
  [Cro::HTTP] ok 21 - check 1
  [Cro::HTTP] ok 22 - Simple GET request with no headers
  [Cro::HTTP] ok 23 - check 1
  [Cro::HTTP] ok 24 - check 2
  [Cro::HTTP] ok 25 - check 3
  [Cro::HTTP] ok 26 - Simple HEAD request with no headers
  [Cro::HTTP] ok 27 - check 1
  [Cro::HTTP] ok 28 - check 2
  [Cro::HTTP] ok 29 - check 3
  [Cro::HTTP] ok 30 - Simple POST request with no headers
  [Cro::HTTP] ok 31 - check 1
  [Cro::HTTP] ok 32 - check 2
  [Cro::HTTP] ok 33 - check 3
  [Cro::HTTP] ok 34 - Simple PUT request with no headers
  [Cro::HTTP] ok 35 - check 1
  [Cro::HTTP] ok 36 - check 2
  [Cro::HTTP] ok 37 - check 3
  [Cro::HTTP] ok 38 - Simple DELETE request with no headers
  [Cro::HTTP] ok 39 - check 1
  [Cro::HTTP] ok 40 - check 2
  [Cro::HTTP] ok 41 - check 3
  [Cro::HTTP] ok 42 - Simple OPTIONS request with no headers
  [Cro::HTTP] ok 43 - check 1
  [Cro::HTTP] ok 44 - check 2
  [Cro::HTTP] ok 45 - check 3
  [Cro::HTTP] ok 46 - The TRACE method, as it is not implemented by default
  [Cro::HTTP] ok 47 - check 1
  [Cro::HTTP] ok 48 - Simple PATCH request with no headers
  [Cro::HTTP] ok 49 - check 1
  [Cro::HTTP] ok 50 - check 2
  [Cro::HTTP] ok 51 - check 3
  [Cro::HTTP] ok 52 - The TRACE method, as it is not implemented by default
  [Cro::HTTP] ok 53 - check 1
  [Cro::HTTP] ok 54 - The TRACE method if included in allowed-methods
  [Cro::HTTP] ok 55 - check 1
  [Cro::HTTP] ok 56 - check 2
  [Cro::HTTP] ok 57 - check 3
  [Cro::HTTP] ok 58 - PUT when it is not included in the allowed methods
  [Cro::HTTP] ok 59 - check 1
  [Cro::HTTP] ok 60 - An empty line before the request line
  [Cro::HTTP] ok 61 - check 1
  [Cro::HTTP] ok 62 - check 2
  [Cro::HTTP] ok 63 - check 3
  [Cro::HTTP] ok 64 - A few empty lines before the request line
  [Cro::HTTP] ok 65 - check 1
  [Cro::HTTP] ok 66 - check 2
  [Cro::HTTP] ok 67 - check 3
  [Cro::HTTP] ok 68 - Host header
  [Cro::HTTP] ok 69 - check 1
  [Cro::HTTP] ok 70 - check 2
  [Cro::HTTP] ok 71 - check 3
  [Cro::HTTP] ok 72 - check 4
  [Cro::HTTP] ok 73 - check 5
  [Cro::HTTP] ok 74 - check 6
  [Cro::HTTP] ok 75 - check 7
  [Cro::HTTP] ok 76 - Host header with no whitespace
  [Cro::HTTP] ok 77 - check 1
  [Cro::HTTP] ok 78 - check 2
  [Cro::HTTP] ok 79 - check 3
  [Cro::HTTP] ok 80 - check 4
  [Cro::HTTP] ok 81 - check 5
  [Cro::HTTP] ok 82 - check 6
  [Cro::HTTP] ok 83 - check 7
  [Cro::HTTP] ok 84 - Host header with trailing whitespace
  [Cro::HTTP] ok 85 - check 1
  [Cro::HTTP] ok 86 - check 2
  [Cro::HTTP] ok 87 - check 3
  [Cro::HTTP] ok 88 - check 4
  [Cro::HTTP] ok 89 - check 5
  [Cro::HTTP] ok 90 - check 6
  [Cro::HTTP] ok 91 - check 7
  [Cro::HTTP] ok 92 - Host header with tab before and after value
  [Cro::HTTP] ok 93 - check 1
  [Cro::HTTP] ok 94 - check 2
  [Cro::HTTP] ok 95 - check 3
  [Cro::HTTP] ok 96 - check 4
  [Cro::HTTP] ok 97 - check 5
  [Cro::HTTP] ok 98 - check 6
  [Cro::HTTP] ok 99 - check 7
  [Cro::HTTP] ok 100 - Header with insane but actually totally legit name
  [Cro::HTTP] ok 101 - check 1
  [Cro::HTTP] ok 102 - check 2
  [Cro::HTTP] ok 103 - check 3
  [Cro::HTTP] ok 104 - check 4
  [Cro::HTTP] ok 105 - check 5
  [Cro::HTTP] ok 106 - check 6
  [Cro::HTTP] ok 107 - check 7
  [Cro::HTTP] ok 108 - Not allowed " in header
  [Cro::HTTP] ok 109 - check 1
  [Cro::HTTP] ok 110 - Not allowed ( in header
  [Cro::HTTP] ok 111 - check 1
  [Cro::HTTP] ok 112 - Not allowed ) in header
  [Cro::HTTP] ok 113 - check 1
  [Cro::HTTP] ok 114 - Not allowed [ in header
  [Cro::HTTP] ok 115 - check 1
  [Cro::HTTP] ok 116 - Not allowed ] in header
  [Cro::HTTP] ok 117 - check 1
  [Cro::HTTP] ok 118 - Not allowed { in header
  [Cro::HTTP] ok 119 - check 1
  [Cro::HTTP] ok 120 - Not allowed } in header
  [Cro::HTTP] ok 121 - check 1
  [Cro::HTTP] ok 122 - Not allowed @ in header
  [Cro::HTTP] ok 123 - check 1
  [Cro::HTTP] ok 124 - Not allowed \ in header
  [Cro::HTTP] ok 125 - check 1
  [Cro::HTTP] ok 126 - Not allowed / in header
  [Cro::HTTP] ok 127 - check 1
  [Cro::HTTP] ok 128 - Not allowed < in header
  [Cro::HTTP] ok 129 - check 1
  [Cro::HTTP] ok 130 - Not allowed > in header
  [Cro::HTTP] ok 131 - check 1
  [Cro::HTTP] ok 132 - Not allowed , in header
  [Cro::HTTP] ok 133 - check 1
  [Cro::HTTP] ok 134 - Not allowed ; in header
  [Cro::HTTP] ok 135 - check 1
  [Cro::HTTP] ok 136 - Header with empty field
  [Cro::HTTP] ok 137 - check 1
  [Cro::HTTP] ok 138 - check 2
  [Cro::HTTP] ok 139 - check 3
  [Cro::HTTP] ok 140 - check 4
  [Cro::HTTP] ok 141 - check 5
  [Cro::HTTP] ok 142 - check 6
  [Cro::HTTP] ok 143 - check 7
  [Cro::HTTP] ok 144 - Field value can be any printable char including latin-1 range
  [Cro::HTTP] ok 145 - check 1
  [Cro::HTTP] ok 146 - check 2
  [Cro::HTTP] ok 147 - check 3
  [Cro::HTTP] ok 148 - check 4
  [Cro::HTTP] ok 149 - check 5
  [Cro::HTTP] ok 150 - check 6
  [Cro::HTTP] ok 151 - check 7
  [Cro::HTTP] ok 152 - Field values may have whitespace in them
  [Cro::HTTP] ok 153 - check 1
  [Cro::HTTP] ok 154 - check 2
  [Cro::HTTP] ok 155 - check 3
  [Cro::HTTP] ok 156 - check 4
  [Cro::HTTP] ok 157 - check 5
  [Cro::HTTP] ok 158 - check 6
  [Cro::HTTP] ok 159 - check 7
  [Cro::HTTP] ok 160 - Whitespace after field name ignored
  [Cro::HTTP] ok 161 - check 1
  [Cro::HTTP] ok 162 - check 2
  [Cro::HTTP] ok 163 - check 3
  [Cro::HTTP] ok 164 - check 4
  [Cro::HTTP] ok 165 - check 5
  [Cro::HTTP] ok 166 - check 6
  [Cro::HTTP] ok 167 - check 7
  [Cro::HTTP] ok 168 - Control chars other than space/tab not allowed (0)
  [Cro::HTTP] ok 169 - check 1
  [Cro::HTTP] ok 170 - Control chars other than space/tab not allowed (1)
  [Cro::HTTP] ok 171 - check 1
  [Cro::HTTP] ok 172 - Request with multiple headers (example from RFC)
  [Cro::HTTP] ok 173 - check 1
  [Cro::HTTP] ok 174 - check 2
  [Cro::HTTP] ok 175 - check 3
  [Cro::HTTP] ok 176 - check 4
  [Cro::HTTP] ok 177 - check 5
  [Cro::HTTP] ok 178 - check 6
  [Cro::HTTP] ok 179 - check 7
  [Cro::HTTP] ok 180 - check 8
  [Cro::HTTP] ok 181 - check 9
  [Cro::HTTP] ok 182 - check 10
  [Cro::HTTP] ok 183 - check 11
  [Cro::HTTP] ok 184 - check 12
  [Cro::HTTP] ok 185 - check 13
  [Cro::HTTP] ok 186 - Request path and path segments for /hello.txt
  [Cro::HTTP] ok 187 - check 1
  [Cro::HTTP] ok 188 - check 2
  [Cro::HTTP] ok 189 - Request path and path segments for /oh/my/path
  [Cro::HTTP] ok 190 - check 1
  [Cro::HTTP] ok 191 - check 2
  [Cro::HTTP] ok 192 - Query strings are parsed and accessible
  [Cro::HTTP] ok 193 - check 1
  [Cro::HTTP] ok 194 - check 2
  [Cro::HTTP] ok 195 - check 3
  [Cro::HTTP] ok 196 - check 4
  [Cro::HTTP] ok 197 - check 5
  [Cro::HTTP] ok 198 - check 6
  [Cro::HTTP] ok 199 - check 7
  [Cro::HTTP] ok 200 - Query strings with empty values
  [Cro::HTTP] ok 201 - check 1
  [Cro::HTTP] ok 202 - check 2
  [Cro::HTTP] ok 203 - check 3
  [Cro::HTTP] ok 204 - check 4
  [Cro::HTTP] ok 205 - check 5
  [Cro::HTTP] ok 206 - check 6
  [Cro::HTTP] ok 207 - check 7
  [Cro::HTTP] ok 208 - Query string keys and values that are encoded
  [Cro::HTTP] ok 209 - check 1
  [Cro::HTTP] ok 210 - check 2
  [Cro::HTTP] ok 211 - check 3
  [Cro::HTTP] ok 212 - check 4
  [Cro::HTTP] ok 213 - check 5
  [Cro::HTTP] ok 214 - check 6
  [Cro::HTTP] ok 215 - check 7
  [Cro::HTTP] ok 216 - Query strings with multiple values for the same key
  [Cro::HTTP] ok 217 - check 1
  [Cro::HTTP] ok 218 - check 2
  [Cro::HTTP] ok 219 - check 3
  [Cro::HTTP] ok 220 - check 4
  [Cro::HTTP] ok 221 - check 5
  [Cro::HTTP] ok 222 - check 6
  [Cro::HTTP] ok 223 - check 7
  [Cro::HTTP] ok 224 - check 8
  [Cro::HTTP] ok 225 - check 9
  [Cro::HTTP] ok 226 - Request with body, length specified by content-length
  [Cro::HTTP] ok 227 - check 1
  [Cro::HTTP] ok 228 - check 2
  [Cro::HTTP] ok 229 - check 3
  [Cro::HTTP] ok 230 - Request with body, sent with chunked encoding
  [Cro::HTTP] ok 231 - check 1
  [Cro::HTTP] ok 232 - check 2
  [Cro::HTTP] ok 233 - check 3
  [Cro::HTTP] ok 234 - A text/whatever request with body
  [Cro::HTTP] ok 235 - text/whatever gives string body
  [Cro::HTTP] ok 236 - Body contains the correct value
  [Cro::HTTP] ok 237 - A unknown/foo request with body
  [Cro::HTTP] ok 238 - unknown/foo .body gives Blob
  [Cro::HTTP] ok 239 - Blob has correct content
  [Cro::HTTP] ok 240 - Basic case of application/x-www-form-urlencoded
  [Cro::HTTP] ok 241 - .pairs returns ordered pairs from the decoded body
  [Cro::HTTP] ok 242 - .list returns ordered pairs from the decoded body
  [Cro::HTTP] ok 243 - .hash returns hash of the decoded body
  [Cro::HTTP] ok 244 - Can index associatively (1)
  [Cro::HTTP] ok 245 - Can index associatively (2)
  [Cro::HTTP] ok 246 - Can index associatively (3)
  [Cro::HTTP] ok 247 - Can index associatively with :exists (1)
  [Cro::HTTP] ok 248 - Can index associatively with :exists (2)
  [Cro::HTTP] ok 249 - Can index associatively with :exists (3)
  [Cro::HTTP] ok 250 - Multiple entries with same name in application/x-www-form-urlencoded
  [Cro::HTTP] ok 251 - .pairs returns ordered pairs, with multiple values in place
  [Cro::HTTP] ok 252 - .list returns ordered pairs, with muliplte values in place
  [Cro::HTTP] ok 253 - .hash gives back Hash with 3 elements
  [Cro::HTTP] ok 254 - Get back a HTTP multi-value (1)
  [Cro::HTTP] ok 255 - Get back a HTTP multi-value (2)
  [Cro::HTTP] ok 256 - Stringifying multi-value is correct (1)
  [Cro::HTTP] ok 257 - Stringifying multi-value is correct (2)
  [Cro::HTTP] ok 258 - Indexing multi-value is correct (1)
  [Cro::HTTP] ok 259 - Indexing multi-value is correct (2)
  [Cro::HTTP] ok 260 - When only one value with the name, get back a Str
  [Cro::HTTP] ok 261 - Value is correct
  [Cro::HTTP] ok 262 - Hash-indexing body gives HTTP multi-value (1)
  [Cro::HTTP] ok 263 - Hash-indexing body gives HTTP multi-value (2)
  [Cro::HTTP] ok 264 - Except when only one value for the name, then it is Str
  [Cro::HTTP] ok 265 - Charset present in content-type header field after application/x-www-form-urlencoded
  [Cro::HTTP] ok 266 - WWWUrlEncode prasers works correct with charset in content-type
  [Cro::HTTP] ok 267 - WWWFormUrlEncoded with empty body
  [Cro::HTTP] ok 268 - test `with message.content-type` returns Boolean
  [Cro::HTTP] ok 269 - Basic %-encoded things in an application/x-www-form-urlencoded
  [Cro::HTTP] ok 270 - %-encoded values in ASCII range handled correctly
  [Cro::HTTP] ok 271 - %-encoded non-ASCII is utf-8 by default in  application/x-www-form-urlencoded
  [Cro::HTTP] ok 272 - %-encoded values default to UTF-8 decoding
  [Cro::HTTP] ok 273 - Can pick default encoding for application/x-www-form-urlencoded
  [Cro::HTTP] ok 274 - 
  [Cro::HTTP] ok 275 - 
  [Cro::HTTP] ok 276 - %-encoded values handled correctly when default set to latin-1
  [Cro::HTTP] ok 277 - 
  [Cro::HTTP] ok 278 - 
  [Cro::HTTP] ok 279 - Respects encoding set by _charset_ in application/x-www-form-urlencoded
  [Cro::HTTP] ok 280 - %-encoded values decoded as latin-1 as set in _charset_
  [Cro::HTTP] ok 281 - A _charset_ in application/x-www-form-urlencoded overrides configured default
  [Cro::HTTP] ok 282 - Values were decoded as utf-8, not latin-1 default, due to _charset_
  [Cro::HTTP] ok 283 - No errors on keys with empty value or missing value
  [Cro::HTTP] ok 284 - 
  [Cro::HTTP] ok 285 - Simple multipart/form-data
  [Cro::HTTP] ok 286 - First part has 1 header
  [Cro::HTTP] ok 287 - First part header name correct
  [Cro::HTTP] ok 288 - First part header value correct
  [Cro::HTTP] ok 289 - First part has a content-type that is a Cro::MediaType
  [Cro::HTTP] ok 290 - First part has default text type
  [Cro::HTTP] ok 291 - First part has default plain subtype
  [Cro::HTTP] ok 292 - First part has correct field name
  [Cro::HTTP] ok 293 - First part has correct body blob
  [Cro::HTTP] ok 294 - First part has correct body text
  [Cro::HTTP] ok 295 - First part has correct body
  [Cro::HTTP] ok 296 - Second part has 1 header
  [Cro::HTTP] ok 297 - Second part header name correct
  [Cro::HTTP] ok 298 - Second part header value correct
  [Cro::HTTP] ok 299 - Second part has correct field name
  [Cro::HTTP] ok 300 - Second part has a content-type that is a Cro::MediaType
  [Cro::HTTP] ok 301 - Second part has default text type
  [Cro::HTTP] ok 302 - Second part has default plain subtype
  [Cro::HTTP] ok 303 - Second part has correct body blob
  [Cro::HTTP] ok 304 - Second part has correct body text
  [Cro::HTTP] ok 305 - Second part has correct body
  [Cro::HTTP] ok 306 - A multipart/form-data with a file upload
  [Cro::HTTP] ok 307 - Have 2 parts
  [Cro::HTTP] ok 308 - First part has 1 header
  [Cro::HTTP] ok 309 - First part header name correct
  [Cro::HTTP] ok 310 - First part header value correct
  [Cro::HTTP] ok 311 - First part has a content-type that is a Cro::MediaType
  [Cro::HTTP] ok 312 - First part has default text type
  [Cro::HTTP] ok 313 - First part has default plain subtype
  [Cro::HTTP] ok 314 - First part has correct field name
  [Cro::HTTP] ok 315 - First part has no filename
  [Cro::HTTP] ok 316 - First part has correct body text
  [Cro::HTTP] ok 317 - First part has correct body
  [Cro::HTTP] ok 318 - Second part has 2 headers
  [Cro::HTTP] ok 319 - First header name correct
  [Cro::HTTP] ok 320 - First header value correct
  [Cro::HTTP] ok 321 - Second header name correct
  [Cro::HTTP] ok 322 - Second header value correct
  [Cro::HTTP] ok 323 - Second part has a content-type that is a Cro::MediaType
  [Cro::HTTP] ok 324 - Second part has image media type
  [Cro::HTTP] ok 325 - Second part has gif media subtype
  [Cro::HTTP] ok 326 - Second part has correct field name
  [Cro::HTTP] ok 327 - Second part has correct filename
  [Cro::HTTP] ok 328 - Second part has correct body blob
  [Cro::HTTP] ok 329 - Second part has correct body
  [Cro::HTTP] ok 330 - An application/json request decodes JSON body
  [Cro::HTTP] ok 331 - .body of application/json with object gives Hash
  [Cro::HTTP] ok 332 - JSON was correctly decoded
  [Cro::HTTP] ok 333 - An media type with the +json suffix decodes JSON body
  [Cro::HTTP] ok 334 - .body of application/vnd.my-org+json with object gives Hash
  [Cro::HTTP] ok 335 - JSON was correctly decoded
  [Cro::HTTP] ok 336 - check first 1
  [Cro::HTTP] ok 337 - check second 1
  [Cro::HTTP] ok 338 - Two separate packages are parsed
  [Cro::HTTP] ok 339 - check first 1
  [Cro::HTTP] ok 340 - check second 1
  [Cro::HTTP] ok 341 - Two separate packages are parsed, RequestLine in the first
  [Cro::HTTP] ok 342 - check first 1
  [Cro::HTTP] ok 343 - check second 1
  [Cro::HTTP] ok 344 - Two separate packages are parsed, RequestLine and part of header in the first
  [Cro::HTTP] 1..344
  [Cro::HTTP] Saw 1 occurrence of deprecated code.
  [Cro::HTTP] ================================================================================
  [Cro::HTTP] Method perl (from Mu) seen at:
  [Cro::HTTP]   /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist/lib/Cro/HTTP/Body.rakumod (Cro::HTTP::Body), line 38
  [Cro::HTTP] Please use raku instead.
  [Cro::HTTP] --------------------------------------------------------------------------------
  [Cro::HTTP] Please contact the author to have these occurrences of deprecated code
  [Cro::HTTP] adapted, so that this message will disappear!
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request-serializer.rakutest
  [Cro::HTTP] ok 1 - Basic request with no Host header uses HTTP/1.0
  [Cro::HTTP] ok 2 - Basic request with Host header uses HTTP/1.1
  [Cro::HTTP] ok 3 - Basic request with blob body adds application/octet-stream and length
  [Cro::HTTP] ok 4 - Basic request with blob body does not replace existing content-type
  [Cro::HTTP] ok 5 - Basic request with string body adds text/plain and length
  [Cro::HTTP] ok 6 - Basic request with string body does not replace existing content-type
  [Cro::HTTP] ok 7 - application/json content serializes Hash to JSON
  [Cro::HTTP] ok 8 - application/json content serializes Array to JSON
  [Cro::HTTP] ok 9 - Media type with +json suffix also serializes JSON
  [Cro::HTTP] ok 10 - application/x-www-form-urlencoded with list of pairs
  [Cro::HTTP] ok 11 - application/x-www-form-urlencoded with ASCII things needing escaping
  [Cro::HTTP] ok 12 - application/x-www-form-urlencoded with ASCII things needing escaping
  [Cro::HTTP] ok 13 - application/x-www-form-urlencoded with hash
  [Cro::HTTP] ok 14 - application/x-www-form-urlencoded with body object
  [Cro::HTTP] ok 15 - application/x-www-form-urlencoded body object implies header
  [Cro::HTTP] ok 16 - multipart/form-data with list of pairs
  [Cro::HTTP] ok 17 - multipart/form-data with filename and extra header
  [Cro::HTTP] 1..17
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request.rakutest
  [Cro::HTTP] # Subtest: Request missing method and target throws on .Str
  [Cro::HTTP]     1..2
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Request::Incomplete)
  [Cro::HTTP] ok 1 - Request missing method and target throws on .Str
  [Cro::HTTP] # Subtest: Request missing target throws on .Str
  [Cro::HTTP]     1..2
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Request::Incomplete)
  [Cro::HTTP] ok 2 - Request missing target throws on .Str
  [Cro::HTTP] # Subtest: Request missing method throws on .Str
  [Cro::HTTP]     1..2
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Request::Incomplete)
  [Cro::HTTP] ok 3 - Request missing method throws on .Str
  [Cro::HTTP] ok 4 - Can serialize simple request built with accessors (HTTP/1.0 with no Host)
  [Cro::HTTP] ok 5 - Can serialize simple request with method/target in constructor (HTTP/1.0 with no Host)
  [Cro::HTTP] ok 6 - Lowercase method not allowed
  [Cro::HTTP] ok 7 - Mixed case method not allowed
  [Cro::HTTP] ok 8 - Method with space not allowed
  [Cro::HTTP] ok 9 - Target with space in not allowed
  [Cro::HTTP] ok 10 - Target with newline in not allowed
  [Cro::HTTP] ok 11 - Target with control char not allowed
  [Cro::HTTP] ok 12 - Target with non-Latin-1 characters not allowed
  [Cro::HTTP] ok 13 - Request with Host header will use HTTP/1.1
  [Cro::HTTP] ok 14 - Request header constructed with single-arg append-header overload works
  [Cro::HTTP] ok 15 - Refuses to add request header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 16 - Refuses to add request header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 17 - Refuses to add request header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 18 - Refuses to add request header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 19 - Refuses to add request header with illegal name containing " (single-arg)
  [Cro::HTTP] ok 20 - Refuses to add request header with illegal name containing ( (single-arg)
  [Cro::HTTP] ok 21 - Refuses to add request header with illegal name containing ) (single-arg)
  [Cro::HTTP] ok 22 - Refuses to add request header with illegal name containing [ (single-arg)
  [Cro::HTTP] ok 23 - Refuses to add request header with illegal name containing ] (single-arg)
  [Cro::HTTP] ok 24 - Refuses to add request header with illegal name containing { (single-arg)
  [Cro::HTTP] ok 25 - Refuses to add request header with illegal name containing } (single-arg)
  [Cro::HTTP] ok 26 - Refuses to add request header with illegal name containing @ (single-arg)
  [Cro::HTTP] ok 27 - Refuses to add request header with illegal name containing \ (single-arg)
  [Cro::HTTP] ok 28 - Refuses to add request header with illegal name containing / (single-arg)
  [Cro::HTTP] ok 29 - Refuses to add request header with illegal name containing < (single-arg)
  [Cro::HTTP] ok 30 - Refuses to add request header with illegal name containing > (single-arg)
  [Cro::HTTP] ok 31 - Refuses to add request header with illegal name containing , (single-arg)
  [Cro::HTTP] ok 32 - Refuses to add request header with illegal name containing ; (single-arg)
  [Cro::HTTP] ok 33 - Utterly crazy but valid header can be added (single-arg)
  [Cro::HTTP] ok 34 - Request header constructed with two-arg append-header overload works
  [Cro::HTTP] ok 35 - Refuses to add request header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 36 - Refuses to add request header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 37 - Refuses to add request header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 38 - Refuses to add request header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 39 - Refuses to add request header with illegal name containing " (two-arg)
  [Cro::HTTP] ok 40 - Refuses to add request header with illegal name containing ( (two-arg)
  [Cro::HTTP] ok 41 - Refuses to add request header with illegal name containing ) (two-arg)
  [Cro::HTTP] ok 42 - Refuses to add request header with illegal name containing [ (two-arg)
  [Cro::HTTP] ok 43 - Refuses to add request header with illegal name containing ] (two-arg)
  [Cro::HTTP] ok 44 - Refuses to add request header with illegal name containing { (two-arg)
  [Cro::HTTP] ok 45 - Refuses to add request header with illegal name containing } (two-arg)
  [Cro::HTTP] ok 46 - Refuses to add request header with illegal name containing @ (two-arg)
  [Cro::HTTP] ok 47 - Refuses to add request header with illegal name containing \ (two-arg)
  [Cro::HTTP] ok 48 - Refuses to add request header with illegal name containing / (two-arg)
  [Cro::HTTP] ok 49 - Refuses to add request header with illegal name containing < (two-arg)
  [Cro::HTTP] ok 50 - Refuses to add request header with illegal name containing > (two-arg)
  [Cro::HTTP] ok 51 - Refuses to add request header with illegal name containing , (two-arg)
  [Cro::HTTP] ok 52 - Refuses to add request header with illegal name containing ; (two-arg)
  [Cro::HTTP] ok 53 - Utterly crazy but valid header can be added (two-arg)
  [Cro::HTTP] ok 54 - has-header returns True on header we have
  [Cro::HTTP] ok 55 - has-header is not case-sensitive (1)
  [Cro::HTTP] ok 56 - has-header is not case-sensitive (2)
  [Cro::HTTP] ok 57 - has-header returns False on header we do not have
  [Cro::HTTP] ok 58 - header method fetches a header
  [Cro::HTTP] ok 59 - header method is not case sensitive (1)
  [Cro::HTTP] ok 60 - header method is not case sensitive (2)
  [Cro::HTTP] ok 61 - when there are multiple headers with the name, the value comma-joins them
  [Cro::HTTP] ok 62 - header we do not have returns Nil
  [Cro::HTTP] ok 63 - header-list method returns a List of one header for Host
  [Cro::HTTP] ok 64 - header-list method works case-insensitively
  [Cro::HTTP] ok 65 - header-list method returns a list of values when there are multiple headers
  [Cro::HTTP] ok 66 - header-list methods returns an empty list when no header of the requested name
  [Cro::HTTP] ok 67 - Removing single Host header returns 1
  [Cro::HTTP] ok 68 - Host header was really removed
  [Cro::HTTP] ok 69 - Removing 2 accept-language headers returns 2
  [Cro::HTTP] ok 70 - Headers really removed
  [Cro::HTTP] ok 71 - Removing single header matched by predicate works
  [Cro::HTTP] ok 72 - Header identified by predicate was really removed
  [Cro::HTTP] ok 73 - Removing an exact header returns 1
  [Cro::HTTP] ok 74 - Headers really removed
  [Cro::HTTP] not ok 75 - 
  [Cro::HTTP] # Failed test at t/http-request.rakutest line 162
  [Cro::HTTP] # expected: $(:jp(1), :cs(1), :fr(1), :mi(0.8), :en(0.7), :kr(0))
  [Cro::HTTP] #      got: $[:jp(1), :cs(1), :fr(1), :mi(0.8), :en(0.7), :kr(0)]
  [Cro::HTTP] ok 76 - content-type method returns a Cro::MediaType when there is a content-type header
  [Cro::HTTP] ok 77 - Correct type
  [Cro::HTTP] ok 78 - Correct subtype
  [Cro::HTTP] ok 79 - Correct parameters list
  [Cro::HTTP] ok 80 - content-type returns Nil when no header
  [Cro::HTTP] ok 81 - has-cookie on non-existent cookie returns False
  [Cro::HTTP] ok 82 - cookie-value on non-existent cookie returns Nil
  [Cro::HTTP] ok 83 - cookie-hash returns empty hash when cookies not set
  [Cro::HTTP] ok 84 - Can add cookie
  [Cro::HTTP] ok 85 - has-cookie on added cookie returns True
  [Cro::HTTP] ok 86 - cookie-value on added cookie returns correct value
  [Cro::HTTP] ok 87 - cookie-hash returns correct result
  [Cro::HTTP] ok 88 - Can update cookie
  [Cro::HTTP] ok 89 - has-cookie on updated cookie returns True
  [Cro::HTTP] ok 90 - cookie-value on updated cookie returns correct value
  [Cro::HTTP] ok 91 - Can remove cookie
  [Cro::HTTP] ok 92 - Removed cookie is removed
  [Cro::HTTP] ok 93 - Empty names are not permitted
  [Cro::HTTP] ok 94 - Cookie header looks good
  [Cro::HTTP] ok 95 - lang cookie header should not be parsed for HTTP 1.1
  [Cro::HTTP] ok 96 - lang cookie header should be parsed for HTTP 2
  [Cro::HTTP] ok 97 - Can cope with trailing ; in cookie line
  [Cro::HTTP] ok 98 - Target is set
  [Cro::HTTP] ok 99 - original-target equals target
  [Cro::HTTP] ok 100 - original-path path equals target
  [Cro::HTTP] ok 101 - original-path-segments are equal to target segments
  [Cro::HTTP] ok 102 - target on stripped request changes
  [Cro::HTTP] ok 103 - original-target preserves
  [Cro::HTTP] ok 104 - original-path preserves
  [Cro::HTTP] ok 105 - original-path-segments are preserved
  [Cro::HTTP] ok 106 - target on second stripped request changes
  [Cro::HTTP] ok 107 - original-target preserves
  [Cro::HTTP] ok 108 - original-path preserves
  [Cro::HTTP] ok 109 - original-path-segments are preserved
  [Cro::HTTP] 1..109
  [Cro::HTTP] # You failed 1 test of 109
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response-parser.rakutest
  [Cro::HTTP] ok 1 - HTTP response parser is a transform
  [Cro::HTTP] ok 2 - HTTP response parser consumes TCP messages
  [Cro::HTTP] ok 3 - HTTP respose parser produces HTTP responses
  [Cro::HTTP] ok 4 - Simple 204 no content response
  [Cro::HTTP] ok 5 - check 1
  [Cro::HTTP] ok 6 - check 2
  [Cro::HTTP] ok 7 - Malformed status line - only version
  [Cro::HTTP] ok 8 - Malformed status line - missing space after status code
  [Cro::HTTP] ok 9 - Simple 204 no content response with empty reason
  [Cro::HTTP] ok 10 - check 1
  [Cro::HTTP] ok 11 - check 2
  [Cro::HTTP] ok 12 - Malformed status line - code is only one digit
  [Cro::HTTP] ok 13 - Malformed status line - code is only two digits
  [Cro::HTTP] ok 14 - Malformed status line - code is four digits
  [Cro::HTTP] ok 15 - Minor version other than 1 OK (1)
  [Cro::HTTP] ok 16 - check 1
  [Cro::HTTP] ok 17 - check 2
  [Cro::HTTP] ok 18 - Minor version other than 1 OK (2)
  [Cro::HTTP] ok 19 - check 1
  [Cro::HTTP] ok 20 - check 2
  [Cro::HTTP] ok 21 - Invalid major version (1)
  [Cro::HTTP] ok 22 - Invalid major version (2)
  [Cro::HTTP] ok 23 - Double-digit minor version
  [Cro::HTTP] ok 24 - All non-controls allowed in reason
  [Cro::HTTP] ok 25 - check 1
  [Cro::HTTP] ok 26 - check 2
  [Cro::HTTP] ok 27 - Control chars in reason (0)
  [Cro::HTTP] ok 28 - Control chars in reason (1)
  [Cro::HTTP] ok 29 - Single simple header
  [Cro::HTTP] ok 30 - check 1
  [Cro::HTTP] ok 31 - check 2
  [Cro::HTTP] ok 32 - check 3
  [Cro::HTTP] ok 33 - check 4
  [Cro::HTTP] ok 34 - check 5
  [Cro::HTTP] ok 35 - Single header without whitespace
  [Cro::HTTP] ok 36 - check 1
  [Cro::HTTP] ok 37 - check 2
  [Cro::HTTP] ok 38 - check 3
  [Cro::HTTP] ok 39 - check 4
  [Cro::HTTP] ok 40 - check 5
  [Cro::HTTP] ok 41 - Single header with trailing whitespace
  [Cro::HTTP] ok 42 - check 1
  [Cro::HTTP] ok 43 - check 2
  [Cro::HTTP] ok 44 - check 3
  [Cro::HTTP] ok 45 - check 4
  [Cro::HTTP] ok 46 - check 5
  [Cro::HTTP] ok 47 - Host header with tab before and after value
  [Cro::HTTP] ok 48 - check 1
  [Cro::HTTP] ok 49 - check 2
  [Cro::HTTP] ok 50 - check 3
  [Cro::HTTP] ok 51 - check 4
  [Cro::HTTP] ok 52 - check 5
  [Cro::HTTP] ok 53 - Header with insane but actually totally legit name
  [Cro::HTTP] ok 54 - check 1
  [Cro::HTTP] ok 55 - check 2
  [Cro::HTTP] ok 56 - check 3
  [Cro::HTTP] ok 57 - check 4
  [Cro::HTTP] ok 58 - check 5
  [Cro::HTTP] ok 59 - Not allowed " in header name
  [Cro::HTTP] ok 60 - Not allowed ( in header name
  [Cro::HTTP] ok 61 - Not allowed ) in header name
  [Cro::HTTP] ok 62 - Not allowed [ in header name
  [Cro::HTTP] ok 63 - Not allowed ] in header name
  [Cro::HTTP] ok 64 - Not allowed { in header name
  [Cro::HTTP] ok 65 - Not allowed } in header name
  [Cro::HTTP] ok 66 - Not allowed @ in header name
  [Cro::HTTP] ok 67 - Not allowed \ in header name
  [Cro::HTTP] ok 68 - Not allowed / in header name
  [Cro::HTTP] ok 69 - Not allowed < in header name
  [Cro::HTTP] ok 70 - Not allowed > in header name
  [Cro::HTTP] ok 71 - Not allowed , in header name
  [Cro::HTTP] ok 72 - Not allowed ; in header name
  [Cro::HTTP] ok 73 - Header field value can be any printable char including latin-1 range
  [Cro::HTTP] ok 74 - check 1
  [Cro::HTTP] ok 75 - check 2
  [Cro::HTTP] ok 76 - check 3
  [Cro::HTTP] ok 77 - check 4
  [Cro::HTTP] ok 78 - check 5
  [Cro::HTTP] ok 79 - check 6
  [Cro::HTTP] ok 80 - Single header with whitespace in value
  [Cro::HTTP] ok 81 - check 1
  [Cro::HTTP] ok 82 - check 2
  [Cro::HTTP] ok 83 - check 3
  [Cro::HTTP] ok 84 - check 4
  [Cro::HTTP] ok 85 - check 5
  [Cro::HTTP] ok 86 - Response with multiple headers and content-length body (example from RFC)
  [Cro::HTTP] ok 87 - check 1
  [Cro::HTTP] ok 88 - check 2
  [Cro::HTTP] ok 89 - check 3
  [Cro::HTTP] ok 90 - check 4
  [Cro::HTTP] ok 91 - check 5
  [Cro::HTTP] ok 92 - check 6
  [Cro::HTTP] ok 93 - check 7
  [Cro::HTTP] ok 94 - check 8
  [Cro::HTTP] ok 95 - check 9
  [Cro::HTTP] ok 96 - check 10
  [Cro::HTTP] ok 97 - check 11
  [Cro::HTTP] ok 98 - check 12
  [Cro::HTTP] ok 99 - check 13
  [Cro::HTTP] ok 100 - check 14
  [Cro::HTTP] ok 101 - check 15
  [Cro::HTTP] ok 102 - check 16
  [Cro::HTTP] ok 103 - check 17
  [Cro::HTTP] ok 104 - check 18
  [Cro::HTTP] ok 105 - check 19
  [Cro::HTTP] ok 106 - check 20
  [Cro::HTTP] ok 107 - Response with body terminated by close of connection
  [Cro::HTTP] ok 108 - check 1
  [Cro::HTTP] ok 109 - check 2
  [Cro::HTTP] ok 110 - check 3
  [Cro::HTTP] ok 111 - check 4
  [Cro::HTTP] ok 112 - Connection close with incomplete body throws
  [Cro::HTTP] ok 113 - check 1
  [Cro::HTTP] ok 114 - check 2
  [Cro::HTTP] ok 115 - check 3
  [Cro::HTTP] ok 116 - check 4
  [Cro::HTTP] ok 117 - Response with chunked encoding
  [Cro::HTTP] ok 118 - check 1
  [Cro::HTTP] ok 119 - check 2
  [Cro::HTTP] ok 120 - check 3
  [Cro::HTTP] ok 121 - check 4
  [Cro::HTTP] ok 122 - A text/whatever response has Str .body
  [Cro::HTTP] ok 123 - check 1
  [Cro::HTTP] ok 124 - A unknown/foo response has Blob .body
  [Cro::HTTP] ok 125 - check 1
  [Cro::HTTP] ok 126 - charset in content-type is respected by body-text
  [Cro::HTTP] ok 127 - check 1
  [Cro::HTTP] ok 128 - check 2
  [Cro::HTTP] ok 129 - check 3
  [Cro::HTTP] ok 130 - check 4
  [Cro::HTTP] ok 131 - A UTF-8 BOM is respected and stripped
  [Cro::HTTP] ok 132 - check 1
  [Cro::HTTP] ok 133 - check 2
  [Cro::HTTP] ok 134 - check 3
  [Cro::HTTP] ok 135 - check 4
  [Cro::HTTP] ok 136 - A UTF-16 LE BOM is respected and stripped
  [Cro::HTTP] ok 137 - check 1
  [Cro::HTTP] ok 138 - check 2
  [Cro::HTTP] ok 139 - check 3
  [Cro::HTTP] ok 140 - check 4
  [Cro::HTTP] ok 141 - A UTF-16 BE BOM is respected and stripped
  [Cro::HTTP] ok 142 - check 1
  [Cro::HTTP] ok 143 - check 2
  [Cro::HTTP] ok 144 - check 3
  [Cro::HTTP] ok 145 - check 4
  [Cro::HTTP] ok 146 - With not other indications, and it utf-8 fails, decode as latin-1
  [Cro::HTTP] ok 147 - check 1
  [Cro::HTTP] ok 148 - check 2
  [Cro::HTTP] ok 149 - check 3
  [Cro::HTTP] ok 150 - check 4
  [Cro::HTTP] ok 151 - An application/json response decodes JSON body
  [Cro::HTTP] ok 152 - .body of application/json with object gives Hash
  [Cro::HTTP] ok 153 - JSON was correctly decoded
  [Cro::HTTP] ok 154 - A media type with the +json suffix decodes JSON body
  [Cro::HTTP] ok 155 - .body of application/vnd.my-org+json with object gives Hash
  [Cro::HTTP] ok 156 - JSON was correctly decoded
  [Cro::HTTP] 1..156
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response-serializer.rakutest
  [Cro::HTTP] ok 1 - Basic 204 status response serialized correctly
  [Cro::HTTP] ok 2 - 200 response with body readily available emits Content-length
  [Cro::HTTP] ok 3 - 200 response with streaming body does chunked encoding
  [Cro::HTTP] ok 4 - Chunked encoding not messed up by empty blobs
  [Cro::HTTP] ok 5 - application/json encodes Hash as JSON
  [Cro::HTTP] ok 6 - application/json encodes Array as JSON
  [Cro::HTTP] ok 7 - application/vnd.foobar+json encodes Hash as JSON
  [Cro::HTTP] 1..7
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response.rakutest
  [Cro::HTTP] ok 1 - Unconfigured HTTP response is HTTP/1.1 and 204 status
  [Cro::HTTP] ok 2 - Setting status in constructor includes it in the response
  [Cro::HTTP] ok 3 - Setting status and version in constructor includes it in the response
  [Cro::HTTP] ok 4 - Setting status and version attributes includes them in the response
  [Cro::HTTP] ok 5 - Status of 10 is invalid
  [Cro::HTTP] ok 6 - Status of 99 is invalid
  [Cro::HTTP] ok 7 - Status of 1000 is invalid
  [Cro::HTTP] ok 8 - Status of 4004 is invalid
  [Cro::HTTP] ok 9 - Headers are included in the response
  [Cro::HTTP] ok 10 - has-header returns True on header we have
  [Cro::HTTP] ok 11 - has-header is not case-sensitive (1)
  [Cro::HTTP] ok 12 - has-header is not case-sensitive (2)
  [Cro::HTTP] ok 13 - has-header returns False on header we do not have
  [Cro::HTTP] ok 14 - header method fetches a header
  [Cro::HTTP] ok 15 - header method is not case sensitive (1)
  [Cro::HTTP] ok 16 - header method is not case sensitive (2)
  [Cro::HTTP] ok 17 - header method returns Nil on header we do not have
  [Cro::HTTP] ok 18 - Refuses to add response header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 19 - Refuses to add response header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 20 - Refuses to add response header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 21 - Refuses to add response header with illegal control char in value (single-arg)
  [Cro::HTTP] ok 22 - Refuses to add response header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 23 - Refuses to add response header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 24 - Refuses to add response header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 25 - Refuses to add response header with illegal control char in value (two-arg)
  [Cro::HTTP] ok 26 - Refuses to add response header with illegal name containing " (single-arg)
  [Cro::HTTP] ok 27 - Refuses to add response header with illegal name containing ( (single-arg)
  [Cro::HTTP] ok 28 - Refuses to add response header with illegal name containing ) (single-arg)
  [Cro::HTTP] ok 29 - Refuses to add response header with illegal name containing [ (single-arg)
  [Cro::HTTP] ok 30 - Refuses to add response header with illegal name containing ] (single-arg)
  [Cro::HTTP] ok 31 - Refuses to add response header with illegal name containing { (single-arg)
  [Cro::HTTP] ok 32 - Refuses to add response header with illegal name containing } (single-arg)
  [Cro::HTTP] ok 33 - Refuses to add response header with illegal name containing @ (single-arg)
  [Cro::HTTP] ok 34 - Refuses to add response header with illegal name containing \ (single-arg)
  [Cro::HTTP] ok 35 - Refuses to add response header with illegal name containing / (single-arg)
  [Cro::HTTP] ok 36 - Refuses to add response header with illegal name containing < (single-arg)
  [Cro::HTTP] ok 37 - Refuses to add response header with illegal name containing > (single-arg)
  [Cro::HTTP] ok 38 - Refuses to add response header with illegal name containing , (single-arg)
  [Cro::HTTP] ok 39 - Refuses to add response header with illegal name containing ; (single-arg)
  [Cro::HTTP] ok 40 - Refuses to add response header with illegal name containing " (two-arg)
  [Cro::HTTP] ok 41 - Refuses to add response header with illegal name containing ( (two-arg)
  [Cro::HTTP] ok 42 - Refuses to add response header with illegal name containing ) (two-arg)
  [Cro::HTTP] ok 43 - Refuses to add response header with illegal name containing [ (two-arg)
  [Cro::HTTP] ok 44 - Refuses to add response header with illegal name containing ] (two-arg)
  [Cro::HTTP] ok 45 - Refuses to add response header with illegal name containing { (two-arg)
  [Cro::HTTP] ok 46 - Refuses to add response header with illegal name containing } (two-arg)
  [Cro::HTTP] ok 47 - Refuses to add response header with illegal name containing @ (two-arg)
  [Cro::HTTP] ok 48 - Refuses to add response header with illegal name containing \ (two-arg)
  [Cro::HTTP] ok 49 - Refuses to add response header with illegal name containing / (two-arg)
  [Cro::HTTP] ok 50 - Refuses to add response header with illegal name containing < (two-arg)
  [Cro::HTTP] ok 51 - Refuses to add response header with illegal name containing > (two-arg)
  [Cro::HTTP] ok 52 - Refuses to add response header with illegal name containing , (two-arg)
  [Cro::HTTP] ok 53 - Refuses to add response header with illegal name containing ; (two-arg)
  [Cro::HTTP] ok 54 - Utterly crazy but valid header can be added (single-arg)
  [Cro::HTTP] ok 55 - Utterly crazy but valid header can be added (two-arg)
  [Cro::HTTP] ok 56 - Can set body
  [Cro::HTTP] ok 57 - Default status code when body set is 200, not 204
  [Cro::HTTP] ok 58 - Can set correct cookie
  [Cro::HTTP] ok 59 - Cookie header is set
  [Cro::HTTP] ok 60 - Cookie cannot be set twice
  [Cro::HTTP] ok 61 - Cookie header is set for two cookies
  [Cro::HTTP] ok 62 - Cookie header is set for a complex cookie
  [Cro::HTTP] ok 63 - Cookies are returned from .cookies call
  [Cro::HTTP] ok 64 - All cookies are returned
  [Cro::HTTP] 1..64
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router-named-urls.t
  [Cro::HTTP] ok 1 - Escaped named param
  [Cro::HTTP] ok 2 - Escaped positional
  [Cro::HTTP] ok 3 - Non-path related parameters were not counted
  [Cro::HTTP] ok 4 - Auth parameter is ignored when creating uri
  [Cro::HTTP] ok 5 - Parameter with type that does Auth is ignored when creating uri
  [Cro::HTTP] ok 6 - GET option to multi method named endpoint
  [Cro::HTTP] ok 7 - POST option to multi method named endpoint
  [Cro::HTTP] ok 8 - PUT option to multi method named endpoint
  [Cro::HTTP] ok 9 - DELETE option to multi method named endpoint
  [Cro::HTTP] ok 10 - No named urls
  [Cro::HTTP] ok 11 - No named urls with a prefix
  [Cro::HTTP] ok 12 - Basic call of a generator by a qualified name is correct
  [Cro::HTTP] # Subtest: did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::DuplicateLinkName)
  [Cro::HTTP]     ok 3 - .message matches Conflicting link name: home
  [Cro::HTTP] ok 13 - did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP] # Subtest: did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::DuplicateLinkName)
  [Cro::HTTP]     ok 3 - .message matches Conflicting link name: main.home
  [Cro::HTTP] ok 14 - did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP] ok 15 - URL is generated correctly
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Not enough arguments
  [Cro::HTTP] ok 16 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Extraneous arguments
  [Cro::HTTP] ok 17 - did we throws-like Exception?
  [Cro::HTTP] ok 18 - 
  [Cro::HTTP] ok 19 - 
  [Cro::HTTP] ok 20 - 
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Extraneous arguments
  [Cro::HTTP] ok 21 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Extraneous named arguments: c.
  [Cro::HTTP] ok 22 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Extraneous named arguments: c.
  [Cro::HTTP] ok 23 - did we throws-like Exception?
  [Cro::HTTP] ok 24 - 
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Missing named arguments: b.
  [Cro::HTTP] ok 25 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Missing named arguments: a.
  [Cro::HTTP] ok 26 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Extraneous arguments
  [Cro::HTTP] ok 27 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Missing named arguments: a, b. Extraneous named arguments: c.
  [Cro::HTTP] ok 28 - did we throws-like Exception?
  [Cro::HTTP] # Subtest: did we throws-like Exception?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (Exception)
  [Cro::HTTP]     ok 3 - .message matches Missing named arguments: b. Extraneous named arguments: c.
  [Cro::HTTP] ok 29 - did we throws-like Exception?
  [Cro::HTTP] ok 30 - 
  [Cro::HTTP] ok 31 - 
  [Cro::HTTP] ok 32 - Splat with no args at all
  [Cro::HTTP] ok 33 - Splat with no named args
  [Cro::HTTP] ok 34 - Splat with no pos args
  [Cro::HTTP] ok 35 - Splat with both types of args
  [Cro::HTTP] ok 36 - Conflict check is per-route block 1
  [Cro::HTTP] ok 37 - Conflict check is per-route block 2
  [Cro::HTTP] ok 38 - Conflict check is by route name
  [Cro::HTTP] # Subtest: did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::DuplicateLinkName)
  [Cro::HTTP]     ok 3 - .message matches Conflicting link name: foo.home
  [Cro::HTTP] ok 39 - did we throws-like X::Cro::HTTP::Router::DuplicateLinkName?
  [Cro::HTTP] 1..39
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router-plugin.rakutest
  [Cro::HTTP] # Subtest: router-plugin-add-config throws outside of route block
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInRouteBlock)
  [Cro::HTTP]     ok 3 - .what matches add-message
  [Cro::HTTP] ok 1 - router-plugin-add-config throws outside of route block
  [Cro::HTTP] ok 2 - Can add plugin configuration to the route block
  [Cro::HTTP] ok 3 - Got expected error from add-message
  [Cro::HTTP] # Subtest: Access to configuration with single level route block
  [Cro::HTTP]     ok 1 - Got a response
  [Cro::HTTP]     ok 2 - Local configuration was available in route handler
  [Cro::HTTP]     ok 3 - Got a response
  [Cro::HTTP]     ok 4 - All configuration was available in route handler
  [Cro::HTTP]     1..4
  [Cro::HTTP] ok 4 - Access to configuration with single level route block
  [Cro::HTTP] # Subtest: Access to configuration with include
  [Cro::HTTP]     ok 1 - Got a response
  [Cro::HTTP]     ok 2 - Local configuration in included route handler not affected by outer
  [Cro::HTTP]     ok 3 - Got a response
  [Cro::HTTP]     ok 4 - Outer configuration in included router handler available if requested
  [Cro::HTTP]     ok 5 - Got a response
  [Cro::HTTP]     ok 6 - Inner route block configuration does not leak into outer local configuration
  [Cro::HTTP]     ok 7 - Got a response
  [Cro::HTTP]     ok 8 - Inner route block configuration does not leak into outer configuration
  [Cro::HTTP]     1..8
  [Cro::HTTP] ok 5 - Access to configuration with include
  [Cro::HTTP] # Subtest: Access to configuration in before block
  [Cro::HTTP]     ok 1 - Got a response
  [Cro::HTTP]     ok 2 - Got 200 when before middleware ran and did not produce response
  [Cro::HTTP]     ok 3 - Got a response
  [Cro::HTTP]     ok 4 - Got 404 when before middleware ran and changed response
  [Cro::HTTP]     1..4
  [Cro::HTTP] ok 6 - Access to configuration in before block
  [Cro::HTTP] # Subtest: Access to configuration in after block
  [Cro::HTTP]     ok 1 - Got a response
  [Cro::HTTP]     ok 2 - Got 200 when after middleware ran and did not change response
  [Cro::HTTP]     ok 3 - Got a response
  [Cro::HTTP]     ok 4 - Got 404 when after middleware ran and changed response
  [Cro::HTTP]     1..4
  [Cro::HTTP] ok 7 - Access to configuration in after block
  [Cro::HTTP] 1..7
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router.rakutest
  [Cro::HTTP] ok 1 - Route block with no routes gives back a Cro::Transform
  [Cro::HTTP] ok 2 - Empty route set gives a response
  [Cro::HTTP] ok 3 - Status code from empty route set is 404
  [Cro::HTTP] ok 4 - No matching route gets a HTTP response
  [Cro::HTTP] ok 5 - Status code uri is invalid is 400
  [Cro::HTTP] # Subtest: Can only use request term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches request
  [Cro::HTTP] ok 6 - Can only use request term inside of a handler
  [Cro::HTTP] # Subtest: Can only use response term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches response
  [Cro::HTTP] ok 7 - Can only use response term inside of a handler
  [Cro::HTTP] # Subtest: Can only use created term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches created
  [Cro::HTTP] ok 8 - Can only use created term inside of a handler
  [Cro::HTTP] # Subtest: Can only use not-found term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches not-found
  [Cro::HTTP] ok 9 - Can only use not-found term inside of a handler
  [Cro::HTTP] # Subtest: Can only use forbidden term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches forbidden
  [Cro::HTTP] ok 10 - Can only use forbidden term inside of a handler
  [Cro::HTTP] # Subtest: Can only use redirect term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches redirected
  [Cro::HTTP] ok 11 - Can only use redirect term inside of a handler
  [Cro::HTTP] # Subtest: Can only use conflict term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches conflict
  [Cro::HTTP] ok 12 - Can only use conflict term inside of a handler
  [Cro::HTTP] # Subtest: Can only use i'm-a-teapot term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches i'm-a-teapot
  [Cro::HTTP] ok 13 - Can only use i'm-a-teapot term inside of a handler
  [Cro::HTTP] # Subtest: Can only use bad-request term inside of a handler
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Router::OnlyInHandler)
  [Cro::HTTP]     ok 3 - .what matches bad-request
  [Cro::HTTP] ok 14 - Can only use bad-request term inside of a handler
  [Cro::HTTP] ok 15 - Route block with routes gives back a Cro::Transform
  [Cro::HTTP] ok 16 - Route set routes / correctly
  [Cro::HTTP] ok 17 - Got 200 response
  [Cro::HTTP] ok 18 - Got expected header
  [Cro::HTTP] ok 19 - Got expected body
  [Cro::HTTP] ok 20 - Route set routes /about correctly
  [Cro::HTTP] ok 21 - Got 200 response
  [Cro::HTTP] ok 22 - Got expected header
  [Cro::HTTP] ok 23 - Got expected body
  [Cro::HTTP] ok 24 - Route set routes /company/careers correctly
  [Cro::HTTP] ok 25 - Got 200 response
  [Cro::HTTP] ok 26 - Got expected header
  [Cro::HTTP] ok 27 - Got expected body
  [Cro::HTTP] ok 28 - No matching route gets a HTTP response
  [Cro::HTTP] ok 29 - Status code when no matching route is 404
  [Cro::HTTP] ok 30 - Route set routes GET
  [Cro::HTTP] ok 31 - Got 200 response
  [Cro::HTTP] ok 32 - Got expected header
  [Cro::HTTP] ok 33 - Got expected body
  [Cro::HTTP] ok 34 - Route set routes POST
  [Cro::HTTP] ok 35 - Got 201 response
  [Cro::HTTP] ok 36 - Got expected header
  [Cro::HTTP] ok 37 - Got expected body
  [Cro::HTTP] ok 38 - Route set routes PUT
  [Cro::HTTP] ok 39 - Got 204 response
  [Cro::HTTP] ok 40 - Route set routes DELETE
  [Cro::HTTP] ok 41 - Got 200 response
  [Cro::HTTP] ok 42 - Got expected header
  [Cro::HTTP] ok 43 - Got expected body
  [Cro::HTTP] ok 44 - Route set routes PATCH
  [Cro::HTTP] ok 45 - Got 200 response
  [Cro::HTTP] ok 46 - Got expected header
  [Cro::HTTP] ok 47 - Got expected body
  [Cro::HTTP] ok 48 - Mu variable at end handled correctly
  [Cro::HTTP] ok 49 - Any variable at end handled correctly
  [Cro::HTTP] ok 50 - Str variable at end handled correctly
  [Cro::HTTP] ok 51 - Longest literal prefix wins
  [Cro::HTTP] ok 52 - Str variable in middle of literals handled correctly
  [Cro::HTTP] ok 53 - Having both Str and Int variables handled correctly
  [Cro::HTTP] ok 54 - Int may have a sign
  [Cro::HTTP] ok 55 - Slurpy handled correctly (empty case)
  [Cro::HTTP] ok 56 - Slurpy handled correctly (one segment case)
  [Cro::HTTP] ok 57 - Slurpy handled correctly (two segment case)
  [Cro::HTTP] ok 58 - Slurpy handled correctly (three segment case)
  [Cro::HTTP] ok 59 - Optional segment handled correctly (no argument)
  [Cro::HTTP] ok 60 - Optional segment handled correctly (argument)
  [Cro::HTTP] ok 61 - Two optional segments handled correctly (none passed)
  [Cro::HTTP] ok 62 - Two optional segments handled correctly (one passed)
  [Cro::HTTP] ok 63 - Two optional segments handled correctly (two passed)
  [Cro::HTTP] ok 64 - Two query string parameters, neither passed (explicit is query)
  [Cro::HTTP] ok 65 - Two query string parameters, first passed (explicit is query)
  [Cro::HTTP] ok 66 - Two query string parameters, second passed (explicit is query)
  [Cro::HTTP] ok 67 - Two query string parameters, both passed (explicit is query)
  [Cro::HTTP] ok 68 - Two header parameters, one for a non-present header
  [Cro::HTTP] ok 69 - Two header parameters, both present
  [Cro::HTTP] ok 70 - Header parameters are case-insensitive
  [Cro::HTTP] ok 71 - Required query parameter selects correct route (1)
  [Cro::HTTP] ok 72 - Required query parameter selects correct route (2)
  [Cro::HTTP] ok 73 - First winning route with required query items wins
  [Cro::HTTP] ok 74 - Route with named array of query parameters works
  [Cro::HTTP] ok 75 - Route with named array of headers works
  [Cro::HTTP] ok 76 - Correct route picked when there are required headers
  [Cro::HTTP] ok 77 - Route with named array of headers works
  [Cro::HTTP] ok 78 - Route with named hash of headers works
  [Cro::HTTP] ok 79 - Route with required Int named arg for query parameter works
  [Cro::HTTP] ok 80 - Route with optional Int named arg for query parameter works when passed
  [Cro::HTTP] ok 81 - Route with optional Int named arg for query parameter works when not passed
  [Cro::HTTP] ok 82 - Route with optional UInt named arg for query parameter works when passed
  [Cro::HTTP] ok 83 - Route with optional UInt named arg for query parameter doesn't match negative values
  [Cro::HTTP] ok 84 - Route for positional int8 works
  [Cro::HTTP] ok 85 - 
  [Cro::HTTP] ok 86 - Lower border for positional int8 route works
  [Cro::HTTP] ok 87 - 
  [Cro::HTTP] ok 88 - Upper border for positional int8 route works
  [Cro::HTTP] ok 89 - Route for positional uint8 works
  [Cro::HTTP] ok 90 - 
  [Cro::HTTP] ok 91 - Lower border for positional uint8 route works
  [Cro::HTTP] ok 92 - 
  [Cro::HTTP] ok 93 - Upper border for positional uint8 route works
  [Cro::HTTP] ok 94 - Route for positional int16 works
  [Cro::HTTP] ok 95 - 
  [Cro::HTTP] ok 96 - Lower border for positional int16 route works
  [Cro::HTTP] ok 97 - 
  [Cro::HTTP] ok 98 - Upper border for positional int16 route works
  [Cro::HTTP] ok 99 - Route for positional uint16 works
  [Cro::HTTP] ok 100 - 
  [Cro::HTTP] ok 101 - Lower border for positional uint16 route works
  [Cro::HTTP] ok 102 - 
  [Cro::HTTP] ok 103 - Upper border for positional uint16 route works
  [Cro::HTTP] ok 104 - Route for positional int32 works
  [Cro::HTTP] ok 105 - 
  [Cro::HTTP] ok 106 - Lower border for positional int32 route works
  [Cro::HTTP] ok 107 - 
  [Cro::HTTP] ok 108 - Upper border for positional int32 route works
  [Cro::HTTP] ok 109 - Route for positional  uint32 works
  [Cro::HTTP] ok 110 - 
  [Cro::HTTP] ok 111 - Lower border for positional uint32 route works
  [Cro::HTTP] ok 112 - 
  [Cro::HTTP] ok 113 - Upper border for positional uint32 route works
  [Cro::HTTP] ok 114 - Route for positional int64 works
  [Cro::HTTP] ok 115 - 
  [Cro::HTTP] ok 116 - Lower border for positional int64 route works
  [Cro::HTTP] ok 117 - 
  [Cro::HTTP] ok 118 - Upper border for positional int64 route works
  [Cro::HTTP] ok 119 - Route for positional uint64 works
  [Cro::HTTP] ok 120 - 
  [Cro::HTTP] ok 121 - Lower border for positional uint64 route works
  [Cro::HTTP] ok 122 - 
  [Cro::HTTP] ok 123 - Upper border for positional uint64 route works
  [Cro::HTTP] ok 124 - Route with optional named int8 works
  [Cro::HTTP] ok 125 - Route for named int8 works
  [Cro::HTTP] ok 126 - 
  [Cro::HTTP] ok 127 - Lower border for named int8 route works
  [Cro::HTTP] ok 128 - 
  [Cro::HTTP] ok 129 - Upper border for named int8 route works
  [Cro::HTTP] ok 130 - Route with optional named uint8 works
  [Cro::HTTP] ok 131 - Route for named uint8 works
  [Cro::HTTP] ok 132 - 
  [Cro::HTTP] ok 133 - Lower border for named uint8 route works
  [Cro::HTTP] ok 134 - 
  [Cro::HTTP] ok 135 - Upper border for named uint8 route works
  [Cro::HTTP] ok 136 - Route with optional named int16 works
  [Cro::HTTP] ok 137 - Route for named int16 works
  [Cro::HTTP] ok 138 - 
  [Cro::HTTP] ok 139 - Lower border for named int16 route works
  [Cro::HTTP] ok 140 - 
  [Cro::HTTP] ok 141 - Upper border for named int16 route works
  [Cro::HTTP] ok 142 - Route with optional named uint16 works
  [Cro::HTTP] ok 143 - Route for named uint16 works
  [Cro::HTTP] ok 144 - 
  [Cro::HTTP] ok 145 - Lower border for named uint16 route works
  [Cro::HTTP] ok 146 - 
  [Cro::HTTP] ok 147 - Upper border for named uint16 route works
  [Cro::HTTP] ok 148 - Route with optional named int32 works
  [Cro::HTTP] ok 149 - Route for named int32 works
  [Cro::HTTP] ok 150 - 
  [Cro::HTTP] ok 151 - Lower border for named int32 route works
  [Cro::HTTP] ok 152 - 
  [Cro::HTTP] ok 153 - Upper border for named int32 route works
  [Cro::HTTP] ok 154 - Route with optional named uint32 works
  [Cro::HTTP] ok 155 - Route for named uint32 works
  [Cro::HTTP] ok 156 - 
  [Cro::HTTP] ok 157 - Lower border for named uint32 route works
  [Cro::HTTP] ok 158 - 
  [Cro::HTTP] ok 159 - Upper border for named uint32 route works
  [Cro::HTTP] ok 160 - Route with optional named int64 works
  [Cro::HTTP] ok 161 - Route for named int64 works
  [Cro::HTTP] ok 162 - 
  [Cro::HTTP] ok 163 - Lower border for named int64 route works
  [Cro::HTTP] ok 164 - 
  [Cro::HTTP] ok 165 - Upper border for named int64 route works
  [Cro::HTTP] ok 166 - Route with optional named uint64 works
  [Cro::HTTP] ok 167 - Route for named uint64 works
  [Cro::HTTP] ok 168 - 
  [Cro::HTTP] ok 169 - Lower border for named uint64 route works
  [Cro::HTTP] ok 170 - 
  [Cro::HTTP] ok 171 - Upper border for named uint64 route works
  [Cro::HTTP] ok 172 - Segment constrained by Str-base subset type matches when it should
  [Cro::HTTP] ok 173 - Segment constrained by Int-base subset type matches when it should
  [Cro::HTTP] ok 174 - Segment constrained by where clause matches when it should
  [Cro::HTTP] ok 175 - Segment of type Int constrained by where clause matches when it should
  [Cro::HTTP] ok 176 - Slurpy segment with where clause matches when it could
  [Cro::HTTP] ok 177 - Non-matching segment gives 404 error (subset, Str)
  [Cro::HTTP] ok 178 - Non-matching segment gives 404 error (subset, Int)
  [Cro::HTTP] ok 179 - Non-matching segment gives 404 error (where, Str)
  [Cro::HTTP] ok 180 - Non-matching segment gives 404 error (where, Int)
  [Cro::HTTP] ok 181 - Non-matching where clause on slurpy gives 404 error
  [Cro::HTTP] ok 182 - Required unpack constrained by Str-base subset type works
  [Cro::HTTP] ok 183 - Optional unpack constrained by Str-base subset type works (provided)
  [Cro::HTTP] ok 184 - Optional unpack constrained by Str-base subset type works (not provided)
  [Cro::HTTP] ok 185 - Required unpack constrained by Int-base subset type works
  [Cro::HTTP] ok 186 - Optional unpack constrained by Int-base subset type works (provided)
  [Cro::HTTP] ok 187 - Optional unpack constrained by Int-base subset type works (not provided)
  [Cro::HTTP] ok 188 - Required unpack untyped with where constraint works
  [Cro::HTTP] ok 189 - Required unpack of type Int with where constraint works
  [Cro::HTTP] ok 190 - Missing unpack gives 400 error (subset, Str)
  [Cro::HTTP] ok 191 - Non-matching unpack gives 400 error (subset, Str)
  [Cro::HTTP] ok 192 - Non-matching optional unpack gives 400 error (subset, Str)
  [Cro::HTTP] ok 193 - Missing unpack gives 400 error (subset, Int)
  [Cro::HTTP] ok 194 - Non-matching unpack gives 400 error (subset, Int)
  [Cro::HTTP] ok 195 - Non-matching optional unpack gives 400 error (subset, Int)
  [Cro::HTTP] ok 196 - Missing unpack gives 400 error (where, Str)
  [Cro::HTTP] ok 197 - Non-matching unpack gives 400 error (where, Str)
  [Cro::HTTP] ok 198 - Missing unpack gives 400 error (where, Int)
  [Cro::HTTP] ok 199 - Non-matching unpack gives 400 error (where, Int)
  [Cro::HTTP] ok 200 - URL that matches on segments but not method is 405
  [Cro::HTTP] ok 201 - URL that matches on segments but not method is 405
  [Cro::HTTP] ok 202 - URL that matches on segments but not method is 405
  [Cro::HTTP] ok 203 - Simple binary content response has 200 status
  [Cro::HTTP] ok 204 - Correct content-type set
  [Cro::HTTP] ok 205 - Got expected body
  [Cro::HTTP] ok 206 - Simple text content response has 200 status
  [Cro::HTTP] ok 207 - Correct content-type set including charset
  [Cro::HTTP] ok 208 - Got expected body
  [Cro::HTTP] ok 209 - Simple JSON content response has 200 status
  [Cro::HTTP] ok 210 - Got two Link headers
  [Cro::HTTP] ok 211 - Got expected link header value (1)
  [Cro::HTTP] ok 212 - Got expected link header value (2)
  [Cro::HTTP] ok 213 - Correct content-type set including charset
  [Cro::HTTP] ok 214 - Got expected body
  [Cro::HTTP] ok 215 - created + content response has 201 status
  [Cro::HTTP] ok 216 - Location header is set
  [Cro::HTTP] ok 217 - Correct content-type set including charset
  [Cro::HTTP] ok 218 - Got expected body
  [Cro::HTTP] ok 219 - created response has 201 status
  [Cro::HTTP] ok 220 - Location header is set
  [Cro::HTTP] ok 221 - Correct content-type set including charset
  [Cro::HTTP] ok 222 - Got expected body
  [Cro::HTTP] ok 223 - Str content with :enc<ISO-8859-1> has 200 response
  [Cro::HTTP] ok 224 - Correct content-type with charset=ISO-8859-1
  [Cro::HTTP] ok 225 - Got expected body
  [Cro::HTTP] ok 226 - Error routine not found sanity (1) - status
  [Cro::HTTP] ok 227 - Error routine not found sanity (1) - content type
  [Cro::HTTP] ok 228 - Error routine not found sanity (1) - body
  [Cro::HTTP] ok 229 - Error routine not found (1) - status
  [Cro::HTTP] ok 230 - Error routine not found (1) - content type
  [Cro::HTTP] ok 231 - Error routine not found (1) - body
  [Cro::HTTP] ok 232 - Error routine not found sanity (2) - status
  [Cro::HTTP] ok 233 - Error routine not found sanity (2) - content type
  [Cro::HTTP] ok 234 - Error routine not found sanity (2) - body
  [Cro::HTTP] ok 235 - Error routine not found (2) - status
  [Cro::HTTP] ok 236 - Error routine not found (2) - content type
  [Cro::HTTP] ok 237 - Error routine not found (2) - body
  [Cro::HTTP] ok 238 - Error routine bad request sanity (1) - status
  [Cro::HTTP] ok 239 - Error routine bad request sanity (1) - content type
  [Cro::HTTP] ok 240 - Error routine bad request sanity (1) - body
  [Cro::HTTP] ok 241 - Error routine bad request (1) - status
  [Cro::HTTP] ok 242 - Error routine bad request (1) - content type
  [Cro::HTTP] ok 243 - Error routine bad request (1) - body
  [Cro::HTTP] ok 244 - Error routine bad request sanity (2) - status
  [Cro::HTTP] ok 245 - Error routine bad request sanity (2) - content type
  [Cro::HTTP] ok 246 - Error routine bad request sanity (2) - body
  [Cro::HTTP] ok 247 - Error routine bad request (2) - status
  [Cro::HTTP] ok 248 - Error routine bad request (2) - content type
  [Cro::HTTP] ok 249 - Error routine bad request (2) - body
  [Cro::HTTP] ok 250 - Error routine forbidden sanity (1) - status
  [Cro::HTTP] ok 251 - Error routine forbidden sanity (1) - content type
  [Cro::HTTP] ok 252 - Error routine forbidden sanity (1) - body
  [Cro::HTTP] ok 253 - Error routine forbidden (1) - status
  [Cro::HTTP] ok 254 - Error routine forbidden (1) - content type
  [Cro::HTTP] ok 255 - Error routine forbidden (1) - body
  [Cro::HTTP] ok 256 - Error routine forbidden sanity (2) - status
  [Cro::HTTP] ok 257 - Error routine forbidden sanity (2) - content type
  [Cro::HTTP] ok 258 - Error routine forbidden sanity (2) - body
  [Cro::HTTP] ok 259 - Error routine forbidden (2) - status
  [Cro::HTTP] ok 260 - Error routine forbidden (2) - content type
  [Cro::HTTP] ok 261 - Error routine forbidden (2) - body
  [Cro::HTTP] ok 262 - Error routine conflict sanity (1) - status
  [Cro::HTTP] ok 263 - Error routine conflict sanity (1) - content type
  [Cro::HTTP] ok 264 - Error routine conflict sanity (1) - body
  [Cro::HTTP] ok 265 - Error routine conflict (1) - status
  [Cro::HTTP] ok 266 - Error routine conflict (1) - content type
  [Cro::HTTP] ok 267 - Error routine conflict (1) - body
  [Cro::HTTP] ok 268 - Error routine conflict sanity (2) - status
  [Cro::HTTP] ok 269 - Error routine conflict sanity (2) - content type
  [Cro::HTTP] ok 270 - Error routine conflict sanity (2) - body
  [Cro::HTTP] ok 271 - Error routine conflict (2) - status
  [Cro::HTTP] ok 272 - Error routine conflict (2) - content type
  [Cro::HTTP] ok 273 - Error routine conflict (2) - body
  [Cro::HTTP] ok 274 - Error routine i'm-a-teapot sanity (1) - status
  [Cro::HTTP] ok 275 - Error routine i'm-a-teapot sanity (1) - content type
  [Cro::HTTP] ok 276 - Error routine i'm-a-teapot sanity (1) - body
  [Cro::HTTP] ok 277 - Error routine i'm-a-teapot (1) - status
  [Cro::HTTP] ok 278 - Error routine i'm-a-teapot (1) - content type
  [Cro::HTTP] ok 279 - Error routine i'm-a-teapot (1) - body
  [Cro::HTTP] ok 280 - Error routine i'm-a-teapot sanity (2) - status
  [Cro::HTTP] ok 281 - Error routine i'm-a-teapot sanity (2) - content type
  [Cro::HTTP] ok 282 - Error routine i'm-a-teapot sanity (2) - body
  [Cro::HTTP] ok 283 - Error routine i'm-a-teapot (2) - status
  [Cro::HTTP] ok 284 - Error routine i'm-a-teapot (2) - content type
  [Cro::HTTP] ok 285 - Error routine i'm-a-teapot (2) - body
  [Cro::HTTP] ok 286 - Temporary redirect (1) - status
  [Cro::HTTP] ok 287 - Temporary redirect (1) - content type
  [Cro::HTTP] ok 288 - Temporary redirect (1) - location
  [Cro::HTTP] ok 289 - Temporary redirect (1) - body
  [Cro::HTTP] ok 290 - Temporary redirect (2) - status
  [Cro::HTTP] ok 291 - Temporary redirect (2) - content type
  [Cro::HTTP] ok 292 - Temporary redirect (2) - location
  [Cro::HTTP] ok 293 - Temporary redirect (2) - body
  [Cro::HTTP] ok 294 - Temporary redirect (3) - status
  [Cro::HTTP] ok 295 - Temporary redirect (3) - content type
  [Cro::HTTP] ok 296 - Temporary redirect (3) - location
  [Cro::HTTP] ok 297 - Temporary redirect (3) - body
  [Cro::HTTP] ok 298 - Temporary redirect (4) - status
  [Cro::HTTP] ok 299 - Temporary redirect (4) - content type
  [Cro::HTTP] ok 300 - Temporary redirect (4) - location
  [Cro::HTTP] ok 301 - Temporary redirect (4) - body
  [Cro::HTTP] ok 302 - Permanent redirect (1) - status
  [Cro::HTTP] ok 303 - Permanent redirect (1) - content type
  [Cro::HTTP] ok 304 - Permanent redirect (1) - location
  [Cro::HTTP] ok 305 - Permanent redirect (1) - body
  [Cro::HTTP] ok 306 - Permanent redirect (2) - status
  [Cro::HTTP] ok 307 - Permanent redirect (2) - content type
  [Cro::HTTP] ok 308 - Permanent redirect (2) - location
  [Cro::HTTP] ok 309 - Permanent redirect (2) - body
  [Cro::HTTP] ok 310 - See other redirect (1) - status
  [Cro::HTTP] ok 311 - See other redirect (1) - content type
  [Cro::HTTP] ok 312 - See other redirect (1) - location
  [Cro::HTTP] ok 313 - See other redirect (1) - body
  [Cro::HTTP] ok 314 - See other redirect (2) - status
  [Cro::HTTP] ok 315 - See other redirect (2) - content type
  [Cro::HTTP] ok 316 - See other redirect (2) - location
  [Cro::HTTP] ok 317 - See other redirect (2) - body
  [Cro::HTTP] ok 318 - Can use request inside of a handler
  [Cro::HTTP] ok 319 - request-body-blob passed a block invokes it with the body blob
  [Cro::HTTP] ok 320 - request-body-text passed a block invokes it with the body text
  [Cro::HTTP] ok 321 - request-body passed a block invokes it with the body object
  [Cro::HTTP] ok 322 - request-body passed a pair invokes block when content type matches
  [Cro::HTTP] ok 323 - When no body match, get bad request response
  [Cro::HTTP] ok 324 - request-body passed a list chooses first Pair if there is a match
  [Cro::HTTP] ok 325 - request-body passed a list chooses second Pair if there is a match
  [Cro::HTTP] ok 326 - request-body passed a list chooses final block if no earlier pairs match
  [Cro::HTTP] ok 327 - request-body matches by signature (Pair case)
  [Cro::HTTP] ok 328 - request-body matches by signature (Block case)
  [Cro::HTTP] ok 329 - body-parser installs a new body parser and it is used
  [Cro::HTTP] ok 330 - body-parser leaves existing body parsers in place
  [Cro::HTTP] ok 331 - body-serializer prepends a new body serializer and it is used
  [Cro::HTTP] ok 332 - body-serializer does not prevent default serializers being found
  [Cro::HTTP] ok 333 - Optional cookie route matches without cookie
  [Cro::HTTP] ok 334 - Status is good
  [Cro::HTTP] ok 335 - Optional cookie route matches with cookie
  [Cro::HTTP] ok 336 - Status is good
  [Cro::HTTP] ok 337 - Request without needed cookie was rejected
  [Cro::HTTP] ok 338 - Bad request to access page without needed cookie
  [Cro::HTTP] ok 339 - Request with required cookie works correctly
  [Cro::HTTP] ok 340 - Status is good
  [Cro::HTTP] ok 341 - Cookie hash works correctly
  [Cro::HTTP] ok 342 - Status is good
  [Cro::HTTP] ok 343 - 
  [Cro::HTTP] ok 344 - Got plain cookie
  [Cro::HTTP] ok 345 - Cookie is here
  [Cro::HTTP] ok 346 - 
  [Cro::HTTP] ok 347 - Status is good
  [Cro::HTTP] ok 348 - Complex cookie is here
  [Cro::HTTP] ok 349 - Static index is fine
  [Cro::HTTP] ok 350 - Static sets correct status code
  [Cro::HTTP] ok 351 - Files with long path work
  [Cro::HTTP] ok 352 - Good status
  [Cro::HTTP] ok 353 - 404 for static works
  [Cro::HTTP] ok 354 - 403 for static works
  [Cro::HTTP] ok 355 - Content-type was setted correctly
  [Cro::HTTP] ok 356 - Custom extension works
  [Cro::HTTP] ok 357 - 200 for static works
  [Cro::HTTP] ok 358 - Cache-Control header is set
  [Cro::HTTP] ok 359 - max-age is added
  [Cro::HTTP] ok 360 - public directive is added
  [Cro::HTTP] ok 361 - multipart/form-data is handled with destructuring
  [Cro::HTTP] ok 362 - urlencoded is handled with destructuring
  [Cro::HTTP] ok 363 - json is handled with destructuring
  [Cro::HTTP] ok 364 - request.uri reconstructs full request URI
  [Cro::HTTP] ok 365 - Basic include: before (outer)
  [Cro::HTTP] ok 366 - Basic include: empty route (include)
  [Cro::HTTP] ok 367 - Basic include: some parts (include)
  [Cro::HTTP] ok 368 - Basic include: after (outer)
  [Cro::HTTP] ok 369 - include and body-parser: body parser in include works in include
  [Cro::HTTP] ok 370 - include and body-parser: outer has outer body parser
  [Cro::HTTP] ok 371 - include and body-parser: outer body parser visible in include
  [Cro::HTTP] ok 372 - include and body-parser: body parser in include does not leak out
  [Cro::HTTP] ok 373 - Basic include: route 1A
  [Cro::HTTP] ok 374 - Basic include: route 1B
  [Cro::HTTP] ok 375 - Basic include: route 1B
  [Cro::HTTP] ok 376 - Basic include: route 1B
  [Cro::HTTP] ok 377 - Basic include: route 1A
  [Cro::HTTP] ok 378 - Basic include: route 1A
  [Cro::HTTP] ok 379 - Basic include: route 2B
  [Cro::HTTP] ok 380 - Basic include: route 1B
  [Cro::HTTP] ok 381 - Basic include: route 2A
  [Cro::HTTP] ok 382 - Basic include: route 2A
  [Cro::HTTP] ok 383 - Basic include: route 2B
  [Cro::HTTP] ok 384 - Basic include: route 2A
  [Cro::HTTP] ok 385 - Basic include: route 2A
  [Cro::HTTP] ok 386 - Basic include: route 1A
  [Cro::HTTP] ok 387 - Basic include: route 2B
  [Cro::HTTP] ok 388 - Basic include: route 2B
  [Cro::HTTP] ok 389 - Basic delegation: delegated transform and second
  [Cro::HTTP] ok 390 - Basic delegation: delegated transform multi part
  [Cro::HTTP] ok 391 - Basic delegation: delegated transform first
  [Cro::HTTP] ok 392 - Basic delegation: delegated transform simple
  [Cro::HTTP] ok 393 - Delegation: / and /category
  [Cro::HTTP] ok 394 - Delegation: /item/1 and /proxy/item/1
  [Cro::HTTP] ok 395 - Delegation: Home
  [Cro::HTTP] ok 396 - Delegation: Slash
  [Cro::HTTP] ok 397 - Delegation: /item and /proxy/item
  [Cro::HTTP] ok 398 - Delegation: Path
  [Cro::HTTP] ok 399 - Can match URL segments with encoded bits (/a%2Bplus)
  [Cro::HTTP] ok 400 - Can match URL segments with encoded bits (/encoded%2Fslash)
  [Cro::HTTP] ok 401 - Can pass query argument without path components (/?value=1)
  [Cro::HTTP] ok 402 - Can pass query arguments with slurpy path signature (/x?value=1)
  [Cro::HTTP] ok 403 - Can pass query arguments with slurpy path signature (/?value=1)
  [Cro::HTTP] ok 404 - Get value from index
  [Cro::HTTP] ok 405 - Static sets correct status code
  [Cro::HTTP] ok 406 - static indexes order check, 1
  [Cro::HTTP] ok 407 - Good status
  [Cro::HTTP] ok 408 - static indexes order check, 2
  [Cro::HTTP] ok 409 - Good status
  [Cro::HTTP] ok 410 - No candidate served with empty indexes
  [Cro::HTTP] ok 411 - Indexes with mime-types returns good status
  [Cro::HTTP] ok 412 - Indexes with mime-types returns proper content-type
  [Cro::HTTP] ok 413 - Get index.html from resources
  [Cro::HTTP] ok 414 - resource sets correct status code
  [Cro::HTTP] ok 415 - resource sets correct content-type
  [Cro::HTTP] ok 416 - Get folder/test.txt from resources
  [Cro::HTTP] ok 417 - Good status
  [Cro::HTTP] ok 418 - Good content-type
  [Cro::HTTP] ok 419 - Get <folder test.txt> from resources
  [Cro::HTTP] ok 420 - Good status
  [Cro::HTTP] ok 421 - Good content-type
  [Cro::HTTP] ok 422 - indexes in a folder of resources
  [Cro::HTTP] ok 423 - Good status
  [Cro::HTTP] ok 424 - Good content-type
  [Cro::HTTP] ok 425 - indexes in root of resources, 1
  [Cro::HTTP] ok 426 - Good status
  [Cro::HTTP] ok 427 - Good content-type
  [Cro::HTTP] ok 428 - indexes in root of resources, 2
  [Cro::HTTP] ok 429 - Good status
  [Cro::HTTP] ok 430 - Good content-type
  [Cro::HTTP] ok 431 - The extension point for other plugins wanting to use resources works
  [Cro::HTTP] ok 432 - Good content-type
  [Cro::HTTP] ok 433 - Around block was called
  [Cro::HTTP] ok 434 - Around block can send response
  [Cro::HTTP] ok 435 - Handler works normally with around block(s)
  [Cro::HTTP] ok 436 - Handler works normally with around block(s)
  [Cro::HTTP] ok 437 - The around blocks are called in top-to-bottom order
  [Cro::HTTP] ok 438 - Content-type header set by content replaces any existing one
  [Cro::HTTP] ok 439 - Recieved proper status for the case where a capture cannot be unpacked for whatever reason
  [Cro::HTTP] 1..439
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-session-inmemory.rakutest
  [Cro::HTTP] ok 1 - Request with no session cookie gets fresh state (1)
  [Cro::HTTP] ok 2 - Request with no session cookie gets fresh state (2)
  [Cro::HTTP] ok 3 - Session cookie being sent makes state work (request 1)
  [Cro::HTTP] ok 4 - Session cookie being sent makes state work (request 2)
  [Cro::HTTP] ok 5 - Session cookie being sent makes state work (request 3)
  [Cro::HTTP] ok 6 - Session cookie being sent makes state work (request 4)
  [Cro::HTTP] ok 7 - Session cookie being sent makes state work (request 5)
  [Cro::HTTP] ok 8 - No session confusion with concurrent clients (A)
  [Cro::HTTP] ok 9 - No session confusion with concurrent clients (B)
  [Cro::HTTP] ok 10 - New session for expiration test (sanity check)
  [Cro::HTTP] ok 11 - Request before expiration is OK
  [Cro::HTTP] ok 12 - A use of the session bumps its expiration
  [Cro::HTTP] ok 13 - Session expires appropriately
  [Cro::HTTP] 1..13
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-session-persistent.rakutest
  [Cro::HTTP] ok 1 - Request with no session cookie gets fresh state (1)
  [Cro::HTTP] ok 2 - Request with no session cookie gets fresh state (2)
  [Cro::HTTP] ok 3 - Session cookie being sent makes state work (request 1)
  [Cro::HTTP] ok 4 - Session cookie being sent makes state work (request 2)
  [Cro::HTTP] ok 5 - Session cookie being sent makes state work (request 3)
  [Cro::HTTP] ok 6 - Session cookie being sent makes state work (request 4)
  [Cro::HTTP] ok 7 - Session cookie being sent makes state work (request 5)
  [Cro::HTTP] ok 8 - No session confusion with concurrent clients (A)
  [Cro::HTTP] ok 9 - No session confusion with concurrent clients (B)
  [Cro::HTTP] ok 10 - New session for expiration test (sanity check)
  [Cro::HTTP] ok 11 - Request before expiration is OK
  [Cro::HTTP] ok 12 - A use of the session bumps its expiration
  [Cro::HTTP] ok 13 - Session expires appropriately
  [Cro::HTTP] ok 14 - Logging
  [Cro::HTTP] ok 15 - New session for route 1
  [Cro::HTTP] ok 16 - Using old session for route 2
  [Cro::HTTP] ok 17 - New session for route 1
  [Cro::HTTP] ok 18 - Logging
  [Cro::HTTP] ok 19 - Using old session for route 2
  [Cro::HTTP] 1..19
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame-parser.rakutest
  [Cro::HTTP] ok 1 - HTTP2 frame parser is a transform
  [Cro::HTTP] ok 2 - HTTP2 frame parser consumes TCP messages
  [Cro::HTTP] ok 3 - HTTP2 frame parser produces HTTP2 frames
  [Cro::HTTP] ok 4 - DATA Frame length cannot be less than padding length
  [Cro::HTTP] ok 5 - Empty DATA frame
  [Cro::HTTP] ok 6 - Empty DATA frame is serialized back
  [Cro::HTTP] ok 7 - DATA frame without padding
  [Cro::HTTP] ok 8 - DATA frame without padding is serialized back
  [Cro::HTTP] ok 9 - DATA frame with zero padding
  [Cro::HTTP] ok 10 - DATA frame with zero padding is serialized back
  [Cro::HTTP] ok 11 - DATA frame with padding
  [Cro::HTTP] ok 12 - DATA frame with padding is serialized back
  [Cro::HTTP] ok 13 - HEADERS Frame length cannot be less than padding length
  [Cro::HTTP] ok 14 - Empty HEADERS frame
  [Cro::HTTP] ok 15 - Empty HEADERS frame is serialized back
  [Cro::HTTP] ok 16 - HEADERS frame without padding
  [Cro::HTTP] ok 17 - HEADERS frame without padding is serialized back
  [Cro::HTTP] ok 18 - HEADERS frame with zero padding
  [Cro::HTTP] ok 19 - HEADERS frame with zero padding is serialized back
  [Cro::HTTP] ok 20 - PRIORITY Frame length is always 5 bytes
  [Cro::HTTP] ok 21 - RST_STREAM Frame length is always 4 bytes
  [Cro::HTTP] ok 22 - Ack SETTINGS Frame length is always 0
  [Cro::HTTP] ok 23 - SETTINGS Frame length is always divisible by 6
  [Cro::HTTP] ok 24 - SETTINGS Frame length is always divisible by 6
  [Cro::HTTP] ok 25 - WindowIncrement Frame length is always 4
  [Cro::HTTP] ok 26 - SETTINGS frame with zero content is emitted correctly
  [Cro::HTTP] 1..26
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame-serializer.rakutest
  [Cro::HTTP] ok 1 - HTTP2 frame serializer is a transform
  [Cro::HTTP] ok 2 - HTTP2 frame serializer consumes HTTP2 frames
  [Cro::HTTP] ok 3 - HTTP2 frame serializer produces TCP messages
  [Cro::HTTP] ok 4 - Simple data frame
  [Cro::HTTP] ok 5 - Simple data frame is parsed back
  [Cro::HTTP] ok 6 - Simple data frame with padding
  [Cro::HTTP] ok 7 - Simple data frame with padding is parsed back
  [Cro::HTTP] ok 8 - Simple headers frame
  [Cro::HTTP] ok 9 - Simple headers frame is parsed back
  [Cro::HTTP] ok 10 - Simple headers frame with padding
  [Cro::HTTP] ok 11 - Simple headers frame with padding is parsed back
  [Cro::HTTP] ok 12 - Simple priority frame
  [Cro::HTTP] ok 13 - Simple priority frame is parsed back
  [Cro::HTTP] ok 14 - Simple RstStream frame
  [Cro::HTTP] ok 15 - Simple RstStream frame is parsed back
  [Cro::HTTP] ok 16 - RstStream frame with a custom error treats it as INTERNAL_ERROR
  [Cro::HTTP] ok 17 - RstStream frame with a custom error treats it as INTERNAL_ERROR is parsed back
  [Cro::HTTP] ok 18 - Simple Settings frame
  [Cro::HTTP] ok 19 - Settings frame is successful
  [Cro::HTTP] ok 20 - Simple PushPromise frame
  [Cro::HTTP] ok 21 - Simple PushPromise frame is parsed back
  [Cro::HTTP] ok 22 - PushPromise frame with padding
  [Cro::HTTP] ok 23 - PushPromise frame with padding is parsed back
  [Cro::HTTP] ok 24 - Simple Ping frame
  [Cro::HTTP] ok 25 - Ping frame is successful
  [Cro::HTTP] ok 26 - Ping payload cannot be more than 8 bytes
  [Cro::HTTP] ok 27 - Simple GoAway frame
  [Cro::HTTP] ok 28 - Simple GoAway frame is parsed back
  [Cro::HTTP] ok 29 - GoAway frame with a custom error treats it as INTERNAL_ERROR
  [Cro::HTTP] ok 30 - GoAway frame with a custom error treats it as INTERNAL_ERROR is parsed back
  [Cro::HTTP] ok 31 - Simple WindowUpdate frame
  [Cro::HTTP] ok 32 - Simple WindowUpdate frame is parsed back
  [Cro::HTTP] ok 33 - Simple Continuation frame
  [Cro::HTTP] ok 34 - Simple Continuation frame is parsed back
  [Cro::HTTP] ok 35 - 
  [Cro::HTTP] ok 36 - 
  [Cro::HTTP] ok 37 - 
  [Cro::HTTP] ok 38 - 
  [Cro::HTTP] ok 39 - Too long Headers frame is splitted
  [Cro::HTTP] ok 40 - 
  [Cro::HTTP] ok 41 - 
  [Cro::HTTP] ok 42 - 
  [Cro::HTTP] ok 43 - 
  [Cro::HTTP] ok 44 - Too long Data frame is splitted
  [Cro::HTTP] 1..44
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame.rakutest
  [Cro::HTTP] ok 1 - DATA frame stream identifier cannot be 0
  [Cro::HTTP] ok 2 - HEADERS frame stream identifier cannot be 0
  [Cro::HTTP] ok 3 - PRIORITY frame stream identifier cannot be 0
  [Cro::HTTP] ok 4 - Settings stream-identifier cannot be non-zero
  [Cro::HTTP] ok 5 - PUSH_PROMISE frame stream identifier cannot be 0
  [Cro::HTTP] ok 6 - Ping stream-identifier cannot be non-zero
  [Cro::HTTP] ok 7 - GOAWAY Frame stream-identifier cannot be non-zero
  [Cro::HTTP] 1..7
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-request-parser.rakutest
  [Cro::HTTP] ok 1 - check 1
  [Cro::HTTP] ok 2 - check 2
  [Cro::HTTP] ok 3 - check 3
  [Cro::HTTP] ok 4 - check 4
  [Cro::HTTP] ok 5 - check 5
  [Cro::HTTP] ok 6 - Headers
  [Cro::HTTP] ok 7 - check 1
  [Cro::HTTP] ok 8 - check 2
  [Cro::HTTP] ok 9 - check 3
  [Cro::HTTP] ok 10 - check 4
  [Cro::HTTP] ok 11 - check 5
  [Cro::HTTP] ok 12 - check 6
  [Cro::HTTP] ok 13 - Headers + Continuation
  [Cro::HTTP] ok 14 - check 1
  [Cro::HTTP] ok 15 - check 2
  [Cro::HTTP] ok 16 - check 3
  [Cro::HTTP] ok 17 - check 4
  [Cro::HTTP] ok 18 - Headers + Data
  [Cro::HTTP] ok 19 - check 1
  [Cro::HTTP] ok 20 - check 2
  [Cro::HTTP] ok 21 - check 3
  [Cro::HTTP] ok 22 - check 4
  [Cro::HTTP] ok 23 - check 5
  [Cro::HTTP] ok 24 - check 6
  [Cro::HTTP] ok 25 - check 7
  [Cro::HTTP] ok 26 - Headers + Continuation + Data
  [Cro::HTTP] ok 27 - check 1
  [Cro::HTTP] ok 28 - check 2
  [Cro::HTTP] ok 29 - check 3
  [Cro::HTTP] ok 30 - check 4
  [Cro::HTTP] ok 31 - check 5
  [Cro::HTTP] ok 32 - check 6
  [Cro::HTTP] ok 33 - check 7
  [Cro::HTTP] ok 34 - check 8
  [Cro::HTTP] ok 35 - Headers + Continuation + Data + Headers
  [Cro::HTTP] ok 36 - check 1
  [Cro::HTTP] ok 37 - check 2
  [Cro::HTTP] ok 38 - check 3
  [Cro::HTTP] ok 39 - check 4
  [Cro::HTTP] ok 40 - check 1
  [Cro::HTTP] ok 41 - check 2
  [Cro::HTTP] ok 42 - check 3
  [Cro::HTTP] ok 43 - Header1 + Header2 + Data1
  [Cro::HTTP] ok 44 - check 1
  [Cro::HTTP] ok 45 - check 2
  [Cro::HTTP] ok 46 - check 3
  [Cro::HTTP] ok 47 - check 4
  [Cro::HTTP] ok 48 - check 1
  [Cro::HTTP] ok 49 - check 2
  [Cro::HTTP] ok 50 - check 3
  [Cro::HTTP] ok 51 - check 4
  [Cro::HTTP] ok 52 - Header1 + Header2 + Data1 + Data2
  [Cro::HTTP] ok 53 - check 1
  [Cro::HTTP] ok 54 - check 2
  [Cro::HTTP] ok 55 - check 3
  [Cro::HTTP] ok 56 - check 4
  [Cro::HTTP] ok 57 - check 1
  [Cro::HTTP] ok 58 - check 2
  [Cro::HTTP] ok 59 - check 3
  [Cro::HTTP] ok 60 - Header1 + Continuation1 + Header2 + Data1
  [Cro::HTTP] # Subtest: Unfinished header cannot be interrupted
  [Cro::HTTP]     1..2
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP2::Error)
  [Cro::HTTP] ok 61 - Unfinished header cannot be interrupted
  [Cro::HTTP] 1..61
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-request-serializer.rakutest
  [Cro::HTTP] ok 1 - check 1
  [Cro::HTTP] ok 2 - check 2
  [Cro::HTTP] ok 3 - check 3
  [Cro::HTTP] ok 4 - check 4
  [Cro::HTTP] ok 5 - Header
  [Cro::HTTP] ok 6 - check 1
  [Cro::HTTP] ok 7 - check 2
  [Cro::HTTP] ok 8 - check 3
  [Cro::HTTP] ok 9 - check 4
  [Cro::HTTP] ok 10 - check 1
  [Cro::HTTP] ok 11 - check 2
  [Cro::HTTP] ok 12 - check 3
  [Cro::HTTP] ok 13 - check 4
  [Cro::HTTP] ok 14 - Header + Data
  [Cro::HTTP] ok 15 - check 1
  [Cro::HTTP] ok 16 - check 2
  [Cro::HTTP] ok 17 - check 3
  [Cro::HTTP] ok 18 - check 4
  [Cro::HTTP] ok 19 - check 1
  [Cro::HTTP] ok 20 - check 2
  [Cro::HTTP] ok 21 - check 3
  [Cro::HTTP] ok 22 - check 4
  [Cro::HTTP] ok 23 - check 1
  [Cro::HTTP] ok 24 - check 2
  [Cro::HTTP] ok 25 - check 3
  [Cro::HTTP] ok 26 - check 4
  [Cro::HTTP] ok 27 - Header + Data with unknown Content-Length
  [Cro::HTTP] ok 28 - round-trip: method
  [Cro::HTTP] ok 29 - round-trip: target
  [Cro::HTTP] ok 30 - round-trip: content-length header present and correct
  [Cro::HTTP] ok 31 - round-trip: body text
  [Cro::HTTP] ok 32 - POST with set-body round-trips correctly over HTTP/2
  [Cro::HTTP] 1..32
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-response-parser.rakutest
  [Cro::HTTP] ok 1 - check 1
  [Cro::HTTP] ok 2 - check 2
  [Cro::HTTP] ok 3 - check 3
  [Cro::HTTP] ok 4 - Headers
  [Cro::HTTP] ok 5 - check 1
  [Cro::HTTP] ok 6 - check 2
  [Cro::HTTP] ok 7 - check 3
  [Cro::HTTP] ok 8 - check 4
  [Cro::HTTP] ok 9 - Headers + Data
  [Cro::HTTP] 1..9
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-response-serializer.rakutest
  [Cro::HTTP] ok 1 - check 1
  [Cro::HTTP] ok 2 - check 2
  [Cro::HTTP] ok 3 - check 3
  [Cro::HTTP] ok 4 - check 4
  [Cro::HTTP] ok 5 - Header
  [Cro::HTTP] ok 6 - check 1
  [Cro::HTTP] ok 7 - check 2
  [Cro::HTTP] ok 8 - check 3
  [Cro::HTTP] ok 9 - check 4
  [Cro::HTTP] ok 10 - check 1
  [Cro::HTTP] ok 11 - check 2
  [Cro::HTTP] ok 12 - check 3
  [Cro::HTTP] ok 13 - check 4
  [Cro::HTTP] ok 14 - Header + Data
  [Cro::HTTP] ok 15 - check 1
  [Cro::HTTP] ok 16 - check 2
  [Cro::HTTP] ok 17 - check 3
  [Cro::HTTP] ok 18 - check 4
  [Cro::HTTP] ok 19 - check 1
  [Cro::HTTP] ok 20 - check 2
  [Cro::HTTP] ok 21 - check 3
  [Cro::HTTP] ok 22 - check 4
  [Cro::HTTP] ok 23 - check 1
  [Cro::HTTP] ok 24 - check 2
  [Cro::HTTP] ok 25 - check 3
  [Cro::HTTP] ok 26 - check 4
  [Cro::HTTP] ok 27 - Header + Data - Content-Length unspecified
  [Cro::HTTP] ok 28 - Too small body throws
  [Cro::HTTP] ok 29 - Too big body throws
  [Cro::HTTP] 1..29
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/router-auth.rakutest
  [Cro::HTTP] # Subtest: Auth parameter with type that implements Cro::HTTP::Auth
  [Cro::HTTP]     ok 1 - Can request / successfully with non-logged-in, non-admin
  [Cro::HTTP]     ok 2 - Get the authorization object
  [Cro::HTTP]     ok 3 - Request to /page when not logged in is 401
  [Cro::HTTP]     ok 4 - Request to /admin when not logged in is 401
  [Cro::HTTP]     ok 5 - Can request / successfully with logged-in, non-admin
  [Cro::HTTP]     ok 6 - Get the authorization object
  [Cro::HTTP]     ok 7 - Can request /page successfully with logged-in, non-admin
  [Cro::HTTP]     ok 8 - Got expected body
  [Cro::HTTP]     ok 9 - Request to /admin when not an admin is 401
  [Cro::HTTP]     ok 10 - Can request / successfully with logged-in admin
  [Cro::HTTP]     ok 11 - Get the authorization object
  [Cro::HTTP]     ok 12 - Can request /page successfully with logged-in admin
  [Cro::HTTP]     ok 13 - Got expected body
  [Cro::HTTP]     ok 14 - Can request /admin successfully with logged-in admin
  [Cro::HTTP]     ok 15 - Got expected body
  [Cro::HTTP]     1..15
  [Cro::HTTP] ok 1 - Auth parameter with type that implements Cro::HTTP::Auth
  [Cro::HTTP] # Subtest: Auth parameter marked with is auth trait, not doing Cro::HTTP::Auth
  [Cro::HTTP]     ok 1 - Can request / successfully with non-logged-in, non-admin
  [Cro::HTTP]     ok 2 - Get the authorization object
  [Cro::HTTP]     ok 3 - Request to /page when not logged in is 401
  [Cro::HTTP]     ok 4 - Request to /admin when not logged in is 401
  [Cro::HTTP]     ok 5 - Can request / successfully with logged-in, non-admin
  [Cro::HTTP]     ok 6 - Get the authorization object
  [Cro::HTTP]     ok 7 - Can request /page successfully with logged-in, non-admin
  [Cro::HTTP]     ok 8 - Got expected body
  [Cro::HTTP]     ok 9 - Request to /admin when not an admin is 401
  [Cro::HTTP]     ok 10 - Can request / successfully with logged-in admin
  [Cro::HTTP]     ok 11 - Get the authorization object
  [Cro::HTTP]     ok 12 - Can request /page successfully with logged-in admin
  [Cro::HTTP]     ok 13 - Got expected body
  [Cro::HTTP]     ok 14 - Can request /admin successfully with logged-in admin
  [Cro::HTTP]     ok 15 - Got expected body
  [Cro::HTTP]     1..15
  [Cro::HTTP] ok 2 - Auth parameter marked with is auth trait, not doing Cro::HTTP::Auth
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/uri-http.rakutest
  [Cro::HTTP] ok 1 - A single / request target
  [Cro::HTTP] ok 2 - Check 1
  [Cro::HTTP] ok 3 - Check 2
  [Cro::HTTP] ok 4 - Check 3
  [Cro::HTTP] ok 5 - Check 4
  [Cro::HTTP] ok 6 - Check 5
  [Cro::HTTP] ok 7 - Check 6
  [Cro::HTTP] ok 8 - A single /foo/bar.html request target
  [Cro::HTTP] ok 9 - Check 1
  [Cro::HTTP] ok 10 - Check 2
  [Cro::HTTP] ok 11 - Check 3
  [Cro::HTTP] # Subtest: Basic query string additions as pair arguemnts
  [Cro::HTTP]     ok 1 - Path was retained correctly
  [Cro::HTTP]     ok 2 - Query string correctly appended
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 12 - Basic query string additions as pair arguemnts
  [Cro::HTTP] # Subtest: Basic query string additions as named arguments
  [Cro::HTTP]     ok 1 - Path was retained correctly
  [Cro::HTTP]     ok 2 - Query string correctly appended
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 13 - Basic query string additions as named arguments
  [Cro::HTTP] # Subtest: Basic query string additions retain what was originally there
  [Cro::HTTP]     ok 1 - Path was retained correctly
  [Cro::HTTP]     ok 2 - Existing query string values were retained
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 14 - Basic query string additions retain what was originally there
  [Cro::HTTP] # Subtest: Query string keys and values are encoded
  [Cro::HTTP]     ok 1 - Path was retained correctly
  [Cro::HTTP]     ok 2 - Correct encoding
  [Cro::HTTP]     1..2
  [Cro::HTTP] ok 15 - Query string keys and values are encoded
  [Cro::HTTP] ok 16 - + signs in query string decoded correctly
  [Cro::HTTP] 1..16
  ===> Testing [FAIL]: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0>
  [Cro::HTTP] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0>
  ===> Install [OK] for Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 2min 26.677s
               CPU time consumed: 3min 27.031s
                     Memory peak: 2.3G (swap: 0B)

  ```
  </details>
* [ ] [Game::Sudoku](https://raku.land/zef:Scimon/Game::Sudoku) – Fail, Bisected: [afee7d8](https://github.com/rakudo/rakudo/commit/afee7d8d3197b7a093355d98a90f6f86d8bda32a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1405539-i1439247.service; invocation ID: 79b8ef54b2cb4154a77cda6a17cadac2
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Game::Sudoku
  ===> Found: Game::Sudoku:ver<1.1.5>:auth<zef:Scimon> [via Zef::Repository::Ecosystems<fez>]
  [Game::Sudoku] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549414.1405540.8656.452074917712/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz https://360.zef.pm/G/AM/GAME_SUDOKU/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz
  ===> Fetching [OK]: Game::Sudoku:ver<1.1.5>:auth<zef:Scimon> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549414.1405540.8656.452074917712/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz
  [Game::Sudoku] Command: tar -t -f ./0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz
  [Game::Sudoku] Command: tar -xvf ./0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz -C ../0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz
  ===> Extraction [OK]: Game::Sudoku to /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz
  ===> Testing: Game::Sudoku:ver<1.1.5>:auth<zef:Scimon>
  [Game::Sudoku] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz/Game-Sudoku-1.1.5 t/01-basic.t
  [Game::Sudoku] ok 1 - Game::Sudoku module can be use-d ok
  [Game::Sudoku] ok 2 - Game::Sudoku::Solver module can be use-d ok
  [Game::Sudoku] 1..2
  [Game::Sudoku] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz/Game-Sudoku-1.1.5 t/02-create-and-display.t
  [Game::Sudoku] ok 1 - String rep is 81 0's
  [Game::Sudoku] ok 2 - Grid is as expected
  [Game::Sudoku] ok 3 - Empty grid is valid
  [Game::Sudoku] ok 4 - Empty grid is not complete
  [Game::Sudoku] ok 5 - String rep is as expected
  [Game::Sudoku] ok 6 - Grid is as expected
  [Game::Sudoku] ok 7 - Grid is valid
  [Game::Sudoku] ok 8 - Grid is not complete
  [Game::Sudoku] ok 9 - String rep is as expected
  [Game::Sudoku] ok 10 - Grid is as expected
  [Game::Sudoku] ok 11 - Grid is valid
  [Game::Sudoku] ok 12 - Grid is complete.
  [Game::Sudoku] 1..12
  [Game::Sudoku] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz/Game-Sudoku-1.1.5 t/03-validation.t
  [Game::Sudoku] ok 1 - 000000000000000000000000000000000000000000000000000000000000000000000000000000000 is valid
  [Game::Sudoku] ok 2 - 100000000000000000000000000000000000000000000000000000000000000000000000000000000 is valid
  [Game::Sudoku] ok 3 - 123000000000000000000000000000000000000000000000000000000000000000000000000000000 is valid
  [Game::Sudoku] ok 4 - 483921657967345821251876493548132976729564138136798245372689514814253769695417382 is valid
  [Game::Sudoku] ok 5 - 003020600900305001001806400008102900700000008006708200002609500800203009005010300 is valid
  [Game::Sudoku] ok 6 - 110000000000000000000000000000000000000000000000000000000000000000000000000000000 is invalid
  [Game::Sudoku] ok 7 - 123000000123000000000000000000000000000000000000000000000000000000000000000000000 is invalid
  [Game::Sudoku] ok 8 - 843921657967345821251876493548132976729564138136798245372689514814253769695417382 is invalid
  [Game::Sudoku] ok 9 - 003020600900305001001806400008102900700000008006708200002609500800203009005010303 is invalid
  [Game::Sudoku] 1..9
  [Game::Sudoku] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz/Game-Sudoku-1.1.5 t/04-possible.t
  [Game::Sudoku] ok 1 - Nothing to see here
  [Game::Sudoku] ok 2 - Everything is possible
  [Game::Sudoku] ok 3 - Setting returns the updated object
  [Game::Sudoku] ok 4 - Can also get a cells current value
  [Game::Sudoku] ok 5 - Requesting an unset cell returns Nil
  [Game::Sudoku] ok 6 - We have no options
  [Game::Sudoku] ok 7 - We have options
  [Game::Sudoku] ok 8 - We have a sequence
  [Game::Sudoku] ok 9 - We have a set
  [Game::Sudoku] ok 10 - We have a list when there's no options
  [Game::Sudoku] ok 11 - We have a set
  [Game::Sudoku] ok 12 - Game state is valid
  [Game::Sudoku] ok 13 - Now we have a cell
  [Game::Sudoku] ok 14 - We have no options
  [Game::Sudoku] ok 15 - We have options
  [Game::Sudoku] ok 16 - Game state is valid
  [Game::Sudoku] ok 17 - Still getting games
  [Game::Sudoku] ok 18 - Game state is invalid as we have 2 2's
  [Game::Sudoku] ok 19 - Game as expected
  [Game::Sudoku] ok 20 - Can't modify initial values
  [Game::Sudoku] ok 21 - Got expected possibilites
  [Game::Sudoku] ok 22 - Game is valid
  [Game::Sudoku] ok 23 - Game is valid
  [Game::Sudoku] ok 24 - Game is valid
  [Game::Sudoku] ok 25 - Game is valid
  [Game::Sudoku] ok 26 - Game is valid
  [Game::Sudoku] ok 27 - Game is valid
  [Game::Sudoku] ok 28 - Game is complete
  [Game::Sudoku] ok 29 - Game is valid
  [Game::Sudoku] ok 30 - Game is full
  [Game::Sudoku] ok 31 - Got expected solution
  [Game::Sudoku] 1..31
  [Game::Sudoku] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz/Game-Sudoku-1.1.5 t/05-solver.t
  [Game::Sudoku] ok 1 - Game is complete
  [Game::Sudoku] ok 2 - Game is valid
  [Game::Sudoku] ok 3 - Game is full
  [Game::Sudoku] ok 4 - got expected value
  [Game::Sudoku] ok 5 - Game is complete
  [Game::Sudoku] ok 6 - Game is valid
  [Game::Sudoku] ok 7 - Game is full
  [Game::Sudoku] ok 8 - got expected value
  [Game::Sudoku] ok 9 - Game is complete
  [Game::Sudoku] ok 10 - Game is valid
  [Game::Sudoku] ok 11 - Game is full
  [Game::Sudoku] ok 12 - got expected value
  [Game::Sudoku] 1..12
  ===> Testing [OK] for Game::Sudoku:ver<1.1.5>:auth<zef:Scimon>
  ===> Installing: Game::Sudoku:ver<1.1.5>:auth<zef:Scimon>
  ===> Install [OK] for Game::Sudoku:ver<1.1.5>:auth<zef:Scimon>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 48.150s
               CPU time consumed: 1min 8.308s
                     Memory peak: 1009.9M (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1404976-i1372136.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Game::Sudoku
  ===> Found: Game::Sudoku:ver<1.1.5>:auth<zef:Scimon> [via Zef::Repository::Ecosystems<fez>]
  [Game::Sudoku] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549360.1404981.8708.656118415347/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz https://360.zef.pm/G/AM/GAME_SUDOKU/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz
  ===> Fetching [OK]: Game::Sudoku:ver<1.1.5>:auth<zef:Scimon> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549360.1404981.8708.656118415347/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz
  [Game::Sudoku] Command: tar -t -f ./0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz
  [Game::Sudoku] Command: tar -xvf ./0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz -C ../0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz
  ===> Extraction [OK]: Game::Sudoku to /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz
  ===> Testing: Game::Sudoku:ver<1.1.5>:auth<zef:Scimon>
  [Game::Sudoku] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz/Game-Sudoku-1.1.5 t/01-basic.t
  [Game::Sudoku] ok 1 - Game::Sudoku module can be use-d ok
  [Game::Sudoku] ok 2 - Game::Sudoku::Solver module can be use-d ok
  [Game::Sudoku] 1..2
  [Game::Sudoku] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz/Game-Sudoku-1.1.5 t/02-create-and-display.t
  [Game::Sudoku] ok 1 - String rep is 81 0's
  [Game::Sudoku] ok 2 - Grid is as expected
  [Game::Sudoku] ok 3 - Empty grid is valid
  [Game::Sudoku] ok 4 - Empty grid is not complete
  [Game::Sudoku] ok 5 - String rep is as expected
  [Game::Sudoku] ok 6 - Grid is as expected
  [Game::Sudoku] ok 7 - Grid is valid
  [Game::Sudoku] ok 8 - Grid is not complete
  [Game::Sudoku] ok 9 - String rep is as expected
  [Game::Sudoku] ok 10 - Grid is as expected
  [Game::Sudoku] ok 11 - Grid is valid
  [Game::Sudoku] ok 12 - Grid is complete.
  [Game::Sudoku] 1..12
  [Game::Sudoku] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz/Game-Sudoku-1.1.5 t/03-validation.t
  [Game::Sudoku] ok 1 - 000000000000000000000000000000000000000000000000000000000000000000000000000000000 is valid
  [Game::Sudoku] ok 2 - 100000000000000000000000000000000000000000000000000000000000000000000000000000000 is valid
  [Game::Sudoku] ok 3 - 123000000000000000000000000000000000000000000000000000000000000000000000000000000 is valid
  [Game::Sudoku] ok 4 - 483921657967345821251876493548132976729564138136798245372689514814253769695417382 is valid
  [Game::Sudoku] ok 5 - 003020600900305001001806400008102900700000008006708200002609500800203009005010300 is valid
  [Game::Sudoku] ok 6 - 110000000000000000000000000000000000000000000000000000000000000000000000000000000 is invalid
  [Game::Sudoku] ok 7 - 123000000123000000000000000000000000000000000000000000000000000000000000000000000 is invalid
  [Game::Sudoku] ok 8 - 843921657967345821251876493548132976729564138136798245372689514814253769695417382 is invalid
  [Game::Sudoku] ok 9 - 003020600900305001001806400008102900700000008006708200002609500800203009005010303 is invalid
  [Game::Sudoku] 1..9
  [Game::Sudoku] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz/Game-Sudoku-1.1.5 t/04-possible.t
  [Game::Sudoku] ok 1 - Nothing to see here
  [Game::Sudoku] ok 2 - Everything is possible
  [Game::Sudoku] ok 3 - Setting returns the updated object
  [Game::Sudoku] ok 4 - Can also get a cells current value
  [Game::Sudoku] ok 5 - Requesting an unset cell returns Nil
  [Game::Sudoku] ok 6 - We have no options
  [Game::Sudoku] ok 7 - We have options
  [Game::Sudoku] not ok 8 - We have a sequence
  [Game::Sudoku] ok 9 - We have a set
  [Game::Sudoku] ok 10 - We have a list when there's no options
  [Game::Sudoku] ok 11 - We have a set
  [Game::Sudoku] # Failed test 'We have a sequence'
  [Game::Sudoku] # at t/04-possible.t line 14
  [Game::Sudoku] # expected: (Seq)
  [Game::Sudoku] #      got: (List)
  [Game::Sudoku] ok 12 - Game state is valid
  [Game::Sudoku] ok 13 - Now we have a cell
  [Game::Sudoku] ok 14 - We have no options
  [Game::Sudoku] ok 15 - We have options
  [Game::Sudoku] ok 16 - Game state is valid
  [Game::Sudoku] ok 17 - Still getting games
  [Game::Sudoku] ok 18 - Game state is invalid as we have 2 2's
  [Game::Sudoku] ok 19 - Game as expected
  [Game::Sudoku] ok 20 - Can't modify initial values
  [Game::Sudoku] ok 21 - Got expected possibilites
  [Game::Sudoku] ok 22 - Game is valid
  [Game::Sudoku] ok 23 - Game is valid
  [Game::Sudoku] ok 24 - Game is valid
  [Game::Sudoku] ok 25 - Game is valid
  [Game::Sudoku] ok 26 - Game is valid
  [Game::Sudoku] ok 27 - Game is valid
  [Game::Sudoku] ok 28 - Game is complete
  [Game::Sudoku] ok 29 - Game is valid
  [Game::Sudoku] ok 30 - Game is full
  [Game::Sudoku] ok 31 - Got expected solution
  [Game::Sudoku] 1..31
  [Game::Sudoku] # You failed 1 test of 31
  [Game::Sudoku] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/0785bc8060afe03cd9d30913d33f6cf317c78a65.tar.gz/Game-Sudoku-1.1.5 t/05-solver.t
  [Game::Sudoku] ok 1 - Game is complete
  [Game::Sudoku] ok 2 - Game is valid
  [Game::Sudoku] ok 3 - Game is full
  [Game::Sudoku] ok 4 - got expected value
  [Game::Sudoku] ok 5 - Game is complete
  [Game::Sudoku] ok 6 - Game is valid
  [Game::Sudoku] ok 7 - Game is full
  [Game::Sudoku] ok 8 - got expected value
  [Game::Sudoku] ok 9 - Game is complete
  [Game::Sudoku] ok 10 - Game is valid
  [Game::Sudoku] ok 11 - Game is full
  [Game::Sudoku] ok 12 - got expected value
  [Game::Sudoku] 1..12
  ===> Testing [FAIL]: Game::Sudoku:ver<1.1.5>:auth<zef:Scimon>
  [Game::Sudoku] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Game::Sudoku:ver<1.1.5>:auth<zef:Scimon>
  ===> Install [OK] for Game::Sudoku:ver<1.1.5>:auth<zef:Scimon>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 19.431s
               CPU time consumed: 12.933s
                     Memory peak: 979.6M (swap: 0B)

  ```
  </details>
* [ ] [HTTP::Headers](https://raku.land/cpan:HANENKAMP/HTTP::Headers) – Fail, Bisected: [afee7d8](https://github.com/rakudo/rakudo/commit/afee7d8d3197b7a093355d98a90f6f86d8bda32a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1406989-i1359286.service; invocation ID: a9aee349d5eb4a05a1ea0528a4aa6a4e
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: HTTP::Headers
  ===> Found: HTTP::Headers:ver<0.5.0>:auth<cpan:HANENKAMP> [via Zef::Repository::Ecosystems<rea>]
  [HTTP::Headers] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549445.1406990.8595.87268969071/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/H/HTTP%3A%3AHeaders/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz
  ===> Fetching [OK]: HTTP::Headers:ver<0.5.0>:auth<cpan:HANENKAMP> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549445.1406990.8595.87268969071/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz
  [HTTP::Headers] Command: tar -t -f ./HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz
  [HTTP::Headers] Command: tar -xvf ./HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz -C ../HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz
  ===> Extraction [OK]: HTTP::Headers to /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz
  ===> Testing: HTTP::Headers:ver<0.5.0>
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/content-type.t
  [HTTP::Headers] ok 1 - 
  [HTTP::Headers] ok 2 - 
  [HTTP::Headers] ok 3 - 
  [HTTP::Headers] ok 4 - 
  [HTTP::Headers] ok 5 - 
  [HTTP::Headers] ok 6 - 
  [HTTP::Headers] ok 7 - 
  [HTTP::Headers] ok 8 - 
  [HTTP::Headers] ok 9 - 
  [HTTP::Headers] 1..9
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/extending.t
  [HTTP::Headers] ok 1 - 
  [HTTP::Headers] ok 2 - 
  [HTTP::Headers] ok 3 - 
  [HTTP::Headers] 1..3
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/hash-like.t
  [HTTP::Headers] ok 1 - 
  [HTTP::Headers] Calling .header(Content-Type) is preferred to .header("Content-Type") for standard HTTP headers.
  [HTTP::Headers]   in method header at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 338
  [HTTP::Headers] ok 2 - 
  [HTTP::Headers] ok 3 - 
  [HTTP::Headers] ok 4 - 
  [HTTP::Headers] ok 5 - 
  [HTTP::Headers] ok 6 - 
  [HTTP::Headers] ok 7 - 
  [HTTP::Headers] 1..7
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/headers-from-pairs.t
  [HTTP::Headers] ok 1 - Content-Type
  [HTTP::Headers] ok 2 - Content-Length
  [HTTP::Headers] ok 3 - X-Foo-Bar
  [HTTP::Headers] ok 4 - Content-Type still ok
  [HTTP::Headers] ok 5 - Allow
  [HTTP::Headers] Calling .header(Content-Length) is preferred to .header("Content-Length") for standard HTTP headers.
  [HTTP::Headers]   in method header at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 338
  [HTTP::Headers] Calling .header(Content-Type) is preferred to .header("Content-Type") for standard HTTP headers.
  [HTTP::Headers]   in method header at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 338
  [HTTP::Headers] ok 6 - Content-Type
  [HTTP::Headers] ok 7 - Content-Length
  [HTTP::Headers] ok 8 - X-Foo-Bar
  [HTTP::Headers] ok 9 - Content-Type still ok
  [HTTP::Headers] ok 10 - Allow
  [HTTP::Headers] ok 11 - Content-Type
  [HTTP::Headers] ok 12 - Content-Length
  [HTTP::Headers] ok 13 - X-Foo-Bar
  [HTTP::Headers] Calling .header(Allow) is preferred to .header("Allow") for standard HTTP headers.
  [HTTP::Headers]   in method header at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 338
  [HTTP::Headers] Calling .header(Content-Type) is preferred to .header("Content-Type") for standard HTTP headers.
  [HTTP::Headers]   in method header at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 338
  [HTTP::Headers] ok 14 - Content-Type still ok
  [HTTP::Headers] ok 15 - Allow
  [HTTP::Headers] 1..15
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/headers.t
  [HTTP::Headers] ok 1 - 
  [HTTP::Headers] ok 2 - The object is-a '"HTTP::Headers"'
  [HTTP::Headers] ok 3 - 
  [HTTP::Headers] ok 4 - 
  [HTTP::Headers] ok 5 - 
  [HTTP::Headers] ok 6 - 
  [HTTP::Headers] ok 7 - 
  [HTTP::Headers] ok 8 - 
  [HTTP::Headers] ok 9 - 
  [HTTP::Headers] ok 10 - 
  [HTTP::Headers] ok 11 - 
  [HTTP::Headers] ok 12 - 
  [HTTP::Headers] ok 13 - 
  [HTTP::Headers] ok 14 - 
  [HTTP::Headers] ok 15 - 
  [HTTP::Headers] ok 16 - 
  [HTTP::Headers] ok 17 - 
  [HTTP::Headers] ok 18 - 
  [HTTP::Headers] ok 19 - 
  [HTTP::Headers] ok 20 - 
  [HTTP::Headers] ok 21 - 
  [HTTP::Headers] ok 22 - 
  [HTTP::Headers] ok 23 - 
  [HTTP::Headers] ok 24 - 
  [HTTP::Headers] ok 25 - 
  [HTTP::Headers] ok 26 - 
  [HTTP::Headers] ok 27 - 
  [HTTP::Headers] ok 28 - 
  [HTTP::Headers] ok 29 - 
  [HTTP::Headers] ok 30 - 
  [HTTP::Headers] ok 31 - 
  [HTTP::Headers] ok 32 - 
  [HTTP::Headers] ok 33 - 
  [HTTP::Headers] ok 34 - 
  [HTTP::Headers] ok 35 - 
  [HTTP::Headers] ok 36 - 
  [HTTP::Headers] ok 37 - 
  [HTTP::Headers] ok 38 - 
  [HTTP::Headers] ok 39 - 
  [HTTP::Headers] ok 40 - 
  [HTTP::Headers] ok 41 - 
  [HTTP::Headers] ok 42 - 
  [HTTP::Headers] ok 43 - 
  [HTTP::Headers] 1..43
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/numeric.t
  [HTTP::Headers] not ok 1 - cannot assign non-decimals to Age # TODO we want to type check Age header, but do not do so yet
  [HTTP::Headers] # Failed test 'cannot assign non-decimals to Age'
  [HTTP::Headers] # at t/numeric.t line 12
  [HTTP::Headers] ok 2 - can assign decimal on Age
  [HTTP::Headers] ok 3 - can udpate decimal on Age
  [HTTP::Headers] ok 4 - decimal assignments worked as expected for Age
  [HTTP::Headers] not ok 5 - cannot assign non-decimals to Content-Length # TODO we want to type check Content-Length headers, but do not do so yet
  [HTTP::Headers] # Failed test 'cannot assign non-decimals to Content-Length'
  [HTTP::Headers] # at t/numeric.t line 18
  [HTTP::Headers] ok 6 - can assign decimal on Content-Length
  [HTTP::Headers] ok 7 - can udpate decimal on Content-Length
  [HTTP::Headers] ok 8 - decimal assignments worked as expected for Content-Length
  [HTTP::Headers] 1..8
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/prepared.t
  [HTTP::Headers] ok 1 - 
  [HTTP::Headers] ok 2 - 
  [HTTP::Headers] ok 3 - 
  [HTTP::Headers] 1..3
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/primary-from-index-0.t
  [HTTP::Headers] ok 1 - primary from empty is Str
  [HTTP::Headers] 1..1
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/quiet.t
  [HTTP::Headers] 1..3
  [HTTP::Headers] ok 1 - got preferred warning
  [HTTP::Headers] ok 2 - class quiet worked
  [HTTP::Headers] ok 3 - method quiet worked
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/standard-names.t
  [HTTP::Headers] ok 1 - standard header method works: Accept
  [HTTP::Headers] ok 2 - standard header method works: Accept-Charset
  [HTTP::Headers] ok 3 - standard header method works: Accept-Encoding
  [HTTP::Headers] ok 4 - standard header method works: Accept-Language
  [HTTP::Headers] ok 5 - standard header method works: Accept-Ranges
  [HTTP::Headers] ok 6 - standard header method works: Age
  [HTTP::Headers] ok 7 - standard header method works: Allow
  [HTTP::Headers] ok 8 - standard header method works: Authorization
  [HTTP::Headers] ok 9 - standard header method works: Cache-Control
  [HTTP::Headers] ok 10 - standard header method works: Connection
  [HTTP::Headers] ok 11 - standard header method works: Content-Encoding
  [HTTP::Headers] ok 12 - standard header method works: Content-Language
  [HTTP::Headers] ok 13 - standard header method works: Content-Length
  [HTTP::Headers] ok 14 - standard header method works: Content-Location
  [HTTP::Headers] ok 15 - standard header method works: Content-MD5
  [HTTP::Headers] ok 16 - standard header method works: Content-Range
  [HTTP::Headers] ok 17 - standard header method works: Content-Type
  [HTTP::Headers] ok 18 - standard header method works: Cookie
  [HTTP::Headers] ok 19 - standard header method works: Date
  [HTTP::Headers] ok 20 - standard header method works: ETag
  [HTTP::Headers] ok 21 - standard header method works: Expect
  [HTTP::Headers] ok 22 - standard header method works: Expires
  [HTTP::Headers] ok 23 - standard header method works: From
  [HTTP::Headers] ok 24 - standard header method works: Host
  [HTTP::Headers] ok 25 - standard header method works: If-Match
  [HTTP::Headers] ok 26 - standard header method works: If-Modified-Since
  [HTTP::Headers] ok 27 - standard header method works: If-None-Match
  [HTTP::Headers] ok 28 - standard header method works: If-Range
  [HTTP::Headers] ok 29 - standard header method works: If-Unmodified-Since
  [HTTP::Headers] ok 30 - standard header method works: Last-Modified
  [HTTP::Headers] ok 31 - standard header method works: Location
  [HTTP::Headers] ok 32 - standard header method works: Max-Forwards
  [HTTP::Headers] ok 33 - standard header method works: Pragma
  [HTTP::Headers] ok 34 - standard header method works: Proxy-Authenticate
  [HTTP::Headers] ok 35 - standard header method works: Proxy-Authorization
  [HTTP::Headers] ok 36 - standard header method works: Range
  [HTTP::Headers] ok 37 - standard header method works: Referer
  [HTTP::Headers] ok 38 - standard header method works: Retry-After
  [HTTP::Headers] ok 39 - standard header method works: Server
  [HTTP::Headers] ok 40 - standard header method works: Set-Cookie
  [HTTP::Headers] ok 41 - standard header method works: TE
  [HTTP::Headers] ok 42 - standard header method works: Trailer
  [HTTP::Headers] ok 43 - standard header method works: Transfer-Encoding
  [HTTP::Headers] ok 44 - standard header method works: Upgrade
  [HTTP::Headers] ok 45 - standard header method works: User-Agent
  [HTTP::Headers] ok 46 - standard header method works: Vary
  [HTTP::Headers] ok 47 - standard header method works: Via
  [HTTP::Headers] ok 48 - standard header method works: WWW-Authenticate
  [HTTP::Headers] ok 49 - standard header method works: Warning
  [HTTP::Headers] ok 50 - standard header enum works: Accept
  [HTTP::Headers] ok 51 - standard header enum works: Accept-Charset
  [HTTP::Headers] ok 52 - standard header enum works: Accept-Encoding
  [HTTP::Headers] ok 53 - standard header enum works: Accept-Language
  [HTTP::Headers] ok 54 - standard header enum works: Accept-Ranges
  [HTTP::Headers] ok 55 - standard header enum works: Age
  [HTTP::Headers] ok 56 - standard header enum works: Allow
  [HTTP::Headers] ok 57 - standard header enum works: Authorization
  [HTTP::Headers] ok 58 - standard header enum works: Cache-Control
  [HTTP::Headers] ok 59 - standard header enum works: Connection
  [HTTP::Headers] ok 60 - standard header enum works: Content-Encoding
  [HTTP::Headers] ok 61 - standard header enum works: Content-Language
  [HTTP::Headers] ok 62 - standard header enum works: Content-Length
  [HTTP::Headers] ok 63 - standard header enum works: Content-Location
  [HTTP::Headers] ok 64 - standard header enum works: Content-MD5
  [HTTP::Headers] ok 65 - standard header enum works: Content-Range
  [HTTP::Headers] ok 66 - standard header enum works: Content-Type
  [HTTP::Headers] ok 67 - standard header enum works: Cookie
  [HTTP::Headers] ok 68 - standard header enum works: Date
  [HTTP::Headers] ok 69 - standard header enum works: ETag
  [HTTP::Headers] ok 70 - standard header enum works: Expect
  [HTTP::Headers] ok 71 - standard header enum works: Expires
  [HTTP::Headers] ok 72 - standard header enum works: From
  [HTTP::Headers] ok 73 - standard header enum works: Host
  [HTTP::Headers] ok 74 - standard header enum works: If-Match
  [HTTP::Headers] ok 75 - standard header enum works: If-Modified-Since
  [HTTP::Headers] ok 76 - standard header enum works: If-None-Match
  [HTTP::Headers] ok 77 - standard header enum works: If-Range
  [HTTP::Headers] ok 78 - standard header enum works: If-Unmodified-Since
  [HTTP::Headers] ok 79 - standard header enum works: Last-Modified
  [HTTP::Headers] ok 80 - standard header enum works: Location
  [HTTP::Headers] ok 81 - standard header enum works: Max-Forwards
  [HTTP::Headers] ok 82 - standard header enum works: Pragma
  [HTTP::Headers] ok 83 - standard header enum works: Proxy-Authenticate
  [HTTP::Headers] ok 84 - standard header enum works: Proxy-Authorization
  [HTTP::Headers] ok 85 - standard header enum works: Range
  [HTTP::Headers] ok 86 - standard header enum works: Referer
  [HTTP::Headers] ok 87 - standard header enum works: Retry-After
  [HTTP::Headers] ok 88 - standard header enum works: Server
  [HTTP::Headers] ok 89 - standard header enum works: Set-Cookie
  [HTTP::Headers] ok 90 - standard header enum works: TE
  [HTTP::Headers] ok 91 - standard header enum works: Trailer
  [HTTP::Headers] ok 92 - standard header enum works: Transfer-Encoding
  [HTTP::Headers] ok 93 - standard header enum works: Upgrade
  [HTTP::Headers] ok 94 - standard header enum works: User-Agent
  [HTTP::Headers] ok 95 - standard header enum works: Vary
  [HTTP::Headers] ok 96 - standard header enum works: Via
  [HTTP::Headers] ok 97 - standard header enum works: WWW-Authenticate
  [HTTP::Headers] ok 98 - standard header enum works: Warning
  [HTTP::Headers] 1..98
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/weird-names.t
  [HTTP::Headers] ok 1 - CONTENT_LENGTH -> Content-Length
  [HTTP::Headers] ok 2 - X_FOO -> X-Foo
  [HTTP::Headers] ok 3 - as-string as expected
  [HTTP::Headers] 1..3
  ===> Testing [OK] for HTTP::Headers:ver<0.5.0>
  ===> Installing: HTTP::Headers:ver<0.5.0>
  ===> Install [OK] for HTTP::Headers:ver<0.5.0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 49.541s
               CPU time consumed: 1min 9.633s
                     Memory peak: 1.3G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1404990-i1322320.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: HTTP::Headers
  ===> Found: HTTP::Headers:ver<0.5.0>:auth<cpan:HANENKAMP> [via Zef::Repository::Ecosystems<rea>]
  [HTTP::Headers] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549388.1404996.7557.345012427703/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/H/HTTP%3A%3AHeaders/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz
  ===> Fetching [OK]: HTTP::Headers:ver<0.5.0>:auth<cpan:HANENKAMP> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549388.1404996.7557.345012427703/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz
  [HTTP::Headers] Command: tar -t -f ./HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz
  [HTTP::Headers] Command: tar -xvf ./HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz -C ../HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz
  ===> Extraction [OK]: HTTP::Headers to /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz
  ===> Testing: HTTP::Headers:ver<0.5.0>
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/content-type.t
  [HTTP::Headers] ok 1 - 
  [HTTP::Headers] ok 2 - 
  [HTTP::Headers] ok 3 - 
  [HTTP::Headers] ok 4 - 
  [HTTP::Headers] ok 5 - 
  [HTTP::Headers] ok 6 - 
  [HTTP::Headers] ok 7 - 
  [HTTP::Headers] ok 8 - 
  [HTTP::Headers] ok 9 - 
  [HTTP::Headers] 1..9
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/extending.t
  [HTTP::Headers] ok 1 - 
  [HTTP::Headers] ok 2 - 
  [HTTP::Headers] Type check failed for return value; expected Seq but got List ((HTTP::Header::Custo...)
  [HTTP::Headers]   in method sorted-headers at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 386
  [HTTP::Headers]   in method as-string at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 422
  [HTTP::Headers]   in block <unit> at t/extending.t line 33
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/hash-like.t
  [HTTP::Headers] ok 1 - 
  [HTTP::Headers] Calling .header(Content-Type) is preferred to .header("Content-Type") for standard HTTP headers.
  [HTTP::Headers]   in method header at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 338
  [HTTP::Headers] ok 2 - 
  [HTTP::Headers] ok 3 - 
  [HTTP::Headers] ok 4 - 
  [HTTP::Headers] ok 5 - 
  [HTTP::Headers] ok 6 - 
  [HTTP::Headers] ok 7 - 
  [HTTP::Headers] 1..7
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/headers-from-pairs.t
  [HTTP::Headers] ok 1 - Content-Type
  [HTTP::Headers] ok 2 - Content-Length
  [HTTP::Headers] ok 3 - X-Foo-Bar
  [HTTP::Headers] ok 4 - Content-Type still ok
  [HTTP::Headers] ok 5 - Allow
  [HTTP::Headers] Calling .header(Content-Type) is preferred to .header("Content-Type") for standard HTTP headers.
  [HTTP::Headers]   in method header at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 338
  [HTTP::Headers] Calling .header(Content-Length) is preferred to .header("Content-Length") for standard HTTP headers.
  [HTTP::Headers]   in method header at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 338
  [HTTP::Headers] ok 6 - Content-Type
  [HTTP::Headers] ok 7 - Content-Length
  [HTTP::Headers] ok 8 - X-Foo-Bar
  [HTTP::Headers] ok 9 - Content-Type still ok
  [HTTP::Headers] ok 10 - Allow
  [HTTP::Headers] ok 11 - Content-Type
  [HTTP::Headers] ok 12 - Content-Length
  [HTTP::Headers] ok 13 - X-Foo-Bar
  [HTTP::Headers] Calling .header(Content-Type) is preferred to .header("Content-Type") for standard HTTP headers.
  [HTTP::Headers]   in method header at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 338
  [HTTP::Headers] Calling .header(Allow) is preferred to .header("Allow") for standard HTTP headers.
  [HTTP::Headers]   in method header at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 338
  [HTTP::Headers] ok 14 - Content-Type still ok
  [HTTP::Headers] ok 15 - Allow
  [HTTP::Headers] 1..15
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/headers.t
  [HTTP::Headers] ok 1 - 
  [HTTP::Headers] ok 2 - The object is-a '"HTTP::Headers"'
  [HTTP::Headers] Type check failed for return value; expected Seq but got List (())
  [HTTP::Headers]   in method sorted-headers at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 386
  [HTTP::Headers]   in method as-string at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 422
  [HTTP::Headers]   in block <unit> at t/headers.t line 13
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/numeric.t
  [HTTP::Headers] not ok 1 - cannot assign non-decimals to Age # TODO we want to type check Age header, but do not do so yet
  [HTTP::Headers] # Failed test 'cannot assign non-decimals to Age'
  [HTTP::Headers] # at t/numeric.t line 12
  [HTTP::Headers] ok 2 - can assign decimal on Age
  [HTTP::Headers] ok 3 - can udpate decimal on Age
  [HTTP::Headers] ok 4 - decimal assignments worked as expected for Age
  [HTTP::Headers] not ok 5 - cannot assign non-decimals to Content-Length # TODO we want to type check Content-Length headers, but do not do so yet
  [HTTP::Headers] # Failed test 'cannot assign non-decimals to Content-Length'
  [HTTP::Headers] # at t/numeric.t line 18
  [HTTP::Headers] ok 6 - can assign decimal on Content-Length
  [HTTP::Headers] ok 7 - can udpate decimal on Content-Length
  [HTTP::Headers] ok 8 - decimal assignments worked as expected for Content-Length
  [HTTP::Headers] 1..8
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/prepared.t
  [HTTP::Headers] Type check failed for return value; expected Seq but got List ((HTTP::Header::Stand...)
  [HTTP::Headers]   in method sorted-headers at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 386
  [HTTP::Headers]   in method as-string at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 422
  [HTTP::Headers]   in block <unit> at t/prepared.t line 12
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/primary-from-index-0.t
  [HTTP::Headers] ok 1 - primary from empty is Str
  [HTTP::Headers] 1..1
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/quiet.t
  [HTTP::Headers] 1..3
  [HTTP::Headers] ok 1 - got preferred warning
  [HTTP::Headers] ok 2 - class quiet worked
  [HTTP::Headers] ok 3 - method quiet worked
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/standard-names.t
  [HTTP::Headers] ok 1 - standard header method works: Accept
  [HTTP::Headers] ok 2 - standard header method works: Accept-Charset
  [HTTP::Headers] ok 3 - standard header method works: Accept-Encoding
  [HTTP::Headers] ok 4 - standard header method works: Accept-Language
  [HTTP::Headers] ok 5 - standard header method works: Accept-Ranges
  [HTTP::Headers] ok 6 - standard header method works: Age
  [HTTP::Headers] ok 7 - standard header method works: Allow
  [HTTP::Headers] ok 8 - standard header method works: Authorization
  [HTTP::Headers] ok 9 - standard header method works: Cache-Control
  [HTTP::Headers] ok 10 - standard header method works: Connection
  [HTTP::Headers] ok 11 - standard header method works: Content-Encoding
  [HTTP::Headers] ok 12 - standard header method works: Content-Language
  [HTTP::Headers] ok 13 - standard header method works: Content-Length
  [HTTP::Headers] ok 14 - standard header method works: Content-Location
  [HTTP::Headers] ok 15 - standard header method works: Content-MD5
  [HTTP::Headers] ok 16 - standard header method works: Content-Range
  [HTTP::Headers] ok 17 - standard header method works: Content-Type
  [HTTP::Headers] ok 18 - standard header method works: Cookie
  [HTTP::Headers] ok 19 - standard header method works: Date
  [HTTP::Headers] ok 20 - standard header method works: ETag
  [HTTP::Headers] ok 21 - standard header method works: Expect
  [HTTP::Headers] ok 22 - standard header method works: Expires
  [HTTP::Headers] ok 23 - standard header method works: From
  [HTTP::Headers] ok 24 - standard header method works: Host
  [HTTP::Headers] ok 25 - standard header method works: If-Match
  [HTTP::Headers] ok 26 - standard header method works: If-Modified-Since
  [HTTP::Headers] ok 27 - standard header method works: If-None-Match
  [HTTP::Headers] ok 28 - standard header method works: If-Range
  [HTTP::Headers] ok 29 - standard header method works: If-Unmodified-Since
  [HTTP::Headers] ok 30 - standard header method works: Last-Modified
  [HTTP::Headers] ok 31 - standard header method works: Location
  [HTTP::Headers] ok 32 - standard header method works: Max-Forwards
  [HTTP::Headers] ok 33 - standard header method works: Pragma
  [HTTP::Headers] ok 34 - standard header method works: Proxy-Authenticate
  [HTTP::Headers] ok 35 - standard header method works: Proxy-Authorization
  [HTTP::Headers] ok 36 - standard header method works: Range
  [HTTP::Headers] ok 37 - standard header method works: Referer
  [HTTP::Headers] ok 38 - standard header method works: Retry-After
  [HTTP::Headers] ok 39 - standard header method works: Server
  [HTTP::Headers] ok 40 - standard header method works: Set-Cookie
  [HTTP::Headers] ok 41 - standard header method works: TE
  [HTTP::Headers] ok 42 - standard header method works: Trailer
  [HTTP::Headers] ok 43 - standard header method works: Transfer-Encoding
  [HTTP::Headers] ok 44 - standard header method works: Upgrade
  [HTTP::Headers] ok 45 - standard header method works: User-Agent
  [HTTP::Headers] ok 46 - standard header method works: Vary
  [HTTP::Headers] ok 47 - standard header method works: Via
  [HTTP::Headers] ok 48 - standard header method works: WWW-Authenticate
  [HTTP::Headers] ok 49 - standard header method works: Warning
  [HTTP::Headers] ok 50 - standard header enum works: Accept
  [HTTP::Headers] ok 51 - standard header enum works: Accept-Charset
  [HTTP::Headers] ok 52 - standard header enum works: Accept-Encoding
  [HTTP::Headers] ok 53 - standard header enum works: Accept-Language
  [HTTP::Headers] ok 54 - standard header enum works: Accept-Ranges
  [HTTP::Headers] ok 55 - standard header enum works: Age
  [HTTP::Headers] ok 56 - standard header enum works: Allow
  [HTTP::Headers] ok 57 - standard header enum works: Authorization
  [HTTP::Headers] ok 58 - standard header enum works: Cache-Control
  [HTTP::Headers] ok 59 - standard header enum works: Connection
  [HTTP::Headers] ok 60 - standard header enum works: Content-Encoding
  [HTTP::Headers] ok 61 - standard header enum works: Content-Language
  [HTTP::Headers] ok 62 - standard header enum works: Content-Length
  [HTTP::Headers] ok 63 - standard header enum works: Content-Location
  [HTTP::Headers] ok 64 - standard header enum works: Content-MD5
  [HTTP::Headers] ok 65 - standard header enum works: Content-Range
  [HTTP::Headers] ok 66 - standard header enum works: Content-Type
  [HTTP::Headers] ok 67 - standard header enum works: Cookie
  [HTTP::Headers] ok 68 - standard header enum works: Date
  [HTTP::Headers] ok 69 - standard header enum works: ETag
  [HTTP::Headers] ok 70 - standard header enum works: Expect
  [HTTP::Headers] ok 71 - standard header enum works: Expires
  [HTTP::Headers] ok 72 - standard header enum works: From
  [HTTP::Headers] ok 73 - standard header enum works: Host
  [HTTP::Headers] ok 74 - standard header enum works: If-Match
  [HTTP::Headers] ok 75 - standard header enum works: If-Modified-Since
  [HTTP::Headers] ok 76 - standard header enum works: If-None-Match
  [HTTP::Headers] ok 77 - standard header enum works: If-Range
  [HTTP::Headers] ok 78 - standard header enum works: If-Unmodified-Since
  [HTTP::Headers] ok 79 - standard header enum works: Last-Modified
  [HTTP::Headers] ok 80 - standard header enum works: Location
  [HTTP::Headers] ok 81 - standard header enum works: Max-Forwards
  [HTTP::Headers] ok 82 - standard header enum works: Pragma
  [HTTP::Headers] ok 83 - standard header enum works: Proxy-Authenticate
  [HTTP::Headers] ok 84 - standard header enum works: Proxy-Authorization
  [HTTP::Headers] ok 85 - standard header enum works: Range
  [HTTP::Headers] ok 86 - standard header enum works: Referer
  [HTTP::Headers] ok 87 - standard header enum works: Retry-After
  [HTTP::Headers] ok 88 - standard header enum works: Server
  [HTTP::Headers] ok 89 - standard header enum works: Set-Cookie
  [HTTP::Headers] ok 90 - standard header enum works: TE
  [HTTP::Headers] ok 91 - standard header enum works: Trailer
  [HTTP::Headers] ok 92 - standard header enum works: Transfer-Encoding
  [HTTP::Headers] ok 93 - standard header enum works: Upgrade
  [HTTP::Headers] ok 94 - standard header enum works: User-Agent
  [HTTP::Headers] ok 95 - standard header enum works: Vary
  [HTTP::Headers] ok 96 - standard header enum works: Via
  [HTTP::Headers] ok 97 - standard header enum works: WWW-Authenticate
  [HTTP::Headers] ok 98 - standard header enum works: Warning
  [HTTP::Headers] 1..98
  [HTTP::Headers] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0 t/weird-names.t
  [HTTP::Headers] ok 1 - CONTENT_LENGTH -> Content-Length
  [HTTP::Headers] ok 2 - X_FOO -> X-Foo
  [HTTP::Headers] Type check failed for return value; expected Seq but got List ((HTTP::Header::Stand...)
  [HTTP::Headers]   in method sorted-headers at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 386
  [HTTP::Headers]   in method as-string at /home/coke/sandbox/blin/data/zef-data/tmp/HTTP%3A%3AHeaders%3Aver%3C0.5.0%3E%3Aauth%3Ccpan%3AHANENKAMP%3E.tar.gz/HTTP-Headers-0.5.0/lib/HTTP/Headers.pm6 (HTTP::Headers) line 422
  [HTTP::Headers]   in block <unit> at t/weird-names.t line 16
  ===> Testing [FAIL]: HTTP::Headers:ver<0.5.0>
  [HTTP::Headers] Failed to get passing tests, but continuing with --force-test
  ===> Installing: HTTP::Headers:ver<0.5.0>
  ===> Install [OK] for HTTP::Headers:ver<0.5.0>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 55.398s
               CPU time consumed: 51.930s
                     Memory peak: 1.4G (swap: 0B)

  ```
  </details>
* [ ] [Ranker](https://raku.land/cpan:UZLUISF/Ranker) – Fail, Bisected: [afee7d8](https://github.com/rakudo/rakudo/commit/afee7d8d3197b7a093355d98a90f6f86d8bda32a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1406766-i1459432.service; invocation ID: beedd6acfced4de99907c38dc3946b02
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Ranker
  ===> Found: Ranker:ver<0.0.3>:auth<cpan:UZLUISF> [via Zef::Repository::Ecosystems<rea>]
  [Ranker] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549440.1406767.3652.0976630509304/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/R/Ranker/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz
  ===> Fetching [OK]: Ranker:ver<0.0.3>:auth<cpan:UZLUISF> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549440.1406767.3652.0976630509304/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz
  [Ranker] Command: tar -t -f ./Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz
  [Ranker] Command: tar -xvf ./Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz -C ../Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz
  ===> Extraction [OK]: Ranker to /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz
  ===> Testing: Ranker:ver<0.0.2>:auth<gitlab:uzluisf>
  [Ranker] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/basic-ranker.t6
  [Ranker] # Subtest: when simple rankables are used
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 3 - last ranking
  [Ranker]     1..3
  [Ranker] ok 1 - when simple rankables are used
  [Ranker] # Subtest: when ranking by block
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 2 - when ranking by block
  [Ranker] # Subtest: when ranking by block and asc true
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 3 - when ranking by block and asc true
  [Ranker] 1..3
  [Ranker] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/basic-ranking.t6
  [Ranker] # Subtest: testing percentile
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct percentile
  [Ranker]         1..1
  [Ranker]     ok 1 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct percentile
  [Ranker]         1..1
  [Ranker]     ok 2 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct percentile
  [Ranker]         1..1
  [Ranker]     ok 3 - third ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - correct percentile
  [Ranker]         1..1
  [Ranker]     ok 4 - last ranking
  [Ranker]     1..4
  [Ranker] ok 1 - testing percentile
  [Ranker] # Subtest: testing z-score
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct z-score
  [Ranker]         1..1
  [Ranker]     ok 1 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct z-score
  [Ranker]         1..1
  [Ranker]     ok 2 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct z-score
  [Ranker]         1..1
  [Ranker]     ok 3 - third ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - correct z-score
  [Ranker]         1..1
  [Ranker]     ok 4 - last ranking
  [Ranker]     # Subtest: when standard deviation is zero
  [Ranker]         # Subtest: first ranking
  [Ranker]             ok 1 - correct z-score
  [Ranker]             1..1
  [Ranker]         ok 1 - first ranking
  [Ranker]         1..1
  [Ranker]     ok 5 - when standard deviation is zero
  [Ranker]     1..5
  [Ranker] ok 2 - testing z-score
  [Ranker] 1..2
  [Ranker] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/basic-rankings.t6
  [Ranker] # Subtest: testing the mean
  [Ranker]     # Subtest: when there are rankables
  [Ranker]         ok 1 - correct mean value
  [Ranker]         1..1
  [Ranker]     ok 1 - when there are rankables
  [Ranker]     # Subtest: when there are no rankables
  [Ranker]         ok 1 - correct NaN value
  [Ranker]         1..1
  [Ranker]     ok 2 - when there are no rankables
  [Ranker]     # Subtest: when rankables contain Any values
  [Ranker]         # Subtest: did we throws-like Exception?
  [Ranker]             1..3
  [Ranker]             ok 1 - code dies
  [Ranker]             ok 2 - right exception type (Exception)
  [Ranker]             ok 3 - .message matches /errors/
  [Ranker]         ok 1 - did we throws-like Exception?
  [Ranker]         1..1
  [Ranker]     ok 3 - when rankables contain Any values
  [Ranker]     1..3
  [Ranker] ok 1 - testing the mean
  [Ranker] # Subtest: testing the standard deviation
  [Ranker]     # Subtest: when there are rankables
  [Ranker]         ok 1 - correct standard deviation
  [Ranker]         1..1
  [Ranker]     ok 1 - when there are rankables
  [Ranker]     # Subtest: when all rankables are the same
  [Ranker]         ok 1 - correct standard deviation
  [Ranker]         1..1
  [Ranker]     ok 2 - when all rankables are the same
  [Ranker]     # Subtest: when there are no rankables
  [Ranker]         ok 1 - result is NaN
  [Ranker]         1..1
  [Ranker]     ok 3 - when there are no rankables
  [Ranker]     1..3
  [Ranker] ok 2 - testing the standard deviation
  [Ranker] 1..2
  [Ranker] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-dense-strategy.t6
  [Ranker] # Subtest: when list of rankables is large
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - fourth ranking
  [Ranker]     # Subtest: fifth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 6 - fifth ranking
  [Ranker]     # Subtest: sixth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 7 - sixth ranking
  [Ranker]     # Subtest: seventh ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 8 - seventh ranking
  [Ranker]     1..8
  [Ranker] ok 1 - when list of rankables is large
  [Ranker] # Subtest: when list of rankables is small
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 2 - when list of rankables is small
  [Ranker] 1..2
  [Ranker] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-fractional-strategy.t6
  [Ranker] # Subtest: when list of rankables is large
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - fourth ranking
  [Ranker]     # Subtest: second to last ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - second to last ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 6 - last ranking
  [Ranker]     1..6
  [Ranker] ok 1 - when list of rankables is large
  [Ranker] # Subtest: when using wikipedia example
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 1 - first ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - third ranking
  [Ranker]     # Subtest: second to last ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second to last ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - last ranking
  [Ranker]     1..4
  [Ranker] ok 2 - when using wikipedia example
  [Ranker] # Subtest: when list of rankables is small
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - fourth ranking
  [Ranker]     1..5
  [Ranker] ok 3 - when list of rankables is small
  [Ranker] 1..3
  [Ranker] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-modified-strategy.t6
  [Ranker] # Subtest: when list of rankables is large
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - fourth ranking
  [Ranker]     # Subtest: fifth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 6 - fifth ranking
  [Ranker]     # Subtest: sixth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 7 - sixth ranking
  [Ranker]     # Subtest: seventh ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 8 - seventh ranking
  [Ranker]     1..8
  [Ranker] ok 1 - when list of rankables is large
  [Ranker] # Subtest: when list of rankables is small
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 2 - when list of rankables is small
  [Ranker] 1..2
  [Ranker] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-ordinal-strategy.t6
  [Ranker] # Subtest: when list of rankables is large
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: second to last ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - second to last ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - last ranking
  [Ranker]     1..5
  [Ranker] ok 1 - when list of rankables is large
  [Ranker] # Subtest: when list of rankables is small
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - fourth ranking
  [Ranker]     1..5
  [Ranker] ok 2 - when list of rankables is small
  [Ranker] 1..2
  [Ranker] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-standard-strategy.t6
  [Ranker] # Subtest: when list of rankables is large
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 4 - third ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 5 - fourth ranking
  [Ranker]     # Subtest: fifth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 6 - fifth ranking
  [Ranker]     # Subtest: sixth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 7 - sixth ranking
  [Ranker]     # Subtest: seventh ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 8 - seventh ranking
  [Ranker]     1..8
  [Ranker] ok 1 - when list of rankables is large
  [Ranker] # Subtest: when list of rankables is small
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 2 - when list of rankables is small
  [Ranker] # Subtest: when ranking with a non-default score block
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 3 - when ranking with a non-default score block
  [Ranker] 1..3
  [Ranker] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-strategy.t6
  [Ranker] # Subtest: fails when instantiating Strategy
  [Ranker]     # Subtest: did we throws-like X::AdHoc?
  [Ranker]         1..2
  [Ranker]         ok 1 - code dies
  [Ranker]         ok 2 - right exception type (X::AdHoc)
  [Ranker]     ok 1 - did we throws-like X::AdHoc?
  [Ranker]     1..1
  [Ranker] ok 1 - fails when instantiating Strategy
  [Ranker] 1..1
  ===> Testing [OK] for Ranker:ver<0.0.2>:auth<gitlab:uzluisf>
  ===> Installing: Ranker:ver<0.0.2>:auth<gitlab:uzluisf>
  ===> Install [OK] for Ranker:ver<0.0.2>:auth<gitlab:uzluisf>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 46.017s
               CPU time consumed: 1min 4.228s
                     Memory peak: 1.6G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1405012-i1434083.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Ranker
  ===> Found: Ranker:ver<0.0.3>:auth<cpan:UZLUISF> [via Zef::Repository::Ecosystems<rea>]
  [Ranker] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792549387.1405019.1022.5318463295663/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/R/Ranker/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz
  ===> Fetching [OK]: Ranker:ver<0.0.3>:auth<cpan:UZLUISF> to /home/coke/sandbox/blin/data/zef-data/tmp/1792549387.1405019.1022.5318463295663/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz
  [Ranker] Command: tar -t -f ./Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz
  [Ranker] Command: tar -xvf ./Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz -C ../Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz
  ===> Extraction [OK]: Ranker to /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz
  ===> Testing: Ranker:ver<0.0.2>:auth<gitlab:uzluisf>
  [Ranker] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/basic-ranker.t6
  [Ranker] # Subtest: when simple rankables are used
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 3 - last ranking
  [Ranker]     1..3
  [Ranker] ok 1 - when simple rankables are used
  [Ranker] # Subtest: when ranking by block
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - rank correct
  [Ranker]         ok 2 - rankables correct
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 2 - when ranking by block
  [Ranker] # Subtest: when ranking by block and asc true
  [Ranker] Type check failed for return value; expected Seq but got List ((25, 100, 150))
  [Ranker]   in method scores-unique-sorted at /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3/lib/Ranker/Strategies.pm6 (Ranker::Strategies) line 61
  [Ranker]   in method execute at /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3/lib/Ranker/Strategies.pm6 (Ranker::Strategies) line 109
  [Ranker]   in method rank at /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3/lib/Ranker/Strategies.pm6 (Ranker::Strategies) line 74
  [Ranker]   in sub rank at /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3/lib/Ranker.pm6 (Ranker) line 61
  [Ranker]   in sub  at t/basic-ranker.t6 line 66
  [Ranker]   in sub subtest at /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/share/perl6/core/sources/19B11E36AA87FFBE8BE6D591C6668274476ADBCC (Test) line 431
  [Ranker]   in sub subtest at /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/share/perl6/core/sources/19B11E36AA87FFBE8BE6D591C6668274476ADBCC (Test) line 416
  [Ranker]   in block <unit> at t/basic-ranker.t6 line 59
  [Ranker] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/basic-ranking.t6
  [Ranker] # Subtest: testing percentile
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct percentile
  [Ranker]         1..1
  [Ranker]     ok 1 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct percentile
  [Ranker]         1..1
  [Ranker]     ok 2 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct percentile
  [Ranker]         1..1
  [Ranker]     ok 3 - third ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - correct percentile
  [Ranker]         1..1
  [Ranker]     ok 4 - last ranking
  [Ranker]     1..4
  [Ranker] ok 1 - testing percentile
  [Ranker] # Subtest: testing z-score
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct z-score
  [Ranker]         1..1
  [Ranker]     ok 1 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct z-score
  [Ranker]         1..1
  [Ranker]     ok 2 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct z-score
  [Ranker]         1..1
  [Ranker]     ok 3 - third ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - correct z-score
  [Ranker]         1..1
  [Ranker]     ok 4 - last ranking
  [Ranker]     # Subtest: when standard deviation is zero
  [Ranker]         # Subtest: first ranking
  [Ranker]             ok 1 - correct z-score
  [Ranker]             1..1
  [Ranker]         ok 1 - first ranking
  [Ranker]         1..1
  [Ranker]     ok 5 - when standard deviation is zero
  [Ranker]     1..5
  [Ranker] ok 2 - testing z-score
  [Ranker] 1..2
  [Ranker] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/basic-rankings.t6
  [Ranker] # Subtest: testing the mean
  [Ranker]     # Subtest: when there are rankables
  [Ranker]         ok 1 - correct mean value
  [Ranker]         1..1
  [Ranker]     ok 1 - when there are rankables
  [Ranker]     # Subtest: when there are no rankables
  [Ranker]         ok 1 - correct NaN value
  [Ranker]         1..1
  [Ranker]     ok 2 - when there are no rankables
  [Ranker]     # Subtest: when rankables contain Any values
  [Ranker]         # Subtest: did we throws-like Exception?
  [Ranker]             1..3
  [Ranker]             ok 1 - code dies
  [Ranker]             ok 2 - right exception type (Exception)
  [Ranker]             ok 3 - .message matches /errors/
  [Ranker]         ok 1 - did we throws-like Exception?
  [Ranker]         1..1
  [Ranker]     ok 3 - when rankables contain Any values
  [Ranker]     1..3
  [Ranker] ok 1 - testing the mean
  [Ranker] # Subtest: testing the standard deviation
  [Ranker]     # Subtest: when there are rankables
  [Ranker]         ok 1 - correct standard deviation
  [Ranker]         1..1
  [Ranker]     ok 1 - when there are rankables
  [Ranker]     # Subtest: when all rankables are the same
  [Ranker]         ok 1 - correct standard deviation
  [Ranker]         1..1
  [Ranker]     ok 2 - when all rankables are the same
  [Ranker]     # Subtest: when there are no rankables
  [Ranker]         ok 1 - result is NaN
  [Ranker]         1..1
  [Ranker]     ok 3 - when there are no rankables
  [Ranker]     1..3
  [Ranker] ok 2 - testing the standard deviation
  [Ranker] 1..2
  [Ranker] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-dense-strategy.t6
  [Ranker] # Subtest: when list of rankables is large
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - fourth ranking
  [Ranker]     # Subtest: fifth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 6 - fifth ranking
  [Ranker]     # Subtest: sixth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 7 - sixth ranking
  [Ranker]     # Subtest: seventh ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 8 - seventh ranking
  [Ranker]     1..8
  [Ranker] ok 1 - when list of rankables is large
  [Ranker] # Subtest: when list of rankables is small
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 2 - when list of rankables is small
  [Ranker] 1..2
  [Ranker] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-fractional-strategy.t6
  [Ranker] # Subtest: when list of rankables is large
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - fourth ranking
  [Ranker]     # Subtest: second to last ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - second to last ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 6 - last ranking
  [Ranker]     1..6
  [Ranker] ok 1 - when list of rankables is large
  [Ranker] # Subtest: when using wikipedia example
  [Ranker] Type check failed for return value; expected Seq but got List ((1.0, 2.0, 3.0, 4.0,...)
  [Ranker]   in method scores-unique-sorted at /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3/lib/Ranker/Strategies.pm6 (Ranker::Strategies) line 61
  [Ranker]   in method execute at /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3/lib/Ranker/Strategies.pm6 (Ranker::Strategies) line 178
  [Ranker]   in method rank at /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3/lib/Ranker/Strategies.pm6 (Ranker::Strategies) line 74
  [Ranker]   in sub  at t/strategies/basic-fractional-strategy.t6 line 44
  [Ranker]   in sub subtest at /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/share/perl6/core/sources/19B11E36AA87FFBE8BE6D591C6668274476ADBCC (Test) line 431
  [Ranker]   in sub subtest at /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/share/perl6/core/sources/19B11E36AA87FFBE8BE6D591C6668274476ADBCC (Test) line 416
  [Ranker]   in block <unit> at t/strategies/basic-fractional-strategy.t6 line 42
  [Ranker] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-modified-strategy.t6
  [Ranker] # Subtest: when list of rankables is large
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - fourth ranking
  [Ranker]     # Subtest: fifth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 6 - fifth ranking
  [Ranker]     # Subtest: sixth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 7 - sixth ranking
  [Ranker]     # Subtest: seventh ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 8 - seventh ranking
  [Ranker]     1..8
  [Ranker] ok 1 - when list of rankables is large
  [Ranker] # Subtest: when list of rankables is small
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 2 - when list of rankables is small
  [Ranker] 1..2
  [Ranker] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-ordinal-strategy.t6
  [Ranker] # Subtest: when list of rankables is large
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: second to last ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - second to last ranking
  [Ranker]     # Subtest: last ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - last ranking
  [Ranker]     1..5
  [Ranker] ok 1 - when list of rankables is large
  [Ranker] # Subtest: when list of rankables is small
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 5 - fourth ranking
  [Ranker]     1..5
  [Ranker] ok 2 - when list of rankables is small
  [Ranker] 1..2
  [Ranker] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-standard-strategy.t6
  [Ranker] # Subtest: when list of rankables is large
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 4 - third ranking
  [Ranker]     # Subtest: fourth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 5 - fourth ranking
  [Ranker]     # Subtest: fifth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 6 - fifth ranking
  [Ranker]     # Subtest: sixth ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 7 - sixth ranking
  [Ranker]     # Subtest: seventh ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct score
  [Ranker]         ok 3 - correct rankable values
  [Ranker]         1..3
  [Ranker]     ok 8 - seventh ranking
  [Ranker]     1..8
  [Ranker] ok 1 - when list of rankables is large
  [Ranker] # Subtest: when list of rankables is small
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 2 - when list of rankables is small
  [Ranker] # Subtest: when ranking with a non-default score block
  [Ranker]     ok 1 - correct number of rankings
  [Ranker]     # Subtest: first ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 2 - first ranking
  [Ranker]     # Subtest: second ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 3 - second ranking
  [Ranker]     # Subtest: third ranking
  [Ranker]         ok 1 - correct rank
  [Ranker]         ok 2 - correct rankable values
  [Ranker]         1..2
  [Ranker]     ok 4 - third ranking
  [Ranker]     1..4
  [Ranker] ok 3 - when ranking with a non-default score block
  [Ranker] 1..3
  [Ranker] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/Ranker%3Aver%3C0.0.3%3E%3Aauth%3Ccpan%3AUZLUISF%3E.tar.gz/Ranker-0.0.3 t/strategies/basic-strategy.t6
  [Ranker] # Subtest: fails when instantiating Strategy
  [Ranker]     # Subtest: did we throws-like X::AdHoc?
  [Ranker]         1..2
  [Ranker]         ok 1 - code dies
  [Ranker]         ok 2 - right exception type (X::AdHoc)
  [Ranker]     ok 1 - did we throws-like X::AdHoc?
  [Ranker]     1..1
  [Ranker] ok 1 - fails when instantiating Strategy
  [Ranker] 1..1
  ===> Testing [FAIL]: Ranker:ver<0.0.2>:auth<gitlab:uzluisf>
  [Ranker] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Ranker:ver<0.0.2>:auth<gitlab:uzluisf>
  ===> Install [OK] for Ranker:ver<0.0.2>:auth<gitlab:uzluisf>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 49.232s
               CPU time consumed: 41.622s
                     Memory peak: 1.7G (swap: 0B)

  ```
  </details>
* [ ] [Sys::HostAddr](https://raku.land/zef:jmaslak/Sys::HostAddr) – Fail, Bisected: [afee7d8](https://github.com/rakudo/rakudo/commit/afee7d8d3197b7a093355d98a90f6f86d8bda32a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p1440025-i1497547.service; invocation ID: e92f7083c8314e4ca0656e69ffdad25a
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Sys::HostAddr
  ===> Found: Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak> [via Zef::Repository::Ecosystems<fez>]
  [Sys::HostAddr] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792551171.1440026.5627.539411911624/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz https://360.zef.pm/S/YS/SYS_HOSTADDR/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz
  ===> Fetching [OK]: Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak> to /home/coke/sandbox/blin/data/zef-data/tmp/1792551171.1440026.5627.539411911624/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz
  [Sys::HostAddr] Command: tar -t -f ./03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz
  [Sys::HostAddr] Command: tar -xvf ./03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz -C ../03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz
  ===> Extraction [OK]: Sys::HostAddr to /home/coke/sandbox/blin/data/zef-data/tmp/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz
  ===> Testing: Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak>
  [Sys::HostAddr] Command: /tmp/whateverable/rakudo-moar/9a94801c154543573d926e6258e062f3c3782635/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz/Sys-HostAddr-0.2.1 t/01-basic.t
  [Sys::HostAddr] # Distro: Ubuntu 26.04.1 LTS
  [Sys::HostAddr] # ip command found: True
  [Sys::HostAddr] ok 1 - Constructor runs
  [Sys::HostAddr] # Subtest: public
  [Sys::HostAddr]     ok 1 - public method exists
  [Sys::HostAddr]     ok 2 - # SKIP Not performing remote tests, set %*ENV<REMOTE_TESTING>
  [Sys::HostAddr]     ok 3 - # SKIP Not performing remote tests, set %*ENV<REMOTE_TESTING>
  [Sys::HostAddr]     1..3
  [Sys::HostAddr] ok 2 - public
  [Sys::HostAddr] # Subtest: interfaces
  [Sys::HostAddr]     ok 1 - Interface list
  [Sys::HostAddr]     ok 2 - Interface list includes at least 1 interface
  [Sys::HostAddr]     1..2
  [Sys::HostAddr] ok 3 - interfaces
  [Sys::HostAddr] # Subtest: addresses
  [Sys::HostAddr]     ok 1 - Address list
  [Sys::HostAddr]     ok 2 - At least one address returned
  [Sys::HostAddr]     1..2
  [Sys::HostAddr] ok 4 - addresses
  [Sys::HostAddr] # Subtest: addresses-on-interface
  [Sys::HostAddr]     ok 1 - All IPs represented
  [Sys::HostAddr]     1..1
  [Sys::HostAddr] ok 5 - addresses-on-interface
  [Sys::HostAddr] # Subtest: guess-ip-for-host
  [Sys::HostAddr]     ok 1 - guess-ip-for-host method exists
  [Sys::HostAddr]     ok 2 - # SKIP Not performing remote tests, set %*ENV<REMOTE_TESTING>
  [Sys::HostAddr]     1..2
  [Sys::HostAddr] ok 6 - guess-ip-for-host
  [Sys::HostAddr] # Subtest: guess-main
  [Sys::HostAddr]     ok 1 - guess-main method exists
  [Sys::HostAddr]     ok 2 - Check we get the expected IP
  [Sys::HostAddr]     1..2
  [Sys::HostAddr] ok 7 - guess-main
  [Sys::HostAddr] ok 8 - Path wasn't reset
  [Sys::HostAddr] 1..8
  ===> Testing [OK] for Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak>
  ===> Installing: Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak>
  ===> Install [OK] for Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 12.367s
               CPU time consumed: 1min 47.952s
                     Memory peak: 2.8G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p1439976-i1489298.service; invocation ID: f78875f4cb4c4971b924b55621039e18
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Sys::HostAddr
  ===> Found: Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak> [via Zef::Repository::Ecosystems<fez>]
  [Sys::HostAddr] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1792551154.1439977.9430.77818098097/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz https://360.zef.pm/S/YS/SYS_HOSTADDR/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz
  ===> Fetching [OK]: Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak> to /home/coke/sandbox/blin/data/zef-data/tmp/1792551154.1439977.9430.77818098097/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz
  [Sys::HostAddr] Command: tar -t -f ./03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz
  [Sys::HostAddr] Command: tar -xvf ./03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz -C ../03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz
  ===> Extraction [OK]: Sys::HostAddr to /home/coke/sandbox/blin/data/zef-data/tmp/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz
  ===> Testing: Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak>
  [Sys::HostAddr] Command: /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz/Sys-HostAddr-0.2.1 t/01-basic.t
  [Sys::HostAddr] # Distro: Ubuntu 26.04.1 LTS
  [Sys::HostAddr] # ip command found: True
  [Sys::HostAddr] ok 1 - Constructor runs
  [Sys::HostAddr] # Subtest: public
  [Sys::HostAddr]     ok 1 - public method exists
  [Sys::HostAddr]     ok 2 - # SKIP Not performing remote tests, set %*ENV<REMOTE_TESTING>
  [Sys::HostAddr]     ok 3 - # SKIP Not performing remote tests, set %*ENV<REMOTE_TESTING>
  [Sys::HostAddr]     1..3
  [Sys::HostAddr] ok 2 - public
  [Sys::HostAddr] # Subtest: interfaces
  [Sys::HostAddr] Type check failed for return value; expected Seq but got List (("enp2s0", "lo", "wl...)
  [Sys::HostAddr]   in method interfaces at /home/coke/sandbox/blin/data/zef-data/tmp/03a4e97bdddc51a2bbc3d475eeb9f06040f4a37b.tar.gz/Sys-HostAddr-0.2.1/lib/Sys/HostAddr.pm6 (Sys::HostAddr) line 55
  [Sys::HostAddr]   in sub  at t/01-basic.t line 39
  [Sys::HostAddr]   in sub subtest at /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/share/perl6/core/sources/19B11E36AA87FFBE8BE6D591C6668274476ADBCC (Test) line 431
  [Sys::HostAddr]   in sub subtest at /tmp/whateverable/rakudo-moar/aa1262d24269fcbc10e6ef7039d91f05bde64b04/share/perl6/core/sources/19B11E36AA87FFBE8BE6D591C6668274476ADBCC (Test) line 416
  [Sys::HostAddr]   in block <unit> at t/01-basic.t line 38
  ===> Testing [FAIL]: Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak>
  [Sys::HostAddr] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak>
  ===> Install [OK] for Sys::HostAddr:ver<0.2.1>:auth<zef:jmaslak>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 5.907s
               CPU time consumed: 6.740s
                     Memory peak: 1.1G (swap: 0B)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| InstallableButUntested    |     1 | [IO::Socket::Async::SSL](https://raku.land/zef:raku-community-modules/IO::Socket::Async::SSL) |
| AlwaysFail                |     4 | [JSON::Class](https://raku.land/zef:jonathanstowe/JSON::Class) [License::SPDX](https://raku.land/zef:jonathanstowe/License::SPDX) [META6](https://raku.land/zef:jonathanstowe/META6) [Test::META](https://raku.land/zef:jonathanstowe/Test::META) |
| Fail                      |     9 | [BinaryHeap](https://raku.land/zef:dumarchie/BinaryHeap) [CSS::Properties](https://raku.land/zef:dwarring/CSS::Properties) [Commands](https://raku.land/zef:lizmat/Commands) [Cro::HTTP](https://raku.land/zef:cro/Cro::HTTP) [Game::Sudoku](https://raku.land/zef:Scimon/Game::Sudoku) [HTTP::Headers](https://raku.land/cpan:HANENKAMP/HTTP::Headers) [Injector](https://raku.land/zef:FCO/Injector) [Ranker](https://raku.land/cpan:UZLUISF/Ranker) [Sys::HostAddr](https://raku.land/zef:jmaslak/Sys::HostAddr) |
| OK                        |    34 | ⋯                         |



This run started on 2026-10-21T03:05:48Z and finished in 44 minutes.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
