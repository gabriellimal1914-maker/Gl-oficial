# GL Contabilidade Digital — site institucional

Site estático de página única. Não precisa de build, npm, nem framework.
O `index.html` é autossuficiente: CSS, ícones e a foto do responsável técnico estão embutidos no próprio arquivo.

---

## Arquivos

```
index.html     → o site inteiro
robots.txt     → instruções para buscadores
sitemap.xml    → mapa do site
.gitignore     → arquivos que o Git deve ignorar
```

---

## Antes de publicar

Trocar em `index.html` (use Ctrl+F):

| Procurar por | Trocar por |
|---|---|
| `https://www.glcontabilidade.com.br` | seu domínio real |
| `contato@glcontabilidade.com.br` | seu e-mail real |
| `@glcontabilidade` | seu Instagram (se mudou) |

Em `robots.txt` e `sitemap.xml`, trocar `SEU-DOMINIO.com.br` pelo domínio real.

**Pendências de conteúdo:**
- Os contadores mostram *150 empresas* e *98% de satisfação* — números ilustrativos, precisam ser substituídos pelos reais
- Os depoimentos precisam ser confirmados como reais antes da publicação
- Os links **Política de Privacidade** e **LGPD** ainda não apontam para nenhuma página

---

## Publicar no GitHub

Se preferir sem instalar nada, use o **GitHub Desktop** (https://desktop.github.com):

1. Crie um repositório novo em https://github.com/new
2. No GitHub Desktop: **File → Clone repository** e escolha o repositório criado
3. Copie os 4 arquivos desta pasta para dentro da pasta local do repositório
4. Escreva uma mensagem de commit e clique em **Commit to main**
5. Clique em **Push origin**

**Importante:** os arquivos precisam ficar na **raiz** do repositório.
Ao abrir o repositório no GitHub, você deve ver `index.html` na primeira tela — não dentro de uma subpasta.

Pela linha de comando, se preferir:

```bash
git init
git add .
git commit -m "Site GL Contabilidade"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
git push -u origin main
```

---

## Publicar na Vercel

1. Acesse https://vercel.com/new
2. Importe o repositório do GitHub
3. Nas configurações do projeto:
   - **Framework Preset:** `Other`
   - **Build Command:** deixe **vazio**
   - **Output Directory:** deixe **vazio** (ou `.`)
   - **Install Command:** deixe **vazio**
4. Clique em **Deploy**

Como não há etapa de build, o deploy leva poucos segundos.
Cada `push` no GitHub gera um novo deploy automaticamente.

### Domínio próprio

No painel da Vercel: **Settings → Domains → Add**.
A Vercel mostra os registros de DNS para você configurar no seu provedor de domínio.
O certificado HTTPS é emitido automaticamente.

---

## Alternativa sem GitHub

Se quiser apenas ver o site no ar rapidamente:
acesse https://app.netlify.com/drop e arraste esta pasta inteira para a página.
O link fica pronto em segundos.

---

## Manutenção

Para editar textos, abra o `index.html` em qualquer editor de texto e use Ctrl+F para achar o trecho.

Para trocar a foto de um depoimento por uma foto real, procure por `Para usar foto real` no arquivo — há um comentário com a linha pronta em cada um dos três depoimentos.
