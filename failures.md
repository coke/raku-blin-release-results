[Blin](https://github.com/Raku/Blin) results between 2026.08 ([24e6e53](https://github.com/rakudo/rakudo/commit/24e6e5312f2868680413b0597aef8772f6b5bcea)) and be8107f365 ([be8107f](https://github.com/rakudo/rakudo/commit/be8107f365b15e3b75859bd093302ba5a39f28ab)):

* [ ] [Stomp](https://raku.land/zef:raku-community-modules/Stomp) – Fail, Bisected: [29d41e0](https://github.com/rakudo/rakudo/commit/29d41e01f80b6fc67bb4a2472987de0c9ff580c9)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2187094-i2228772.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Stomp
  ===> Found: Stomp:ver<0.1.0>:auth<zef:raku-community-modules> [via Zef::Repository::Ecosystems<fez>]
  [Stomp] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789874336.2187103.9908.05310479809/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz https://360.zef.pm/S/TO/STOMP/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz
  ===> Fetching [OK]: Stomp:ver<0.1.0>:auth<zef:raku-community-modules> to /home/coke/sandbox/blin/data/zef-data/tmp/1789874336.2187103.9908.05310479809/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz
  [Stomp] Command: tar -t -f ./ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz
  [Stomp] Command: tar -xvf ./ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz -C ../ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz
  ===> Extraction [OK]: Stomp to /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz
  ===> Testing: Stomp:ver<0.1.0>:auth<zef:raku-community-modules>
  [Stomp] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz/dist t/001-meta.rakutest
  [Stomp] 1..1
  [Stomp] ok 1 - # SKIP no Test::META - skipping
  [Stomp] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz/dist t/client.rakutest
  [Stomp] 1..31
  [Stomp] ok 1 - Connected to the correct host
  [Stomp] ok 2 - Connected to the correct port
  [Stomp] ok 3 - Failed STOMP server connection breaks connect Promise
  [Stomp] ok 4 - Client sent valid message to server
  [Stomp] ok 5 - Client sent a CONNECT command
  [Stomp] ok 6 - Client sent login
  [Stomp] ok 7 - Client sent password
  [Stomp] ok 8 - Client sent accept-version header
  [Stomp] ok 9 - Client sent no message body
  [Stomp] ok 10 - CONNECTED message completes connection
  [Stomp] ok 11 - send method sent well-formed message
  [Stomp] ok 12 - message has SEND command
  [Stomp] ok 13 - destination header correct
  [Stomp] ok 14 - has default content-type header
  [Stomp] ok 15 - message had expected body
  [Stomp] ok 16 - Promise retunred by send was kept
  [Stomp] ok 17 - can set content-type header
  [Stomp] ok 18 - subscribe returns a Supply
  [Stomp] ok 19 - did not yet send subscription request
  [Stomp] ok 20 - subscribe method sent well-formed message
  [Stomp] ok 21 - message has SUBSCRIBE command
  [Stomp] ok 22 - destination header correct
  [Stomp] ok 23 - had an id header
  [Stomp] ok 24 - no messages received yet
  [Stomp] ok 25 - one message now received
  [Stomp] ok 26 - it's a Stomp::Message
  [Stomp] ok 27 - has the command MESSAGE
  [Stomp] ok 28 - has the correct body
  [Stomp] ok 29 - unsubscribing sent well-formed message
  [Stomp] ok 30 - message has UNSUBSCRIBE command
  [Stomp] ok 31 - id matched the subscription
  [Stomp] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz/dist t/message.rakutest
  [Stomp] 1..3
  [Stomp] ok 1 - SEND message correctly formatted
  [Stomp] ok 2 - Stomp::Message must be constructed with a command
  [Stomp] ok 3 - CONNECT message with empty body correctly formatted
  [Stomp] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz/dist t/parser.rakutest
  [Stomp] 1..51
  [Stomp] ok 1 - Can parse CONNECTED command (no headers/body)
  [Stomp] ok 2 - Can parse MESSAGE command (no headers/body)
  [Stomp] ok 3 - Can parse RECEIPT command (no headers/body)
  [Stomp] ok 4 - Can parse ERROR command (no headers/body)
  [Stomp] ok 5 - Can parse SEND command (no headers/body)
  [Stomp] ok 6 - Can parse SUBSCRIBE command (no headers/body)
  [Stomp] ok 7 - Can parse UNSUBSCRIBE command (no headers/body)
  [Stomp] ok 8 - Can parse BEGIN command (no headers/body)
  [Stomp] ok 9 - Can parse COMMIT command (no headers/body)
  [Stomp] ok 10 - Can parse ABORT command (no headers/body)
  [Stomp] ok 11 - Can parse ACK command (no headers/body)
  [Stomp] ok 12 - Can parse NACK command (no headers/body)
  [Stomp] ok 13 - Can parse DISCONNECT command (no headers/body)
  [Stomp] ok 14 - Can parse CONNECT command (no headers/body)
  [Stomp] ok 15 - Can parse STOMP command (no headers/body)
  [Stomp] # Subtest: Cannot parse unknown command FOO
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 16 - Cannot parse unknown command FOO
  [Stomp] ok 17 - Server parser accepts CONNECTED
  [Stomp] # Subtest: Client parser rejects CONNECTED
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 18 - Client parser rejects CONNECTED
  [Stomp] ok 19 - Server parser accepts MESSAGE
  [Stomp] # Subtest: Client parser rejects MESSAGE
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 20 - Client parser rejects MESSAGE
  [Stomp] ok 21 - Server parser accepts RECEIPT
  [Stomp] # Subtest: Client parser rejects RECEIPT
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 22 - Client parser rejects RECEIPT
  [Stomp] ok 23 - Server parser accepts ERROR
  [Stomp] # Subtest: Client parser rejects ERROR
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 24 - Client parser rejects ERROR
  [Stomp] ok 25 - Client parser accepts SEND
  [Stomp] # Subtest: Server parser rejects SEND
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 26 - Server parser rejects SEND
  [Stomp] ok 27 - Client parser accepts SUBSCRIBE
  [Stomp] # Subtest: Server parser rejects SUBSCRIBE
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 28 - Server parser rejects SUBSCRIBE
  [Stomp] ok 29 - Client parser accepts UNSUBSCRIBE
  [Stomp] # Subtest: Server parser rejects UNSUBSCRIBE
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 30 - Server parser rejects UNSUBSCRIBE
  [Stomp] ok 31 - Client parser accepts BEGIN
  [Stomp] # Subtest: Server parser rejects BEGIN
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 32 - Server parser rejects BEGIN
  [Stomp] ok 33 - Client parser accepts COMMIT
  [Stomp] # Subtest: Server parser rejects COMMIT
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 34 - Server parser rejects COMMIT
  [Stomp] ok 35 - Client parser accepts ABORT
  [Stomp] # Subtest: Server parser rejects ABORT
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 36 - Server parser rejects ABORT
  [Stomp] ok 37 - Client parser accepts ACK
  [Stomp] # Subtest: Server parser rejects ACK
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 38 - Server parser rejects ACK
  [Stomp] ok 39 - Client parser accepts NACK
  [Stomp] # Subtest: Server parser rejects NACK
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 40 - Server parser rejects NACK
  [Stomp] ok 41 - Client parser accepts DISCONNECT
  [Stomp] # Subtest: Server parser rejects DISCONNECT
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 42 - Server parser rejects DISCONNECT
  [Stomp] ok 43 - Client parser accepts CONNECT
  [Stomp] # Subtest: Server parser rejects CONNECT
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 44 - Server parser rejects CONNECT
  [Stomp] ok 45 - Client parser accepts STOMP
  [Stomp] # Subtest: Server parser rejects STOMP
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 46 - Server parser rejects STOMP
  [Stomp] ok 47 - Parsed message with header/body
  [Stomp] ok 48 - Parser made a Stomp::Message
  [Stomp] ok 49 - Command is correct
  [Stomp] ok 50 - Header is correct
  [Stomp] ok 51 - Body is correct
  [Stomp] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz/dist t/server.rakutest
  [Stomp] 1..28
  [Stomp] ok 1 - Must provide host and port to new (1)
  [Stomp] ok 2 - Must provide host and port to new (2)
  [Stomp] ok 3 - Must provide host and port to new (3)
  [Stomp] ok 4 - Stomp::Server listen method returns a Supply
  [Stomp] ok 5 - Not listening before supply is tapped
  [Stomp] ok 6 - Listening once supply is tapped
  [Stomp] ok 7 - Listening on correct host
  [Stomp] ok 8 - Listening on correct port
  [Stomp] ok 9 - Closing supply tap also closes socket
  [Stomp] ok 10 - Server responded to CONNECT with valid message
  [Stomp] ok 11 - Server sent CONNECTED command
  [Stomp] ok 12 - Server sent version header
  [Stomp] ok 13 - Server sent no message body
  [Stomp] ok 14 - and the tap received the correct object
  [Stomp] ok 15 - new connection doesn't have a subscription
  [Stomp] ok 16 - now have one subscription
  [Stomp] ok 17 - and it has the right id
  [Stomp] ok 18 - and it has the right destination
  [Stomp] ok 19 - and the ack is 'auto'
  [Stomp] ok 20 - subscription matches message to that destination
  [Stomp] ok 21 - subscription-for-message
  [Stomp] ok 22 - connection matches message to that destination
  [Stomp] ok 23 - got the message from published-messages
  [Stomp] ok 24 - now have no subscription after unsubscribe
  [Stomp] ok 25 - subscription no longer matches message to that destination
  [Stomp] ok 26 - connection no longer matches message to that destination
  [Stomp] ok 27 - Server responded to invalid message with valid message
  [Stomp] ok 28 - Server sent ERROR command
  ===> Testing [OK] for Stomp:ver<0.1.0>:auth<zef:raku-community-modules>
  ===> Installing: Stomp:ver<0.1.0>:auth<zef:raku-community-modules>
  ===> Install [OK] for Stomp:ver<0.1.0>:auth<zef:raku-community-modules>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 57.923s
               CPU time consumed: 2min 9.615s
                     Memory peak: 1.4G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2182882-i2104521.service; invocation ID: ae60f87be5104f778f66bfb61a6f056c
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Stomp
  ===> Found: Stomp:ver<0.1.0>:auth<zef:raku-community-modules> [via Zef::Repository::Ecosystems<fez>]
  [Stomp] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789874226.2182890.4774.561715057947/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz https://360.zef.pm/S/TO/STOMP/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz
  ===> Fetching [OK]: Stomp:ver<0.1.0>:auth<zef:raku-community-modules> to /home/coke/sandbox/blin/data/zef-data/tmp/1789874226.2182890.4774.561715057947/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz
  [Stomp] Command: tar -t -f ./ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz
  [Stomp] Command: tar -xvf ./ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz -C ../ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz
  ===> Extraction [OK]: Stomp to /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz
  ===> Testing: Stomp:ver<0.1.0>:auth<zef:raku-community-modules>
  [Stomp] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz/dist t/001-meta.rakutest
  [Stomp] 1..1
  [Stomp] ok 1 - # SKIP no Test::META - skipping
  [Stomp] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz/dist t/client.rakutest
  [Stomp] 1..31
  [Stomp] ok 1 - Connected to the correct host
  [Stomp] ok 2 - Connected to the correct port
  [Stomp] ok 3 - Failed STOMP server connection breaks connect Promise
  [Stomp] ok 4 - Client sent valid message to server
  [Stomp] ok 5 - Client sent a CONNECT command
  [Stomp] ok 6 - Client sent login
  [Stomp] ok 7 - Client sent password
  [Stomp] ok 8 - Client sent accept-version header
  [Stomp] ok 9 - Client sent no message body
  [Stomp] ok 10 - CONNECTED message completes connection
  [Stomp] ok 11 - send method sent well-formed message
  [Stomp] ok 12 - message has SEND command
  [Stomp] ok 13 - destination header correct
  [Stomp] ok 14 - has default content-type header
  [Stomp] ok 15 - message had expected body
  [Stomp] ok 16 - Promise retunred by send was kept
  [Stomp] ok 17 - can set content-type header
  [Stomp] ok 18 - subscribe returns a Supply
  [Stomp] ok 19 - did not yet send subscription request
  [Stomp] ok 20 - subscribe method sent well-formed message
  [Stomp] ok 21 - message has SUBSCRIBE command
  [Stomp] ok 22 - destination header correct
  [Stomp] ok 23 - had an id header
  [Stomp] ok 24 - no messages received yet
  [Stomp] ok 25 - one message now received
  [Stomp] ok 26 - it's a Stomp::Message
  [Stomp] ok 27 - has the command MESSAGE
  [Stomp] ok 28 - has the correct body
  [Stomp] ok 29 - unsubscribing sent well-formed message
  [Stomp] ok 30 - message has UNSUBSCRIBE command
  [Stomp] ok 31 - id matched the subscription
  [Stomp] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz/dist t/message.rakutest
  [Stomp] 1..3
  [Stomp] ok 1 - SEND message correctly formatted
  [Stomp] ok 2 - Stomp::Message must be constructed with a command
  [Stomp] ok 3 - CONNECT message with empty body correctly formatted
  [Stomp] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz/dist t/parser.rakutest
  [Stomp] 1..51
  [Stomp] ok 1 - Can parse CONNECTED command (no headers/body)
  [Stomp] ok 2 - Can parse MESSAGE command (no headers/body)
  [Stomp] ok 3 - Can parse RECEIPT command (no headers/body)
  [Stomp] ok 4 - Can parse ERROR command (no headers/body)
  [Stomp] ok 5 - Can parse SEND command (no headers/body)
  [Stomp] ok 6 - Can parse SUBSCRIBE command (no headers/body)
  [Stomp] ok 7 - Can parse UNSUBSCRIBE command (no headers/body)
  [Stomp] ok 8 - Can parse BEGIN command (no headers/body)
  [Stomp] ok 9 - Can parse COMMIT command (no headers/body)
  [Stomp] ok 10 - Can parse ABORT command (no headers/body)
  [Stomp] ok 11 - Can parse ACK command (no headers/body)
  [Stomp] ok 12 - Can parse NACK command (no headers/body)
  [Stomp] ok 13 - Can parse DISCONNECT command (no headers/body)
  [Stomp] ok 14 - Can parse CONNECT command (no headers/body)
  [Stomp] ok 15 - Can parse STOMP command (no headers/body)
  [Stomp] # Subtest: Cannot parse unknown command FOO
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 16 - Cannot parse unknown command FOO
  [Stomp] ok 17 - Server parser accepts CONNECTED
  [Stomp] # Subtest: Client parser rejects CONNECTED
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 18 - Client parser rejects CONNECTED
  [Stomp] ok 19 - Server parser accepts MESSAGE
  [Stomp] # Subtest: Client parser rejects MESSAGE
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 20 - Client parser rejects MESSAGE
  [Stomp] ok 21 - Server parser accepts RECEIPT
  [Stomp] # Subtest: Client parser rejects RECEIPT
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 22 - Client parser rejects RECEIPT
  [Stomp] ok 23 - Server parser accepts ERROR
  [Stomp] # Subtest: Client parser rejects ERROR
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 24 - Client parser rejects ERROR
  [Stomp] ok 25 - Client parser accepts SEND
  [Stomp] # Subtest: Server parser rejects SEND
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 26 - Server parser rejects SEND
  [Stomp] ok 27 - Client parser accepts SUBSCRIBE
  [Stomp] # Subtest: Server parser rejects SUBSCRIBE
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 28 - Server parser rejects SUBSCRIBE
  [Stomp] ok 29 - Client parser accepts UNSUBSCRIBE
  [Stomp] # Subtest: Server parser rejects UNSUBSCRIBE
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 30 - Server parser rejects UNSUBSCRIBE
  [Stomp] ok 31 - Client parser accepts BEGIN
  [Stomp] # Subtest: Server parser rejects BEGIN
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 32 - Server parser rejects BEGIN
  [Stomp] ok 33 - Client parser accepts COMMIT
  [Stomp] # Subtest: Server parser rejects COMMIT
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 34 - Server parser rejects COMMIT
  [Stomp] ok 35 - Client parser accepts ABORT
  [Stomp] # Subtest: Server parser rejects ABORT
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 36 - Server parser rejects ABORT
  [Stomp] ok 37 - Client parser accepts ACK
  [Stomp] # Subtest: Server parser rejects ACK
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 38 - Server parser rejects ACK
  [Stomp] ok 39 - Client parser accepts NACK
  [Stomp] # Subtest: Server parser rejects NACK
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 40 - Server parser rejects NACK
  [Stomp] ok 41 - Client parser accepts DISCONNECT
  [Stomp] # Subtest: Server parser rejects DISCONNECT
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 42 - Server parser rejects DISCONNECT
  [Stomp] ok 43 - Client parser accepts CONNECT
  [Stomp] # Subtest: Server parser rejects CONNECT
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 44 - Server parser rejects CONNECT
  [Stomp] ok 45 - Client parser accepts STOMP
  [Stomp] # Subtest: Server parser rejects STOMP
  [Stomp]     1..3
  [Stomp]     ok 1 - code dies
  [Stomp]     ok 2 - right exception type (X::Stomp::MalformedMessage)
  [Stomp]     ok 3 - .reason matches invalid command
  [Stomp] ok 46 - Server parser rejects STOMP
  [Stomp] ok 47 - Parsed message with header/body
  [Stomp] ok 48 - Parser made a Stomp::Message
  [Stomp] ok 49 - Command is correct
  [Stomp] ok 50 - Header is correct
  [Stomp] ok 51 - Body is correct
  [Stomp] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/ef8d4d443a711d336ff54fd80ba239b5657caada.tar.gz/dist t/server.rakutest
  [Stomp] 1..28
  [Stomp] ok 1 - Must provide host and port to new (1)
  [Stomp] ok 2 - Must provide host and port to new (2)
  [Stomp] ok 3 - Must provide host and port to new (3)
  [Stomp] ok 4 - Stomp::Server listen method returns a Supply
  [Stomp] ok 5 - Not listening before supply is tapped
  [Stomp] ok 6 - Listening once supply is tapped
  [Stomp] ok 7 - Listening on correct host
  [Stomp] ok 8 - Listening on correct port
  [Stomp] ok 9 - Closing supply tap also closes socket
  [Stomp] ok 10 - Server responded to CONNECT with valid message
  [Stomp] ok 11 - Server sent CONNECTED command
  [Stomp] ok 12 - Server sent version header
  [Stomp] ok 13 - Server sent no message body
  [Stomp] ok 14 - and the tap received the correct object
  [Stomp] No such method 'subscriptions' for invocant of type 'Any'
  [Stomp]   in block <unit> at t/server.rakutest line 85
  [Stomp] # You planned 28 tests, but ran 14
  ===> Testing [FAIL]: Stomp:ver<0.1.0>:auth<zef:raku-community-modules>
  [Stomp] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Stomp:ver<0.1.0>:auth<zef:raku-community-modules>
  ===> Install [OK] for Stomp:ver<0.1.0>:auth<zef:raku-community-modules>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 1min 42.449s
               CPU time consumed: 1min 56.162s
                     Memory peak: 1.2G (swap: 0B)

  ```
  </details>
* [ ] [CSS::Properties](https://raku.land/zef:dwarring/CSS::Properties) – Fail, Bisected: [6cf7c71](https://github.com/rakudo/rakudo/commit/6cf7c71a971f04d1a2ac2322998631a9a1bcdaac)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2282261-i2202347.service; invocation ID: 7fefdf07d88a40449486f636b31ab0b5
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: CSS::Properties
  ===> Found: CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10> [via Zef::Repository::Ecosystems<fez>]
  [CSS::Properties] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789876827.2282268.7711.627623105575/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz https://360.zef.pm/C/SS/CSS_PROPERTIES/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz
  ===> Fetching [OK]: CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10> to /home/coke/sandbox/blin/data/zef-data/tmp/1789876827.2282268.7711.627623105575/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz
  [CSS::Properties] Command: tar -t -f ./f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz
  [CSS::Properties] Command: tar -xvf ./f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz -C ../f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz
  ===> Extraction [OK]: CSS::Properties to /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz
  ===> Testing: CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10>
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/00-readme.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/01-property-basic.t
  [CSS::Properties] 1..18
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/02-style-basic.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/ast.t
  [CSS::Properties] 1..4
  [CSS::Properties] ok 1 - ast
  [CSS::Properties] ok 2 - style unoptimized
  [CSS::Properties] ok 3 - ast
  [CSS::Properties] ok 4 - style optimized
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/at-font-face.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/box-fonts.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/box-measure.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/box.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/calc.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/colors.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/css-fonts.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/declarations.t
  [CSS::Properties] 1..47
  [CSS::Properties] ok 1 - :values constructor
  [CSS::Properties] ok 2 - box property
  [CSS::Properties] ok 3 - edges property
  [CSS::Properties] ok 4 - simple property
  [CSS::Properties] ok 5 - margin-left is a margin edge
  [CSS::Properties] ok 6 - default azimuth
  [CSS::Properties] ok 7 - default azimuth
  [CSS::Properties] ok 8 - default background position
  [CSS::Properties] ok 9 - default margin
  [CSS::Properties] ok 10 - default margin-left
  [CSS::Properties] ok 11 - default margin left type
  [CSS::Properties] ok 12 - default background-color
  [CSS::Properties] ok 13 - default background-color
  [CSS::Properties] ok 14 - basic css rewritten
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/errors.t
  [CSS::Properties] 1..6
  [CSS::Properties] ok 1 - 
  [CSS::Properties] unable to parse CSS property 'width: 2furlongs;'
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] unable to parse CSS property 'width: foo(42);'
  [CSS::Properties] ok 5 - 
  [CSS::Properties] expected type of length, got number: calc(42)
  [CSS::Properties] ok 6 - 
  [CSS::Properties] unable to evaluate expression: calc(2em + 3hz)
  [CSS::Properties] usage: calc( <calc-sum> )
  [CSS::Properties] unable to evaluate expression: calc('foo')
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/extend.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/important.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/inherit.t
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
  [CSS::Properties]     ok 1 - cloned css
  [CSS::Properties]     ok 2 - cloned css
  [CSS::Properties]     ok 3 - cloned+inherited css
  [CSS::Properties]     ok 4 - inherited+cloned css
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     ok 7 - 
  [CSS::Properties]     ok 8 - original css
  [CSS::Properties]     1..8
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/measure.t
  [CSS::Properties] 1..32
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/modules.t
  [CSS::Properties] 1..5
  [CSS::Properties] ok 1 - azimuth is unknown in CSS1
  [CSS::Properties] ok 2 - azimuth is known in CSS21
  [CSS::Properties] ok 3 - azimuth is known in CSS3
  [CSS::Properties] dropping unknown @fontface property azimuth
  [CSS::Properties] ok 4 - src is known in @font-face
  [CSS::Properties] ok 5 - azimuth is unknown in @font-face
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/optimize.t
  [CSS::Properties] 1..16
  [CSS::Properties] ok 1 - optimised ast border:1px solid red;
  [CSS::Properties] ok 2 - optimised css border:1px solid red;
  [CSS::Properties] ok 3 - optimised ast border-width:5pt 5px 5in 5mm;
  [CSS::Properties] ok 4 - optimised css border-width:5pt 5px 5in 5mm;
  [CSS::Properties] ok 5 - optimised ast border-top:5px!important;
  [CSS::Properties] ok 6 - optimised css border-top:5px!important;
  [CSS::Properties] ok 7 - optimised ast border:5pt solid; border-color:red green blue yellow;
  [CSS::Properties] ok 8 - optimised css border:5pt solid; border-color:red green blue yellow;
  [CSS::Properties] ok 9 - optimised ast font-family:times; font-size:inherit; font-weight:inherit;
  [CSS::Properties] ok 10 - optimised css font-family:times; font-size:inherit; font-weight:inherit;
  [CSS::Properties] ok 11 - optimised ast background:no-repeat 50% 75%;
  [CSS::Properties] ok 12 - optimised css background:no-repeat 50% 75%;
  [CSS::Properties] ok 13 - optimised ast font:1.1em/1.3 Verdana, Arial, sans-serif;
  [CSS::Properties] ok 14 - optimised css font:1.1em/1.3 Verdana, Arial, sans-serif;
  [CSS::Properties] ok 15 - optimised ast list-style:circle;
  [CSS::Properties] ok 16 - optimised css list-style:circle;
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/page-box.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/svg-properties.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/threads.t
  [CSS::Properties] 1..4
  [CSS::Properties] ok 1 - basic
  [CSS::Properties] ok 2 - info
  [CSS::Properties] ok 3 - no property name errors
  [CSS::Properties] ok 4 - mixed modules
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/units.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/vivify.t
  [CSS::Properties] 1..6
  [CSS::Properties] ok 1 - vivifed-name
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/24e6e5312f2868680413b0597aef8772f6b5bcea/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/write.t
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
  ===> Testing [OK] for CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10>
  ===> Installing: CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10>
  ===> Install [OK] for CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 9min 41.396s
               CPU time consumed: 10min 549ms
                     Memory peak: 2G (swap: 766.5M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2271494-i2137988.service; invocation ID: b8f08de647e7486f87f0deacb0cb6e4b
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: CSS::Properties
  ===> Found: CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10> [via Zef::Repository::Ecosystems<fez>]
  [CSS::Properties] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789876510.2271509.1736.3482167161815/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz https://360.zef.pm/C/SS/CSS_PROPERTIES/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz
  ===> Fetching [OK]: CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10> to /home/coke/sandbox/blin/data/zef-data/tmp/1789876510.2271509.1736.3482167161815/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz
  [CSS::Properties] Command: tar -t -f ./f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz
  [CSS::Properties] Command: tar -xvf ./f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz -C ../f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz
  ===> Extraction [OK]: CSS::Properties to /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz
  ===> Testing: CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10>
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/00-readme.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/01-property-basic.t
  [CSS::Properties] 1..18
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/02-style-basic.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/ast.t
  [CSS::Properties] 1..4
  [CSS::Properties] ok 1 - ast
  [CSS::Properties] ok 2 - style unoptimized
  [CSS::Properties] ok 3 - ast
  [CSS::Properties] ok 4 - style optimized
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/at-font-face.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/box-fonts.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/box-measure.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/box.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/calc.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/colors.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/css-fonts.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/declarations.t
  [CSS::Properties] 1..47
  [CSS::Properties] ok 1 - :values constructor
  [CSS::Properties] ok 2 - box property
  [CSS::Properties] ok 3 - edges property
  [CSS::Properties] ok 4 - simple property
  [CSS::Properties] ok 5 - margin-left is a margin edge
  [CSS::Properties] ok 6 - default azimuth
  [CSS::Properties] ok 7 - default azimuth
  [CSS::Properties] ok 8 - default background position
  [CSS::Properties] ok 9 - default margin
  [CSS::Properties] ok 10 - default margin-left
  [CSS::Properties] ok 11 - default margin left type
  [CSS::Properties] ok 12 - default background-color
  [CSS::Properties] ok 13 - default background-color
  [CSS::Properties] ok 14 - basic css rewritten
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/errors.t
  [CSS::Properties] 1..6
  [CSS::Properties] ok 1 - 
  [CSS::Properties] unable to parse CSS property 'width: 2furlongs;'
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] unable to parse CSS property 'width: foo(42);'
  [CSS::Properties] ok 5 - 
  [CSS::Properties] expected type of length, got number: calc(42)
  [CSS::Properties] ok 6 - 
  [CSS::Properties] unable to evaluate expression: calc(2em + 3hz)
  [CSS::Properties] usage: calc( <calc-sum> )
  [CSS::Properties] unable to evaluate expression: calc('foo')
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/extend.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/important.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/inherit.t
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
  [CSS::Properties]     ok 1 - cloned css
  [CSS::Properties]     ok 2 - cloned css
  [CSS::Properties]     ok 3 - cloned+inherited css
  [CSS::Properties]     ok 4 - inherited+cloned css
  [CSS::Properties]     ok 5 - 
  [CSS::Properties]     ok 6 - 
  [CSS::Properties]     ok 7 - 
  [CSS::Properties]     ok 8 - original css
  [CSS::Properties]     1..8
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/measure.t
  [CSS::Properties] 1..32
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/modules.t
  [CSS::Properties] 1..5
  [CSS::Properties] ok 1 - azimuth is unknown in CSS1
  [CSS::Properties] ok 2 - azimuth is known in CSS21
  [CSS::Properties] ok 3 - azimuth is known in CSS3
  [CSS::Properties] dropping unknown @fontface property azimuth
  [CSS::Properties] ok 4 - src is known in @font-face
  [CSS::Properties] ok 5 - azimuth is unknown in @font-face
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/optimize.t
  [CSS::Properties] 1..16
  [CSS::Properties] ok 1 - optimised ast border:1px solid red;
  [CSS::Properties] ok 2 - optimised css border:1px solid red;
  [CSS::Properties] ok 3 - optimised ast border-width:5pt 5px 5in 5mm;
  [CSS::Properties] ok 4 - optimised css border-width:5pt 5px 5in 5mm;
  [CSS::Properties] ok 5 - optimised ast border-top:5px!important;
  [CSS::Properties] ok 6 - optimised css border-top:5px!important;
  [CSS::Properties] ok 7 - optimised ast border:5pt solid; border-color:red green blue yellow;
  [CSS::Properties] ok 8 - optimised css border:5pt solid; border-color:red green blue yellow;
  [CSS::Properties] ok 9 - optimised ast font-family:times; font-size:inherit; font-weight:inherit;
  [CSS::Properties] ok 10 - optimised css font-family:times; font-size:inherit; font-weight:inherit;
  [CSS::Properties] ok 11 - optimised ast background:no-repeat 50% 75%;
  [CSS::Properties] ok 12 - optimised css background:no-repeat 50% 75%;
  [CSS::Properties] ok 13 - optimised ast font:1.1em/1.3 Verdana, Arial, sans-serif;
  [CSS::Properties] ok 14 - optimised css font:1.1em/1.3 Verdana, Arial, sans-serif;
  [CSS::Properties] ok 15 - optimised ast list-style:circle;
  [CSS::Properties] ok 16 - optimised css list-style:circle;
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/page-box.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/svg-properties.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/threads.t
  [CSS::Properties] 1..4
  [CSS::Properties] MoarVM oops: MVM_str_hash_fetch_nocheck called with a stale hashtable pointer
  [CSS::Properties]    at SETTING::src/core.c/Hash/Typed.rakumod:11  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:ASSIGN-KEY)
  [CSS::Properties]  from /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9/lib/CSS/Properties.rakumod (CSS::Properties):330  (/home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9/.precomp/ACC227A2C59C784F0B2E45F5498F1A3C9796FD8F/74/743BD9FCBFC0D9B0D4D5F4BE67AFA4FE449F40FF:)
  [CSS::Properties]  from SETTING::src/core.c/operators.rakumod:360  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:infix:<andthen>)
  [CSS::Properties]  from /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9/lib/CSS/Properties.rakumod (CSS::Properties):329  (/home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9/.precomp/ACC227A2C59C784F0B2E45F5498F1A3C9796FD8F/74/743BD9FCBFC0D9B0D4D5F4BE67AFA4FE449F40FF:)
  [CSS::Properties]  from /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9/lib/CSS/Properties.rakumod (CSS::Properties):322  (/home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9/.precomp/ACC227A2C59C784F0B2E45F5498F1A3C9796FD8F/74/743BD9FCBFC0D9B0D4D5F4BE67AFA4FE449F40FF:STORE)
  [CSS::Properties]  from src/Perl6/bootstrap.c/BOOTSTRAP.nqp:2614  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/lib/Perl6/BOOTSTRAP/v6c.moarvm:)
  [CSS::Properties]  from t/threads.t:28  (<ephemeral file>:)
  [CSS::Properties]  from SETTING::src/core.c/Rakudo/Internals/HyperRaceSharedImpl.rakumod:106  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:process-batch)
  [CSS::Properties]  from SETTING::src/core.c/Rakudo/Internals/HyperPipeline.rakumod:124  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:)
  [CSS::Properties]  from SETTING::src/core.c/Rakudo/Internals/HyperPipeline.rakumod:123  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:)
  [CSS::Properties]  from SETTING::src/core.c/Rakudo/Internals/HyperPipeline.rakumod:113  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:)
  [CSS::Properties]  from SETTING::src/core.c/Promise.rakumod:370  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:)
  [CSS::Properties]  from SETTING::src/core.c/ThreadPoolScheduler.rakumod:911  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:)
  [CSS::Properties]  from SETTING::src/core.c/ThreadPoolScheduler.rakumod:271  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:)
  [CSS::Properties]  from SETTING::src/core.c/ThreadPoolScheduler.rakumod:249  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:run-one)
  [CSS::Properties]  from SETTING::src/core.c/ThreadPoolScheduler.rakumod:290  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:)
  [CSS::Properties]  from SETTING::src/core.c/Thread.rakumod:84  (/tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/share/perl6/runtime/CORE.c.setting.moarvm:THREAD-ENTRY)
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/units.t
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
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/vivify.t
  [CSS::Properties] 1..6
  [CSS::Properties] ok 1 - vivifed-name
  [CSS::Properties] ok 2 - 
  [CSS::Properties] ok 3 - 
  [CSS::Properties] ok 4 - 
  [CSS::Properties] ok 5 - 
  [CSS::Properties] ok 6 - 
  [CSS::Properties] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/f1b1015317c03fb74197067930bc3cdd939038eb.tar.gz/CSS-Properties-0.10.9 t/write.t
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
  ===> Testing [FAIL]: CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10>
  [CSS::Properties] Failed to get passing tests, but continuing with --force-test
  ===> Installing: CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10>
  ===> Install [OK] for CSS::Properties:ver<0.10.9>:auth<zef:dwarring>:api<0.10>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 5min 23.020s
               CPU time consumed: 5min 15.633s
                     Memory peak: 1.1G (swap: 621.3M)

  ```
  </details>
* [ ] [Polyglot::Regexen](https://raku.land/zef:guifa/Polyglot::Regexen) – Fail, Bisected: [aab0778](https://github.com/rakudo/rakudo/commit/aab0778725da5848824f07514c0ae355d972926a)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2049275-i2070637.service; invocation ID: 6a6fc99da63040c7a1c640f1cdaf1489
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Polyglot::Regexen
  ===> Found: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> [via Zef::Repository::Ecosystems<fez>]
  [Polyglot::Regexen] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789870523.2049282.2662.638383207373/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz https://360.zef.pm/P/OL/POLYGLOT_REGEXEN/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Fetching [OK]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> to /home/coke/sandbox/blin/data/zef-data/tmp/1789870523.2049282.2662.638383207373/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
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
                 Service runtime: 2min 17.361s
               CPU time consumed: 2min 31.755s
                     Memory peak: 1.6G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2044618-i2009106.service; invocation ID: 284e33c725544177bfc70207b9618c81
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Polyglot::Regexen
  ===> Found: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> [via Zef::Repository::Ecosystems<fez>]
  [Polyglot::Regexen] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789870384.2044619.2734.827234857157/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz https://360.zef.pm/P/OL/POLYGLOT_REGEXEN/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Fetching [OK]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa> to /home/coke/sandbox/blin/data/zef-data/tmp/1789870384.2044619.2734.827234857157/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  [Polyglot::Regexen] Command: tar -t -f ./17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  [Polyglot::Regexen] Command: tar -xvf ./17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz -C ../17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Extraction [OK]: Polyglot::Regexen to /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz
  ===> Testing: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/00-sanity.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/00-sanity.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regexen.rakumod (Polyglot::Regexen)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions-Mixin.rakumod (Polyglot::Regex::ECMA262::Actions-Mixin)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions-Mixin.rakumod (Polyglot::Regex::ECMA262::Actions-Mixin):8
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regexen.rakumod (Polyglot::Regexen):5
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/00-sanity.rakutest:3
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/01-literals.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/01-literals.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support):5
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/01-literals.rakutest:4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/02-character-classes.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/02-character-classes.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support):5
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/02-character-classes.rakutest:4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/03-alternation.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/03-alternation.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support):5
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/03-alternation.rakutest:4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/04-assertions.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/04-assertions.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support):5
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/04-assertions.rakutest:4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/05-quantifiers.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/05-quantifiers.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support):5
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/05-quantifiers.rakutest:4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/06-captures.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/06-captures.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support):5
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/06-captures.rakutest:4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/07-unicode.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/07-unicode.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support):5
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/07-unicode.rakutest:4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/08-modifiers.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/08-modifiers.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/Support.rakumod (Support):5
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/08-modifiers.rakutest:4
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/09-role.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/09-role.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/09-role.rakutest:3
  [Polyglot::Regexen] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist t/ecma/10-usage.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/10-usage.rakutest
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regexen.rakumod (Polyglot::Regexen)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions-Mixin.rakumod (Polyglot::Regex::ECMA262::Actions-Mixin)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions)
  [Polyglot::Regexen] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes)
  [Polyglot::Regexen] An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  [Polyglot::Regexen] Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes):222
  [Polyglot::Regexen] Exception details:
  [Polyglot::Regexen]   Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  [Polyglot::Regexen]     in any new at src/Raku/ast/regex.rakumod line 2061
  [Polyglot::Regexen]     in block  at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Classes.rakumod (Polyglot::Regex::ECMA262::Classes) line 222
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions.rakumod (Polyglot::Regex::ECMA262::Actions):2
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regex/ECMA262/Actions-Mixin.rakumod (Polyglot::Regex::ECMA262::Actions-Mixin):8
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/lib/Polyglot/Regexen.rakumod (Polyglot::Regexen):5
  [Polyglot::Regexen] at /home/coke/sandbox/blin/data/zef-data/tmp/17071274ecb11bce167fcb8d42ae1a45eba739f5.tar.gz/dist/t/ecma/10-usage.rakutest:1
  ===> Testing [FAIL]: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  [Polyglot::Regexen] Failed to get passing tests, but continuing with --force-test
  ===> Installing: Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>
  ===> Install [FAIL] for Polyglot::Regexen:ver<0.1.0>:auth<zef:guifa>: ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Polyglot::Regexen_zef:guifa_0.1.0_0/sources/BC6D3C1653A62CB7973AF2249F0997287ACC0612 (Polyglot::Regex::ECMA262::Actions)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Polyglot::Regexen_zef:guifa_0.1.0_0/sources/963BC5BF2466B70304F9EA3766FAD96D15589D78 (Polyglot::Regex::ECMA262::Classes)
  An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  at /home/coke/sandbox/blin/installed/Polyglot::Regexen_zef:guifa_0.1.0_0/sources/963BC5BF2466B70304F9EA3766FAD96D15589D78 (Polyglot::Regex::ECMA262::Classes):222
  Exception details:
    Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
      in any new at src/Raku/ast/regex.rakumod line 2061
      in block  at /home/coke/sandbox/blin/installed/Polyglot::Regexen_zef:guifa_0.1.0_0/sources/963BC5BF2466B70304F9EA3766FAD96D15589D78 (Polyglot::Regex::ECMA262::Classes) line 222


  at /home/coke/sandbox/blin/installed/Polyglot::Regexen_zef:guifa_0.1.0_0/sources/BC6D3C1653A62CB7973AF2249F0997287ACC0612 (Polyglot::Regex::ECMA262::Actions):2

  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Polyglot::Regexen_zef:guifa_0.1.0_0/sources/BC6D3C1653A62CB7973AF2249F0997287ACC0612 (Polyglot::Regex::ECMA262::Actions)
  ===SORRY!=== Error while compiling /home/coke/sandbox/blin/installed/Polyglot::Regexen_zef:guifa_0.1.0_0/sources/963BC5BF2466B70304F9EA3766FAD96D15589D78 (Polyglot::Regex::ECMA262::Classes)
  An exception X::TypeCheck::Binding::Parameter occurred while evaluating a constant:
  Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
  at /home/coke/sandbox/blin/installed/Polyglot::Regexen_zef:guifa_0.1.0_0/sources/963BC5BF2466B70304F9EA3766FAD96D15589D78 (Polyglot::Regex::ECMA262::Classes):222
  Exception details:
    Type check failed in binding to parameter '$elements'; expected List but got Mu (Mu)
      in any new at src/Raku/ast/regex.rakumod line 2061
      in block  at /home/coke/sandbox/blin/installed/Polyglot::Regexen_zef:guifa_0.1.0_0/sources/963BC5BF2466B70304F9EA3766FAD96D15589D78 (Polyglot::Regex::ECMA262::Classes) line 222


  at /home/coke/sandbox/blin/installed/Polyglot::Regexen_zef:guifa_0.1.0_0/sources/BC6D3C1653A62CB7973AF2249F0997287ACC0612 (Polyglot::Regex::ECMA262::Actions):2

            Finished with result: exit-code
  Main processes terminated with: code=exited, status=1/FAILURE
                 Service runtime: 2min 21.136s
               CPU time consumed: 2min 25.947s
                     Memory peak: 1.4G (swap: 0B)

  ```
  </details>
* [ ] [Terminal::UI](https://raku.land/zef:bduggan/Terminal::UI) – Fail, Bisected: [f841d9a](https://github.com/rakudo/rakudo/commit/f841d9ace153fb2c99d01b79bfadebbd39704a0a) [6b65291](https://github.com/rakudo/rakudo/commit/6b65291224e70825fc33ce1421444fd1688fd3ab)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2237327-i2199506.service; invocation ID: ce97d9d644cf4014bf22800f713e3f7e
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Terminal::UI
  ===> Found: Terminal::UI:ver<0.1.14>:auth<zef:bduggan> [via Zef::Repository::Ecosystems<fez>]
  [Terminal::UI] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789875603.2237328.6537.978463655059/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz https://360.zef.pm/T/ER/TERMINAL_UI/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  ===> Fetching [OK]: Terminal::UI:ver<0.1.14>:auth<zef:bduggan> to /home/coke/sandbox/blin/data/zef-data/tmp/1789875603.2237328.6537.978463655059/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
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
                 Service runtime: 3min 79ms
               CPU time consumed: 3min 13.768s
                     Memory peak: 1.5G (swap: 136.8M)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2231541-i2294492.service
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: Terminal::UI
  ===> Found: Terminal::UI:ver<0.1.14>:auth<zef:bduggan> [via Zef::Repository::Ecosystems<fez>]
  [Terminal::UI] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789875451.2231552.2759.5564539295824/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz https://360.zef.pm/T/ER/TERMINAL_UI/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  ===> Fetching [OK]: Terminal::UI:ver<0.1.14>:auth<zef:bduggan> to /home/coke/sandbox/blin/data/zef-data/tmp/1789875451.2231552.2759.5564539295824/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  [Terminal::UI] Command: tar -t -f ./97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  [Terminal::UI] Command: tar -xvf ./97be0392703c0ef562b9092d0a52c2623157131c.tar.gz -C ../97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  ===> Extraction [OK]: Terminal::UI to /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz
  ===> Testing: Terminal::UI:ver<0.1.14>:auth<zef:bduggan>
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/00-basic.rakutest
  [Terminal::UI] 1..6
  [Terminal::UI] ok 1 - Terminal::UI module can be use-d ok
  [Terminal::UI] ok 2 - Terminal::UI::Screen module can be use-d ok
  [Terminal::UI] ok 3 - Terminal::UI::Frame module can be use-d ok
  [Terminal::UI] ok 4 - Terminal::UI::Pane module can be use-d ok
  [Terminal::UI] ok 5 - Terminal::UI::Input module can be use-d ok
  [Terminal::UI] ok 6 - Terminal::UI::Style module can be use-d ok
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/01-sizes.rakutest
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
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/02-screen.rakutest
  [Terminal::UI] ok 1 - rows
  [Terminal::UI] ok 2 - cols
  [Terminal::UI] 1..2
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/03-pane.rakutest
  [Terminal::UI] ok 1 - bottom
  [Terminal::UI] ok 2 - right
  [Terminal::UI] ok 3 - lines
  [Terminal::UI] ok 4 - two lines
  [Terminal::UI] ok 5 - scroll up
  [Terminal::UI] ok 6 - word wrap with indent
  [Terminal::UI] ok 7 - hard wrap with indent
  [Terminal::UI] ok 8 - word wrap with hang
  [Terminal::UI] 1..8
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/04-frame.rakutest
  [Terminal::UI] ok 1 - full
  [Terminal::UI] ok 2 - render
  [Terminal::UI] 1..2
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/05-style.rakutest
  [Terminal::UI] 1..2
  [Terminal::UI] ok 1 - set a value
  [Terminal::UI] ok 2 - singleton works
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/06-ui.rakutest
  [Terminal::UI] ok 1 - height
  [Terminal::UI] ok 2 - width
  [Terminal::UI] ok 3 - top
  [Terminal::UI] ok 4 - left
  [Terminal::UI] ok 5 - render
  [Terminal::UI] 1..5
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/07-alert.rakutest
  [Terminal::UI] ok 1 - initial screen
  [Terminal::UI] not ok 2 - alert
  [Terminal::UI] # Failed test 'alert'
  [Terminal::UI] # at t/07-alert.rakutest line 45
  [Terminal::UI] # expected: '"╔══════════════════╗\n║Hello!            ║\n║w╔══════════════╗ ║\n║ ║   ¡ALERT!    ║ ║\n║ ╟──────────────╢ ║\n║ ╢      ok      ║ ║\n║ ╚══════════════╝ ║\n║                  ║\n║                  ║\n╚══════════════════╝\n"'
  [Terminal::UI] #      got: '"╔══════════════════╗\n║Hello!            ║\n║w╔══════════════╗ ║\n║ ║   ¡ALERT!    ║ ║\n║ ║              ║ ║\n║ ║      ok      ║ ║\n║ ╚══════════════╝ ║\n║                  ║\n║                  ║\n╚══════════════════╝\n"'
  [Terminal::UI] ok 3 - dismissed
  [Terminal::UI] 1..3
  [Terminal::UI] # You failed 1 test of 3
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/08-resize.rakutest
  [Terminal::UI] 1..2
  [Terminal::UI] ok 1 - initial heights
  [Terminal::UI] ok 2 - resize
  [Terminal::UI] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/97be0392703c0ef562b9092d0a52c2623157131c.tar.gz/Terminal-UI-0.1.14 t/09-print.rakutest
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
                 Service runtime: 2min 33.816s
               CPU time consumed: 2min 40.891s
                     Memory peak: 1.2G (swap: 136.1M)

  ```
  </details>
