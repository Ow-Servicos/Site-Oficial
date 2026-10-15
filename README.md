# OW-SERVIÇOS — Manual do Website Institucional & Guia de Publicação

Website institucional de alto padrão, desenvolvido para a **OW-Serviços**, empresa moçambicana especializada em protocolo, coordenação e gestão operacional de eventos sediada em Maputo.

Desenvolvido estritamente com **HTML5 semântico, CSS3 moderno e JavaScript puro (Vanilla)**, sem recurso a frameworks ou dependências externas, garantindo tempos de carregamento ultrarrápidos, total independência técnica e máxima conversão para pedidos de proposta via WhatsApp.

---

## 1. Estrutura de Ficheiros

```text
Site- Ow Services/
│
├── .nojekyll                    # Impede que o GitHub Pages bloqueie pastas e imagens
├── index.html                   # Estrutura semântica completa e de alta conversão
├── README.md                    # Este manual de edição e publicação
│
├── css/
│   └── styles.css               # Design tokens, tipografia, secções e responsividade
│
├── js/
│   └── main.js                  # Lógica de portefólio, lightbox, FAQ, filtros e WhatsApp
│
└── assets/
    ├── logo.png                 # Logótipo oficial em formato PNG autêntico
    ├── logo.jpg                 # Cópia em formato JPG para redundância
    ├── placeholder-hero.svg     # Placeholder do ecrã inicial (Hero)
    ├── placeholder-team.svg     # Placeholder da secção Sobre a OW (Equipa)
    ├── placeholder-event-1.svg  # Casamento Iracema & Matheus (Real)
    ├── placeholder-event-2.svg  # 17ª Conferência da GRAF (Real)
    ├── placeholder-event-3.svg  # Placeholder Corporativo (SUBSTITUIR)
    └── placeholder-event-4.svg  # Placeholder Institucional (SUBSTITUIR)
```

---

## 2. Publicação no GitHub Pages (Sem Falhas nas Imagens)

Para que as imagens apareçam corretamente na internet via **GitHub Pages**, foram aplicadas 4 correções diretas no código:

1. **Ficheiro `.nojekyll` na raiz**: O GitHub Pages por padrão usa o processador Jekyll, que frequentemente ignora ou bloqueia pastas de ativos estáticos como `assets/`. O ficheiro `.nojekyll` desativa esse processamento.
2. **Caminhos Relativos Explícitos (`./assets/...`)**: Evita que o navegador tente procurar as imagens na raiz do domínio (`usuario.github.io/assets/...`) em vez da subpasta do repositório (`usuario.github.io/nome-do-repositorio/assets/...`).
3. **Conversão de `logo.png` em PNG Real**: O ficheiro anterior era um JPEG disfarçado com extensão `.png`. Servidores estritos como o GitHub Pages enviavam cabeçalho MIME incorreto, impedindo a renderização (especialmente em Safari/iOS). Foi convertido para PNG autêntico com fallback para JPG.
4. **Script de Normalização de Barra Final**: Redireciona automaticamente URLs sem barra final (`/`) no GitHub Pages para que a resolução de caminhos relativos seja sempre precisa.

### ⚠️ Regra Crítica ao Enviar para o GitHub:
Ao enviar os ficheiros para o seu repositório no GitHub:
- Certifique-se de que os ficheiros (`index.html`, pasta `assets`, pasta `css`, pasta `js`, `.nojekyll`) ficam **DIRETAMENTE NA RAIZ DO REPOSITÓRIO**.
- **NÃO envie a pasta "Site- Ow Services" como uma subpasta** dentro do repositório. O ficheiro `index.html` deve estar na página principal do repositório no GitHub.

---

## 3. Onde Estão os Conteúdos Marcados "SUBSTITUIR"

| Secção | Ficheiro | O Que Substituir |
| :--- | :--- | :--- |
| **Hero (Fundo)** | `index.html` | Substituir `./assets/placeholder-hero.svg` pela fotografia real de destaque. |
| **Sobre a OW (Equipa)** | `index.html` | Substituir `./assets/placeholder-team.svg` pela foto da equipa OW em serviço. |
| **Testemunhos** | `index.html` | Substituir os 3 textos por citações reais de clientes com nomes e tipo de evento. |
| **Portefólio (Eventos 3 e 4)** | `js/main.js` | Atualizar títulos, datas e caminhos das fotos de novos eventos corporativos e cerimoniais. |
| **Contadores (Opcional)** | `index.html` | Descomentar o elemento `#counters` caso pretenda ativar números estatísticos. |
| **Sede / Morada** | `index.html` | Atualizar morada exata do escritório em Maputo, se aplicável. |

---

## 4. Contactos Configurados

- **WhatsApp Principal**: `https://wa.me/258846161126` (+258 84 616 1126)
- **Linha Telefónica**: `tel:+258820890320` (+258 82 089 0320)
- **E-mail Institucional**: `mailto:info@ow-servicos.co.mz`
- **Redes Sociais**: Instagram e Facebook `@ow_servicos`
