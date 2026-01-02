# Laravel Dashboard - Docker Setup

Este repositório é um fork do projeto [LibreCode Laravel Dashboard](https://github.com/LibreCodeCoop/laravel-dashboard) com ajustes no Docker Compose.

## Alterações realizadas

- Ajustado para rodar em **Mac Apple Silicon (M1/M2)**.
- Atualizado para **PHP 8.2** e **MySQL 5.7**.
- Corrigidos nomes de containers e volumes para compatibilidade com Docker Compose moderno.
- Removido atributo `version` obsoleto do docker-compose.yml.

- Ao rodar a aplicação localmente, pode ocorrer o erro HTTP ERROR 500 no navegador (http://localhost:8000).
Esse erro é esperado se as dependências do Laravel (vendor/) ainda não estiverem instaladas ou se o arquivo .env não estiver configurado.

O foco deste repositório foi ajustar o Docker Compose para que a aplicação possa rodar em Mac Apple Silicon, com PHP 8.2 e MySQL 5.7.
Com o container rodando corretamente, basta instalar as dependências via Composer e gerar a APP_KEY no Laravel para que a aplicação funcione sem erro 500.
