# Projeto paralelo: biogás e biometano

> Status: **versão 2 (out/2026)**, com 120 registros: pesquisa web + Panorama do Biogás 2025 (CIBiogás). A base ainda **não é exaustiva**: veja a seção "Lacunas".

## Arquivos

| Arquivo | Conteúdo |
|---|---|
| `empresas.csv` | Base de dados das empresas da cadeia (120 registros). Separador `;`, abre direto no Excel |
| `estados-panorama-2025.csv` | Dados por estado (plantas, volume, uso), do Panorama CIBiogás 2025 |
| `ficha-panorama-cibiogas-2025.md` | Resumo detalhado do Panorama do Biogás 2025 (CIBiogás) |
| `oportunidades-de-solucao.md` | 6 soluções propostas a partir dos dados, com priorização |
| `README.md` | Este resumo: panorama do setor, mapa da cadeia, lacunas e próximos passos |

### Colunas da base

`empresa` · `elo_cadeia` · `categoria` · `fonte_materia_prima` · `uf` · `municipio_ou_area` · `descricao` · `capacidade_ou_porte` · `status` · `socios_parceiros` · `confianca` (Alta/Média/Baixa) · `fonte` (link)

**Confiança:** *Alta* indica fonte jornalística ou oficial específica. *Média* indica fonte indireta ou dado parcial. *Baixa* indica empresa apenas citada, ainda a verificar.

## Panorama do setor (números de 2025-2026)

- Dados oficiais detalhados em `ficha-panorama-cibiogas-2025.md`.
- **1.803 plantas de biogás** cadastradas no Brasil (2025; 1.727 em operação), com produção próxima de **5 bilhões de Nm³ por ano**. Do biogás, **62% vai para eletricidade**, **34% para biometano** e o restante para calor.
- **Biometano**: **21 plantas autorizadas pela ANP** (jul/2026), com **1,37 milhão de Nm³ por dia**. Há mais **48 em autorização** (cerca de 2 milhões de Nm³ por dia).
- O planejamento do setor identifica **127 projetos adicionais**, o que poderia levar a oferta a **cerca de 8 milhões de m³ por dia em 2030**. A expectativa é de **R$ 25 bilhões de investimento até 2030**.
- **São Paulo lidera**, com 8 plantas de biometano e cerca de 500 mil m³ por dia, seguido por RJ, PR e MG.
- **Mandato do Combustível do Futuro**: a mistura obrigatória de biometano no gás natural começou em 2026. ⚠️ As fontes divergem quanto ao percentual de 2026 (0,5% ou 1%) e precisam ser confirmadas na resolução do CNPE.
- **RenovaBio**: apenas **6 das 19 plantas de biometano** estavam certificadas em fev/2026. **É um sinal de oportunidade de serviço.**

## Mapa da cadeia

```
MATÉRIA-PRIMA            PRODUÇÃO                 TECNOLOGIA / EQUIPAMENTOS
Aterros sanitários  ──►  Gás Verde, Orizon,       Biodigestores: Sansuy, Biokohler,
Vinhaça / torta     ──►  Ecometano, CRVR,         Methanum, Bazico, ER-BR, Geo
Dejetos suínos      ──►  Raízen, Cocal, ZEG,      Upgrading: Greenlane/Panasonic,
Esgoto (ETE)        ──►  H2A, Primato, Sabesp     Evonik, Air Liquide, Bright, Roeslein
Resíduos industriais                              Motores: MWM, Jenbacher, WEG
                              │
                              ▼
LOGÍSTICA / COMERCIALIZAÇÃO              CONSUMO
Gasoduto virtual: Galileo, Neogás,  ──►  Indústrias off-grid, distribuidoras
CTG. Traders: Edge/Compass,              (Copergás, Cegás, Gasmig, Sulgás),
Ultragaz, Vibra, Copersucar,             frotas (Scania, Iveco: ReiterLog,
Petrobras                                Transvale, Marquise, Atvos)
                              │
                              ▼
CERTIFICAÇÃO / SERVIÇOS: KPMG, Instituto Totum (RenovaBio), AFRY (engenharia)
INSTITUIÇÕES: Abiogás, CIBiogás, GEF Biogás Brasil, B2Biogas (diretório)
```

## Distribuição da primeira versão da base (70 registros, antes do Panorama)

| Elo da cadeia | Registros |
|---|---|
| Produção (inclui produção combinada com tecnologia, desenvolvimento ou consumo) | 23 |
| Tecnologia e equipamentos | 23 |
| Comercialização, distribuição e logística | 12 |
| Veículos e consumo | 4 |
| Serviços e instituições | 7 |
| Desenvolvimento | 1 |

