# Sistema MRV para transporte: análise de viabilidade

> Status: **análise inicial, sem validação de mercado.** As estimativas de custo e prazo são ordens de grandeza.

## 1. Conclusão curta

**Vale a pena, mas como software que lê dados que já existem (dMRV), e não como hardware de medição.** E só depois de alguns clientes de consultoria confirmarem a demanda.

## 2. "Medição real" de emissões: o que é aceito

- Em combustão (caminhões, caldeiras, fornos), o método aceito pelo GHG Protocol, pela ISO 14083 e pelos mercados regulados é **calcular a partir do combustível consumido**: litros × fator de emissão. Para veículos, esse método é mais preciso e mais barato do que medir o gás no escapamento.
- Medição direta na chaminé (CEMS, monitoramento contínuo) existe para indústrias grandes, mas é exceção e não se aplica a frotas.
- Por isso, **"comprovar volume" significa comprovar os dados de entrada**: quanto combustível foi comprado e consumido, quantos quilômetros foram rodados e quanta carga foi levada, e para quem. Também é preciso uma trilha de auditoria que um verificador independente aceite.

**Conclusão:** o valor está na **rastreabilidade dos dados**, e não em sensores. Desenvolver hardware próprio seria caro e colocaria o projeto contra empresas de telemetria já consolidadas. O melhor é **integrar** com elas.

## 3. A vantagem brasileira: documentos fiscais eletrônicos

O Brasil tem algo que poucos países têm: **documentos fiscais eletrônicos obrigatórios e estruturados**.

| Documento | O que fornece para o cálculo |
|---|---|
| **NF-e de combustível** (postos, cartão-combustível) | Litros, tipo de combustível, data, placa (quando informada) |
| **CT-e** (Conhecimento de Transporte eletrônico) | **Tomador, ou seja, o cliente**, peso da carga, origem e destino, valor |
| **MDF-e** (Manifesto de Documentos Fiscais) | Viagem, veículo, conjunto de CT-e, percurso |
| Telemetria / tacógrafo / TMS | Quilometragem real, consumo, rota, ociosidade |

Combinando esses dados, o sistema calcula **automaticamente e com evidência documental**:
- o inventário da transportadora (Escopo 1, com o diesel e a mistura de biodiesel brasileira tratados corretamente);
- a **emissão atribuída a cada cliente** (kgCO₂e e kgCO₂e por t·km, conforme ISO 14083/GLEC);
- a intensidade por veículo, motorista e rota, que é a base do plano de redução.

As plataformas estrangeiras (ShipZero, EcoTransIT, Dcycle etc.) **não leem CT-e, MDF-e e NF-e brasileiros**. Essa integração local é a **barreira de entrada** do produto.

## 4. Quem compra e por quê

| Cliente | Dor | Disposição a pagar |
|---|---|---|
| Transportadora média (30 a 500 veículos) | Clientes pedindo dados de emissão; quer diferencial em concorrência; quer reduzir diesel | Média. Precisa de preço acessível e de retorno via economia de combustível |
| Embarcador (indústria, varejo, agro) | Escopo 3 do frete com dados ruins; metas de redução | Alta. Pode pagar a plataforma para todos os seus transportadores |
| Operador logístico grande | Já tem demanda de clientes multinacionais | Alta, mas exige mais funcionalidades |

## 5. E o MRV para as instalações reguladas pelo SBCE?

É **outro mercado**: indústrias acima de 10 mil tCO₂e (cimento, siderurgia, química, papel e celulose, refino). Os contratos são maiores, mas:
- o ciclo de venda é longo e os clientes são exigentes;
- a concorrência é forte (SAP, Enablon/Wolters Kluwer, Sphera, WayCarbon, grandes consultorias);
- as regras de MRV do SBCE **ainda estão em consulta pública**.

**Recomendação:** não começar por aqui. Acompanhar a regulação e reavaliar em 2027 ou 2028. O motor de cálculo e a trilha de auditoria do produto de transporte podem ser reaproveitados.

## 6. Riscos

- **Construir antes de vender.** É o erro mais comum. Mitigação: vender consultoria primeiro e automatizar o que se repete.
- **Concorrência das empresas de telemetria**, que podem lançar um módulo de carbono. Mitigação: virar parceiro delas, porque o diferencial está em metodologia, CT-e e relatório por cliente.
- **Aceitação pelos verificadores.** Mitigação: desenhar a trilha de auditoria seguindo a ISO 14064-3 e envolver um verificador (OVV) desde o início.
- **Dados ruins na origem** (placa ausente na NF-e, abastecimento em posto externo). Mitigação: regras de conciliação e indicadores de qualidade do dado.

## 7. Caminho recomendado, em fases

| Fase | O que fazer | Gatilho para avançar |
|---|---|---|
| 0. Consultoria manual | Planilha ISO 14083 e importação manual de CT-e e NF-e (XML) para 3 a 5 transportadoras piloto | Clientes pagando e pedindo recorrência |
| 1. Ferramenta interna | Scripts que leem os XMLs e geram os relatórios. Reduz horas de consultoria por cliente | Mais de 10 clientes ou um embarcador patrocinador |
| 2. MVP SaaS | Portal da transportadora com upload de XML, painel, relatório por cliente e exportação para o verificador | Receita recorrente cobrindo o desenvolvimento |
| 3. Integrações | APIs de cartão-combustível, telemetria e TMS; portal do embarcador | Parcerias firmadas |
| 4. Expansão | Outros modos (ferroviário, cabotagem), armazéns e, eventualmente, MRV para o SBCE | Tração comprovada |

**Ordem de grandeza (a validar):** o MVP da fase 2 pede algo como 3 a 6 meses com 1 ou 2 desenvolvedores, mais um especialista em metodologia. As fases 0 e 1 têm custo baixo e podem começar já.

## 8. Próximo passo concreto

Construir o **motor de cálculo da fase 0/1**: ler CT-e e NF-e (XML), aplicar os fatores de emissão brasileiros e gerar o relatório por cliente. Esse motor serve ao mesmo tempo para a consultoria, para o futuro SaaS e como material de curso.
