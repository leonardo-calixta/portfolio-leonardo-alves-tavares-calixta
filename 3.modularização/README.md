🧩 Modularização — Sistema de Caixa
📝 Descrição do Projeto
Este projeto consiste em um sistema de caixa comercial desenvolvido com foco em modularização: a solução é dividida em 5 módulos independentes, cada um com responsabilidade única, que se comunicam entre si para realizar o processo completo de uma venda — da validação do pagamento até a emissão do recibo com o troco em notas.
Desenvolvido como parte da disciplina de Modularização, o projeto demonstra na prática como decompor um problema complexo em funções menores, reutilizáveis e de fácil manutenção, aplicando o princípio de separação de responsabilidades.
⚙️ Arquitetura dos Módulos
MóduloFunçãoResponsabilidadeMódulo 1validar_pagamento(total, pago)Verifica se o valor pago é suficiente para cobrir o total da compra. Retorna Verdadeiro ou Falso.Módulo 2calcular_troco(total, pago)Calcula o troco: troco ← pago - total. Retorna o valor do troco.Módulo 3decompor_notas(troco)Quebra o troco nas menores quantidades de notas possíveis usando as denominações [100, 50, 10, 5, 1].Módulo 4exibir_recibo(total, pago, troco, notas)Imprime o recibo formatado com cabeçalho, composição do troco em notas e rodapé.Módulo 5sistema_caixa()Módulo principal: lê os dados, valida o pagamento e orquestra a chamada dos demais módulos.
🔄 Fluxo de Execução
Início
  → Ler total_compra e valor_pago
  → Módulo 1: validar_pagamento?
      SIM → Módulo 2: calcular_troco
           → Módulo 3: decompor_notas
           → Módulo 4: exibir_recibo
      NÃO → Escrever "ERRO: Pagamento Insuficiente" → Encerrar
Fim
📊 Resultados e Aprendizados

Modularização reduz complexidade: Cada função faz apenas uma coisa, tornando o código fácil de testar e corrigir isoladamente.
Algoritmo guloso em decompor_notas: O módulo percorre as denominações do maior para o menor valor, usando divisão inteira e módulo — garantindo sempre o menor número de notas possível.
Separação entre lógica e apresentação: A validação (Módulo 1), o cálculo (Módulos 2 e 3) e a exibição (Módulo 4) são completamente independentes, permitindo alterar um sem impactar os demais.

🛠️ Tecnologias e Conceitos Utilizados

Representação: Fluxogramas por módulo + Pseudocódigo estruturado
Conceitos aplicados: Funções com parâmetros e retorno, estruturas de repetição (para cada), operadores de divisão inteira e módulo (mod), listas, mapas (dicionários)
Ferramenta: Desenvolvido manualmente (caderno) como exercício de lógica modular

🔧 Arquivos do Projeto

modulos_1_2_3_fluxograma.jpg — Fluxogramas dos módulos 1, 2 e 3
modulos_4_5_fluxograma.jpg — Fluxogramas dos módulos 4 e 5
pseudocodigo_funcoes.jpg — Pseudocódigo completo das funções
pseudocodigo_sistema_caixa.jpg — Pseudocódigo do programa principal
