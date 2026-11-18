# Display safely quoted arguments: implementation

## What the example does

shlex.join produces POSIX-shell quoting for a list of strings. Use subprocess argument arrays for execution and never assume this quoting works on Windows cmd.

The public function is `solve(value)`. The JSON input contract can be seen in this concrete example:

```json
[
  "echo",
  "hello world"
]
```

Expected result:

```json
"echo 'hello world'"
```

Run `python3 example.py` for the Python representation of the result. `solution.py` contains the full implementation and can also be imported by another script.

## Scope

The function implements exactly the behavior described above. It does not perform network or filesystem access. Python exceptions indicate unsupported input; the next lesson turns them into a command-line error response. Review the limitations before reusing it in an application.
