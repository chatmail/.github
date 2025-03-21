
# Chatmail makes e-mail fun, secure and instant 

Chatmail aims to comprehensively modernize the e-mail system to become fast, reliable and secure. 

It involves two key complementary project areas: 

- [chatmail server](https://github.com/chatmail/server) is the main template to deploy a minimal and 
  fast e-mail server providing instant onboarding and cryptographically secured interoperability. 

- [chatmail core Rust library](https://github.com/chatmail/core) serves 
  a higher level chat messaging API and automatically manages 
  DNS, TLS, HTTPS, SMTP, IMAP, MIME, OpenPGP and [Iroh-based](https://iroh.computer)  
  Peer-to-Peer realtime messaging,
  and includes the [SecureJoin protocol](https://github.com/chatmail/securejoin) 
  for protection against active attacks (MITM attacks). 
  
Both areas have undergone several independent [security audits and analysis](https://delta.chat/en/help#security-audits) and are actively developed. 
