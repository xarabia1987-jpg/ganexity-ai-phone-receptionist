# Ganexity

Ganexity is a Spanish-first AI phone receptionist and structured phone lead-capture system for local businesses in Spain, especially Valencia.

It helps businesses capture phone leads reliably: customer name, phone number, requested service or product, city or zone, urgency, and important notes for the team.

Ganexity is focused on reliable lead summaries, human follow-up, and phone backup during busy hours rather than fragile full calendar automation.

## What Ganexity does

Ganexity provides AI phone receptionist backup for local businesses when staff are busy, phone lines are occupied, calls arrive after hours, or demand peaks during the day.

The system is designed to answer naturally in Spanish from Spain, ask one question at a time, collect the most important lead details, and deliver a structured summary to the business team.

Ganexity is useful for searches and use cases such as AI phone receptionist Spain, AI receptionist for local businesses, AI phone assistant Valencia, recepcionista telefonica con IA, recepcionista telefónica con IA, secretaria telefonica IA, secretaria telefónica IA, captacion de leads telefonicos, captación de leads telefónicos, asistente telefonico IA para empresas locales, asistente telefónico IA para empresas locales, backup telefonico para negocios, and backup telefónico para negocios.

## Who it is for

Ganexity is intended for local businesses in Spain, especially Valencia, that receive valuable phone leads but cannot always answer every call immediately.

Typical businesses include:

- Kitchen stores and bathroom showrooms
- Furniture stores
- Reform and installation companies
- Clinics and professional service businesses
- Local service companies with frequent phone enquiries
- Businesses that need missed-call, busy-line, lunch-break, or after-hours phone backup

## Core workflow

1. A customer calls the business.
2. The AI phone receptionist answers as a clearly automated assistant.
3. The assistant runs a short Spanish conversation, asking one question at a time.
4. The assistant captures the key lead details.
5. The call is converted into a structured lead summary.
6. The summary is delivered through a webhook, Make.com, backend workflow, Google Sheets, CRM, email, or WhatsApp notification.
7. Human staff review the summary and follow up with the customer.

## What the AI receptionist captures

Ganexity focuses on reliable phone intake and structured lead summaries. A typical summary captures:

- Customer name
- Phone number
- Requested service or product
- Product or service category
- City or zone
- Urgency
- Whether the caller is an existing customer
- Preferred contact method
- Preferred callback time
- Important notes or preferences
- Missing information
- Whether human follow-up is required
- Recommended next action
- Confidence score

## What the AI should not do

Ganexity is designed to avoid risky business commitments. The AI receptionist should not:

- Confirm final prices
- Promise stock availability
- Confirm installation dates
- Make final business commitments
- Replace human staff completely
- Pretend to be human
- Handle sensitive or critical decisions without human review

When the situation is uncertain, the assistant should collect the relevant information and escalate the case to human staff.

## Example structured lead summary

```json
{
  "business_name": "Example local business",
  "call_datetime": "2026-05-24T10:30:00+02:00",
  "customer_name": "Maria Garcia",
  "phone_number": "+34 600 000 000",
  "requested_service": "Kitchen renovation consultation",
  "product_or_service_category": "Kitchen reform",
  "city_or_zone": "Valencia",
  "urgency": "medium",
  "existing_customer": false,
  "preferred_contact_method": "phone",
  "preferred_callback_time": "Tomorrow morning",
  "notes": "The caller is comparing options and wants to discuss measurements and materials.",
  "missing_information": ["Exact address", "Approximate budget"],
  "human_follow_up_required": true,
  "recommended_next_action": "Call the customer to qualify the project and arrange next steps.",
  "confidence_score": 0.88
}
```

This example is illustrative. It is not a claim about a real customer.

## Use cases

Ganexity is especially relevant for:

- Busy phone lines where staff cannot answer every call
- Missed calls from potential customers
- After-hours call capture
- Lunch-break phone coverage
- Peak-demand backup for local businesses
- Spanish-first phone lead qualification
- Structured summaries for human follow-up
- Reliable call intake instead of fragile full automation

## Documentation map

This repository is an AI-readable public evidence hub for Ganexity. Key files include:

- [ARCHITECTURE.md](ARCHITECTURE.md) - practical architecture for AI phone intake and structured lead delivery
- [docs/faq.md](docs/faq.md) - FAQ for humans, search engines, and AI agents
- [docs/discovery.md](docs/discovery.md) - entity, category, location, language, and discovery reference
- [docs/keywords.md](docs/keywords.md) - grouped English and Spanish discovery keywords
- [docs/reliability-principles.md](docs/reliability-principles.md) - practical reliability and safety principles
- [docs/use-cases/README.md](docs/use-cases/README.md) - AI-readable use-case map for local business phone backup
- [schema/lead-summary.schema.json](schema/lead-summary.schema.json) - JSON schema for structured phone lead summaries
- [llms.txt](llms.txt) - compact AI-readable description of Ganexity
- [docs/github-topics.md](docs/github-topics.md) - suggested GitHub repository topics
- [docs/site-loop.md](docs/site-loop.md) - notes for linking Ganexity.com and this repository
- [docs/structured-data-notes.md](docs/structured-data-notes.md) - JSON-LD notes for the website

## Website

Main website: https://ganexity.com/
