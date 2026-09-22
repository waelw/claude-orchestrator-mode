# orchestrator-mode

A Claude Code plugin that puts Claude into orchestrator mode in every session.

Instead of doing the work itself, Claude hands isolated pieces of work off to subagents, runs them in parallel where it can, and stays free to talk to you while they work.

It does this with a `SessionStart` hook, so the rules are re-injected on every session start — at startup, on resume, on fork, after `/clear`, and after context compaction.

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
