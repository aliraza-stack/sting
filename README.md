<div id="header" align="center">
  <img src="https://github.com/aliraxa-hub/sting/blob/master/public/coffee-sting.png" width="500"/>
</div>


<h1 align="center">COFFEE STING</h1>
<h3 align="center">Project of learning basic to advance concepts of ruby-on-rails, bootstrap, react</h3>

<hr>

[![project development work](https://img.shields.io/github/hacktoberfest/2021/aliraxa-hub/sting?color=FF&label=project%20development%20work&logo=ruby&logoColor=FF0000&style=plastic&suggestion_label=hack%20to%20be%20rfest)](https://github.com/aliraxa-hub/sting)
[![Total no of lines](https://img.shields.io/tokei/lines/github.com/aliraxa-hub/sting?label=Total%20no%20of%20lines&logo=git&style=plastic)](https://github.com/aliraxa-hub/sting)
[![Weekly Commets](https://img.shields.io/github/commit-activity/w/aliraxa-hub/sting?logo=git&style=plastic)](https://github.com/aliraxa-hub/sting)
[![Monthly Commets](https://img.shields.io/github/commit-activity/m/aliraxa-hub/sting?logo=git&style=plastic)](https://github.com/aliraxa-hub/sting)
[![Yearly Commets](https://img.shields.io/github/commit-activity/y/aliraxa-hub/sting?logo=git&style=plastic)](https://github.com/aliraxa-hub/sting)
[![Last Commet](https://img.shields.io/github/last-commit/aliraxa-hub/sting?logo=git&style=plastic)](https://github.com/aliraxa-hub/sting)

<hr>

<p align="center">
<a href="https://getbootstrap.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-plain-wordmark.svg" alt="bootstrap" width="40" height="40"/> </a> 
<a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> 
<a href="https://www.figma.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/figma/figma-icon.svg" alt="figma" width="40" height="40"/> </a> 
<a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> 
<a href="https://heroku.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/heroku/heroku-icon.svg" alt="heroku" width="40" height="40"/> </a> 
<a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> 
<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> 
<a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> 
<a href="https://www.microsoft.com/en-us/sql-server" target="_blank" rel="noreferrer"> <img src="https://www.svgrepo.com/show/303229/microsoft-sql-server-logo.svg" alt="mssql" width="40" height="40"/> </a> 
<a href="https://www.postgresql.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="postgresql" width="40" height="40"/> </a> 
<a href="https://rubyonrails.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/rails/rails-original-wordmark.svg" alt="rails" width="40" height="40"/> </a> 
<a href="https://reactjs.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="react" width="40" height="40"/> </a> 
<a href="https://www.ruby-lang.org/en/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/ruby/ruby-original.svg" alt="ruby" width="40" height="40"/> </a> 
<a href="https://sass-lang.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sass/sass-original.svg" alt="sass" width="40" height="40"/> </a> 
<a href="https://tailwindcss.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg" alt="tailwind" width="40" height="40"/> </a> </p>

<hr>

> ***Ruby version*** *3.1.2p20* <br>
> ***Rails Version*** *7.0.4* <br>
> ***Bundler version*** *2.3.22* <br>
> ***Gem version*** *3.3.7* <br>

<hr>

### Project Startup with Postgres
  - Implement this project to learn at the stage of beginning.
  ```
  rails new (project-name) --database=postgresql
  cd (project-name)
  bundle install
  ```
  - After creating the project, you need to create a database. To create a database, you need to configer 
  database.yml file. First you need to create a role with password in postgres.
  ```
  sudo -u postgres psql
  create role (role-name) with createdb login password '(password)';
  alter role (role-name) superuser
  create database (database-name) owner (role-name);
  ```

  - Configer database.yml file
  ```
  host: <%= ENV['DB_HOST'] %>
  database: <%= ENV['DEVELOPMENT_DB_NAME'] %>
  username: <%= ENV['DB_USERNAME'] %>
  password: <%= ENV['DB_PASSWORD'] %>
  ```
  - After creating a role, you need to create .ENV file and run the migrations.
  ```
  touch .env    (to create .ENV file in the project)
  ```

  - Configer .ENV file by adding these lines in the .ENV file
  ```
  DB_HOST=localhost

  # Development database
  DB_USERNAME=(role-name)
  DB_PASSWORD=(role-password)
  DEVELOPMENT_DB_NAME=(database-name)_development  (Example: STING_development)
  ```

  - Run the migrations
  ```
  rails db:migrate (to run the migrations)
  ```

  - Run the server to check everything is in working condition.
  ```
  rails s (to run the server)
  ```