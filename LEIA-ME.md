# Site — Giselle Abissamra | Fonoaudiologia

Site institucional em HTML, CSS e JavaScript puro (sem frameworks). Basta abrir `index.html` no navegador para visualizar.

## Estrutura

```
/
├── index.html
├── css/style.css
├── js/script.js
└── assets/
    ├── images/   → fotos do site
    ├── icons/    → ícones adicionais, se necessário
    └── logo/     → logo e favicon
```

## O que precisa ser substituído antes de publicar

1. **Imagens** (pasta `assets/images/`) — atualmente há placeholders com moldura laranja no lugar das fotos:
   - `hero-fonoaudiologia.jpg` — imagem da seção inicial (Hero)
   - `giselle.jpg` — foto da seção "Sobre Mim"
   Depois de adicionar os arquivos, troque as `<div class="hero__image-placeholder">` e `<div class="about__image-placeholder">` por `<img>` apontando para os arquivos correspondentes (há comentários no HTML indicando exatamente onde).

2. **Logo** (pasta `assets/logo/`) — o cabeçalho usa um ícone SVG genérico. Se houver uma logo própria, substitua o bloco `.logo__mark` no `index.html` e adicione um `favicon.png`.

3. **Depoimentos** — os 3 depoimentos da seção "Depoimentos" são **fictícios**, marcados com comentário no HTML. Substitua pelos depoimentos reais e autorizados dos pacientes.

4. **Dados de contato** — telefone, WhatsApp, e-mail e localização são placeholders. Atualize em:
   - Seção "Entre em contato" (`#contato`)
   - Botão flutuante do WhatsApp
   - Rodapé (redes sociais)

5. **Sobre Mim** — o texto institucional é genérico e não inclui formação, CRFa ou especializações (informações não fornecidas). Substitua pelo texto real da profissional.

6. **Formulário de contato** — atualmente apenas valida os campos no navegador e não envia dados de verdade. Para receber as mensagens, é necessário integrar com um backend, serviço de e-mail (ex.: Formspree, EmailJS) ou similar.

## Paleta de cores (definida em `css/style.css`, no `:root`)

| Variável | Cor | Uso |
|---|---|---|
| `--primary` | `#E8893A` | Laranja principal |
| `--primary-dark` | `#D96F24` | Botões e destaques |
| `--primary-light` | `#F6C69D` | Laranja claro |
| `--background` | `#FFF8F2` | Fundo bege claro |
| `--ink` | `#2B2620` | Títulos |
| `--text` / `--text-light` | `#333333` / `#666666` | Textos |

## Testado

- Responsivo de 360px a 1440px+
- Menu hamburger no mobile com fechamento automático ao clicar em um link
- Header com sombra e compactação ao rolar
- Animações de entrada discretas via `IntersectionObserver`
- Validação de formulário (nome, e-mail, telefone, mensagem) com mensagens de erro/sucesso
- Botão flutuante do WhatsApp com tooltip
- Carrossel de depoimentos com setas e indicadores, navegável por toque/arraste no mobile
- Sem scroll horizontal em nenhum breakpoint
