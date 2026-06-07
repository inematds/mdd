# MDD — Mestre de Direção Dinâmica

Skill para [Claude Code](https://claude.com/claude-code) que transforma **qualquer assunto** em um pacote completo de direção de vídeo dinâmico, pronto pra gerar em Seedance, Kling, Runway, Veo, Luma ou similares.

Em vez de devolver "uma pessoa usando X", a skill dirige uma **cena com movimento, intenção e continuidade**: câmera que muda por motivo, ação que progride e um fechamento forte.

## O que ela gera

Para qualquer assunto, sempre na mesma ordem:

| Bloco | Conteúdo |
| --- | --- |
| **01 Cartão do projeto** | título, linha meta, prioridade, micro brief |
| **02 Pacote de cena** | premissa, resumo, local, elementos, estado inicial/final, cadeia de ação |
| **03 Bloqueios de estilo** | o que não muda: estilo, câmera, efeitos, continuidade, negativo |
| **04 Storyboard** | 8/12/16 painéis — câmera, ação, continuidade, efeito, intenção emocional |
| **05 Faixa do diretor** | beat, câmera, ação, ritmo, escalação, estado, estilo |
| **06 Prompt final de vídeo** | prompt limpo pra colar na ferramenta de geração |
| **07 Prompt negativo** | tudo que a IA deve evitar |

## A fórmula central

> **Assunto → conflito visual → progressão → virada → impacto suspenso.**

Sem conflito visual, o vídeo fica parado. A skill encontra o conflito antes de montar o storyboard (produto: problema vs solução; imóvel: espaço comum vs experiência desejada; IA: tela vazia vs revelação; etc.).

E a regra de ouro de cada tomada:

> **Câmera + ação + continuidade + emoção + efeito permitido.**

## Como usar

Com a skill instalada, basta pedir em linguagem natural:

```
direção dinâmica sobre IA no cinema
```
```
monta um pacote de vídeo dinâmico pra esse produto, versão 9:16, 15s
```
```
transforma em 12 tomadas e usa o preset de imobiliário
```

A skill não trava com perguntas: se faltar formato, duração ou estilo, ela assume a opção mais forte pro conflito visual e declara a suposição. A **chamada principal fica fora do prompt de vídeo** (vai na edição), pra evitar que a IA renderize texto torto.

## Estrutura

```
skill/
├── SKILL.md                    # fluxo, fórmula de ouro, template 01–07, checklist de qualidade
└── references/
    ├── biblioteca-tomadas.md   # tomadas de câmera (push-in, crash zoom, orbit…) + sequências por assunto
    └── presets.md              # 6 presets de estilo + guia de conflito visual por domínio
```

### Presets disponíveis

Ação/esporte · Produto premium · Tecnologia/IA · Imobiliário · Evento · História emocional.

## Instalação

Copie a pasta `skill/` para o diretório de skills do Claude Code, com o nome da skill:

```bash
cp -r skill ~/.claude/skills/mestre-direcao-dinamica
```

A skill passa a ser acionada automaticamente quando você pedir "direção dinâmica", "vídeo dinâmico sobre X", "storyboard + prompt de vídeo", "pacote de vídeo" ou der um assunto pra virar vídeo cinematográfico.

## Licença

MIT.
