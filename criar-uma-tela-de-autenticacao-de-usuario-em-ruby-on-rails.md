# 3. Criar uma tela de autenticação de usuário em Ruby on Rails

## 1. **Entrar no projeto rails criado ComputacaoNaPratica**

```bash
C:\Projetos>cd computacaonapratica
C:\Projetos\computacaonapratica>
```

**\#Iniciar o servidor**

```bash
C:\Projetos\computacaonapratica>rails s
```

```bash
=> Booting WEBrick
=> Rails 4.2.8 application starting in development on http://localhost:3000
=> Run `rails server -h` for more startup options
=> Ctrl-C to shutdown server
[2017-09-13 05:16:16] INFO  WEBrick 1.3.1
[2017-09-13 05:16:16] INFO  ruby 2.2.6 (2016-11-15) [x64-mingw32]
[2017-09-13 05:16:16] INFO  WEBrick::HTTPServer#start: pid=18536 port=3000
```

**Abrir o navegador em http://localhost:3000/**

**\#Parar o servidor**

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

## **2. Instalar o bootstrap**

Instalar e Abrir o Sublime Text3.

Abrir o arquivo **C:\Projetos\computacaonapratica\Gemfile** e adicionar

`gem 'bootstrap-sass', '~> 3.3.6'`

{% hint style="info" %}
**S**alvar o arquivo Gemfile.
{% endhint %}

No prompt executar: 

```bash
C:\Projetos\computacaonapratica>bundle install
Fetching gem metadata from https://rubygems.org/...........
Fetching gem metadata from https://rubygems.org/..............
Fetching gem metadata from https://rubygems.org/...
Resolving dependencies...
Using rake 12.1.0
Using i18n 0.8.6
Using minitest 5.10.3
Using thread_safe 0.3.6
Using tzinfo 1.2.3
Using activesupport 4.2.8
Using builder 3.2.3
Using erubis 2.7.0
Using mini_portile2 2.2.0
Using nokogiri 1.8.0 (x64-mingw32)
Using rails-deprecated_sanitizer 1.0.3
Using rails-dom-testing 1.0.8
Using loofah 2.0.3
Using rails-html-sanitizer 1.0.3
Using actionview 4.2.8
Using rack 1.6.8
Using rack-test 0.6.3
Using actionpack 4.2.8
Using globalid 0.4.0
Using activejob 4.2.8
Using mime-types-data 3.2016.0521
Using mime-types 3.1
Using mail 2.6.6
Using actionmailer 4.2.8
Using activemodel 4.2.8
Using arel 6.0.4
Using activerecord 4.2.8
Using execjs 2.7.0
Fetching autoprefixer-rails 7.1.4
Installing autoprefixer-rails 7.1.4
Using debug_inspector 0.0.3
Using binding_of_caller 0.7.2
Using rb-fsevent 0.10.2
Using ffi 1.9.18 (x64-mingw32)
Using rb-inotify 0.9.10
Using sass-listen 4.0.0
Using sass 3.5.1
Using bootstrap-sass 3.3.7
Using bundler 1.16.0.pre.2
Using byebug 9.1.0
Using coffee-script-source 1.12.2
Using coffee-script 2.4.1
Using thor 0.20.0
Using railties 4.2.8
Using coffee-rails 4.1.1
Using concurrent-ruby 1.0.5
Using multi_json 1.12.2
Using jbuilder 2.7.0
Using jquery-rails 4.3.1
Using json 1.8.6
Using sprockets 3.7.1
Using sprockets-rails 3.2.1
Using rails 4.2.8
Using rdoc 4.3.0
Using tilt 2.0.8
Using sass-rails 5.0.6
Using sdoc 0.4.2
Using sqlite3 1.3.13 (x64-mingw32)
Using turbolinks-source 5.0.3
Using turbolinks 5.0.1
Using tzinfo-data 1.2017.2
Using uglifier 3.2.0
Using web-console 2.3.0
Bundle complete! 13 Gemfile dependencies, 62 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.

C:\Projetos\computacaonapratica>
```

Verificar que o bootstrap-sass foi instalado

**\# Configurar o bootstrap**

Renomear o arquivo app/assets/stylesheets/application.css para:

```css
app/assets/stylesheets/application.scss

Limpar todo o conteúdo do arquivo application.scss 

No arquivo application.scss adicionar:

@import "bootstrap-sprockets";
@import "bootstrap";

Abrir o arquivo app/assets/javascripts/application.js
# Adicionar o bootstrap ABAIXO de //= require jquery

//= require jquery
//= require bootstrap-sprockets
```

**\#Iniciar o servidor**

```bash
C:\Projetos\computacaonapratica>rails s
```

