# Steam Gaming Analytics 2026

[![Power BI](https://shields.io)](https://microsoft.com)
[![GitHub](https://shields.io)](https://github.com)


## 🎯 Objetivo do Projeto
Este projeto analisa o comportamento dos usuários na plataforma Steam durante o ano de 2026. O foco principal é identificar os jogos dominantes do mercado, compreender a evolução temporal da atividade dos jogadores (sazonalidade) e destacar as tendências emergentes no cenário de games globais.

### ❓ Pergunta Central
> **Quais jogos dominam a Steam em 2026, como a atividade dos jogadores evolui ao longo dos meses e quais tendências podemos identificar a partir desses dados?**

---

## 📋 Escopo das Análises

O projeto foi segmentado em cinco grandes vertentes analíticas:

| Análise | O que queremos descobrir |
| :--- | :--- |
| **Popularidade** | Quais são os 20 jogos mais populares da plataforma? |
| **Atividade** | Quais jogos acumulam o maior volume de horas estimadas de gameplay? |
| **Tendências** | Quais títulos estão em crescimento acelerado ou perdendo base de jogadores? |
| **Sazonalidade** | Em quais meses ou períodos do ano os jogadores ficam mais ativos? |
| **Comparativo** | Como os jogos gratuitos (Free-to-Play) e pagos diferem em engajamento? |

---

## 🗃️ Estrutura do Modelo de Dados

O projeto conta com um modelo relacional desenvolvido diretamente via **Power Query** e **Power BI**, estruturado da seguinte forma:

- **TabelaTop202026 (Tabela Fato/Dimensão Central):** Contém os dados consolidados do ranking, títulos e gêneros dos principais jogos.
- **TabelaHorasMensaisLooker & TabelaAtividadeMensal:** Tabelas de suporte temporal ligadas em relacionamento de 1 para muitos (`1:*`) com a tabela de jogos principal através do campo comum de gênero/identificação.
- **TabelaMetodologiaFontes:** Tabela isolada contendo as referências informativas do projeto.

---

## 🌐 Fontes de Dados

As extrações de dados foram baseadas em três plataformas de monitoramento consolidadas:

1. **[SteamCharts (Fonte Principal)](https://steamcharts.com/)** - Histórico detalhado de jogadores simultâneos, médias mensais e picos acumulados desde 2012.
2. **[Steam – Estatísticas Oficiais](https://store.steampowered.com/charts)** - Snapshot em tempo real e de curto prazo da popularidade global e vendas na loja.
3. **[SteamDB](https://steamdb.info/charts/)** - Base robusta comparativa e dados técnicos de engajamento do ecossistema Steam.

---

## 🚀 Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com
   ```
2. Navegue até a pasta `pbix/`.
3. Abra o arquivo `steam_analytics.pbix` no **Power BI Desktop**.
4. (Opcional) Caso as fontes locais de dados solicitem atualização, verifique os caminhos parametrizados no Power Query.
