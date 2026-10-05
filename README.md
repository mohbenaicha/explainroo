# explainroo on DSH

```powershell
git clone https://github.com/vincentsch/explainroo.git "$HOME\.explainroo"
cd "$HOME\.explainroo"; npm.cmd install; node bin/explainroo.js doctor --fetch
```

Then copy `skills\explainroo` into `$HOME\.agents\skills\`, so DSH finds it
machine-wide. DSH scans only `<root>/<name>/SKILL.md`, one level deep.

Edit that SKILL.md: replace upstream's bash checks with
`node "$HOME\.explainroo\bin\explainroo.js"`, and keep its pointer to
`$HOME\.explainroo\AGENTS.md` — the steps, writing rules and Scene API live
there, not in the skill.

Use `npm.cmd`; `npm.ps1` is blocked by execution policy.