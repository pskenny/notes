---
tags:
  - Functional_Programming
  - Programming_Language/Haskell
status:
  - Fleeting
type:
  - Tag_Page
creationDate: 2025-07-16
modifiedDate: 2025-08-08
published: 2025-07-28
publicUrl: https://www.haskell.org/
access: Public
tag_page:
  - Programming_Language/Haskell
---

It's a functional, statically typed, lazy, compiled language.

<details>
<summary>Dev Quickstart</summary>

- Install development tools via [GHCup](https://www.haskell.org/ghcup/)
- `stack new haskell-test` ([Stack hello world example](https://docs.haskellstack.org/en/stable/tutorial/hello_world_example/))
- `cd haskell-test`
- `stack build`
- `stack exec haskell-test-exe`
- Cheatsheet: `curl -s cht.sh/haskell/:learn | less`

</details>

Started learning some Haskell after thinking about [Anthony Raynes](https://github.com/Raynes) (acidraynes) and looked at [My Personal Website](My Personal Website.md) again.

## Notes

Because it's lazy you can have infinite lists! Values are computed when used.

Uses prefix notation and you can use infix of you put it between two ticks.

```haskell
-- prefix
funcName par1 par2
-- infix
par1 `funcName` par2
```

### List Comprehensions

Something I've not encountered before is list comprehensions.

```haskell
ghci> [x*2 | x <- [2..5], x > 3]
[8,10]
```

Breaking the expression down:

- `x*2` is the output of the list comprehension aka what to do with the list elements after the vertical pipe operator
- `|` pipe operator, "for" (as in, "list of `x*2` for `x` in `[2..5]`) [paraphrased from official docs](https://wiki.haskell.org/Keywords#.7C)
- `x <- [2..5]` we assign a range of 2 to 5 to `x` using the bind operator (`<-`) (more in [official docs](https://wiki.haskell.org/Keywords#%3C-))
- `, x > 3` is a predicate applied for `x*2`. It is not a predicate for when binding `x` to the range, x is still `[2, 3, 4, 5]`, not `[4, 5].

The format is very much like [Set-builder notation](https://en.m.wikipedia.org/wiki/Set-builder_notation) in mathematics.

```haskell
-- add two lists together
ghci> [adjective ++ " " ++ noun | noun <- ["sham", "mentaller"], adjective <- ["sound", "sly"]]
["sound sham","sly sham","sound mentaller","sly mentaller"]
-- list comprehension as function
ghci> vowelsAreForFls str = [c | c <- str, not (c `elem` ['a', 'e', 'i', 'o', 'u'])]
ghci> vowelsAreForFls "fools"
"fls"
```

More: [List comprehension - HaskellWiki](https://wiki.haskell.org/List_comprehension)

## Links

- Try Haskell in the browser - [Haskell Playground](https://play.haskell.org/)
