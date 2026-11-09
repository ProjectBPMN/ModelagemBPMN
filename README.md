# Modelagem de Processos de Negócio (BPMN 2.0) e Diagnóstico Institucional de BPM no IF Sudeste MG

[![BPMN 2.0](https://img.shields.io/badge/Notation-BPMN%202.0-blue.svg)](https://www.omg.org/spec/BPMN/2.0/)
[![Bizagi](https://img.shields.io/badge/Modeler-Bizagi-brightgreen.svg)](https://www.bizagi.com/)
[![Instituição](https://img.shields.io/badge/Instituição-IF%20Sudeste%20MG-red.svg)](https://www.ifsudestemg.edu.br/)
[![Status](https://img.shields.io/badge/Status-Publicado%20%2F%20Open%20Research-success.svg)](#)

Este repositório reúne os artefatos de pesquisa e modelagem do projeto de **Gerenciamento de Processos de Negócio (Business Process Management - BPM)** aplicado à administração pública educacional, com foco no **Instituto Federal de Educação, Ciência e Tecnologia do Sudeste de Minas Gerais (IFSEMG) - Campus Rio Pomba**.

O acervo é composto por:
1. **Modelagem de Processos (*AS-IS*)**: Levantamento empírico e mapeamento integral na notação **BPMN 2.0** do fluxo de manutenção predial e infraestrutura física do setor de Prefeitura/DEMO (Divisão de Engenharia, Manutenção e Obras).
2. **Diagnóstico Institucional de BPM**: Instrumentos de coleta, planilha tabulada e respostas oficiais (via e-SIC / Lei de Acesso à Informação) sobre a maturidade e adoção de práticas de BPM nas 10 unidades de ensino e na Reitoria do IFSEMG.

---

## 📁 Estrutura do Repositório

```text
.
├── Modelagem/
│   ├── Controle da manutencao e infraestrutura fisica (AS IS).bpm   # Modelo completo no Bizagi Modeler
│   ├── Gestão de Demandas e Execução de Manutenção.png              # Diagrama Macro (Visão Geral)
│   ├── Triagem de chamados.png                                      # Subprocesso 1: Triagem e Qualificação
│   ├── Manutenção Equipe D.E.M.O.png                                # Subprocesso 2: Atendimento Interno (D.E.M.O.)
│   ├── Negociação e Manutenção Sobdemanda.png                       # Subprocesso 3: Orçamento e Contratação
│   ├── Executar Serviço sobdemanda.png                              # Subprocesso 4: Execução Terceirizada
│   └── Documentação e Pagamento.png                                 # Subprocesso 5: Conferência e Liquidação
└── PesquisaBPMnoIFSEMG/
    ├── QUESTIONÁRIO SOBRE GERENCIAMENTO DE PROCESSOS DE NEGÓCIO (BPM) - Questionário.pdf  # Instrumento de coleta
    ├── QUESTIONÁRIO SOBRE GERENCIAMENTO DE PROCESSOS DE NEGÓCIO (BPM)_unidades.xlsx       # Respostas tabuladas por unidade
    ├── INFORMAÇÕES Nº 32492025 - GABREITORI (11.01.01).pdf                                # Parecer do Gabinete da Reitoria
    └── Resposta ao pedido 23546.104950_2025-15.pdf                                        # Resposta oficial LAI / e-SIC
```

---

## 📐 1. Arquitetura dos Processos Modelados (AS-IS)

O fluxo de **Controle da Manutenção e Infraestrutura Física** retrata o ciclo de vida completo de atendimento às demandas de reparos, manutenções rotineiras e serviços prediais no Campus Rio Pomba. A modelagem segue estritamente o padrão internacional **BPMN 2.0 (OMG)**, implementado na ferramenta **Bizagi Process Modeler**.

### 🔹 Visão Geral e Subprocessos

| Artefato | Tipo | Descrição do Fluxo |
|---|---|---|
| [**Controle da manutencao e infraestrutura fisica (AS IS).bpm**](Modelagem/Controle%20da%20manutencao%20e%20infraestrutura%20fisica%20(AS%20IS).bpm) | Arquivo Fonte (Bizagi) | Projeto consolidado contendo todas as piscinas (*pools*), raias (*lanes*), subprocessos e anotações. |
| [**Gestão de Demandas e Execução de Manutenção.png**](Modelagem/Gest%C3%A3o%20de%20Demandas%20e%20Execu%C3%A7%C3%A3o%20de%20Manuten%C3%A7%C3%A3o.png) | Macroprocesso | Fluxo arquitetural integrador: entrada via GLPI, encaminhamento entre as vias interna e terceirizada e controle de entrega. |
| [**Triagem de chamados.png**](Modelagem/Triagem%20de%20chamados.png) | Subprocesso | Recepção e triagem das ordens de serviço: análise de duplicidade, avaliação de viabilidade técnica e direcionamento de fila. |
| [**Manutenção Equipe D.E.M.O.png**](Modelagem/Manuten%C3%A7%C3%A3o%20Equipe%20D.E.M.O.png) | Subprocesso | Atendimento com equipe interna com dedicação exclusiva de mão de obra (gestão de escalas, saída a campo e ateste de serviço). |
| [**Negociação e Manutenção Sobdemanda.png**](Modelagem/Negocia%C3%A7%C3%A3o%20e%20Manuten%C3%A7%C3%A3o%20Sobdemanda.png) | Subprocesso | Trâmites para demandas que extrapolam a capacidade interna: orçamentação, autorização fiscal, emissão de nota de empenho e ordem de fornecimento. |
| [**Executar Serviço sobdemanda.png**](Modelagem/Executar%20Servi%C3%A7o%20sobdemanda.png) | Subprocesso | Acompanhamento e fiscalização técnica dos serviços executados por empresas contratadas no perímetro do campus. |
| [**Documentação e Pagamento.png**](Modelagem/Documenta%C3%A7%C3%A3o%20e%20Pagamento.png) | Subprocesso | Consolidação de registros fiscais: conferência de medição, relatórios fotográficos, ateste de nota fiscal e envio para liquidação financeira. |

---

### 📊 Métricas Estruturais da Modelagem

A análise quantitativa dos diagramas evidencia a complexidade da esteira de serviços analisada:

- **116 Atividades Mapeadas no Total**:
  - **59 Tarefas de Usuário** (*User Tasks*): atividades humanas intermediadas por sistemas computacionais (ex.: GLPI, SIPAC, e-mails).
  - **39 Tarefas Manuais Puras** (*Manual Tasks*): intervenções físicas diretas (reparos elétricos, hidráulicos, pintura, vistorias prediais).
- **Gateways Decisórios**: predomínio de desvios exclusivos baseados em pareceres técnicos e disponibilidade de materiais/contratos.
- **7 Eventos Intermediários de Espera**: pontos de retenção temporal para secagem de materiais, testes de bancada ou envio de cotações por fornecedores.
- **16 Fluxos de Mensagem**: interações interorganizacionais formais entre o setor de infraestrutura e fornecedores externos.

---

### ⚠️ Principais Gargalos Diagnosticados no Estado Legado

1. **Dependência Crítica de Conhecimento Tácito**: decisões de triagem concentradas na experiência individual dos servidores, sem regras formais parametrizadas.
2. **Ausência de Deduplicação Automatizada**: abertura de múltiplos chamados para a mesma falha estrutural, fragmentando o histórico e alocando equipes em duplicidade.
3. **Comunicação e Instrução Descentralizada**: utilização concorrente de GLPI, formulários físicos, mensagens de texto e memorandos, dificultando a rastreabilidade fiscal.
4. **Acúmulo Operacional no Encerramento e Ateste**: lentidão na consolidação de relatórios de medição e notas fiscais para encaminhamento ao setor de finanças.

---

## 📊 2. Diagnóstico de Maturidade BPM no IFSEMG

A pesquisa documental e de campo investigou o nível de maturidade e a institucionalização da disciplina de BPM nas diferentes unidades que compõem o Instituto Federal do Sudeste de Minas Gerais.

### 📌 Instrumentos e Evidências Disponíveis

- [**Questionário de BPM**](PesquisaBPMnoIFSEMG/QUESTION%C3%81RIO%20SOBRE%20GERENCIAMENTO%20DE%20PROCESSOS%20DE%20NEG%C3%93CIO%20(BPM)%20-%20Question%C3%A1rio.pdf): Formulário estruturado aplicado aos gestores das unidades para mapear existência de comitês de governança, métodos de modelagem, ferramentas utilizadas e maturidade de processos.
- [**Planilha de Respostas por Unidades (XLSX)**](PesquisaBPMnoIFSEMG/QUESTION%C3%81RIO%20SOBRE%20GERENCIAMENTO%20DE%20PROCESSOS%20DE%20NEG%C3%93CIO%20(BPM)_unidades.xlsx): Dados brutos tabulados com as respostas consolidadas das 10 unidades do IFSEMG consultadas.
- [**Informações da Reitoria**](PesquisaBPMnoIFSEMG/INFORMA%C3%87%C3%95ES%20N%C2%BA%2032492025%20-%20GABREITORI%20(11.01.01).pdf): Manifestação da administração central detalhando as iniciativas sistêmicas de processos em nível institucional.
- [**Resposta Oficial LAI / e-SIC**](PesquisaBPMnoIFSEMG/Resposta%20ao%20pedido%2023546.104950_2025-15.pdf): Documento protocolado sob o número `23546.104950/2025-15` fornecendo as respostas oficiais da instituição para fins de comprovação científica e transparência pública.

### 🔍 Principais Conclusões da Pesquisa

- **Disparidade e Assimetria**: 8 das 10 unidades consultadas informaram não dispor de metodologia formal ou escritório de processos (EPRO) local ativo.
- **Iniciativas Pontuais vs. Sistêmicas**: constataram-se esforços isolados de otimização conduzidos por servidores dedicados, porém sem padronização ou governança contínua institucionalizada.
- **Importância do Caso de Estudo**: o mapeamento do setor de Prefeitura do Campus Rio Pomba fornece um roteiro metodológico e empírico de referência para expansão a outras pró-reitorias e unidades acadêmicas.

---

## 💻 3. Como Visualizar e Reutilizar os Artefatos

### Visualização Rápida
- Todas as imagens dos diagramas estão renderizadas em formato `.png` de alta resolução na pasta [`Modelagem/`](Modelagem/). Basta clicar sobre qualquer um dos arquivos no GitHub para visualizar o fluxo correspondente.

### Edição e Exploração Estrutural (`.bpm`)
Para inspecionar as propriedades dos elementos, documentações de campos, variáveis e atributos das tarefas:
1. Faça o download gratuito do [**Bizagi Process Modeler**](https://www.bizagi.com/pt/plataforma/modeler) (Windows).
2. Clone este repositório ou baixe o arquivo:
   ```bash
   git clone https://github.com/ProjectBPMN/ModelagemBPMN.git
   ```
3. Abra o arquivo [`Modelagem/Controle da manutencao e infraestrutura fisica (AS IS).bpm`](Modelagem/Controle%20da%20manutencao%20e%20infraestrutura%20fisica%20(AS%20IS).bpm) no Bizagi Modeler.

### Leitura dos Dados e Documentos
- Para a planilha de dados: utilize o Microsoft Excel, LibreOffice Calc ou o visualizador nativo de planilhas.
- Para os arquivos de texto e questionários: utilize qualquer leitor compatível com PDF.

---

## 📚 Como Citar este Trabalho

Caso utilize estes modelos de processos ou os dados diagnósticos em artigos, dissertações, teses ou relatórios técnicos, cite a fonte de acordo com as normas ABNT:

```text
PROJETO BPMN. Modelagem de Processos de Negócio (BPMN 2.0) e Diagnóstico Institucional no IF Sudeste MG. 
Repositório de dados e modelos de pesquisa. GitHub, 2026. 
Disponível em: https://github.com/ProjectBPMN/ModelagemBPMN. Acesso em: [data de acesso].
```

**BibTeX:**
```bibtex
@misc{modelagembpmn2026,
  author       = {{Project BPMN}},
  title        = {Modelagem de Processos de Neg{\'o}cio (BPMN 2.0) e Diagn{\'o}stico Institucional no IF Sudeste MG},
  year         = {2026},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/ProjectBPMN/ModelagemBPMN}},
  note         = {Reposit{\'o}rio de dados e modelos de pesquisa aberta}
}
```

---

## 📜 Licença e Uso Acadêmico

Os artefatos disponibilizados neste repositório têm caráter estritamente educacional, científico e de governança pública, regidos pelas diretrizes de transparência e ciência aberta.
