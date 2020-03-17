

Projeto do Mercadinho
=====================

Kandy é dona de um mercadinho que vende doces e guloseimas. Ela gostaria de ter uma forma melhor de controlar a venda dos produtos, e pediu nossa ajuda para isso.

- [Entrada e saída](#entrada-e-saida)
	- [Boas-vindas!](#boas-vindas)
	- [Boas vindas, Alex!](#boas-vindas-alex)
	- [Indicar um produto](#indicar-um-produto)
	- [Preço do novo produto](#preco-do-novo-produto)
	- [Estoque de bala arco-íris](#estoque-de-bala-arco-iris)
- [Condições](#condicoes)


## Entrada e saída

#### Boas-vindas!

Kandy gostaria de poder saudar as clientes que entram na sua loja.

```
programa
{ 
	funcao inicio () 
	{
		escreva("Boas vindas!")
	} 
}
```


#### Boas vindas, Alex!

As boas vindas fizeram um sucesso com as clientes! Mas mesmo assim, Kandy recebeu algumas reclamações dizendo que o atendimento era muito impessoal. Ela gostaria que fosse possível saudar as clientes com os seus próprios nomes.


```
programa
{
	funcao inicio ()
	{
		cadeia nome

		escreva("Digite seu nome: ")
		leia(nome)

		escreva("Boas-vindas, ", nome, "!")
	}
}
```



#### Indicar um produto

Um novo produto surgiu nas prateleiras e Kandy gostaria de poder indicar para todos que entrassem na loja.
Mas ela precisa que guardem o nome desse produto, para que fique mais fácil trocar depois.
O produto se chama "Bala Arco-íris".

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"

		escreva("Conheça o novo produto ", produto, "!")
	}
}
```

**Um pouco mais sobre variáveis**

Variáveis são nomes que damos as coisas para ficar mais fácil de reconhecê-las. Toda variável possui um tipo.

Existem os seguintes tipos:

* **cadeia** que significa que a variável é do tipo texto (mais pra frente você entenderá o porquê deste nome estranho),
* **inteiro** para números (1,2,3...)
* **real** para números quebrados (1.5, 2.2...)

Os tipo acima podem ter outros nomes quando se trabalha com outras ferramentas de programação (como por exemplo cadeia pode ser String e etc...).

Existem outros tipos mas os acima são os principais! No nosso programa acima, **produto é uma variável!**



#### Preço do novo produto

Agora, todos que entram na loja querem saber o preço do produto novo. Podemos armazenar o preço e mostrá-lo junto com o nome?
O preço da Bala Azul é R$ 0,25.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco)
	}
}

```

**O que é esse \n?**

No código acima podemos notar um \n. Em uma frase, o \n é um símbolo que representa a quebra de linha. Sem este símbolo todas as instruções *escreva* apareceriam juntas.

*Exemplo sem quebra de linha:* Conheço novo produtoApenas R$ 2,00

*Exemplo com quebra de linha (\n):*

Conheço novo produto

Apenas R$ 2,00

#### Estoque de Bala Arco-íris

Após algumas pesquisas, descobriu-se que por algum motivo desconhecido o novo produto vende mais quando se sabe a quantidade em estoque. Além de exibir, Kandy gostaria de controlar a quantidade da mesma forma que as outras informações.
Atualmente o mercadinho possui 20 balas no estoque.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 20

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")
		escreva("Temos ", quantidade, " restante(s) no estoque!")
	}
}

```

#### Comprar produto

Chegou o grande momento! Kandy gostaria que fosse possível oferecer para o cliente comprar balas arco-íris. Precisamos que o cliente consiga dizer que gostaria de comprar uma bala.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 20
		caracter resposta

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")
		escreva("Temos ", quantidade, " restante(s) no estoque!")

		escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
		leia(resposta)
	}
}
```

## Condições

#### Obrigada por comprar!

Os clientes reclamaram que não recebem nenhuma confirmação de que compraram o produto. Kandy acha que seria bem legal mostrar uma mensagem de "Obrigada por comprar!" quando o produto é comprado.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 10
		caracter resposta

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")
		escreva("Temos ", quantidade, " restante(s) no estoque!")

		escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
		leia(resposta)

		se (resposta == 'S') {
			escreva("Obrigada por comprar! Volte sempre!")
		}
	}
}
```

**= VS ==**

Podemos notar acima que quando checamos se o usuário apertou S fazemos isso comparando se reposta == "S". Porém utilizados um sinal de "=" quando estamos dizendo que produto = "Bala de Arco-íris". Qual a diferença?

O == é sempre utilizado para operações de comparação, enquanto o = é utilizado para operações de atribuição, você quer que uma variável tenha um valor, por exemplo.

**Um pouco sobre comparação**

Nos exemplo acima estamos usando uma operação no *se* para saber se uma coisa é igual a outra.

* Quando o computador identifica coisas iguais ele responde **true** (verdadeiro em inglês).

* Quando o computador identifica coisas diferentes ele responde **false** (falso em inglês)

Então se (reposta == 'S') o computador vai analisar essa expressão e vai entender que ela é true e vai entrar no bloco desejado.

Salve seu programa e vamos abrir outro!! Vamos criar duas variáveis! 


```
programa
{
	funcao inicio ()
	{
		inteiro numeroUm = 1
		inteiro numeroDois = 2
		escreva(numeroUm == numeroDois)
	}
}
```

Perceba que o programa mostrou como saída o resultado **False ou Falso**. Dizendo que os números não são iguais.

Se substituirmos o valor 2 no programa acima por 2 teremos o resultado **True ou Verdadeiro)**.

**E se quero testar se duas coisas são diferentes?**

No exemplo acima estamos testando igualdade. E se queremos comparar se duas coisas são diferentes? Utiliza-se a mesma lógica aplicada acima só que o símbolo de diferente é !=

```
programa
{
	funcao inicio ()
	{
		inteiro numeroUm = 1
		inteiro numeroDois = 2
		escreva(numeroUm != numeroDois)
	}
}
```
Veja que quando estamos testando se variáveis são iguais este exemplo dá Falso, porém se estou testando se 1 e 2 são diferentes, o resultado é verdadeiro.


 
#### Isso dá muito trabalho!

Todas as vezes que um cliente compra uma bala, Kandy tem que mudar o valor da quantidade em estoque. Ela gostaria de saber se é possível que o estoque se atualizasse automaticamente.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 10
		caracter resposta

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")

		escreva("Temos ", quantidade, " restante(s) no estoque!")

		escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
		leia(resposta)

		se (resposta == 'S') {
				quantidade = quantidade - 1
				escreva("Obrigada por comprar! Volte sempre!")
		}
	}
}
```


#### Produto esgotado!

O sucesso da Bala Arco-íris foi tão grande que os estoques esgotam muito rápido! Temos que informar quando o produto está esgotado! Ah, e não podemos vender o produto nesses casos.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 10
		caracter resposta

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")
		se (quantidade == 0){
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade, " restante(s) no estoque!")

			escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
			leia(resposta)

			se (resposta == 'S'){
					quantidade = quantidade - 1
					escreva("Obrigada por comprar! Volte sempre!")
			}
		}
	}
}
```

#### Eu quero 5 balas!

Uma cliente entrou no mercadinho querendo comprar 5 Balas Arco-íris e teve que usar o sistema 5 vezes! Kandy quer saber se é possível comprar uma quantidade maior do que 1 por vez.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 10
		caracter resposta

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")
		
		se (quantidade == 0) {
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade, " restante(s) no estoque!\n")
			
			escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
			leia(resposta)

			se (resposta == 'S') {
					escreva("Qual a quantidade desejada? \n")
					inteiro quantidade_desejada
					leia(quantidade_desejada)

					quantidade = quantidade - quantidade_desejada
					escreva("Obrigada por comprar! Volte sempre!")
			}
		}
	}
}
```

