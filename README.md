# Traefik

Este repositório contém uma configuração de **Traefik como proxy reverso**, usando Docker Compose.  
O setup fornece:

- HTTPS automático com Let's Encrypt
- Redirecionamento de HTTP para HTTPS
- Suporte a múltiplos domínios
- Rede compartilhada Docker para comunicação entre Traefik e Nginx

---

## Estrutura do projeto
/opt/traefik/
├─ docker-compose.yml # Compose do Traefik
├─ letsencrypt/ # Diretório de certificados
├─ traefik.yml # Configuração do Traefik

---

## Rede (Servidor Linux - Docker)

  docker network create web
  docker network connect web <nome_ou_id_do_container> #Executar para o Traefik e para os containers que irão utiliza-lo

