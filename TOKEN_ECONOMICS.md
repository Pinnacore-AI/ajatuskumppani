# AJT Arcade Token Economics

## Executive Summary

**AJT (Ajatuskumppani Token)** is an **arcade token** - a consumption-based utility token designed specifically for AI inference and compute services within the Ajatuskumppani ecosystem. Unlike governance or security tokens, AJT functions as **digital credits** for AI services, similar to arcade tokens, loyalty points, or in-game currency.

**Key Characteristics**:
- 💰 **Stable pricing** - Pegged to service units, not speculative
- 🔄 **Unlimited supply** - Minted on-demand to meet usage
- 🎯 **Pure utility** - Pay-per-use for AI services
- ⚖️ **Non-security** - Not an investment product
- ⚡ **Solana SPL** - Fast, cheap transactions

---

## What is an Arcade Token?

Think of a traditional arcade:
1. You enter with fiat currency (EUR/USD)
2. You exchange it for **arcade tokens**
3. You use tokens to play games
4. Tokens are **not meant to be held** as investments

**AJT works the same way**:
1. Users buy AJT with SOL/USDC
2. They spend AJT on AI services
3. Tokens are burned after use
4. New tokens are minted as needed

**Not a typical crypto token**:
- ❌ No governance rights
- ❌ No revenue sharing
- ❌ No staking rewards
- ❌ No price speculation
- ✅ Just a **payment method** for services

---

## Token Specifications

| Property | Value |
|----------|-------|
| **Name** | Ajatuskumppani Token |
| **Symbol** | AJT |
| **Blockchain** | Solana (SPL Token) |
| **Type** | Arcade Token (Utility) |
| **Supply Model** | Unlimited (minted on-demand) |
| **Decimals** | 9 |
| **Target Price** | ~$0.001 USD per token |
| **Minimum Purchase** | 1,000 AJT ($1 USD) |

---

## Pricing Model

### Base Rate
```
1 AJT ≈ $0.001 USD
1,000 AJT ≈ $1 USD
```

### Service Pricing

| Service | Cost (AJT) | USD Equivalent |
|---------|------------|----------------|
| **Chat Message** (1K tokens) | 1 AJT | $0.001 |
| **Code Execution** (1 run) | 10 AJT | $0.01 |
| **RAG Document** (upload) | 5 AJT | $0.005 |
| **Image Generation** (1 image) | 50 AJT | $0.05 |
| **Agent Evolution** (1 generation) | 100 AJT | $0.10 |
| **Voice Synthesis** (1 minute) | 20 AJT | $0.02 |

### Volume Discounts

| Purchase Amount | Bonus | Effective Price |
|-----------------|-------|-----------------|
| 10,000 AJT ($10) | 0% | $0.001/AJT |
| 100,000 AJT ($100) | +5% | $0.00095/AJT |
| 1,000,000 AJT ($1K) | +10% | $0.00091/AJT |
| 10,000,000 AJT ($10K) | +20% | $0.00083/AJT |

---

## Supply Mechanics

### Unlimited Supply Model

