# Ajatuskumppani - Projektin Yhteenveto

**Luotu**: 14. lokakuuta 2025  
**Tekijä**: Pinnacore AI  
**Versio**: 0.1.0

## Yleiskatsaus

Ajatuskumppani on kunnianhimoinen avoimen lähdekoodin tekoälyalusta, joka pyrkii luomaan ensimmäisen eurooppalaisen käyttäjälähtöisen AI-käyttöjärjestelmän. Projekti yhdistää yksityisyyden, avoimuuden ja älykkyyden hajautetun infrastruktuurin kautta.

## Projektin Rakenne

Projekti koostuu seitsemästä pääkomponentista, jotka toimivat itsenäisesti mutta integroituvat saumattomasti yhteen:

### 1. **AjatusCore** - Kielimalli ja AI-ydin
- Perustuu Mistral 7B Instruct -malliin
- Fine-tuning suomenkielisellä datalla
- Optimoitu inference vLLM:n ja Ollaman avulla
- Tukee sekä GPU- että CPU-pohjaista ajoa

### 2. **AjatusServer** - Keskitetty API ja orkestrointi
- FastAPI-pohjainen backend-palvelu
- PostgreSQL-tietokanta pgvector-laajennuksella
- Redis-välimuisti ja viestijono
- JWT-pohjainen autentikointi
- WebSocket-tuki reaaliaikaiselle viestinnälle

### 3. **AjatusNode** - Hajautettu laskentanode
- DePIN-malli (Decentralized Physical Infrastructure Network)
- Proof-of-Contribution -palkkiojärjestelmä
- Docker-pohjainen eristys
- CLI-työkalu noden hallintaan

### 4. **AjatusUI** - Käyttöliittymä
- React Native -pohjainen cross-platform sovellus
- Tukee iOS, Android ja web-alustoja
- Kaksikielinen (suomi/englanti)
- Tailwind CSS -tyylit
- Zustand state management

### 5. **AjatusMemory** - Vektorimuisti ja oppiva profiilimalli
- Sentence-transformers embedding-generointiin
- pgvector ja FAISS vektorihakuun
- Oppiva käyttäjäprofiili
- Lokaalinen välimuisti

### 6. **AjatusToken (AJT)** - Token-ekonomia
- ERC-20-standardin mukainen token
- Maksimitarjonta: 1 miljardia AJT
- Proof-of-Contribution -palkkiot
- Staking ja governance
- Burn-mekanismi inflaation estämiseksi

### 7. **AjatusAgents** - Autonomiset agentit
- Task AI - Tehtävienhallinta
- News AI - Uutisten seuranta
- Social AI - Sosiaalinen vuorovaikutus
- Trade AI - Kaupankäynti
- LangChain/LangGraph-pohjainen

## Teknologiapino

### Backend
- **Kieli**: Python 3.11+
- **Web Framework**: FastAPI
- **Tietokanta**: PostgreSQL 15+ (pgvector)
- **Cache**: Redis
- **LLM Inference**: vLLM, Ollama
- **Vector Store**: FAISS, pgvector

### Frontend
- **Framework**: React Native
- **Kieli**: TypeScript
- **Styling**: Tailwind CSS
- **State**: Zustand

### DevOps
- **Kontterointi**: Docker, Docker Compose
- **CI/CD**: GitHub Actions
- **Paketointi**: Debian (.deb), npm, PyPI

### Blockchain
- **Verkko**: Ethereum L2 / Peaq / DeNet
- **Framework**: Hardhat
- **Kieli**: Solidity 0.8+

## Kehityksen Roadmap

### Phase 1: Foundation & MVP (0–3 kk)
- GitHub-repositoriot ja dokumentaatio ✅
- AjatusCore v0.1 (base model + inference)
- AjatusServer v0.1 (core API)
- AjatusUI MVP (web chat)

### Phase 2: Decentralization & Learning (3–6 kk)
- AjatusNode v1.0 (DePIN client)
- AjatusToken (AJT) deployment
- AjatusMemory v1.0 (learning system)
- Premium-ominaisuudet
- Mobile app (alpha)

