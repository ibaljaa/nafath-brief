Version: NAFATH-V3
Track: Cybersecurity

## Overview
A trustworthy government AI assistant depends on six connected IT fields. Software engineering defines a stable public API so the mobile app can communicate with government services as they evolve. Artificial intelligence uses retrieval-augmented generation (RAG) to retrieve relevant information from approved sources before generating answers. Mobile security helps protect communication between the app and its servers. Networking provides the addressing and connectivity needed for citizens to access the service across different devices and networks. Cybersecurity reduces risks such as prompt injection, unauthorized access, and exposure of sensitive information. Data management determines how chat logs are stored, protected, and retained while respecting privacy requirements. These fields must work together to keep the service reliable, accessible, and safe. My Cybersecurity track focuses on mitigating direct and indirect prompt injection in a government AI assistant.


## Software
Under Semantic Versioning, a public API must increase its MAJOR version when a change is incompatible with the previous version. A MINOR version increases when new functionality is added in a backward-compatible way. A PATCH version increases when backward-compatible bug fixes are made. For example, changing a required API field in a way that breaks older clients may require a MAJOR release, while fixing a compatible bug may require a PATCH release.
Resource: Semantic Versioning 2.0.0 - https://semver.org/spec/v2.0.0.html

## AI
Retrieval-Augmented Generation (RAG) combines information retrieval with text generation. Before answering a question, the system retrieves relevant information from an external source and provides it to the AI model as context. In a government assistant, this could mean retrieving current service requirements from approved government documents. RAG can reduce incorrect answers by grounding responses in relevant information, but it does not guarantee accuracy if the sources are outdated or the model misinterprets them.
Resource: Retrieval-Augmented Generation (RAG) - https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview

## Mobile
App Transport Security (ATS) is an Apple platform feature that enforces security requirements for network connections made by apps. It generally requires HTTPS connections that meet Apple's transport security requirements. If an iOS app tries to connect to a plain HTTP endpoint, ATS normally blocks the connection unless an applicable exception is configured. A government app should use secure HTTPS endpoints to help protect information exchanged between citizens' devices and its servers.
Resource: Preventing Insecure Network Connections - https://developer.apple.com/documentation/bundleresources/information_property_list/nsapptransportsecurity
  
## Networking
IPv4 uses 32-bit addresses, while IPv6 uses 128-bit addresses and provides a much larger address space. As more phones, sensors, and connected devices use government services, IPv6 helps support the growing number of devices that need network addresses. IPv6 also includes improvements to network configuration. Supporting IPv6 can help the service scale, although secure configuration and compatibility with existing networks are still important.
Resource: IPv6 - Internet Protocol Version 6 - https://www.rfc-editor.org/rfc/rfc8200.html
  

## Cybersecurity
Prompt injection occurs when malicious instructions try to manipulate an AI system into ignoring its intended rules. Direct prompt injection comes from a user's input, while indirect prompt injection can be hidden in external content the AI retrieves, such as a webpage or document. Two mitigations are to treat retrieved content as untrusted data and to restrict the AI's access to sensitive tools and information. These controls reduce risk but cannot eliminate it completely.
Resource: Prompt injection - https://owasp.org/www-project-top-10-for-large-language-model-applications/

## Data
Anonymization removes identifying information so that a person can no longer reasonably be identified from the data. Pseudonymization replaces direct identifiers with artificial labels, but the data may still be linked back to a person using additional information. For a government AI assistant, removing names alone may not fully anonymize chat logs. Pseudonymized data generally remains personal data under data protection law, while properly anonymized data may fall outside its scope.
Resource: What is personal data? - https://commission.europa.eu/law/law-topic/data-protection/reform/what-personal-data_en

## Misconception in My Track
A common misconception is that a system prompt alone can fully prevent prompt injection. In reality, attackers may still manipulate an AI system through direct user input or indirect instructions hidden in retrieved content. System prompts are useful, but they are not a complete security boundary. The OWASP Top 10 for LLM Applications discusses prompt injection under the heading “LLM01: Prompt Injection” and explains why additional safeguards are needed, including limiting privileges and controlling how external content is handled.
Resource: OWASP Top 10 for Large Language Model Applications - https://owasp.org/www-project-top-10-for-large-language-model-applications/

## Open Question
How can a government AI assistant detect indirect prompt injection hidden in retrieved documents while still providing accurate and helpful answers to citizens?
 