* [ ] [GIO](https://raku.land/cpan:CBWOOD/GIO) – Fail, Bisected: [6357ccf](https://github.com/rakudo/rakudo/commit/6357ccf97f2c4b1dd1067bf4f50b6cdcfdb78373)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2552231-i2538201.service; invocation ID: 8e1642f89b084b06856f4ea34867a63c
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: GIO
  ===> Found: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1> [via Zef::Repository::Ecosystems<rea>]
  [GIO] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789884747.2552232.6220.072139306217/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/GIO/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  ===> Fetching [OK]: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1> to /home/coke/sandbox/blin/data/zef-data/tmp/1789884747.2552232.6220.072139306217/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
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
                 Service runtime: 3min 40.718s
               CPU time consumed: 5min 5.888s
                     Memory peak: 4G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2551942-i2543133.service; invocation ID: e64142f7016e426f9216049fd596c1d9
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: GIO
  ===> Found: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1> [via Zef::Repository::Ecosystems<rea>]
  [GIO] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789884725.2551943.4787.604030042436/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/GIO/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  ===> Fetching [OK]: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1> to /home/coke/sandbox/blin/data/zef-data/tmp/1789884725.2551943.4787.604030042436/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  [GIO] Command: tar -t -f ./GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  [GIO] Command: tar -xvf ./GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz -C ../GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  ===> Extraction [OK]: GIO to /home/coke/sandbox/blin/data/zef-data/tmp/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz
  ===> Testing: GIO:ver<0.0.4>:auth<cpan:CBWOOD>:api<1>
  [GIO] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GIO%3Aver%3C0.0.4%3E%3Aauth%3Ccpan%3ACBWOOD%3E%3Aapi%3C1%3E.tar.gz/GIO-0.0.4 t/01-modules.t
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
                 Service runtime: 21.808s
               CPU time consumed: 28.862s
                     Memory peak: 2.3G (swap: 0B)

  ```
  </details>
* [ ] [GLib](https://raku.land/cpan:CBWOOD/GLib) – Fail, Bisected: [6357ccf](https://github.com/rakudo/rakudo/commit/6357ccf97f2c4b1dd1067bf4f50b6cdcfdb78373)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2425564-i2479018.service; invocation ID: dc2e9d8d1cf44da9a756e6cfe36e05b2
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: GLib
  ===> Found: GLib:ver<0.0.11>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [GLib] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789880853.2425567.7761.782153766373/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/GLib/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: GLib:ver<0.0.11>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789880853.2425567.7761.782153766373/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
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
      at /tmp/GwQ3TY8GrZ/sources/6CA058F1742AC15AF9A8D119F6535617F1C5EFF5 (GLib::Class::Object):103
      ------> class <HERE>GLib::Class::Object is export {
  ===> Install [OK] for GLib:ver<0.0.11>:auth<cpan:CBWOOD>
            Finished with result: success
  Main processes terminated with: code=exited, status=0/SUCCESS
                 Service runtime: 18min 41.925s
               CPU time consumed: 15min 17.525s
                     Memory peak: 2.6G (swap: 1.2G)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2418783-i2462891.service; invocation ID: 14e5caccfcf943dda44af9ca098f6094
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: GLib
  ===> Found: GLib:ver<0.0.11>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [GLib] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789880667.2418792.5922.254033745487/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/G/GLib/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: GLib:ver<0.0.11>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789880667.2418792.5922.254033745487/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [GLib] Command: tar -t -f ./GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [GLib] Command: tar -xvf ./GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz -C ../GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Extraction [OK]: GLib to /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Testing: GLib:ver<0.0.11>:auth<cpan:CBWOOD>
  [GLib] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/00-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs)
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions)
  [GLib] Can only use : as invocant marker in a signature after the first parameter
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions):133
  [GLib] ------>   method new (<HERE> :
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs):10
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00-struct-sizes.t:7
  [GLib] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/00b-class-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00b-class-struct-sizes.t
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs)
  [GLib] ===SORRY!=== Error while compiling /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions)
  [GLib] Can only use : as invocant marker in a signature after the first parameter
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Exceptions.pm6 (GLib::Raw::Exceptions):133
  [GLib] ------>   method new (<HERE> :
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/lib/GLib/Raw/Subs.pm6 (GLib::Raw::Subs):10
  [GLib] at /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11/t/00b-class-struct-sizes.t:7
  [GLib] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/GLib%3Aver%3C0.0.11%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/GLib-0.0.11 t/01-modules.t
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
                 Service runtime: 2min 58.613s
               CPU time consumed: 2min 54.322s
                     Memory peak: 2.3G (swap: 498.1M)

  ```
  </details>
* [ ] [JSON::GLib::Node](https://raku.land/cpan:CBWOOD/JSON::GLib::Node) – Fail, Bisected: [6357ccf](https://github.com/rakudo/rakudo/commit/6357ccf97f2c4b1dd1067bf4f50b6cdcfdb78373)
  <details><Summary>Old Output</summary>

  ```
  Running as unit: run-p2566891-i2636966.service; invocation ID: bc19c11a78894299a465c57617987299
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: JSON::GLib::Node
  ===> Found: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [JSON::GLib::Node] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789886618.2566892.5447.59147260517/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/J/JSON%3A%3AGLib%3A%3ANode/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789886618.2566892.5447.59147260517/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
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
                 Service runtime: 1min 44.956s
               CPU time consumed: 2min 29.042s
                     Memory peak: 3.2G (swap: 0B)

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  Running as unit: run-p2566744-i2636939.service; invocation ID: 51e08ff699ba497f8c1be1c2298c5afe
  Press ^] three times within 1s to disconnect TTY.
  ===> Searching for: JSON::GLib::Node
  ===> Found: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> [via Zef::Repository::Ecosystems<rea>]
  [JSON::GLib::Node] Command: curl --silent -L -o /home/coke/sandbox/blin/data/zef-data/tmp/1789886599.2566745.4686.421922137538/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz https://raw.githubusercontent.com/raku/REA/main/archive/J/JSON%3A%3AGLib%3A%3ANode/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Fetching [OK]: JSON::GLib::Node:ver<0.0.1>:auth<cpan:CBWOOD> to /home/coke/sandbox/blin/data/zef-data/tmp/1789886599.2566745.4686.421922137538/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [JSON::GLib::Node] Command: tar -t -f ./JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  [JSON::GLib::Node] Command: tar -xvf ./JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz -C ../JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Extraction [OK]: JSON::GLib::Node to /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz
  ===> Testing: JSON::GLib::Node:ver<0.0.1>
  [JSON::GLib::Node] Command: /tmp/whateverable/rakudo-moar/be8107f365b15e3b75859bd093302ba5a39f28ab/bin/perl6 -I /home/coke/sandbox/blin/data/zef-data/tmp/JSON%3A%3AGLib%3A%3ANode%3Aver%3C0.0.1%3E%3Aauth%3Ccpan%3ACBWOOD%3E.tar.gz/JSON-GLib-Node-0.0.1 t/01-basic.t
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
                 Service runtime: 19.182s
               CPU time consumed: 25.902s
                     Memory peak: 2G (swap: 0B)

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| UnhandledException        |     1 | [Foo:: Foo](https://raku.land/github:AlexDaniel/Foo:: Foo) |
| Flapper                   |     2 | [LWP::Simple](https://raku.land/zef:dwarring/LWP::Simple) [Proc::Q](https://raku.land//Proc::Q) |
| Fail                      |     7 | [CSS::Properties](https://raku.land/zef:dwarring/CSS::Properties) [GIO](https://raku.land/cpan:CBWOOD/GIO) [GLib](https://raku.land/cpan:CBWOOD/GLib) [JSON::GLib::Node](https://raku.land/cpan:CBWOOD/JSON::GLib::Node) [Polyglot::Regexen](https://raku.land/zef:guifa/Polyglot::Regexen) [Stomp](https://raku.land/zef:raku-community-modules/Stomp) [Terminal::UI](https://raku.land/zef:bduggan/Terminal::UI) |
| InstallableButUntested    |    10 | [HTTP::Server::Async](https://raku.land/zef:raku-community-modules/HTTP::Server::Async) [IO::Socket::Async::SSL](https://raku.land/zef:raku-community-modules/IO::Socket::Async::SSL) [IRC::Client](https://raku.land/zef:lizmat/IRC::Client) [Log::Minimal](https://raku.land//Log::Minimal) [Russian](https://raku.land/zef:slavenskoj/Russian) [Text::Markdown::Discount](https://raku.land/github:hartenfels/Text::Markdown::Discount) [Time::Duration](https://raku.land/zef:masukomi/Time::Duration) [Toaster](https://raku.land//Toaster) [Uzu](https://raku.land/cpan:SACOMO/Uzu) [Web::Scraper](https://raku.land/zef:tony-o/Web::Scraper) |
| MissingDependency         |    11 | [App::Ebread](https://raku.land/zef:samy/App::Ebread) [App::Perl6LangServer](https://raku.land/cpan:AZAWAWI/App::Perl6LangServer) [Chemistry::Elements](https://raku.land/github:briandfoy/Chemistry::Elements) [DBIx::NamedQueries](https://raku.land/cpan:MZIESCHA/DBIx::NamedQueries) [Ethelia](https://raku.land/zef:knarkhov/Ethelia) [Learn::Raku::With](https://raku.land/zef:codesections/Learn::Raku::With) [META6::To::Man](https://raku.land/cpan:TBROWDER/META6::To::Man) [Pakku](https://raku.land/zef:hythm/Pakku) [Perl6::Tracer](https://raku.land/github:jaffa4/Perl6::Tracer) [Task::Galaxy](https://raku.land//Task::Galaxy) [Touch](https://raku.land/zef:rir/Touch) |
| ZefFailure                |    14 | [BDD::Behave](https://raku.land/zef:gdonald/BDD::Behave) [Concurrent::BoundedChannel](https://raku.land/zef:raku-community-modules/Concurrent::BoundedChannel) [Cro::ZeroMQ](https://raku.land/cpan:JNTHN/Cro::ZeroMQ) [Gnome::Gtk4](https://raku.land/zef:martimm/Gnome::Gtk4) [ORM::ActiveRecord](https://raku.land/zef:gdonald/ORM::ActiveRecord) [ParaSeq](https://raku.land/zef:lizmat/ParaSeq) [Proc::ZMQed](https://raku.land/zef:antononcube/Proc::ZMQed) [Sitemap](https://raku.land/zef:sasha/Sitemap) [Syndicate](https://raku.land/zef:sasha/Syndicate) [TXN](https://raku.land//TXN) [TXN::Parser](https://raku.land//TXN::Parser) [TXN::Remarshal](https://raku.land//TXN::Remarshal) [Test::Time](https://raku.land/zef:FCO/Test::Time) [cro](https://raku.land/zef:cro/cro) |
| CyclicDependency          |    48 | ⋯                         |
| AlwaysFail                |   782 | ⋯                         |
| OK                        |  1656 | ⋯                         |



This run started on 2026-09-20T06:57:12Z and finished in ≈5 hours.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
