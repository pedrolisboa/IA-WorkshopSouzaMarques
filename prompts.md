# Prompts das demos

Os prompts usados durante a oficina. A ideia é você rodar todos na **mesma planilha**, no **mesmo chat**, e comparar o que muda no resultado.

---

## Demo 1 — Planilha bagunçada

**Antes de começar:** faça upload de [`planilha_demo1.csv`](planilha_demo1.csv) na sua IA (precisa ter code interpreter / análise de dados ativo — ChatGPT Plus, Claude, Gemini, etc.).

A progressão abaixo vai do mais vago ao mais profissional. **Rode todos no mesmo chat com a mesma planilha** para ver como a qualidade do prompt define a qualidade da resposta.

### Nível 0 — O vibe-prompt

```
Limpa essa planilha.
```

Vai funcionar. Mas você consegue conferir o que ele fez? Sabe que critério usou? Vai aceitar?

### Nível 1 — Adiciona contexto

```
Limpa essa planilha de dados de pesquisa clínica. Quero usar pra análise.
```

Melhora. Agora a IA sabe o domínio. Mas o critério de "limpo" continua implícito — quem está decidindo o que é outlier, você ou ela?

### Nível 2 — Esqueleto completo (contexto · sucesso · verificação)

```
Limpa essa planilha: deduplica, normaliza os formatos de data inconsistentes,
identifica outliers em age e lab_creatinina, e me dá resumo descritivo
(contagem, mediana, mínimo, máximo) por diagnosis_code. Me explique em
português o que você jogou fora e por quê.
```

Esse é o padrão defensável. Você sabe o que pediu, sabe o que esperar, e tem a explicação que permite conferir cada decisão.

### Nível 3 — Padrão profissional (auditoria antes de executar)

```
Você vai limpar uma planilha de pesquisa clínica fictícia (30 linhas).
Antes de qualquer transformação:

1. Faça inventário do que encontrou de errado (duplicatas, valores faltantes,
   outliers, formatos inconsistentes, valores em formato errado).
   Liste com número de linha.
2. Para cada problema, proponha uma operação E me diga o critério usado
   (ex.: "outlier de age = qualquer valor fora de 0–120").
3. NÃO execute nada ainda. Espere meu OK.

Depois que eu aprovar, faça as transformações e me retorne:
- linhas antes/depois
- summary descritivo por diagnosis_code (n, mediana, IQR de length_of_stay)
- log do que jogou fora, linha por linha
- coisas que VOCÊ ficou em dúvida e que eu, humano, deveria revisar antes
  de aceitar
```

Esse é o padrão para dado que vai virar publicação ou apoio a decisão clínica. Mais lento — mas você aprova cada decisão antes que aconteça.

---

## Experimentos que provocam falhas (use como contra-exemplo)

Cada um destes prompts é projetado para induzir um modo de falha específico. Rode pra ver acontecer.

### Confabulação — pede o que não existe nos dados

```
Calcule a taxa de mortalidade neste dataset por faixa etária.
```

> **Observe:** a planilha não tem coluna de mortalidade. Como a IA reage? Recusa? Inventa? Usa proxy sem avisar? A diferença separa modelo honesto de modelo confabulando.

### Suposições silenciosas

```
Remove os outliers.
```

> **Observe:** sem critério explícito, a IA decide sozinha. Qual o critério? Ela disse? Se isso virasse análise estatística pra publicação, você teria que justificar o método para o revisor — e a IA não te deu a justificativa.

### Insights alucinados

```
Que padrões interessantes você vê nesses dados?
```

> **Observe:** com 30 linhas, nenhum "padrão" é estatisticamente justificável. Mas a IA vai apresentar achados como se fossem. Plausível ≠ verdadeiro.

### Sumário que esconde defeitos

```
Me dá um executive summary desses dados em 3 bullets.
```

> **Observe:** o sumário vai mencionar os problemas do dado bruto (duplicatas, outliers absurdos, valores em formato errado)? Ou vai apresentar tudo como dado limpo?

---

## Variações para aprofundar

Se você quiser explorar mais, tente:

### Pergunta clínica direta com verificação possível

```
Para cada diagnosis_code, quantos pacientes ficaram internados acima da
mediana geral de length_of_stay? Me dê uma tabela em markdown, e me mostre
os números que você usou (mediana geral, valores individuais por grupo).
```

### Pergunta com auditoria embutida

```
Identifique qualquer linha cujos valores sejam clinicamente implausíveis
(considerando humanos vivos). Para cada uma, explique por quê e sugira:
remover, corrigir (e como), ou marcar como suspeita pra revisão humana.
```

### Pergunta de juízo metodológico

```
Se eu quisesse publicar uma análise descritiva desses dados, que cuidados
metodológicos você sugere antes? Liste com prioridade.
```

---

## Demo 2 — Deep research (ANVISA)

Use uma ferramenta com modo "Deep Research": Claude, ChatGPT, Gemini ou Perplexity. Espere 10–20 minutos para a resposta completa.

```
Liste os sistemas de Inteligência Artificial aprovados pela ANVISA para uso
médico no Brasil. Para cada sistema, forneça em formato estruturado:

- Nome do produto/sistema
- Fabricante
- Classe de risco (I, II, III ou IV)
- Indicação de uso (área clínica e função)
- RDC aplicável
- Número de registro ANVISA, quando disponível
- Ano de aprovação

Para cada item, cite a fonte consultada com link, quando possível. Se houver
incerteza sobre alguma informação, marque explicitamente como "não confirmado"
— prefiro honestidade sobre completude.
```

### Como verificar o resultado

1. Pegue 2–3 itens listados na resposta.
2. Para cada um, abra o [portal da ANVISA](https://consultas.anvisa.gov.br) ou faça uma busca pelo nome do fabricante.
3. Confirme: o fabricante existe? O número de registro corresponde? A RDC citada é real?
4. Se algum item for **confabulado** (referência plausível mas falsa) — anote. É exatamente o que a oficina ensina a procurar.

---

## A tese

> *A IA é uma máquina estatística. Vai errar com confiança.
> A responsabilidade é de quem assina — e não há mais ninguém para assinar.*

Tudo aqui é exercício pra você internalizar essa frase. Quando achar uma resposta da IA que parece pronta, a pergunta certa é: *"como vou conferir?"*
