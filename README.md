# JundBio - Conectando Pessoas e Natureza na Serra do Japi

![Logo JundBio](assets/logo.png)  JundBio é uma plataforma web dedicada à documentação, visualização e preservação da rica biodiversidade da Serra do Japi, localizada em Jundiaí, São Paulo. O projeto visa criar uma comunidade engajada de entusiastas da natureza, pesquisadores e especialistas, facilitando o compartilhamento de informações, avistamentos de espécies e promovendo a conscientização ambiental.

## 🌿 Sobre o Projeto

A Serra do Japi é um importante remanescente de Mata Atlântica no interior paulista, abrigando uma vasta gama de fauna e flora. O JundBio surge como uma ferramenta para:

* **Documentar:** Permitir que usuários registrem suas observações de espécies (fauna e flora) através de postagens com fotos, descrições e localização geográfica.
* **Informar:** Oferecer um catálogo detalhado de espécies encontradas na região, com informações sobre nome comum, nome científico, família, classificação, status de conservação e descrição.
* **Conectar:** Criar um espaço para que a comunidade interaja, comente postagens e compartilhe conhecimento.
* **Mapear:** Visualizar a distribuição geográfica dos avistamentos e atropelamentos em um mapa interativo, auxiliando na identificação de áreas de maior ocorrência ou risco.
* **Engajar:** Incentivar a participação através de um sistema de gamificação com níveis e conquistas baseados na contribuição do usuário.
* **Preservar:** Fornecer dados valiosos que podem ser utilizados por pesquisadores e órgãos ambientais para estudos e ações de conservação.

## ✨ Funcionalidades Principais

* **Cadastro e Login de Usuários:** Sistema de autenticação para participação na plataforma.
* **Criação de Postagens:** Usuários podem criar postagens sobre avistamentos ou atropelamentos, adicionando:
    * Texto descritivo
    * Múltiplas fotos
    * Tipo de postagem (ex: Avistamento, Atropelamento)
    * Espécie observada (opcional, selecionada de uma lista)
    * Localização geográfica (manual, automática ou selecionada no mapa)
* **Visualização de Postagens:**
    * Feed principal com as postagens mais recentes, mais curtidas ou mais comentadas.
    * Página de detalhes da postagem com todas as informações, fotos, mapa de localização e seção de comentários.
* **Catálogo de Espécies:**
    * Listagem de espécies com filtros (tipo, status de conservação) e busca.
    * Página de detalhes da espécie com nome comum/científico, classificação, família, ordem, habitat, descrição, status de extinção, galeria de fotos e mapa de distribuição dos avistamentos.
* **Mapa Interativo:**
    * Visualização de todas as postagens (avistamentos, atropelamentos) e registros de espécies georreferenciados.
    * Filtros para exibir diferentes tipos de marcadores.
    * Clusters de marcadores para melhor visualização em áreas com muitas ocorrências.
* **Perfis de Usuário:**
    * Visualização de informações do usuário, biografia, ocupação.
    * Sistema de níveis e pontos com base na participação.
    * Conquistas (medalhas) por marcos alcançados (ex: número de fotos, curtidas, comentários).
    * Listagem das postagens criadas pelo usuário.
    * Edição de perfil e foto.
* **Interações Sociais:**
    * Curtir postagens.
    * Comentar em postagens.
* **Painel Administrativo:**
    * Dashboard com estatísticas gerais (total de espécies, usuários, posts, comentários).
    * Gerenciamento de espécies (cadastro, edição, exclusão).
    * Gerenciamento de usuários (visualização, alteração de status e tipo).
    * Moderação de postagens (aprovação ou negação de postagens pendentes).

## 🛠️ Tecnologias Utilizadas

