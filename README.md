# Book of Business

> **NOTE:** This repository is for the working group to use while drafting documentation and specifications before they are formally ratified.  Users outside of the working group should not begin implementing solutions based on the content in this repository as it is likely to change without notice.

This initiative gives distribution partners self-service, on-demand access to their book of business, including a complete view of active cases and case-level details, eliminating dependence on manual reports and one-off requests. Providing distribution partners with quicker independent access to this information will improve overall user experience, improve data consistency and reduce carrier case-related support call volume.

## API Specifications

The working group's draft OpenAPI specification is in the [draft-api-specs](./draft-api-specs) directory.  See [README.md](draft-api-specs/README.md) for more details.

## Business Case

**Executive Summary:**
Provide distribution partners a standardized API to retrieve active in-force case information. The primary list endpoint returns high level case identifiers and key metadata for a partner's book of business, with supporting detail endpoints (funding, values, dates, etc.) available for drill down on specific cases. This replaces the current need for manual reporting requests or repeated transactional lookups.

**Problem:**
Currently there is no reporting tier API endpoint that exposes active case details to distribution partners. The closest existing option, Policy Inquiry, is transactional and designed for single case, which forces partners into inefficient workarounds when they need book level visibility. This API closes that gap by providing a list endpoint for book of business retrieval and dedicated micro service endpoints for detail data, allowing partners to pull only the information they need, when they need it. The design supports both bulk reconciliation use cases and targeted lookups.

**Objective:** Create a reporting-tier API that gives distribution partners book-level visibility into active in-force case information and supports targeted drill-down through detail endpoints.

**Key Results:**
· Reduction in manual report requests and ad-hoc data pulls handled by operations
· Volume of partner adoption
· Reduction in Policy Inquiry calls

**Use Case 1:** Nightly book-of-business reconciliation

**Use Case 2:** On-demand case detail lookup for advisor support

**User Story 1:** As a distribution partner, I want to retrieve active in-force case information for my book of business so that I can reconcile and report without manual requests.

**User Story 2:** As an advisor support team member, I want to look up case detail data on demand so that I can respond to questions quickly and accurately.

**Journey Maps:** Map partner request, list endpoint response, detail endpoint drill-down, and operational follow-up touchpoints across distributor, carrier, and solution provider systems.

**Integration Points:** Standardized reporting-tier API; list endpoint for active in-force cases; detail microservice endpoints for funding, values, dates, and related case data; Policy Inquiry where applicable for transactional single-case lookup.

**Required Data:** Case identifiers, key case metadata, active in-force case status, funding details, values, dates, book-of-business ownership/partner relationship data, and other detail fields exposed through supporting endpoints.

## Business Owners 
- **Magnifact:** Nick Bartlett, Tyler Gutner, Krish Krishnan 
- **Proformex:** Amanda Yoho,  
- **Prudential:** Megan Cahill, Asif Dewji, Ron Jones, Robert Moarcas 
- **Nationwide:** Stephanie Sabado, John Wissenbach 

## How to engage, contribute, and give feedback
Please contact the business owners or IRI (hpikus@irionline.org) and Matt Hendrickson (mhendrickson@irionline.org) at IRI to get added to the working group discussions.

## Change subsmissions and reporting issues and bugs

Security issues and bugs should be reported directly to Hannah Pikus at hpikus@irionline.org and Matthew Hendrickson at mhendrickson@irionline.org. Issues and bugs can be reported directly within the issues tab of a repository. Change requests should follow the standards governance workflow outlined on the main page.

## Code of conduct

See the [Digital-First-Specifications](https://github.com/Insured-Retirement-Institute/Digital-First-Specifications) repository
