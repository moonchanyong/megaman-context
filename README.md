# megaman-context

Shared mode repository for `megaman`.

This repository contains reusable remote modes that can be synced into a `megaman`-enabled project.

Current example modes:

- `onboarding`
- `aidlc-workflows`
- `superpowers`

Typical usage from a project that already ran `megaman init`:

```bash
megaman sync megaman-context
megaman mode list
megaman mode apply megaman-context/onboarding
```