### Phase 3: Expansion & Community (6–12 kk)
- AR/VR-integraatio
- Community governance
- NFT-identiteetit
- Agent marketplace

### Phase 4: The Open AI Network (12+ kk)
- Inter-node communication
- Federated learning
- Global AI network

## Lisensointi

Projekti käyttää multi-license-mallia:

| Komponentti | Lisenssi |
|------------|----------|
| AjatusCore | Apache 2.0 |
| AjatusNode | AGPL 3.0 |
| AjatusServer | AGPL 3.0 |
| AjatusUI | Apache 2.0 |
| AjatusMemory | Apache 2.0 |
| AjatusToken | MIT |
| AjatusAgents | AGPL 3.0 |

## Token-ekonomia

### AJT Token Specs
- **Maksimitarjonta**: 1,000,000,000 AJT
- **Alkutarjonta**: 100,000,000 AJT (10%)
- **Standardi**: ERC-20
- **Blockchain**: Ethereum L2 / Peaq / DeNet

### Jakautuminen
- Community Rewards: 40% (400M AJT)
- Team & Advisors: 20% (200M AJT)
- Public Sale: 15% (150M AJT)
- Ecosystem Development: 15% (150M AJT)
- Treasury: 10% (100M AJT)

### Käyttötarkoitukset
1. **Proof-of-Contribution Rewards** - Palkkiot laskentaresurssien jakamisesta
2. **Premium Features** - Pääsy premium-ominaisuuksiin
3. **Governance** - Äänioikeus päätöksenteossa
4. **Staking** - Tokenien lukitseminen palkkioita vastaan

## Yhteisö ja Kommunikaatio

### Kanavat
- **GitHub**: Koodi, issues, discussions
- **Discord**: Reaaliaikainen chat
- **Telegram**: Suomenkielinen yhteisö
- **Email**: gronmark@pinnacore.ai

### Roolit
- **Core Team**: Pinnacore AI
- **Contributors**: Avoimen lähdekoodin kehittäjät
- **Node Operators**: DePIN-operaattorit
- **Community**: Käyttäjät ja testaajat

## Brändi ja Identiteetti

### Nimi
- **Suomeksi**: Ajatuskumppani
- **Englanniksi**: ThoughtMate OS

### Visuaalinen Identiteetti
- **Värit**: Lime-vihreä, musta, valkoinen
- **Tyyli**: Minimalistinen, futuristinen
- **Maskotti**: Pinnacore-jänis (uteliaisuus ja vapaus)

### Slogan
> "Ajatuskumppani – tekoäly, joka oppii sinut."  
> "Built in Finland. Open to the world."

## Turvallisuus ja Yksityisyys

- **GDPR-yhteensopiva**: Täydet oikeudet omaan dataan
- **Lokaalinen oppiminen**: Kaikki oppiminen tapahtuu lokaalisti tai salatusti
- **Läpinäkyvä AI-etiikka**: "Open weights" -periaate
- **Säännölliset auditoinnit**: Neljännesvuosittaiset turvallisuustarkastukset

## Seuraavat Askeleet

1. ✅ Projektisuunnittelu ja dokumentaatio
2. ⏭️ GitHub-repositorioiden julkaisu
3. ⏭️ AjatusCore-mallin fine-tuning
4. ⏭️ AjatusServer MVP:n kehitys
5. ⏭️ AjatusUI web-version julkaisu
6. ⏭️ Yhteisön käynnistys (Discord, Telegram)
7. ⏭️ AjatusNode alpha-version julkaisu
8. ⏭️ AJT token deployment

## Yhteystiedot

**Pinnacore AI**  
Email: gronmark@pinnacore.ai  
Website: https://pinnacore.ai  
GitHub: https://github.com/pinnacore-ai

---

**This is the project that will define Pinnacore AI's legacy.**  
**This is The ThoughtMate Revolution.**

// Ajatuskumppani — built in Finland, by the free minds of Pinnacore.

