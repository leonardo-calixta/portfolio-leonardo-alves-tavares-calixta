🏙️ Engenharia de Contexto e Lógica Física
📝 Descrição do Projeto
Este projeto aplica conceitos de listas, estruturas de repetição (for, while), estruturas de decisão (if/elif/else, match-case), funções e operadores complexos na resolução de dois problemas do mundo real — exigindo coleta de dados manual e mapeamento espacial como ponto de partida.
Desenvolvido como parte da disciplina de Engenharia de Contexto e Lógica Física, o projeto é dividido em duas partes práticas e uma reflexão crítica sobre como o pensamento lógico transforma a percepção do cotidiano.

⚙️ Parte 1 — Análise de Microclima Urbano
Analisa dados reais de temperatura, umidade e Índice de Qualidade do Ar (IQA) de 3 cidades do estado de São Paulo (São Paulo, Santos e Campinas) em dois horários distintos (15h e 18h).
Funcionalidades:

Classificação da qualidade do ar com match-case seguindo as faixas oficiais da CETESB
Cálculo de uma Nota de Conforto Urbano (0–10) com fórmula ponderada:

Temperatura (peso 35%): ideal entre 18°C e 26°C
Umidade (peso 25%): ideal entre 50% e 70%
IQA (peso 40%): escala invertida (IQA 0 = 10pts, IQA 120+ = 0pts)



LocalHorárioTempUmidadeIQAQualidade do ArSão Paulo15h27°C57%61ModeradaSão Paulo18h22°C45%61ModeradaSantos15h26°C54%67ModeradaSantos18h24°C58%68ModeradaCampinas15h27°C42%81RuimCampinas18h23°C53%84Ruim

🚨 Parte 2 — Simulador de Evacuação de Emergência
Simula o trajeto de um agente tentando evacuar uma residência com obstáculos físicos reais (mapeados da própria casa), utilizando um loop while com sistema de inventário e energia.
Mecânica do simulador:

O agente percorre 6 locais: Quarto dos fundos → Corredor → Cozinha → Sala → Hall → Saída
Obstáculos como porta trancada e fumaça exigem que o agente colete itens (chave, extintor) antes de avançar
Se não tiver o item necessário, o agente recua e perde energia extra
A evacuação falha se a energia chegar a zero


💡 Parte 3 — Reflexão Crítica

"Ao transformar portas e corredores em lógica de programação, percebi que o pensamento cotidiano costuma ser impreciso. Enquanto no dia a dia agimos de forma vaga, a programação exige respostas claras para cada situação."

O projeto revelou que aprender programação também organiza o pensamento no dia a dia — antecipar obstáculos no código é o mesmo raciocínio de antecipar problemas na vida real.

📊 Resultados e Aprendizados

match-case como alternativa ao if/elif encadeado: Mais legível para classificações com múltiplas faixas numéricas.
enumerate no for: Permite iterar com índice sem usar range(len()), tornando o código mais Pythonico.
Loop while com estado: O simulador de evacuação exigiu controle simultâneo de posição, energia e inventário dentro de um loop de condição composta.
Dados reais aumentam o engajamento: Usar dados climáticos reais de cidades conhecidas e mapear a própria casa tornaram os problemas mais significativos do que exercícios abstratos.

🚀 Tecnologias Utilizadas

Linguagem: Python 3
Conceitos aplicados: Listas, for com enumerate, while, match-case, funções, operadores aritméticos complexos, f-strings, lógica de inventário
Ferramenta: Google Colab

🔧 Como Executar

Acesse o Google Colab ou execute localmente com Python 3.
Abra o arquivo engenharia_de_contexto_e_logica_fisica.py.
Execute — a Parte 1 roda automaticamente com dados embutidos; a Parte 2 simula o trajeto de evacuação.
