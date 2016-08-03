#LambdaConf 2015 - Dynamic vs Static Having a Discussion without Sounding Like a Lunatic

* Order of Keys in JSON Matters
* We cannot easily present everything. fe. Maps
* JSON has hidden types because you need to know how it is structured - even if it is schemaless
* Important thing is that engineer care
* The Expression problem
  - The expression problem is a new name for an old problem. The goal is to define a datatype by cases, where one can add new cases to the datatype and new functions over the datatype, without recompiling existing code, and while retaining static type safety (e.g., no casts).
* There are two types of Types: for programmers (Haskell, Ocaml) and for computer (Java, C, Go)
* Context, Requirement, Decision
  - How quickly it can be deployed
  - How expensive are failures
    - do we redeploy or do we bankrupt
* Why use types over TLA+?
  - Easier to learn Haskell than formal method
  - But TLA+ was used in Amazon in just few weeks
