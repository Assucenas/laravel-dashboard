## Docker Setup

Este projeto foi adaptado para funcionar corretamente em ambientes Apple Silicon (ARM).

### Ajustes realizados
- Compatibilidade ARM com `platform: linux/amd64`
- Substituição de `mysql:5.7` por `mariadb:10.6`
- Configuração de variáveis de ambiente via `.env`
- Ambiente funcional utilizando Docker Compose

### Como rodar o projeto
```bash
docker compose up -d