#### Quantidade no estoque não suficiente

Um outro cliente entrou no mercadinho querendo comprar 12 Balas Arco-íris, mas há apenas 10 balas no estoque. Devemos informar que só é possível vender a quantidade em estoque.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 10
		caracter resposta

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")
		
		se (quantidade == 0) {
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade, " restante(s) no estoque!\n")
			
			escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
			leia(resposta)

			se (resposta == 'S') {
				escreva("Qual a quantidade desejada? \n")
				inteiro quantidade_desejada
				leia(quantidade_desejada)

				se (quantidade_desejada > quantidade) {
					escreva("Só foi possível comprar ", quantidade, " produtos.")
					quantidade = 0
				}
				senao {
					quantidade = quantidade - quantidade_desejada
				}

				escreva("Obrigada por comprar! Volte sempre!")
			}
		}

	}
}
```


## Vetores

#### Mais produtos!

Kandy está muito feliz com sua loja, porém ela gostaria de vender outros produtos. Ela fez uma pesquisa de mercado com seus clientes e concluiu que eles gostariam de comprar Chiclete-Menta e Bombom-Supresa. Cada produto deve ter um preço e quantidade associados.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 10

		cadeia produto2 = "Chiclete-Menta"
		real preco2 = 0.5
		inteiro quantidade2 = 5

		cadeia produto3 = "Bombom-Supresa"
		real preco3 = 1.0
		inteiro quantidade3 = 3
		
		
		caracter resposta

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")
		
		se (quantidade == 0) {
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade, " restante(s) no estoque!\n")
			
			escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
			leia(resposta)

			se (resposta == 'S') {
				escreva("Qual a quantidade desejada? \n")
				inteiro quantidade_desejada
				leia(quantidade_desejada)

				se (quantidade_desejada > quantidade) {
					escreva("Só foi possível comprar ", quantidade, " produtos.")
					quantidade = 0
				}
				senao {
					quantidade = quantidade - quantidade_desejada
				}

				escreva("Obrigada por comprar! Volte sempre!")
			}
		}

	}
}
```

