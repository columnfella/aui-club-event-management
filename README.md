# AUI Club, Event & Facility Management System

A PostgreSQL database for managing student clubs, events and campus facilities at Al Akhawayn University. Built as a team project for **CSC 3326 – Database Systems**.

## Overview

The database models how students join clubs, how clubs organize events, how students register for and attend those events, and how venues and equipment are requested and approved by administrators.

### Schema (11 tables)

| Area | Tables |
|---|---|
| People | `student`, `administrator` |
| Clubs | `club`, `membership`, `officer` |
| Events | `event`, `event_club`, `registration` |
| Facilities | `venue`, `equipment`, `request` |

### Example queries

The query file answers questions such as:

- Which clubs does each student belong to, and how many members does each club have?
- Who are the officers of each club, and what are their roles?
- Which clubs organize each event, and how many students registered for it?
- For events with recorded attendance, how many registered students actually attended?
- Which students belong to more than one club?
- Which venue requests were approved, and for which events?

## Files

| File | Description |
|---|---|
| `Aui_schema_pg.sql` | Creates the tables and constraints, with starter data |
| `Aui_sample_data_pg.sql` | Loads a fuller sample dataset (clears the tables first) |
| `Aui_queries_pg.sql` | Reporting queries using joins and aggregation |
| `AUI_Club_Event_Facility_Management_Project_Description-1.pdf` | Original project brief |

## Running it

Requires PostgreSQL. Run the scripts in order:

```bash
psql -v ON_ERROR_STOP=1 -a -f Aui_schema_pg.sql      -U <user>
psql -v ON_ERROR_STOP=1 -a -f Aui_sample_data_pg.sql -U <user>
psql -v ON_ERROR_STOP=1 -a -f Aui_queries_pg.sql     -U <user>
```
