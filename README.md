# Fluency Quest

Painel gamificado para acompanhar a trilha de inglês na Fluency Academy. É um site estático: funciona no GitHub Pages, sem servidor e sem banco de dados.

## Arquivos

- `index.html`: o site inteiro (trilha, XP, conquistas, login e sincronização).
- `config.js`: seu nome, usuário e o hash da senha.
- `gerar-senha.html`: página que cria o `config.js` a partir da sua senha.

## Como publicar

1. Crie um repositório no GitHub (por exemplo, `fluency-quest`).
2. Envie os três arquivos: **Add file › Upload files**.
3. Em **Settings › Pages**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)` e salve.
4. Em um ou dois minutos o site fica em `https://SEU-USUARIO.github.io/fluency-quest/`.

## Criar seu login

1. Abra `https://SEU-USUARIO.github.io/fluency-quest/gerar-senha.html`.
2. Preencha nome, usuário e senha (mínimo de 10 caracteres) e clique em **Gerar config.js**.
3. Baixe o arquivo e substitua o `config.js` do repositório por ele.
4. Espere a página atualizar e entre no site.

Para trocar a senha, repita os passos. Quem estava conectado precisa entrar de novo.

## Onde o progresso fica salvo

- **Neste navegador**, sempre (localStorage).
- **Na sua conta do GitHub**, se você conectar um token: o site cria um gist secreto chamado `fluency-quest.json` e salva lá a cada mudança. Assim o celular e o computador mostram o mesmo progresso.
  - Crie o token em **Settings › Developer settings › Personal access tokens › Fine-grained tokens**, com **Account permissions › Gists: Read and write**. Nenhuma outra permissão é necessária.
  - No site, clique em “Salvo neste navegador”, cole o token e clique em **Conectar**. Faça isso uma vez em cada aparelho.
- **Backup em arquivo**: no mesmo menu, **Baixar backup** e **Restaurar backup**.

No primeiro acesso o site já começa com o progresso que você tinha no artifact do Claude (39 itens concluídos, até 28/10/2026).

## Sobre a segurança

O login protege sua página de olhares curiosos, mas não é uma trava de banco. Em um repositório público qualquer pessoa pode ver o código e o hash da senha. Por isso:

- use uma senha longa e que você não use em nenhum outro lugar;
- não coloque o token do GitHub no código: ele fica só no navegador de cada aparelho;
- em computador compartilhado, desmarque “Manter conectado” e desconecte o GitHub ao sair.
