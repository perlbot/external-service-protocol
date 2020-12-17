This is a repo for developing the external service protocol, to implement things like the Discord and Matrix bridges, and eventually a different IRC protocol client

The main purposes for this are to allow for a more flexible and featureful communications protocol, allowing "server" pushed messages and for making non-IRC related features more possible.  Along with supporting features like automatic factoid namespace (and other databases) creation for different discord server/guilds.

TODO
----

Define protocol
  Define protocol state machine

Create Perl Implementation
Create Rust Implementation
Create Node Implementation

FAQ
---

Why not use Protocol Buffers?

Mostly because I'm fed up with their support in Perl, Alien::uPB doesn't work with versions above 3.6.X (todo check this number again), which means that it's getting more and more difficult to properly support the evalserver using them as I've upgraded systems.  Debian Bullseye will not have native packages for this version anymore, and Debian Buster with backports already gets in the way requiring package holds to be made.

Why MessagePack?

It's the most widely and easily supported serialization library among the languages I need to support.  I'd like to use Sereal but there's no rust implementation.

Will you use TLS?

Probably.  Not going to implement it in place right away but I'll probably require it as part of the final implementation, including required client side certificates.  I'll make some shell scripts for setting up all the bits needed for supporting that.  Main reason is so that I can easily use it to expose the bot to places that have other network restrictions without issues.

