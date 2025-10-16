# Ajatuskumppani - Projektirakenne

## Yleiskatsaus

Ajatuskumppani on avoimen lähdekoodin tekoälyalusta, joka koostuu useista itsenäisistä mutta integroiduista komponenteista. Projekti noudattaa mikropalveluarkkitehtuuria ja hajautettua laskentamallia.

## Komponentit

### 1. AjatusCore
**Kuvaus**: Kielimalli ja AI-ydin  
**Teknologia**: Python, Mistral 7B, vLLM/Ollama  
**Lisenssi**: Apache 2.0  
**Repositorio**: `ajatuskumppani/ajatus-core`

**Rakenne**:
```
ajatus-core/
├── models/              # Mallit ja painot
├── training/            # Fine-tuning skriptit
├── inference/           # Inference engine
├── config/              # Konfiguraatiot
├── tests/               # Testit
└── docs/                # Dokumentaatio
```

### 2. AjatusNode
**Kuvaus**: Hajautettu agentti ja laskentanode  
**Teknologia**: Python, Docker, Debian packaging  
**Lisenssi**: AGPL 3.0  
**Repositorio**: `ajatuskumppani/ajatus-node`

**Rakenne**:
```
ajatus-node/
├── src/
│   ├── compute/         # Laskentamoottori
│   ├── storage/         # Hajautettu tallennus
│   ├── validator/       # PoC validointi
│   └── network/         # P2P verkko
├── docker/              # Docker konfiguraatiot
├── debian/              # .deb paketointi
├── cli/                 # Komentorivityökalu
└── tests/
```

### 3. AjatusServer
**Kuvaus**: API ja orkestrointi  
**Teknologia**: FastAPI, PostgreSQL, Redis, vLLM  
**Lisenssi**: AGPL 3.0  
**Repositorio**: `ajatuskumppani/ajatus-server`

**Rakenne**:
```
ajatus-server/
├── api/
│   ├── routes/          # API endpoints
│   ├── middleware/      # Middleware
│   └── schemas/         # Pydantic schemas
├── services/
│   ├── llm/             # LLM palvelu
│   ├── memory/          # Muistipalvelu
│   ├── auth/            # Autentikointi
│   └── orchestrator/    # Agenttien orkestrointi
├── database/
│   ├── models/          # SQLAlchemy mallit
│   └── migrations/      # Alembic migraatiot
├── config/
└── tests/
```

### 4. AjatusUI
**Kuvaus**: Käyttöliittymä  
**Teknologia**: React Native, Tailwind CSS, TypeScript  
**Lisenssi**: Apache 2.0  
**Repositorio**: `ajatuskumppani/ajatus-ui`

**Rakenne**:
```
ajatus-ui/
├── src/
│   ├── components/      # React komponentit
│   ├── screens/         # Näkymät
│   ├── services/        # API integraatiot
│   ├── store/           # State management
│   ├── i18n/            # Kielitiedostot (FI/EN)
│   └── theme/           # Teemat ja tyylit
├── assets/              # Kuvat, fontit
├── ios/                 # iOS build
├── android/             # Android build
└── web/                 # Web build
```

### 5. AjatusMemory
**Kuvaus**: Vektorimuisti ja oppiva profiilimalli  
**Teknologia**: Python, pgvector, FAISS, sentence-transformers  
**Lisenssi**: Apache 2.0  
**Repositorio**: `ajatuskumppani/ajatus-memory`

**Rakenne**:
```
ajatus-memory/
├── src/
│   ├── embeddings/      # Embedding generaattorit
│   ├── vector_store/    # Vektoritietokanta
│   ├── profile/         # Käyttäjäprofiili
│   └── retrieval/       # Tiedonhaku
├── models/              # Embedding mallit
└── tests/
```

### 6. AjatusToken
**Kuvaus**: Token-ekonomia ja blockchain-integraatio  
**Teknologia**: Solidity, Hardhat, ethers.js  
**Lisenssi**: MIT  
**Repositorio**: `ajatuskumppani/ajatus-token`

**Rakenne**:
```
ajatus-token/
├── contracts/           # Smart contracts
│   ├── AJT.sol          # ERC-20 token
│   ├── Staking.sol      # Staking mekaniikka
│   └── PoC.sol          # Proof of Contribution
├── scripts/             # Deployment skriptit
├── test/                # Contract testit
└── docs/                # Token dokumentaatio
```

### 7. AjatusAgents
**Kuvaus**: Autonomiset agentit (Task AI, News AI, Social AI, Trade AI)  
**Teknologia**: Python, LangChain/LangGraph  
**Lisenssi**: AGPL 3.0  
**Repositorio**: `ajatuskumppani/ajatus-agents`

**Rakenne**:
```
ajatus-agents/
├── src/
│   ├── task_agent/      # Tehtävienhallinta
│   ├── news_agent/      # Uutisten seuranta
│   ├── social_agent/    # Sosiaalinen vuorovaikutus
│   ├── trade_agent/     # Kaupankäynti
│   └── base/            # Yhteinen agenttipohja
├── tools/               # Agenttityökalut
└── tests/
```

