# Estante

Sistema para controlar o empréstimo de livros de uma pequena biblioteca: quais livros existem, quem está com cada um e quando ele precisa ser devolvido.

Trabalho final da disciplina de Rapid Application Development (RAD), Tecnólogo em Sistemas para Internet, Instituto Federal da Paraíba (IFPB).

## Integrantes

| Nome completo | Usuário no GitHub |
|---|---|
| Felipe Macedo | [@felipemcd](https://github.com/felipemcd) |
| José Correia | [@JoseJunior07](https://github.com/JoseJunior07) |
| Maria Luiza | [@Luizalima3](https://github.com/Luizalima3) |

## Proposta

Documento de proposta aprovado: _(colar aqui o link do Google Docs)_

## Usuários e o que cada um pode fazer

| Papel | O que pode fazer |
|---|---|
| Leitor | Criar a própria conta, buscar livros no acervo, ver se há exemplar disponível, consultar os próprios empréstimos e renovar um empréstimo. Não vê empréstimos de outros leitores e não altera o acervo. |
| Bibliotecário | Cadastrar e editar livros, registrar empréstimos e devoluções, consultar todos os empréstimos e a lista de atrasados. |

**Regras do sistema:** o empréstimo dura 14 dias; pode ser renovado uma única vez, por mais 7 dias; cada leitor pode ter no máximo 3 livros ao mesmo tempo.

## Histórias de usuário

**H1.** Como leitor, quero criar minha conta, para poder acompanhar meus empréstimos.
_Critério:_ depois de criar a conta, o leitor entra no sistema com seu e-mail e senha.

**H2.** Como leitor, quero buscar livros por título ou autor, para saber se a biblioteca tem o livro que procuro.
_Critério:_ a busca mostra os livros cujo título ou autor contém o termo digitado.

**H3.** Como leitor, quero ver quantos exemplares de um livro estão disponíveis, para saber se vale a pena ir à biblioteca buscá-lo.
_Critério:_ disponíveis = total de exemplares menos os empréstimos em aberto daquele livro.

**H4.** Como leitor, quero ver meus empréstimos com a data de devolução, para não atrasar a entrega.
_Critério:_ o leitor vê somente os próprios empréstimos; os atrasados aparecem destacados.

**H5.** Como leitor, quero renovar um empréstimo, para ficar mais 7 dias com o livro.
_Critério de recusa:_ a renovação é recusada quando o empréstimo já está atrasado ou já foi renovado uma vez.

**H6.** Como bibliotecário, quero cadastrar um livro informando a quantidade de exemplares, para que os leitores o encontrem na busca.
_Critério:_ a quantidade de exemplares precisa ser de pelo menos 1.

**H7.** Como bibliotecário, quero registrar o empréstimo de um livro para um leitor, para saber com quem está cada exemplar.
_Critério de recusa:_ o empréstimo é recusado quando o livro não tem nenhum exemplar disponível.

**H8.** Como bibliotecário, quero conferir a situação do leitor no momento do empréstimo, para não emprestar a quem já está com livros demais ou em atraso.
_Critério de recusa:_ o empréstimo é recusado quando o leitor já tem 3 livros em aberto ou tem algum empréstimo atrasado.

**H9.** Como bibliotecário, quero registrar a devolução de um livro, para que o exemplar volte a ficar disponível.
_Critério:_ após a devolução, a quantidade disponível do livro aumenta em 1.

**H10.** Como bibliotecário, quero ver a lista de empréstimos atrasados, para cobrar os leitores.
_Critério:_ a lista mostra leitor, livro e dias de atraso, do maior atraso para o menor.

## As três recusas

| História | O que o sistema não deixa acontecer | Onde está implementada |
|---|---|---|
| H5 | Renovar empréstimo atrasado ou já renovado | _(preencher)_ |
| H7 | Emprestar livro sem exemplar disponível | _(preencher)_ |
| H8 | Emprestar para leitor com 3 livros em aberto ou com atraso | _(preencher)_ |

## Tecnologia

Django 5.2 com templates Django (sem front-end separado), Python 3.12, SQLite, uv para dependências e Docker Compose para subir o sistema.

## Status

Em desenvolvimento.