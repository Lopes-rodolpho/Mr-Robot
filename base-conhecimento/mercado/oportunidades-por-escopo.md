# Oportunidades de monitoramento por escopo

> Status: **análise inicial (out/2026).** Ideias para validar com clientes.

## Conceito-chave: a emissão do pequeno fornecedor não fica "fora do controle"

As emissões do pequeno fornecedor **já entram no inventário da grande empresa**, no Escopo 3, mas como **estimativa**: valor gasto × fator médio do setor. Os problemas dessa estimativa são:
1. **É imprecisa**: o fornecedor eficiente e o ineficiente recebem o mesmo número.
2. **Não permite mostrar redução**: o número só cai se a empresa comprar menos, mesmo que o fornecedor melhore.
3. **Não serve para decidir**: não mostra de quais fornecedores deveria comprar.

A oportunidade é **transformar estimativa em dado real (primário)** e **dado real em redução**. E a escala é muito maior que 10 fornecedores: uma multinacional tem **milhares**, e o Escopo 3 costuma representar de 70% a 97% das emissões dela (97% no caso da Microsoft).

O limite de 10 mil tCO₂e é do **SBCE** (instalações reguladas). O Escopo 3 é relatado de forma voluntária ou por exigência de mercado, e **não tem limite mínimo**.

## Escopo 1: emissões diretas

| Oportunidade | Detalhe | Clientes |
|---|---|---|
| **Combustível de frota e equipamentos** | Controle por NF-e, cartão-combustível e telemetria (tese das transportadoras) | Transportadoras, construtoras, agro, mineração |
| **Vazamento de gás refrigerante** ⭐ | Fluidos HFC têm efeito estufa até milhares de vezes maior que o CO₂. Em **supermercados e na cadeia fria**, os vazamentos podem ser parte relevante do Escopo 1 e quase ninguém monitora. Envolve controle de recargas, detecção de vazamento e troca de fluido | Supermercados, frigoríficos, centros de distribuição refrigerados, shoppings, hospitais |
| **Metano** | Detecção em aterros, estações de esgoto, biodigestores e pecuária, com sensores, drones ou satélite | Concessionárias de saneamento, aterros, agroindústria |
| **Caldeiras e fornos** | Consumo de lenha, gás e óleo. Troca de combustível por biomassa ou biometano | Indústria de alimentos, têxtil, cerâmica |

## Escopo 2: energia comprada

- No Brasil, a **rede elétrica é muito limpa**, então o Escopo 2 costuma ser **pequeno**. É a menor oportunidade dos três.
- Nichos que restam:
  - **Certificados de energia renovável (I-REC)** e migração para o **mercado livre de energia**.
  - **Correspondência horária** (energia limpa medida hora a hora), tendência entre big techs e **data centers**. O Brasil atrai data centers justamente pela matriz limpa.
  - Eficiência energética, que se justifica mais pelo custo do que pelo carbono.

## Escopo 3: cadeia de valor (a maior oportunidade)

### Ideia 1: plataforma de dois lados, "o grande paga, o pequeno informa" ⭐⭐⭐

Uma resposta a "atuar no pequeno ou no grande?": **nos dois, com o grande pagando**.

- **A grande empresa** contrata a plataforma e convida seus fornecedores.
- **O pequeno fornecedor** usa de graça ou quase de graça: uma calculadora simples, em português, pensada para quem não tem equipe de sustentabilidade, que gera o inventário dele.
- **O dado sobe automaticamente** para o inventário da grande empresa, com rastreabilidade.
- **Efeito de rede**: o fornecedor informa uma vez e compartilha com todos os clientes dele, como um "cadastro positivo do carbono". Cada novo fornecedor torna a plataforma mais valiosa para todos os compradores.
- **A dor é comprovada**: a nota técnica da CVM sobre a Resolução 193 (nov/2025) registra que as companhias abertas têm dificuldade de engajar fornecedores, especialmente pequenas e médias empresas, no Escopo 3.

**Concorrentes globais:** CDP Supply Chain (cerca de 45 mil fornecedores e mais de 270 compradores), EcoVadis Carbon, Terrascope, Normative, CO2 AI. Os padrões de troca de dados são o **PACT** (WBCSD) e o **Catena-X** (setor automotivo).
**Brecha:** são caros, em inglês e baseados em questionários. Não falam com o pequeno fornecedor brasileiro e **não usam os documentos fiscais eletrônicos brasileiros**.

### Ideia 2: Escopo 3 automático a partir da NF-e ⭐⭐⭐

Toda compra no Brasil gera uma **NF-e com código NCM, quantidade, peso e fornecedor**. Um sistema que lê as notas de compra da empresa pode:
- calcular automaticamente a **categoria 1** (bens comprados) por massa ou por produto, e não apenas pelo valor gasto;
- calcular a **categoria 4** (frete) com os CT-e;
- montar o **ranking dos fornecedores que mais pesam**, indicando onde vale engajar (normalmente poucos fornecedores concentram a maior parte das emissões);
- servir de **porta de entrada** para a Ideia 1, convidando os fornecedores que mais pesam a enviar dados reais.

