# Custom Cloud Providers

Codex supports cloud providers through the existing model_providers configuration. No local model is required.

## Basic provider

Add a provider to ~/.codex/config.toml:

```toml
model_provider = "my-provider"

[model_providers.my-provider]
name = "My Provider"
base_url = "https://api.example.com/v1"
env_key = "MY_PROVIDER_API_KEY"
wire_api = "responses"
requires_openai_auth = false
```

Then export the API key:

```bash
export MY_PROVIDER_API_KEY="your-api-key"
```

ChatGPT authentication remains optional. API-key based cloud providers can operate independently through the existing provider abstraction.
