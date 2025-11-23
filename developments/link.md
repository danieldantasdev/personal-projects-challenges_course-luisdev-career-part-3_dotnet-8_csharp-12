
Buscar

Notificações
99+

Carreira
Desafios - Projetos Pessoais
Desafios

Projeto 3: Gerenciador de Avaliação de Livros
Desenvolver um sistema (API ou Full-Stack) de avaliação de livros, baseado no GoodReads.

Gerenciamento de Livros (Cadastro, Atualização, Remoção, Listagem, Detalhes)
Validar dados.
Criar um endpoint que integra API externa para consulta de livro. (PLUS)
Criar um endpoint que permite subir um arquivo de imagem de capa de livro (PLUS)
Gerenciamento de Usuário (Cadastro, Atualização, Remoção, Listagem, Detalhes com Avaliação daquele usuário)
Validar dados.
Cadastro e Listagem de Avaliação para determinado Livro
Validar dados.
Relatórios
Gerar um relatório sobre a quantidade de livros lidos naquele ano.. (PLUS)


Criar Publicação no LinkedIn

Cumprimentar
Comunicar que está iniciando um projeto como parte do Treinamento (me marcando https://www.linkedin.com/in/luisdeol/)
Falar Sobre o Projeto
Concluir falando que vai publicando na rede sobre as evoluções do Projeto


Regras de negócio
Data de início não pode ser maior que fim de leitura, ao cadastrar a Avaliação
Livros não podem ser cadastrados tendo o mesmo ISBN
Nota deve ser de 1 a 5


Entidades e Dados
Livro
Id (int)
Título (string)
Descrição (string)
ISBN (string)
Autor (string)
Editora (string)
Genero (Enum GeneroLivroEnum)
AnoDePublicacao (int)
QuantidadePaginas (int)
DataCriacao (datetime)
NotaMedia (decimal) // PLUS: A cada cadastro de avaliação poderá ser calculada a média e esse cmapo atualizado
CapaLivro (bytes) // PLUS: nesse caso pode armazenar a imagem em string de bytes diretamente mesmo, não é o ideal em cenários mais reais mas nos atende perfeitamente
Avaliações (List<Avaliacao>)


Avaliacao
Id (int)
Nota (int) // de 1 a 5
Descrição (string)
IdUsuario (int)
IdLivro (int)
DataCriacao (datetime)


Usuario
Id (int)
Email (string)
Nome (string)
Avaliações (List<Avaliacao>)




Stack / Padrões
Nível Básico I: Aplicação Console
Nível Básico II
ASP NET Core API
Entity Framework Core
POO
Banco em memória
Nível Intermediário
Fluent Validation
Padrão Repository
Middleware (Lidar com exceções)
InputModel, ViewModel, DTO’s (Modelos de entrada e saída de dados)
IEntityTipeConfiguration (mapear as entidades separadamente)
Sql Server ou SqLite
Nível Avançado
Unit Of Work
HostedService
Domain Event
CQRS
Teste Unitários
Arquitetura Limpa
Como você avalia este conteúdo?





Marcar como concluído
20%
2 Comentários



Mais recentes
Mais antigos
Meus comentários

Thiago Da Cruz Marcel
12 meses atrás
A Avaliacao deve ter um controller próprio ou deve ser tratada como um agregado e ficar junto com o de livros assim como no exemplo da formação aspnet com os comments?
 
[Equipe LuisDev] Francisco Victor
12 meses atrás
Fica a seu critério, Thiago! Criar uma nova controller só para o agregado também não tem problema.