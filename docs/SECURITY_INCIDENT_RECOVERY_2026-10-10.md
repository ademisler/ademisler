# Security incident recovery — 2026-10-10

- Repository: `ademisler/ademisler` (public)
- Previous GitHub ID: `1215041500`; restricted private archive: `archive-ademisler-20261010-1215041500`
- New empty, non-template repository ID: `1413138394`
- Rebuilt one-root source commit: `d60d0d4d6040140bf5297adec1a7422364a0bdb7`
- Independently verified original clean source tree: `afd2f0e91e8c16bbf10f935f31b174346541a855`; tracked files: 23

## Verified source/history reset

The contaminated Git history, old refs and objects, autorun editor tasks, fake font payloads, caches and old credential values were not imported. Pinned source archives were reviewed and rebuilt in a network-isolated environment. Git integrity and SHA-256 checks passed; the known malicious historical blob SHAs were not resolvable in the new GitHub repository. The previous repository remains private and read-only for forensic evidence.

Across all recovered repositories, 712 JavaScript/Python/Bash/JSON files and 917 TypeScript/TSX/JSX files passed static syntax checks. These are not end-to-end functional, dependency or deployment tests.

## Follow-up and boundaries

- Existing releases, PR conversations and tags remain in the private archive unless independently reviewed and reconstructed.
- GitHub Actions is disabled except explicitly reconfigured GitHub Pages publishing.
- Reauthorize only required integrations with **fresh** credentials; never copy archived secret values, Git object databases or untrusted caches.
- Verify live releases, external DNS and application tests separately. For GitHub Pages projects, verify the actual public site, HTTPS and custom DNS configuration.
- The clean source bundle, Git SHA and content digests are retained in restricted recovery storage.

This report documents the GitHub source/history reset; it does not assert production readiness or completion of external secret rotation.
