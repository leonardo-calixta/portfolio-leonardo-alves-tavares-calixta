# 📊 Auditoria de Vendas Semanais
 
## 📝 Descrição do Projeto
 
Este projeto consiste em um programa de auditoria financeira que analisa a consistência de vendas semanais com base em um limite de segurança predefinido. O objetivo principal é identificar automaticamente quando a média de vendas ultrapassa o limiar estabelecido, acionando um alerta de revisão manual para prevenção de anomalias.
 
Desenvolvido como parte da disciplina de **Modelagem de Banco de Dados**, o sistema coleta três registros de vendas, calcula a média e aplica lógica condicional para classificar o resultado como seguro ou em quarentena — ilustrando na prática o conceito de **normalização de dados** e o impacto de outliers em análises financeiras.
 
## 🚀 Tecnologias Utilizadas
 
- **Linguagem:** Python 3
- **Conceitos aplicados:** Escopo de variáveis (global/local), funções, estruturas condicionais (if/else), entrada de dados (`input`), formatação de saída (`f-string`)
- **Ferramentas:** Google Colab
## 📊 Resultados e Aprendizados
 
- **Detecção de anomalias:** O programa identifica corretamente quando a média de vendas ultrapassa o `Limite_Segurança` de R$ 1.000,00, acionando o alerta de quarentena.
- **Impacto de outliers:** Observou-se que um único valor extremo (ex: R$ 5.000,00) eleva a média de forma desproporcional, reforçando a importância da normalização antes de qualquer análise.
- **Desafios:** A maior dificuldade foi encaixar corretamente a função `analisar_vendas()`, que inicialmente não aparecia no resultado final — resolvido após ajustes de sintaxe e ordem de execução.
## 🔧 Como Executar
 
1. Acesse o [Google Colab](https://colab.research.google.com/) ou execute localmente com Python 3.
2. Abra o arquivo `projeto_auditoria_de_vendas_semanais.py`.
3. Execute o script e insira os três valores de venda quando solicitado.
4. O sistema exibirá a média calculada e o status da auditoria.
