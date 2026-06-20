# Guia de Contribuição — Observatório Nacional da Participação Digital

## Branches

| Branch | Finalidade |
|--------|-----------|
| `main` | Produção — cada merge aqui dispara o deploy automático no GitHub Pages |
| `develop` | Integração — branch base para todas as novas mudanças |
| `feature/*` | Desenvolvimento — uma branch por mudança ou funcionalidade |

## Fluxo de trabalho

### 1. Atualizar o develop local

Antes de começar qualquer mudança, garanta que seu `develop` está atualizado:

```bash
git checkout develop
git pull origin develop
```

### 2. Criar uma branch de feature

Crie uma branch a partir do `develop` com um nome descritivo:

```bash
git checkout -b feature/nome-da-mudanca
```

Exemplos:
- `feature/grafico-evolucao`
- `feature/formulario-pesquisa`
- `fix/link-explorar-dados`

### 3. Fazer as alterações e commitar

```bash
git add .
git commit -m "descrição clara do que foi feito e por quê"
```

Boas mensagens de commit:
- ✅ `feat: adiciona gráfico de linha na seção de evolução`
- ✅ `fix: corrige link para /explorar-dados no GitHub Pages`
- ✅ `style: ajusta cor da seção de parceiros`
- ❌ `mudanças`
- ❌ `update`

### 4. Subir a branch para o GitHub

```bash
git push -u origin feature/nome-da-mudanca
```

### 5. Abrir Pull Request: feature → develop

1. Acesse [github.com/RenanGirao/Observatorio-Nacional/pulls](https://github.com/RenanGirao/Observatorio-Nacional/pulls)
2. Clique em **"New pull request"**
3. Base: `develop` ← Compare: `feature/nome-da-mudanca`
4. Descreva o que foi feito e por quê
5. Clique em **"Create pull request"**

### 6. Após revisão: merge feature → develop

Depois que o PR for aprovado, faça o merge no GitHub.

### 7. Quando pronto para produção: PR develop → main

1. Abra um novo PR: Base `main` ← Compare `develop`
2. Título: `release: descrição das mudanças`
3. Após merge, o deploy acontece automaticamente em ~30 segundos

---

## Deploy

O deploy é feito automaticamente via GitHub Actions ao fazer merge na `main`.

URL de produção: **https://renangirao.github.io/Observatorio-Nacional/**

Para acompanhar o status do deploy:
[github.com/RenanGirao/Observatorio-Nacional/actions](https://github.com/RenanGirao/Observatorio-Nacional/actions)

---

## Estrutura do projeto

```
src/
├── components/     # Componentes reutilizáveis (.astro)
├── layouts/        # Layout base da página (Layout.astro)
└── pages/          # Páginas — cada arquivo vira uma rota
    ├── index.astro         # Página principal
    └── explorar-dados.astro # Página de exploração de dados
public/             # Arquivos estáticos (imagens, fontes)
.github/workflows/  # Pipeline de deploy (não editar)
```

## Dúvidas

Em caso de dúvidas, abra uma [Issue](https://github.com/RenanGirao/Observatorio-Nacional/issues) no repositório.
