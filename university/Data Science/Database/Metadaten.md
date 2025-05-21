---
uni-module: "KonzMod"

alias: ["Metadata"]
---

# Metadaten

Metadaten sind Daten, die Daten beschreiben. Oft enthalten sie Informationen über die Struktur einer [[Datenbank]] oder eines [[Data Warehouse]] und ihre Speicherungsstrukturen.

## Different Types

- **Business Metadata**

  - terms and definitions
  - logical data mapping
  - data ownership
  - charging policies

- **Process Execution Metadata**

  - Data acquisition schedule.
  - [[Data Cleaning]] specifications.
  - Aggregate specifications.
  - Slowly changing dimensions policies.
  - Duration of [[Extract Transform Load]], rows rejected and successfull.

- **Technical Metadata**
  - table structure and attributes
  - derived data definitions
  - results from [[Data Profiling]]
  - [[Data Lineage]] → where did this data point come from
