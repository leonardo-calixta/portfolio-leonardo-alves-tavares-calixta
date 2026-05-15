😊 Desenhando Emojis com Dados — Smile
📝 Descrição do Projeto
Este projeto consiste em manipular listas, tuplas e dicionários usando loops aninhados para criar e modificar a "arte" de um emoji pixel a pixel. Um emoji smile 5×5 é representado como uma estrutura de dados e transformado por um filtro de sombreamento aplicado programaticamente.
Desenvolvido como parte da disciplina de Desenhando Emojis com Dados, o projeto demonstra como dados estruturados podem ser usados para representar e manipular imagens, conectando lógica de programação com visualização gráfica.
⚙️ Como Funciona
O emoji é armazenado em um dicionário Python com uma grade de tuplas RGB:
Linha 0: 🟡 🟡 🟡 🟡 🟡  (fundo)
Linha 1: 🟡 ⚫ 🟡 ⚫ 🟡  (olhos)
Linha 2: 🟡 🟡 🟡 🟡 🟡  (fundo)
Linha 3: 🟡 ⚫ ⚫ ⚫ 🟡  (boca)
Linha 4: 🟡 🟡 🟡 🟡 🟡  (fundo)
O código percorre a estrutura em 3 níveis de loop aninhado:
NívelIteraçãoAçãoNível 1Dicionário (emoji_data)Localiza a chave "grade"Nível 2Linhas da gradePercorre cada linha do emojiNível 3Pixels da linhaAplica o filtro em cada pixel
Filtro de sombreamento: Todo pixel amarelo (255, 255, 0) tem seu brilho reduzido em 50% usando divisão inteira → (127, 127, 0). Pixels pretos são mantidos inalterados.
📊 Resultados e Aprendizados

Dicionários como estrutura de dados visual: Representar uma imagem como um dicionário de listas de tuplas mostrou como estruturas de dados complexas podem modelar problemas não convencionais.
Loops aninhados com propósito real: Cada nível de iteração tinha uma responsabilidade clara — iterar o dicionário, depois as linhas, depois os pixels.
Imutabilidade de tuplas: Para modificar um pixel, foi necessário criar uma nova tupla com os valores alterados, não editar a original — reforçando o conceito de imutabilidade em Python.
Visualização com matplotlib: O plt.imshow() renderiza a grade de tuplas RGB diretamente como imagem, conectando estruturas de dados à representação visual.

🚀 Tecnologias Utilizadas

Linguagem: Python 3
Bibliotecas: matplotlib
Conceitos aplicados: Dicionários, listas, tuplas, loops aninhados (for em 3 níveis), divisão inteira (//), condicionais, manipulação de estruturas de dados
Ferramenta: Google Colab

🔧 Como Executar

Acesse o Google Colab ou execute localmente com Python 3.
Certifique-se de ter o matplotlib instalado: pip install matplotlib.
Abra o arquivo smile.py e execute — o emoji sombreado será exibido como imagem.
