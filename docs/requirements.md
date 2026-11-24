# Pharmap — Requirements Specification

**Version:** 1.0  
**Initial market:** Mauritius  
**Long-term scope:** International

## 1. Product Overview

Pharmap is a medicine information and discovery platform designed to make structured, reliable medicine information accessible to the general public and healthcare professionals.

The platform will initially focus on Mauritius, with an architecture capable of supporting international expansion.

## 2. Target Users

### 2.1 General Public
Users seeking to:
- Identify medicines by brand or generic name.
- Understand basic medicine information.
- Identify active ingredients and strengths.
- Find country-specific registration information.
- Discover reported pharmacy availability.

### 2.2 Healthcare Professionals
Users seeking to:
- Retrieve structured medicine information.
- Compare medicine products and formulations.
- Identify active ingredients and manufacturers.
- Review regulatory and market status.
- Access information sources and verification dates.

## 3. Functional Requirements

### FR-01: Medicine Search
Users must be able to search using:
- Brand name
- Generic or non-proprietary name
- Active ingredient
- Manufacturer
- Strength
- Dosage form

### FR-02: Medicine Product Information
Users must be able to view:
- Product name
- Brand name, where applicable
- Active ingredients
- Strength and strength units
- Dosage form
- Route of administration
- Manufacturer
- Relevant product identifiers

### FR-03: Brand and Generic Relationships
The system must support relationships between branded and generic medicine products.

Products must not automatically be considered interchangeable solely because they share an active ingredient.

### FR-04: Ingredient Information
The system must maintain structured information about:
- Active ingredients
- Ingredient identifiers
- Ingredient combinations
- Relevant ingredient classifications

### FR-05: Manufacturer Information
Users must be able to identify manufacturers associated with medicine products.

### FR-06: Country-Specific Regulatory Information
The system must support:
- Country of registration
- Regulatory authority
- Registration or authorisation number
- Registration status
- Approval date, where available
- Withdrawal or suspension information, where applicable
- Source and last verification date

### FR-07: Market Status
The system must distinguish between regulatory authorisation and actual commercial marketing.

Market status should support:
- Marketed
- Discontinued
- Not marketed
- Unknown
- Unverified

### FR-08: Pharmacy Availability
The system should eventually support:
- Pharmacy identification
- Medicine product identification
- Reported stock status
- Last stock verification date
- Availability information source

Stock information must be treated as time-sensitive and must not be presented as guaranteed real-time availability unless supported by a reliable live data source.

### FR-09: Medicine Classification
The system should support relevant classification systems, such as ATC.

### FR-10: Search Filtering
Users must be able to filter by:
- Active ingredient
- Strength
- Dosage form
- Manufacturer
- Country
- Regulatory status
- Market status

## 4. Non-Functional Requirements

- Data accuracy and consistency
- Source traceability and provenance
- Relational data integrity
- Scalability across countries
- Efficient search performance
- Support for multiple regulatory systems
- Secure handling of user information
- Clear distinction between verified and unverified data

## 5. Geographic Scope

Initial market: Mauritius.

Future expansion: Other countries and their respective medicine regulatory systems.

Country-specific information must remain independently identifiable.

## 6. Medicine Scope

The platform will cover:
- Prescription medicines
- Over-the-counter medicines

Prescription classification and dispensing requirements must be represented at the appropriate country level.

## 7. Safety and Information Boundaries

Pharmap is an information and discovery platform, not a diagnostic or prescribing system.

It must not:
- Diagnose medical conditions.
- Generate personalised treatment recommendations.
- Recommend changing prescribed medication.
- Imply that medicines sharing ingredients are automatically interchangeable.
- Present outdated or unverified stock information as current.

Medicine information should be traceable to reliable sources.

## 8. Initial Development Priorities

1. Medicine and ingredient catalogue
2. Brand and product relationships
3. Manufacturer catalogue
4. Country and regulatory information
5. Search and filtering
6. Market status
7. Pharmacy availability integration

## 9. Technical Direction

- Database: PostgreSQL
- Version control: Git
- Repository hosting: GitHub
- Development environment: Visual Studio Code

Database design will follow relational modelling principles, normalisation, referential integrity and appropriate indexing.