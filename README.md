# Teller

Teller is a unified banking API providing real-time access to bank accounts, transactions, balances, identity data, and payment initiation across US financial institutions. Connect to thousands of banks and credit unions through a single integration. Teller uses mutual TLS (mTLS) for application authentication and access tokens obtained via Teller Connect for per-account authorization.

**Website:** https://teller.io/

**Developer Portal:** https://teller.io/docs/api

**GitHub Organization:** https://github.com/tellerhq

## API

| Resource | Operations |
|----------|-----------|
| `GET /identity` | List accounts with owner identity |
| `GET /accounts` | List all accounts |
| `GET /accounts/{id}` | Get single account |
| `DELETE /accounts/{id}` | Revoke account authorization |
| `GET /accounts/{id}/details` | Get routing + account numbers |
| `GET /accounts/{id}/balances` | Get available + ledger balances |
| `GET /accounts/{id}/transactions` | List transactions (paginated) |
| `GET /accounts/{id}/transactions/{txn_id}` | Get single transaction |
| `GET /institutions` | List supported institutions (public) |

## Authentication

Teller uses two complementary mechanisms:
1. **mTLS** — Teller issues client certificates for application-level authentication
2. **Access Tokens** — Per-user tokens obtained via Teller Connect, used as HTTP Basic Auth username

## SDKs

| Platform | Repository |
|----------|-----------|
| React | [teller-connect-react](https://github.com/tellerhq/teller-connect-react) |
| iOS | [iOS-SDK](https://github.com/tellerhq/iOS-SDK) |
| Android | [teller-connect-android](https://github.com/tellerhq/teller-connect-android) |
| Ruby | [teller-ruby](https://github.com/tellerhq/teller-ruby) |

## Links

- [Website](https://teller.io/)
- [Documentation](https://teller.io/docs)
- [API Reference](https://teller.io/docs/api)
- [Quickstart](https://teller.io/docs/guides/quickstart)
- [Authentication Guide](https://teller.io/docs/api/authentication)
- [GitHub Organization](https://github.com/tellerhq)

## Capabilities

| Capability | Description |
|------------|-------------|
| [open-banking.yaml](capabilities/open-banking.yaml) | Unified open banking data access workflow |

### Shared Definitions

| File | API |
|------|-----|
| [capabilities/shared/teller.yaml](capabilities/shared/teller.yaml) | Teller API |

## Artifacts

| Artifact | Description |
|----------|-------------|
| [apis.yml](apis.yml) | API catalog index |
| [openapi/teller-openapi.yml](openapi/teller-openapi.yml) | OpenAPI specification |
| [rules/teller-rules.yml](rules/teller-rules.yml) | Spectral ruleset |
| [json-schema/teller-account-schema.json](json-schema/teller-account-schema.json) | Account schema |
| [json-schema/teller-transaction-schema.json](json-schema/teller-transaction-schema.json) | Transaction schema |
| [json-structure/teller-banking-structure.json](json-structure/teller-banking-structure.json) | API structure documentation |
| [json-ld/teller-context.jsonld](json-ld/teller-context.jsonld) | JSON-LD context |
| [examples/teller-list-accounts-example.json](examples/teller-list-accounts-example.json) | List accounts example |
| [examples/teller-list-transactions-example.json](examples/teller-list-transactions-example.json) | List transactions example |
| [examples/teller-get-balances-example.json](examples/teller-get-balances-example.json) | Get balances example |
| [vocabulary/teller-vocabulary.yml](vocabulary/teller-vocabulary.yml) | Domain vocabulary |
