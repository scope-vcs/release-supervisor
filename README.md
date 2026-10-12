# Scope release supervisor

Bounded release supervision for
[scope-vcs/scope-vcs](https://github.com/scope-vcs/scope-vcs). It runs on the
operator's Surface as `scope-deployment-session.service`, starts and supervises
daily and signed Release events, and escalates through GitHub issues.

The Scope repository's `Deployment supervision event` and `Deployment watcher
heartbeat` workflows check out a pinned commit of this repository to forward
Release events (`deployment_webhook.py`) and check supervision health
(`heartbeat.py check`). Update that pin when either script changes.

See [OPERATIONS.md](OPERATIONS.md) and [heartbeat.md](heartbeat.md).

```sh
python3 -B -m unittest discover -p 'test_*.py'
```
