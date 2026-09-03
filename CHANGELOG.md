# Change Log

## [0.0.3] - 2026-09-03

- Fixed all Vescura commands (`addMapping` and others) throwing `command not found`: the extension only declared `onStartupFinished` as an activation event, so if that event didn't fire promptly no command was ever registered for the rest of the session. Added explicit `onCommand:*` activation events for every contributed command plus `onView:vescura.panel`, so opening the Vescura panel or invoking any command from the Command Palette reliably activates the extension on demand
- Excluded `.github/**` from the packaged `.vsix` (was being bundled in by mistake)

## [0.0.2] - 2026-09-03

- Fixed `command 'vescura.addMapping' not found` and other commands failing to register: `libsodium-wrappers` was bundled into `dist/extension.js` instead of left as an external runtime dependency, which was missing from the packaged extension and crashed activation

## [0.0.1] - 2026-03-17

- Initial release
- Push `.env` variables to GitHub Secrets and GitLab CI/CD Variables
- Pull remote variables into local `.env` files
- Per-variable CodeLens to toggle push/skip and secret/plain
- GitHub OAuth and GitLab PAT authentication
- Environment scoping for GitHub Environments and GitLab CI scopes