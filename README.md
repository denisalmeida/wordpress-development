# Desenvolvimento Wordpress

## Introdução:

Bem-vindo! Neste projeto compartilho minhas experiências e habilidades, com foco em:

- Desenvolvimento de temas e plugins personalizados.
- Woocommerce e suas integrações.
- Criação e consumo de APIs.
- Clean Code, SOLID e OOP (Programação orientada a objetos).
- Design modular com foco na reutilização eficiente de código.
- Design responsivo e compatibilidade entre navegadores.
- Integração com meios de pagamento e serviços de terceiros.
- Conhecimento da arquitetura e melhores práticas do WordPress.


## Tecnologias:

- Wordpress
- Woocommerce
- ACF - Advanced Custom Fields
- PHP
- Node.js
- MySQL
- API Rest
- HTML, CSS, LESS, TailwindCSS, JavaScript, jQuery, GruntJS
- Docker
- Git
- GitHub Actions
- CI/CD


## Requisitos

Certifique-se de ter as versões mais recentes do **Docker**, **Docker Compose** e **Node.js** instaladas em sua máquina.

Clone este repositório ou copie os arquivos deste repositório para uma nova pasta. No arquivo **docker-compose.yml** você pode alterar o endereço IP (caso execute múltiplos contêineres) ou o banco de dados de MySQL para MariaDB.

[adicionar seu usuário ao `docker` group](https://docs.docker.com/install/linux/linux-postinstall/#manage-docker-as-a-non-root-user) ao usar o Linux.


## Configuração

Copie o ambiente de exemplo `.env`

```
cp .env.example .env
```
Edite o `.env` para alterar as variaveis de ambiente.


## Instalação

Para instalar e rodar em ambiente local, siga as instruções abaixo:

Clone o repositório e inicialize o docker :

```
git clone https://github.com/denisalmeida/wordpress-dev.git
cd wordpress-dev
docker-compose up -d
```

A estrutura da aplicação será criada na raiz do projeto.

Os contêineres agora estão construídos e em execução. Você deve conseguir acessar a instalação do WordPress com o IP configurado no endereço do navegador. Por padrão, é `http://127.0.0.1`.

Para maior comodidade, você pode adicionar uma nova entrada no seu arquivo hosts.


## Uso

### Incializando containers

Você pode iniciar os contêineres com o  comando `up` no modo daemon (adicionando `-d` como argumento) ou usando o comando `start`:

```
docker-compose start
```

### Parando containers

```
docker-compose stop
```

### Removendo containers
Para parar e remover todos os contêineres, use o comando `down`:

```
docker-compose down
```

Use `-v` se precisar remover o volume do banco de dados que é usado para persistir o banco de dados:

```
docker-compose down -v
```

### Para projeto existentes
Copie o arquivo `docker-compose.yml` para um novo diretório.

Agora você pode usar o comando `up`:

```
docker-compose up
```

Isso criará os contêineres e irá popular o banco de dados com o dump fornecido. Você pode definir sua entrada de host e alterá-la no banco de dados, ou simplesmente substituir `wp-config.php` adicionando:

```
define('WP_HOME','http://wp.docker');
define('WP_SITEURL','http://wp.docker');
```

### Adminer

Você também pode visitar `http://127.0.0.1:8080` para acessar a interface de banco de dados Adminer, depois de iniciar os contêineres.

O nome de usuário default é `root`, e a senha é a mesma fornecida no arquivo `.env`.


# Authors

*   [Denis Almeida](https://denisalmeida.com)
