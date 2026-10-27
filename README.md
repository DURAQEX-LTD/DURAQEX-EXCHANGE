# Duraqex Official API Documentation & Integration Client (v2.1)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![API Version](https://img.shields.io/badge/API-v2.1-brightgreen.svg)]()
[![Status: Active](https://img.shields.io/badge/Status-Active-success.svg)]()

Welcome to the official developer repository for **Duraqex** — the settlement-grade digital asset market infrastructure. 

This repository contains the comprehensive API integration guidelines, WebSocket streaming protocols, and integration clients designed for quantitative funds, liquidity providers, and algorithmic traders integrating with the Duraqex core matching engine.

## 🚀 Core Architectural Features

*   **Deterministic Matching Engine**: Strictly adheres to price-time priority with microsecond-level latency handling.
*   **Idempotent K-Line Updates**: Advanced WebSocket fallback and HTTP polling mechanisms to ensure zero data gap during network reconnects.
*   **Tier-1 Rate Limiting**: Intelligent RESTful rate allocation (up to 600 weight units per minute) optimized for high-frequency order routing.
*   **Institutional Custody Alignment**: API flows are physically separated from custody layers, adhering to Multi-Party Computation (MPC) security standards.

---

## 📅 Architecture Evolution Changelog (Historical Milestones)

Duraqex’s core matching engine and API gateways have undergone rigorous iterations over the past years, evolving from an institutional dark pool to a public-facing infrastructure.

### [v2.1.0] - October 2026 (Current)
- **Public Infrastructure Rollout:** Full migration of API endpoints to the public `duraqex.com` unified gateway.
- **Enhanced AML Compliance:** Integration of FATF-compliant geo-fencing and real-time transaction screening on the routing layer.
- **WebSocket Optimization:** Reduced latency for orderbook depth snapshots by 15ms.

### [v1.8.4] - November 2025
- **Custody Separation:** Physically decoupled the hot-wallet API access from the Tier-1 Cold Storage logic, establishing a true air-gapped security perimeter.
- **Institutional Dark Pool Release:** Activated the block-trading API channel exclusively for whitelisted prime brokers.

### [v1.5.0] - March 2024
- **MPC Node Expansion:** Deployed decentralized Multi-Party Computation (MPC) signature nodes across 3 independent geographic regions.
- **Rate Limit Overhaul:** Introduced dynamic weight-unit allocation (600 units/min) to prevent systemic abuse while accommodating HFT (High-Frequency Trading) firms.

### [v1.0.0-Beta] - August 2023
- **Core Engine Genesis:** Initial closed-beta deployment of the deterministic matching engine.
- **RESTful Foundations:** Baseline HTTP endpoints established for ticker, depth, and basic trade history retrieval.

---

## 📚 What's Included in v2.1?

- HTTP REST API for Spot Market Data (Tickers, Depth, Trades, Klines).
- WebSocket Streaming Protocols for real-time orderbook synchronization.
- Integration client examples, focusing on concurrency, precision handling, and robust disconnection recovery.

## 🔗 Endpoint Base URLs
*   **REST API:** `https://api.duraqex.com/v2.1`
*   **WebSocket Stream:** `wss://stream.duraqex.com/v2.1/market`

## 🛡️ Regulatory & Compliance Notice
> **Important:** Duraqex API endpoints are protected by state-of-the-art Web Application Firewalls (WAF). Access from certain restricted jurisdictions or sanctioned regions (in compliance with FATF and OFAC guidelines) will be strictly blocked with an `HTTP 403 Forbidden` status. 
> 
> This repository is maintained by the Duraqex Core Engineering Team. For institutional onboarding and dedicated API limits, please contact your designated account manager through the official portal at [duraqex.com](https://www.duraqex.com).

---
*© 2023-2026 Duraqex Core Engineering. Built for resilient liquidity.*