* **Frontend:**
    * HTML5
    * CSS3 (com estrutura modular)
    * JavaScript (para interatividade, como curtidas e mapas)
    * [Leaflet.js](https://leafletjs.com/) para mapas interativos.
    * [Font Awesome](https://fontawesome.com/) para ícones.
* **Backend:**
    * PHP
* **Banco de Dados:**
    * MySQL
* **Servidor (Ambiente de Desenvolvimento Comum):**
    * XAMPP ou similar (Apache, MySQL, PHP)

## 🏗️ Estrutura do Projeto

O projeto está organizado da seguinte forma:

JundBio/
├── admin/                # Arquivos do painel administrativo
│   ├── especies.php
│   ├── index.php
│   ├── postagens.php     # Gerenciamento de postagens (recém-criado)
│   ├── usuarios.php
│   └── ...               # Outros arquivos de administração
├── assets/               # Imagens estáticas, logos, etc.
│   └── team/
├── css/                  # Arquivos de estilo
│   ├── modules/          # Módulos CSS (variáveis, global, botões, etc.)
│   ├── pages/            # CSS específico para cada página
│   ├── admin.css         # Estilos do painel administrativo
│   └── main.css          # Arquivo CSS principal que importa os módulos
├── functions/            # Funções PHP reutilizáveis (getters, inserts, updates, validações)
├── js/                   # Arquivos JavaScript
│   └── curtir.js
├── layouts/              # Partes reutilizáveis do layout (header, footer, navbar, alerts)
├── uploads/              # Diretório para uploads de usuários (avatares, fotos de postagens)
│   ├── avatars/
│   └── posts/
├── .htaccess             # Configurações do servidor Apache (ex: URLs amigáveis)
├── 404.php               # Página de erro 404
├── cadastro.php
├── Codigo.sql            # Script SQL para criação do banco e tabelas
├── database.php          # Configuração e conexão com o banco de dados
├── editar_perfil.php
├── especies.php
├── index.php             # Página inicial / Feed de postagens
├── login.php
├── logout.php
├── mapa.php
├── perfil.php
├── postar.php
├── privacidade.php       # Página de Política de Privacidade
├── sobre.php             # Página Sobre o Projeto
├── termos.php            # Página de Termos de Uso
├── verespecie.php
├── verpost.php
└── README.md             # Este arquivo



## 🚀 Como Executar o Projeto (Desenvolvimento)

1.  **Pré-requisitos:**
    * Servidor web local com PHP e MySQL (Ex: XAMPP, WAMP, MAMP, Laragon).
    * Um navegador web.
    * Um cliente MySQL (Ex: phpMyAdmin, DBeaver, MySQL Workbench) para importar o banco.

2.  **Configuração:**
    * Clone ou baixe este repositório para o diretório `htdocs` (XAMPP) ou o diretório web equivalente do seu servidor e altere o nome para `JundBio`.
    * **Banco de Dados:**
        * Crie um banco de dados chamado `jundbio` (ou o nome definido em `database.php`).
        * Importe o arquivo `Codigo.sql` para criar as tabelas e inserir dados iniciais (como o usuário administrador e a espécie "Desconhecido").
        * Verifique as credenciais de acesso ao banco de dados no arquivo `database.php` e ajuste-as se necessário para o seu ambiente.
    * **Permissões:** Certifique-se de que o servidor web tenha permissão de escrita nos diretórios `uploads/avatars/` e `uploads/posts/` para o upload de imagens.

3.  **Acesso:**
    * Inicie seu servidor Apache e MySQL.
    * Acesse o projeto no seu navegador, geralmente através de `http://localhost/JundBio/` (o caminho pode variar dependendo de onde você colocou os arquivos).

4.  **Credenciais de Administrador Padrão:**
    * **Email:** `admin@jundbio.com`
    * **Senha:** `admin123`
    * Acesse o painel administrativo em `http://localhost/JundBio/admin/`.

## 🤝 Contribuição

Este projeto é desenvolvido para fins avaliativos. No entanto, sugestões e ideias para melhorias são bem-vindas!

## 👨‍💻 Equipe

* Luan Pascoal
* Tomás Wong
* Heitor Lima
* Eric Rodrigues
* Vinícius Tega


