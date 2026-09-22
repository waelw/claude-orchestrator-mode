# orchestrator-mode

A Claude Code plugin that puts Claude into orchestrator mode in every session.

Instead of doing the work itself, Claude hands isolated pieces of work off to subagents, runs them in parallel where it can, and stays free to talk to you while they work.

It does this with a `SessionStart` hook that injects the orchestrator rules at startup, on resume, after `/clear`, and after a compact.

## Install

```
/plugin marketplace add waelw/claude-orchestrator-mode
/plugin install orchestrator-mode
```

## Verify

Run `/hooks` and look under `SessionStart`. You should see an entry pointing at `scripts/inject-orchestrator.sh` in this plugin.

## Uninstall

```
/plugin uninstall orchestrator-mode
```

## License

MIT
