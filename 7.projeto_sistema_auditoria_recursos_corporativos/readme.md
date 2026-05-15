# 🏢 Sistema de Auditoria de Recursos Corporativos
 
## 📝 Descrição do Projeto
 
Este projeto consiste em um sistema em Python para realizar auditoria e cálculo de orçamentos corporativos, utilizando **recursão**, **decorators** e **estruturas de dados aninhadas**. O sistema navega por uma hierarquia corporativa de múltiplos níveis (Matriz → Departamentos → Subdepartamentos) para consolidar orçamentos, aplicar filtros e converter valores entre moedas.
 
Desenvolvido como parte da disciplina de **Sistema de Auditoria de Recursos Corporativos**, o projeto explora recursos avançados de Python como `*args`, `**kwargs`, funções de ordem superior e a separação entre lógica de negócio e lógica de monitoramento via decorator.
 
## ⚙️ Arquitetura do Sistema
 
### 🗂️ Estrutura de Dados (Dicionário Aninhado)
```
Matriz
├── TI
│   ├── Infraestrutura → Servidores (50.000) + Segurança (30.000)
│   └── Desenvolvimento → Frontend (20.000) + Backend (25.000) + DevOps (15.000)
├── RH
│   ├── Recrutamento (10.000) + Treinamento (12.000)
│   └── Cultura → Eventos (5.000) + Brindes (2.000)
└── Financeiro (40.000)
```
 
### 🔁 Função Recursiva — `calcular_orcamento_recursivo()`
Percorre a árvore de departamentos independente de quantos níveis ela tenha:
- **Caso base:** valor é numérico → soma diretamente
- **Caso recursivo:** valor é um dicionário → chama a si mesma para o subdicionário
- Aceita `*deptos_ignorados` para excluir departamentos da soma
### 🔍 Decorator — `@auditor`
Envolve qualquer função auditada sem modificar seu código, adicionando automaticamente:
- Log de entrada com `args` e `kwargs`
- Medição de tempo de execução com `time.time()`
### 💱 Conversão de Moeda — `**kwargs`
A função principal aceita parâmetros nomeados opcionais (`moeda_destino`, `taxa_cambio`) para converter o orçamento em qualquer moeda.
 
## 🧪 Casos de Teste
 
| Teste | Descrição | Resultado |
|-------|-----------|-----------|
| **Teste 1** | Orçamento total sem filtros | USD 209.000,00 |
| **Teste 2** | Ignorando `Cultura` e `Desenvolvimento` | Soma sem esses departamentos |
| **Teste 3** | Conversão para BRL (taxa 5,20) | BRL 1.086.800,00 |
 
## 📊 Resultados e Aprendizados
 
- **Recursão para estruturas dinâmicas:** A solução recursiva funciona independente da profundidade da hierarquia — adicionar novos níveis à empresa não exige alteração no código.
- **Decorator como camada de observabilidade:** O `@auditor` é aplicado com uma linha e transforma qualquer função em uma função auditada, sem acoplamento com a lógica de negócio.
- **`*args` e `**kwargs` juntos:** A mesma função aceita lista variável de departamentos a ignorar E parâmetros nomeados de câmbio simultaneamente, demonstrando a flexibilidade da assinatura de funções em Python.
## 🚀 Tecnologias Utilizadas
 
- **Linguagem:** Python 3
- **Biblioteca:** `time`
- **Conceitos aplicados:** Recursão, decorators, `*args`, `**kwargs`, dicionários aninhados, funções de ordem superior, constantes globais, conversão de tipos
- **Ferramenta:** Google Colab
## 🔧 Como Executar
 
1. Acesse o [Google Colab](https://colab.research.google.com/) ou execute localmente com Python 3.
2. Abra o arquivo `sistema_de_auditoria_de_recursos_corporativos.py`.
3. Execute — os 3 testes rodam automaticamente e exibem o log completo de auditoria para cada cenário.
---
