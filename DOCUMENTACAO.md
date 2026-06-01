# 📘 Documentação — Site Acolhimento da Mente (Iolanda Fernandes)

Documentação completa do site profissional de psicanálise da **Iolanda Fernandes**.

- 🌐 **Site no ar:** https://acolhimentodamente.com.br
- 📦 **Repositório:** https://github.com/GrupoFernandes/Site-Psicanalise
- 📅 **Publicado em:** 31/05/2026 · **Conteúdo real publicado em:** 31/05/2026

---

## 1. Visão geral

Site institucional de **página única** (*one-page*), estático e leve, para apresentar o trabalho da psicanalista Iolanda Fernandes. Não tem login nem banco de dados. O contato é feito por **formulário** (que chega no e-mail dela) e por **WhatsApp**.

| Item | Detalhe |
|------|---------|
| Tipo | Site estático (HTML + CSS + JavaScript puro) |
| Hospedagem | GitHub Pages (gratuita) |
| Domínio | `acolhimentodamente.com.br` (registrado na Locaweb) |
| Segurança | HTTPS ativo (certificado Let's Encrypt, renovação automática) |
| Formulário | FormSubmit (gratuito, sem servidor) → envia para o e-mail da Iolanda |
| Custo | Apenas a renovação anual do domínio (~R$ 40–50/ano). Zero mensalidade. |

---

## 2. Estrutura de arquivos

```
Site-Psicanalise/
├── index.html          # A página inteira (todas as seções)
├── obrigada.html       # Página exibida após enviar o formulário
├── css/
│   └── styles.css      # Todo o visual: cores, fontes, layout, responsividade
├── js/
│   └── main.js         # Menu mobile + ano automático no rodapé
├── img/                # Imagens do site (otimizadas para web)
│   ├── iolanda.jpg         # Foto da Iolanda (seção "Sobre mim")
│   ├── campo-verde.jpg     # Imagem do topo (hero)
│   ├── broto.jpg           # Imagem da seção "Sobre meu trabalho"
│   └── luz-folhas.jpg      # Fundo da faixa de citação
├── CNAME               # Contém o domínio (não apagar — liga o site ao endereço)
├── README.md           # Documento original de planejamento do projeto
└── DOCUMENTACAO.md     # Este arquivo
```

> ⚠️ **Não apague o arquivo `CNAME`.** Ele conecta o site ao endereço `acolhimentodamente.com.br`. Se sumir, o domínio personalizado para de funcionar.

---

## 3. Seções da página

A página (`index.html`) tem as seguintes seções, na ordem em que aparecem:

| # | Seção | ID (âncora) | Conteúdo |
|---|-------|-------------|----------|
| 1 | **Hero (topo)** | `#hero` | Frase de acolhimento, imagem serena e botão "Agende seu atendimento" |
| 2 | **Sobre meu trabalho** | `#trabalho` | O que é a psicanálise + imagem do broto |
| 3 | **Como posso te ajudar?** | `#areas` | 5 temas (ansiedade, conflitos, relacionamentos, autoconhecimento, transição) |
| 4 | **Sobre mim** | `#sobre` | Biografia da Iolanda + foto |
| 5 | **Atendimento** | `#atendimento` | Como funciona · Online/Individual/50 min · Para quem · Diferenciais |
| 6 | **Faixa de citação** | — | Frase de encerramento sobre imagem de fundo |
| 7 | **Contato** | `#contato` | Formulário + WhatsApp + e-mail |

O menu do topo leva direto a cada seção. No celular, vira um menu "hambúrguer" (☰).

---

## 4. Contato — como funciona

O site tem **duas formas de contato**, ambas já configuradas:

### 📬 Formulário (FormSubmit)
- Campos: Nome, E-mail, Telefone/WhatsApp, Mensagem
- Ao enviar, a mensagem vai para **acolhimentodamente@gmail.com** pelo serviço gratuito **FormSubmit** (não precisa de servidor nem de conta)
- Depois de enviar, o visitante vê a página `obrigada.html`
- ⚠️ **Ativação única:** na **primeira vez** que o formulário for enviado, o FormSubmit manda um e-mail pedindo confirmação. A Iolanda precisa abrir esse e-mail (conferir o **Spam** também) e clicar em **"Activate Form"**. Depois disso, todas as mensagens chegam normalmente.
- Para mudar o e-mail de destino: no `index.html`, alterar o endereço em `action="https://formsubmit.co/SEU-EMAIL"`

### 🟢 WhatsApp
- Número: **(11) 99950-0914** → link `https://wa.me/5511999500914`
- Aparece em **dois lugares**: botão verde flutuante (canto inferior direito) e na seção Contato
- Já vem com uma mensagem pronta ("Olá, Iolanda! Vim pelo site...")
- Para mudar o número: trocar `5511999500914` no `index.html` (formato: 55 + DDD + número)

---

## 5. Como editar o conteúdo

Tudo é feito editando os arquivos no VSCode, na pasta do projeto.

- **Mudar textos** → editar `index.html`
- **Trocar a foto ou as imagens** → substituir os arquivos dentro de `img/` (mantendo os mesmos nomes), ou apontar para um arquivo novo no `index.html`
- **Mudar cores, fontes ou layout** → editar `css/styles.css`
- **Mudar e-mail/WhatsApp de contato** → ver seção 4 acima

> 💡 **Imagens:** sempre otimize antes de subir (reduza o tamanho). As fotos de celular costumam ter vários MB; o ideal para web é deixá-las abaixo de ~500 KB. As imagens atuais já foram otimizadas.

---

## 6. Como publicar alterações (colocar no ar)

O site atualiza sozinho sempre que as mudanças chegam ao GitHub:

1. **Edite** os arquivos no VSCode e salve (Ctrl+S)
2. Abra o **Source Control** (ícone de galho, ou `Ctrl+Shift+G`)
3. Escreva uma mensagem curta da mudança e clique em **Commit**
4. Clique em **Sync Changes** (ou **Push**)

Em **1 a 3 minutos**, as mudanças aparecem no ar em https://acolhimentodamente.com.br.

> 💡 Se não vir a mudança, recarregue com **Ctrl + Shift + R** (limpa o cache).

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
| Terracota suave | `#C28E73` | Detalhes, "eyebrow" |
| Lilás suave | `#B9A7C9` | Acento opcional |

### Tipografia (Google Fonts)
- **Playfair Display** (serifada, elegante) — títulos
- **Inter** (sem serifa, limpa) — textos

### Responsividade (mobile-first)
- Base: layout de coluna única (celular)
- A partir de **720px**: grades de 2–3 colunas
- A partir de **960px**: "Como posso te ajudar?" em 5 colunas

---

## 8. JavaScript (`js/main.js`)

Arquivo minúsculo, com duas funções:
1. **Menu mobile** — abre/fecha o menu "hambúrguer" no celular
2. **Ano automático** — preenche o ano atual no rodapé sozinho

Sem bibliotecas externas — JavaScript puro.

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
- Configurado em: **Settings → Pages** · Origem: branch `main`, pasta `/ (root)`
- Domínio personalizado: `acolhimentodamente.com.br` · **Enforce HTTPS** ✅

---

## 10. Manutenção e cuidados

- 🗓️ **Renovação do domínio:** fique atento ao e-mail da Locaweb todo ano. Se o domínio expirar, o site sai do ar. É o **único custo recorrente**.
- 📬 **Formulário:** lembre-se da **ativação única** do FormSubmit (seção 4). Se as mensagens pararem de chegar, confira o e-mail e o Spam.
- 🔒 **Certificado HTTPS:** renova sozinho. Não precisa fazer nada.
- 🚫 **Não apagar** o `CNAME` nem desativar o GitHub Pages.
- 💾 **Backup:** o GitHub guarda todo o histórico; cada alteração pode ser revertida.

---

## 11. Solução de problemas

| Problema | Possível causa / solução |
|----------|--------------------------|
| Site fora do ar (erro 404) | Verificar se o GitHub Pages está ativo e se o `CNAME` existe |
| "Site não seguro" | Acessar com `https://` e conferir "Enforce HTTPS" em Settings → Pages |
| Mudança não aparece | Aguardar 1–3 min e recarregar com `Ctrl + Shift + R` |
| Formulário não chega no e-mail | Confirmar a **ativação** do FormSubmit (e o Spam); conferir o e-mail em `action=` no index.html |
| WhatsApp abre número errado | Conferir o número `5511999500914` no index.html (55 + DDD + número) |
| Imagem não aparece | Conferir se o arquivo existe em `img/` com o nome certo |
| Domínio parou de funcionar | Conferir se não expirou na Locaweb e se os registros DNS continuam corretos (seção 9) |

---

## 12. Considerações éticas / legais

A Iolanda atua como **psicanalista**. O site mantém sobriedade e foco no acolhimento, sem prometer resultados ou exibir depoimentos de pacientes.

> Caso futuramente ela passe a ter registro de **psicóloga (CRP)**, será necessário seguir a **Resolução CFP 06/2019** (exibir o número do CRP, não prometer curas, etc.).

---

## 13. Itens opcionais / futuros

- 📷 **Instagram:** ainda não há perfil. Quando houver, adicionar na seção Contato.
- 🏢 **Atendimento presencial:** hoje o site informa apenas **online**. Se passar a atender presencialmente, incluir cidade/endereço.
- ✍️ Pode-se adicionar futuramente: depoimentos (com cuidado ético), blog/artigos, ou um FAQ.

---

_Documentação atualizada em 31/05/2026. Mantenha este arquivo atualizado conforme o site evoluir._
