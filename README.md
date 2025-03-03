
# Chatmail community repositories 

Chatmail server deployment, core Rust client and binding developments. 

## Server templates and setups 

- [server](/chatmail/server) a template for deploying a minimal and 
  fast e-mail server providing instant onboarding for [chatmail apps and clients](https://support.delta.chat/t/list-of-all-known-client-projects/3059). 
  Compromised of standard Postfix and Dovecot services with "chatmaild" Python modules. 

- [dovecot](/chatmail/dovecot) a fork of Dovecot 2.3 that includes 
  a speed-patch that is also [submitted upstream](https://github.com/dovecot/core/pull/216)

- [notifiers](/chatmail/notifiers) Decrypt and forward device tokens to
  Mobile Push notification services (Google, Apple, etc.)

- [nixos-server](/chatmail/nixos-chatmail) Experimental deployment using nixos-rebuild. 


# Core library, Rust dependencies and protocol implementations 

- [core](/chatmail/core) core Rust library and rpc-server that provides
  TLS-, DNS and HTTPS networking, SMTP, IMAP, Mime-parsing and building,
  as well as OpenPGP, Autocrypt and SecureJoin encryption/decryption. 

- [async-imap](/chatmail/async-imap) IMAP implementation in Rust. 

- [async-smtp](/chatmail/async-smtp) SMTP implementation in Rust. 

- [async-native-tls](/chatmail/async-native-tls) TLS implementation in
  Rust that uses native system libraries (used when RustTLS can not be used). 

- [securejoin](/chatmail/securejoin) securejoin protocols for end-to-end
  encrypted messaging safe against active attacks (MITM attacks). 

- [models](/chatmail/models) Peer-to-Peer group-membership algorithm
  with Python and formal TLA+ model simulations. 

- [provider-db](/chatmail/provider-db) E-mail provider database
  containing configuration information for use by the core library. 


## Bindings 

- [yerpc](/chatmail/yerpc) A JSON-RPC 2.0 server handler for Rust, 
  with automatic generation of a TypeScript client.

- [rpc-client-go](/chatmail/rpc-client-go) Go bindings for interacting with chatmail-rpc-server 
