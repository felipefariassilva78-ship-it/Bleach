# BLEACH — Fan Site

Fan site do anime **Bleach** com visual profissional, moderno e minimalista, criado por Felps.

- **Tecnologia:** HTML, CSS e JavaScript puros (sem framework, sem build)
- **Estilo:** tema claro premium, responsivo e acessível
- **Deploy:** pronto para Vercel (site estático)

## Estrutura

```
.
├── index.html        # Página principal
├── style.css         # Estilos (design tokens + componentes)
├── script.js         # Interatividade (menu, rolagem, animações)
├── vercel.json       # Configuração de deploy estático
├── package.json      # Metadados do projeto (deploy sem build)
├── .env.example      # (vazio) - não há variáveis obrigatórias
├── .gitignore
└── README.md
```

## Executar localmente

```bash
# Opção 1 - Python (já vem instalado em quase todo sistema):
python3 -m http.server 8000
# acesse: http://localhost:8000

# Opção 2 - NPM (requer Node.js):
npm run dev
# acesse: http://localhost:3000
```

Também é possível abrir o `index.html` diretamente no navegador.

## Deploy na Vercel

### 1) Publicar no GitHub

```bash
git init
git add .
git commit -m "Site Bleach - v2"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/SEU_REPO.git
git push -u origin main
```

### 2) Importar na Vercel

1. Acesse https://vercel.com e crie uma conta (login com GitHub).
2. **Add New → Project → Import** o repositório que você acabou de publicar.
3. A Vercel detecta o projeto como estático automaticamente.
4. Clique em **Deploy**.

### Configuração recomendada na Vercel (valores padrão do projeto)

| Campo | Valor |
|---|---|
| **Framework Preset** | *Other* (site estático) ou deixar automático |
| **Root Directory** | Raiz do repositório (ou a pasta que contém o `index.html`) |
| **Build Command** | *não preencher* (o `npm run build` existente é um no-op) |
| **Install Command** | *não preencher* (sem dependências) |
| **Output Directory** | *não preencher* (o `index.html` está na raiz) |

> O `vercel.json` já declara `\"framework\": null` e URLs limpas, então basta importar e dar deploy.

### Variáveis de ambiente

**Nenhuma.** O projeto não utiliza API keys, tokens ou credenciais. O arquivo `.env.example` é apenas um modelo vazio para futuras necessidades.

## Comandos úteis

| Ação | Comando |
|---|---|
| Rodar localmente (Python) | `python3 -m http.server 8000` |
| Rodar localmente (Node) | `npm run dev` |
| Build | `npm run build` (no-op, echo informativo) |

## Licença

Bleach é uma obra de **Tite Kubo**. Todos os direitos pertencem a Shueisha, TV Tokyo, dentsu e Pierrot. Este é um site de fã, sem fins lucrativos e sem afiliação oficial.
