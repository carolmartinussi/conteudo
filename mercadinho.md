

Projeto do Mercadinho
=====================

Kandy é dona de um mercadinho que vende doces e guloseimas. Ela gostaria de ter uma forma melhor de controlar a venda dos produtos, e pediu nossa ajuda para isso.

- [Entrada e saída](#entrada-e-saida)
	- [Escrever no console](#seja-bem-vindoa)
	- [Variável cadeia (String)](#indicar-um-produto)
	- [variável real](#preco-do-novo-produto)
	- [variável inteiro](#estoque-de-bala-arco-iris)
	- [ler do console](#seja-bem-vindo-joao)
- [Condições](#condicoes)
	- [Se](#produto-esgotado)
	- [Senão](#temos-0-restantes-no-estoque)

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

Agora, todos que entram na loja querem saber o preço do produto novo. Podemos armazenar o preço e mostra-lo junto com o nome?
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

#### Seja bem vindo, João!

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

## Condições

#### Produto esgotado!

O sucesso da Bala Arco-íris foi tão grande que os estoques esgotam muito rápido! Queremos informar os clientes que o produto está esgotado quando a quantidade for 0.

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
		
		se (quantidade == 0){
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
		
		se (quantidade == 0){
			escreva("Produto esgotado!")
		}
		senao {
			escreva("Temos ", quantidade, " restante(s) no estoque!\n")
		}
	}
}
```

