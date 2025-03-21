
# Chatmail: secure and fast e-mail infrastructure for all 

Chatmail aims to comprehensively modernize the e-mail system to become fast, reliable and secure. 

It involves two key complementary project areas: 

- [server](https://github.com/chatmail/server) is the main template to deploy a minimal and 
  fast e-mail server providing instant onboarding and cryptographically secured interoperability. 

- [core Rust library](https://github.com/chatmail/core) and rpc-server that provides
  TLS-, DNS and HTTPS networking, SMTP, IMAP, Mime-parsing and building,
  as well as OpenPGP encryption/decryption based on the [securejoin protocol](https://github.com/chatmail/securejoin) for security against active attacks (MITM attacks). 

Both areas have undergone several independent [security audits and analysis](https://delta.chat/en/help#security-audits) and are actively developed. 

We moreover maintain complementary chatmail compoments: 

- [provider-db](https://github.com/chatmail/provider-db) E-mail provider database
  containing configuration information for classic e-mail providers 
  for use by the core library. 

- [async-imap](https://github.com/chatmail/async-imap) IMAP client implementation in Rust. 

- [async-smtp](https://github.com/chatmail/async-smtp) SMTP client implementation in Rust. 

- [async-native-tls](https://github.com/chatmail/async-native-tls) TLS implementation in
  Rust that uses native system libraries (used when RustTLS can not be used). 

- [dovecot](https://github.com/chatmail/dovecot) is a fork of Dovecot 2.3 that includes 
  a speed-patch that is also [submitted upstream](https://github.com/dovecot/core/pull/216)

- [notifiers](https://github.com/chatmail/notifiers) is a minimal server 
  that decrypts and forward device tokens to
  Mobile Push notification services (Google, Apple, etc.)

- [yerpc](https://github.com/chatmail/yerpc) A JSON-RPC 2.0 server handler for Rust, 
  with automatic generation of a TypeScript client.

- Python bindings are currently contained in the core library directly
  and are available via [deltachat-rpc-client](https://pypi.org/project/deltachat-rpc-client). 

- [rpc-client-go](https://github.com/chatmail/rpc-client-go) Go bindings for interacting with chatmail-rpc-server 
