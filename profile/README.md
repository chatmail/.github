
# Chatmail: secure and instant e-mail infrastructure 

Chatmail aims to comprehensively modernize the e-mail system to become fast, reliable and secure. 

It involves two key complementary project areas: 

- [server](https://github.com/chatmail/server) is the main template to deploy a minimal and 
  fast e-mail server providing instant onboarding and cryptographically secured interoperability. 

- [core Rust library](https://github.com/chatmail/core) and rpc-server that provides
  TLS-, DNS and HTTPS networking, SMTP, IMAP, Mime-parsing and building,
  as well as OpenPGP encryption/decryption based on the [securejoin protocol](https://github.com/chatmail/securejoin) for security against active attacks (MITM attacks). 

Both areas have undergone several independent [security audits and analysis](https://delta.chat/en/help#security-audits) and are actively developed. 

