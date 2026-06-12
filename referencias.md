# Referências verificadas

Todas as fontes citadas durante a oficina foram verificadas contra a fonte primária. Os DOIs e links abaixo permitem que você confira diretamente.

---

## Evidência empírica

**Parasuraman, R. & Manzey, D. (2010).** Complacency and Bias in Human Use of Automation: An Attentional Integration. *Human Factors* 52(3), 381–410.
DOI: [10.1177/0018720810376055](https://doi.org/10.1177/0018720810376055) · PMID: 21077562

> Revisão integrativa que sintetiza décadas de pesquisa em automation bias. Trecho-chave do abstract: *"Automation complacency is found in both naive and expert participants and cannot be overcome with simple practice."*

**Alberdi, E., Povykalo, A., Strigini, L. & Ayton, P. (2004).** Effects of incorrect computer-aided detection (CAD) output on human decision-making in mammography. *Academic Radiology* 11(8), 909–918.
DOI: [10.1016/j.acra.2004.05.012](https://doi.org/10.1016/j.acra.2004.05.012) · PMID: 15354301

> Quando o CAD errava em mamografia, radiologistas tiveram sensibilidade MENOR do que sem apoio nenhum.

**Rezazade Mehrizi, M.H., Mol, F., Peter, M. et al. (2023).** The impact of AI suggestions on radiologists' decisions: a pilot study of explainability and attitudinal priming interventions in mammography examination. *Scientific Reports* 13:9230.
DOI: [10.1038/s41598-023-36435-3](https://doi.org/10.1038/s41598-023-36435-3)

> Estudo com 92 radiologistas. Nem explicar a IA pra eles desfez o viés de automação.

---

## Filosofia & epistemologia

**Hicks, M.T., Humphries, J. & Slater, J. (2024).** ChatGPT is bullshit. *Ethics and Information Technology* 26:38.
DOI: [10.1007/s10676-024-09775-5](https://doi.org/10.1007/s10676-024-09775-5)

> Argumenta que "alucinação" é uma metáfora equivocada — o problema dos LLMs é *indiferença à verdade*, no sentido filosófico de Frankfurt.

**Matthias, A. (2004).** The responsibility gap: Ascribing responsibility for the actions of learning automata. *Ethics and Information Technology* 6, 175–183.
DOI: [10.1007/s10676-004-3422-1](https://doi.org/10.1007/s10676-004-3422-1)

> O paper que popularizou a tese do "vácuo de responsabilidade". Importante notar que cobre máquinas que continuam aprendendo em deployment — não LLMs com pesos congelados.

---

## Normativo · Brasil

**Resolução CFM nº 2.454/2026** — Normatiza o uso da inteligência artificial na medicina. Publicada em 27/02/2026 (retificada em 05/03/2026), em vigor a partir de 26/08/2026. Disponível em: [portal.cfm.org.br](https://portal.cfm.org.br)

Artigos centrais para profissionais:
- **Art. 4°** — Deveres do médico: IA exclusivamente como apoio; julgamento crítico obrigatório; uso registrado no prontuário.
- **Art. 5° §2°** — *É vedado ao médico delegar à IA a comunicação de diagnósticos, prognósticos ou decisões terapêuticas, sem a devida mediação humana.*
- **Art. 7°** — *O médico permanece integralmente responsável pelos atos médicos por ele praticados mediante a utilização de modelos, sistemas e aplicações de IA.*
- **Art. 11** — Qualquer utilização de IA deverá ser comunicada e explicada ao paciente.
- **Art. 18 §1°** — *Em nenhum momento os modelos, sistemas e aplicações de IA na medicina poderão restringir ou substituir a autoridade final do médico.*
- **Anexo I, XVII** — Definição formal de "prompt".

**LGPD — Lei nº 13.709/2018** — Lei Geral de Proteção de Dados Pessoais.
- **Art. 5°, II** — Define dado pessoal sensível, incluindo dado referente à saúde.
- **Art. 11** — Tratamento de dados pessoais sensíveis.

---

## Indústria & mercado

**Gartner (2026).** Half of Companies That Cut Customer Service Staff Due to AI Will Rehire by 2027. Press release de 03/02/2026.
https://www.gartner.com/en/newsroom/press-releases/2026-02-03-gartner-predicts-half-of-companies-that-cut-customer-service-staff-due-to-ai-will-rehire-by-2027

> Previsão baseada em survey com 321 líderes de customer service em outubro de 2025. Importante: apenas 20% efetivamente reduziram headcount por causa de IA (o restante foi atribuído a IA mas tinha outras causas).

**Veracode (2025).** 2025 GenAI Code Security Report.
https://www.veracode.com/resources/analyst-reports/2025-genai-code-security-report/

> Teste de 80 tarefas de codificação em mais de 100 LLMs. 45% das saídas continham vulnerabilidades OWASP Top 10. XSS com 86% de falha; log injection com 88%. Java foi a linguagem com pior desempenho (~70% de falha).

**Palmer, M. & Low, K. (2025).** Auditoria automatizada de 1.645 aplicações do showcase do Lovable.

> 170 aplicações (10,3%) com falhas críticas de segurança; 303 endpoints vulneráveis. Associado a CVE-2025-48757 (Broken Object Level Authorization). Cobertura inicial: *The Register*, 27/02/2026.

---

## Outras leituras úteis (não citadas diretamente na oficina)

- **Forrester (2026).** *Future of Work* outlook — projeta reversão de metade dos layoffs atribuídos a IA.
- **Challenger, Gray & Christmas (2025).** Jobs report — menos de 5% dos layoffs nos EUA em 2025 foram diretamente atribuídos a IA.
- **Sparrow, R. (2007).** Killer robots. *Journal of Applied Philosophy* 24(1), 62–77. (Argumenta a favor do responsibility gap em sistemas autônomos.)
- **Tigard, D. (2021).** There Is No Techno-Responsibility Gap. *Philosophy & Technology*. (Argumenta contra.)
- **Königs, P. (2022).** Artificial intelligence and responsibility gaps: what is the problem? *Ethics and Information Technology*.
