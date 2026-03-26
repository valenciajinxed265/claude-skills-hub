# security-guidance

Official Anthropic security reminder plugin for Claude Code. Automatically warns about potential security vulnerabilities when editing files.

**Source:** [anthropics/claude-code/plugins/security-guidance](https://github.com/anthropics/claude-code/tree/main/plugins/security-guidance)
**Author:** David Dworken (Anthropic)

## What it detects

| Pattern | Risk |
|---------|------|
| GitHub Actions workflow injection | Command injection via untrusted inputs |
| `child_process.exec()` | Shell command injection |
| `new Function()` | Code injection |
| `eval()` | Arbitrary code execution |
| `dangerouslySetInnerHTML` | XSS via React |
| `document.write()` | XSS attacks |
| `.innerHTML =` | XSS via DOM manipulation |
| `pickle` | Arbitrary code execution via deserialization |
| `os.system()` | Shell command injection (Python) |

## Installation

```bash
# Copy the entire plugin folder to your Claude plugins directory
cp -r security-guidance ~/.claude/plugins/security-guidance
```

Or install project-level:
```bash
cp -r security-guidance .claude/plugins/security-guidance
```

## How it works

This plugin uses a **PreToolUse hook** that runs before every `Edit`, `Write`, or `MultiEdit` operation. It scans the content being written for known dangerous patterns and warns you before the edit is applied.

Warnings are shown once per file per pattern per session — they won't spam you repeatedly.

## Configuration

Disable security reminders by setting the environment variable:
```bash
export ENABLE_SECURITY_REMINDER=0
```
