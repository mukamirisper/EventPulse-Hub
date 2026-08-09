# EventPulse-Hub
## 📸 Preview
(EventPulse Hub.png)

## 📌 Project Overview

EventPulse Hub is a centralized management system for competitions and events, built on Airtable. It consolidates event operations, organizer relationships, and promotional content into a single connected workspace — replacing scattered spreadsheets and disconnected tools with one source of truth.

The platform is designed for teams that run recurring competitions and events across many categories (sports, tech, creative, culinary, and more) and need to manage the full lifecycle: from drafting and QA review, through scheduling and going live, to archiving.

## 📌 The Problem

Organizations that manage a portfolio of competitions and events typically struggle with:

Fragmented data — event details, fees, deadlines, and organizer contacts live in separate files.
No lifecycle visibility — it's hard to know which events are in draft, under review, scheduled, live, or archived.
Disconnected promotion — blog and marketing content isn't linked to the events it promotes.
Weak organizer tracking — no clean directory of partner organizations or a live count of what each is running.

## 📌 The Solution
EventPulse Hub is structured around three interconnected tables:

### Table:
| Talent | Purpose | 
| :--- | :--- | 
| `Competitions & Events` | `The core registry of every competition/event, with status tracking, categorization, entry fees, prize pools, deadlines, and organizer links.` |
| `Organizers` | `A directory of partner organizations with contact info, website, and an automatically tracked count of active listings.` |
| `Blog & Promo Posts` |  `Content used to promote events, scheduled by publication date and linked directly to the relevant event.` |


The tables are relationally linked — each event points to its organizer, and each promo post points to the event it supports — enabling end-to-end traceability from a partner organization to an event to the content that markets it.

## 📌 Key Data Model

### Competitions & Events

Title, Category (18 options incl. Tech & Coding, Sports, Art, Music, Film, Culinary, Debate, Fashion, and more)
Status: Draft → QA Review → Scheduled → Live → Open → Archived
Entry Fee and Prize Pool (currency)
Deadline (date)
Organizer (linked to the Organizers directory)

### Organizers

Organization Name, Contact Email, Website
Active Listings (auto-computed count of linked events)

### Blog & Promo Posts

Post Title, Article Body, Publication Date
Related Event (linked to Competitions & Events)

## 📌 Results & Snapshot Metrics
The current state of the base demonstrates the platform in active use:
