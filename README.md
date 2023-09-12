# Docker

O projeto tem a função de provisionar o ambiente de desenvolvimento.

### Baixar repositório

* Clonar o repositório do ambiente do projeto:

```sh
git clone git@github.com:alsalvad/tray-challenge-docker.git
```

### Baixar repositórios

* Dentro da pasta clonada haverá o ambiente de desenvolvimento local.

```sh
mkdir repository

cd repository

git clone git@github.com:alsalvad/tray-challenge-project.git
```

### Executar docker-compose

```sh
cd ..

#Construir o ambiente
docker-compose up -d

#Destruir o ambiente
docker-compose down
```

### Iniciando o trabalho

Iniciando os containers:

```sh
docker-compose start
```

### Configurar o app (Laravel)

Acessar o bash do container:

```sh
docker exec -it app bash
```

Copiar o arquivo .env:

```sh
cp .env.example .env
```

Instalar as dependências do PHP:

```sh
composer install
```


Gerar a chave da aplicação:

```sh
php artisan key:generate
```

Comandos disponíveis:

```sh
# Importa os produtos via api mercado livre
php artisan import-products

# Atualiza as visitas dos produtos
php artisan update-visits
```

### Acesso

* [Tray  Challenge](http://tray.challenge.dev.com)