# Modelo para recomendar livros
Para o projeto final do bootcamp do LAMIA (Laboratório de Aprendizado de Máquina e Imagens Aplicados à Indústria) foi feito um Sistema de recomendação de livros, com um dataset do kaggle (https://www.kaggle.com/arashnic/book-recommendation-dataset) e com a biblioteca Surprise. O conjunto de dados apresentou-se difícil de trabalhar logo à primeira vista, mas foi escolhido.

A modelagem dos dados foi feita com base nas futuras análises de acordo com o modelo de dataset do Surprise, que seria: item, id do usuário e a nota. Primeiramente, foi feita a remoção dos dados que não eram convenientes, como colunas desnecessárias e dados nulos, assim como livros com notas zero. Logo após a limpeza, que constitui a parte mais longa do projeto, foi feito e exportado o dataframe final para ser usado no modelo. O dataframe final foi feito apenas com três colunas: o nome do livro, o id do usuário e a nota que o usuário deu para o livro em questão. Antes de ir para a confecção do modelo, foram feitas análises gráficas para verificar a distribuição das notas, idade dos usuários e sobre quais livros foram mais avaliados. Essa primeira etapa do projeto foi um pouco complicada de se fazer, pois tinha que tomar uma decisão difícil de retirar, ou não, mais de 60% dados totais.

[Dashboard - idades](https://github.com/felipelapadn/Modelo--recomendacao-de-livro/files/9251960/Dashboard.-.idades.pdf)

[Dashboard - idades](https://github.com/felipelapadn/Modelo--recomendacao-de-livro/files/9251965/Dashboard.-.idades.pdf)

Foram testados cerca de 10 modelos, variando do “vizinho mais próximo” até os modelos de árvores. Depois de ver o desempenho dos modelos do Scikit-Learn, resolvi não usá-los. O modelo usado foi o KNNBasic, da biblioteca Python Surprise. Foi desafiador descobrir como ele funciona, pois ele precisa de um modelo próprio do conjunto de dados, com apenas 3 variáveis. Os passos para se construir um modelo são baseados na estrutura do Surprise. Para começar, é preciso criar um leitor para os dados e usá-lo como base para criar um conjunto de dados para ser usado no modelo. Logo após, é feita a divisão dos dados em treino e teste, as previsões são geradas e testamos o modelo depois de treinado. Para recomendar os livros, é preciso gerar os vizinhos mais próximos. No final, foi recomendado dez livros para os dez primeiros usuários e criou-se um gráfico para verificar quais livros foram mais recomendados.

[Dashboard - avaliações](https://github.com/felipelapadn/Modelo--recomendacao-de-livro/files/9251931/Dashboard.-.avaliacoes.pdf)
