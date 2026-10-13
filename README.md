# library-semantic-network
Interactive website for a Knowledge Representation and Reasoning microproject: a library management system modelled as a semantic network, with inheritance-based reasoning queries.
# Semantic Network Representation of a Library Management System

A Knowledge Representation and Reasoning (KRR) microproject at Sandip University.
The library is modelled as a semantic network, and the website lets you explore
the network and run reasoning queries on it.

**Live demo:** <add your GitHub Pages or Netlify link here>

## What it shows

- **Interactive network:** classes (Member, Book, Staff, Author, Publisher),
  subclasses (Student, Faculty, Textbook, Novel, Reference, Librarian) and
  individuals (Alice, Bob, DrRao, AIMA, Godan and more). Click a node to see
  its is-a chain and inherited properties.
- **Knowledge base:** tables of the class hierarchy, properties and relations.
- **Reasoning queries:**
  - Can a member borrow a book?
  - Is X a kind of Y?
  - What properties does X have?
  - Who borrowed what?
  - List everything under a class

## How the reasoning works

1. Start at a node.
2. Climb the is-a and instance-of links.
3. The nearest value wins, so a specific class overrides a general one.

Example: Faculty overrides Member's 14-day loan period with 30 days, and
Reference overrides Book's `borrowable = true` with `false`.

## Limitations

- Link meanings are informal, with no formal semantics.
- No general negation, quantifiers or uncertainty.
- Single inheritance only.

Future work: convert to an OWL ontology or use first-order logic.

## Run it

It is a single static file. Open `index.html` in any browser. No install needed.

## Team

- S.V. Karthik
- K. Mahesh

Guided by Ashish kasar.
