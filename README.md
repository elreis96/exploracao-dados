# 🚗 Projeto: Análise e Engenharia de Dados - Locação de Veículos

Este projeto demonstra o pipeline de dados de uma empresa de aluguel de carros, focando na transformação de dados brutos em métricas de negócio.

## 🧹 Limpeza de Dados (Data Cleaning)
Para garantir cálculos precisos, realizei as seguintes correções:
* **Tratamento de Datas:** Conversão de strings para `datetime` com tratamento de erros (`NaT`).
* **Correção Financeira:** Transformação da coluna `daily_rate` para numérico e tratamento de valores negativos.
* **Valores Ausentes:** Preenchimento de idades (`age`) e emissões de CO₂ com médias calculadas.

## 🚀 Engenharia de Dados (Feature Engineering)
Criação de novas inteligências sobre os dados:
1. **Duração (dias_locacao):** Diferença exata entre data de início e fim.
2. **Receita Total:** Cálculo de faturamento por contrato (Dias × Diária).
3. **Pegada de Carbono:** Cálculo de `co2_emitido` por viagem.
4. **Sazonalidade:** Extração de mês e ano para análise de tendências.

## 🧠 Desafios Técnicos Resolvidos
* **Correção de Atribuição:** Ajuste de bugs onde conversões de data sobrescreviam colunas de preço.
* **Erro de Tipagem:** Resolução de erros de operação entre strings e números.

---
### Como Executar
1. Certifique-se de que os arquivos `customers_data.csv`, `rentals_data.json` e `vehicles_data.json` estão na mesma pasta.
2. Execute o script Python para gerar a base consolidada.