## Lacunas: o que falta para a lista ficar "completa"

1. **Lista oficial da ANP** (o Panorama CIBiogás traz os totais, com 59 unidades em mar/2026, mas não os nomes): as 21 plantas autorizadas e as 48 em autorização. Fonte: *Painel Dinâmico de Produtores de Biometano* da ANP. Ele **não pôde ser acessado deste ambiente**, porque o acesso de rede bloqueia vários sites. É preciso baixar manualmente ou liberar o domínio `gov.br`.
2. **Panorama Abiogás** (relatório anual) e **mapa CIBiogás (BiogasMap)**: listam as 1.803 plantas de biogás, inclusive as pequenas.
3. **Diretório B2Biogas**: dezenas de fornecedores (biodigestores, upgrading, motores, engenharia). Também bloqueado aqui.
4. **Lista de firmas inspetoras credenciadas no RenovaBio** e **agentes certificadores do CGOB**, a serem publicados pela ANP.
5. **Empresas de saneamento** (Sanepar, Copasa, Aegea, Iguá, BRK) e **frigoríficos e cooperativas** (BRF, Aurora, JBS, Lar, C.Vale) com projetos de biogás.
6. **Fabricantes de compressores, flares, analisadores de gás e medidores**, que são justamente os equipamentos de MRV.

## Ligações com o projeto principal (gestão de emissões)

| Oportunidade | Ligação |
|---|---|
| **Certificação RenovaBio e CGOB** | Só 6 de 19 plantas estão certificadas. Assessoria de certificação e MRV |
| **Agregação de pequenos produtores** (suínos, cooperativas) | Créditos de carbono de metano evitado (PoA). Exemplo: COOASGO com Cargill |
| **Transporte a biometano** | Liga com a tese das transportadoras: inventário, ISO 14083 e insetting |
| **Financiamento** (Fundo Clima, BNDES) | Assessoria de crédito verde para biodigestores e frotas |
| **Curso e livro** | Quase não há conteúdo de formação sobre a cadeia de biometano no Brasil |

## Próximos passos

- [ ] Completar a base com a lista oficial da ANP (lacuna 1)
- [ ] Incluir colunas de contato (site, LinkedIn, decisor) para uso comercial
- [ ] Classificar cada empresa como **cliente potencial**, **parceiro** ou **concorrente** do nosso projeto
- [ ] Mapear em um mapa interativo (por UF e tipo de matéria-prima)

## Principais fontes

- [Abiogás: 1.803 plantas de biogás (O Presente Rural)](https://opresenterural.com.br/brasil-alcanca-1-803-plantas-de-biogas-e-producao-anual-perto-de-5-bilhoes-de-nm%C2%B3/)
- [Cenário Energia: biogás avança no Brasil](https://cenarioenergia.com.br/2026/04/20/biogas-avanca-no-brasil-com-1-803-plantas-e-impulsiona-nova-fronteira-energetica-com-biometano/)
- [Movimento Econômico: 21 usinas e 48 projetos](https://movimentoeconomico.com.br/petroleo-e-gas/2026/08/12/biometano-ganha-regra-unica-com-21-usinas-instaladas-e-48-projetos-em-expansao/)
- [Cenário Energia: 20 plantas autorizadas](https://cenarioenergia.com.br/2026/06/22/mercado-de-biometano-quintuplica-de-tamanho-e-atinge-marca-de-20-plantas-autorizadas-no-pais/)
- [Cenário Energia: project finance no biometano](https://cenarioenergia.com.br/2026/10/01/mercado-de-biometano-avanca-e-amplia-espaco-para-project-finance-no-brasil/)
- [eixos: mapa de investidores do biometano](https://eixos.com.br/combustiveis-e-bioenergia/biocombustiveis/investidores-se-posicionam-no-biometano-veja-o-mapa-do-mercado-brasileiro/)
- [ANP: apresentação RenovaBio (mar/2026)](https://www.gov.br/anp/pt-br/centrais-de-conteudo/apresentacoes-palestras/2026/arquivos/apresentacao-anp-renovabio-03032026.pdf)
- [ScienceDirect: Biogas upgrading to biomethane in Brazil](https://www.sciencedirect.com/science/article/pii/S2666188825009840)
- Cada empresa tem seu link de fonte na coluna `fonte` do `empresas.csv`.
