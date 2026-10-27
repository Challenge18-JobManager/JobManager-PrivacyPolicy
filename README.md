# JobManager-PrivacyPolicy

Política de privacidade do app (nome provisório: **Apply**), publicada no GitHub Pages.

| Idioma | Página |
|---|---|
| Português (Brasil) | https://challenge18-jobmanager.github.io/JobManager-PrivacyPolicy/ |
| English | https://challenge18-jobmanager.github.io/JobManager-PrivacyPolicy/en/ |
| Español | https://challenge18-jobmanager.github.io/JobManager-PrivacyPolicy/es/ |

A página em inglês é a que vai no campo **Privacy Policy URL** do App Store Connect.

## Estrutura

```
index.html          pt-BR
en/index.html       inglês
es/index.html       espanhol
assets/style.css    tokens de cor e layout
assets/fonts/       Urbanist (SIL Open Font License, em OFL.txt)
assets/favicon.svg
```

HTML e CSS puros, sem build. A fonte fica no repositório para a página não fazer requisição a terceiros.

## Regras

- **O texto do app e o desta página são o mesmo.** Mudou a política, mudam juntos: as três páginas aqui, o texto embutido na `SettingsFeature` e a data de atualização no topo de cada página.
- **Os três idiomas andam juntos.** Nenhuma mudança entra em um idioma só.
- **Identidade visual provisória.** Cores e fonte vêm do Figma (Challenge-18, página "02. Design System & Foundations", frame "Teste de cores escolhida"). Quando a identidade fechar, troque os valores de marca no `:root` de `assets/style.css`.
- **Nome do app provisório.** Para trocar, substitua "Apply" nos três `index.html` (título, marca, texto e rodapé).

## Rodar localmente

```bash
python3 -m http.server 8765
```

E abra http://localhost:8765.

## Publicação

O GitHub Pages publica a branch `main` a partir da raiz. Todo merge na `main` atualiza o site.
