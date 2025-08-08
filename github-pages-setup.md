# 📖 Setup GitHub Pages para Imagens da Igreja Oliveira

## 🚀 Passo a Passo Completo

### 1️⃣ Criar Repositório no GitHub

1. Acesse [GitHub.com](https://github.com)
2. Clique em **"New repository"**
3. Nome do repositório: `igreja-oliveira-assets`
4. Marque como **"Public"** (necessário para GitHub Pages gratuito)
5. Marque **"Add a README file"**
6. Clique **"Create repository"**

### 2️⃣ Configurar GitHub Pages

1. No seu repositório, vá em **Settings** > **Pages**
2. Em **"Source"**, selecione **"Deploy from a branch"**
3. Escolha **"main"** branch e **"/ (root)"**
4. Clique **"Save"**
5. Aguarde alguns minutos - sua URL será: `https://[seu-usuario].github.io/igreja-oliveira-assets/`

### 3️⃣ Estrutura de Pastas

```
igreja-oliveira-assets/
├── README.md
├── assets/
│   └── images/
│       ├── logos/
│       │   ├── logo-white-no-bg.png
│       │   ├── logo-dark-no-bg.png
│       │   └── logo-circular.png
│       └── email/
│           ├── header-bg.jpg
│           └── social-icons/
│               ├── instagram.svg
│               └── youtube.svg
└── index.html (opcional - página de demonstração)
```

### 4️⃣ Upload das Imagens

**Opção A: Via Interface Web do GitHub**
1. No seu repositório, clique **"Add file"** > **"Upload files"**
2. Crie a pasta `assets/images/logos/`
3. Faça upload da sua logo como `logo-white-no-bg.png`
4. Commit as alterações

**Opção B: Via Git (Recomendado)**
```bash
git clone https://github.com/[seu-usuario]/igreja-oliveira-assets.git
cd igreja-oliveira-assets
mkdir -p assets/images/logos
# Copie sua imagem para assets/images/logos/logo-white-no-bg.png
git add .
git commit -m "feat: add Igreja Oliveira logo"
git push origin main
```

### 5️⃣ URL Final da Imagem

Após o upload, sua imagem estará disponível em:
```
https://[seu-usuario].github.io/igreja-oliveira-assets/assets/images/logos/logo-white-no-bg.png
```

### 6️⃣ Atualizar Template de Email

Substitua no template:
```html
<!-- DE: -->
<img src="https://cghxhewgelpcnglfeirw.supabase.co/storage/v1/object/public/igreja-oliveira/imagens/logo-withe-no-background.png" alt="Logo Igreja Oliveira" class="logo">

<!-- PARA: -->
<img src="https://[seu-usuario].github.io/igreja-oliveira-assets/assets/images/logos/logo-white-no-bg.png" alt="Logo Igreja Oliveira" class="logo">
```

## 🎯 Vantagens do GitHub Pages

✅ **100% Gratuito** - Sem limites para repositórios públicos  
✅ **URLs Confiáveis** - Domínio github.io é confiável para email  
✅ **CDN Global** - Carregamento rápido mundial  
✅ **SSL Gratuito** - HTTPS por padrão  
✅ **Zero Manutenção** - GitHub cuida de tudo  
✅ **Controle de Versão** - Histórico de mudanças  
✅ **Fácil Atualização** - Basta fazer commit  

## 🔧 Configurações Adicionais (Opcional)

### Custom Domain (Se tiver)
1. Compre um domínio (ex: `assets.igrejaOliveira.com`)
2. No GitHub Pages Settings, adicione o custom domain
3. Configure DNS no seu provedor:
   ```
   Type: CNAME
   Name: assets
   Value: [seu-usuario].github.io
   ```

### Cache Headers (Para Performance)
Crie arquivo `.htaccess` ou `_config.yml`:
```yaml
# _config.yml
plugins:
  - jekyll-gist

# Cache images por 1 ano
headers:
  "assets/**/*":
    Cache-Control: "max-age=31536000, public, immutable"
```

## 🚨 Importante

- Repositório deve ser **público** (GitHub Pages gratuito)
- Imagens devem ser **otimizadas** (< 1MB recomendado)
- URLs são **case-sensitive**
- Mudanças levam **alguns minutos** para propagar

## 📞 Suporte

Se tiver problemas:
1. Verifique se o repositório é público
2. Aguarde 5-10 minutos após upload
3. Teste a URL diretamente no navegador
4. Verifique logs no GitHub Actions (se houver erros)