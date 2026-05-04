# 🚗 Dashboard KM — Renata & Gian

Dashboard interativo de km rodados e valores recebidos por entregador, com entrada manual de dados, importação e exportação de planilha CSV.

## ✨ Funcionalidades

- Formulário para inserir data, entregador, km e taxa R$/km
- Prévia do valor do dia antes de confirmar o lançamento
- Exportar CSV — baixa todos os registros como planilha
- Importar CSV — carrega dados de uma planilha existente (ignora duplicatas)
- Filtro por entregador: Renata, Gian ou ambos
- Cards de métricas com alternância entre KM e R$
- Gráfico de barras com km por dia
- Gráfico de barras horizontal com total acumulado por entregador
- Gráfico semanal (KM ou Valor R$) com filtro de entregador independente
- Semanas contadas de domingo a sábado
- Histórico de registros em seção recolhível
- Dados salvos no navegador (localStorage)
- Responsivo para celular, tablet e desktop

## 🚀 Como usar

Abra o `index.html` diretamente no navegador. Sem servidor, sem instalação.

**Para publicar online (recomendado):**
1. Crie um repositório no GitHub
2. Faça upload do `index.html`
3. Ative o GitHub Pages em **Settings → Pages → Branch: main**
4. Acesse o link gerado pelo GitHub Pages
5. No celular, salve como atalho na tela inicial para usar como app

## 📊 Fluxo com planilha

1. Insira os dados diários pelo formulário
2. Clique em **Exportar CSV** para baixar a planilha
3. Abra no Excel, confira ou adicione linhas
4. Salve como `.csv` e clique em **Importar CSV** para recarregar
5. O sistema ignora registros duplicados automaticamente

### Formato do CSV para importação

```
data,entregador,km
2025-04-13,renata,128.4
2025-04-13,gian,178.1
2025-04-14,renata,122.0
```

- **data**: formato `AAAA-MM-DD`
- **entregador**: `renata` ou `gian` (letras minúsculas)
- **km**: número com ponto decimal (ex: `128.4`)

## 💡 Taxa por km

A taxa R$/km é inserida junto com cada registro no formulário. O valor digitado fica salvo no navegador e é sugerido automaticamente no próximo lançamento. Para alterar, basta digitar o novo valor no campo antes de adicionar.

## 🛠️ Tecnologias

- HTML5 / CSS3 / JavaScript vanilla
- [Chart.js 4.4.1](https://www.chartjs.org/) — gráficos interativos
- Google Fonts: Noto Serif JP + DM Sans
- localStorage para persistência dos dados
- FileReader API para importação de CSV

---

Desenvolvido para portfólio · parte da jornada de transição para Ciência de Dados · Renata Citelli
