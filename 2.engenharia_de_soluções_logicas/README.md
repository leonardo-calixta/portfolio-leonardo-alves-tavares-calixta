🚦 Engenharia de Soluções Lógicas — Cidade Inteligente
📝 Descrição do Projeto
Este projeto consiste no desenvolvimento de um algoritmo de controle inteligente de semáforos urbanos, partindo da abstração visual (fluxograma) até a validação lógica (teste de mesa). O objetivo é simular um sistema capaz de analisar o fluxo de veículos em 4 cruzamentos simultaneamente e tomar decisões automáticas para reduzir congestionamentos.
Desenvolvido como parte da disciplina de Engenharia de Soluções Lógicas, o projeto aplica os fundamentos de algoritmos estruturados: leitura de dados, processamento com operadores, estruturas de decisão encadeadas (if/else aninhado) e saída formatada — tudo modelado em pseudocódigo antes da implementação.
⚙️ Como o Sistema Funciona
O algoritmo SemaforoInteligente opera em 3 decisões sequenciais:
DecisãoCondiçãoAçãoD1 — Rede congestionada?Total_Rede > 80 carrosEntra em Modo Ajuste e identifica cruzamento críticoD2 — Emergência?Crítico > 50 carrosAtiva Modo Crise e aciona agente de trânsitoD3 — Onda verde possível?Crítico ≤ 40 carrosSincroniza fases (A, B, C, D) com +8s no cruzamento crítico
Se nenhuma condição for atingida, o sistema opera em Modo Livre com ciclo padrão de 30s.
🧪 Cenários de Teste (Teste de Mesa)
Cenário A — Normal

Valores: A=25, B=30, C=38, D=12 → Total=109 | Crítico=38
D1: 109>80 ✅ | D2: 38>50 ❌ | D3: 38≤40 ✅
Resultado: Modo Onda Verde, +8s no cruzamento C

Cenário B — Valor Exato de Fronteira

Valores: A=20, B=20, C=50, D=10 → Total=100 | Crítico=50
D1: 100>80 ✅ | D2: 50>50 ❌ (50 não é maior que 50) | D3: 50≤40 ❌
Resultado: Modo Ajuste Independente, +15s no cruzamento C

Cenário C — Sensor Quebrado (Dado Inválido)

Valores: A=-5, B=40, C=30, D=20 → Total=85 (distorcido pelo -5)
O algoritmo aceitou o valor negativo sem questionar → falha identificada
Solução proposta: validação enquanto (sensor < 0) → solicitar novo valor

📊 Resultados e Aprendizados

Valores de fronteira são críticos: A diferença entre >50 e >=50 muda completamente o caminho do algoritmo — na lógica binária, 50 e 51 são respostas opostas.
Validação de entrada é essencial: Sensores com falha (valores negativos) distorcem todos os cálculos subsequentes sem gerar alerta, provando a necessidade de validação após cada leitura.
Fluxograma como base: Desenhar o fluxo antes de escrever o pseudocódigo facilitou identificar as 3 decisões e suas ramificações com mais clareza.

🛠️ Tecnologias e Conceitos Utilizados

Representação: Fluxograma (papel) + Pseudocódigo estruturado
Conceitos aplicados: Estruturas de decisão (if/else aninhado), operadores relacionais, variáveis de controle, teste de mesa com múltiplos cenários
Ferramenta: Desenvolvido manualmente (caderno) como exercício de lógica pura

🔧 Arquivos do Projeto

fluxograma_cidade_inteligente.jpg — Fluxograma do algoritmo (páginas 1 e 3)
pseudocodigo_semaforo_inteligente.jpg — Pseudocódigo completo (páginas 4, 5 e 6)
teste_de_mesa.jpg — Cenários A, B e C com análise (páginas 2 e 3)
