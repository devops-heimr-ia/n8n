# 🚀 n8n com Docker + Volume Persistente

Este projeto configura e executa o [n8n](https://n8n.io), uma ferramenta de automação de workflows, com persistência de dados mesmo após reinicializações.

## 🧾 Pré-requisitos

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## 📦 Como rodar

1. Clone o repositório ou copie os arquivos:

```bash
git clone https://github.com/seu-usuario/n8n-docker.git
cd n8n-docker
```

2. Suba o ambiente com Docker Compose:

```bash
docker-compose up -d
```

3. Acesse o n8n no navegador:

```
http://localhost:5678
```

Usuário e senha padrão (editável via `docker-compose.yml`):

```
Usuário: admin
Senha: admin123
```

> ⚠️ Altere o usuário e senha padrão antes de usar em produção!

## 💾 Persistência de Dados

Todos os dados (credenciais, workflows, execuções) são armazenados em um volume Docker chamado `n8n_data`, garantindo que nada seja perdido ao reiniciar o contêiner.

## 🛠️ Comandos úteis

- **Parar e remover o contêiner (mantendo os dados):**

```bash
docker-compose down
```

- **Remover contêiner e volume (apagar tudo):**

```bash
docker-compose down -v
```

## 📅 Timezone

O contêiner está configurado para o fuso horário `America/Sao_Paulo`. Edite o valor de `TZ` se precisar de outro fuso.

---

Criado com 💡 por [Seu Nome ou Empresa]
