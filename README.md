# TOTRE — versão pronta para GitHub Pages

Esta versão preserva o sistema do arquivo `index.html` original e foi empacotada para publicação estática no GitHub Pages.

## Publicação

1. Crie um repositório vazio no GitHub.
2. Envie **todo o conteúdo desta pasta para a raiz do repositório**. Não envie a pasta por fora; `index.html` precisa aparecer na primeira tela do repositório.
3. Abra `Settings` → `Pages`.
4. Em `Build and deployment`, escolha **GitHub Actions**.
5. Abra a aba `Actions` e aguarde `Publicar TOTRE no GitHub Pages` terminar com marca verde.
6. Volte a `Settings` → `Pages` e abra a URL publicada.

## Primeiro acesso ao sistema

O sistema original solicita a URL e a chave anônima do Supabase pelo botão **Conexão Supabase**. Essas informações ficam no navegador (`localStorage`) e não são gravadas no GitHub.

Use somente a **anon/public key**. Nunca coloque a `service_role` no navegador ou no repositório.

## Atualização sem cache

Depois de publicar mudanças, abra a URL em janela anônima ou pressione `Ctrl + Shift + R`. Como esta versão possui PWA/service worker, uma versão anterior pode ficar em cache por alguns instantes.

## Estrutura

- `index.html`: sistema principal original.
- `404.html`: fallback para GitHub Pages.
- `manifest.webmanifest`: instalação como PWA.
- `sw.js`: cache básico do PWA.
- `.github/workflows/pages.yml`: publicação automática.
