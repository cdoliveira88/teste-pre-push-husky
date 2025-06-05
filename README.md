# teste-pre-push-husky
Repositório para testes de git hook husky para pre-push

# 🚀 Setup de Rebase Diário - Projeto SFDX

Este projeto adota um processo de rebase obrigatório com a `feature/integrado` para evitar conflitos de código e manter a base estável.

## ✅ Como manter sua branch sincronizada

**Todo dia, antes de codar:**

```bash
npm run sync
```

Ou, se preferir, use o Git Alias:

```bash
git config --global alias.sync '!git fetch origin && git rebase origin/feature/integrado'
git sync
```

## 🚫 Bloqueio de push

Pushs serão bloqueados se sua branch estiver desatualizada com a `feature/integrado`. Isso é verificado automaticamente via Husky (pre-push).

## ✔️ Checklist do Pull Request

- [ ] A branch foi rebaseada com `feature/integrado` hoje (`npm run sync`)
