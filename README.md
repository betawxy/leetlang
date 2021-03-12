# leetlang

A language for leetcoding

- high perf
- very rich data structures/algorithms libs
- typed with inference
- very expressive and succinct
- transpiles to c/c++
- browser native (transpile to webassembly)
- profiling support
- debugging support
- vis support

## roadmap

- [ ] define core syntax
- [ ] impl important data structures/algorithms
- [ ] syntax highlighter for markdown
- [ ] transpiler

## sample

```
int i = 1000000000000000000000000000000
float f = 1000000000000000000000000000000.123235345634567345673
str s = 'kjnsadfiuwy3498nkj3r2jku3h42kjm34I*&Y*ISUDN(&*#@Y*(N#J<MBJHKIHJ&Y&*UIOH闹事的海河等法律可视对讲卢卡斯电脑卡时间考虑到'

for ref var c of s {
  c.toUpper()  // c is a ref and will update s
}

for var i of [0..10) {
  print(i ** .5)
}

const A = [1, 3, 5]
const B = A.map(e -> e ** 2 + 1).filter(e -> e % 3 == 2).sort(e -> -e)

const ss = SortedSet([1..100])
var h = Heap(ref A) // will heapify A without coping
h.pop()
h.push(4)
h.remove(3) // heap lazy removal

p(ss) // pretty print anything
d() // debug here - will save a snapshot of stuff for later inspection. can also timetravel to here

ref int res = 0

@cache
any dfs(node) {
  if not node {
    return -1
  }
  (lh, rh) = (dfs(node.left), dfs(node.right))
  res = max(res, lh + rh + 2)
  return max(lh, rh) + 1

dfs(root)
```
