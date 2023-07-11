
# Transactional Data Processing

Records transactions that encapsulates events that an organisation wants to track.

Transactions can be:
- Financially related
- Retail related

These systems are high in volume with quick access.

Online Transactional Procesing (OLP) units must enforce ACID semantics

- **Atomicity**
    - Each transaction is a single unit that either succeeds or fails
- **Consistency**
    - Transactions must be consistently valid and correct
- **Isolation**
    - Transactions can not interact with one another
    - Two items can not be changed at same time to ensure data consistentcy and integrity
- **Durability**
    - When a transactions has been committed, it remains committed.
    - Persistent storage of transactions

