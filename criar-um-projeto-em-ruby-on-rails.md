---
description: 'Nessa aula, será apresentado a criação do projeto Computação na Prática.'
---

# Criar um projeto em Ruby on Rails

## 1. Criar um projeto em Rails

Acessar o diretório um diretório qualquer no terminal e executar o seguinte comando:  
  
Por exemplo:

```text
C:\Projetos>rails new computacaonapratica
```

  
Abrir o diretório criado "computacaonapratica" e visualizar todos os arquivos criados.  
      create  README.rdoc      create  Rakefile      create  config.ru      create  .gitignore      create  Gemfile      create  app      create  app/assets/javascripts/application.js      create  app/assets/stylesheets/application.css      create  app/controllers/application\_controller.rb      create  app/helpers/application\_helper.rb      create  app/views/layouts/application.html.erb     ...

## 2. Acessar o diretório do projeto criado

No terminal entrar no diretório criado e instale o bundle no projeto:  
  
Por exemplo:

```text
C:\Projetos>cd computacaonapratica
```

Abrir o arquivo Gemfile em um editor de texto, alterar a gem sqlite3 para:

```text
gem 'sqlite3', '< 1.4'
```

No terminal entrar no diretório criado e instale o bundle no projeto:  


```text
C:\Projetos\computacaonapratica>bundle install 
```

  
Descrição de cada pasta criada no projeto:

| Pasta | Propósito |
| :--- | :--- |
| app/ | Contém os controllers, models, views, helpers, mailers e assets. |
| bin/ | Contém o rails script que inicia sua aplicação e pode conter outros scripts configuráveis: update, deploy ou executar sua aplicação. |
| config/ | Configura sua aplicação relacionado as rotas, banco de dados, etc. |
| config.ru | Usado para iniciar a aplicação. |
| db/ | Contém o esquema da sua base de dados e também as migrations. |
| GemfileGemfile.lock | Este arquivo permite especificar quais "gems" são dependentes na sua aplicação Rails. Estes arquivos são usados no momento de executar o Bundler gem. |
| lib/ | Módulos de extensão da aplicação, novas bibliotecas prontas para serem incluídadas na aplicação. |
| log/ | Arquivos de log da aplicação. |
| public/ | Diretório onde o seu conteúdo estará disponível na aplicação, como arquivos de imagem. |
| app/assets | Diretório onde se encontram todos os conteúdos de configuração para o layout da página: javascripts, css, imagens. |
| app/controllers | Diretório onde se encontram os controladores da aplicação. Para cada página que houver uma ação dinâmica entre o usuário e a aplicação.  É necessário criar um arquivo "users\_controller.rb" com os respecitivos métodos que irão executar a ação e redirecionar o usuário para uma outra página ou apenas exibir uma mensagem de sucesso/alerta. |
| app/models | Diretório onde se encontram os modelos da aplicação. Para cada tabela criada no banco de dados é criado automaticamente uma classe Model.  Por exemplo: "user.rb", neste arquivo irá conter todos as referências de relacionamento com outras tabelas \(um-para-um, um-para-muitos\), validaação das colunas, se podem ser nulas ou se possuem um valor inicial. |
| app/views | Diretório onde se encontram as páginas da aplicação. Nestas páginas será possível o usuário interagir com a aplicação, através de formulários. É necessário escrever código html juntamente com métodos rails e javascripts.  Por exemplo: O arquivo user.html.erb |
| vendor/ | Neste diretório ficam aplicações criadas por terceiros, são aplicações prontas que podem ser incluídas na sua aplicação, usando apenas algum método de referência ou algum javascript. |

## 3. Iniciando servidor web

No terminal entrar no diretório do projeto criado e inicie o servidor com o seguinte comando:

```text
C:\Projetos\computacaonapratica>rails server
```

Acessar a página: [http://localhost:3000](http://localhost:3000/)Visualizar a página do Rails!Para fazer a página inicial, o prompt fazer Ctrl + c para parar o servidor, então confirme a operação.  


