# TWE Architecture

## Purpose

TWE is a content, tools and resource platform built around Technology, Work and Enterprise.

It serves developers, business users and teams while creating a natural path to Imara Flow and Valron when the user's problem requires persistent business software or implementation.

## Product layers

```text
Public web
├── Articles
├── Resources
├── Technical tools
├── Business tools
├── Search
└── Conversion / handoff

Control Centre
├── CMS content
├── Tools
├── Resources
├── Jobs
├── Newsletters
├── Leads
├── Settings
└── Team access

Connected services
├── Imara Flow
├── Email delivery
├── Authentication
├── Payments
└── Valron lead handoff
```

## Separation of concerns

### TWE owns

- public discovery
- SEO pages
- articles
- resources
- technical utilities
- anonymous tool interaction
- attribution and conversion context

### Imara Flow owns

Persistent operational business records such as customers, products, invoices, sales, inventory, money records and stores.

### Valron owns

Qualified implementation, custom systems, integrations and infrastructure work when a problem exceeds the self-serve layer.

## Hosting constraint

Production must remain deployable on ordinary cPanel/shared hosting without requiring Composer or npm at deployment time.

## Data rules

- avoid parallel sources of truth
- keep production secrets outside Git
- keep runtime/generated data separate from source where practical
- prefer versioned migrations for schema changes
- preserve backwards compatibility across deployment steps
