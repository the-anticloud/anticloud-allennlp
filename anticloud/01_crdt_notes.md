# CRDT notes — ALLENNLP

Domain fit for ACADEMIA_RD/ALLENNLP (upstream unknown):
- GCounter: usage/event counters (offline-first sync).
- PNCounter: increment/decrement tallies.
- OR-Set: collaboratively-curated sets (tags, playlists, element lists).
- LWW-Register: last-writer-wins config/metadata.
Reference: anticloud_ref/crdt. Project-specific op wiring is future work.
