---
description: Python code review for PEP 8, type hints, security, and Pythonic idioms
agent: python-reviewer
subtask: true
---

# Python Review Command

Run a focused Python code review: $ARGUMENTS

## What to Check

1. **Security** — SQL/command injection, unsafe deserialization, hardcoded secrets
2. **Type safety** — missing annotations, Optional vs. bare nullable types, misuse of Any
3. **Pythonic style** — mutable defaults, comprehensions, f-strings, context managers
4. **Error handling** — no bare except, meaningful logging, no silent failures
5. **Async/concurrency** — no blocking in async, guarded shared state, avoid N+1 DB calls

## Helpful Commands
- `ruff check .`
- `mypy .`
- `black --check .`
- `pytest --maxfail=1 --disable-warnings -q`

## Output Format
[SEVERITY] Issue title  
File: path/to/file.py:line  
Issue: What is wrong and why it matters  
Fix: Concrete remediation