## Monorepo vs. Multi-repo strategia

**Valinta**: Multi-repo (useita repositorioita)

**Perustelu**:
- Komponentit ovat riittävän itsenäisiä
- Eri lisenssit eri komponenteille
- Helpompi versionhallinta
- Selkeämpi vastuunjako kehittäjille

**Päärepositorio**: `ajatuskumppani` (dokumentaatio, yleiskatsaus)

## Teknologiapino

### Backend
- **Kieli**: Python 3.11+
- **Web Framework**: FastAPI
- **Tietokanta**: PostgreSQL 15+ (pgvector)
- **Cache**: Redis
- **LLM Inference**: vLLM, Ollama
- **Vector Store**: FAISS, pgvector
- **Task Queue**: Celery + Redis

### Frontend
- **Framework**: React Native (Web + Mobile)
- **Kieli**: TypeScript
- **Styling**: Tailwind CSS
- **State**: Zustand / Redux Toolkit
- **API Client**: Axios / React Query

### DevOps
- **Kontterointi**: Docker, Docker Compose
- **CI/CD**: GitHub Actions
- **Paketointi**: Debian (.deb), npm, PyPI
- **Monitorointi**: Prometheus + Grafana

### Blockchain
- **Verkko**: Ethereum L2 / Peaq / DeNet
- **Framework**: Hardhat
- **Kieli**: Solidity 0.8+

## Kehitysympäristö

### Vaatimukset
- Python 3.11+
- Node.js 18+
- Docker & Docker Compose
- PostgreSQL 15+
- CUDA 11.8+ (GPU inference)

### Suositellut työkalut
- **IDE**: VSCode, PyCharm
- **Git**: Conventional Commits
- **Linting**: ruff (Python), ESLint (TypeScript)
- **Formatting**: black (Python), Prettier (TypeScript)
- **Testing**: pytest (Python), Jest (TypeScript)

## Lisensointi

| Komponentti | Lisenssi | Perustelu |
|------------|----------|-----------|
| AjatusCore | Apache 2.0 | Maksimaalinen yhteensopivuus |
| AjatusNode | AGPL 3.0 | Hajautettu verkko, copyleft |
| AjatusServer | AGPL 3.0 | Backend palvelu, copyleft |
| AjatusUI | Apache 2.0 | Käyttöliittymä, permissiivinen |
| AjatusMemory | Apache 2.0 | Kirjasto, laaja käyttö |
| AjatusToken | MIT | Blockchain, standardilisenss |
| AjatusAgents | AGPL 3.0 | Agentit, copyleft |

## Versionhallinta

**Strategia**: Semantic Versioning (SemVer)

**Format**: `MAJOR.MINOR.PATCH`

**Branching**:
- `main` - Vakaa tuotantoversio
- `develop` - Kehitysversio
- `feature/*` - Uudet ominaisuudet
- `bugfix/*` - Bugikorjaukset
- `release/*` - Release kandidaatit

## Dokumentaatio

### Pakollinen dokumentaatio jokaisessa repossa:
- `README.md` - Yleiskatsaus ja pika-aloitus
- `CONTRIBUTING.md` - Kontribuutio-ohjeistus
- `LICENSE` - Lisenssitiedosto
- `CHANGELOG.md` - Muutosloki
- `docs/` - Tekninen dokumentaatio
  - `architecture.md` - Arkkitehtuuri
  - `api.md` - API dokumentaatio
  - `development.md` - Kehitysohjeistus
  - `deployment.md` - Käyttöönotto-ohje

## Testaus

### Testausstrategia:
- **Unit tests**: 80%+ coverage
- **Integration tests**: Kriittiset polut
- **E2E tests**: Pääkäyttötapaukset
- **Performance tests**: Inference, API

### CI/CD Pipeline:
1. Linting & Formatting
2. Unit tests
3. Integration tests
4. Build Docker images
5. Deploy to staging
6. E2E tests
7. Deploy to production

## Turvallisuus

### Turvallisuuskäytännöt:
- **Dependency scanning**: Dependabot, Snyk
- **Secret management**: Vault, env-tiedostot
- **Code scanning**: CodeQL, Bandit
- **GDPR compliance**: Data minimization, encryption
- **Security audits**: Quarterly reviews

## Yhteisö

### Kommunikaatiokanavat:
- **GitHub Discussions**: Keskustelu, Q&A
- **Discord**: Reaaliaikainen chat
- **Telegram**: Suomenkielinen yhteisö
- **Email**: gronmark@pinnacore.ai

### Roolit:
- **Core Team**: Pinnacore AI
- **Contributors**: Avoimen lähdekoodin kehittäjät
- **Node Operators**: DePIN-operaattorit
- **Community**: Käyttäjät ja testaajat

## Seuraavat askeleet

1. ✅ Projektisuunnittelu
2. ⏭️ GitHub-repositorioiden luonti
3. ⏭️ Peruskoodin kehitys
4. ⏭️ Dokumentaation kirjoitus
5. ⏭️ CI/CD pystytys
6. ⏭️ Yhteisön käynnistys

