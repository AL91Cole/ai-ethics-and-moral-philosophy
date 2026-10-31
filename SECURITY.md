# Repository security and privacy

## Scope

This is a research-document repository. It has no deployed service, executable AI system, authentication boundary, or conversation store. Statements about zero trust and encryption describe proposed requirements, not implemented protections. Related software must be assessed in its own repository and deployment.

## Keep contributions free of private data

- Use synthetic examples. Do not submit real conversations, student records, personal case files, production logs, account exports, credentials, or private incident evidence.
- Keep sensitive local material outside this checkout. `.gitignore` reduces accidental additions; it is not access control and does not affect already tracked files.
- Before attaching a document or image, review visible content, hidden text, comments, revision history, metadata, and embedded attachments. The automated check does not inspect binary contents.
- Use ordinary links to external sources. Remote images, media, and scripts can contact outside services when rendered and are blocked by the repository check.

## Automated checks

After staging intended changes, run:

```sh
node --test scripts/repository-privacy.test.mjs
node scripts/repository-privacy.mjs
```

The dependency-free check scans tracked files for common credential formats, sensitive file names, and remote embedded resources. It reports file paths and rule names without printing matches. It does not detect all secrets, personal information, obfuscated content, binary contents, historical commits, or information held by GitHub and other services. Passing is not a security certification.

CI uses a read-only repository token, disables credential persistence, pins checkout to a reviewed commit, and runs no package-install scripts or external scanning service. Branch rules must separately require review and the `Repository privacy / check` status before merging; source files cannot enforce account settings. Review the rule's exact status name after its first run.

## Report privately

If GitHub private vulnerability reporting is enabled, use this repository's Security tab to report privately. If it is unavailable, open only a minimal request for a private reporting channel, without exploit details or personal information. Reports concerning another implementation belong in that repository's private reporting channel.

If a credential was committed, revoke or rotate it promptly, then assess Git history, forks, caches, releases, and downloads. Deleting the current file alone does not invalidate the credential or recover published data. Do not paste a live secret into an issue, pull request, or CI log.
