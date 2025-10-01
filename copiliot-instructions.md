# GitHub Copilot Instructions

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

### Fixing issues

- If you're in VS Code and you're asked to fix issues, always make a branch first.
- When asked to interact with GitHub, use its CLI if needed.
- Use the existing tests wherever possible. Ask a single question first.
- Only make a new test class if absolutely necessary.

### Bootstrap and Setup
- Install Python dependencies: `pip install -r requirements.txt` -- takes 2-3 minutes on first install. NEVER CANCEL. Set timeout to 5+ minutes.
- Install GUI support: `sudo apt-get update && sudo apt-get install -y python3-tk` -- takes 3-5 minutes. NEVER CANCEL. Set timeout to 10+ minutes.
- Install testing framework: `pip install pytest` -- takes 30 seconds.
- Install Playwright browsers (optional): `playwright install` -- takes 5-15 minutes and may fail due to download issues. This is OK to skip if it fails.

## Common Tasks

### Timeout Values and Timing Expectations
- **CRITICAL**: Always set appropriate timeouts for long-running operations:
  - Dependency installation: 5+ minutes timeout, typically takes 2-3 minutes
  - System package installation: 10+ minutes timeout, typically takes 3-5 minutes
  - Test execution: 1 minute timeout, typically takes 5-10 seconds
  - Playwright installation: 20+ minutes timeout, typically takes 5-15 minutes (may fail)
- **NEVER CANCEL** any build or installation command before timeout expires