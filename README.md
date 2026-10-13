# workflow-trans-bootstrap

A privacy-scoped, client-neutral entry point for preparing portable workflow
bundles. It does not contain a personal profile, credentials, private repository
URLs, account identifiers, or machine-specific paths.

Current release: `v0.2.0`.

## Start here

1. Read [`BOOTSTRAP.md`](BOOTSTRAP.md).
2. Copy [`environment.example.json`](environment.example.json) and describe the
   current device, account, task, budget, and requested persistence.
3. Generate and review an import plan before applying anything.
4. Verify the result in a fresh session. Keep unsupported combinations marked
   `NOT_RUN`.

The optional [`workflow-bootstrap` Skill](skills/workflow-bootstrap/SKILL.md)
encodes the same safety gates for compatible agents. Unknown or shared devices
default to sanitized, session-only behavior.

## Integrity

[`manifest.json`](manifest.json) records SHA-256 hashes for every bootstrap
payload file. Hashes prove file integrity, not publisher identity; verify the
repository owner through your normal trust channel before first use.

The deterministic `v0.2.0` release archive has SHA-256:

```text
e7f625f890297633ca20a2c115e47e3ea979a832bceeea81dbb037c75c44bb45
```

## License

MIT. See [`LICENSE`](LICENSE).
