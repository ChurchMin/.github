# ChurchMin

**Practical church operations software, built for the work that happens behind the scenes.**

ChurchMin is an early-stage church management and operations platform designed to help churches move away from disconnected spreadsheets, manual processes, and systems that don't quite fit how ministry actually works.

We're building ChurchMin around a simple idea:

> **Church software should make ministry operations simpler, not create more administration.**

---

## What we're building

ChurchMin is being developed as a modular platform, with each area able to work independently while still connecting naturally to the rest of the system.

### People

A central view of the people connected to your church, providing the foundation for attendance, teams, registrations, communication, groups, and more.

### Check-In

Fast, flexible Check-In for children's ministry, youth programmes, events, and other gatherings.

Designed around real-world church workflows including:

- participant rosters
- participant groups
- locations
- labels
- family and participant search
- attendance
- headcounts
- kiosk workflows
- local printing

### Calendar & Events

A simple church-wide calendar for understanding **what is happening, when, and where**.

Events remain intentionally lightweight, allowing other ChurchMin areas to connect to them without making the Event itself responsible for everything.

### Resources

Manage shared church resources such as:

- equipment
- vehicles
- technical gear
- portable resources

Resources can be booked against Events or independently.

### Teams & Clearance

Build reusable serving Teams and define:

- Team Members
- Team Leaders
- Team Roles
- role eligibility
- clearance requirements
- missing or expired clearances

Teams exist independently of individual Events or Plans.

### Plans & Scheduling

Create reusable Plan Templates and turn them into real, dated Plans.

Plans will support:

- plan items
- required Teams
- required roles
- open role slots
- assignments
- clearance-aware scheduling

### Registration & Participant Logistics

Registration shouldn't end when someone submits a form.

ChurchMin is being designed to support the operational work that follows registration, including:

- participant management
- capacity
- dorm and room allocations
- activity teams
- transport allocations
- workshops and tracks
- bulk allocation
- operational reports
- printable/offline participant lists
- optional Check-In integration

The goal is to remove the spreadsheet that often appears between **registration** and actually **running the event**.

---

## Our product philosophy

ChurchMin is being built around a few architectural principles.

**Keep domains focused.**  
Check-In manages attendance. Registration manages participants. Teams describe who can serve. Plans handle scheduling. Events describe what is happening.

**Simple things should stay simple.**  
A Baptism Interest registration shouldn't require an Event, Check-In programme, allocations, or a planning workspace.

**Complex workflows should still be possible.**  
A large camp should be able to manage registrations, participant allocations, teams, resources, plans, and Check-In without exporting everything into spreadsheets.

**Use only what you need.**  
ChurchMin modules are designed to work independently and connect when useful.

**Don't hide complexity inside one giant entity.**  
We favour clear domain boundaries over turning `Event`, `Group`, or any other concept into a container for the entire application.

---

## Platform architecture

ChurchMin is being developed as a **modular monolith**, giving us strong domain boundaries without the operational complexity of unnecessary microservices.

Our core stack includes:

- **ASP.NET Core**
- **C#**
- **Entity Framework Core**
- **Angular**
- **Tailwind CSS**
- **SQL Server**
- **Docker**
- **OpenTelemetry**

Our platform work also includes:

- multi-tenancy
- role and permission-based access
- shared file storage
- subscription entitlements
- storage quotas and add-ons
- background jobs
- observability
- CI/CD
- Windows Print Connector integration

---

## Shared file storage

ChurchMin is moving toward a shared tenant-scoped file storage platform.

Files are physically stored once, while each product area controls how those files may be used.

Examples include:

- church branding
- Check-In label assets
- Event images
- Plan attachments
- song audio
- chord charts
- Registration attachments
- future document storage

Storage allowance will be tied to subscription entitlements, with additional storage available separately.

---

## Printing

ChurchMin includes support for local label printing through a Windows Print Connector.

The long-term goal is simple:

1. Install the ChurchMin Print Connector.
2. Enrol it with the church.
3. Discover and configure printers.
4. Print labels securely from ChurchMin.
5. Keep the Connector automatically updated.

Printing should work without requiring churches to expose local printers directly to the internet.

---

## Current direction

Our development roadmap is intentionally staged:

```text
Part 1 — Check-In

Part 2 — Calendar & Events + Resources

Part 3 — Teams + Clearance

Part 4 — Plans + Scheduling

Part 5 — Registration + Participant Logistics
```

Alongside these product areas, we're building the platform capabilities needed to run ChurchMin reliably as a hosted SaaS application.

---

## Infrastructure

ChurchMin is being designed for cloud deployment with:

- containerised application workloads
- managed or dedicated SQL Server infrastructure
- object storage
- transactional email
- container image hosting
- automated builds and deployments
- monitoring and alerting
- automated backups
- secure secret management

Our goal is to keep the early infrastructure lean while maintaining a clear path for growth.

---

## Why ChurchMin?

Church operations are often held together by a combination of:

- spreadsheets
- WhatsApp
- shared documents
- disconnected registration forms
- paper lists
- separate planning tools
- manual Check-In processes

ChurchMin aims to connect that operational work without forcing churches into unnecessarily complicated workflows.

> **One platform for the operational side of church life — without the spreadsheet scramble.**

---

## Project status

ChurchMin is under active development and the architecture is evolving as we validate real church workflows.

Some areas described here represent the current product while others form part of the planned roadmap.

We're deliberately building the foundations first so that future features sit on clean, maintainable domain boundaries.

---

## Technology with purpose

ChurchMin isn't about adding software for the sake of software.

The goal is to give church teams better tools so they can spend less time managing administration and more time focused on people.

**ChurchMin — practical software for practical ministry.**
