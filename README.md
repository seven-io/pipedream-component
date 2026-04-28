<p align="center">
  <img src="https://www.seven.io/wp-content/uploads/Logo.svg" width="250" alt="seven logo" />
</p>

<h1 align="center">seven Components for Pipedream</h1>

<p align="center">
  Collection of <a href="https://pipedream.com/">Pipedream</a> components for sending SMS, placing voice calls and running phone-number lookups via the seven gateway.
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-teal.svg" alt="MIT License" /></a>
  <img src="https://img.shields.io/badge/Pipedream-component-9333ea" alt="Pipedream component" />
  <img src="https://img.shields.io/badge/Node.js-18%2B-brightgreen" alt="Node.js 18+" />
</p>

---

## Components

| File | Action |
|------|--------|
| `actions/send-sms/send-sms.mjs` | Send an SMS |
| `actions/tts-call/tts-call.mjs` | Place a text-to-speech voice call |
| `actions/lookup-cnam/lookup-cnam.mjs` | CNAM (caller-name) lookup |
| `actions/lookup-format/lookup-format.mjs` | Format / validate a phone number |
| `actions/lookup-hlr/lookup-hlr.mjs` | HLR phone-number lookup |
| `actions/lookup-mnp/lookup-mnp.mjs` | MNP (number-portability) lookup |

## Prerequisites

- A [Pipedream](https://pipedream.com/) account and the [`pd` CLI](https://pipedream.com/docs/cli/reference/) authenticated against your workspace
- A [seven account](https://www.seven.io/) with API key ([How to get your API key](https://help.seven.io/en/developer/where-do-i-find-my-api-key))

## Installation

```bash
git clone https://github.com/seven-io/pipedream-component.git
cd pipedream-component
```

Publish the components you need:

```bash
pd publish ./actions/send-sms/send-sms.mjs
pd publish ./actions/tts-call/tts-call.mjs
pd publish ./actions/lookup-cnam/lookup-cnam.mjs
pd publish ./actions/lookup-format/lookup-format.mjs
pd publish ./actions/lookup-hlr/lookup-hlr.mjs
pd publish ./actions/lookup-mnp/lookup-mnp.mjs
```

## Configuration

Set your API key in one of two ways:

- **Workspace env var** - Add `SEVEN_API_KEY` under [Pipedream environment variables](https://pipedream.com/docs/environment-variables).
- **Per-step** - Fill the `apiKey` field directly on each component instance.

## Support

Need help? Feel free to [contact us](https://www.seven.io/en/company/contact/) or [open an issue](https://github.com/seven-io/pipedream-component/issues).

## License

[MIT](LICENSE)
