# Blockchain no MRV: validade e potencial

> Status: análise (out/2026).

## Resposta curta

- **Nenhuma norma exige ou reconhece blockchain como critério de MRV.** GHG Protocol, ISO 14064, ISO 14083, SBCE, RenovaBio e CGOB avaliam **metodologia, qualidade do dado e verificação independente**. A tecnologia de registro não entra na avaliação.
- **Ainda assim, há potencial real**, mas em outro lugar: deixou de ser "token de crédito de carbono" (moda de 2021-2022) e passou a ser **infraestrutura de MRV digital (dMRV) e trilha de auditoria**.

## O que mudou de 2021 a 2026

| Fase | O que aconteceu |
|---|---|
| 2021-2022: hype dos tokens | Protocolos como Toucan e KlimaDAO "tokenizaram" créditos antigos e de baixa qualidade. **A Verra proibiu tokens baseados em créditos aposentados** e passou a exigir imobilização do crédito no registro e controles de identificação do cliente (KYC) |
| 2023-2025: virada para dMRV | Verra e Hedera fazem parceria para digitalizar metodologias via **Hedera Guardian** (código aberto), integrado ao Project Hub da Verra |
| **Mar/2026** | **Gold Standard emite os primeiros créditos 100% digitais** (fogões, ATEC Global): sensores coletam o dado, auditoria independente, rastreabilidade pública no Hedera Guardian |
| Fev/2026 | O registro BCarbon migra mais de 2 milhões de créditos para a Hedera |
| **Brasil, nov/2025** | **O Banco Central desligou a blockchain do Drex**, um dos motivos sendo a **incompatibilidade da imutabilidade com a LGPD** (direito de apagar dados pessoais) |

**Tendência:** créditos com dMRV (sensores, satélite, registro imutável) **conseguem preço maior** e **emissão mais rápida** do que os verificados só por auditoria anual em campo.

## Limites (o que blockchain NÃO resolve)

1. **Problema do oráculo:** a blockchain garante que o dado **não foi alterado depois** de registrado, mas **não que estava certo** quando entrou. Se o sensor está descalibrado ou alguém digitou errado, o erro fica gravado para sempre. O difícil do MRV continua sendo **medir bem e verificar**.
2. **Registros oficiais mandam:** o ativo legal está no registro oficial. No **SBCE**, é o registro central do órgão gestor; o **CBIO** é escriturado na B3; o **CGOB** segue o sistema da ANP e dos certificadores credenciados. Um token é, no máximo, um **espelho** e não substitui o ativo.
3. **LGPD:** dados de produtores rurais, motoristas e CPFs **não podem ir para uma blockchain pública**. Foi um dos motivos do recuo do Drex.
4. **Regulação financeira:** pela Lei 15.042/2024, créditos de carbono podem ser **valores mobiliários**. Fracionar e vender tokens para o público pode ser uma **oferta sob regras da CVM** (por exemplo, a Res. CVM 88 para crowdfunding). É um risco regulatório relevante.
5. **Custo e complexidade:** para um sistema com um só dono do dado, um banco de dados com trilha de auditoria criptográfica entrega quase o mesmo resultado por uma fração do custo.

## Onde há valor para os nossos produtos

| Uso | Valor | Recomendação |
|---|---|---|
| **Trilha de auditoria à prova de adulteração** | Provar ao verificador que o dado do sensor, da NF-e ou do CT-e não foi alterado | ✅ **Usar.** Dados assinados na origem, encadeados por hash e **somente o hash ancorado periodicamente** numa rede pública (Hedera ou similar). É barato e compatível com a LGPD, porque nenhum dado pessoal vai para a blockchain |
| **Prevenção de dupla contagem** entre CGOB, CBIO, I-REC, crédito de carbono e Escopo 3 | O mesmo m³ ou tonelada não pode ser vendido duas vezes (alerta da ABAR) | ✅ **Potencial alto**, mas o ganho real exige um **registro compartilhado entre certificadores**. Começar com registro interno e propor um consórcio depois |
| **Integração com Verra e Gold Standard via Guardian** | Emissão mais rápida e preço maior para créditos voluntários (metano de granjas, biochar, frotas) | ✅ **Usar no programa de agregação de créditos (S2)**: projetar o MRV para exportar dados no formato do Guardian |
| **Contratos inteligentes para divisão de receita** | Pagamento automático a centenas de granjas no programa agregado | ⚠️ Possível, mas o **software convencional com Pix** faz o mesmo com menos risco. Só vale se o comprador exigir |
| **Tokenizar e vender créditos fracionados ao público** | Liquidez e acesso de pequenos compradores | ❌ **Evitar por enquanto**: risco regulatório (CVM), reputacional (histórico de 2022) e sem reconhecimento oficial |

## Recomendação de arquitetura: "pronto para blockchain, mas sem depender dela"

```
Sensor / NF-e / CT-e
   │  (assinatura digital na origem)
   ▼
Banco de dados do MRV ── registro encadeado por hash (append-only)
   │                          │
   │                          └─► hash diário ancorado em rede pública
   ▼                              (prova de integridade, sem dados pessoais)
Relatórios / certificados
   ├─► Registros oficiais (SBCE, B3/CBIO, ANP/CGOB)
   └─► Hedera Guardian (créditos voluntários Verra / Gold Standard)
```

**Como vender:** o cliente compra **confiança, velocidade de emissão e preço maior do crédito**, e não "blockchain". A tecnologia aparece como garantia técnica, não como produto.

## Fontes

- [Verra: Addresses Crypto Instruments and Tokens](https://verra.org/verra-addresses-crypto-instruments-and-tokens/)
- [Carbon Herald: Verra bans tokenized (retired) carbon credits](https://carbonherald.com/verra-bans-tokenized-carbon-credits-toucan-approves/)
- [Verra e Hedera: transformação digital dos mercados de carbono](https://verra.org/verra-and-hedera-to-accelerate-digital-transformation-of-carbon-markets/)
- [Gold Standard: primeiros créditos totalmente digitais no Hedera Guardian](https://www.goldstandard.org/news/first-fully-digital-cookstove-carbon-credits-issued-publicly-traceable-on-hedera-guardian)
- [Carbon Pulse: primeiros créditos digitalizados com dMRV](https://carbon-pulse.com/496286/)
- [Carbon Market Network: o que é dMRV](https://carbonmarketnetwork.com/blog/what-is-dmrv/)
- [Finsiders: Drex abandona blockchain](https://finsidersbrasil.com.br/pagamentos/drex/drex-abandona-blockchain-em-nova-fase-tokenizacao-continua/)
- [Forbes: Brazil abandons blockchain for Drex](https://www.forbes.com/sites/digital-assets/2025/08/13/brazil-abandons-blockchain-for-its-drex-cbdc-project/)
- [Finfy: Drex 2026 e o desligamento da blockchain](https://blog.finfy.com.br/drex-2026-o-banco-central-desligou-a-blockchain-e-isso-pode-ser-a-melhor-noticia-para-fintechs/)
- [arXiv: Blockchain and Carbon Markets, Standards Overview](https://arxiv.org/pdf/2403.03865)
