# stop-slop-pt-br

Skill para o Claude (Claude Code, claude.ai e Agent SDK) que tira a cara de IA de textos em português do Brasil.

Adaptação pt-BR do [stop-slop](https://github.com/hardikpandya/stop-slop), de Hardik Pandya. A original lista vícios do inglês; esta lista os que a IA comete em português: "Vale ressaltar que", "No cenário atual", "Ótima pergunta!", "alavancar", "endereçar o problema", "vou estar enviando", "Não é X, é Y" e companhia.

## O que ela corta

| Categoria | Exemplos |
| --------- | -------- |
| Aberturas e fechamentos | "Vale ressaltar que", "Dito isso", "Espero ter ajudado", "Fico à disposição" |
| Bajulação | "Ótima pergunta!", "Faz total sentido", "Perfeito!", "Com certeza!" |
| Jargão | alavancar, potencializar, jornada, ecossistema, robusto, agregar valor |
| Anglicismos | endereçar o problema, no final do dia, performar |
| Burocratês | "realizar a implementação", "se faz necessário", "a nível de" |
| Gerundismo | "vou estar enviando" |
| Estruturas | "Mais do que X, é Y", "O resultado? Incrível.", tríade de adjetivos, agência falsa |
| Formatação | Title Case em título, travessão em texto expositivo, emoji como marcador |

Ela também dá nota de 1 a 50 ao texto (objetividade, ritmo, confiança, autenticidade e densidade) e manda reescrever abaixo de 35.

## Instalação

### Claude Code (global, vale para todos os projetos)

```bash
git clone https://github.com/leolegends/stop-slop-pt-br ~/.claude/skills/stop-slop-pt-br
```

### Claude Code (só um projeto)

```bash
git clone https://github.com/leolegends/stop-slop-pt-br .claude/skills/stop-slop-pt-br
```

Numa sessão já aberta, rode `/reload-skills`. Sessões novas carregam sozinhas.

### claude.ai

Baixe o repositório como ZIP e envie em **Configurações → Capacidades → Skills**.

### Atualizar

```bash
git -C ~/.claude/skills/stop-slop-pt-br pull
```

## Como usar

- Chame direto: `/stop-slop-pt-br`
- Ou peça: "revisa esse texto", "tira a cara de IA", "deixa mais humano"
- O Claude também aplica sozinho quando você pede para escrever ou revisar texto em português.

## Estrutura

```
stop-slop-pt-br/
├── SKILL.md                  # regras centrais, checagem rápida e pontuação
├── references/
│   ├── frases.md             # frases, jargão, anglicismos, burocratês, advérbios
│   ├── estruturas.md         # estruturas de fórmula, agência falsa, ritmo, formatação
│   └── exemplos.md           # 7 exemplos de antes e depois
└── LICENSE
```

## Contribuir

Achou um vício que falta? Abra uma issue ou um PR com o padrão, o motivo e um exemplo de antes e depois.

## Licença

MIT. Baseado em [stop-slop](https://github.com/hardikpandya/stop-slop) © Hardik Pandya.
