# `verif/common/` — Testbench support code

## What lives here
Clock and reset generators, scoreboards, AXI bus-functional models, coverage helpers.

## What does *not* live here
Anything synthesisable.

## How to add something
If two testbenches need it, it belongs here. Files here are include-only (`.svh`); the unit-test
runner puts this directory on the include path, so a testbench writes `` `include "name.svh" ``.

## Contents
- `rv64_golden.svh`: reference RV64IMAC_Zicsr_Zifencei decoder (mask/match table) producing
  `decoded_op_t`, plus a generator of legal encodings. Used by `tb_s1_execute`.

## Catalogue projects that land here
shared

---
*Conventions: [`docs/guidelines/CODING_STANDARD.md`](../../docs/guidelines/CODING_STANDARD.md) ·
Definition of done: [`EXECUTION_PLAN.md`](../../EXECUTION_PLAN.md) §8*
