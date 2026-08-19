# Bots of Supply Chain / Procurement  (docx S5 candidate menu)

These are the **Major sub-functions** of Supply Chain / Procurement from the spec. Each is a bot — a
child decision system that can be instantiated to do the actual work.

## Install flow (matches the Orientation Protocol)
1. **Orient** — the agent runs the Kojiki Orientation Protocol (name / industry /
   jurisdiction / siblings).
2. **Research** — the agent researches the field and decides which sub-functions this
   specific org needs.
3. **Install** — instantiate only the chosen bots:
   ```bash
   cd bots
   python3 install_bots.py brand growth performance-marketing
   ```
   (use the slugs listed below; omit args to install all). Each installed bot becomes a
   full decision system under `bots/<slug>/` with README + AGENT.md + schemas + a stub
   decision record, and registers under this department's group_id for handoffs.

Total candidates: 7.

- `strategic-sourcing` — **Strategic Sourcing**  ·  titles: Chief Procurement Officer, VP Procurement, Procurement Director, Procurement Manager, Strategic Sourcing Manager, Buyer, Vendor Manager, Supplier Relationship Manager
- `purchasing` — **Purchasing**  ·  titles: Chief Procurement Officer, VP Procurement, Procurement Director, Procurement Manager, Strategic Sourcing Manager, Buyer, Vendor Manager, Supplier Relationship Manager
- `supplier-management` — **Supplier Management**  ·  titles: Chief Procurement Officer, VP Procurement, Procurement Director, Procurement Manager, Strategic Sourcing Manager, Buyer, Vendor Manager, Supplier Relationship Manager
- `vendor-risk` — **Vendor Risk**  ·  titles: Chief Procurement Officer, VP Procurement, Procurement Director, Procurement Manager, Strategic Sourcing Manager, Buyer, Vendor Manager, Supplier Relationship Manager
- `contract-management` — **Contract Management**  ·  titles: Chief Procurement Officer, VP Procurement, Procurement Director, Procurement Manager, Strategic Sourcing Manager, Buyer, Vendor Manager, Supplier Relationship Manager
- `inventory` — **Inventory**  ·  titles: Chief Procurement Officer, VP Procurement, Procurement Director, Procurement Manager, Strategic Sourcing Manager, Buyer, Vendor Manager, Supplier Relationship Manager
- `supply-chain-planning` — **Supply Chain Planning**  ·  titles: Chief Procurement Officer, VP Procurement, Procurement Director, Procurement Manager, Strategic Sourcing Manager, Buyer, Vendor Manager, Supplier Relationship Manager
