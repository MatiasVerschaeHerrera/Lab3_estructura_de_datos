# HashMap Lab (C)

## Project Overview
A C programming lab assignment to implement a HashMap (Hash Table) data structure using linear probing for collision resolution. Keys are strings (`char*`), values are generic (`void*`).

## Tech Stack
- **Language:** C
- **Compiler:** gcc
- **Debugger:** gdb
- **Testing:** `bash test.sh` (compiles `test.c` and runs tests)

## Project Structure
- `hashmap.h` — Struct definitions (`Pair`, `HashMap`) and function prototypes
- `hashmap.c` — HashMap implementation (student exercises)
- `main.c` — Example word counter app using the HashMap
- `test.c` — Automated test suite (6 exercises, 60 points total)
- `test.sh` — Shell script to compile and run tests

## Running the Project
- **Run tests:** `bash test.sh` (configured as the "Run Tests" workflow)
- **Run main app:** `gcc main.c hashmap.c -o main && ./main`

## Exercises
1. `createMap` — Allocate and initialize a HashMap
2. `insertMap` — Insert a key-value pair with linear probing
3. `searchMap` — Find a pair by key
4. `eraseMap` — Invalidate a pair (set `key=NULL`)
5. `firstMap` / `nextMap` — Iterator functions
6. `enlarge` — Double capacity and rehash all elements

## Notes
- Only `hashmap.c` and `main.c` are meant to be modified by the student
- `test.c` is reset on each test run via `git checkout`
- The array is circular (wraps around on collision probing)
- Erased pairs have `key=NULL` but are not freed (tombstone approach)