```bash
=> Booting WEBrick
=> Rails 4.2.8 application starting in development on http://localhost:3000
=> Run `rails server -h` for more startup options
=> Ctrl-C to shutdown server
[2017-09-13 05:16:16] INFO  WEBrick 1.3.1
[2017-09-13 05:16:16] INFO  ruby 2.2.6 (2016-11-15) [x64-mingw32]
[2017-09-13 05:16:16] INFO  WEBrick::HTTPServer#start: pid=18536 port=3000
```

Abrir o navegador em [http://localhost:3000/](http://localhost:3000/)

**\#Parar o servidor**

```bash
Ctrl + c 
```

```bash
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

## **3. Criar a página de login para usuário**

**\#\# Instalando o Devise**

No arquivo Gemfile adicionar**:**

```ruby
gem 'devise', '~> 4.2'
```

{% hint style="info" %}
**S**alvar o arquivo Gemfile.
{% endhint %}

Executar o comando:

```bash
C:\Projetos\computacaonapratica>bundle install
```

Em seguida, executar o comando: 

```text
C:\Projetos\computacaonapratica>rails g devise:install
```

```bash
create  config/initializers/devise.rb
      create  config/locales/devise.en.yml
===============================================================================

Some setup you must do manually if you haven't yet:

  1. Ensure you have defined default url options in your environments files. Here
     is an example of default_url_options appropriate for a development environment
     in config/environments/development.rb:

       config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

     In production, :host should be set to the actual host of your application.

  2. Ensure you have defined root_url to *something* in your config/routes.rb.
     For example:

       root to: "home#index"

  3. Ensure you have flash messages in app/views/layouts/application.html.erb.
     For example:

       <'p class="notice"><'%= notice %><'/p>
       <'p class="alert"><'%= alert %><'/p>

  4. You can copy Devise views (for customization) to your app by running:

       rails g devise:views

===============================================================================


```

**\# Configurar o Devise**

**\#\# Adicionar no arquivo config/environments/development.rb:**

```ruby
config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }
```

{% hint style="info" %}
**S**alvar o arquivo.
{% endhint %}

**\#\# Adicionar no arquivo config/routes.rb:**

```ruby
root 'pages#home'
```

{% hint style="info" %}
Salvar o arquivo.
{% endhint %}

**\#\# Criar a rota**

Executar o comando: 

```bash
C:\Projetos\computacaonapratica>rake routes
```

```ruby
Prefix Verb   URI Pattern       Controller#Action
        new_user_session GET    /users/sign_in(.:format)       devise/sessions#new
            user_session POST   /users/sign_in(.:format)       devise/sessions#create
    destroy_user_session DELETE /users/sign_out(.:format)      devise/sessions#destroy
           user_password POST   /users/password(.:format)      devise/passwords#create
       new_user_password GET    /users/password/new(.:format)  devise/passwords#new
      edit_user_password GET    /users/password/edit(.:format) devise/passwords#edit
                         PATCH  /users/password(.:format)      devise/passwords#update
                         PUT    /users/password(.:format)      devise/passwords#update
cancel_user_registration GET    /users/cancel(.:format)        devise/registrations#cancel
       user_registration POST   /users(.:format)               devise/registrations#create
   new_user_registration GET    /users/sign_up(.:format)       devise/registrations#new
  edit_user_registration GET    /users/edit(.:format)          devise/registrations#edit
                         PATCH  /users(.:format)               devise/registrations#update
                         PUT    /users(.:format)               devise/registrations#update
                         DELETE /users(.:format)               devise/registrations#destroy
                    root GET    /                              pages#home

```

**\#\# Criar a pasta app/views/pages**

**\#\# Criar o arquivo home.html.erb dentro da pasta app/views/pages**

Com o seguinte conteúdo:

```markup
<p>pages#home</p>
<%= link_to "Log in", new_user_session_path %> | <%= link_to "Log out", destroy_user_session_path, method: :delete %>
```

{% hint style="info" %}
Salvar o arquivo.
{% endhint %}

**\#\# Criar o controlador PagesController em app/controller/pages\_controller.rb**

Com o seguinte conteúdo:

```ruby

class PagesController < ApplicationController
  def home
      
  end

end
```

{% hint style="info" %}
Salvar o arquivo.
{% endhint %}

**\#\# No arquivo app/views/layouts/application.html.erb:**

```markup
  <html>
  ...
  
  <body>
     <p class="notice"><%= notice %></p>
     <p class="alert"><%= alert %></p>
     <%= yield %>
  </body>
 </html>
```

{% hint style="info" %}
Salvar o arquivo.
{% endhint %}

**\# Criar o model User**

```bash
C:\Projetos\computacaonapratica>rails g devise User
```

```ruby
invoke  active_record
      create    db/migrate/20170809005335_devise_create_users.rb
      create    app/models/user.rb
      invoke    test_unit
      create      test/models/user_test.rb
      create      test/fixtures/users.yml
      insert    app/models/user.rb
       route  devise_for :users
```

**\# Adicionar no Banco de Dados**

```ruby
rails 4> C:\Projetos\computacaonapratica>rake db:migrate

