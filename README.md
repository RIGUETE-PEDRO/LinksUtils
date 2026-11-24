# LinksUtils


Pratica
`https://github.com/RIGUETE-PEDRO/ConfirmaPresenca`


desafio
`https://drive.google.com/drive/folders/1XInOAcIe3IduOvUiyue0ES5bMx7CSErD?usp=drive_link`



# 🐳 Comandos Básicos do Docker

Material de apoio para aula introdutória sobre Docker.

## 1. Imagens Docker

| Comando | Função |
|---|---|
| `docker images` | Lista as imagens disponíveis |
| `docker pull nginx` | Baixa uma imagem |
| `docker build -t minha-imagem .` | Constrói uma imagem |
| `docker rmi minha-imagem` | Remove uma imagem |
| `docker image inspect nginx` | Exibe detalhes de uma imagem |

## 2. Contêineres

| Comando | Função |
|---|---|
| `docker ps` | Lista contêineres em execução |
| `docker ps -a` | Lista todos os contêineres |
| `docker run nginx` | Cria e inicia um contêiner |
| `docker run -d nginx` | Executa em segundo plano |
| `docker run -d -p 8080:80 nginx` | Executa com mapeamento de portas |
| `docker stop nome` | Para um contêiner |
| `docker start nome` | Inicia um contêiner parado |
| `docker restart nome` | Reinicia um contêiner |
| `docker rm nome` | Remove um contêiner parado |
| `docker logs nome` | Exibe os logs |
| `docker exec -it nome bash` | Acessa o terminal do contêiner |

## 3. Docker Compose

| Comando | Função |
|---|---|
| `docker compose up` | Inicia os serviços |
| `docker compose up -d` | Inicia em segundo plano |
| `docker compose up -d --build` | Constrói as imagens e inicia os serviços |
| `docker compose down` | Para e remove os contêineres e a rede do projeto |
| `docker compose ps` | Lista os serviços |
| `docker compose logs` | Exibe os logs |
| `docker compose logs -f` | Acompanha os logs em tempo real |
| `docker compose restart` | Reinicia os serviços |
| `docker compose build` | Constrói as imagens |

## 4. Volumes

| Comando | Função |
|---|---|
| `docker volume ls` | Lista os volumes |
| `docker volume create dados` | Cria um volume |
| `docker volume inspect dados` | Exibe detalhes |
| `docker volume rm dados` | Remove um volume |
| `docker volume prune` | Remove volumes não utilizados |

## 5. Redes

| Comando | Função |
|---|---|
| `docker network ls` | Lista as redes |
| `docker network create minha-rede` | Cria uma rede |
| `docker network inspect minha-rede` | Exibe detalhes |
| `docker network rm minha-rede` | Remove uma rede |

## 6. Informações gerais

| Comando | Função |
|---|---|
| `docker --version` | Mostra a versão |
| `docker info` | Mostra informações do Docker |
| `docker stats` | Mostra consumo de recursos |
| `docker system df` | Mostra uso de disco |
| `docker system prune` | Limpa recursos não utilizados |

---

# 7. Exercício prático: executando o Nginx

### 1. Baixar uma imagem

```bash
docker pull nginx
```

### 2. Verificar as imagens

```bash
docker images
```

### 3. Criar e executar um contêiner

```bash
docker run -d --name meu-nginx -p 8080:80 nginx
```

### 4. Verificar os contêineres

```bash
docker ps
```

### 5. Acessar no navegador

```text
http://localhost:8080
```

A página padrão do Nginx deverá aparecer.

### 6. Consultar os logs

```bash
docker logs meu-nginx
```

### 7. Entrar no contêiner

```bash
docker exec -it meu-nginx bash
```

### 8. Sair do contêiner

```bash
exit
```

### 9. Parar o contêiner

```bash
docker stop meu-nginx
```

### 10. Remover o contêiner

```bash
docker rm meu-nginx
```

---

# 8. Os 10 comandos mais importantes

1. `docker pull`
2. `docker images`
3. `docker build`
4. `docker run`
5. `docker ps`
6. `docker stop`
7. `docker start`
8. `docker logs`
9. `docker exec`
10. `docker compose up -d`

---

# 9. Observações importantes

- `-d`: executa o contêiner em segundo plano.
- `-p`: faz o mapeamento de portas.
- `-it`: permite interação com o terminal do contêiner.
- `docker stop`: para o contêiner, mas não o remove.
- `docker rm`: remove um contêiner parado.
- `docker compose down -v`: também remove os volumes do projeto, podendo apagar dados persistidos.
- Em `8080:80`, a primeira porta pertence ao computador (host) e a segunda ao contêiner.

---

**Objetivo da aula:** conhecer os principais comandos do Docker, aprender a criar e gerenciar contêineres e compreender a utilização do Docker Compose.
