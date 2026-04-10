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

**Agência B16** — Henrique Cardoso, Business Inteligence. Data: 09/04/2026.

## 📋 Changelog — Histórico de Versões

### v5 · 09/04/2026
`feat: abas reordenadas, perfil alvo, insights de mídia e perfil, comparação pesquisa`

**Novas funcionalidades:**
- Ordem das abas alterada: Visão Geral → Pesquisa → Insights
- Aba Pesquisa: seção "Comparação com Perfil Alvo" com 10 cards (Q1–Q11)
  - Badge 🎯 Perto / ⚡ Longe do alvo por dimensão
  - Barras de progresso com percentual real vs threshold definido
  - Barras dos gráficos em amarelo B16 para respostas dentro do perfil alvo
- Aba Insights dividida em duas seções:
  - **Insights de Mídia** — análises de tráfego (CTR, CPL, criativos, público)
  - **Insights de Perfil** — comparação automática com o avatar do lançamento (idade, gênero, renda, ocupação, canal de descoberta, motivação)
- Perfil alvo integrado ao código: homem, 18–35 anos, baixa renda, CLT/informal, busca negócio próprio

---

### v4 · 09/04/2026
`feat: filtro de data, comparativo de períodos, abas, rodapé com legenda`

**Novas funcionalidades:**
- Filtro de período principal + período de comparação no header
- Delta percentual nos big numbers (▲▼ vs período comparativo)
- Sistema de 3 abas: Visão Geral, Insights, Pesquisa
- Rodapé fixo com legenda explicando o significado das cores (verde, amarelo, vermelho)
- Badge "COMPARATIVO ATIVO" quando período de comparação está selecionado

---

### v3 · 09/04/2026
`feat: tabela de criativos, leitura dinâmica das 3 abas do Sheets`

**Novas funcionalidades:**
- Tabela de performance por criativo: nome curto + nome completo | valor gasto | leads | CPL
- CPL colorido: verde (<R$3), laranja (R$3–7), vermelho (>R$7)
- 🏆 badge no criativo com melhor CPL
- Leitura dinâmica da aba Pesquisa (Q1–Q11, gráficos de barra horizontal)
- Big number de % de respondentes da pesquisa
- `Promise.all` para buscar as 3 abas em paralelo (mais rápido)

---

### v2 · 09/04/2026
`fix: parser CSV robusto + conexão ao vivo com Google Sheets`

**Correções e melhorias:**
- Parser CSV reescrito para lidar com campos que contêm vírgulas no nome (coluna `Spend (Cost, Amount Spent)`)
- Função `num()` com busca flexível por substring — resistente a variações de nome do Sheets
- Dashboard hospedado no GitHub Pages (HTTPS resolve bloqueio de CORS)
- Conexão ao vivo com Google Sheets via `gviz/tq?tqx=out:csv`
- Atualização automática a cada 2 horas com contador regressivo
- Badge de status: 🟡 Carregando → 🟢 Ao vivo → 🔴 Erro
- Botão 🔄 Atualizar para refresh manual

---

### v1 · 09/04/2026
`feat: dashboard inicial com dados estáticos`

**Funcionalidades:**
- Big numbers: Valor Investido, Total de Leads, CPL, Melhor CPL por criativo
- Funil de conversão: Impressões → Alcance → Cliques → LPV → Leads (com custo por etapa)
- Gráficos diários: investimento, leads, CPL, pagos vs orgânicos
- Top criativos por leads (barra horizontal)
- Distribuição por plataforma (Instagram vs Facebook) com ícones SVG
- Distribuição por formato (Reels, Stories, Feed) — pizza
- CPL por público: FRIO vs QUENTE
- 8 insights automáticos de gestor de tráfego
- Logo B16 embutida em base64
- Visual clean: fundo off-white, preto e amarelo B16
- Dados de leads estáticos (WordPress/Elementor)
- Filtro por campanhas com tag `[CNP]` a partir de 05/04/2026


### v6 · 10/04/2026
`feat: previsao de leads com slider + 3 cenarios dinamicos`

**Novas funcionalidades:**
- Seção "Previsão de Leads até o Evento" no topo da aba Insights
- Slider de investimento de R$ 0 a R$ 70.000 (passo R$ 500)
- 3 cenários calculados automaticamente com base no CPL atual:
  - 🚀 Otimista: CPL atual × 1,0
  - 🎯 Realista: CPL atual × 1,36 (+36%)
  - 🛡️ Conservador: CPL atual × 1,56 (+56%)
- Cenários atualizam automaticamente quando o período ou dados mudam
- Nota metodológica explicando a lógica dos multiplicadores
