# Trabalhar com IA: o que muda na sua segunda-feira

Material complementar da oficina apresentada no **Congresso da Faculdade Souza Marques** em 12 de junho de 2026.


---

## O que tem aqui

- [`planilha_demo1.csv`](planilha_demo1.csv) — Planilha clínica **fictícia** com 30 linhas, usada na Demo 1 da oficina. Contém problemas plantados de propósito (duplicatas, valores impossíveis, formatos inconsistentes) para você experimentar limpeza de dados com IA.
- [`prompts.md`](prompts.md) — Os prompts usados nas demos, organizados em uma progressão do mais vago ao mais profissional, mais experimentos que provocam falhas específicas.
- [`referencias.md`](referencias.md) — As fontes citadas durante a oficina, todas verificadas na fonte primária.

---

## Como usar

### Demo 1 — Planilha bagunçada

1. Baixe o arquivo [`planilha_demo1.csv`](planilha_demo1.csv).
2. Abra uma IA com capacidade de executar código (ChatGPT, Claude, Gemini — qualquer uma com code interpreter / análise de dados ativa).
3. Faça upload do CSV na conversa.
4. Escolha um prompt de [`prompts.md`](prompts.md). Sugestão: comece pelo "vibe-prompt" e vá subindo até o "padrão profissional" — compare como o resultado muda.
5. **Confira o resultado.** Esse é o ponto da oficina inteira.

### Demo 2 — Deep research

Use o prompt da query da ANVISA em [`prompts.md`](prompts.md). Rode em qualquer ferramenta com modo "Deep Research" (Claude, ChatGPT, Gemini, Perplexity). Verifique 2–3 referências citadas contra o portal da ANVISA (consultas.anvisa.gov.br) antes de aceitar qualquer item.

---

## ⚠️ Aviso sobre os dados

O arquivo `planilha_demo1.csv` contém **dados fictícios** — gerados especificamente para fins pedagógicos. Não representam pacientes reais. Os campos imitam a estrutura de um export de pesquisa clínica (patient_id, age, sex, diagnosis_code, lab_creatinina, visit_date, length_of_stay), mas todos os valores são inventados.

Não use esse arquivo como base para análise clínica real. Não use o padrão dos prompts aqui sobre dados reais de pacientes sem antes ler a [Resolução CFM nº 2.454/2026](https://portal.cfm.org.br) e considerar implicações de sigilo médico e LGPD.

---

## Tese central da oficina

> *A IA é uma máquina estatística. Vai errar com confiança.
> A responsabilidade é de quem assina — e não há mais ninguém para assinar.*

---

## Licença

Os materiais deste repositório (textos, prompts, dataset fictício) estão disponíveis sob a licença [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Você pode usar, modificar e redistribuir, desde que dê o crédito apropriado.

---

## Contato

Para feedback, perguntas ou correções: abrir uma issue neste repositório.
