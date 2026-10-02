# Cadeia de confiança no MRV: quem mede, quem relata, quem verifica

> Status: análise (out/2026). Itens "a confirmar" devem ser checados no texto das normas.

## 1. A lógica é a mesma da metrologia de água e gás

Nos mercados de água, gás e petróleo, a confiança na medição vem de **camadas separadas**:

| Mercado | Norma de medição | Quem garante |
|---|---|---|
| **Água (tarifação)** | **Portaria Inmetro 155/2022**: Regulamento Técnico Metrológico (RTM) de medidores de água fria e quente. Passou a admitir medidores **ultrassônicos e eletromagnéticos** | Aprovação de modelo e verificação pelo Inmetro e pelos IPEMs |
| **Gás natural, biometano e GLP (comercialização)** | **Portaria Inmetro 156/2022**: RTM de medidores de vazão de gás natural, **biometano** e GLP em fase gasosa | Inmetro/IPEM |
| **Petróleo e gás (medição fiscal)** | **Resolução Conjunta ANP/Inmetro nº 1/2013**: Regulamento Técnico de Medição (em revisão) | ANP aprova o sistema de medição; Inmetro cuida da metrologia |

Essas normas são de **metrologia legal**: valem quando a medição define **cobrança ou tributo** (transferência de custódia, conta de água, royalties).

## 2. Para emissões (MRV), a cadeia tem três camadas

```
CAMADA 1: MEDIÇÃO              CAMADA 2: MONITORAMENTO E RELATO     CAMADA 3: VERIFICAÇÃO
(o número é confiável?)        (o cálculo e o processo estão         (um terceiro confirma?)
                                corretos?)
Equipamento adequado           Plano de monitoramento               Organismo independente
+ calibração rastreável        + coleta, QA/QC, cálculo              ACREDITADO
  (laboratório RBC,            + relatório                          - Inventário: OVV (ISO 14065,
  ISO/IEC 17025)                                                      acreditado pelo Inmetro/Cgcre)
+ metrologia legal, se         Responsável: a empresa (operador)    - SBCE: organismo de inspeção
  houver venda                 ou quem ela contrata                   acreditado (Lei 15.042)
  (Portaria 156/2022, RTM                                           - RenovaBio: firma inspetora
  ANP/Inmetro)                 ⇒ NÃO precisa ser independente.        credenciada na ANP
                                 É o lugar do consultor e do        - CGOB: certificador credenciado
                                 provedor de MRV                      na ANP
                                                                    - Créditos voluntários: VVB
                                                                      (Verra, Gold Standard)
                                                                    ⇒ PRECISA ser independente
```

## 3. Normas por camada

### Camada 1: medição

- **Calibração rastreável:** as metodologias de carbono e os planos de monitoramento exigem instrumentos calibrados, conforme o fabricante ou as normas, com rastreabilidade metrológica. No Brasil, isso significa **laboratórios acreditados pela Cgcre/Inmetro (RBC, ABNT NBR ISO/IEC 17025)**.
- **Metrologia legal** só se aplica quando há **transação comercial**. Por exemplo, o **biometano vendido** na rede da Comgás segue o RTM ANP/Inmetro e a Portaria 156/2022. **O biogás bruto medido para calcular emissões normalmente não está sujeito à metrologia legal**, mas precisa de calibração rastreável (a confirmar caso a caso no plano de monitoramento).

### Camada 2: monitoramento e relato

- **SBCE (Lei 15.042/2024):** o operador deve apresentar um **plano de monitoramento** ao órgão gestor e **relatórios de emissões e remoções** conforme o plano aprovado.
- **Inventário corporativo:** GHG Protocol e **ABNT NBR ISO 14064-1**.
- **Biometano e biocombustíveis:** regras de cálculo da ANP (RenovaBio, CGOB).
- **Nenhuma dessas normas impede que um consultor ou provedor de tecnologia faça esta camada.** É o modelo usual de mercado.

### Camada 3: verificação (onde a independência é obrigatória)

