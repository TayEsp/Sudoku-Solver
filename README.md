# Sudoku-Solver
Trabalho para a disciplina de Projeto e Analise de Algoritmos

1- Problema abordado: 

  O problema deste trabalho foi desenvolver um algoritmo de força bruta utilizando backtracking para resolver o jogo chamado Sudoku. O jogo consiste em colocar números de 1 a 9 em uma matriz 9x9, mas o mesmo número não pode ser encontrado na mesma linha, coluna e no quadrante de 3x3. 
  O paradigma usado foi o de força bruta com backtracking, que compõe-se  em achar uma solução para o problema testando os candidatos parciais possíveis, enquanto constrói uma árvore profunda, onde cada ramificação é uma tentativa de um possível candidato, portanto é realizada uma busca por profundidade. 

2- Explicando o que o código faz: 

O nosso código foi pensado utilizando uma pilha implícita de recursão onde é verificado os numero de 1 a 9 em cada posição vaga, assim verifica se o número que está na posição vaga é válido ou não (se é ou não um possível candidato), caso seja, ele coloca o numero na matriz, e chama recursivamente a função novamente, verificando se ainda é possível andar na coluna, ou se a coluna acabou e deve se passar para a linha de baixo. Caso não seja possível colocar nenhum dos 9 números na posição, é feito o backtracking, saindo do loop e retornando falso para retirar o número da matriz, voltando como 0 e verificando os outros números ainda não verificados. Caso o número não seja um número vago, então é somado mais 1 na coluna ou na linha, seguindo a mesma lógica da função de recursão, porém sem a recursão, para a verificação do próximo número que esteja vago. Dessa forma, ou chegando ao final da matriz, o caso base é de que se a matriz não possui mais nenhum número 0, e assim é retornado verdadeiro, para todas as recursão removendo em cadeia da pilha.
  Abaixo está uma breve explicação de todas as funções que foram utilizadas durante o codigo:
  
 Função “posicao_valida”:
 
  Esta função verifica se é possível inserir um número (num) em uma posição específica de uma matriz 9x9 (matrix) que representa um jogo de Sudoku, seguindo as regras do Sudoku. As coordenadas da posição em que se deseja inserir o número são especificadas pelas variáveis lin (linha) e col (coluna).
  Primeiro vai conferir as linhas e colunas, em seguida em qual quadrado 3x3 o número se encontra para conferir se é válido ou não, se não for válida a posição o “if” retorna falso.

Função “sudoku_solver”:

  O algoritmo utiliza recursão para preencher a matriz do Sudoku com números válidos, começando pela primeira posição com 0 (ou seja, posição vaga) e continuando em direção à direita e para baixo. Ele tenta números de 1 a 9 e verifica se cada número é válido na posição atual usando a função posicao_valida. Se encontrar uma solução válida, a função retorna True. Caso contrário, ela faz um backtrack, retornando False, coloca a posição de volta como 0 e tenta o próximo número.
	
Função “validar_sudoku”:

  Esta função verifica se a matriz do Sudoku é válida antes de tentar resolvê-la. Ela percorre todas as posições com números diferentes de 0 da matriz e verifica se cada número na matriz é válido de acordo com as regras do Sudoku.

Função “print_matrix”:

  Esta função imprime a matriz do Sudoku em um formato legível.

