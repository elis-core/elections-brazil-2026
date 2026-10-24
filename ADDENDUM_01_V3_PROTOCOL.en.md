# Addendum no. 1 to the publication commitment: proof of date of the protocol for version 3 of the presidential-vote estimator

> **British English version (D31).** This file translates `ADENDO_01_V3_PROTOCOLO.md` (Brazilian Portuguese), **SHA-256 of the pt-BR text, with LF line endings: `1bd357c00c6cacbd1897bf52202c3a3867c8f1f9b0fd43e569dfdefc06829030`**. The pt-BR version is the reference and prevails in case of divergence.

---

**Addendum to the publication commitment of 24 October 2026.** The commitment is not changed. The protocol for version 3 of the estimator was fixed before any calculation of that version (see the commit below). The calculations of version 3 had already started at the time of this publication, and no result has been published. This addendum is published before voting starts in the second round (25 October 2026); the date and time of publication are those of the public commit and of the upload to the OSF.

**What it is.** A proof of date. This addendum records the SHA-256 of the protocol for version 3 of the presidential-vote estimator, fixed **before any calculation of that version**. The text of the protocol is **not** published now: it will be published together with the results of the project. This addendum **contains no results, thresholds or lists of sections**.

**Context.** The estimator is an exploratory model, at the level of the electoral section, that calculates the expected value of the composition of the presidential vote from the other offices, with an interval and a residual for each section. Version 1 and version 2 are identified in the commitment. After them, an extra validation, with data from 2014, 2018 and 2022, pointed to limits of the method. Version 3 addresses those limits and is therefore **later** than version 2 and the extra validation (**post hoc**).

**Extra validation (already complete; report not yet published).** Repository commit: `d9e5ec873fca1db05d9d5ab7b6500d7d3973a529` (24 October 2026, 17:57:02Z). SHA-256 (LF line endings):

| File | SHA-256 (LF line endings) |
|---|---|
| `resultados/camada_c/estimador_presidencial/validacao_extra/PROTOCOLO_20261024.md` | `d47e3ea61a76637001ea0810c7ae9ed3901d11a544be13872e63eea700347952` |
| `resultados/camada_c/estimador_presidencial/validacao_extra/RELATORIO_validacao_extra_20261024.md` | `c53799685c41576100f9be6cd4b61623752467e4002d5279e94dc77406017d9b` |
| `resultados/camada_c/estimador_presidencial/validacao_extra/RELATORIO_validacao_extra_20261024.en.md` | `71cc63b260de55373431e20519466cd8adf03eba5b0e1672fb5068e72fafed68` |

**Protocol for version 3.** Repository commit: `c35947ede6c6de9af552570f6faa0a12476bf3f9`, of **24 October 2026, 18:35:56Z** (15:35:56 in Brasília). The commit is later than the record of the decision that authorised version 3 (commit `7ba29a0c1d03852ba9c9d9f82b1b61ac21a92246`, 24 October 2026, 18:32:34Z) and earlier than any calculation of version 3.

| File | SHA-256 (LF line endings) | Bytes |
|---|---|---:|
| `resultados/camada_c/estimador_presidencial/v3/PROTOCOLO_v3_20261024.md` | `183adf9d33131239b9c754f021f6fbfa6bce18a2754227140407a668ff57421e` | 10515 |

**What we commit to do.**

* One single version 3, with no further cycle of testing and adjustment after it.
* Use only data from 2014, 2018 and 2022. No 2026 data is used to develop, to choose the model or to fix a criterion or threshold.
* Change no criterion or threshold of the protocol after running. Whatever does not meet the criteria of the protocol is not adopted, and the failure is reported.
* Publish the text of the protocol and **all** the results of version 3 and of the extra validation, whatever their direction, together with the results of the project, as the commitment states.
* Publish, in a second addendum and by **25 October 2026, 18:00Z**, the SHA-256 of the text, the code and the manifest of version 3. If version 3 cannot be completed by then, the second addendum says so, and version 2 and the extra validation stand as they are.

**What this addendum does not do.** It does not change the status, the declared limits or the publication commitment. A statistical signal is an anomaly to be investigated, and it does not indicate the cause.

**Licence.** This text is under the CC BY-ND 4.0 licence, like the other texts and documents in the repository.
