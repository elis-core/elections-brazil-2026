# elections-brazil-2026

**PT** · Análise estatística pré-registrada das eleições gerais de 2026 no Brasil. **EN** · Pre-registered statistical analysis of Brazil's 2026 general elections.

[Português](#português) · [English](#english)

---

## Português

**Análise estatística pré-registrada (OSF `9gbtn`) das eleições gerais de 2026 no Brasil: documentos, código, hashes de verificação e canal de revisão aberta.** Um sinal estatístico é uma anomalia a investigar, não prova de fraude nem de regularidade. Resultados publicados após a proclamação do 2º turno.

**Estado: só o compromisso.** Neste momento, este repositório contém **apenas** o compromisso de publicação, a lista de SHA-256 dos arquivos registrados e a política do canal de revisão. **Não há resultados, limiares, listas de seções nem dados de 2026.** Os resultados serão publicados depois de concluída a análise do 2º turno e da proclamação do resultado da eleição pelo TSE (o que ocorrer por último); a data será anunciada com antecedência, aqui e na página do projeto na OSF.

### O que é

Uma pesquisa científica independente que analisa, por meios estatísticos indiretos, os resultados das eleições gerais de 2026, em comparação com 2018 e 2022. O método foi registrado na OSF antes da eleição (registro `9gbtn`, https://osf.io/9gbtn/) e complementado por um adendo, depositado antes do 2º turno. O registro permanece sob embargo da OSF para que métodos e limiares não sejam usados para evitar a sua detecção durante a coleta do 2º turno.

### Estatuto

Pesquisa científica independente, publicada para avaliação dos interessados. Não passou por revisão por pares nem por reprodução integral por estatístico humano, pela dimensão do trabalho. O método foi registrado antes da eleição; os desvios do registro serão listados na publicação dos resultados. **O método só detecta deslocamentos amplos; a ausência de achados não prova ausência de irregularidades.** As duas implementações do modelo são de dois fornecedores de IA, e a independente é do mesmo fornecedor que redigiu a especificação. Este trabalho **não tenta provar fraude nem provar que está tudo certo**; "anomalia" **não** significa "fraude".

### Compromisso e provas de data

- `COMPROMISSO.md` (pt-BR) e `COMMITMENT.en.md` (en-GB): o texto do compromisso.
- `HASHES.txt`: SHA-256 (finais de linha LF) dos arquivos registrados na OSF. O SHA-256 deste arquivo está em `COMPROMISSO.md`.
- Para conferir: obtenha da OSF (quando o embargo terminar) ou de quem tiver autorização o arquivo registrado e compare o seu SHA-256 com a linha correspondente de `HASHES.txt`; em arquivos de texto, converta antes os finais de linha para LF.

### Revisão aberta

A revisão abre quando os resultados forem publicados. Nessa data, achados, erros, lacunas e alternativas melhores serão relatados por *issue* neste repositório (o canal está **desativado até lá**); a primeira rodada dura **21 dias**, cada achado recebe resposta em até **7 dias**, e todos os achados, com a resposta do projeto, serão publicados. Antes dessa data não há resultado a revisar.

### Licença

O **código** está sob a licença **Apache-2.0** (arquivo `LICENSE`); os **textos, documentos e agregados** estão sob a licença **CC BY-ND 4.0** (arquivo `LICENSE-docs`), com atribuição. Os arquivos brutos do TSE e a documentação de terceiros não fazem parte deste repositório.

---

## English

**Pre-registered statistical analysis (OSF `9gbtn`) of Brazil's 2026 general elections: documents, code, verification hashes and an open-review channel.** A statistical signal is an anomaly to investigate, not proof of fraud or of regularity. Results are published after the second round is proclaimed.

**Status: the commitment only.** At this time, this repository contains **only** the publication commitment, the list of SHA-256 hashes of the registered files and the policy of the review channel. **There are no results, thresholds, lists of sections or 2026 data.** The results will be published after the analysis of the second round is complete and after the TSE proclaims the result of the election (whichever comes last); the date will be announced in advance, here and on the project page on the OSF.

### What this is

An independent scientific study that analyses, by indirect statistical means, the results of the 2026 general elections, in comparison with 2018 and 2022. The method was registered on the OSF before the election (registration `9gbtn`, https://osf.io/9gbtn/) and supplemented by an addendum deposited before the second round. The registration remains under OSF embargo so that methods and thresholds cannot be used to avoid their detection during the collection of the second round.

### Status of the work

Independent scientific research, published for evaluation by interested parties. It has not been peer reviewed, nor fully reproduced by a human statistician, given the size of the work. The method was registered before the election; deviations from the registration will be listed in the publication of the results. **The method only detects broad shifts; the absence of findings does not prove the absence of irregularities.** The two implementations of the model are from two AI providers, and the independent one is from the same provider that wrote the specification. This work **does not try to prove fraud nor to prove that everything is right**; an "anomaly" does **not** mean "fraud".

### Commitment and proof of date

- `COMPROMISSO.md` (pt-BR) and `COMMITMENT.en.md` (en-GB): the text of the commitment.
- `HASHES.txt`: SHA-256 (LF line endings) of the files registered on the OSF. The SHA-256 of this file is in `COMPROMISSO.md`.
- To check: obtain the registered file from the OSF (when the embargo ends) or from someone authorised, and compare its SHA-256 with the corresponding line of `HASHES.txt`; for text files, convert line endings to LF first.

### Open review

The review opens when the results are published. On that date, findings, errors, gaps and better alternatives will be reported as an *issue* in this repository (the channel is **disabled until then**); the first round lasts **21 days**, each finding receives a reply within **7 days**, and all findings, with the project's reply, will be published. Before that date there is no result to review.

### Licence

The **code** is under the **Apache-2.0** licence (`LICENSE` file); the **texts, documents and aggregates** are under the **CC BY-ND 4.0** licence (`LICENSE-docs` file), with attribution. The TSE raw files and third-party documentation are not part of this repository.
