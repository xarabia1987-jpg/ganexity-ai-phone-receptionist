# Ganexity Architecture

Ganexity is a Spanish-first AI phone receptionist and structured phone lead-capture system for local businesses in Spain, especially Valencia.

The architecture is intentionally practical: answer calls when the business cannot, collect the right information, create a structured lead summary, and route it to human staff for follow-up.

## Workflow

Inbound call
-> AI phone receptionist
-> short Spanish conversation
-> one question at a time
-> structured lead summary
-> webhook / Make.com / backend
-> Google Sheets / CRM / email / WhatsApp notification
-> human follow-up

## Core components

The system can be understood as a set of simple layers:

- Call intake layer
- Conversation layer
- Lead extraction layer
- Summary delivery layer
- Human escalation layer
- Storage and review layer

Each layer should stay replaceable. A local business should not depend on one fragile automation path if a simpler, more stable route is available.

## Call intake layer

The call intake layer receives phone calls when the business needs backup. Common situations include:

- Staff are busy with customers in the store
- Phone lines are occupied
- Calls arrive after hours
- The business is closed for lunch
- Demand is temporarily high
- Missed calls need to be converted into follow-up opportunities

This layer may use an AI receptionist provider, phone routing, call forwarding, or another telephony setup depending on the business.

## Conversation rules

The AI receptionist should speak naturally and professionally in Spanish from Spain. The call flow should be short, calm, and easy for the caller.

Core conversation rules:

- Identify itself as an AI assistant or automated phone assistant.
- Ask one question at a time.
- Avoid long robotic explanations.
- Confirm only the information needed for lead capture.
- Ask for the caller's name and phone number when appropriate.
- Ask what product, service, or issue the caller is calling about.
- Ask for the city or zone if location matters.
- Ask about urgency without creating false expectations.
- Escalate uncertainty to human staff.

The assistant should avoid confirming final prices, stock availability, installation dates, deadlines, or appointments unless a human-approved system explicitly provides that authority.

## Lead extraction layer

The lead extraction layer converts the conversation into a structured summary. The goal is not to capture everything said. The goal is to capture the useful operational details that help a human follow up quickly.

Recommended fields include:

- Business name
- Call datetime
- Customer name
- Phone number
- Requested service
- Product or service category
- City or zone
- Urgency
- Existing customer status
- Preferred contact method
- Preferred callback time
- Notes
- Missing information
- Human follow-up requirement
- Recommended next action
- Confidence score

The structured schema is defined in [schema/lead-summary.schema.json](schema/lead-summary.schema.json).

## Summary delivery layer

After the call, Ganexity should deliver the summary to the business in a simple and reliable format.

Possible delivery destinations:

- Google Sheets
- CRM
- Email
- WhatsApp notification
- Make.com scenario
- Webhook
- Backend endpoint

The delivery method should be chosen based on operational reliability, not novelty. If Google Sheets plus an email notification is the most dependable setup for a pilot business, that is a valid first architecture.

## Human escalation layer

Ganexity is human-escalation-first. The AI receptionist should route uncertain, sensitive, or commitment-heavy requests to human staff.

Human escalation is important when:

- The caller asks for a final price
- The caller asks whether a product is in stock
- The caller asks for a confirmed installation date
- The request is urgent or sensitive
- The assistant has low confidence in the extracted information
- The caller is upset or needs a human decision
- The business rules are unclear

The safest default is to collect the lead and recommend human follow-up.

## Reliability principles

Ganexity prioritizes stable workflows over fragile automations.

Key reliability principles:

- Keep the first deployment simple.
- Capture leads before adding complex actions.
- Use human review for commitments.
- Prefer clear summaries over autonomous decisions.
- Make failure modes visible to the business.
- Avoid hidden dependencies where possible.
- Keep integrations understandable and replaceable.
- Test with real call scenarios before expanding automation.

## What should remain human-approved

The following decisions should remain human-approved unless the business has a reliable, explicit, and tested system for authorizing them:

- Final pricing
- Discounts
- Product availability
- Installation dates
- Delivery dates
- Legal, medical, financial, or sensitive decisions
- Cancellation policies
- Complex complaints
- Any commitment that affects the business calendar, inventory, or finances

## Future-ready architecture

Ganexity can evolve toward more advanced tool and agent workflows while keeping the current focus on reliable lead capture.

Future-compatible areas may include:

- API-based CRM updates
- Verified inventory or catalogue lookup
- Human-approved appointment suggestions
- MCP-compatible tools for controlled data access
- A2A-style agent handoff between specialized business workflows
- Better routing based on service category, city, urgency, or customer status

These capabilities should be added only when they improve reliability and business value. The core architecture remains simple: answer the call, collect the lead, summarize it clearly, and hand it to a human.
