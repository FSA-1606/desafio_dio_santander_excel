Simulador de Investimentos em Fundos Imobiliários (FIIs)

> Projeto desenvolvido para o desafio "Entendendo o Desafio" — Trilha Excel da DIO (Digital Innovation One) em parceria com o Santander.

Uma ferramenta desenvolvida no Microsoft Excel com interface inspirada em aplicativos modernos, projetada para planejamento financeiro pessoal, simulação de acúmulo de patrimônio via juros compostos e alocação dinâmica de aportes em Fundos Imobiliários por perfil de investidor.



Demonstração da Ferramenta

| Perfil Moderado (Padrão) | Perfil Agressivo (Alocação Dinâmica) |
| :: | :: |
| ![Simulação Perfil Moderado](docs/simulacao-moderado.png) | ![Simulação Perfil Agressivo](docs/simulacao-agressivo.png) |



As 5 Perguntas de Negócio Respondidas

A ferramenta foi projetada para responder imediatamente às 5 perguntas fundamentais antes de iniciar os investimentos em FIIs:

| # | Pergunta de Negócio | Onde aparece na planilha | Nome do Intervalo / Fórmula |
| :-: | : | : | : |
| 1 | Quanto investir por mês? | Seção `2. PERGUNTAS DE NEGÓCIO` | Campo de entrada: `aporte` (`R$ 500,00`) |
| 2 | Por quantos anos? | Seção `2. PERGUNTAS DE NEGÓCIO` | Campo de entrada: `qtd_anos` (`5 anos`) |
| 3 | Qual a taxa de rendimento mensal? | Seção `2. PERGUNTAS DE NEGÓCIO` | Campo de entrada: `taxa_mensal` (`1,079% a.m.`) |
| 4 | Quanto de patrimônio vai acumular? | Seção `2. PERGUNTAS DE NEGÓCIO` | Célula calculada: `patrimonio` (`=-VF(...)`) |
| 5 | Quanto vai receber de dividendos por mês? | Seção `2. PERGUNTAS DE NEGÓCIO` | Célula calculada: `=patrimonio * rendimento_carteira` |



Lógica e Funcionamento das Fórmulas

1. Valor Futuro (`VF` / `FV`) — Acúmulo por Juros Compostos
A função `VF` é responsável por calcular o montante final acumulado considerando aportes mensais constantes sob a taxa de juros compostos.

```excel
=-VF(taxa_mensal; qtd_anos * 12; aporte)

Diferenciais e Ideias de Evolução Implementadas

Gráfico de Pizza Dinâmico: Gráfico nativo vinculado à alocação por tipo de FII, que se ajusta em tempo real conforme a troca do perfil na caixa de seleção.

Como Executar a Planilha
Faça o download ou clone este repositório:

Bash
git clone [https://github.com/FSA-1606/deasfio_dio_santader_excel.git](https://github.com/FSA-1606/deasfio_dio_santader_excel.git)
Abra o arquivo Simulador_FII_Pro_DIO.xlsx no Microsoft Excel (2016 ou superior).

Habilite a edição caso o Excel solicite.

Modifique os campos de entrada destacados na seção 1. CONFIGURAÇÕES BASE e 2. PERGUNTAS DE NEGÓCIO e altere a caixa de seleção em 4. ALOCAÇÃO DO APORTE POR PERFIL DE INVESTIDOR.

Elaborado por Fernando Andrade.