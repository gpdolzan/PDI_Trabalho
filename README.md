# Representação

A base de dados em anexo está dividida em 6 classes (personagens dos Simpsons):

* bart
* homer
* lisa
* maggie
* marge
* family

A classe de cada imagem está codificada no nome das imagens. O arquivo treino.zip contem a base de treinamento enquanto o arquivo valid.zip contem as imagens para validar/testar o método desenvolvido. Uma terceira base de dados (teste.zip) sera disponibilizada para os testes finais.

Seu trabalho consiste em atribuir cada imagem da base valid.zip em uma das seis classes descritas acima. Para realizar tal tarefa, você deve extrair um vetor de características (representação) de cada imagem. As bases de treino e validação são compostas de 253 e 106 imagens, respectivamente.

Para classificar uma imagem da base de validação, você deve comparar seu vetor de características com todos os vetores de características da base de treinamento e atribuir a essa imagem a  classe da imagem com a menor distância Euclidiana da base de treinamento (1-Nearest Neighbor). Por exemplo, considere a imagem bart081.bmp da base de validação. Se após você calcular as 253 distâncias para todas as imagens da base de treinamento, a menor distância for qualquer imagem com o nome bart da base de treino, então a imagem bart081.bmp terá sido classificada corretamente. Caso contrário, ela será considerada como erro de classificação. 

Seu programa deve se chamar simpsons  e deve receber como entrada os arquivos de características de treino e validação/teste. Você não precisa entregar o programa que faz a extração de características, somente o programa que faz a classificação usando as duas bases de dados.

`simpons ./treino ./valid`

A saída do programa deve imprimir o nome das imagens da base de validação, o nome da imagem da base de treinamento com a menor distância e se a classificação foi correta (ACERTO) ou não (ERRO). Por exemplo

bart081.bmp bart005.bmp (ACERTO)
bart082.bmp family028.bmp (ERRO)
...
No final dessa lista, o programa também deve imprimir o percentual de imagens classificadas corretamente e a matriz de confusão.

AVALIAÇÃO:

A avaliação desse lab levará em consideração:

Solução implementada 
Relatório em PDF reportando quais foram os métodos de representação implementados e os resultados alcançados. 
Apresentação de 10 minutos.
OBS: O seu programa deve implementar somente a classificação usando a regra 1-NN. Mas seu relatório e apresentação podem apresentar resultados com outros métodos de classificação. Mas o 1-NN é obrigatório e serve como base de comparação entre os trabalhos.