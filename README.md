# Projeto Symfony

Este é um projeto Symfony que foi criado para aula de php da Digital College.

## Instalação

1. **Clonar o repositório:**
   ```
   git clone https://github.com/marcosaureliosl/aula_php_will.git

 2. **Instalar as dependências do Composer:**
    ```
    cd projeto-symfony
        composer install

3. **Configurar o ambiente:**
   ```
   # In all environments, the following files are loaded if they exist,
   # the latter taking precedence over the former:
   #
   #  * .env                contains default values for the environment variables needed by the app
   #  * .env.local          uncommitted file with local overrides
   #  * .env.$APP_ENV       committed environment-specific defaults
   #  * .env.$APP_ENV.local uncommitted environment-specific overrides
   #
   # Real environment variables win over .env files.
   #
   # DO NOT DEFINE PRODUCTION SECRETS IN THIS FILE NOR IN ANY OTHER COMMITTED FILES.
   # https://symfony.com/doc/current/configuration/secrets.html
   #
   # Run "composer dump-env prod" to compile .env files for production use (requires symfony/flex >=1.2).
   # https://symfony.com/doc/current/best_practices.html#use-environment-variables-for-infrastructure-configuration

   ###> symfony/framework-bundle ###
   APP_ENV=dev
   APP_SECRET=b0db7338db178654c9fef53fa1044759
   ###< symfony/framework-bundle ###

   ###> doctrine/doctrine-bundle ###
   # Format described at https://www.doctrine-project.org/projects/doctrine-dbal/en/latest/reference/configuration.html#connecting-using-a-url
   # IMPORTANT: You MUST configure your server version, either here or in config/packages/doctrine.yaml
   #
   # DATABASE_URL="sqlite:///%kernel.project_dir%/var/data.db"
   DATABASE_URL="mysql://user:password@symfony-dc-mysql:3306/symfony_dc?serverVersion=8.0.32&charset=utf8mb4"
   # DATABASE_URL="mysql://app:!ChangeMe!@127.0.0.1:3306/app?serverVersion=10.11.2-MariaDB&charset=utf8mb4"
   # DATABASE_URL="postgresql://app:!ChangeMe!@127.0.0.1:5432/app?serverVersion=16&charset=utf8"
   ###< doctrine/doctrine-bundle ###

4. ***Criar o banco de dados:***
    ```
    php bin/console doctrine:database:create
  
5. ***Aplicar as migrações do banco de dados:
    ```
     php bin/console doctrine:migrations:migrate

## Uso

1. **Iniciar o servidor de desenvolvimento:**
   ```bash
   php bin/console server:run
   ```

2. **Acessar o aplicativo no navegador:**
   ```
   http://localhost:8000
   ```

## Contribuição

Se você encontrar um problema ou tiver alguma sugestão de melhoria, sinta-se à vontade para abrir uma issue ou enviar um pull request.








