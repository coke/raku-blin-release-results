[Blin](https://github.com/Raku/Blin) results between 2026.06 ([878e8b8](https://github.com/rakudo/rakudo/commit/878e8b8d171032bf27e64ae27f98938df9e77385)) and HEAD ([8b21bfd](https://github.com/rakudo/rakudo/commit/8b21bfd10500c2f53419de91288ea8617e072d60)):

* [ ] [Cro::HTTP](https://raku.land/zef:cro/Cro::HTTP) – Fail, Bisected: [8b21bfd](https://github.com/rakudo/rakudo/commit/8b21bfd10500c2f53419de91288ea8617e072d60)
  <details><Summary>Old Output</summary>

  ```
  ===> Searching for: Cro::HTTP
  ===> Found: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0> [via Zef::Repository::Ecosystems<fez>]
  [Cro::HTTP] Command: curl --silent -L -o /blin/data/zef-data/tmp/1784338805.303668.8654.167506620559/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz https://360.zef.pm/C/RO/CRO_HTTP/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Fetching [OK]: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0> to /blin/data/zef-data/tmp/1784338805.303668.8654.167506620559/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  [Cro::HTTP] Command: tar -t -f ./3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  [Cro::HTTP] Command: tar -xvf ./3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz -C ../3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Extraction [OK]: Cro::HTTP to /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Testing: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0>
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-basic-with-session.rakutest
  [Cro::HTTP] ok 1 - Username is set after basic authentication
  [Cro::HTTP] # Subtest: 401 when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2219158738488) ... }
  [Cro::HTTP] ok 2 - 401 when wrong credentials are passed
  [Cro::HTTP] # Subtest: WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2219158738992) ... }
  [Cro::HTTP] ok 3 - WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP] # Subtest: Request without credentials returns 401
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2219158739064) ... }
  [Cro::HTTP] ok 4 - Request without credentials returns 401
  [Cro::HTTP] # Subtest: Request without credentials has WWW-Authenticate header
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2219158739136) ... }
  [Cro::HTTP] ok 5 - Request without credentials has WWW-Authenticate header
  [Cro::HTTP] 1..5
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-basic.rakutest
  [Cro::HTTP] ok 1 - Username is set after basic authentication
  [Cro::HTTP] # Subtest: 401 when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6094628766136) ... }
  [Cro::HTTP] ok 2 - 401 when wrong credentials are passed
  [Cro::HTTP] # Subtest: WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6094628766568) ... }
  [Cro::HTTP] ok 3 - WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP] # Subtest: Request without credentials returns 401
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6094628766640) ... }
  [Cro::HTTP] ok 4 - Request without credentials returns 401
  [Cro::HTTP] # Subtest: Request without credentials has WWW-Authenticate header
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|6094561521480) ... }
  [Cro::HTTP] ok 5 - Request without credentials has WWW-Authenticate header
  [Cro::HTTP] 1..5
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-webtoken-bearer.rakutest
  [Cro::HTTP] ok 1 - Username is correct
  [Cro::HTTP] ok 2 - Expired token is not passed
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-webtoken-cookie.rakutest
  [Cro::HTTP] ok 1 - Token is set to cookies
  [Cro::HTTP] ok 2 - Username is correct
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-cookie.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-cookiejar.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-log-file.rakutest
  [Cro::HTTP] ok 1 - Correct responses logged
  [Cro::HTTP] ok 2 - Error responses logged
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-middleware.rakutest
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
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|3252533243648) ... }
  [Cro::HTTP]     ok 1 - Got 403 response from middleware when no auth header
  [Cro::HTTP]     ok 2 - Got 200 normal response with an auth header
  [Cro::HTTP]     # Subtest: Got 403 response from middleware when no auth header (before-matched in router)
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|3252635689896) ... }
  [Cro::HTTP]     ok 3 - Got 403 response from middleware when no auth header (before-matched in router)
  [Cro::HTTP]     ok 4 - Got 200 normal response with an auth header (before-matched in router)
  [Cro::HTTP]     # Subtest: Got 403 response from middleware when no auth header (before-matched + include in router)
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|3252305582496) ... }
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
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|3252422108728) ... }
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
  [Cro::HTTP]   /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist/lib/Cro/HTTP/Router.rakumod (Cro::HTTP::Router), line 1335
  [Cro::HTTP] Please use raku instead.
  [Cro::HTTP] --------------------------------------------------------------------------------
  [Cro::HTTP] Please contact the author to have these occurrences of deprecated code
  [Cro::HTTP] adapted, so that this message will disappear!
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-rawbodyparserselector.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request-parser.rakutest
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
  [Cro::HTTP]   /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist/lib/Cro/HTTP/Body.rakumod (Cro::HTTP::Body), line 38
  [Cro::HTTP] Please use raku instead.
  [Cro::HTTP] --------------------------------------------------------------------------------
  [Cro::HTTP] Please contact the author to have these occurrences of deprecated code
  [Cro::HTTP] adapted, so that this message will disappear!
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request-serializer.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response-parser.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response-serializer.rakutest
  [Cro::HTTP] ok 1 - Basic 204 status response serialized correctly
  [Cro::HTTP] ok 2 - 200 response with body readily available emits Content-length
  [Cro::HTTP] ok 3 - 200 response with streaming body does chunked encoding
  [Cro::HTTP] ok 4 - Chunked encoding not messed up by empty blobs
  [Cro::HTTP] ok 5 - application/json encodes Hash as JSON
  [Cro::HTTP] ok 6 - application/json encodes Array as JSON
  [Cro::HTTP] ok 7 - application/vnd.foobar+json encodes Hash as JSON
  [Cro::HTTP] 1..7
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router-named-urls.t
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router-plugin.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router.rakutest
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
  [Cro::HTTP] ok 366 - Basic include: some parts (include)
  [Cro::HTTP] ok 367 - Basic include: after (outer)
  [Cro::HTTP] ok 368 - Basic include: empty route (include)
  [Cro::HTTP] ok 369 - include and body-parser: outer body parser visible in include
  [Cro::HTTP] ok 370 - include and body-parser: outer has outer body parser
  [Cro::HTTP] ok 371 - include and body-parser: body parser in include does not leak out
  [Cro::HTTP] ok 372 - include and body-parser: body parser in include works in include
  [Cro::HTTP] ok 373 - Basic include: route 2B
  [Cro::HTTP] ok 374 - Basic include: route 1A
  [Cro::HTTP] ok 375 - Basic include: route 2A
  [Cro::HTTP] ok 376 - Basic include: route 2B
  [Cro::HTTP] ok 377 - Basic include: route 1B
  [Cro::HTTP] ok 378 - Basic include: route 2A
  [Cro::HTTP] ok 379 - Basic include: route 1B
  [Cro::HTTP] ok 380 - Basic include: route 2B
  [Cro::HTTP] ok 381 - Basic include: route 1A
  [Cro::HTTP] ok 382 - Basic include: route 2A
  [Cro::HTTP] ok 383 - Basic include: route 1A
  [Cro::HTTP] ok 384 - Basic include: route 1B
  [Cro::HTTP] ok 385 - Basic include: route 1B
  [Cro::HTTP] ok 386 - Basic include: route 1A
  [Cro::HTTP] ok 387 - Basic include: route 2A
  [Cro::HTTP] ok 388 - Basic include: route 2B
  [Cro::HTTP] ok 389 - Basic delegation: delegated transform simple
  [Cro::HTTP] ok 390 - Basic delegation: delegated transform multi part
  [Cro::HTTP] ok 391 - Basic delegation: delegated transform first
  [Cro::HTTP] ok 392 - Basic delegation: delegated transform and second
  [Cro::HTTP] ok 393 - Delegation: / and /category
  [Cro::HTTP] ok 394 - Delegation: /item and /proxy/item
  [Cro::HTTP] ok 395 - Delegation: Home
  [Cro::HTTP] ok 396 - Delegation: Slash
  [Cro::HTTP] ok 397 - Delegation: /item/1 and /proxy/item/1
  [Cro::HTTP] ok 398 - Delegation: Path
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-session-inmemory.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-session-persistent.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame-parser.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame-serializer.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame.rakutest
  [Cro::HTTP] ok 1 - DATA frame stream identifier cannot be 0
  [Cro::HTTP] ok 2 - HEADERS frame stream identifier cannot be 0
  [Cro::HTTP] ok 3 - PRIORITY frame stream identifier cannot be 0
  [Cro::HTTP] ok 4 - Settings stream-identifier cannot be non-zero
  [Cro::HTTP] ok 5 - PUSH_PROMISE frame stream identifier cannot be 0
  [Cro::HTTP] ok 6 - Ping stream-identifier cannot be non-zero
  [Cro::HTTP] ok 7 - GOAWAY Frame stream-identifier cannot be non-zero
  [Cro::HTTP] 1..7
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-request-parser.rakutest
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
  [Cro::HTTP] ok 39 - check 1
  [Cro::HTTP] ok 40 - check 4
  [Cro::HTTP] ok 41 - check 2
  [Cro::HTTP] ok 42 - check 3
  [Cro::HTTP] ok 43 - Header1 + Header2 + Data1
  [Cro::HTTP] ok 44 - check 1
  [Cro::HTTP] ok 45 - check 2
  [Cro::HTTP] ok 46 - check 3
  [Cro::HTTP] ok 47 - check 1
  [Cro::HTTP] ok 48 - check 4
  [Cro::HTTP] ok 49 - check 2
  [Cro::HTTP] ok 50 - check 3
  [Cro::HTTP] ok 51 - check 4
  [Cro::HTTP] ok 52 - Header1 + Header2 + Data1 + Data2
  [Cro::HTTP] ok 53 - check 1
  [Cro::HTTP] ok 54 - check 2
  [Cro::HTTP] ok 55 - check 3
  [Cro::HTTP] ok 56 - check 1
  [Cro::HTTP] ok 57 - check 4
  [Cro::HTTP] ok 58 - check 2
  [Cro::HTTP] ok 59 - check 3
  [Cro::HTTP] ok 60 - Header1 + Continuation1 + Header2 + Data1
  [Cro::HTTP] # Subtest: Unfinished header cannot be interrupted
  [Cro::HTTP]     1..2
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP2::Error)
  [Cro::HTTP] ok 61 - Unfinished header cannot be interrupted
  [Cro::HTTP] 1..61
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-request-serializer.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-response-parser.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-response-serializer.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/router-auth.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/uri-http.rakutest
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

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  ===> Searching for: Cro::HTTP
  ===> Found: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0> [via Zef::Repository::Ecosystems<fez>]
  [Cro::HTTP] Command: curl --silent -L -o /blin/data/zef-data/tmp/1784338545.300498.4816.594427349516/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz https://360.zef.pm/C/RO/CRO_HTTP/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Fetching [OK]: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0> to /blin/data/zef-data/tmp/1784338545.300498.4816.594427349516/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  [Cro::HTTP] Command: tar -t -f ./3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  [Cro::HTTP] Command: tar -xvf ./3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz -C ../3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Extraction [OK]: Cro::HTTP to /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz
  ===> Testing: Cro::HTTP:ver<0.8.13>:auth<zef:cro>:api<0>
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-basic-with-session.rakutest
  [Cro::HTTP] ok 1 - Username is set after basic authentication
  [Cro::HTTP] # Subtest: 401 when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2229867911640) ... }
  [Cro::HTTP] ok 2 - 401 when wrong credentials are passed
  [Cro::HTTP] # Subtest: WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2229660838648) ... }
  [Cro::HTTP] ok 3 - WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP] # Subtest: Request without credentials returns 401
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2229660838720) ... }
  [Cro::HTTP] ok 4 - Request without credentials returns 401
  [Cro::HTTP] # Subtest: Request without credentials has WWW-Authenticate header
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2229867929600) ... }
  [Cro::HTTP] ok 5 - Request without credentials has WWW-Authenticate header
  [Cro::HTTP] 1..5
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-basic.rakutest
  [Cro::HTTP] ok 1 - Username is set after basic authentication
  [Cro::HTTP] # Subtest: 401 when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4196346676352) ... }
  [Cro::HTTP] ok 2 - 401 when wrong credentials are passed
  [Cro::HTTP] # Subtest: WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4196521616800) ... }
  [Cro::HTTP] ok 3 - WWW-Authenticate header when wrong credentials are passed
  [Cro::HTTP] # Subtest: Request without credentials returns 401
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4196521616872) ... }
  [Cro::HTTP] ok 4 - Request without credentials returns 401
  [Cro::HTTP] # Subtest: Request without credentials has WWW-Authenticate header
  [Cro::HTTP]     1..3
  [Cro::HTTP]     ok 1 - code dies
  [Cro::HTTP]     ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]     ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|4196521616944) ... }
  [Cro::HTTP] ok 5 - Request without credentials has WWW-Authenticate header
  [Cro::HTTP] 1..5
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-webtoken-bearer.rakutest
  [Cro::HTTP] ok 1 - Username is correct
  [Cro::HTTP] ok 2 - Expired token is not passed
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-auth-webtoken-cookie.rakutest
  [Cro::HTTP] ok 1 - Token is set to cookies
  [Cro::HTTP] ok 2 - Username is correct
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-cookie.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-cookiejar.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-log-file.rakutest
  [Cro::HTTP] ok 1 - Correct responses logged
  [Cro::HTTP] ok 2 - Error responses logged
  [Cro::HTTP] 1..2
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-middleware.rakutest
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
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2270640693416) ... }
  [Cro::HTTP]     ok 1 - Got 403 response from middleware when no auth header
  [Cro::HTTP]     ok 2 - Got 200 normal response with an auth header
  [Cro::HTTP]     # Subtest: Got 403 response from middleware when no auth header (before-matched in router)
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2270732145936) ... }
  [Cro::HTTP]     ok 3 - Got 403 response from middleware when no auth header (before-matched in router)
  [Cro::HTTP]     ok 4 - Got 200 normal response with an auth header (before-matched in router)
  [Cro::HTTP]     # Subtest: Got 403 response from middleware when no auth header (before-matched + include in router)
  [Cro::HTTP]         1..3
  [Cro::HTTP]         ok 1 - code dies
  [Cro::HTTP]         ok 2 - right exception type (X::Cro::HTTP::Error::Client)
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2270574776464) ... }
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
  [Cro::HTTP]         ok 3 - .response matches -> ;; $_? is raw = OUTER::<$_> {  \#`(Block|2270572068320) ... }
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
  [Cro::HTTP]   /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist/lib/Cro/HTTP/Router.rakumod (Cro::HTTP::Router), line 1335
  [Cro::HTTP] Please use raku instead.
  [Cro::HTTP] --------------------------------------------------------------------------------
  [Cro::HTTP] Please contact the author to have these occurrences of deprecated code
  [Cro::HTTP] adapted, so that this message will disappear!
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-rawbodyparserselector.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request-parser.rakutest
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
  [Cro::HTTP]   /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist/lib/Cro/HTTP/Body.rakumod (Cro::HTTP::Body), line 38
  [Cro::HTTP] Please use raku instead.
  [Cro::HTTP] --------------------------------------------------------------------------------
  [Cro::HTTP] Please contact the author to have these occurrences of deprecated code
  [Cro::HTTP] adapted, so that this message will disappear!
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request-serializer.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-request.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response-parser.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response-serializer.rakutest
  [Cro::HTTP] ok 1 - Basic 204 status response serialized correctly
  [Cro::HTTP] ok 2 - 200 response with body readily available emits Content-length
  [Cro::HTTP] ok 3 - 200 response with streaming body does chunked encoding
  [Cro::HTTP] ok 4 - Chunked encoding not messed up by empty blobs
  [Cro::HTTP] ok 5 - application/json encodes Hash as JSON
  [Cro::HTTP] ok 6 - application/json encodes Array as JSON
  [Cro::HTTP] ok 7 - application/vnd.foobar+json encodes Hash as JSON
  [Cro::HTTP] 1..7
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-response.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router-named-urls.t
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router-plugin.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-router.rakutest
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
  [Cro::HTTP] ok 366 - Basic include: some parts (include)
  [Cro::HTTP] ok 367 - Basic include: empty route (include)
  [Cro::HTTP] ok 368 - Basic include: before (outer)
  [Cro::HTTP] ok 369 - include and body-parser: body parser in include does not leak out
  [Cro::HTTP] ok 370 - include and body-parser: body parser in include works in include
  [Cro::HTTP] ok 371 - include and body-parser: outer has outer body parser
  [Cro::HTTP] ok 372 - include and body-parser: outer body parser visible in include
  [Cro::HTTP] ok 373 - Basic include: route 1B
  [Cro::HTTP] ok 374 - Basic include: route 1B
  [Cro::HTTP] ok 375 - Basic include: route 1A
  [Cro::HTTP] ok 376 - Basic include: route 2B
  [Cro::HTTP] ok 377 - Basic include: route 2A
  [Cro::HTTP] ok 378 - Basic include: route 1A
  [Cro::HTTP] ok 379 - Basic include: route 2A
  [Cro::HTTP] ok 380 - Basic include: route 1A
  [Cro::HTTP] ok 381 - Basic include: route 2B
  [Cro::HTTP] ok 382 - Basic include: route 2B
  [Cro::HTTP] ok 383 - Basic include: route 2A
  [Cro::HTTP] ok 384 - Basic include: route 1A
  [Cro::HTTP] ok 385 - Basic include: route 2B
  [Cro::HTTP] ok 386 - Basic include: route 2A
  [Cro::HTTP] ok 387 - Basic include: route 1B
  [Cro::HTTP] ok 388 - Basic include: route 1B
  [Cro::HTTP] ok 389 - Basic delegation: delegated transform simple
  [Cro::HTTP] ok 390 - Basic delegation: delegated transform multi part
  [Cro::HTTP] ok 391 - Basic delegation: delegated transform and second
  [Cro::HTTP] ok 392 - Basic delegation: delegated transform first
  [Cro::HTTP] ok 393 - Delegation: Slash
  [Cro::HTTP] ok 394 - Delegation: Home
  [Cro::HTTP] ok 395 - Delegation: / and /category
  [Cro::HTTP] ok 396 - Delegation: /item/1 and /proxy/item/1
  [Cro::HTTP] ok 397 - Delegation: /item and /proxy/item
  [Cro::HTTP] ok 398 - Delegation: Path
  [Cro::HTTP] ok 399 - Can match URL segments with encoded bits (/encoded%2Fslash)
  [Cro::HTTP] ok 400 - Can match URL segments with encoded bits (/a%2Bplus)
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-session-inmemory.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http-session-persistent.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame-parser.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame-serializer.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-frame.rakutest
  [Cro::HTTP] ok 1 - DATA frame stream identifier cannot be 0
  [Cro::HTTP] ok 2 - HEADERS frame stream identifier cannot be 0
  [Cro::HTTP] ok 3 - PRIORITY frame stream identifier cannot be 0
  [Cro::HTTP] ok 4 - Settings stream-identifier cannot be non-zero
  [Cro::HTTP] ok 5 - PUSH_PROMISE frame stream identifier cannot be 0
  [Cro::HTTP] ok 6 - Ping stream-identifier cannot be non-zero
  [Cro::HTTP] ok 7 - GOAWAY Frame stream-identifier cannot be non-zero
  [Cro::HTTP] 1..7
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-request-parser.rakutest
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
  [Cro::HTTP] ok 59 - Header1 + Continuation1 + Header2 + Data1
  [Cro::HTTP] # Subtest: Unfinished header cannot be interrupted
  [Cro::HTTP]     ok 1 - check 4
  [Cro::HTTP]     1..2
  [Cro::HTTP]     ok 2 - code dies
  [Cro::HTTP]     ok 3 - right exception type (X::Cro::HTTP2::Error)
  [Cro::HTTP] not ok 60 - Unfinished header cannot be interrupted
  [Cro::HTTP] 1..60
  [Cro::HTTP]     # You planned 2 tests, but ran 3
  [Cro::HTTP] # Failed test 'Unfinished header cannot be interrupted'
  [Cro::HTTP] # at t/http2-request-parser.rakutest line 250
  [Cro::HTTP] # You failed 1 test of 60
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-request-serializer.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-response-parser.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/http2-response-serializer.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/router-auth.rakutest
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
  [Cro::HTTP] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/3a9832b52924f07d3c66fadcd2309ab8e0cffa41.tar.gz/dist t/uri-http.rakutest
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

  ```
  </details>
* [ ] [L10N::ZH](https://raku.land/zef:l10n/L10N::ZH) – Fail, Bisected: [dbb13f4](https://github.com/rakudo/rakudo/commit/dbb13f451c5ecacf1acbe73e3b7a690abcc7b094)
  <details><Summary>Old Output</summary>

  ```
  ===> Searching for: L10N::ZH
  ===> Found: L10N::ZH:ver<0.0.3>:auth<zef:l10n> [via Zef::Repository::Ecosystems<fez>]
  [L10N::ZH] Command: curl --silent -L -o /blin/data/zef-data/tmp/1784320912.60268.4321.825481991312/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz https://360.zef.pm/L/10/L10N_ZH/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz
  ===> Fetching [OK]: L10N::ZH:ver<0.0.3>:auth<zef:l10n> to /blin/data/zef-data/tmp/1784320912.60268.4321.825481991312/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz
  [L10N::ZH] Command: tar -t -f ./241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz
  [L10N::ZH] Command: tar -xvf ./241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz -C ../241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz
  ===> Extraction [OK]: L10N::ZH to /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz
  ===> Testing: L10N::ZH:ver<0.0.3>:auth<zef:l10n>
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/01-basic.rakutest
  [L10N::ZH] ok 1 - 中文本地化测试开始
  [L10N::ZH] 1..1
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/10-block.rakutest
  [L10N::ZH] ok 1 - 如果
  [L10N::ZH] ok 2 - 如果-否则
  [L10N::ZH] ok 3 - 如果不
  [L10N::ZH] ok 4 - 若定义且真
  [L10N::ZH] ok 5 - 若未定义或假
  [L10N::ZH] ok 6 - 或用
  [L10N::ZH] ok 7 - do 若定义且真 / 或用
  [L10N::ZH] ok 8 - 针对-若是-其他情况
  [L10N::ZH] ok 9 - 对每个
  [L10N::ZH] ok 10 - 有条件循环
  [L10N::ZH] ok 11 - 直到
  [L10N::ZH] ok 12 - 循环
  [L10N::ZH] ok 13 - 重复执行-直到
  [L10N::ZH] ok 14 - 嵌套如果
  [L10N::ZH] ok 15 - 每当
  [L10N::ZH] 1..15
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/11-use-import.rakutest
  [L10N::ZH] ok 1 - 使用
  [L10N::ZH] ok 2 - 导入
  [L10N::ZH] 1..2
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/12-scope.rakutest
  [L10N::ZH] ok 1 - 局部
  [L10N::ZH] ok 2 - 公开
  [L10N::ZH] ok 3 - 持续量
  [L10N::ZH] 1..3
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/13-package.rakutest
  [L10N::ZH] ok 1 - 类
  [L10N::ZH] ok 2 - 模块
  [L10N::ZH] ok 3 - 包
  [L10N::ZH] ok 4 - 能力
  [L10N::ZH] ok 5 - 语法
  [L10N::ZH] 1..5
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/14-routine.rakutest
  [L10N::ZH] ok 1 - 过程
  [L10N::ZH] ok 2 - 方法
  [L10N::ZH] ok 3 - 非继承方法
  [L10N::ZH] ok 4 - 正则
  [L10N::ZH] ok 5 - 符号
  [L10N::ZH] ok 6 - 规则
  [L10N::ZH] 1..6
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/15-modifier.rakutest
  [L10N::ZH] ok 1 - 对每个
  [L10N::ZH] ok 2 - 针对
  [L10N::ZH] ok 3 - 如果
  [L10N::ZH] ok 4 - 如果不
  [L10N::ZH] ok 5 - 直到
  [L10N::ZH] ok 6 - 若是
  [L10N::ZH] ok 7 - 有条件循环
  [L10N::ZH] ok 8 - 若后者定义且真
  [L10N::ZH] ok 9 - 若后者未定义或假
  [L10N::ZH] 1..9
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/16-enum-subset.rakutest
  [L10N::ZH] ok 1 - 真
  [L10N::ZH] ok 2 - 假
  [L10N::ZH] ok 3 - 选项集
  [L10N::ZH] ok 4 - 子集
  [L10N::ZH] 1..4
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/17-control-flow.rakutest
  [L10N::ZH] ok 1 - 终止循环
  [L10N::ZH] ok 2 - 下一轮循环
  [L10N::ZH] ok 3 - 重新此轮循环
  [L10N::ZH] ok 4 - 返回
  [L10N::ZH] ok 5 - 试试
  [L10N::ZH] ok 6 - 捕获错误
  [L10N::ZH] 1..6
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/878e8b8d171032bf27e64ae27f98938df9e77385/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/19-logic.rakutest
  [L10N::ZH] ok 1 - 所有
  [L10N::ZH] ok 2 - 任一
  [L10N::ZH] ok 3 - 是否定义
  [L10N::ZH] ok 4 - 是否定义 Nil
  [L10N::ZH] ok 5 - 等待
  [L10N::ZH] 1..5
  ===> Testing [OK] for L10N::ZH:ver<0.0.3>:auth<zef:l10n>
  ===> Installing: L10N::ZH:ver<0.0.3>:auth<zef:l10n>
  ===> Install [OK] for L10N::ZH:ver<0.0.3>:auth<zef:l10n>

  1 bin/ script [taoyuan] installed to:
  /tmp/dd64eDGvwc/bin

  ```
  </details>
  <details>
  <summary>New Output</summary>

  ```
  ===> Searching for: L10N::ZH
  ===> Found: L10N::ZH:ver<0.0.3>:auth<zef:l10n> [via Zef::Repository::Ecosystems<fez>]
  [L10N::ZH] Command: curl --silent -L -o /blin/data/zef-data/tmp/1784320815.59131.910.7677949141613/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz https://360.zef.pm/L/10/L10N_ZH/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz
  ===> Fetching [OK]: L10N::ZH:ver<0.0.3>:auth<zef:l10n> to /blin/data/zef-data/tmp/1784320815.59131.910.7677949141613/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz
  [L10N::ZH] Command: tar -t -f ./241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz
  [L10N::ZH] Command: tar -xvf ./241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz -C ../241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz
  ===> Extraction [OK]: L10N::ZH to /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz
  ===> Testing: L10N::ZH:ver<0.0.3>:auth<zef:l10n>
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/01-basic.rakutest
  [L10N::ZH] ok 1 - 中文本地化测试开始
  [L10N::ZH] 1..1
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/10-block.rakutest
  [L10N::ZH] ok 1 - 如果
  [L10N::ZH] ok 2 - 如果-否则
  [L10N::ZH] ok 3 - 如果不
  [L10N::ZH] ok 4 - 若定义且真
  [L10N::ZH] ok 5 - 若未定义或假
  [L10N::ZH] ok 6 - 或用
  [L10N::ZH] ===SORRY!=== Error while compiling /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3/EVAL_12
  [L10N::ZH] Unexpected block in infix position (missing statement control word before the expression? Or did you forget a semi-colon?)
  [L10N::ZH] at /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3/EVAL_12:2
  [L10N::ZH] ------> 局部 $result = do 若定义且真 $value<HERE> {
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/11-use-import.rakutest
  [L10N::ZH] ok 1 - 使用
  [L10N::ZH] ok 2 - 导入
  [L10N::ZH] 1..2
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/12-scope.rakutest
  [L10N::ZH] ok 1 - 局部
  [L10N::ZH] ok 2 - 公开
  [L10N::ZH] ok 3 - 持续量
  [L10N::ZH] 1..3
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/13-package.rakutest
  [L10N::ZH] ok 1 - 类
  [L10N::ZH] ok 2 - 模块
  [L10N::ZH] ok 3 - 包
  [L10N::ZH] ok 4 - 能力
  [L10N::ZH] ok 5 - 语法
  [L10N::ZH] 1..5
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/14-routine.rakutest
  [L10N::ZH] ok 1 - 过程
  [L10N::ZH] ok 2 - 方法
  [L10N::ZH] ok 3 - 非继承方法
  [L10N::ZH] ok 4 - 正则
  [L10N::ZH] ok 5 - 符号
  [L10N::ZH] ok 6 - 规则
  [L10N::ZH] 1..6
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/15-modifier.rakutest
  [L10N::ZH] ok 1 - 对每个
  [L10N::ZH] ok 2 - 针对
  [L10N::ZH] ok 3 - 如果
  [L10N::ZH] ok 4 - 如果不
  [L10N::ZH] ok 5 - 直到
  [L10N::ZH] ok 6 - 若是
  [L10N::ZH] ok 7 - 有条件循环
  [L10N::ZH] ok 8 - 若后者定义且真
  [L10N::ZH] ok 9 - 若后者未定义或假
  [L10N::ZH] 1..9
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/16-enum-subset.rakutest
  [L10N::ZH] ok 1 - 真
  [L10N::ZH] ok 2 - 假
  [L10N::ZH] ok 3 - 选项集
  [L10N::ZH] ok 4 - 子集
  [L10N::ZH] 1..4
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/17-control-flow.rakutest
  [L10N::ZH] ok 1 - 终止循环
  [L10N::ZH] ok 2 - 下一轮循环
  [L10N::ZH] ok 3 - 重新此轮循环
  [L10N::ZH] ok 4 - 返回
  [L10N::ZH] ok 5 - 试试
  [L10N::ZH] ok 6 - 捕获错误
  [L10N::ZH] 1..6
  [L10N::ZH] Command: /tmp/whateverable/rakudo-moar/8b21bfd10500c2f53419de91288ea8617e072d60/bin/perl6 -I /blin/data/zef-data/tmp/241bb932b28aa9e7503e0892023f1d87f0b24f07.tar.gz/L10N-ZH-0.0.3 t/19-logic.rakutest
  [L10N::ZH] ok 1 - 所有
  [L10N::ZH] ok 2 - 任一
  [L10N::ZH] ok 3 - 是否定义
  [L10N::ZH] ok 4 - 是否定义 Nil
  [L10N::ZH] ok 5 - 等待
  [L10N::ZH] 1..5
  ===> Testing [FAIL]: L10N::ZH:ver<0.0.3>:auth<zef:l10n>
  [L10N::ZH] Failed to get passing tests, but continuing with --force-test
  ===> Installing: L10N::ZH:ver<0.0.3>:auth<zef:l10n>
  ===> Install [OK] for L10N::ZH:ver<0.0.3>:auth<zef:l10n>

  1 bin/ script [taoyuan] installed to:
  /blin/installed/L10N::ZH_0.0.3/bin

  ```
  </details>



| Status                    | Count |          Modules          |
| :------------------------ | :---: | :------------------------ |
| UnhandledException        |     1 | [Foo:: Foo](https://raku.land/github:AlexDaniel/Foo:: Foo) |
| Flapper                   |     1 | [Cro::FCGI](https://raku.land/zef:patrickb/Cro::FCGI) |
| Fail                      |     2 | [Cro::HTTP](https://raku.land/zef:cro/Cro::HTTP) [L10N::ZH](https://raku.land/zef:l10n/L10N::ZH) |
| InstallableButUntested    |     8 | [HTTP::Server::Async](https://raku.land/zef:raku-community-modules/HTTP::Server::Async) [IO::Socket::Async::SSL](https://raku.land/zef:raku-community-modules/IO::Socket::Async::SSL) [IRC::Client](https://raku.land/zef:lizmat/IRC::Client) [Log::Minimal](https://raku.land//Log::Minimal) [Russian](https://raku.land/zef:slavenskoj/Russian) [Time::Duration](https://raku.land/zef:masukomi/Time::Duration) [Toaster](https://raku.land//Toaster) [Uzu](https://raku.land/cpan:SACOMO/Uzu) |
| ZefFailure                |     9 | [BDD::Behave](https://raku.land/zef:gdonald/BDD::Behave) [Concurrent::BoundedChannel](https://raku.land/zef:raku-community-modules/Concurrent::BoundedChannel) [ParaSeq](https://raku.land/zef:lizmat/ParaSeq) [Proc::ZMQed](https://raku.land/zef:antononcube/Proc::ZMQed) [TXN](https://raku.land//TXN) [TXN::Parser](https://raku.land//TXN::Parser) [TXN::Remarshal](https://raku.land//TXN::Remarshal) [Web::Scraper](https://raku.land/zef:tony-o/Web::Scraper) [cro](https://raku.land/zef:cro/cro) |
| MissingDependency         |    12 | [App::Ebread](https://raku.land/zef:samy/App::Ebread) [App::Perl6LangServer](https://raku.land/cpan:AZAWAWI/App::Perl6LangServer) [Chemistry::Elements](https://raku.land/github:briandfoy/Chemistry::Elements) [DBIx::NamedQueries](https://raku.land/cpan:MZIESCHA/DBIx::NamedQueries) [Ethelia](https://raku.land/zef:knarkhov/Ethelia) [Learn::Raku::With](https://raku.land/zef:codesections/Learn::Raku::With) [META6::To::Man](https://raku.land/cpan:TBROWDER/META6::To::Man) [Pakku](https://raku.land/zef:hythm/Pakku) [Perl6::Tracer](https://raku.land/github:jaffa4/Perl6::Tracer) [Pheix](https://raku.land/zef:knarkhov/Pheix) [Task::Galaxy](https://raku.land//Task::Galaxy) [Touch](https://raku.land/zef:rir/Touch) |
| CyclicDependency          |    46 | ⋯                         |
| AlwaysFail                |   723 | ⋯                         |
| OK                        |  1680 | ⋯                         |



This run started on 2026-07-18T07:04:44Z and finished in ≈11 hours.

<!--
Graph of bisected modules and their dependencies:

⚠ Drag'n'drop the generated output/overview.png file here! ⚠
-->
