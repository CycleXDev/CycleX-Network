<div align="center">

<img src="assets/elofid-logo.png" alt="Elofid" width="112" />

# Elofid

**On-chain security tools for wallets, tokens and communities.**

See what a token, a contract or a wallet permission can really do, before you sign, buy or connect.

[![Website](https://img.shields.io/badge/Website-elofid.com-22d3ee?style=flat-square)](https://elofid.com)
[![Telegram Bot](https://img.shields.io/badge/Telegram-Scanner%20Bot-6366f1?style=flat-square&logo=telegram&logoColor=white)](https://t.me/ElofidBot)
[![X](https://img.shields.io/badge/X-@ElofidNetwork-0f172a?style=flat-square&logo=x&logoColor=white)](https://x.com/ElofidNetwork)
[![Security Policy](https://img.shields.io/badge/Security-Policy-8b5cf6?style=flat-square)](SECURITY.md)

</div>

---

## Why Elofid

Most losses in Web3 are not dramatic hacks. They come from tokens that cannot be sold, taxes hidden in a contract, forgotten wallet approvals and transactions whose real effect was never clear.

Elofid reads the blockchain directly, simulates what would happen before anything is signed, and presents the result in plain language. Every figure is either verified on-chain or clearly marked as unverified.

## Products

| Product | What it does |
| --- | --- |
| **[Security Hub](https://elofid.com/security)** | Multi-chain token and contract scanner. Contract controls, liquidity, LP lock and burn evidence, holder concentration and market structure. No wallet connection required. |
| **Deep Intelligence** | Advanced analysis inside the Security Hub. A real buy and sell simulation through the token's own DEX router detects honeypots and measures buy, sell and transfer tax. Also covers deployer history, early buyers, shared-funding wallets, LP lock expiry and ownership history. |
| **[Scanner Bot](https://t.me/ElofidBot)** | The same engine inside Telegram. Paste a contract address and get a structured security report with contract risks, DEX and CEX liquidity, holder analysis and Exit Path. |
| **Firewall** | Wallet protection. Blast Radius maps every active approval, Fix Mode guides revocation, Wallet Watch alerts on new approvals, and Wallet Passport issues a signed, wallet-bound security record. |
| **Developer API** | Programmatic access to monitoring, security events, incidents, watchlists and webhooks. |

The Security Hub also includes a **Tx Decoder**, which turns a transaction into a readable preview before it is signed, and an **RPC Health Checker**, which flags unhealthy or suspicious network endpoints.

## How we report risk

Every Elofid product follows the same rules.

- **Unknown is never shown as clean.** If a data source fails or coverage is incomplete, the report says so and explains why. A missing value is never displayed as zero, "none" or "safe".
- **On-chain verification is marked.** Figures read directly from the blockchain are labeled as verified. Figures from third-party providers are labeled by source.
- **Simulations never touch real funds.** Buy, sell and transfer tests run as read-only simulations. Nothing is broadcast and nothing is signed.
- **Context, not accusations.** Signals such as a fresh deployer wallet or shared funding are shown as evidence to review, with the reasoning visible.
- **No secrets in the browser.** Scans never ask for a seed phrase or a wallet signature, and provider keys stay server-side.

## Supported networks

| EVM | | | Non-EVM |
| --- | --- | --- | --- |
| BNB Smart Chain | Ethereum | Base | Solana |
| Arbitrum | Polygon | Optimism | |
| Avalanche | Linea | Scroll | |
| opBNB | Robinhood Chain | | |

## Developer API

```bash
curl https://api.elofid.com/v1/health

curl https://api.elofid.com/v1/incidents \
  -H "Authorization: Bearer <API_KEY>"
```

| Endpoint | Description |
| --- | --- |
| `GET /v1/health` | Service status |
| `GET /v1/monitoring/assets/:chain/:token/events` | Security events for a monitored asset |
| `GET /v1/monitoring/assets/:chain/:token/incidents` | Incidents for a monitored asset |
| `GET /v1/events` · `GET /v1/incidents` | Account-wide feeds |
| `/v1/watchlists` | Manage monitored assets |
| `GET /v1/webhooks` · `POST /v1/webhooks` | Webhook delivery |
| `GET /v1/usage` | Current usage (does not count toward quota) |

| Plan | API calls / month | History |
| --- | --- | --- |
| Free | 10,000 | 7 days |
| Starter | 50,000 | 30 days |
| Growth | 250,000 | 60 days |
| Pro | 1,000,000 | 90 days |
| Enterprise | Custom | Custom |

Every plan, including Free, uses an API key. Only authenticated customer calls count toward the monthly quota.

## CYCX token

| | |
| --- | --- |
| Token | CYCX |
| Network | BNB Smart Chain (BEP-20) |
| Contract | [`0xda63b65825AE30532a507B0C091B0bD9F8204F7E`](https://bscscan.com/address/0xda63b65825AE30532a507B0C091B0bD9F8204F7E) |
| Total supply | 99,000,000,000 (fixed, no mint) |
| Status | **Not launched yet** |

The launch date and the reward-cycle schedule will be announced only through the official Elofid channels. Anyone offering CYCX before an official announcement is not affiliated with the project.

Read more in the **[Whitepaper](https://elofid.com/whitepaper.pdf)** and the **[FAQ](https://elofid.com/FAQ.pdf)**.

## Official channels

| Channel | Link |
| --- | --- |
| Website | [elofid.com](https://elofid.com) |
| Support | [support@elofid.com](mailto:support@elofid.com) |
| Telegram Scanner Bot | [@ElofidBot](https://t.me/ElofidBot) |
| Official Telegram | [@cyclex_official](https://t.me/cyclex_official) |
| Community | [@cyclexcommunity](https://t.me/cyclexcommunity) |
| X | [@ElofidNetwork](https://x.com/ElofidNetwork) |

> **Admins will never message you first.** Elofid will never ask for a seed phrase, a private key or a "manual claim". Treat any such message as a scam.

## Security

Found a vulnerability? Please follow our **[Security Policy](SECURITY.md)** and report it privately. Do not open a public issue.

## Disclaimer

Scores, signals and warnings are informational only. They are not an audit, financial advice or a guarantee of safety. Security scans reduce risk but cannot eliminate it.

<div align="center">

**Elofid · Security that starts before the loss.**

</div>
