# Fluxos do Agente – Escritório de Advocacia

## 📁 Imagens (PNG/SVG)
> Os arquivos ficam na pasta `assets/`. Ajuste os nomes se estiverem diferentes no seu repositório.

### Triagem (imagem)
![Fluxo de Triagem](assets/novo-nome.png)

### Follow-up (imagem)
![Acompanhamento pós-consulta](assets/acompanhamento-pos-consulta-e-relacionamento.png)

---

## 🧩 Diagramas (Mermaid)
> Para renderizar, cada diagrama deve estar dentro de um bloco cercado **```mermaid** e fechar com **```**. (O GitHub recomenda também uma linha em branco antes/depois do bloco.) 

### 1) Atendimento / Triagem detalhado
```mermaid
flowchart TD
  A["Mensagem inicial (Site/WhatsApp/Instagram)"] --> B{"Consentimento LGPD?"}
  B -->|Não| X["Mostrar política e solicitar consentimento"]
  B -->|Sim| C["Coletar dados mínimos (nome, e-mail/telefone, cidade/UF)"]
  C --> D["Identificar área do direito (trabalho, cível, família, previdenciário, etc.)"]
  D --> E["Perguntas-chave de triagem (urgência, prazos, partes)"]
  E --> F{"É caso do escritório?"}
  F -->|Não| G["Enviar conteúdo informativo permitido pela OAB + contatos úteis"]
  F -->|Sim| H["Escolher canal de consulta (online/presencial)"]
  H --> I["Oferecer horários disponíveis"]
  I --> J{"Cliente confirma horário?"}
  J -->|Não| I
  J -->|Sim| K["Enviar confirmação + política de privacidade"]
  K --> L["Criar ticket e checklist de documentos"]
  L --> M["Encaminhar checklist e link de upload seguro"]
  M --> N["Fim da triagem (aguardar documentos)"]

```
### 2) Intake (pré-consulta, LGPD e documentos)
```mermaid
flowchart TD
  A["Lead qualificado"] --> B["Enviar checklist por área (previdenciário, cível, etc.)"]
  B --> C{"Documentos recebidos?"}
  C -->|Não| D["Lembrar cliente / reenviar link de upload"]
  C -->|Sim| E["Upload seguro + registrar consentimento (LGPD)"]
  E --> F["Extrair texto dos PDFs"]
  F --> G["Gerar resumo automático p/ advogado"]
  G --> H{"Faltam itens essenciais?"}
  H -->|Sim| I["Solicitar itens faltantes ao cliente"]
  H -->|Não| J["Pronto para consulta"]

```
### 3) Pesquisa de jurisprudência (com links oficiais)
```mermaid
flowchart TD
  A["Pergunta/tese do caso"] --> B["Selecionar tribunal e período (STJ/STF/TJs)"]
  B --> C["Gerar termos de busca"]
  C --> D["Consultar portais oficiais (STJ/STF/TJ)"]
  D --> E{"Encontrou decisões relevantes?"}
  E -->|Não| F["Ajustar termos / ampliar período"]
  E -->|Sim| G["Extrair metadados (nº, relator, data, ementa)"]
  G --> H["Compilar resumo e links oficiais"]
  H --> I["Salvar log para auditoria"]
  I --> J["Enviar ao advogado"]

```
### 4) Geração de petição (rascunho + revisão humana)
```mermaid
flowchart TD
  A["Briefing estruturado (partes, fatos, pedidos)"] --> B["Selecionar template do escritório"]
  B --> C["Inserir fundamentos e placeholders de provas"]
  C --> D{"Jurisprudência vinculada?"}
  D -->|Não| E["Marcar TODO para pesquisa e citação"]
  D -->|Sim| F["Inserir referências (links oficiais)"]
  E --> G["Gerar rascunho"]
  F --> G["Gerar rascunho"]
  G --> H["Revisão humana obrigatória"]
  H --> I["Exportar DOCX/PDF e protocolar"]

```
### 5) Follow-up pós-consulta e relacionamento
```mermaid
flowchart TD
  A["Consulta realizada"] --> B["Gerar resumo da consulta"]
  B --> C["Revisão do advogado"]
  C --> D{"Pendências de documentos?"}
  D -->|Sim| E["Solicitar documentos pendentes (e-mail/WhatsApp)"]
  E --> F["Confirmar recebimento e anexar ao dossiê"]
  D -->|Não| G["Redigir plano de ação e próximos passos"]
  F --> G
  G --> H{"Cliente consente receber atualizações?"}
  H -->|Não| I["Registrar opt-out e orientar canal oficial de contato"]
  H -->|Sim| J["Agendar lembretes de prazos/etapas (calendário)"]
  J --> K["Enviar resumo informativo (compliance OAB)"]
  K --> L{"Audiência/ato processual marcado?"}
  L -->|Sim| M["Enviar instruções e checklist pré-ato"]
  L -->|Não| N["Acompanhar andamento e enviar status periódico"]
  M --> O["Após o ato: registrar ocorrências e atualizar cliente"]
  N --> O
  O --> P{"Caso encerrado?"}
  P -->|Não| N
  P -->|Sim| Q["Solicitar feedback e autorização para case (opcional)"]
  Q --> R["Arquivar dossiê conforme política de retenção (LGPD)"]
  R --> S["Fim"]

```
