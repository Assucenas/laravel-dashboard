# Laravel Dashboard - Docker Setup

## Ajustes realizados

- Ajustado para rodar em **Mac Apple Silicon (M1/M2)**.
- Atualizado para **PHP 8.2** e **MySQL 5.7**.
- Nomes de containers e volumes corrigidos para compatibilidade com o Docker Compose moderno.
- Removido o atributo `version` obsoleto do `docker-compose.yml`.

## Sobre o HTTP ERROR 500

Ao rodar a aplicação localmente, pode ocorrer o erro **HTTP ERROR 500** ao acessar `http://localhost:8000`.

Esse comportamento é esperado quando:
- As dependências do Laravel (`vendor/`) ainda não foram instaladas via Composer;
- O arquivo `.env` não está configurado;
- A `APP_KEY` da aplicação ainda não foi gerada.

Nesses casos, o container e o servidor web (NGINX) estão funcionando corretamente, porém o Laravel não consegue iniciar sua aplicação internamente.

O foco deste repositório foi ajustar o **Docker Compose** para garantir compatibilidade com **Mac Apple Silicon**, utilizando **PHP 8.2** e **MySQL 5.7**.  
Com o ambiente Docker configurado, basta instalar as dependências do Laravel e gerar a `APP_KEY` para que a aplicação funcione normalmente.
