# Pet Shop Database Management System

An academic database-design project (Databases course, LAU, Spring 2025)
for a fictional pet retail business, *BeirutPets*. The deliverable is a
complete relational schema and design document covering the full lifecycle
of a small pet-shop operation: customers, pets, products, and services.

## What's in the repository

- `DATABASE DESIGN FOR BEIRUTPETS PET STORE (1).pdf` — the full design
  document: business requirements, ER model, relational schema, sample
  queries and design decisions.

## What the design covers

- **Customers** — contact details and purchase history.
- **Pets** — pets owned by customers, species and identifying information,
  linked to the customer who owns them.
- **Products** — inventory of goods sold by the store, with pricing and
  stock levels.
- **Services** — bookings for services the shop provides (grooming,
  boarding, vet appointments), linked to a pet and to the staff member
  performing them.
- **Orders & sales** — line-item purchases connecting customers, products
  and quantities.
- **Staff** — employees, roles and their service assignments.

## Design decisions worth noting

- **Normalised schema** — each entity in its own table, with foreign keys
  enforcing referential integrity between customers, pets, orders and
  services.
- **Lookup tables** for controlled vocabularies (species, service types,
  order status) rather than free-text fields, to prevent inconsistent data.
- **Composite keys** on the order-line table so a single order can carry
  multiple products cleanly.
- **Separation of pet and owner** as distinct entities linked by ownership,
  so a pet can outlive a customer relationship without losing its history.

## Tech

- Relational modelling (ER diagrams, normalisation to 3NF)
- SQL DDL (schema creation, constraints, indexes)

## Context

Coursework project for the Databases course at Lebanese American University,
Spring 2025. The focus was on schema design and normalisation rather than
building an application on top of it.
