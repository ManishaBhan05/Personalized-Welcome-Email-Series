
# Personalized Welcome Email Series
### Salesforce Marketing Cloud | AMPscript | HTML/CSS

## Project Overview

A personalized three-part welcome email series developed for **The Tavern Group**, a fictional hospitality brand managing five different pub venues.

Built using Salesforce Marketing Cloud (SFMC), AMPscript, and HTML/CSS, this project demonstrates dynamic personalization, conditional messaging, data transformation, and content retrieval from multiple Data Extensions.

## Business Scenario

The Tavern Group wants to create a personalized onboarding experience for new members who register at its venues.

The email series is designed to welcome members, introduce upcoming events, and encourage repeat visits through exclusive promotional offers.

| Email | Timing | Purpose |
|---|---|---|
| Initial Welcome Email | Day 0 | Welcome new members and introduce their venue |
| Educational Email | Day 3 | Promote upcoming events at their venue |
| Discount Offer Email | Day 7 | Encourage repeat visits with a personalized 20% offer |

## AMPscript Features Demonstrated

### 1. Personalization
- Dynamic first-name greetings
- Personalized subject lines
- Venue-specific logos and branding
- Dynamic venue details and manager information

### 2. Conditional Messaging
- Fallback greetings for missing first names
- Conditional subject lines
- Handling venue names beginning with "The"
- Error handling for missing Data Extension records

### 3. Data Transformation
- Name capitalization using `ProperCase()`
- Removing extra spaces using `Trim()`
- Date formatting using `FormatDate()`
- Calculating days remaining using `DateDiff()`
- Generating redemption codes using `Concat()`

### 4. Dynamic Content
- Venue information retrieved using `LookupRows()`
- Event details retrieved based on VenueID
- Personalized event descriptions and URLs
- Venue-specific discount redemption codes

## Data Extensions

The project uses three Data Extensions to support personalization.

### 1. Welcome_Audience

Stores member registration details.

| Field | Description |
|---|---|
| MemberID | Unique member identifier |
| FirstName | Member's first name |
| LastName | Member's last name |
| Email | Member's email address |
| SignupDate | Registration date |
| VenueID | Registered venue identifier |

### 2. Venue

Stores venue-specific information.

| Field | Description |
|---|---|
| VenueID | Unique venue identifier |
| VenueName | Name of the venue |
| VenueManager | Venue manager's name |
| LogoURL | Venue logo URL |
| Address | Venue address |
| ContactInfo | Contact number |
| FacebookLink | Social media URL |
| VoucherPrefix | Venue-specific voucher prefix |

### 3. Venue_Events

Stores upcoming event information.

| Field | Description |
|---|---|
| VenueID | Associated venue identifier |
| EventName | Name of the event |
| EventDate | Scheduled event date |
| EventDescription | Event details |
| EventURL | Event information link |

## Email Implementation

### Email 1: Initial Welcome Email

**Timing:** Day 0

**Purpose:** Welcome new members and introduce their registered venue.

**Key Features:**
- Personalized greeting and subject line
- Dynamic venue branding and logo
- Venue-specific address and contact details
- Personalized manager sign-off
- Fallback logic for missing first names

### Email 2: Educational Email

**Timing:** Day 3

**Purpose:** Inform members about upcoming events at their venue.

**Key Features:**
- Personalized member greeting
- Dynamic event name and description
- Event date formatting
- Calculation of days remaining until the event
- Dynamic event URL

### Email 3: Discount Offer Email

**Timing:** Day 7

**Purpose:** Encourage repeat visits through an exclusive promotional offer.

**Key Features:**
- Personalized greeting and venue branding
- Exclusive 20% discount offer
- Unique redemption code
- Voucher code generated using VoucherPrefix and MemberID
- Call-to-action encouraging a return visit

## Preview and Testing

The emails were previewed and tested in Salesforce Marketing Cloud using sample member and venue data.

Testing focused on:
- First-name personalization and fallback handling
- Correct venue information retrieval
- Dynamic event content
- Date formatting and calculations
- Personalized redemption code generation

### Email Preview Screenshots

Add screenshots of the three personalized emails here.

## Project Files

- `01-Initial-Welcome-Email.ampscript`
- `02-Educational-Email.ampscript`
- `03-Discount-Offer-Email.ampscript`

## Tools and Technologies

- Salesforce Marketing Cloud (Email Studio)
- AMPscript
- HTML/CSS
- Data Extensions
- GitHub

## Project Note

This project was completed as part of the **AMPscript Academy Capstone 1** assignment.

The business scenario and customer data are fictional and used for educational and portfolio demonstration purposes.
