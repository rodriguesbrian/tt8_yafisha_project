# Y.Afisha – Análise de Produto, Vendas e ROI de Marketing

Este projeto foi desenvolvido como parte do estágio no departamento analítico da **Y.Afisha**, com o objetivo de otimizar os investimentos em marketing com base em dados reais de uso, conversão e receita.

O foco é responder uma pergunta central:

> Onde investir para maximizar retorno e crescimento sustentável?

---

## 🎯 Objetivo

Analisar dados de:

- Acessos ao site (logs de servidor)
- Pedidos realizados
- Despesas com marketing

Para entender:

- Como os usuários utilizam o produto
- Quando convertem
- Quanto geram de receita (LTV)
- Se o marketing gera ROI positivo
- Quais canais merecem mais orçamento

---

## 📊 Estrutura do Projeto

O notebook está dividido em três grandes blocos: **Produto, Vendas e Marketing**.

---

# 1️⃣ Preparação dos Dados

### Arquivos utilizados

- `/datasets/visits_log_us.csv`
- `/datasets/orders_log_us.csv`
- `/datasets/costs_us.csv`

### Etapas realizadas

- Importação com Pandas
- Conversão de datas para datetime
- Otimização de tipos (`category`, `int`, `float`)
- Criação de colunas auxiliares:
  - Dia
  - Semana
  - Mês
  - Coorte de aquisição
  - Tempo até conversão
- Cálculo da duração das sessões

---

# 2️⃣ Produto – Como as pessoas usam o site?

### Métricas analisadas

### 📌 Usuários ativos
- DAU (Daily Active Users)
- WAU (Weekly Active Users)
- MAU (Monthly Active Users)

### 📌 Sessões
- Sessões por dia
- Sessões médias por usuário
- Duração média das sessões

### 📌 Retenção
- Análise de coortes
- Frequência de retorno
- Curva de retenção por dispositivo e canal

### Visualizações
- Evolução temporal de DAU/WAU/MAU
- Duração média de sessão
- Heatmap de retenção por coorte
- Comparação entre dispositivos (Desktop vs Mobile)

---

# 3️⃣ Vendas – Quando e quanto os usuários compram?

### 📌 Tempo até conversão
- Diferença entre primeira visita e primeira compra
- Classificação por:
  - Conversão 0d
  - Conversão 1d
  - Conversão 7d
  - Conversão 30d+

Comparação entre canais e coortes.

### 📌 Pedidos
- Pedidos médios por cliente
- Frequência de recompra
- Receita média por pedido (AOV)

### 📌 LTV (Lifetime Value)
Cálculo por:
- Coorte
- Origem de tráfego
- Dispositivo

Análise acumulada ao longo do tempo.

---

# 4️⃣ Marketing – O investimento valeu a pena?

### 📌 Investimentos
- Gasto total
- Gasto por canal
- Evolução mensal de despesas

### 📌 CAC (Customer Acquisition Cost)
Cálculo por origem:
CAC = custo total da origem / número de clientes adquiridos

### 📌 ROI
ROI = (LTV − CAC) / CAC

Análise por:
- Canal
- Coorte
- Dispositivo
- Evolução temporal

### Visualizações
- Gasto por origem
- LTV vs CAC por canal
- ROI acumulado
- Payback period (tempo até cobrir o custo de aquisição)

---

# 5️⃣ Principais Métricas Utilizadas

- DAU / WAU / MAU
- Retenção por coorte
- Taxa de conversão
- Tempo até primeira compra
- AOV (Average Order Value)
- LTV
- CAC
- ROI
- Payback period

---

# 6️⃣ Conclusão Estratégica

A seção final apresenta:

- Canais com maior LTV
- Canais com menor CAC
- Canais com ROI positivo consistente
- Identificação de canais que destroem valor
- Recomendação objetiva de redistribuição de orçamento

A recomendação é baseada principalmente em:

1. ROI por canal
2. Tempo de payback
3. Escalabilidade da retenção
4. Qualidade da coorte ao longo do tempo

---

# 🚀 Tecnologias Utilizadas

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 📦 Como Executar

1. Clone o repositório:

```bash
git clone https://github.com/rodriguesbrian/tt8_yafisha_project
cd tt8_yafisha_project