É **difícil de copiar** por estrangeiros e usa a mesma base técnica do motor de MRV de transporte (leitura de XML fiscal).

### Ideia 3: dados de carbono para exportadores (CBAM) ⭐⭐⭐

- O **CBAM** (taxa de carbono na fronteira da União Europeia) está em **fase definitiva desde 1º/01/2026**. Os importadores europeus de **aço, ferro-gusa, ferro-ligas, alumínio, cimento e fertilizantes** compram certificados conforme as emissões embutidas no produto. A primeira liquidação ocorre em 2027, retroativa a 2026.
- **Exportadores que não fornecem dados reais** são taxados por **valores-padrão europeus, geralmente mais altos**. Logo, dado real tem **valor em dinheiro direto**.
- Muitos exportadores são **pequenos e médios**, como os **guseiros de Minas Gerais**. É exatamente o fornecedor pequeno pressionado pelo comprador grande, e aqui **com obrigação legal e efeito financeiro**.
- O serviço: cálculo da pegada por produto, relatório no formato CBAM e verificação.

### Ideia 4: financiamento atrelado ao carbono

- Parceria com banco ou fintech de **antecipação de recebíveis** (*supply chain finance*): o fornecedor que informa e reduz emissões ganha **taxa menor** para antecipar o que tem a receber da grande empresa.
- O fornecedor ganha um **incentivo financeiro concreto** para participar, o que resolve o problema do "pequeno que não se preocupa".

### Ideia 5: programas setoriais de redução (insetting)

- A grande empresa financia a redução **dentro da própria cadeia** (biodigestor no fornecedor de suínos, caminhão a biometano na transportadora, pó de rocha na fazenda de soja) e contabiliza no próprio Escopo 3. Exemplo: Minerva, Athian e Rumin8 na pecuária.
- Nosso papel seria **estruturar, medir e verificar** esses programas, agregando muitos fornecedores pequenos.

## Avaliação

| Ideia | Dor comprovada | Quem paga | Concorrência no Brasil | Sinergia com o que já temos |
|---|---|---|---|---|
| 1. Plataforma de dois lados | Alta | Grande empresa | Média (estrangeiros) | Alta |
| 2. Escopo 3 via NF-e | Alta | Grande e média empresa | Baixa | Muito alta (motor XML) |
| 3. CBAM exportadores | Alta, com prazo legal | Exportador | Média, crescendo | Média |
| 4. Financiamento | Média | Banco / fintech | Baixa | Média |
| 5. Insetting | Média e crescente | Grande empresa | Baixa | Alta (metano, transporte) |
| Escopo 1: refrigerantes | Média | Supermercados, cadeia fria | Baixa | Média |

**Sugestão de foco:** juntar as ideias **2 + 1**. Começar pelo Escopo 3 automático via NF-e, vendido à grande empresa, e usá-lo para puxar os fornecedores para a plataforma. O **transporte** (CT-e) é o primeiro módulo da cadeia, o que conecta com a tese das transportadoras.

## Fontes

- [CVM: Nota Técnica sobre a Resolução 193 (nov/2025)](https://www.gov.br/cvm/pt-br/assuntos/noticias/anexos/2025/20251124-nota-tecnica-pesquisa-resolucao-cvm-193.pdf)
- [CDP: Scope 3, primary data and supplier engagement](https://cdn.cdp.net/cdp-production/comfy/cms/files/files/000/008/036/original/Scope_3_-_implementing_primary_data_and_supplier_engagement_strategies.pdf)
- [EcoVadis Carbon](https://ecovadis.com/solutions/carbon/)
- [Terrascope: Scope 3 supplier engagement](https://www.terrascope.com/scope-3-supplier-engagement)
- [Normative: Scope 3 supplier engagement](https://normative.io/insight/scope-3-supplier-engagement/)
- [CO2 AI: dados de carbono e contratos de fornecedores](https://co2ai.com/insights/cpg-scope-3-emissions-suppliers-why-your-carbon-data-determines-your-contracts)
- [Carbonova: CBAM para exportadores brasileiros](https://carbonova.ai/cbam-exportadores-brasileiros)
- [Monitore: CBAM em vigor](https://www.monitore.com.br/post/cbam-em-vigor-como-calcular-emiss%C3%B5es-embutidas-na-exporta%C3%A7%C3%A3o)
- [Instituto Multiplicidades: CBAM e o Brasil](https://multiplicidades.org.br/cbam-e-o-brasil-como-o-mecanismo-de-ajuste-de-carbono-na-fronteira-pode-transformar-a-industria-nacional-em-oportunidade-competitiva/)
