# Because why not


## Day 1
```py
[print([b2, b3][i](re(s.argv[1]), s.argv[2] if len(s.argv) > 2 else 2020)[0]) for i in range(2) for b3 in [lambda x, w: [(a,b, c, a*b*c) for c in x for b in x for a in x if a+b+c == w]] for b2 in [lambda x, w: [(a,b, a*b) for b in x for a in x if a+b == w]] for re in (lambda f: [int(x.strip()) for x in open(f, "r").readlines()], ) for s in (__builtins__.__import__("sys"), )]
```

## Day 2
```py
[[print(f"Amount of valid passwords:\n  old policy: {sum(1 for entry in entries if old_is_valid_password(*entry))}\n  new policy: {sum(1 for entry in entries if new_is_valid_password(*entry))}") for entries in (findall(r"(\d+)-(\d+)\s(\w):\s(\w+)", open(sys.argv[1], "r").read()), )] for sys, findall, new_is_valid_password, old_is_valid_password in [(__builtins__.__import__("sys"), __builtins__.__import__("re").findall, lambda lower, upper, char, pw: sum(1 for idx in (int(lower), int(upper)) if pw[idx - 1] == char) == 1, lambda lower, upper, char, pw: int(lower) <= sum(1 for c in pw if c == char) <= int(upper))]]
```

## Day 3
```py
[[[print(f"Part1: {get_tree_cnt(map, 3, 1, map_get)}\nPart2: {prod(get_tree_cnt(map, *vec, map_get) for vec in ((1, 1), (3, 1), (5, 1), (7, 1), (1, 2)))}")] for map in (init_map(argv[1] if len(argv) > 1 else "input.txt"), )] for init_map, map_get, get_tree_cnt, argv, prod in [(lambda path: open(path, "r").read().strip().split("\n"), lambda map, x, y: map[y][x % len(map[0])], lambda map, x_vec, y_vec, map_get: sum(map_get(map, x, y) == "#" for x, y in zip(range(0, 99999, x_vec), range(0, len(map), y_vec))), __builtins__.__import__("sys").argv, __builtins__.__import__("math").prod)]]
```
