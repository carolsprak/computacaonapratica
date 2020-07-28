# Criar um Menu para Aplicação em Ruby on Rails

## 1. **Criar uma menu de navegação para a página inicial** 

![Tela de login](https://2.bp.blogspot.com/-1Y2KGM7EWDI/WxgyiJH8YoI/AAAAAAAABnk/bFUWSjOfwMcRPlSGD5is5cAlvr5jHOb7wCLcBGAs/s640/Menu01.png)

**Abrir o projeto no programa Sublime 3**

```ruby
 - Criar no projeto uma nova pasta /app/views/shared/ 
 - Criar um novo arquivo 
 /app/views/shared/ _navbar.html.erb 
```

Acessar a página e copiar o código abaixo neste arquivo \_navbar.html.erb:

[**`http://getbootstrap.com/examples/navbar-static-top/`**](http://getbootstrap.com/examples/navbar-static-top/)

```markup
    <!-- Static navbar -->
    <nav class="navbar navbar-default navbar-static-top">
      <div class="container">
        <div class="navbar-header">
          <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false"  aria-controls="navbar">
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <a class="navbar-brand" href="#">Project name</a>
        </div>
        <div id="navbar" class="navbar-collapse collapse">
          <ul class="nav navbar-nav">
            <li class="active"><a href="#">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#contact">Contact</a></li>
            <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown"  role="button" aria-haspopup="true" aria-expanded="false">Dropdown  <span class="caret"></span></a>
              <ul class="dropdown-menu">
                <li><a href="#">Action</a></li>
                <li><a href="#">Another action</a></li>
                <li><a href="#">Something else here</a></li>
                <li role="separator" class="divider"></li>
                <li class="dropdown-header">Nav header</li>
                <li><a href="#">Separated link</a></li>
                <li><a href="#">One more separated link</a></li>
              </ul>
            </li>
          </ul>
          <ul class="nav navbar-nav navbar-right">
            <li><a href="../navbar/">Default</a></li>
            <li class="active"><a href="./">Static top <span class="sr-only">(current)</span></a></li>
            <li><a href="../navbar-fixed-top/">Fixed top</a></li>
          </ul>
        </div><!--/.nav-collapse -->
      </div>
    </nav>
```

**\#\# Alterar o arquivo app/views/layouts/application.html.erb:**

```markup
 ... 
 
  <body> 
 
 <%= render 'shared/navbar' %>   
    <p class="notice"><%= notice %></p>  
    <p class="alert"><%= alert %></p>        

     <div class="container">
       <%= yield %> 
   </div> 
  </body>
</html>
```

> Salvar o arquivo

**\#Iniciar o servidor**

`C:\Projetos\computacaonapratica>rails s`  


```bash
=> Booting WEBrick
=> Rails 4.2.8 application starting in development on http://localhost:3000
=> Run `rails server -h` for more startup options
=> Ctrl-C to shutdown server
[2017-09-13 05:16:16] INFO  WEBrick 1.3.1
[2017-09-13 05:16:16] INFO  ruby 2.2.6 (2016-11-15) [x64-mingw32]
[2017-09-13 05:16:16] INFO  WEBrick::HTTPServer#start: pid=18536 port=3000

```

Abrir o navegador em [http://localhost:3000/home/](http://localhost:3000/home/)

## **2. Alterar o menu de navegação**

```ruby
 Abrir o arquivo 
 /app/views/shared/_navbar.html.erb 
 
 <!-- Static navbar -->
  <nav class="navbar navbar-default navbar-static-top">
    <div class="container">
      <div class="navbar-header">
        <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
          <span class="sr-only">Toggle navigation</span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
        <a class="navbar-brand" href="#">Computação na Prática</a>
     </div>
     <div id="navbar" class="navbar-collapse collapse">
      <ul class="nav navbar-nav navbar-right">
        <% if (!user_signed_in?) %>
          <li><%= link_to "Login", new_user_session_path %> </li>
          <li><%= link_to "Cadastrar", new_user_registration_path %> </li>
        <% else %>
          <li class="dropdown">
            <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
              <%= current_user.email %> <span class="caret"></span></a>
            <ul class="dropdown-menu">
              <li><a href="#">Gerenciar cursos</a></li>
              <li><a href="#">Gerenciar reservas</a></li>
              <li><a href="#">Suas reservas</a></li>
              <li><a href="#">Seus cursos</a></li>
              <li role="separator" class="divider"></li>
              <li><%= link_to "Alterar Perfil", edit_user_registration_path %></li>
              <li><%= link_to "Sair", destroy_user_session_path, method: :delete %></li>
            </ul>
          </li>
        <% end %>
        </ul>
        <ul class="nav navbar-nav navbar-right">
          <li><a href="#">Pesquisa</a></li>
          <li class="active"><a href="#">Cursos</a></li>
          <li><a href="#">Notícias</a></li>
        </ul>
      </div><!--/.nav-collapse -->
    </div>
  </nav>  
 

```

Atualizar a página no navegador em [http://localhost:3000/home/](http://localhost:3000/home/) para ver as mudanças.

   
**\#Parar o servidor**

![Menu p&#xE1;gina inicial](https://4.bp.blogspot.com/-lLtSZlhMTis/WxgyiISdriI/AAAAAAAABno/4EpXF5UM6EEHimt98i12etndQj-xqSQPQCLcBGAs/s640/Menu02.png)

```bash
Ctrl + c 

Started GET "/" for ::1 at 2017-09-13 05:17:29 -0300
Processing by Rails::WelcomeController#index as HTML
  Rendered C:/Ruby22-x64/lib/ruby/gems/2.2.0/gems/railties-4.2.8/lib/rails/templates/rails/welcome/index.html.erb (25.7ms)
Completed 200 OK in 272ms (Views: 250.5ms | ActiveRecord: 0.0ms)
[2017-09-13 05:19:46] INFO  going to shutdown ...
[2017-09-13 05:19:46] INFO  WEBrick::HTTPServer#start done.
Exiting
Deseja finalizar o arquivo em lotes (S/N)? S

C:\Projetos\computacaonapratica>
```

