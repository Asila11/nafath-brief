Version: NAFATH-V3
Track: Networking

Overview

The government’s AI chat assistant depends on six interconnected IT fields to provide reliable 
and secure services to citizens. Software engineering maintains compatibility between the mobile 
application and its APIs. Artificial intelligence helps generate answers using trusted government information. 
Mobile security protects communications between citizens’ devices and government services. Networking enables 
reliable connectivity and supports a growing number of connected devices. Cybersecurity protects the assistant 
from malicious instructions and unauthorized access. Data management ensures chat logs are handled responsibly 
and citizens’ privacy is protected. These fields must work together because a weakness in one area can affect 
the entire service. For the Networking track, IPv6 addressing is particularly important because it supports 
the growth of connected devices.


Software

Semantic Versioning uses MAJOR.MINOR.PATCH to communicate API changes. 
Increase MAJOR when a change breaks compatibility with existing clients, 
such as removing an endpoint. Increase MINOR when adding backward-compatible 
functionality, such as an optional field. Increase PATCH for backward-compatible 
bug fixes. For the government assistant, following these rules helps developers 
update services without unexpectedly breaking the mobile application.

Resource: Semantic Versioning 2.0.0 - https://semver.org/spec/v2.0.0.html


AI

Retrieval-Augmented Generation (RAG) combines a generative AI model with an information 
retrieval system. When citizens ask questions, the system retrieves relevant information 
from trusted government documents and provides it to the model as context. This can reduce 
fabricated answers and help keep responses aligned with current service information without 
retraining the model. However, inaccurate documents or poor retrieval can still produce incorrect answers.

Resource: retrieval-augmented generation - Glossary | NIST - https://csrc.nist.gov/glossary/term/retrieval_augmented_generation


Mobile

Apple’s App Transport Security (ATS) enforces secure connections through the standard URL Loading System. 
It requires HTTPS and appropriate TLS security. If an iOS app attempts to access a plain HTTP endpoint, 
ATS normally blocks the request unless a suitable exception is configured. This failure may prevent 
the assistant from retrieving answers. The government should use HTTPS endpoints and avoid weakening ATS protections.

Resource: Preventing Insecure Network Connections | Apple Developer Documentation - https://developer.apple.com/documentation/security/preventing-insecure-network-connections


Networking

IPv4 uses 32-bit addresses, whereas IPv6 uses 128-bit addresses, providing a much larger address space. 
This supports a growing number of connected devices, including mobile phones, servers, and sensors. 
For the government assistant, IPv6 readiness should be assessed across mobile connectivity, APIs, 
routing, firewalls, and monitoring. IPv6 does not automatically improve security, so networks
 must be configured and tested carefully.

Resource: RFC 8200 - Internet Protocol, Version 6 (IPv6) Specification - https://www.rfc-editor.org/rfc/rfc8200


Cybersecurity

Prompt injection occurs when malicious instructions attempt to manipulate an AI model into ignoring its intended rules. 
Direct injection comes from a user’s message, while indirect injection is embedded in external content, 
such as a retrieved webpage. Two mitigations are treating retrieved content as untrusted input and enforcing 
least-privilege access to backend systems. These controls reduce risk but cannot guarantee complete prevention.

Resource: LLM01: Prompt Injection - OWASP Gen AI Security Project - https://genai.owasp.org/llmrisk2023-24/llm01-24-prompt-injection/


Data

Anonymization removes identifying links so individuals are no longer identifiable by means reasonably likely to be used. 
Pseudonymization replaces identifiers with codes, but additional information may still allow re-identification. Effectively 
anonymized data falls outside data protection law governing personal data, while pseudonymized chat logs remain personal data. 
The government should assess re-identification risks before treating chat logs as anonymous.

Resource: Anonymisation | ICO - https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/data-sharing/anonymisation/


Misconception in My Track

Open Question