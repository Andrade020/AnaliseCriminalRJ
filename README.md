# AnaliseCriminalRJ

Análise dos crimes ocorridos no estado do Rio de Janeiro, com foco na capital, de 2003 a 2024.

## Conteúdo

| Arquivo | Descrição |
|---|---|
| `BaseDPEvolucaoMensalCisp.csv` | Série histórica mensal de indicadores criminais por área de delegacia (CISP), desde 01/2003. Separador `;`, codificação `latin1`. |
| `série_histórica_mensal_por_área_de_delegacia_desde_01_2003.ipynb` | Notebook que carrega o CSV direto do GitHub e gera os gráficos. Pode ser aberto no Google Colab. |
| `Evolução dos Crimes no Rio de Janeiro (2003-2024) -- Anual e Mensal.html` | Gráfico interativo da evolução anual e mensal dos crimes. |
| `Homícidios e Casos Suspeitos no Município do Rio de Janeiro (2003-2024) Anual.html` | Gráfico interativo de homicídios e casos suspeitos na capital. |
| `crime_rj_interativo (1).html` | Visualização interativa dos dados. |

## Sobre os dados

Cada linha é uma CISP em um mês. Colunas principais: `cisp`, `ano`, `mes`, `aisp`, `risp`, `munic`, `regiao` e as contagens por tipo de crime (`hom_doloso`, `latrocinio`, `roubo_celular`, `estupro` etc.). O arquivo segue o formato da base de evolução mensal por CISP divulgada pelo ISP-RJ.

Para filtrar a capital: `df[df["munic"] == "Rio de Janeiro"]`.

## Como usar

- **Notebook:** abra no Colab pelo botão no topo do notebook. Rode **cada gráfico individualmente**, pois alguns gráficos substituem os anteriores quando executados em sequência.
- **HTMLs interativos:** baixe e abra no navegador.
- **Localmente:**

```bash
pip install pandas matplotlib plotly jupyter
jupyter notebook
```
