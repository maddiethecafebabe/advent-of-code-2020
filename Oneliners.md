# Because why not


## Day 1
```py
[print([b2, b3][i](re(s.argv[1]), s.argv[2] if len(s.argv) > 2 else 2020)[0]) for i in range(2) for b3 in [lambda x, w: [(a,b, c, a*b*c) for c in x for b in x for a in x if a+b+c == w]] for b2 in [lambda x, w: [(a,b, a*b) for b in x for a in x if a+b == w]] for re in (lambda f: [int(x.strip()) for x in open(f, "r").readlines()], ) for s in (__builtins__.__import__("sys"), )]
```

## Day 2
```py
[[print(f"Amount of valid passwords:\n  old policy: {sum(1 for entry in entries if old_is_valid_password(*entry))}\n  new policy: {sum(1 for entry in entries if new_is_valid_password(*entry))}") for entries in (findall(r"(\d+)-(\d+)\s(\w):\s(\w+)", open(sys.argv[1], "r").read()), )] for sys, findall, new_is_valid_password, old_is_valid_password in [(__builtins__.__import__("sys"), __builtins__.__import__("re").findall, lambda lower, upper, char, pw: sum(1 for idx in (int(lower), int(upper)) if pw[idx - 1] == char) == 1, lambda lower, upper, char, pw: int(lower) <= sum(1 for c in pw if c == char) <= int(upper))]]
```

