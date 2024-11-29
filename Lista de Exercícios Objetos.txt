# Lista de Exercícios: Objetos em Javascript

1. Crie um objeto chamado `livro` com as propriedades `titulo`, `autor` e `paginas`. Em seguida, exiba cada propriedade no console usando a notação de ponto e a notação de colchetes.

2. Adicione uma nova propriedade chamada `editora` ao objeto `livro` criado na questão anterior. Modifique o valor da propriedade `titulo` e remova a propriedade `autor`. Exiba o objeto atualizado no console.

3. Crie um objeto chamado `carro` com as propriedades `marca`, `modelo` e `ano`. Adicione um método chamado `descricao` que retorna uma string no formato: "Este carro é um [marca] [modelo] do ano [ano]". Exiba o resultado do método no console.

4. Crie um objeto chamado `aluno` com as propriedades `nome`, `idade` e `matriculado` (com valores booleanos). Use um `for...in` para iterar sobre o objeto e exibir as chaves e os valores no console.

5. Crie dois objetos chamados `usuario1` e `usuario2` com as propriedades `nome` e `idade`. Combine os dois objetos em um único objeto chamado `usuarios`, utilizando o spread operator. Exiba o objeto resultante no console.

6. Utilize o método `Object.keys()` para obter todas as chaves de um objeto chamado `produto` com as propriedades `nome`, `preco` e `estoque`. Exiba as chaves no console.

7. Crie um objeto chamado `config` com as propriedades `tema` e `idioma`. Use o método `Object.freeze()` para impedir alterações no objeto e, em seguida, tente modificar o valor da propriedade `tema`. Exiba o objeto no console para verificar se a alteração foi aplicada.

8. Crie um objeto chamado `pessoa` com as propriedades `nome` e `idade`. Use o método `Object.seal()` para impedir a adição ou remoção de propriedades, mas permita a modificação dos valores existentes. Modifique o valor da propriedade `nome` e tente adicionar uma nova propriedade chamada `cidade`. Exiba o objeto no console.

9. Crie um objeto chamado `calculadora` com os métodos `somar(a, b)` e `multiplicar(a, b)`. Use esses métodos para somar e multiplicar dois números, e exiba os resultados no console.

10. Crie um objeto chamado `agenda` que armazena informações sobre uma pessoa: `nome`, `telefone` e `email`. Crie uma função fora do objeto que receba este objeto como parâmetro e exiba uma mensagem formatada com todas as informações da pessoa.

11. Crie um objeto chamado `biblioteca` que possui uma propriedade `livros` (um array de objetos). Cada objeto no array deve representar um livro, com as propriedades `titulo` e `autor`. Adicione um método ao objeto `biblioteca` chamado `listarLivros` que exibe o título e o autor de cada livro.

12. Crie um objeto chamado `estoque` com produtos como propriedades, onde cada propriedade é um nome de produto e o valor é a quantidade em estoque. Escreva uma função que recebe o nome de um produto como parâmetro e verifica se ele está disponível no estoque.

13. Crie um objeto chamado `filme` com as propriedades `titulo`, `diretor` e `ano`. Adicione uma propriedade chamada `atores` contendo um array com nomes de atores. Adicione um método chamado `descricaoCompleta` que retorna uma string descrevendo o filme, incluindo o título, diretor, ano e atores.

14. Crie um objeto chamado `pedido` com as propriedades `numeroPedido`, `cliente` e `itens` (um array de objetos, onde cada objeto representa um item com `nome` e `quantidade`). Adicione um método chamado `resumoPedido` que retorna o número do pedido e o nome de todos os itens.

15. Crie um objeto chamado `jogador` com as propriedades `nome` e `pontuacao`. Adicione um método chamado `adicionarPontos` que aumenta a pontuação do jogador em um valor especificado como parâmetro. Teste o método e exiba o resultado no console.

