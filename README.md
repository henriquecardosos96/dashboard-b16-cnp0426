# 📊 Dashboard CNP0426 — Cromador Nível Pro

Dashboard de performance desenvolvido pela **Agência B16** para acompanhamento em tempo real do lançamento **Cromador Nível Pro** da Mundial Cromo.

🔗 **Acesse o dashboard:** https://henriquecardosos96.github.io/dashboard-b16/

---

## 🎯 Sobre o projeto

Este dashboard foi construído para centralizar e visualizar os dados de mídia paga e captação de leads de uma campanha de lançamento digital, permitindo decisões rápidas e baseadas em dados durante o período de veiculação.

Os dados são atualizados automaticamente a cada 2 horas diretamente do Google Sheets, sem necessidade de exportação manual ou ferramentas pagas de BI.

---

## 📦 Fontes de dados

| Fonte | Aba no Sheets | Atualização |
|---|---|---|
| Meta Ads (Facebook/Instagram) | `Dados Meta Ads` | Manual (exportação do Ads Manager) |
| Leads / Elementor (WordPress) | `Elementor` | Manual diário |
| Pesquisa de público | `Pesquisa` | Automática (formulário conectado) |

---

## 📈 O que o dashboard exibe

### Visão Geral
- Valor investido nas campanhas `[CNP]`
- Total de leads captados (pagos e orgânicos)
- CPL — Custo por Lead médio
- Melhor CPL por criativo

### Funil de Conversão
- Impressões → Alcance → Cliques → Landing Page View → Leads
- Taxa de conversão entre cada etapa
- Custo por etapa (CPM, CP Alcance, CPC, CP LPV, CPL)

### Evolução Diária
- Investimento por dia
- Leads por dia
- CPL por dia
- Leads pagos vs orgânicos

### Criativos & Distribuição
- Top criativos por volume de leads
- Tabela completa: criativo | valor gasto | leads | CPL
- Distribuição por plataforma (Instagram vs Facebook)
- Distribuição por formato (Reels, Stories, Feed)

### CPL por Público
- Comparativo FRIO vs QUENTE
- Investimento, leads e CPL por segmento

### Pesquisa de Público
- % de leads que responderam a pesquisa
- 11 gráficos de distribuição de respostas (Q1 a Q11)

### Insights — Gestor de Tráfego
- Análises automáticas geradas a partir dos dados
- Identificação de gargalos, oportunidades e recomendações de otimização
- Atualizados a cada refresh dos dados

---

## 🛠️ Tecnologias utilizadas

- **HTML/CSS/JS** puro — sem frameworks, sem dependências pesadas
- **Chart.js** para visualizações
- **Google Sheets** como banco de dados via CSV público
- **GitHub Pages** para hospedagem gratuita e entrega via HTTPS

---

## 🔄 Como atualizar os dados

1. Exporte os dados do Meta Ads Manager e cole na aba `Dados Meta Ads`
2. Atualize os leads na aba `Elementor` e registre a data na célula `Q2`
3. O dashboard busca os dados automaticamente a cada 2h — ou clique em **🔄 Atualizar** para forçar

---

## 🏢 Desenvolvido por

**Agência B16** — Hub Estratégico de Marketing Digital  
[agenciab16.com.
