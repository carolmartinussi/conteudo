

Projeto do Mercadinho
=====================

Kandy é dona de um mercadinho que vende doces e guloseimas. Ela gostaria de ter uma forma melhor de controlar a venda dos produtos, e pediu nossa ajuda para isso.

Por conteúdo:

- [Entrada e saída](#entrada-e-saida)
	- [Seja Bem Vindo(a)!](#seja-bem-vindoa)
	- [Seja bem vindo(a), João](#seja-bem-vindo-joao)
	- [Indicar um produto](#indicar-um-produto)
	- [Preço do novo produto](#preco-do-novo-produto)
	- [Estoque de bala arco-íris](#estoque-de-bala-arco-iris)
- [Condições](#condicoes)
	- [Produto esgotado!](#produto-esgotado)
	- ["Temos 0 restante(s) no estoque!"?](#temos-0-restantes-no-estoque)



## Entrada e saída

#### Seja bem vindo(a)!

Kandy gostaria de poder saudar os clientes que entram na sua loja.

```
programa
{ 
	funcao inicio () 
	{
		escreva("Seja bem vindo(a)!")
	} 
}
```

#### Seja bem vindo(a), João!

As boas vindas fizeram um sucesso com os clientes! Mas mesmo assim, Kandy recebeu algumas reclamações dizendo que o atendimento era muito impessoal. Ela gostaria que fosse possível saudar os clientes com o nome deles.


```
programa
{
	funcao inicio ()
	{
		cadeia nome

		escreva("Digite seu nome: ")
		leia(nome)

		escreva("Seja bem vindo(a), ", nome, "!")
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

		escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
		leia(resposta)

		se (resposta == 'S') {
			escreva("Obrigada por comprar! Volte sempre!")
		}
	}
}
```

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

		escreva("Digite S para comprar ou qualquer outra coisa pra sair.\n")
		leia(resposta)

		se (resposta == 'S') {
				quantidade = quantidade - 1
				escreva("Obrigada por comprar! Volte sempre!")
		}
	}
}
```


------------------

Editar daqui pra baixo :)

------------------

#### Produto esgotado!

O sucesso da Bala Arco-íris foi tão grande que os estoques esgotaram muito rápido! Queremos informar os clientes que o produto está esgotado quando a quantidade for 0.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 0

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")
		escreva("Temos ", quantidade, " restante(s) no estoque!\n")
		
		se (quantidade == 0) {
			quantidade = quantidade - 1
			escreva("Produto esgotado!")
		}
	}
}
```

#### "Temos 0 restante(s) no estoque!"?

Kandy adorou a mensagem de produto esgotado, mas acha que ainda pode melhorar. Ela quer que a quantidade seja exibida apenas quando ainda houver produto em estoque.

```
programa
{
	funcao inicio ()
	{
		cadeia produto = "Bala Arco-íris"
		real preco = 0.25
		inteiro quantidade = 0

		escreva("Conheça o novo produto ", produto, "!\n")
		escreva("Apenas R$ ", preco, "\n")
		
		se (quantidade == 0) {
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade, " restante(s) no estoque!\n")
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

#### Desconto para grandes quantidades

## Ciclos


