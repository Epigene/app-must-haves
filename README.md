# App-Must-Haves
A curated list of structures and features every (web) app could use.

Examples given in Ruby for Rails apps.

## Data structures
### A tagging ecosystem
Do not make this fully polymorphic, instead, make per-model tag tables. Naive, but robust implementation stores a timestamp, tracking "is an object is tagged?" and "if tagged, when?".
A more complexed system could have a key-value storage, providing enum-style labeling.

## Processes
### 

## Abstraction layers
### Universal jobs
Do not keep code in /jobs. Instead, write services that are agnostic of the runtime/async split. Then, if you need to run a service asynchroniously, simply enqueue a wrapper job that will init a needed object and call a required method on it. Use argument-less methods, but provide a rich object find/init functionality.