== 20170809005335 DeviseCreateUsers: migrating ================================
-- create_table(:users)
   -> 0.0033s
-- add_index(:users, :email, {:unique=>true})
   -> 0.0019s
-- add_index(:users, :reset_password_token, {:unique=>true})
   -> 0.0013s
== 20170809005335 DeviseCreateUsers: migrated (0.0092s) =======================
```

**\# Abrir o programa DB Browser for SQLite que está instalado na máquina**

Selecionar o esquema em "Abrir banco de dados" com o arquivo:

```text
C:\Projetos\computacaonapratica/db/development.sqlite3
```

Abrir a tabela "Users" em Navergar dados &gt; Tabela "User"

**\# Adicionar as Views**

```text
C:\Projetos\computacaonapratica>rails g devise:views
```

```text
 
Expected boolean default value for '--markerb'; got :erb (string)
      invoke  Devise::Generators::SharedViewsGenerator
      create    app/views/devise/shared
      create    app/views/devise/shared/_links.html.erb
      invoke  form_for
      create    app/views/devise/confirmations
      create    app/views/devise/confirmations/new.html.erb
      create    app/views/devise/passwords
      create    app/views/devise/passwords/edit.html.erb
      create    app/views/devise/passwords/new.html.erb
      create    app/views/devise/registrations
      create    app/views/devise/registrations/edit.html.erb
      create    app/views/devise/registrations/new.html.erb
      create    app/views/devise/sessions
      create    app/views/devise/sessions/new.html.erb
      create    app/views/devise/unlocks
      create    app/views/devise/unlocks/new.html.erb
      invoke  erb
      create    app/views/devise/mailer
      create    app/views/devise/mailer/confirmation_instructions.html.erb
      create    app/views/devise/mailer/email_changed.html.erb
      create    app/views/devise/mailer/password_change.html.erb
      create    app/views/devise/mailer/reset_password_instructions.html.erb
      create    app/views/devise/mailer/unlock_instructions.html.erb


```

**\# Iniciar o servidor e cadastrar um novo usuário**

```text
C:\Projetos\computacaonapratica>rails s
```

Acessar a página [http://localhost:3000/users/sign\_up](http://localhost:3000/users/sign_up)

[  
](https://3.bp.blogspot.com/-w3CnVTg7MH0/WdBYzhozJjI/AAAAAAAABTo/jqI-83jTlN4iNyJyAwY68x_ZjvdMjegJwCEwYBhgL/s1600/computacaonapratica_032.png)  


![](https://3.bp.blogspot.com/-w3CnVTg7MH0/WdBYzhozJjI/AAAAAAAABTo/jqI-83jTlN4iNyJyAwY68x_ZjvdMjegJwCEwYBhgL/s320/computacaonapratica_032.png)

**Cadastrar um novo usuário**

  


![](https://1.bp.blogspot.com/-KEIC-3myL0A/WdBY63XNxiI/AAAAAAAABTo/WocED9p4PTYq0KRDCjsaCxJVNBnu1sEIACEwYBhgL/s320/computacaonapratica_033.png)

**\# O sistema direciona para a página Home.**

  


![](https://3.bp.blogspot.com/-xoXlpzVidO4/WdBY69ONg8I/AAAAAAAABTo/XeGiYAtSEck5ibp_shUu79PhX6JTbJMAACEwYBhgL/s320/computacaonapratica_034.png)

**Verificar no banco de dados se o usuário foi criado com sucesso.**

  


![](https://2.bp.blogspot.com/--d_Acboaa8c/WdBY69XoB4I/AAAAAAAABTo/YAjjotmZFjYFxAGGdsvsmoLMybJxNP1jgCEwYBhgL/s320/computacaonapratica_035.png)

**\# Fazer o log out.**

  


![](https://3.bp.blogspot.com/-_ystAfACt9w/WdBY7JILXdI/AAAAAAAABTo/vD_7mVmbS8km71BGAZKWccTAbrcVJxzZgCEwYBhgL/s320/computacaonapratica_036.png)

**\# Fazer o login**

  


![](https://1.bp.blogspot.com/-oWijQBBRwVM/WdBY7SasL3I/AAAAAAAABTo/TduApvbuR7MvljhYxthXTvcCnN2YlKzqgCEwYBhgL/s320/computacaonapratica_037.png)

**\# Mensagem de login com sucesso**

![](https://4.bp.blogspot.com/-iGJC6uacpXM/WdBY7ZvINAI/AAAAAAAABTo/qd3f0mON1tk9mUmXTTkU3ZwyaFE6kxoYQCEwYBhgL/s320/computacaonapratica_038.png)

> DICA: Se houver algum erro "cannot load such file -- bcrypt\_ext", precisa alterar no arquivo Gemfile da raíz do projeto

```bash
gem 'bcrypt', git: 'https://github.com/codahale/bcrypt-ruby.git', 
:require => 'bcrypt'
```

