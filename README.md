# Lume — Fluxo de Preparação, Limpeza e Modelagem de Dados

Projeto de engenharia e preparação de dados desenvolvido no **Tableau Prep Builder**, focado na higienização, padronização e estruturação de uma base de dados fictícia construída para refletir com alta fidelidade o comportamento e as regras de negócio reais do mercado.

## Sobre o projeto

No dia a dia corporativo, bases de dados brutas extraídas de planilhas frequentemente apresentam inconsistências — como valores nulos, registros duplicados, tipagens incorretas e formatos não padronizados — que comprometem a confiabilidade das análises gerenciais e dos painéis de Business Intelligence.

O **Lume** propõe um pipeline completo de preparação e tratamento de dados utilizando fluxos do **Tableau Prep** (`.tflx`). A partir de uma base em Excel (`Lume_v3.xlsx`) que simula cenários reais de mercado, o projeto aplica etapas sistemáticas de auditoria, limpeza e transformação para entregar dados íntegros, prontos para visualização analítica e tomada de decisão.

## Produto esperado

Fluxo estruturado e reproduzível de preparação de dados empacotado em **Tableau Prep Builder** (`Lume_ProjetoVFinal.tflx`), contendo a base de entrada integrada, as etapas de limpeza e padronização documentadas visualmente no grafo de fluxo e a saída pronta para análise.

> Não fazem parte do escopo: ingestão de dados em tempo real via APIs externas e implementação de modelos preditivos em produção. A base de dados (`Lume_v3.xlsx`) é estática e simulada, mantendo alta fidelidade às métricas e estruturas do mercado.

## Etapas do Fluxo (Data Prep)

O desenvolvimento do pipeline no **Tableau Prep** foi estruturado nas seguintes etapas:

| Etapa | Atividades Realizadas | Artefato no Fluxo |
|---|---|---|
| **1. Ingestão e Diagnóstico** | Conexão com a planilha base (`Lume_v3.xlsx`), mapeamento de colunas, identificação de nulos, outliers e duplicidades. | Etapa de Entrada (*Input Step*) |
| **2. Limpeza e Padronização** | Remoção de registros duplicados, tratamento de valores ausentes, uniformização de categorias textuais e ajuste de tipos de dados. | Etapas de Limpeza (*Clean Steps*) |
| **3. Transformação e Regras** | Criação de campos calculados, padronização de métricas de mercado e estruturação de chaves para análise. | Campos Calculados e Agrupamentos |
| **4. Consolidação e Saída** | Validação final da integridade da base tratada e empacotamento do fluxo completo com os dados embutidos. | `Lume_ProjetoVFinal.tflx` |

**Ferramentas e arquivos utilizados:** Tableau Prep Builder (`.tflx`), Microsoft Excel (`.xlsx`) e Git/GitHub para versionamento.

## Estrutura do Repositório

Com base nos arquivos presentes no repositório `Lume-S2`:

```text
Lume-S2-main/
├── .gitattributes             # Configurações de controle de linha e atributos do Git[cite: 1]
├── LICENSE                    # Licença de uso e distribuição do projeto[cite: 1]
├── Lume_ProjetoV4.tflx        # Versão intermediária do fluxo empacotado no Tableau Prep[cite: 1]
├── Lume_ProjetoVFinal.tflx    # Versão final consolidada do fluxo no Tableau Prep (com Lume_v3.xlsx embutido)[cite: 1]
└── README.md                  # Documentação do projeto
