# Security policy

## Reporting a vulnerability

Report a vulnerability privately, through GitHub: on the repository's **Security** tab, choose
**Report a vulnerability**. Do not open a public issue or pull request for it.

Say what is affected, such as a package and its version, how to reproduce it, and what an attacker
could do with it. We will confirm we received it, keep you told as we investigate and fix it, and
publish a security advisory once a fix is released, crediting you if you would like.

## Supported versions

These packages are in early development. Fixes go into `main` and the next release of each
package; earlier releases do not receive them.

## Scope

Reports are welcome for every package in this repository: above all, a transport that takes a
request as its system's without verifying it as the system signs it.

Some behavior is by design, and is not a vulnerability:

- **The contract verifies nothing itself.** `receive` is each transport's to implement, and a
  transport is what verifies that a request is its system's.
- **What becomes of an event is the application's.** Which conversations a transport's events
  reach, and who sees them, is decided by what consumes them.

A vulnerability in Effect, an external system, its client, or another dependency belongs with that
project. Tell us too when it affects these packages in a way of its own.

## Running transports

- Keep each system's tokens and signing secrets secret: whoever holds a signing secret can send
  requests a transport takes as its system's.
