# Royal Threads - Technical Operations Portfolio

This repository contains portfolio briefs and frontend documentation for systems engineered during my Operations Internship at Royal Threads. These projects were developed to digitize manual workflows, mitigate operational risk, and establish scalable data pipelines across our production and corporate facilities.

## Project 1: Bilingual Visitor Check-In Kiosk

A responsive frontend web interface designed for an iPad-based visitor registration kiosk deployed at the Raleigh facility. This system was developed to eliminate manual, paper-based visitor tracking, reduce front-desk administrative overhead, and improve facility security compliance.

### Live Frontend Demo
Link: https://github.io

### Project Overview and Business Value
In a high-volume manufacturing and corporate facility, manual visitor logging creates operational bottlenecks and data silos. This kiosk interface serves as the frontend for an automated check-in pipeline designed to address these challenges by:
* Optimizing Workflow: Streamlining the visitor onboarding process to save operational hours for front-desk staff.
* Mitigating Risk: Capturing structured visitor data, facilitating badge verification, and programmatically flagging credential conflicts.
* Driving Cross-Functional Communication: Serving as the user entry point for system-wide automation that alerts relevant team managers instantly upon a visitor's arrival.

### Technical Framework
* Architecture: Semantic HTML5 and CSS3, optimized for iPad viewports and touch targets.
* Localization: Bilingual design (English / Spanish) to support a diverse user and operator base.
* Deployment: Hosted via GitHub Pages.

---

## Project 2: Enterprise Production Floor Tracking System

An enterprise-grade, mobile-first barcode scanning application and data pipeline built to digitize production tracking across a 26-machine industrial embroidery facility. This system completely replaced manual, handwritten logs with a live data architecture, optimizing floor operations and providing management with real-time labor and throughput dashboards.

### Core Live Architecture
* Transactional Database: Deployed via Supabase to manage relational live order, operator, and machine state history.
* Operational Resilience: Engineered an atomic staging and publishing pipeline capable of processing and normalizing workbooks containing over 15,000 active order rows.
* Batch Optimization: Implemented recursive batch processing for database transactions to eliminate Statement Timeout errors during high-volume data updates.

### Business Impact and Operational Logic
* Workforce Optimization: Programmatically links live operator barcode data to active machinery sessions, allowing management to track unit output, stitch counts, and labor efficiency metrics in real time.
* Data Integrity and Error Mitigation: Programmatically handles physical operator edge cases by stripping control characters, correcting numeric optical character recognition (OCR) errors, and resolving legacy badge records into standard data streams.
* Data-Driven Scheduling: Consolidated fragmented floor updates into unified manager views, allowing supervisors to balance floor workloads dynamically to hitting precise shipment target dates.

### Key Technical Implementations
* Secure Access Controls: Built a fast, low-latency PIN-authentication layer optimized for rapid, secure device verification on active production tablets.
* Dynamic Data Staging: Isolated current scanner lookups from new catalog uploads, ensuring zero floor operational downtime while backend data sets are being refreshed or published.
* Localization and Onboarding: Structured fully bilingual worker guides (English and Spanish) native to the browser interface to maximize user adoption and minimize training time for operators.
