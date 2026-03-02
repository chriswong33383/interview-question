## Log / IOC Detector (Security-automation style)

**Task**

Part 1 - Programming:

Build a command-line tool that analyzes web/application logs, extracts Indicators of Compromise (IOCs), performs basic detection logic, and produces structured output suitable for security operations use.

- Parses mixed web/app logs
- Extracts and normalizes IOCs:
    - IPs (v4/v6), domains, URLs, hashes (MD5/SHA1/SHA256)
- Deduplicates, scores, and outputs:
    - JSON report + human-readable summary
- Applies basic detection logic:
    - suspicious user agents
    - high 401 rate per IP (brute force)
    - access to sensitive endpoints
- Includes tests for parsing edge cases

Part 2 — System Design (Architecture Exercise)

Provide a short design document (1–2 pages) describing:

A. Backend Service Design

How would you:
- Expose this functionality as an API?
- Handle large log uploads?
- Ensure performance and scalability?
- Store results?
- Enable rule configuration?

Include:
- Component diagram (simple is fine)
- Data flow
- API design (high-level)

B. Frontend Integration

Design a frontend interface that connects to the backend.

Must include:
- Log upload interface
- IOC visualization table
- Detection findings dashboard
- Filtering and search capability

Explain:
- How data flows from backend to frontend
- How large reports are handled
- Error handling approach

C. GenAI Chatbot Integration

Describe how you would integrate a GenAI assistant that:
- Summarizes findings
- Explains risk level
- Answers analyst questions about the report
- Suggests remediation actions

Address:
- Data privacy considerations
- Prompt design
- Preventing data leakage
- Caching / cost control
- Guardrails

| No need to implement — design explanation only.
