| [DeltaChat](https://github.com/deltachat) | [DeltaChat Bots](https://github.com/deltachat-bot) | chatmail infrastructure                                | [webxdc: Private Apps](https://github.com/webxdc) | [cosmos](https://cosmos.delta.chat) |
| ----------------------------------------- | -------------------------------------------------- | ------------------------------------------------------ | ------------------------------------------------- | ----------------------------------- |

# Chatmail: secure and fast e-mail infrastructure for all 

Chatmail aims to comprehensively modernize the e-mail system to become fast, reliable and secure. 

It involves two complementary project areas: 

- the `chatmail/server` template that automatically sets up a minimal
  e-mail server with battle-tested server components 
  that are configured to work as *Internet-Scale Message routers* 
  with *anonymous instant onboarding* and *interoperable cryptography* to secure all
  network connectivity between clients and servers;

- the `chatmail/core` library which implements the 
  [core chatmail protocol specification](https://github.com/chatmail/core/blob/main/spec.md)
  and neccessary parts of [existing IETF standards](https://github.com/chatmail/core/blob/main/standards.md) to enable a wide range of higher level chat apps and bots 
  to participate in the globally scaled federated Internet Messaging system, 
  without them having to care for low level network and encryption protocols. 

Both areas have undergone several independent [security audits](https://delta.chat/en/help#security-audits) and are actively developed. 


## Servers for interoperable cryptographically-secured Internet Message routing

- [server](https://github.com/chatmail/server) is the main template to deploy a minimal and 
  fast e-mail server providing instant onboarding and cryptographically secured interoperability. 

- [dovecot](https://github.com/chatmail/dovecot) is a fork of Dovecot 2.3 that includes 
  a speed-patch that is also [submitted upstream](https://github.com/dovecot/core/pull/216)

- [notifiers](https://github.com/chatmail/notifiers) is a minimal server 
  that decrypts and forward device tokens to
  Mobile Push notification services (Google, Apple, etc.)

- [nixos-server](https://github.com/chatmail/nixos-chatmail) 
  is an experimental deployment using nixos-rebuild. 


## Core library with end-to-end encryption protocols and simulation models

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

## Language Bindings for chatmail core Rust library 

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
  implementation with security audits. 