| Regime | Quem verifica | Base |
|---|---|---|
| Inventário corporativo (GHG Protocol, ISO 14064) | **OVV**, Organismo de Verificação de Inventários de GEE, **acreditado pelo Inmetro/Cgcre** | **ABNT NBR ISO 14065** (requisitos de imparcialidade e competência), ISO 14064-3 (processo de verificação), ISO 14066 (competência das equipes) |
| **SBCE** | "Avaliação da conformidade **por organismo de inspeção acreditado**", conforme ato do órgão gestor. Créditos (CRVE) **verificados por entidade independente** | Lei 15.042/2024. A regulamentação de MRV está em consulta pública |
| RenovaBio (CBIO) | **Firma inspetora credenciada pela ANP** | Res. ANP 984/2025 (substituiu a 758/2018). As regras de conflito de interesse precisam ser confirmadas no texto |
| CGOB (biometano) | **Agente certificador credenciado pela ANP** | Lei 14.993/2024, Res. ANP 995/2026 |
| Créditos voluntários | **VVB** (organismo de validação e verificação) aprovado pelo padrão | Regras da Verra e da Gold Standard, ISO 14065 |

**Princípio da ISO 14065 (imparcialidade):** o verificador **não pode verificar algo que ele mesmo projetou, calculou ou prestou consultoria**. A norma chama isso de ameaça de *autorrevisão*. Por isso:
- **nós** (equipamento, plataforma, consultoria) **não podemos ser o verificador** dos nossos clientes;
- **o verificador também não pode vender consultoria** para o mesmo cliente e o mesmo escopo.

Exemplos de OVVs e certificadoras no Brasil: SGS, Bureau Veritas, Intertek, Instituto Totum, ABNT e KPMG (RenovaBio).

## 4. Consequências práticas para o nosso negócio

1. **Podemos legalmente** vender o medidor, instalar, gerir a calibração, operar a plataforma de MRV, preparar o plano de monitoramento, o inventário e os relatórios, e apoiar a certificação.
2. **Não podemos** ser o OVV, a firma inspetora ou o certificador dos mesmos clientes.
3. **Devemos evitar** receber comissão de verificadores por indicação de clientes, porque isso compromete a imparcialidade percebida.
4. **Diferencial:** entregar ao verificador um **"pacote pronto para auditoria"** (dados assinados, trilha de auditoria, certificados de calibração, memória de cálculo). Isso reduz o custo e o prazo da verificação para o cliente.

## Fontes

- [Inmetro: Portaria 155/2022 (medidores de água)](http://www.inmetro.gov.br/legislacao/detalhe.asp?seq_classe=1&seq_ato=2971)
- [Conaut: a Portaria Inmetro 155/2022 e os medidores de água](https://www.conaut.com.br/blog/nova-portaria-inmetro)
- [Inmetro: AIR sobre medidores de gás natural (Portaria 156/2022)](https://www.gov.br/inmetro/pt-br/assuntos/regulamentacao/analise-de-impacto-regulatorio/dispensas-de-air/2024/medidores-de-gas-natural/relatorio)
- [ANP: gasodutos, normas e legislação aplicáveis (RTM ANP/Inmetro)](https://www.gov.br/anp/pt-br/assuntos/movimentacao-estocagem-e-comercializacao-de-gas-natural/transporte-de-gas-natural/gasodutos-de-transporte-normas-e-legislacao-aplicaveis)
- [eixos: nova resolução da ANP sobre especificação do biometano](https://eixos.com.br/gas-natural/biogas/nova-resolucao-da-anp-abre-espaco-para-flexibilizar-especificacao-do-biometano/)
- [Inmetro: acreditação de OVV de inventários de GEE](http://www.inmetro.gov.br/credenciamento/acre_org_estufa.asp)
- [ABNT: Programa de Verificação de Inventário de GEE](https://portaldasustentabilidade.abnt.org.br/programa-de-verificacao-de-inventario-de-gee/)
- [SGS: como o inventário de GEE é verificado (ISO 14064)](https://www.sgs.com/pt-br/noticias/2026/03/como-o-inventario-de-geee-verificado-guia-completo-da-iso-14064)
- [RBNA: verificação de inventário de GEE, guia 2026 (SBCE, ISO 14064, ISO 14065)](https://rbnaconsult.com/verificacao-auditoria-de-inventario-de-gee-guia-completo-2026-sbce-iso-14064-e-iso-14065/)
- [Planalto: Lei 15.042/2024](https://www.planalto.gov.br/ccivil_03/_ato2023-2026/2024/lei/l15042.htm)
- [ANP: nova resolução de certificação do RenovaBio](https://eixos.com.br/combustiveis-e-bioenergia/biocombustiveis/anp-publica-resolucao-com-atualizacao-de-regras-de-certificacao-no-renovabio/)