Unlike traditional tokens with fixed supply (e.g., Bitcoin's 21M), AJT uses an **unlimited supply** model:

**Why?**
- ✅ **Stable pricing** - No artificial scarcity driving speculation
- ✅ **Scalability** - Never run out of tokens
- ✅ **Predictable costs** - Users know exactly what they pay
- ✅ **Non-security** - Not an investment product

### Minting & Burning

**Minting** (Creating new tokens):
- Tokens are minted when users purchase credits
- Minted at a **fixed rate** (~$0.001 per AJT)
- No limit on total supply
- Controlled by Pinnacore treasury

**Burning** (Destroying tokens):
- Tokens are burned when users consume services
- Permanent removal from circulation
- Deflationary pressure on circulating supply
- Transparent on-chain

**Example Flow**:
```
User buys 10,000 AJT ($10)
→ 10,000 AJT minted to user wallet
→ User spends 1,000 AJT on chat
→ 1,000 AJT burned
→ 9,000 AJT remain in user wallet
```

---

## Token Distribution

### Initial Allocation (Bootstrap Phase)

| Allocation | Amount | Purpose |
|------------|--------|---------|
| **Treasury Reserve** | 100M AJT | Operational liquidity |
| **Team & Advisors** | 50M AJT | 2-year vesting |
| **Early Adopters** | 25M AJT | Airdrop & rewards |
| **Liquidity Pools** | 25M AJT | DEX liquidity (Raydium, Orca) |
| **Total Initial** | 200M AJT | ~$200K at $0.001/AJT |

**Note**: After bootstrap, supply becomes **unlimited** and minted on-demand.

### Vesting Schedule

**Team & Advisors** (50M AJT):
- 6-month cliff
- 24-month linear vesting
- No tokens sold during vesting

**Early Adopters** (25M AJT):
- 10M AJT: Immediate airdrop (first 10K users)
- 15M AJT: Referral rewards (12 months)

---

## Revenue Model

### How Pinnacore Makes Money

**1. Token Sales** (Primary Revenue)
- Users buy AJT at ~$0.001
- Pinnacore receives SOL/USDC
- Tokens are minted on-demand
- **Margin**: ~20-30% after AI costs

**2. Premium Features**
- Priority inference (faster responses)
- Private models (dedicated compute)
- API access (enterprise)
- **Pricing**: 2-5× base rate

**3. Node Operator Fees**
- Node operators stake SOL to join network
- Pinnacore takes 10% fee on node earnings
- **Revenue**: ~$50K-$500K/year (at scale)

### Cost Structure

| Cost Category | % of Revenue | Notes |
|---------------|--------------|-------|
| **AI Compute** | 40-50% | GPU/CPU costs |
| **Infrastructure** | 10-15% | Servers, bandwidth |
| **Development** | 15-20% | Team salaries |
| **Marketing** | 10-15% | User acquisition |
| **Operations** | 5-10% | Admin, legal, etc. |
| **Profit Margin** | 10-20% | Target |

---

## User Economics

### Example: Casual User

**Monthly Budget**: $10 (10,000 AJT)

| Activity | Usage | Cost (AJT) | USD |
|----------|-------|------------|-----|
| Chat (100 msgs) | 100K tokens | 100 AJT | $0.10 |
| Code runs (20×) | 20 runs | 200 AJT | $0.20 |
| RAG docs (10×) | 10 uploads | 50 AJT | $0.05 |
| Images (5×) | 5 images | 250 AJT | $0.25 |
| **Total** | - | **600 AJT** | **$0.60** |

**Result**: $10 lasts ~16 months for casual use!

### Example: Power User

**Monthly Budget**: $100 (100,000 AJT + 5% bonus = 105,000 AJT)

| Activity | Usage | Cost (AJT) | USD |
|----------|-------|------------|-----|
| Chat (1K msgs) | 1M tokens | 1,000 AJT | $1.00 |
| Code runs (500×) | 500 runs | 5,000 AJT | $5.00 |
| RAG docs (200×) | 200 uploads | 1,000 AJT | $1.00 |
| Images (100×) | 100 images | 5,000 AJT | $5.00 |
| Agents (50×) | 50 evolutions | 5,000 AJT | $5.00 |
| **Total** | - | **17,000 AJT** | **$17.00** |

**Result**: $100 lasts ~6 months for power users!

### Example: Enterprise

**Monthly Budget**: $10,000 (10M AJT + 20% bonus = 12M AJT)

| Activity | Usage | Cost (AJT) | USD |
|----------|-------|------------|-----|
| API calls | 10M tokens | 10,000 AJT | $10.00 |
| Dedicated model | 1 month | 5,000,000 AJT | $5,000.00 |
| Priority support | 1 month | 1,000,000 AJT | $1,000.00 |
| **Total** | - | **6,010,000 AJT** | **$6,010.00** |

**Result**: $10K covers enterprise needs + room for growth.

---

## Comparison: Arcade vs Traditional Tokens

| Feature | Arcade Token (AJT) | Governance Token | Security Token |
|---------|-------------------|------------------|----------------|
| **Purpose** | Pay for services | Vote on proposals | Investment |
| **Supply** | Unlimited | Fixed (e.g., 1B) | Fixed |
| **Price** | Stable (~$0.001) | Volatile | Tied to revenue |
| **Holder Expectation** | Spend it | Hold & vote | Hold & earn |
| **Regulation** | Utility (safe) | Gray area | Security (strict) |
| **Use Case** | AI credits | DAO governance | Equity-like |
| **Speculation** | Low | High | Medium-High |

---

## Regulatory Considerations

### Why AJT is NOT a Security

According to the **Howey Test** (U.S. SEC):

A security requires:
1. ✅ Investment of money
2. ✅ In a common enterprise
3. ✅ With expectation of profits
4. ✅ Derived from efforts of others

**AJT fails #3 and #4**:
- ❌ **No profit expectation** - Price is stable, not speculative
- ❌ **Not derived from others' efforts** - Value comes from utility, not Pinnacore's work

**AJT is a utility token**:
- ✅ Used to purchase services
- ✅ Consumed immediately
- ✅ No investment characteristics
- ✅ Similar to gift cards, loyalty points, in-game currency

### Precedents

**Similar models** (non-securities):
- **Airline miles** - Buy flights, not investments
- **Starbucks Rewards** - Buy coffee, not equity
- **Xbox Live Points** - Buy games, not shares
- **AWS Credits** - Buy compute, not stock

**Crypto precedents**:
- **Helium (HNT)** - Pay for IoT data
- **Filecoin (FIL)** - Pay for storage
- **Render (RNDR)** - Pay for GPU rendering

---

## Liquidity & Trading

### DEX Liquidity

**Initial Pools** (Raydium, Orca):
- AJT/SOL: 10M AJT + 100 SOL (~$20K)
- AJT/USDC: 10M AJT + $10K USDC

**Purpose**:
- Allow users to buy/sell AJT
- Provide price discovery
- Enable arbitrage (keeps price stable)

**Not for speculation**:
- Low liquidity (intentional)
- High slippage on large trades
- Discourage trading, encourage usage

### Price Stability Mechanism

**Target**: 1 AJT ≈ $0.001 USD

**How we maintain it**:
1. **Mint at fixed price** - Always sell at ~$0.001
2. **Burn on use** - Remove tokens from circulation
3. **Arbitrage** - If DEX price > $0.001, users buy from us and sell on DEX
4. **Treasury intervention** - Buy back if price drops too low

**Example**:
```
DEX price: 1 AJT = $0.0015 (50% premium)
→ User buys from Pinnacore at $0.001
→ Sells on DEX at $0.0015
→ Profit: $0.0005 per AJT
→ DEX price drops back to $0.001
```

---

## Roadmap

### Phase 1: Bootstrap (Q1 2025)
- ✅ Token design & economics
- ✅ Smart contract development
- ✅ Testnet deployment
- 🔄 Devnet launch

### Phase 2: Mainnet (Q2 2025)
- 🔜 Mainnet deployment
- 🔜 Initial liquidity (Raydium, Orca)
- 🔜 First 10K users airdrop
- 🔜 Web app integration

### Phase 3: Growth (Q3-Q4 2025)
- 🔜 Mobile app integration
- 🔜 Enterprise API launch
- 🔜 Node operator network
- 🔜 100K+ users

### Phase 4: Scale (2026+)
- 🔜 Multi-chain expansion (Ethereum, Polygon)
- 🔜 B2B partnerships
- 🔜 1M+ users
- 🔜 $10M+ monthly revenue

---

## FAQ

### Q: Is AJT a good investment?
**A**: No. AJT is **not an investment**. It's a payment method for AI services. If you're looking for investment returns, buy SOL, ETH, or BTC instead.

### Q: Will AJT price go up?
**A**: No. AJT is designed to stay **stable** at ~$0.001. It's not meant to appreciate in value.

### Q: Can I stake AJT?
**A**: No. Staking implies investment returns, which would make AJT a security. AJT is purely for consumption.

### Q: Why not just use SOL or USDC?
**A**: We could, but arcade tokens allow us to:
- Build gamification and rewards
- Adjust internal pricing without affecting external fiat pairs
- Create a closed-loop economy
- Avoid heavy stablecoin regulation

### Q: What if I don't use all my AJT?
**A**: Unused AJT stays in your wallet indefinitely. No expiration. You can also sell it back on DEXs (though at a slight loss due to slippage).

### Q: How is this different from OpenAI credits?
**A**: OpenAI credits are:
- Centralized (controlled by OpenAI)
- Non-transferable
- Fiat-denominated

AJT is:
- Decentralized (on Solana blockchain)
- Transferable (trade on DEXs)
- Crypto-native (buy with SOL/USDC)

### Q: What prevents Pinnacore from inflating supply?
**A**: Transparency. All minting/burning is on-chain and auditable. If we mint excessively, users will see it and lose trust.

---

## Conclusion

**AJT is an arcade token** - a new category of utility token designed for consumption, not speculation. It's the **digital equivalent of arcade tokens**, optimized for AI services in a decentralized, transparent, and user-friendly way.

**Key Takeaways**:
- 💰 Stable pricing (~$0.001/AJT)
- 🔄 Unlimited supply (minted on-demand)
- 🎯 Pure utility (pay-per-use)
- ⚖️ Non-security (no investment characteristics)
- ⚡ Solana-based (fast, cheap)

**For Users**: Buy AJT, use AI, repeat. Simple.

**For Investors**: Look elsewhere. AJT is not an investment.

**For Regulators**: AJT is a utility token, similar to gift cards or loyalty points, not a security.

---

**Built in Finland. Open to the world.** 🇫🇮

**Pinnacore Oy** | www.pinnacore.ai | ajatuskumppani@pinnacore.ai

