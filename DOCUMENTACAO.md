# 📘 Documentação — Site Acolhimento da Mente (Iolanda Fernandes)

Documentação completa do site profissional de psicanálise da **Iolanda Fernandes**.

- 🌐 **Site no ar:** https://acolhimentodamente.com.br
- 📦 **Repositório:** https://github.com/GrupoFernandes/Site-Psicanalise
- 📅 **Publicado em:** 31/05/2026

---

## 1. Visão geral

Site institucional de **página única** (*one-page*), estático e leve, feito para apresentar o trabalho da psicanalista Iolanda Fernandes. Não tem login, banco de dados nem formulários que enviam dados — é apenas conteúdo visual e informativo, com o contato feito por WhatsApp/e-mail/Instagram.

| Item | Detalhe |
|------|---------|
| Tipo | Site estático (HTML + CSS + JavaScript puro) |
| Hospedagem | GitHub Pages (gratuita) |
| Domínio | `acolhimentodamente.com.br` (registrado na Locaweb) |
| Segurança | HTTPS ativo (certificado Let's Encrypt, renovação automática) |
| Custo | Apenas a renovação anual do domínio (~R$ 40–50/ano). Zero mensalidade. |

---

## 2. Estrutura de arquivos

```
Site-Psicanalise/
├── index.html          # A página inteira (todas as seções)
├── css/
│   └── styles.css      # Todo o visual: cores, fontes, layout, responsividade
├── js/
│   └── main.js         # Menu mobile + ano automático no rodapé
├── CNAME               # Contém o domínio (não apagar — liga o site ao endereço)
├── README.md           # Documento original de planejamento do projeto
└── DOCUMENTACAO.md     # Este arquivo
```

> ⚠️ **Não apague o arquivo `CNAME`.** Ele é o que conecta o site ao endereço `acolhimentodamente.com.br`. Se sumir, o domínio personalizado para de funcionar.

---

## 3. Seções da página

A página (`index.html`) é dividida em 6 seções, na ordem em que aparecem:

| # | Seção | ID (âncora) | Conteúdo |
|---|-------|-------------|----------|
| 1 | **Hero** | `#hero` | Abertura: frase de impacto, subtítulo, botão "Agendar conversa inicial" e foto |
| 2 | **Sobre** | `#sobre` | Biografia + box lateral de formação/credenciais |
| 3 | **Atendimento** | `#atendimento` | 3 cards: Online, Presencial, Para quem |
| 4 | **Áreas de atuação** | `#areas` | 6 áreas em grade (ansiedade, luto, autoconhecimento, etc.) |
| 5 | **Como funciona** | `#como-funciona` | 3 passos numerados (primeira conversa, frequência, sigilo) |
| 6 | **Contato** | `#contato` | WhatsApp, e-mail, Instagram e endereço |

O menu do topo (cabeçalho fixo) leva direto a cada seção. No celular, ele vira um menu "hambúrguer" (☰).

---

## 4. ⚠️ Conteúdo a preencher (PLACEHOLDERS)

> **Importante:** o site está no ar com a estrutura e o visual prontos, mas **os textos ainda são provisórios**. Em `index.html` existem várias marcações `[PLACEHOLDER: ...]` e comentários `<!-- TODO -->` que precisam ser substituídos pelo conteúdo real da Iolanda.

O que ainda falta preencher:

- [ ] **Meta descrição** (linha 6 do `index.html`) — texto que aparece no Google
- [ ] **Frase de abertura** e subtítulo do Hero
- [ ] **Foto profissional** da Iolanda → salvar em `img/iolanda.jpg` e trocar o bloco de placeholder
- [ ] **Biografia** (3 parágrafos) na seção Sobre
- [ ] **Formação / instituições / filiações** no box lateral
- [ ] **CRP** (se a Iolanda for psicóloga formada) — no box de formação e no rodapé
- [ ] Textos dos cards de **Atendimento** (online, presencial, para quem)
- [ ] Descrições das **Áreas de atuação**
- [ ] Textos de **Como funciona** (primeira conversa, frequência, sigilo)
- [ ] **WhatsApp** real (formato do link: `https://wa.me/55XXXXXXXXXXX`)
- [ ] **E-mail** real
- [ ] **Instagram** real
- [ ] **Endereço/bairro** (somente se houver atendimento presencial)

> 💡 Para encontrar tudo o que falta, abra o `index.html` e procure (Ctrl+F) pela palavra `PLACEHOLDER`.

---

## 5. Como editar o conteúdo

Tudo é feito editando os arquivos no VSCode, na pasta do projeto.

- **Mudar textos** → editar `index.html` (substituir os trechos `[PLACEHOLDER]`)
- **Mudar cores, fontes ou layout** → editar `css/styles.css`
- **Adicionar a foto** → criar a pasta `img/`, colocar a foto lá, e ajustar o `index.html`

Exemplo prático — trocar a frase de abertura:
```html
<!-- ANTES -->
<h1>[PLACEHOLDER: frase acolhedora de abertura — ex.: "Um espaço para escutar o que ainda não foi dito."]</h1>

<!-- DEPOIS -->
<h1>Um espaço para escutar o que ainda não foi dito.</h1>
```

---

## 6. Como publicar alterações (colocar no ar)

O site atualiza sozinho sempre que as mudanças chegam ao GitHub. O fluxo é:

1. **Edite** os arquivos no VSCode e salve (Ctrl+S)
2. Abra o painel **Source Control** (ícone de galho na barra esquerda, ou `Ctrl+Shift+G`)
3. Escreva uma mensagem curta descrevendo a mudança (ex.: *"Adiciona biografia e contatos reais"*)
4. Clique em **Commit**
5. Clique em **Sync Changes** (ou **Push**)

Em **1 a 2 minutos**, as mudanças aparecem no ar em https://acolhimentodamente.com.br.

> 💡 Dica: se não vir a mudança no navegador, recarregue com **Ctrl + Shift + R** (limpa o cache).

---

## 7. Identidade visual

Definida via variáveis no topo do `css/styles.css` (`:root`). Para mudar a cara do site inteiro, basta alterar esses valores.

### Paleta de cores
| Cor | Código | Uso |
|-----|--------|-----|
| Off-white | `#FAF7F2` | Fundo principal |
| Off-white quente | `#F1ECE3` | Fundo de seções alternadas |
| Verde-acinzentado escuro | `#2E3A36` | Textos e rodapé |
| Verde-sálvia | `#8FA68E` | Destaques, detalhes |
| Verde-sálvia escuro | `#6E8A6D` | Botões, links |
| Terracota suave | `#C28E73` | Detalhes, "eyebrow", números |

### Tipografia (Google Fonts)
- **Playfair Display** (serifada, elegante) — títulos
- **Inter** (sem serifa, limpa) — textos

### Responsividade (mobile-first)
- Base: layout de coluna única (celular)
- A partir de **720px**: layouts em grade (tablet/desktop)
- A partir de **960px**: áreas de atuação em 3 colunas

---

## 8. JavaScript (`js/main.js`)

Arquivo minúsculo, com apenas duas funções:
1. **Menu mobile** — abre/fecha o menu "hambúrguer" no celular e fecha ao clicar num link
2. **Ano automático** — preenche o ano atual no rodapé sozinho (não precisa atualizar todo ano)

Não há bibliotecas externas — JavaScript puro, sem dependências.

---

## 9. Infraestrutura (como o site fica no ar)

```
Visitante digita acolhimentodamente.com.br
        │
        ▼
   DNS na Locaweb  ──►  aponta para os servidores do GitHub
        │                (4 registros A + 1 CNAME para "www")
        ▼
   GitHub Pages    ──►  serve os arquivos do repositório (branch main)
        │
        ▼
   HTTPS (Let's Encrypt) ──► cadeado de segurança 🔒
```

### Registros DNS configurados na Locaweb
| Tipo | Nome | Valor |
|------|------|-------|
| A | (vazio) | `185.199.108.153` |
| A | (vazio) | `185.199.109.153` |
| A | (vazio) | `185.199.110.153` |
| A | (vazio) | `185.199.111.153` |
| CNAME | `www` | `grupofernandes.github.io.` |

### GitHub Pages
- Configurado em: **Settings → Pages**
- Origem: branch `main`, pasta `/ (root)`
- Domínio personalizado: `acolhimentodamente.com.br`
- **Enforce HTTPS:** ✅ ativado

---

## 10. Manutenção e cuidados

- 🗓️ **Renovação do domínio:** fique atento ao e-mail da Locaweb todo ano. Se o domínio expirar, o site sai do ar. Esse é o **único custo recorrente**.
- 🔒 **Certificado HTTPS:** renova sozinho (GitHub + Let's Encrypt). Não precisa fazer nada.
- 🚫 **Não apagar** os arquivos `CNAME` nem desativar o GitHub Pages.
- 💾 **Backup:** o próprio GitHub já guarda todo o histórico. Cada alteração publicada fica registrada e pode ser revertida.

---

## 11. Solução de problemas

| Problema | Possível causa / solução |
|----------|--------------------------|
| Site fora do ar (erro 404) | Verificar se o GitHub Pages está ativo e se o arquivo `CNAME` existe no repositório |
| "Site não seguro" | Acessar com `https://` e conferir se "Enforce HTTPS" está marcado em Settings → Pages |
| Mudança não aparece | Aguardar 1–2 min e recarregar com `Ctrl + Shift + R` |
| Domínio parou de funcionar | Conferir se o domínio não expirou na Locaweb e se os registros DNS continuam corretos (seção 9) |
| Menu mobile não abre | Conferir se o `js/main.js` está sendo carregado (final do `index.html`) |

---

## 12. Considerações éticas / legais

Se a Iolanda for **psicóloga formada com CRP**, o site deve seguir a **Resolução CFP 06/2019**:
- Não prometer resultados ou curas
- Não exibir depoimentos de pacientes
- Evitar termos comerciais agressivos
- Exibir o número do CRP

Se for **somente psicanalista** (sem CRP), a publicidade é mais livre, mas recomenda-se manter a sobriedade — a psicanálise valoriza a discrição.

---

_Documentação criada em 31/05/2026. Mantenha este arquivo atualizado conforme o site evoluir._
