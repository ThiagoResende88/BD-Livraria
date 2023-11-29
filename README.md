### Biblioteca Online - Sistema de Gerenciamento

#### Descrição:

Este projeto propõe um sistema de gerenciamento para bibliotecas, visando otimizar o controle de empréstimos, devoluções, além do cadastro de livros, autores, usuários e editoras.

#### Entidades:

1. **Livro:**
   - **Atributos:** ISBN (chave primária), Título, Ano de Publicação, Quantidade Disponível.

2. **Autor:**
   - **Atributos:** ID (chave primária), Nome, Nacionalidade.

3. **Usuário:**
   - **Atributos:** ID (chave primária), Nome, Endereço, E-mail.

4. **Empréstimo:**
   - **Atributos:** ID (chave primária), Data de Empréstimo, Data de Devolução, Status.

5. **Editora:**
   - **Atributos:** ID (chave primária), Nome, Endereço.

#### Relacionamentos:

- **Livro - Autor (Muitos para Muitos - N:N):**
  - Um livro pode ter vários autores, e um autor pode escrever vários livros.

- **Empréstimo - Livro (Muitos para Um - N:1):**
  - Vários livros podem ser emprestados em um único empréstimo, mas um livro só pode ser emprestado uma vez por empréstimo.

- **Empréstimo - Usuário (Muitos para Um - N:1):**
  - Vários empréstimos podem ser feitos por um usuário, mas um empréstimo pertence a apenas um usuário.

#### Modelagem Conceitual (DER):

![image](https://github.com/ThiagoResende88/BD-Livraria/assets/117482959/96c0ce06-4286-4b69-a070-ff63650e3574)
[https://drive.google.com/file/d/1Z0amxrYavlkSgF-G2LYSI0tl2tDJBkcC/view?usp=sharing]

#### Modelagem Lógica:

1. **Tabela Livro:**
   - ISBN (PK, varchar)
   - Título (varchar)
   - Ano de Publicação (int)
   - Quantidade Disponível (int)

2. **Tabela Autor:**
   - ID (PK, int)
   - Nome (varchar)
   - Nacionalidade (varchar)

3. **Tabela Usuário:**
   - ID (PK, int)
   - Nome (varchar)
   - Endereço (varchar)
   - E-mail (varchar)

4. **Tabela Empréstimo:**
   - ID (PK, int)
   - Data de Empréstimo (date)
   - Data de Devolução (date)
   - Status (varchar)
   - ID_Livro (FK para Tabela Livro)
   - ID_Usuário (FK para Tabela Usuário)

5. **Tabela Editora:**
   - ID (PK, int)
   - Nome (varchar)
   - Endereço (varchar)

#### Modelagem Física:


#### Dados:


#### CRUD:


#### Relatórios:
  
