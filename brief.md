Version: NAFATH-V3
Track: Cybersecurity

## Overview
A trustworthy government AI assistant depends on six connected IT fields. Software engineering defines a stable public API so the mobile app can communicate with government services as they evolve. Artificial intelligence uses retrieval-augmented generation (RAG) to retrieve relevant information from approved sources before generating answers. Mobile security helps protect communication between the app and its servers. Networking provides the addressing and connectivity needed for citizens to access the service across different devices and networks. Cybersecurity reduces risks such as prompt injection, unauthorized access, and exposure of sensitive information. Data management determines how chat logs are stored, protected, and retained while respecting privacy requirements. These fields must work together: accurate AI answers are not enough if the connection is insecure, the API breaks the app, or personal data is mishandled. Clear responsibilities, testing, monitoring, and regular reviews help the service remain reliable, accessible, and safe for citizens.


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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
