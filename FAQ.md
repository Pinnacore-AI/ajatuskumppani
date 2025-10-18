# Frequently Asked Questions (FAQ)

## General Questions

### What is Ajatuskumppani?

Ajatuskumppani (ThoughtMate OS in English) is an open-source, user-controlled AI platform built in Finland. It combines privacy, transparency, and intelligence through a decentralized infrastructure. Unlike traditional AI assistants, Ajatuskumppani learns from you continuously and grows alongside you, while you maintain complete control over your data.

### Why "Ajatuskumppani"?

"Ajatuskumppani" is Finnish for "thought companion" or "thought partner." The name reflects our vision of creating an AI that doesn't just respond to commands, but actively engages with your thoughts, learns your preferences, and becomes a true digital companion.

### Is Ajatuskumppani really free and open source?

Yes! All core components are open source under permissive licenses (Apache 2.0, AGPL 3.0, MIT). You can view, modify, and deploy the code yourself. The base version is completely free to use. Premium features are available for those who want additional capabilities.

### How is this different from ChatGPT or other AI assistants?

Key differences include:

- **Open Source**: All code and models are transparent and auditable
- **User Control**: You own your data and can run everything locally
- **Decentralized**: Powered by a distributed network, not a single company
- **Learning Memory**: Builds a persistent profile that evolves with you
- **Finnish-First**: Native support for Finnish language and culture
- **Token Economy**: Contributors are rewarded with AJT tokens

## Technical Questions

### What language model does Ajatuskumppani use?

We use **Mistral 7B Instruct** as our base model, fine-tuned with Finnish language data and user interactions. The model is Apache 2.0 licensed and can run on consumer hardware.

### Can I run Ajatuskumppani on my own computer?

Yes! You can run the entire stack locally using Docker Compose. For the LLM, you can use either vLLM (GPU) or Ollama (CPU). A machine with 16GB RAM and a modern CPU can run the basic version. For optimal performance, a GPU with 8GB+ VRAM is recommended.

### What are the system requirements?

**Minimum** (CPU-only):
- 16GB RAM
- 50GB storage
- Modern multi-core CPU

**Recommended** (with GPU):
- 32GB RAM
- 100GB storage
- NVIDIA GPU with 8GB+ VRAM
- CUDA 11.8+

### How does the decentralized network work?

Users can run **AjatusNode** to contribute their computational resources to the network. The system uses a **Proof-of-Contribution (PoC)** algorithm to measure uptime, performance, and task completion. Contributors earn **AJT tokens** as rewards.

### Is my data private?

Yes. Your data is:
- **Encrypted at rest** and in transit
- **Stored locally** or in your chosen location
- **Never sold** or shared without your consent
- **GDPR compliant** with full data portability

You can export or delete your data at any time.

## Token Economy Questions

### What is the AJT token?

**AjatusToken (AJT)** is an ERC-20 utility token that powers the Ajatuskumppani ecosystem. It's used to reward contributors, unlock premium features, and participate in governance.

### How can I earn AJT tokens?

You can earn AJT by:
- Running an **AjatusNode** and contributing compute resources
- Contributing code, documentation, or translations
- Participating in community governance
- Completing bounties and challenges

### What can I do with AJT tokens?

- **Unlock Premium Features**: Access advanced AI capabilities
- **Stake for Rewards**: Earn additional tokens
- **Vote on Proposals**: Shape the future of the platform
- **Trade**: Exchange on supported platforms

### Is AJT an investment or security?

AJT is a **utility token**, not an investment or security. It's designed to facilitate the Ajatuskumppani ecosystem, not as a speculative asset. Always do your own research and consult with financial advisors.

## Development Questions

### How can I contribute to the project?

We welcome all types of contributions:

1. **Code**: Submit pull requests to any repository
2. **Documentation**: Improve guides, tutorials, and translations
3. **Testing**: Report bugs and test new features
4. **Community**: Help others on Discord/Telegram
5. **Design**: Contribute UI/UX improvements

See our [CONTRIBUTING.md](CONTRIBUTING.md) guide for details.

### What programming languages are used?

- **Backend**: Python (FastAPI, SQLAlchemy)
- **Frontend**: TypeScript (React Native)
- **Smart Contracts**: Solidity
- **AI/ML**: Python (PyTorch, Transformers)

### Do I need to know Finnish to contribute?

No! While the project is built in Finland, all code and documentation are in English. Finnish language support is a feature, not a requirement for contributors.

### How do I report a bug?

1. Check if the issue already exists on [GitHub Issues](https://github.com/Pinnacore-AI/ajatuskumppani/issues)
2. If not, create a new issue with:
   - Clear description of the problem
   - Steps to reproduce
   - Expected vs actual behavior
   - System information (OS, versions, etc.)

## Roadmap Questions

### When will the first version be released?

We're currently in **Phase 1** (Foundation & MVP), targeting a beta release in **Q2 2025**. See our [ROADMAP.md](ROADMAP.md) for detailed timeline.

### Will there be a mobile app?

Yes! The **AjatusUI** is built with React Native, which supports iOS, Android, and Web. The mobile alpha is planned for **Phase 2** (3-6 months).

### What about AR/VR support?

AR/VR integration is planned for **Phase 3** (6-12 months). We'll provide a Unity SDK and WebXR bridge for immersive experiences.

### Will Ajatuskumppani support other languages besides Finnish and English?

Yes! Community translations are welcome. The i18n infrastructure supports multiple languages. We're prioritizing Nordic languages first, then expanding globally.

## Community Questions

### How can I join the community?

- **Telegram**: https://t.me/ajatuskumppani - Main community hub
- **Discord**: [Coming soon]
- **GitHub Discussions**: https://github.com/Pinnacore-AI/ajatuskumppani/discussions
- **Lead Developer**: kryptonaatti@pinnacore.ai
- **General Inquiries**: ajatuskumppani@pinnacore.ai

### Is there a Code of Conduct?

Yes! We follow the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md). We're committed to providing a welcoming and inclusive environment for everyone.

### Can I use Ajatuskumppani for commercial purposes?

Yes, under the terms of the respective licenses:
- **Apache 2.0** components: Very permissive, commercial use allowed
- **AGPL 3.0** components: Commercial use allowed, but modifications must be open-sourced if deployed as a service
- **MIT** components: Very permissive, commercial use allowed

Always review the specific LICENSE file in each repository.

### Who is behind Pinnacore AI?

Pinnacore AI is a Finnish technology company focused on building open-source AI platforms. We believe in transparency, user empowerment, and the democratization of AI technology.

## Still Have Questions?

If your question isn't answered here:

1. Check the [documentation](docs/)
2. Search [GitHub Discussions](https://github.com/Pinnacore-AI/ajatuskumppani/discussions)
3. Join our [Telegram](https://t.me/ajatuskumppani) and ask the community
4. Email us at ajatuskumppani@pinnacore.ai

---

**Built in Finland. Open to the world.** 🇫🇮

*"Ajatuskumppani – tekoäly, joka oppii sinut."*

