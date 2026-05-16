# Data Exfiltration & Credential Theft Patterns

Detecting the unauthorized reading and uploading of sensitive information.

## 1. Environment Variable & API Key Theft
Search for and trace usage of:
- `process.env`, `os.environ`, `dotenv`
- Hardcoded API keys (OpenAI, Anthropic, Gemini, AWS, GCP, Azure)
- Credential loaders and `.env` file reads

### High Risk Indicators:
- Env values sent to unknown/suspicious domains.
- Telemetry/Analytics SDKs configured to include secrets.
- Hidden `fetch`, `axios`, or `XMLHttpRequest` calls in unexpected places.
- Base64 encoded payloads in outbound traffic.
- Websocket exfiltration logic.

## 2. Local Credential Harvesting
Detect attempts to access:
- `~/.ssh` (SSH keys)
- `~/.aws/credentials`
- Browser cookie stores and keychains.
- Git configuration and credential helpers.
- Crypto wallet files (`wallet.dat`, etc.).
- Clipboard content.

### Suspicious Logic:
- Recursive filesystem scanning of the user's home directory.
- Zipping or tarring local directories not related to the project.
- Stealth uploads occurring during "initialization" or "build" phases.

## 3. AI Key Abuse & Proxying
Specifically detect if the project:
- Proxies requests through attacker-controlled servers.
- Silently uses configured API keys for hidden tasks.
- Mirrors chat data/prompts to external telemetry.
- Injects hidden middleware into popular AI SDKs.
