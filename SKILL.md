---
name: stop-slop-pt-br
description: Remove vícios de escrita de IA em textos em português do Brasil. Use ao redigir, editar ou revisar qualquer texto em pt-BR (mensagens, docs, PRs, posts, e-mails, cards do Jira) para cortar frases feitas, estruturas previsíveis e tom robótico. Gatilhos: "revisa esse texto", "tira a cara de IA", "deixa mais humano", "stop slop", "texto em português".
metadata:
  trigger: Escrever ou revisar prosa em português do Brasil
  author: Adaptação pt-BR de stop-slop, de Hardik Pandya (https://hvpandya.com), licença MIT
---

# Stop Slop (pt-BR)

Corte os padrões que denunciam texto gerado por IA em português do Brasil.

## Regras centrais

1. **Corte as frases de enchimento.** Tire aberturas que anunciam o assunto, muletas de ênfase, fechamentos de cortesia e advérbios. Lista em [references/frases.md](references/frases.md).

2. **Quebre as estruturas de fórmula.** Evite contraste binário ("não é X, é Y"), lista pela negação, fragmentação dramática, pergunta retórica seguida de resposta e agência falsa. Lista em [references/estruturas.md](references/estruturas.md).

3. **Use voz ativa com sujeito humano.** Nada de "foi realizado", "se faz necessário", "é recomendado que". Diga quem faz. Coisas não agem sozinhas: "os dados mostram" vira "o time leu os dados e viu".

4. **Troque substantivo por verbo.** "Realizar a implementação" vira "implementar". "Efetuar o pagamento" vira "pagar". "Fazer uso de" vira "usar".

5. **Seja específico.** Nada de declaração vaga ("os impactos são significativos"). Nomeie o impacto. Nada de "sempre", "nunca", "todos" fazendo trabalho vago.

6. **Fale com o leitor.** "Você" em vez de "as pessoas" ou "o usuário". Exemplo concreto em vez de abstração.

7. **Varie o ritmo.** Misture frases curtas e longas. Duas coisas valem mais que três. Termine parágrafos de jeitos diferentes. Sem travessão no texto expositivo.

8. **Confie no leitor.** Afirme direto. Sem amaciar, sem justificar demais, sem pegar na mão.

9. **Corte a frase de efeito.** Se parece frase de LinkedIn ou de citação em destaque, reescreva.

## Checagem rápida

Antes de entregar o texto:

- Abre com "Vale ressaltar", "É importante destacar", "No cenário atual", "Ótima pergunta"? Corte e comece pelo conteúdo.
- Fecha com "Espero ter ajudado", "Fico à disposição", "Em suma"? Corte.
- Tem advérbio em -mente ou locução adverbial ("de forma eficiente", "de maneira significativa")? Tire ou troque por fato.
- Tem voz passiva ou "se" impessoal? Ache quem fez e ponha na frente.
- Tem coisa fazendo ação de gente ("a decisão surge", "o mercado exige")? Nomeie a pessoa.
- Tem "não é X, é Y" ou "mais do que X, é Y"? Diga Y direto.
- Tem gerundismo ("vou estar enviando")? Troque por "vou enviar" ou "envio".
- Tem substantivo onde caberia verbo ("realizar a análise")? Use o verbo.
- Tem lista de três adjetivos ("rápido, seguro e eficiente")? Fique com um ou dois que você consegue provar.
- Três frases seguidas com o mesmo tamanho? Quebre uma.
- Todo parágrafo termina com frase de impacto? Varie.
- Tem travessão (—)? Troque por vírgula, ponto, dois-pontos ou parênteses.
- Tem jargão ("alavancar", "potencializar", "jornada", "ecossistema", "robusto")? Troque por palavra comum.
- Tem anglicismo de tradução ("endereçar o problema", "no final do dia", "performar")? Use o termo em português.
- Título em Title Case ("Como Melhorar Seu Processo")? Português usa só a primeira maiúscula.
- Tem exclamação ou emoji sem motivo? Tire.

## Pontuação

Dê nota de 1 a 10 em cada dimensão:

| Dimensão | Pergunta |
| -------- | -------- |
| Objetividade | Afirma ou anuncia? |
| Ritmo | Variado ou de metrônomo? |
| Confiança | Respeita a inteligência do leitor? |
| Autenticidade | Soa como uma pessoa falando? |
| Densidade | Sobra alguma coisa para cortar? |

Abaixo de 35/50: reescreva.

## O que não muda

- Termos técnicos, nomes de campos, código e citações literais ficam como estão.
- Travessão em diálogo de ficção é norma do português e pode ficar.
- Advérbio que carrega informação (tempo, lugar, negação: "ontem", "aqui", "não") fica. O alvo é o advérbio de ênfase e de enrolação.
- Voz passiva pode ficar quando o agente é desconhecido ou irrelevante e o texto é técnico ("o pacote foi descontinuado em 2024").

## Exemplos

Antes e depois em [references/exemplos.md](references/exemplos.md).

## Licença

MIT. Adaptação para português do Brasil do projeto stop-slop (https://github.com/hardikpandya/stop-slop). Veja LICENSE.
