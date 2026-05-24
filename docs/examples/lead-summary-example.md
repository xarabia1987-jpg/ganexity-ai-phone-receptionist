# Lead Summary Examples

These examples are illustrative only. They do not describe real customers, real calls, or real businesses.

## Example 1: Autoescuela

Raw call situation: A caller in Valencia wants information about getting a driving license and asks about prices, documents, and theory class times.

AI collected information:

- customer name: Example caller
- phone number: not shown
- requested service: driving school enrollment information
- city or zone: Valencia
- urgency: medium
- preferred callback time: afternoon
- notes: caller wants information about documents, theory classes, and practical lesson availability

Structured summary:

```json
{
  "business_name": "Example autoescuela",
  "customer_name": "Example caller",
  "phone_number": "not shown",
  "requested_service": "Driving school enrollment information",
  "product_or_service_category": "Autoescuela",
  "city_or_zone": "Valencia",
  "urgency": "medium",
  "preferred_contact_method": "phone",
  "preferred_callback_time": "Afternoon",
  "notes": "Caller asked about documents, theory class times, prices, and practical lesson availability.",
  "missing_information": ["license category", "exact preferred schedule"],
  "human_follow_up_required": true,
  "recommended_next_action": "Call the customer to explain enrollment steps and available options."
}
```

Recommended next action: Human staff should call the customer and explain course options, documents, and current availability.

Human approval needed: yes. Prices, lesson availability, and enrollment commitments should be confirmed by staff.

## Example 2: Dental clinic

Raw call situation: A caller asks for a dental appointment because they have tooth pain and want the clinic to call them back.

AI collected information:

- customer name: Example caller
- phone number: not shown
- requested service: dental appointment request
- city or zone: Valencia
- urgency: high
- preferred callback time: as soon as possible
- notes: caller mentioned tooth pain and asked for human follow-up

Structured summary:

```json
{
  "business_name": "Example dental clinic",
  "customer_name": "Example caller",
  "phone_number": "not shown",
  "requested_service": "Dental appointment request",
  "product_or_service_category": "Dental clinic",
  "city_or_zone": "Valencia",
  "urgency": "high",
  "preferred_contact_method": "phone",
  "preferred_callback_time": "As soon as possible",
  "notes": "Caller mentioned tooth pain and requested a callback from the clinic.",
  "missing_information": ["existing patient status", "preferred dentist", "exact availability"],
  "human_follow_up_required": true,
  "recommended_next_action": "Reception should call the patient and handle the case according to clinic protocol."
}
```

Recommended next action: Clinic staff should call the patient and decide the appropriate next step.

Human approval needed: yes. The AI should not provide medical advice, diagnosis, emergency triage, treatment recommendations, or final appointment confirmation.

## Example 3: Car repair shop

Raw call situation: A caller says their car makes a noise when braking and wants to know if the workshop can look at it.

AI collected information:

- customer name: Example caller
- phone number: not shown
- requested service: brake noise inspection
- city or zone: not captured
- urgency: medium
- preferred callback time: morning
- notes: caller wants a workshop callback before bringing the car

Structured summary:

```json
{
  "business_name": "Example car repair shop",
  "customer_name": "Example caller",
  "phone_number": "not shown",
  "requested_service": "Brake noise inspection",
  "product_or_service_category": "Auto repair",
  "city_or_zone": null,
  "urgency": "medium",
  "preferred_contact_method": "phone",
  "preferred_callback_time": "Morning",
  "notes": "Caller reported noise when braking and wants to know next steps before visiting the workshop.",
  "missing_information": ["vehicle make and model", "city or zone", "when the issue started"],
  "human_follow_up_required": true,
  "recommended_next_action": "Workshop staff should call the customer, ask for vehicle details, and decide whether to schedule an inspection."
}
```

Recommended next action: Staff should call the customer, ask for vehicle details, and decide the next step.

Human approval needed: yes. The AI should not estimate the final repair price, confirm parts availability, or make vehicle safety decisions.
