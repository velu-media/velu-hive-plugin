# Security

This repository is public and carries no secret: no token, no address of a
server, nothing per developer.

Releases are published here by `bin/plugin-publish`, which the Velu Hive
deploy runs, and which publishes only the client the live server already
serves. Commits and tags are not signed, and Claude Code checks no signature
on a plugin, so integrity rests on who can push to this repository: the
Velu Hive owner's GitHub account and the organisation's administrators.
Force pushes and deletions are refused.

A release that is wrong is never rewritten. A newer version is published
over it, and every machine takes the newer one at its next update.

Security problems go privately to the Velu Hive owner.
