# Como Rodar o Mapa da Prosperidade no seu Computador

Este projeto é um aplicativo web moderno (React + Vite) e **não funciona apenas clicando no arquivo index.html**. Ele precisa de um pequeno servidor web para rodar corretamente.

Aqui estão 3 formas simples de fazer isso funcionar:

## Opção 1: Usando uma Extensão do Chrome (Mais Fácil)
Se você não quer instalar programas, use esta extensão:

1. Instale a extensão **"Web Server for Chrome"** na Chrome Web Store.
2. Abra a extensão e clique em "Choose Folder".
3. Selecione a pasta `dist/public` que está dentro do arquivo zip que você baixou (você precisa extrair o zip antes).
   - **Nota:** Se não houver pasta `dist`, você precisará usar a Opção 3 para "construir" o projeto primeiro.
4. Clique no link que a extensão gerar (ex: `http://127.0.0.1:8887`).

## Opção 2: Usando Python (Se já tiver instalado)
Se você tem Python no computador:

1. Abra o terminal (CMD ou PowerShell).
2. Navegue até a pasta onde você extraiu o projeto.
3. Entre na pasta `dist/public` (se existir) ou na raiz do projeto.
4. Digite: `python -m http.server`
5. Abra seu navegador em `http://localhost:8000`.

## Opção 3: Modo Desenvolvedor (Completo)
Para ter o projeto completo rodando como eu criei:

1. Instale o **Node.js** (baixe em nodejs.org).
2. Abra o terminal na pasta do projeto.
3. Digite `npm install` (para baixar as dependências).
4. Digite `npm run dev` (para iniciar o servidor).
5. O site abrirá em `http://localhost:3000`.

---

**Por que isso é necessário?**
Por segurança, os navegadores bloqueiam certas funcionalidades (como carregar módulos de script) quando você abre um arquivo direto do disco (`file://`). Um servidor local simula um site real (`http://`), permitindo que tudo funcione perfeitamente.
