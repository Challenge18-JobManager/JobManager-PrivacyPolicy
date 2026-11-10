# JobManager-PrivacyPolicy

Política de privacidade e termos de uso (EULA) do app (nome provisório: **Apply**), publicados no GitHub Pages.

## Política de privacidade

| Idioma | Página |
|---|---|
| Português (Brasil) | https://challenge18-jobmanager.github.io/JobManager-PrivacyPolicy/ |
| English | https://challenge18-jobmanager.github.io/JobManager-PrivacyPolicy/en/ |
| Español | https://challenge18-jobmanager.github.io/JobManager-PrivacyPolicy/es/ |

A página em inglês é a que vai no campo **Privacy Policy URL** do App Store Connect.

## Termos de uso (EULA)

| Idioma | Página |
|---|---|
| Português (Brasil) | https://challenge18-jobmanager.github.io/JobManager-PrivacyPolicy/terms/ |
| English | https://challenge18-jobmanager.github.io/JobManager-PrivacyPolicy/en/terms/ |
| Español | https://challenge18-jobmanager.github.io/JobManager-PrivacyPolicy/es/terms/ |

A página em inglês é a que vai no campo **Termos de Uso (EULA)** do App Store Connect.

## Estrutura

```
index.html          pt-BR
en/index.html       inglês
es/index.html       espanhol
terms/index.html    termos de uso, pt-BR
en/terms/index.html termos de uso, inglês
es/terms/index.html termos de uso, espanhol
assets/style.css    tokens de cor e layout
assets/fonts/       Urbanist (SIL Open Font License, em OFL.txt)
assets/favicon.svg
```

HTML e CSS puros, sem build. A fonte fica no repositório para a página não fazer requisição a terceiros.

## Regras

- **O texto do app e o desta página são o mesmo.** Mudou a política, mudam juntos: as três páginas aqui, o texto embutido na `SettingsFeature` e a data de atualização no topo de cada página.
- **O texto dos termos aqui é o mesmo que o app mostra ou linka.** Mudou o termo, mudam juntos: as três páginas `terms/`, o texto no app e a data "Atualizados em" no topo de cada página.
- **Os termos não trazem identificação do responsável, lei aplicável nem foro.** Nada disso é inventado. Se o responsável decidir publicar esses dados, inclua uma seção nos três idiomas; o pendente está registrado em um comentário `TODO(KAN-194)` no topo de cada `terms/index.html`.
- **Links internos apontam para o arquivo.** Troca de idioma e link entre política e termos usam `index.html` explícito (por exemplo, `../index.html`, `terms/index.html`), para funcionar ao abrir o arquivo direto, sem servidor. Na produção, o GitHub Pages serve tanto `/terms/` quanto `/terms/index.html`, então as URLs publicadas acima continuam valendo. Não troque por links de diretório.
- **Preços não aparecem nos termos.** Eles variam por país e a loja os mostra antes da compra.
- **Cada documento linka o outro.** O rodapé da política aponta para os termos, e o dos termos para a política.
- **Os três idiomas andam juntos.** Nenhuma mudança entra em um idioma só.
- **Identidade visual provisória.** Cores e fonte vêm do Figma (Challenge-18, página "02. Design System & Foundations", frame "Teste de cores escolhida"). Quando a identidade fechar, troque os valores de marca no `:root` de `assets/style.css`.
- **Nome do app provisório.** Para trocar, substitua "Apply" em todos os `index.html` (política e termos; título, marca, texto e rodapé).

## Rodar localmente

```bash
python3 -m http.server 8765
```

E abra http://localhost:8765. Também dá para abrir os `index.html` direto no navegador ou no VS Code (`file://`).

## Publicação

O GitHub Pages publica a branch `main` a partir da raiz. Todo merge na `main` atualiza o site.
