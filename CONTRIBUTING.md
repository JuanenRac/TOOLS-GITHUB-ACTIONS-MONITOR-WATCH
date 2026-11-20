# Contributing to TOOLS-GITHUB-ACTIONS-MONITOR-WATCH

Thank you for looking. This repository is a scaffold: it has the base of a repository and no application code, so a contribution is most useful when it says plainly what it does and what has been tried.

1. **Say what runs and what is only planned.** Something counts as working on a phone or a watch only when it has been run on one; a test that passes in the CI is described as that.
2. **Before a pull request:** `python -I tools/ci_validate.py` and the tests of the tools (`python -I -m unittest discover -s tools -p "test_*.py"`) must pass.
3. **Every text exists in eight languages** (English, Spanish, German, French, Italian, Japanese, Chinese and European Portuguese); the README files keep the same structure.
4. **Tuned values live in a configuration file**, never in the code, and no secret, push-service file or keystore is ever committed.
5. Commits are written in English, small and about one thing.
