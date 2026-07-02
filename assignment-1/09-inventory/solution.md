# Solution notes: Inventory

## Approach

* `summary` (Borrowing): I used an immutable slice reference `&[(String, u32)]`. It just reads the length and sums the quantities using an iterator. Because it only borrows, the original inventory isn't moved or changed.

* `restock` (Taking Ownership): The function takes the `Vec`s by value, completely consuming them. I used a `HashMap<String, u32>` to merge duplicates. Since the function owns the data, I moved the `String`s directly into the map as keys without needing to `.clone()` them.

## Edge cases handled


## Anything special

_Tricks, alternatives you considered, performance notes, etc._
