# Modelo de negócio: "MRV pronto para auditoria"

> Status: proposta (out/2026). Preços são hipóteses a validar. Base normativa em `base-conhecimento/regulatorio/cadeia-de-confianca-mrv.md`.

## 1. Posicionamento

**Somos o lado do cliente na cadeia de confiança.** Cuidamos da **medição** (camada 1) e do **monitoramento e relato** (camada 2), e entregamos ao **verificador independente** (camada 3) tudo pronto para auditar.

> **Proposta de valor:** "Seu biogás medido, calculado e documentado de forma que qualquer verificador acreditado aprove na primeira rodada. Mais créditos, certificados emitidos mais rápido e auditoria mais barata."

### Por que não ser o verificador?

| Opção | Prós | Contras | Decisão |
|---|---|---|---|
| **Lado do cliente** (equipamento + MRV + consultoria) | Receita recorrente, venda de hardware, relação longa, sem exigência de acreditação | Concorrência de consultorias | ✅ **Escolhido** |
| **Ser verificador (OVV)** | Demanda crescente com o SBCE e capacidade escassa | Exige acreditação ISO 14065 pelo Inmetro (processo longo), **proíbe vender equipamento e consultoria aos mesmos clientes**, concorrência com SGS, BV e Intertek | ❌ Incompatível com o modelo. Reavaliar no futuro como empresa **totalmente separada** |

## 2. A oferta, em módulos

| Módulo | Camada | O que entrega | Como cobra (hipótese) |
|---|---|---|---|
| **M1. Medição** | 1 | Venda ou comodato do medidor (ex.: OPTISONIC 7300 Biogas, via Conaut), projeto de instalação, comissionamento | Margem ou comissão no equipamento; ou mensalidade de comodato |
| **M2. Gestão metrológica** | 1 | Plano de calibração, agenda, certificados de laboratório acreditado (RBC), registro de manutenção, alertas de vencimento | Mensalidade por ponto de medição |
| **M3. Plataforma de MRV** | 2 | Coleta automática e assinada, trilha de auditoria, cálculo (inventário, metano evitado, CGOB, CBIO, I-REC), controle contra dupla contagem, painéis | **Assinatura mensal** por planta ou ponto de medição |
| **M4. Plano de monitoramento e relatórios** | 2 | Plano de monitoramento (SBCE ou metodologia de crédito), inventário GHG Protocol/ISO 14064-1, relatórios para ANP e certificadores | Projeto (preço fechado) + renovação anual |
| **M5. Preparação para auditoria** | 2→3 | "Pacote de evidências" para o verificador, acompanhamento da auditoria, tratamento de não conformidades | Por ciclo de verificação |
| **M6. Monetização de atributos** (opcional) | após a 3 | Apoio para vender créditos, CGOB ou CBIO (sem ser corretora regulada) | **Percentual sobre a receita** de certificados (*success fee*) |

**Pacotes:**
- **Essencial:** M3 + M4. Para quem já tem medidor (caso da Sabesp em Barueri).
- **Completo:** M1 + M2 + M3 + M4 + M5. Para quem começa do zero.
- **Sem desembolso:** M1 em comodato + M2 + M3 + M6, remunerado **por parte dos créditos**. Para cooperativas e plantas médias.

## 3. Ecossistema de parceiros

| Parceiro | Papel | Regra de relacionamento |
|---|---|---|
| **Fabricante/distribuidor de medidores** (Conaut/KROHNE e outros) | Equipamento, suporte técnico | Parceria comercial (revenda, representação ou integração). **A plataforma aceita outras marcas** |
| **Laboratório de calibração acreditado (RBC)** | Certificados de calibração | Contratado por nós ou pelo cliente |
| **Instalador ou integrador elétrico** | Instalação em área classificada | Subcontratado |
| **Verificadores** (OVV, firma inspetora ANP, certificador CGOB, VVB) | Auditoria independente | **Sem comissão e sem exclusividade.** O cliente escolhe e contrata diretamente. Nós apenas facilitamos |
| **Bancos e Fundo Clima** | Financiamento do comodato e dos projetos | Parceria para estruturar crédito |

## 4. Exemplo de proposta: Sabesp, piloto em 5 ETEs (ilustrativo)

| Item | Escopo | Observação |
|---|---|---|
| Diagnóstico | Mapa de biogás e medição existente; como o metano entra hoje no inventário | Preço fechado |
| M1/M2 | Aproveitar os medidores existentes (Barueri) e instalar onde faltar, com calibração em dia | Equipamento via Conaut |
| M3 | Plataforma conectada às 5 ETEs: biogás medido, metano capturado, destruído ou usado, comparação com o fator padrão | Assinatura |
| M4/M5 | Seção de metano das ETEs no inventário com dado primário; pacote de evidências para o OVV da Sabesp | O OVV continua o mesmo que a Sabesp já contrata |
| Resultado esperado | Dado medido para a meta de 2035, base para CGOB, CBIO e I-REC dos projetos de biometano | Decisão sobre expansão para outras ETEs |

## 5. Riscos e mitigação

| Risco | Mitigação |
|---|---|
| Conflito de interesse percebido | Política escrita de independência: não atuar como verificador, não receber comissão de verificadores, cliente contrata a auditoria diretamente |
| Dependência de um único fabricante | Plataforma aberta a várias marcas e protocolos |
| Regras do SBCE ainda em consulta | Arquitetura flexível. Começar por inventário corporativo, créditos voluntários e certificados da ANP, que já têm regras |
| Responsabilidade por erro de cálculo | Seguro de responsabilidade profissional, metodologia documentada, revisão por especialista e, naturalmente, a verificação independente |
| Ciclo de venda longo em grandes empresas | Piloto pequeno e pago com escopo fechado. Usar casos existentes (Conaut em Barueri) |

## 6. Próximos passos

1. Validar o modelo com a **Conaut** (tipo de parceria, margens, se eles têm laboratório acreditado para calibração).
2. Conversar com **um OVV** (ex.: Totum, SGS, ABNT) para entender o que eles mais sentem falta nos dados dos clientes. Isso define o conteúdo do "pacote de evidências" (M5).
3. Ler as **Resoluções ANP 984/2025 e 995/2026** para confirmar as regras de credenciamento e conflito de interesse de firmas inspetoras e certificadores.
4. Acompanhar a **portaria de MRV do SBCE** (consulta pública do Ministério da Fazenda).
