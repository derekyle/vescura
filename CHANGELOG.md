# Change Log

## [0.0.2] - 2026-09-03

- Fixed `command 'vescura.addMapping' not found` and other commands failing to register: `libsodium-wrappers` was bundled into `dist/extension.js` instead of left as an external runtime dependency, which was missing from the packaged extension and crashed activation

## [0.0.1] - 2026-03-17

- Initial release
- Push `.env` variables to GitHub Secrets and GitLab CI/CD Variables
- Pull remote variables into local `.env` files
- Per-variable CodeLens to toggle push/skip and secret/plain
- GitHub OAuth and GitLab PAT authentication
- Environment scoping for GitHub Environments and GitLab CI scopes