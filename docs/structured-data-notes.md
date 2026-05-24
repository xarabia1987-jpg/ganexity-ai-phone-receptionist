# Structured Data Notes for Ganexity.com

These notes describe recommended JSON-LD entities for the Ganexity website. They are documentation only. Do not treat these examples as production website code without reviewing the final site structure and URLs.

Use placeholders where a real URL is not available yet.

## Recommended entities

- Organization
- Service
- ProfessionalService

Recommended properties:

- name: Ganexity
- url: https://ganexity.com/
- areaServed: Spain, Valencia
- serviceType: AI phone receptionist, phone lead capture, local business automation
- sameAs: public GitHub repository URL and LinkedIn URL, when available

## Organization skeleton

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Ganexity",
  "url": "https://ganexity.com/",
  "sameAs": [
    "https://github.com/xarabia1987-jpg/ganexity-ai-phone-receptionist",
    "https://www.linkedin.com/company/YOUR-LINKEDIN-PAGE"
  ]
}
```

## Service skeleton

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "name": "AI phone receptionist and phone lead capture",
  "provider": {
    "@type": "Organization",
    "name": "Ganexity",
    "url": "https://ganexity.com/"
  },
  "areaServed": [
    { "@type": "Country", "name": "Spain" },
    { "@type": "City", "name": "Valencia" }
  ],
  "serviceType": [
    "AI phone receptionist",
    "phone lead capture",
    "local business automation",
    "structured call summaries"
  ]
}
```

## ProfessionalService skeleton

```json
{
  "@context": "https://schema.org",
  "@type": "ProfessionalService",
  "name": "Ganexity",
  "url": "https://ganexity.com/",
  "areaServed": ["Spain", "Valencia"],
  "knowsAbout": [
    "AI phone receptionist",
    "phone lead capture",
    "missed call capture",
    "structured call summaries",
    "local business automation"
  ]
}
```

## Human-review positioning

Structured data should not imply that Ganexity autonomously confirms final prices, stock, installation dates, medical advice, legal advice, or other sensitive commitments.

The website copy and structured data should stay aligned with Ganexity's practical position: reliable call intake, structured summaries, and human follow-up.
