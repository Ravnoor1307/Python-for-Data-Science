# 🧠 01_Iterators_Generators — Coupon-Reader se Lazy-Factory tak

> **Folder path:** `00_Python/03_Pythonic_Thinking/01_Iterators_Generators/`
> **Level:** 🐥→🐔 · **Type:** PRACTICAL 📝 · **Dataset:** sales_data.csv (500 orders, lazy pipelines 🌊)

---

## 📖 5-Line Summary

1. **Iterable** = shelf 📚 (list/str/dict/set/range — jis pe `iter()` chale); **Iterator** = reader 🕵️ (jis pe `next()` chale, state-yaad one-way!).
2. `for` loop internally = `iter()` + `while: next()` + `StopIteration` catch — engine khud bana ke dekh liya! 🔧
3. ⚠️ **Exhausted iterator = silent-empty plate** — 2nd `sum(stream)` gives **0**, no error (sneakiest bug!).
4. **Generators** (`yield` / genexpr `()`) = pause-resume factories — 10k squares list **85,176B** vs gen **200B** (425×! 💰).
5. 💾 Lazy pipeline = reader → filter → aggregate chains; sales ₹11,869,830 across 500 orders, sab 200-byte machines se 🎯.

## 🌍 Analogy Corner

| Concept | Real life |
|---|---|
| iterable 📚 | coupon-book gaddi (sab pages hai!) |
| iterator 🎟️ | page-tearing reader — ek baar phada, wapas nahi |
| `StopIteration` 🛑 | tapri bhaiya: "Coupon khatam bhaiya!" |
| silent-empty 🤫 | khaali plate dobara spline chaatne — nakhura nahi milega, error bhi nahi |
| generator 🏭 | demand-pe-cutting-tapri — maango, tab banao |
| `islice` 🥛 | infinite-river se chhoti glass — controlled fill |
| gen vs list 💰 | thermos (poora bhara) vs tapri (on-demand) |

## 📁 Files Is Folder Me

| File | Kya hai |
|---|---|
| `01_iterators_theory.ipynb` | Coupon-reader theory, iter/next-UA engine rebuild, dict-keys iter, SILENT-EMPTY trap live 🤫 |
| `02_generators_yield.ipynb` | yield pause/resume, genexpr-vs-comp, 10k memory WAR (425×📉), `islice` river-glass, 💾 lazy sales reader |
| `task.ipynb` | 7 tasks ⭐→🏆 — coupon drill se 💾 **Lazy Pipeline Detective** (big-orders avg ₹52,311 · 97%-in-44%-Pareto!) tak |

## 🧾 Cheat Sheet

```python
# PROTOCOL
it = iter(iterable);  x = next(it)      # StopIteration = the end 🛑
iter(obj) is obj      # False for lists/shelves, True for iterators/self-readable!
# for-UA: for x in obj: → iter(obj) + while-next + catch StopIteration → break

# GENERATORS
def my_gen(n):
    for i in range(n): yield i*i        # pause with value, resume next call!

ge = (x*x for x in nums)                # genexpr — comp का lazy twin
sum(x*x for x in nums)                  # sum() SEEDHA gen khaata — list mat banao!
from itertools import islice
ten = list(islice(infinite_gen(), 10))  # river se glass 🥛

# LAZY PIPELINE (💾 sales!):
def lazy_rows(path):
    with open(path) as f:
        yield from csv.DictReader(f)        # ek-ek row pull ✨
total = sum(int(r["quantity"])*int(r["unit_price"]) for r in lazy_rows(p))

# CHECKS
type(ge) → 'generator'  |  sys.getsizeof(gen) ≈ chhota (192–200 bytes!)
# NAYA iter() banao har pass — gen use-ek-use (regen = function call = CHEAP!)
```

## 📊 Dataset Numbers (bash-verified ✅, sales_data.csv 500 rows)

| Fact | Value |
|---|---|
| Total sales | ₹11,869,830 (avg 23,739.66 · max order ₹432,000 · min 45) |
| Regions | East 136 · North 114 · South 117 · West 133 |
| Categories | Books · Clothing · Electronics · Grocery · Toys (15 products) |
| North story | 114 orders = ₹1,580,045 |
| Big orders ≥4000 | **220 orders = ₹11,508,500** (avg 52,311.36!) |
| 🧠 Pareto moment | 44% orders → 96.97% revenue! 😱 |
| Memory | list-500 amounts 4,216B vs gen 192B |

## ⚠️ 5 Common Mistakes

| # | ❌ Galti | ✅ Sahi |
|---|---|---|
| 1 | `next([1,2])` | `next(iter([1,2]))` |
| 2 | Iterator 2nd-pass expect (silence = 0!) | Har pass naya `iter()`/fresh-gen |
| 3 | `list(infinite)` | `islice(gen, n)` |
| 4 | gen ko list me wrap karna bina need | sum/max direct stream khaate |
| 5 | Dict iter se values expect | Dict iterates KEYS; `.values()` alag |

## ⏭️ Aage Kya?

**Topic 03.02 — `Zip, Enumerate, Map, Filter, Reduce`** 🔗 — 4 lineup tools:
pairing zipper 🤐, roll-number enumerate 🎫, transform-machine map, chhalni filter,
rolling-pin reduce — 💾 students_marks ranks + products GST pipelines!
(Generators ke close-cousins — combine karke SQL-like power! 🔥)