#### Ixi! E agora?

Kandy colocou novos produtos porém o programa continua rodando somente com a Bala Arco Íris. Vamos mudar a bala Arco Íris para se chamar poduto1 (preço1 e quantidade1 também) e permitir que o cliente selecione a bala que deseja comprar.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 10

		cadeia produto2 = "Chiclete-Menta"
		real preco2 = 0.5
		inteiro quantidade2 = 5

		cadeia produto3 = "Bombom-Supresa"
		real preco3 = 1.0
		inteiro quantidade3 = 3

		inteiro quantidade_desejada
		
		caracter resposta

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")
		
		se (quantidade == 0) {
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade, " restante(s) no estoque!\n")
			
			escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
			leia(resposta)

			se (resposta == 'S') {
				escreva("Qual a quantidade desejada? \n")
				leia(quantidade_desejada)

				se (quantidade_desejada > quantidade) {
					escreva("Só foi possível comprar ", quantidade, " produtos.")
					quantidade = 0
				}
				senao {
					quantidade = quantidade - quantidade_desejada
				}

				escreva("Obrigada por comprar!\n")
			}
		}

		
		escreva("Conheça o novo produto ", produto2, "!\n")
		escreva("Apenas R$ ", preco2, "\n")
		
		se (quantidade2 == 0) {
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade2, " restante(s) no estoque!\n")
			
			escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
			leia(resposta)

			se (resposta == 'S') {
				escreva("Qual a quantidade desejada? \n")
				leia(quantidade_desejada)

				se (quantidade_desejada > quantidade2) {
					escreva("Só foi possível comprar ", quantidade2, " produtos.")
					quantidade2 = 0
				}
				senao {
					quantidade2 = quantidade2 - quantidade_desejada
				}

				escreva("Obrigada por comprar!\n")
			}
		}

		
		escreva("Conheça o novo produto ", produto3, "!\n")
		escreva("Apenas R$ ", preco3, "\n")
		
		se (quantidade3 == 0) {
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade3, " restante(s) no estoque!\n")
			
			escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
			leia(resposta)

			se (resposta == 'S') {
				escreva("Qual a quantidade desejada? \n")
				leia(quantidade_desejada)

				se (quantidade_desejada > quantidade3) {
					escreva("Só foi possível comprar ", quantidade3, " produtos.")
					quantidade3 = 0
				}
				senao {
					quantidade3 = quantidade3 - quantidade_desejada
				}

				escreva("Obrigada por comprar!\n")
			}
		}

		escreva("Volte sempre!\n")
	}
}
```

#### Nossa! O programa ficou enorme!


**Um pouco sobre vetores**

Uma das boas práticas de programação é evitar repetição de código. Nós, como bons programadores, queremos que o código fique mais enxuto para que outros programadores possam ler nosso código melhor!

Perceba como a palavra produto, quantidade e preço ficou repetida! Temos que consertar isso! Uma possível solução é utilizar vetores. Vetores são um conjunto de caixinhas onde, geralmente, colocamos coisas com uma(s) característica(s) em comum. 

Temos muitas variáveis chamadas de produto. Podemos colocar todos os nomes dos nossos produtos em um vetor chamado produto.

Ficaria mais ou menos assim: produto = { "Bala Arco-íris", "Chiclete-Menta", "Bombom-Supresa"}

Vamos fazer um programa separado que nos mostra o vetor:

```
programa
{
	funcao inicio()
	{
		cadeia produto[3] = { "Bala Arco-íris", "Chiclete-Menta", "Bombom-Supresa"}
	}
}
```
**Repare que no exemplo acima temos que indicar o tamanho do vetor ao construir a variável!!**

Temos agora um vetor produto e dentro desse vetor temos nossas balas em cada caixinha. Para acessar cada caixinha do vetor usamos um número chamado de índice. 

Exemplo: produto[1] deve retornar "Chiclete-Menta"! Ixi! Mas não deveria retonar "Bala Arco-íris"? Todos os vetores começam com posição zero. Logo "Bala Arco-íris" corresponde a produto[0]. Vamos imprimir os elementos do exemplo anterior:

```
programa
{
	funcao inicio()
	{
		cadeia produto[3] = { "Bala Arco-íris", "Chiclete-Menta", "Bombom-Supresa"}
		escreva(produto[0], "   ", produto[1], "   ", produto[2])
	}
}
```
**Repare que apesar do tamanho do vetor ser três, o índice só vai até o 2, pois o vetor começa em zero.**


Quais outras variáveis podemos colocar em caixinhas no nosso mercadinho? Preço e quantidade!

Então agora temos 3 vetores em nosso programa:

produto = { "Bala Arco-íris", "Chiclete-Menta", "Bombom-Supresa"}
quantidade = { 10, 5, 3 }
preco = {0.25, 0.5, 1}

Como sabemos que a quantidade 10 é referente à "Bala Arco-íris"? Simples, podemos usar o número da caixinha (que chamaremos agora de posição. Logo quantidade[0] é a quantidade de produto[0] com preco[0]!

Colocando isso em nosso programa:

```
programa
{
	funcao inicio ()
	{
		cadeia produto[3] = {"Bala Arco-íris", "Chiclete-Menta", "Bombom-Supresa" }
		real preco[3] = { 0.25, 0.5, 1.0 }
		inteiro quantidade[3] = {10, 5, 3}

		inteiro quantidade_desejada
		
		caracter resposta

		escreva("Conheça o novo produto ", produto[0], "!\n")
		escreva("Apenas R$ ", preco[0], "\n")

		se (quantidade[0] == 0) {
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade[0], " restante(s) no estoque!\n")

			escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
			leia(resposta)

			se (resposta == 'S') {
				escreva("Qual a quantidade desejada? \n")
				leia(quantidade_desejada)

				se (quantidade_desejada > quantidade[0]) {
					escreva("Só foi possível comprar ", quantidade[0], " produtos.")
					quantidade[0] = 0
				}
				senao {
					quantidade[0] = quantidade[0] - quantidade_desejada
				}

				escreva("Obrigada por comprar!\n")
			}
		}

		
		escreva("Conheça o novo produto ", produto[1], "!\n")
		escreva("Apenas R$ ", preco[1], "\n")
		
		se (quantidade[1] == 0) {
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade[1], " restante(s) no estoque!\n")
			
			escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
			leia(resposta)

			se (resposta == 'S') {
				escreva("Qual a quantidade desejada? \n")
				leia(quantidade_desejada)

				se (quantidade_desejada > quantidade[1]) {
					escreva("Só foi possível comprar ", quantidade[1], " produtos.")
					quantidade[1] = 0
				}
				senao {
					quantidade[1] = quantidade[1] - quantidade_desejada
				}

				escreva("Obrigada por comprar!\n")
			}
		}


		escreva("Conheça o novo produto ", produto[2], "!\n")
		escreva("Apenas R$ ", preco[2], "\n")

		se (quantidade[2] == 0) {
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade[2], " restante(s) no estoque!\n")

			escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
			leia(resposta)

			se (resposta == 'S') {
				escreva("Qual a quantidade desejada? \n")
				leia(quantidade_desejada)

				se (quantidade_desejada > quantidade[2]) {
					escreva("Só foi possível comprar ", quantidade[2], " produtos.")
					quantidade[2] = 0
				}
				senao {
					quantidade[2] = quantidade[2] - quantidade_desejada
				}

				escreva("Obrigada por comprar!\n")
			}
		}

		escreva("Volte sempre!\n")
	}
}
```

## Expressões Lógicas e Loops


#### Usando repetições para melhorar nosso código!

Se olharmos para o código acima vimos que ele ficou enorme. Em programação existe uma maneira de repetir códigos repetidos.

**Repetindo no infinto!!!**

Podemos começar repetindo uma frase várias vezes (se prepare para apertar stop no Portugol)

```
programa
{
	logico sempre_verdade = verdadeiro
	funcao inicio()
	{
		enquanto (sempre_verdade == verdadeiro) {
			escreva("Frase repetida \n")
		}
	}
}


