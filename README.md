
## 🏆 Sobre o Projeto

Este projeto foi desenvolvido como parte do **Bootcamp New Thinkers 2024**, uma iniciativa da **Squadra Digital** que visa capacitar talentos em tecnologia através de experiências práticas e aprendizado colaborativo. 🎓💻

O objetivo do bootcamp é preparar profissionais para enfrentar os desafios reais do mercado de TI, com foco em **boas práticas de desenvolvimento**, **inovação** e **tecnologias modernas**. 🚀

Durante o programa, aplicamos conhecimentos teóricos e práticos em formato de bootcamp com uma imersão completa em trilhas de conhecimento específicas e acompanhamento de profissionais utilizando ferramentas de ponta como **Drupal**, **DDEV**, **Docker** e **WSL**. Dá uma olhadinha no que fizemos com o drupal 11:


![Página incicial de bem vindo do site](https://github.com/Jessource/desafio-final-drupal/blob/main/assets/pagina-inicial.jpg?raw=true)
![Página incicial de bem vindo do site](https://github.com/Jessource/desafio-final-drupal/blob/main/assets/lista-cachoeiras.jpg?raw=true)
![Página incicial de bem vindo do site](https://github.com/Jessource/desafio-final-drupal/blob/main/assets/lista-parques.jpg?raw=true)
![Página incicial de bem vindo do site](https://github.com/Jessource/desafio-final-drupal/blob/main/assets/posts.jpg?raw=true)
![Página incicial de bem vindo do site](https://github.com/Jessource/desafio-final-drupal/blob/main/assets/parque.jpg?raw=true)
![Página incicial de bem vindo do site](https://github.com/Jessource/desafio-final-drupal/blob/main/assets/cachoeira.jpg?raw=true)









# 🌟 Como executar o projeto 🌟

Bem-vindo ao projeto **Desafio final Drupal**! Este repositório utiliza **DDEV** e **Docker** para criar um ambiente de desenvolvimento otimizado e funcional, especialmente em sistemas Windows com **WSL 2**. 🚀

---

## 📋 Pré-requisitos

Antes de começar, garanta que os seguintes softwares estejam instalados na sua máquina:

- **WSL 2** com Linux (recomendado: Ubuntu)  
  [Guia de instalação do WSL](https://learn.microsoft.com/pt-br/windows/wsl/install)
- **Docker Desktop** (habilitado para WSL 2)  
  [Download Docker Desktop](https://www.docker.com/products/docker-desktop)
- **DDEV**  
  [Guia de instalação do DDEV](https://ddev.readthedocs.io/en/stable/#installation)

---

## ⚙️ Configuração do Projeto

### 1️⃣ Clone o Repositório

Faça o clone deste repositório para a sua máquina local:

```bash
git clone <URL_DO_REPOSITORIO>
cd <PASTA_DO_REPOSITORIO>

2️⃣ Configure o Ambiente com DDEV

Verifique se o DDEV está instalado:
ddev --version

Configure o DDEV para o projeto:

ddev config --project-type=drupal --docroot=web --project-name=<NOME_DO_PROJETO>
Substitua <NOME_DO_PROJETO> pelo nome do seu projeto.

Inicie o ambiente:
ddev start
(Opcional) Importe um banco de dados existente:

ddev import-db --src=/caminho/para/seu_banco.sql
(Opcional) Importe os arquivos do site:

ddev import-files --src=/caminho/para/seus_arquivos
3️⃣ Configuração do Drupal
Se necessário, instale o Drupal com o comando:

ddev drush site:install
Certifique-se de ajustar os arquivos settings.php e settings.local.php para apontar para o banco de dados configurado pelo DDEV.

🌐 Acesse o Projeto
Após a configuração, o projeto estará acessível no navegador no endereço:


http://<NOME_DO_PROJETO>.ddev.site

🐳 Gerenciamento do DDEV
Iniciar o ambiente:
ddev start

Parar o ambiente:
ddev stop

Reiniciar o ambiente:
ddev restart

Acessar o terminal do contêiner:

ddev ssh
🧹 Comandos Drush
Limpar caches do Drupal:

ddev drush cr

Sincronizar banco de dados:

ddev drush sql-sync
🛠️ Solução de Problemas
Docker não está iniciando:
Certifique-se de que o Docker Desktop está em execução e configurado para WSL 2.

Problemas com o DDEV:
Reinicie o ambiente com:

ddev restart
Cache corrompido no Drupal:
Limpe os caches com:
ddev drush cr
Caso precise de mais informações, consulte os guias oficiais:

Documentação do DDEV
Drupal
📞 Suporte
Se você tiver dúvidas ou precisar de ajuda, entre em contato comigo ou crie uma issue neste repositório. 💬


