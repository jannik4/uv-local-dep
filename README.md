# Reproduction for [UV#10006](https://github.com/astral-sh/uv/issues/10006)

mylib runs without any problems:

```bash
cd mylib
uv run -- hello.py

Hello from mylib!
```

mybin depends on mylib, and fails to run:

```bash
cd mybin
uv run -- hello.py

Traceback (most recent call last):
  File "...\uv-local-dep\mybin\hello.py", line 1, in <module>
    import mylib
ModuleNotFoundError: No module named 'mylib'
```
