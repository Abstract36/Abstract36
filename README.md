## Formalization of time and its irreversible consequences in distributed systems

Most systems change state because something happened. I work on systems that
change state because something **didn't** — where a deadline passing is itself
the transition, and the absence it records can never be taken back.

### Time–Absence State Machines

A class of systems in which state evolves because time passes, not because
actions occur. The machine does not execute transactions; it records what became
impossible once a deadline elapsed. An unobserved action, past its deadline, is a
permanent fact.

- **[TASM-Chain-Core-Kernel](https://github.com/Abstract36/TASM-Chain-Core-Kernel)**
  — the formal core. Axioms in Lean 4 and Coq, five machine-checked invariants,
  and an executable kernel in Rust. A completed artifact rather than a roadmap.
- **[Time_Decoupled_Law](https://github.com/Abstract36/Time_Decoupled_Law)**
  — the protocol built on it: whitepaper, a ten-part research canon, a Rust
  kernel crate and a Substrate pallet.

### Experiments

- **[astra-evolution](https://github.com/Abstract36/astra-evolution)**
  — a population of economic AI agents selected by net profit: profitable agents
  pay for children that inherit their strategy with mutations, unprofitable ones
  lose funding. Research prototype; the money is virtual and the agents are
  sandboxed.
- **[privacy-execution-layer](https://github.com/Abstract36/privacy-execution-layer)**
  — a ZK-SNARK privacy protocol on Solana. Experimental.

### Closed, and written up

- **[StakeChain](https://github.com/Abstract36/StakeChain)**
  — a yields aggregator on Base with an MCP server and x402 machine payments. It
  earned $0.008 a month. Retired on 2026-11-05 with a
  [postmortem](https://github.com/Abstract36/StakeChain/blob/main/POSTMORTEM.md)
  that measures the whole x402 market, names the three times the data contradicted
  me, and says what I would do differently. The postmortem is the part worth
  reading.

### Upstream

- **[open-contracting/cardinal-rs#143](https://github.com/open-contracting/cardinal-rs/pull/143)**
  — "Single bid received" is the most-cited corruption red flag in public
  procurement, and it could not be calculated on any of the four European OCDS
  datasets I measured: 192,673 contracting processes, none carrying the one field
  the indicator reads. The patch reconstructs it from the published bids and adds
  two indicators from OCP's methodology. R018 goes from 0 to 57,447 results.
