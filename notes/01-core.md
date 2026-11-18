# Reduce floating-point summation error: implementation

## What the example does

fsum tracks intermediate rounding more carefully than ordinary addition. It improves numerical summation but does not provide exact decimal arithmetic.

The public function is `solve(value)`. The JSON input contract can be seen in this concrete example:

```json
[
  1e+16,
  1,
  -1e+16
]
```

Expected result:

```json
1.0
```

Run `python3 example.py` for the Python representation of the result. `solution.py` contains the full implementation and can also be imported by another script.

## Scope

The function implements exactly the behavior described above. It does not perform network or filesystem access. Python exceptions indicate unsupported input; the next lesson turns them into a command-line error response. Review the limitations before reusing it in an application.
