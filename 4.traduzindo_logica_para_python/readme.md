# 🐍 Traduzindo Lógica Para Python
 
## 📝 Descrição do Projeto
 
Este projeto consiste em transformar conceitos de lógica de programação em soluções práticas utilizando a linguagem Python. Três problemas do mundo real foram implementados como funções independentes, aplicando estruturas de repetição, decisão, validação de entrada e cálculos acumulativos.
 
Desenvolvido como parte da disciplina de **Traduzindo Lógica Para Python**, o projeto marca a transição do pseudocódigo/fluxograma para código executável real, consolidando os fundamentos de programação em um ambiente prático (Google Colab).
 
## ⚙️ Funções Implementadas
 
### 🛒 Função 1 — `processar_vendas()`
Sistema de PDV (Ponto de Venda) que calcula o total de uma compra com múltiplos produtos e aplica descontos progressivos:
- **Desconto de 10%** para compras acima de R$ 500,00
- **Desconto de 5%** para compras entre R$ 200,00 e R$ 500,00
- Valida preços e quantidades negativos ou zerados antes de processar
### 🌡️ Função 2 — `analisar_clima()`
Analisador de dados climáticos semanais que processa 7 dias consecutivos de temperatura:
- Calcula a **média semanal** de temperaturas
- Contabiliza **dias acima de 35°C**
- Emite **alerta de condição extrema** se qualquer dia ultrapassar 45°C ou cair abaixo de -5°C
### 🎓 Função 3 — `sistema_notas_turma()`
Sistema de avaliação escolar que processa notas de uma turma inteira e classifica cada aluno:
- **Aprovado** → média ≥ 7,0
- **Recuperação** → média entre 5,0 e 6,9
- **Reprovado** → média < 5,0
## 📊 Resultados e Aprendizados
 
- **Tradução direta do pseudocódigo:** Cada função segue exatamente a lógica estruturada anteriormente em papel, provando que um bom algoritmo facilita a implementação.
- **Acumuladores e contadores:** As três funções utilizam variáveis acumuladoras (`total_compra`, `soma_temperaturas`) e contadores (`itens_comprados`, `dias_quentes`) dentro de loops.
- **Validação de entrada:** A função `processar_vendas` rejeita valores inválidos sem interromper o programa, tratando o erro com uma mensagem e continuando o loop.
## 🚀 Tecnologias Utilizadas
 
- **Linguagem:** Python 3
- **Conceitos aplicados:** Funções, estruturas de repetição (`for`, `range`), estruturas de decisão (`if/elif/else`), acumuladores, validação de entrada, operadores aritméticos e relacionais
- **Ferramenta:** Google Colab
## 🔧 Como Executar
 
1. Acesse o [Google Colab](https://colab.research.google.com/) ou execute localmente com Python 3.
2. Abra o arquivo `traduzindo_logica_para_python.py`.
3. Execute cada função individualmente e siga as instruções no terminal.
