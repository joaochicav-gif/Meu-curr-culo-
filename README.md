# Currículo Pessoal — João Chicava João Dojo

**Turma:** Licenciatura em Informática, 2.º ano — Universidade Licungo (Faculdade de Ciência e Tecnologia)
**Disciplina:** Programação de Design Web — Trabalho Prático I

## Dados do estudante
- **Nome:** João Chicava João Dojo
- **Área:** Estudante de Informática
- **Localização:** Beira, Moçambique
- **Contactos:** Joaochicav@gmail.com · +258 84 936 8986
- **GitHub:** [joaochicava](https://github.com/joaochicava)

## Descrição
Site pessoal de currículo/portfólio construído inteiramente com **HTML5 semântico e CSS3 puro** — sem frameworks (Bootstrap, Tailwind, etc.) e sem JavaScript. Toda a interatividade (menu, estados de validação) resulta de pseudo-classes e seletores nativos do CSS.

## Como visualizar
Abrir `index.html` num navegador. Manter a estrutura de pastas intacta para que `css/` e `assets/` sejam carregados corretamente. Não é necessário nenhum servidor nem instalação.

## Páginas
1. **Home (`index.html`)** — apresentação pessoal, tagline, competências em destaque, vídeo e áudio de apresentação.
2. **Sobre (`about.html`)** — perfil, formação académica, tabela de competências técnicas e experiência.
3. **Portfólio (`portfolio.html`)** — grelha de projetos académicos em CSS Grid.
4. **Hobbies (`hobbies.html`)** — interesses pessoais organizados com Flexbox.
5. **Contacto (`contact.html`)** — formulário HTML5 com vários tipos de campo e validação nativa.

## Identidade visual e escolhas técnicas

**Paleta de cor.** As imagens de referência fornecidas para inspiração eram fotografias de stock com marca de terceiros (logótipos "OnSafety" e "Techlise"). Em vez de reproduzir as imagens em si — o que levantaria questões de direitos de autor e não seria original —, extraí a sua identidade cromática (azul-marinho profundo, azul elétrico e ciano) e recriei-a com **gradientes e sombras 100% em CSS** (`--gradiente-hero`, `--gradiente-marca` em `estilo.css`). Isto também vai ao encontro do espírito do trabalho: privilegiar recursos nativos de CSS em vez de imagens externas sempre que possível.

- `--cor-marinho`, `--cor-azul`, `--cor-ciano`: paleta principal, definida em `:root`.
- O avatar da Home é um **monograma SVG** ("JD") com anéis concêntricos, e não uma fotografia — evita usar uma imagem genérica ou de terceiros como se fosse a do estudante.
- Os quatro ícones do Portfólio (`farmacia.svg`, `vendas.svg`, `viaturas.svg`, `programacao-c.svg`) seguem a mesma paleta, desenhados propositadamente para cada projeto.

**Tipografia.** `Space Grotesk` (títulos, via Google Fonts) transmite um caráter técnico/geométrico coerente com a área de Informática; `Inter` (texto corrido) garante boa legibilidade. Hierarquia de tamanhos com `clamp()` para escalar suavemente entre ecrãs.

**Layout.** `position: sticky` no cabeçalho (comentado em `estilo.css` com a explicação de `static`/`relative`/`absolute`/`fixed`/`sticky`), `display: grid` na grelha de projetos (`repeat(auto-fit, minmax(260px, 1fr))`) e `display: flex` nos cartões de hobbies, conforme exigido no enunciado.

## Principais recursos HTML5
- `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`: estrutura semântica.
- `figure` e `figcaption`: imagens/monograma com legenda.
- `img` com `alt` descritivo em todas as imagens.
- `video` + `source` + `poster`: vídeo nativo (ver nota sobre ficheiros multimédia abaixo).
- `audio` + `source`: áudio nativo.
- `form`, `fieldset`, `legend`, `label`: formulário estruturado.
- `required`, `pattern`, `min`, `max`, `minlength`, `maxlength`: validação nativa HTML5.
- Campos `text`, `email`, `tel`, `date`, `number`, `file`, `select`, `radio`, `textarea`.

## Principais recursos CSS3
- `box-sizing: border-box` em todo o site.
- Seletores avançados: descendente, filho direto (`>`), irmão adjacente (`+`), atributo (`[class~="nav-link"]`).
- Pseudo-classes: `:hover`, `:focus-visible`, `:first-child`, `:last-child`, `:nth-child()`, `:has()`.
- Pseudo-elementos: `::before` e `::after` (sublinhado animado do menu, traço decorativo dos títulos).
- Flexbox (Hobbies) e CSS Grid com `repeat()`/`minmax()`/`auto-fit` (Portfólio).
- `position: sticky` no cabeçalho, com comentário explicativo no CSS.
- Variáveis CSS (`:root`) para cores, espaçamento, raios e sombras.
- `transition` (cartões, botões, links) e `@keyframes` (flutuação suave do avatar na Home).
- `linear-gradient`/`radial-gradient`, `box-shadow` e `text-shadow`.
- Media queries mobile-first em `responsivo.css` (480px e 768px) com unidades relativas (`rem`, `%`, `vw`, `min()`, `clamp()`).

## ⚠️ Nota importante — ficheiros multimédia por adicionar
Por não ter acesso a uma fotografia, vídeo ou áudio reais do estudante, este pacote inclui **apenas a estrutura HTML/CSS pronta** para os receber. Antes da entrega, é necessário:

1. Gravar um pequeno vídeo de apresentação (poucos segundos) e colocar em `assets/video/apresentacao-joao.mp4` — ou substituir o `<video>` por um `<iframe>` do YouTube, como o enunciado permite.
2. Gravar um pequeno áudio de apresentação e colocar em `assets/audio/apresentacao-joao.m4a` (o enunciado exige pelo menos um áudio local).
3. (Opcional, mas recomendado) Substituir o monograma da Home por uma fotografia real, guardando-a em `assets/img/` e ajustando o `src` em `index.html`.

Sem estes ficheiros, as tags `<video>`/`<audio>` ficam corretas em termos de código mas sem conteúdo a reproduzir.

## Organização
```text
meu-curriculo/
├── index.html
├── about.html
├── portfolio.html
├── hobbies.html
├── contact.html
├── css/
│   ├── estilo.css        # variáveis, header/footer, hero, cards, formulário
│   └── responsivo.css    # media queries mobile-first
├── assets/
│   ├── img/               # monograma JD e ícones dos projetos (SVG)
│   ├── video/              # colocar aqui o vídeo de apresentação
│   ├── audio/               # colocar aqui o áudio de apresentação
│   └── ficheiros/            # CV em PDF ou outros anexos
└── README.md
```

## Entrega no GitHub
1. Criar um repositório público chamado, por exemplo, `meu-curriculo`.
2. Fazer commits sucessivos que reflitam a evolução real do trabalho (estrutura → conteúdo → estilo → responsividade → ajustes finais) — **não** um único commit final.
3. Submeter o link do repositório no classroom antes de **2 de setembro de 2026, 23h59**.

> Sugestão de sequência de commits: `feat: estrutura HTML das 5 páginas` → `style: estilos base e variáveis` → `style: grid do portfólio e flexbox dos hobbies` → `feat: formulário e validação HTML5` → `style: responsividade` → `docs: README`.
