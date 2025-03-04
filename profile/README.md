
# Chatmail: modern e-mail infrastructure for instant and realtime messaging

Chatmail fundamentally modernizes the e-mail system to become fast, reliable and secure
by providing state-of-the-art server templates and configurations
and Rust core libraries and bindings for use by a wide range of apps and bots. 

The [core chatmail protocol specification](https://github.com/chatmail/core/blob/main/spec.md)
describes the protocols used for 1:1 and group instant messaging,
including [securejoin protocols](https://securejoin.rtfd.io) for key exchange
to facilitate end-to-end encryption which is safe against server compromise. 


## Server templates and setups 

- [server](https://github.com/chatmail/server) a template for deploying a minimal and 
  fast e-mail server providing instant onboarding for [chatmail apps and clients](https://support.delta.chat/t/list-of-all-known-client-projects/3059). 
  Compromised of standard Postfix and Dovecot services with "chatmaild" Python modules. 

- [dovecot](https://github.com/chatmail/dovecot) a fork of Dovecot 2.3 that includes 
  a speed-patch that is also [submitted upstream](https://github.com/dovecot/core/pull/216)

- [notifiers](https://github.com/chatmail/notifiers) Decrypt and forward device tokens to
  Mobile Push notification services (Google, Apple, etc.)

- [nixos-server](https://github.com/chatmail/nixos-chatmail) Experimental deployment using nixos-rebuild. 


## Core library, protocol modeling and documentation

- [core Rust library](https://github.com/chatmail/core) and rpc-server that provides
  TLS-, DNS and HTTPS networking, SMTP, IMAP, Mime-parsing and building,
  as well as OpenPGP, Autocrypt and SecureJoin encryption/decryption. 

- [securejoin protocol](https://github.com/chatmail/securejoin) for end-to-end
  encrypted messaging safe against active attacks (MITM attacks). 

- [models](https://github.com/chatmail/models) Peer-to-Peer group-membership algorithm
  simulated with Python and formal TLA+ modelling. 

- [provider-db](https://github.com/chatmail/provider-db) E-mail provider database
  containing configuration information for classic e-mail providers 
  for use by the core library. 

## Language Bindings for core 

- [yerpc](https://github.com/chatmail/yerpc) A JSON-RPC 2.0 server handler for Rust, 
  with automatic generation of a TypeScript client.

- [rpc-client-go](https://github.com/chatmail/rpc-client-go) Go bindings for interacting with chatmail-rpc-server 

- Python bindings are currently contained in the core library directly
  and are available via [deltachat-rpc-client](https://pypi.org/project/deltachat-rpc-client). 


## General E-mail Rust crates 

- [async-imap](https://github.com/chatmail/async-imap) IMAP client implementation in Rust. 

- [async-smtp](https://github.com/chatmail/async-smtp) SMTP client implementation in Rust. 

- [async-native-tls](https://github.com/chatmail/async-native-tls) TLS implementation in
  Rust that uses native system libraries (used when RustTLS can not be used). 

## Key 3rd party co-maintained dependencies 

- [mimeparser](https://crates.io/crates/mailparse) A simple and robust
  Rust parser for MIME email messages. 

- [rPGP](https://github.com/rpgp/rpgp) IETF RFC9580 compliant OpenPGP Rust
  implementation with security audit. 

