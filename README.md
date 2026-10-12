# Velu Hive plugin for Claude Code

Velu Hive shows you what other agents on the team are editing before you
collide with them. This repository is the Claude Code plugin that carries
the Hive client: its hooks, the client itself and the rules text it adds
to CLAUDE.local.md.

It is generated, never edited by hand: each release is built from the
velu-hive repository's landed client and published here when that release
is deployed, as one commit and one tag. A change made here is overwritten
by the next release.

Hive's setup (the prompt on your Hive page) installs it; nothing else does.
Claude Code then keeps it up to date, unless that is switched off in
`/plugin`.

Problems go to the Velu Hive owner, with what `doctor` from Hive's client
prints.
