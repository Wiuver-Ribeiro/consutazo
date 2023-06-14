# Consutazo
> Agendamento de consultas psicólogo online.

![](https://i.imgur.com/KbHcORs.png)


### Pré-requisitos

- Você precisa dos seguintes serviços instalados no seu computador:

```
GIT
Servidor WEB
PHP 7.3 || 8.0
MySQL
Composer (https://getcomposer.org/)
Laravel 6.x
```

### Instalando

- Primeiramente é necessária uma base de dados, para isso é preciso criar uma:

```
CREATE DATABASE consutazo;
GRANT ALL PRIVILEGES ON consutazo . * TO 'seu_usuario'@'localhost';
```

- Clone o projeto para sua máquina (coloque na pasta do seu servidor WEB):

```
git clone https://github.com/Wiuver-Ribeiro/consutazo.git
```

- Entre no diretório **consutazo**.
- Copie o arquivo .env.example e nomeie .env:

```
cp .env.example .env
```

- Configurar o arquivo .env com as suas informações:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nome_banco
DB_USERNAME=seu_usuario
DB_PASSWORD=sua_senha
```

- Rodar o comando para instalação (pode demorar alguns minutos):

```
composer install
```

- Rodar o comando para gerar a chave do Laravel:

```
php artisan key:generate
```

- Rodar os comandos para migrar o banco de dados com alguns dados de teste:

```
php artisan migrate --seed
```

- Dar permissão para o servidor WEB:


## Abrir o servidor backend

- Para rodar o servidor backend utilize o comando:

```
php artisan serve
```

## Utilização

- Acessando a URL do projeto, você será direcionado para a *landing page*, onde existem algumas informações sobre o consultório psicólogo e a plataforma de agendamento.

![](https://i.postimg.cc/SQ5xGpbq/01.png)

- A partir dessa página é possível fazer o *login* ou cadastrar-se. Caso queira acessar a plataforma como administrador e o comando de seed foi rodado, é possível com o email **admin@teste.com** e senha **123456**.

![](https://i.imgur.com/ltjjyaC.png)

### Administrador

Como adminitrador dentro da plataforma, é possível:

- Confirmar agendamentos solicitados por pacientes na aba **Dashboard**;
- Agendar consultas para todos os pacientes na aba **Agendamentos**;
- Criar, editar e remover Psicólogo na aba **Psicólogo**;
- Criar, editar e remover pacientes na aba **Pacientes**;
- Criar e remover administradores na aba **Administradores**;
- Alterar as informações do perfil na aba **Configurações**.

![](https://i.postimg.cc/Mpwxs6Pk/02.png)

### Paciente

Como paciente dentro da plataforma, é possível:

- Ver últimos agendamentos solicitados, confirmados e cancelador na aba **Dashboard**;
- Solicitar agendamentos de consultas na aba **Agendamentos**;
- Solicitar agendamentos de consultas por médico na aba **Psicólogo**;
- Alterar as informações do perfil na aba **Configurações**.

![](https://i.postimg.cc/wx0gWYK3/03.png)

### Psicólogo

Como psicólogo dentro da plataforma, é possível:

- Ver próximas consultadas agendadas por pacientes na aba **Dashboard**;
- Ver agendamentos de consultas na aba **Agendamentos**;
- Alterar as informações do perfil na aba **Configurações**.

![](https://i.postimg.cc/rmf39cdk/04.png)