```
Lembra que quando trabalhamos com condicional analisávamos uma expressão procurando saber se ela era **verdadeira** ou **falsa**? 

Perceba que no programa acima estamos usando uma variável que pode assumir só os valores falso e verdadeiro (do tipo lógico) e estamos dizendo que toda vez que sempre_verdadeiro for verdadeiro, o programa irá entrar no bloco que escreve uma frase. Porém essa expressão será sempre verdade fazendo que o programe entre em um **loop infinto**

**Isso ocorre pq ao contrário da expressão SE, a expressão enquanto irá se repetir até que a expressão dê o valor falso!
**

Como isso não ocorre no exemplo acima entramos no loop infinito!


Se dizermos que sempre_verdade for falso, o programa nunca escreverá nenhuma frase pq o programa vai analisar a expressão e sempre dará falso e não entrará no bloco.

```
programa
{
	logico sempre_verdade = falso
	funcao inicio()
	{
		enquanto (sempre_verdade == verdadeiro) {
			escreva("Frase repetida \n")
		}
	}
}
```

Podemos eliminar a variável e colocar direto o valor verdadeiro que o loop infinito irá acontecer de novo, porque no fim das contas o programa sempre lerá verdadeiro então pq usar uma variável?


```
programa
{
	funcao inicio()
	{
		enquanto (verdadeiro) {
			escreva("Frase repetida \n")
		}
	}
}
```

#### Duas expressões lógicas ajudam a enxugar nosso programa!

**De que adianta repetir algo infinitamente?**

Como programadores, queremos ter o controle sobre nossas repetições então repetir algo infinitas vezes não é tão legal.

Podemos então melhorar a vida do usuário e nem dar a chance de ele comprar um produto se o produto não está na loja (faz sentido certo? Não podemos comprar algo que não podemos ver!). Vamos pegar** um pedaço de código** que estávamos construindo e ver como fica:

```
programa
{
	funcao inicio()
	{
	   cadeia produto[3] = {"Bala Arco-íris", "Chiclete-Menta", "Bombom-Supresa" }
        real preco[3] = { 0.25, 0.5, 1.0 }
        inteiro quantidade[3] = {10, 5, 3}

        inteiro quantidade_desejada

        caracter resposta
	   enquanto (quantidade[0] > 0)
	   {

        	escreva("Conheça o novo produto ", produto[0], "!\n")
       		escreva("Apenas R$ ", preco[0], "\n")
          	escreva("Temos ", quantidade[0], " restante(s) no estoque!\n")

          	escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
          	leia(resposta)

          	se (resposta == 'S') {
              escreva("Qual a quantidade desejada? \n")
              leia(quantidade_desejada)

               se (quantidade_desejada > quantidade[0]) {
                  escreva("Só foi possível comprar ", quantidade[0], " produtos.")
                  quantidade[0] = 0
              }
              senao {
                   quantidade[0] = quantidade[0] - quantidade_desejada
              }
                escreva("Obrigada por comprar!\n")
            }
	   	}
	}
}
```

Perceba que, no programa acima, enquanto o produto estiver na loja, oferecemos ele para compra, **porém há um problema neste código. Consegue descobrir qual é?**

O usuário nunca consegue sair do programa se o produto ainda estiver disponível! Como podemos resolver isso?


#### O programa continua enorme!

Se olharmos bem, temos vários códigos repetidos. E se tivessemos uma forma de repetir um mesmo código várias vezes, com condições diferentes?

```
programa 
{
	funcao inicio() 
	{

		cadeia produto[3] = {"Bala Arco-íris", "Chiclete-Menta", "Bombom-Supresa" }
		real preco[3] = { 0.25, 0.5, 1.0 }
		inteiro quantidade[3] = {10, 5, 3}

		caracter resposta
			
		para (inteiro contador = 0; contador < 3; contador++)
		{
			escreva("Conheça o produto ", produto[contador], "!\n")
			escreva("Apenas R$ ", preco[contador], "\n")
			se (quantidade[contador] == 0) {
				escreva("Produto ", produto[contador], " esgotado!")
			}
			senao {
				escreva("Temos ", quantidade[contador], " ", produto[contador], " restante(s) no estoque!\n")
				
				escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
				leia(resposta)
	
				se (resposta == 'S') {
					escreva("Qual a quantidade desejada? \n")
					inteiro quantidade_desejada
					leia(quantidade_desejada)
	
					se (quantidade_desejada > quantidade[contador]) {
						escreva("Só foi possível comprar ", quantidade[contador], " produtos.")
						quantidade[contador] = 0
					}
					senao {
						quantidade[contador] = quantidade[contador] - quantidade_desejada
					}		
				}
				escreva("Obrigada por comprar! \n")
			}
		}
		escreva("Volte sempre! \n")
	}
}
```

#### Total da compra

#### Desconto para grandes quantidades

## Ciclos


