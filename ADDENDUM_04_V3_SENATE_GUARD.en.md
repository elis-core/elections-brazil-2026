# Addendum no. 4 to the publication commitment: first run of the estimator on 2026 data blocked by the Senate consistency guard; dated correction for the two Senate seats of 2026

> **British English version (D31).** This file translates `ADENDO_04_V3_GUARDA_SENADO.md` (Brazilian Portuguese), **SHA-256 of the pt-BR text, with LF line endings: `300e41e532540c8cf99713a492bd7fcc1becbc29e6fbedbfb96fe45ec6ef4adb`**. The pt-BR version is the reference and prevails in case of divergence.

**Addendum to the publication commitment of 24 October 2026.** The commitment is not changed. This addendum supplements Addenda no. 1, no. 2 and no. 3. The date and time of publication of this addendum are those of the public commit and of the upload to the OSF.

**What it is.** A proof of date **and a declaration of deviation**. Addendum no. 3 said that the estimator would be run on 2026 data "only with the version identified in Addenda no. 2 and no. 3, unchanged". This addendum records that the first run was blocked by a safeguard in the frozen code, that **no 2026 result was produced**, and that the safeguard has been corrected, **only** as regards the 2026 Senate, by a dated change (section 3) not yet used in any 2026 run. It contains no results, thresholds or lists of sections.

## 1. What happened on 27 October 2026 (UTC)

* **09:19Z.** The coordinator authorised in writing the run of **target A (first round of 2026)**. Target B (second round) remains conditional on the publication and checking of the section-level second-round data and **was not run**.
* **09:58Z to 10:09Z.** The section-level data of the 2026 first round (files downloaded from the TSE site on 7 October 2026) were loaded into the analysis database and checked against the detail file and against the official TSE tally of the first round. The 2014, 2018 and 2022 data in the database did not change.
* **10:26:32Z to 10:27:33Z.** **First run of target A.** In the 27 states, the consistency guard of the frozen code rejected the senator office, and the 27 states became "not assessable". No per-section output, metric or flag for 2026 was written. **Declared exposure:** during that run the launcher printed vote totals per state, and the ratio of senator votes to presidential votes (about 2) was observed; no estimator result existed. There were two earlier calls that read no 2026 data (one refused by the resource monitor at 09:29Z and one with no 2026 rows in the database at 09:34Z).
* **11:20Z.** The coordinator decided to correct the 2026 Senate factor.

## 2. The cause and the correction

In 2026, as in 2018, each state elects **two** senators and each voter casts **two** votes for senator. The total of senator votes is therefore about **double** the presidential total. The consistency guard, written only for 2018, tolerated double only in that year and treated 2026 as suspicious data. The number of seats is a fact of the electoral calendar, known before any 2026 data.

**The correction (a change of text):** `docs/15c` receives a dated addition ("Emenda datada (27/10/2026, D222)", in §2.4, next to the guard that tolerates "double plus 5% in the 2018 Senate", and in item 11.8) that extends the same factor to the 2026 Senate, and the adapter `ep_2026.py` applies factor 2 to the 2026 Senate. `desenhos_n3.py` and the tag `estimador-v3-congelamento-20261025` are **not altered**. The factor for the other offices and for the 2014 and 2022 Senate (one seat) **does not change**. Method, folds, targets, criteria, thresholds, parameters, cross-validation and the flagging rule **do not change**.

**Post-hoc nature, declared.** The need for the correction was discovered because the guard failed on 2026 data. The factor, however, follows from the number of seats, and the tolerance is the same as in 2018. The mandatory sentence of the 2026 report becomes: **"the 2026 Senate factor (two seats) was corrected after a first attempt refused by the guard; no parameter was adjusted by result"**. The first attempt and all its files are part of the report.

## 3. Hashes (SHA-256 with LF line endings)

**Authorisation of target A (27 October 2026) and state of the database.**

| File | SHA-256 | Bytes |
|---|---|---:|
| `resultados/camada_c/estimador_presidencial/v3/AUTORIZACAO_2026_alvoA_20261027.md` | `77b6c2f0812b633a4b7a2c38316a490d32812f42cee9b7cb691cdc9a5696d063` | 5938 |
| `resultados/camada_c/estimador_presidencial/v3/AUTORIZACAO_2026_hashes.json` | `bdb885bcb648496fdd820508cd3524ff7ae128fe8ac60395ea235b222cf7399a` | 749 |
| Analysis database `elis.duckdb` at the time of the first run (after loading the first round) | `cd548b3ab25badf57ca686a2228d227083fc07dc7f34ceb47b1405d002e16eeb` | 1615605760 |

**First run refused by the guard, and earlier calls** (repository commit `3a17c035fb26038247fff3ed0f78eb0520cfaf6d`, 27 October 2026, 10:36:32Z; folder `resultados/camada_c/estimador_presidencial/v3/2026/`):

| File | SHA-256 | Bytes |
|---|---|---:|
| `NOTA_tentativa_guarda_senado_20261027.md` | `831c347344f26e9fbc81a3cffed175b5ea1de97ec80782c798694a258e11e331` | 3954 |
| `MANIFESTO_tentativa_guarda_senado_T1026Z.json` | `f1189b4df289acae5b97654f4b793c4002e1931d4d289b7d4e08b825aa5414b5` | 8215 |
| `ufs_A_2026_tentativa_guarda_senado_T1026Z.json` | `8330c0de800af92a68d88ba4350fb1ab4e168ae05a542d9351fb74308b9727a9` | 7055 |
| `MONITOR_tentativa_guarda_senado_alvoA_20261027T1026Z.json` | `5d5e7030c42fbc48adf8282a222e1936f459507a7c345075bcf5ed0ebe4d5f07` | 1225 |
| `MONITOR_recusa_alvoA_20261027T0929Z.json` | `fb188e2d727c90b81afe3dcb3077a15e2f695cf3fed098b1ce3a745d072e1629` | 803 |
| `MANIFESTO_tentativa_sem_dados_T0933Z.json` | `53e96ed5122c65b6b75101fe137ee86fdda14b5744971cacfa93708d56c6a1b2` | 5099 |
| `ufs_A_2026_tentativa_sem_dados_T0933Z.json` | `4f53cda18c2baa0c0354bb5f9a3ecbe5ed12ab4d8e11ba873c2f11161202b945` | 2 |
| `MONITOR_tentativa_sem_dados_alvoA_20261027T0933Z.json` | `ebdc483b04cd09081f2469d7ae8a503687d43c898bae48e4504698620bb53bb5` | 1127 |

**Dated correction** (repository commits `cfc188616edad9c47a873ee97780dc4adf568685`, 2026-10-27T11:57:43Z, and `0c19af60e410d9ea69d367bf9c0e08880737f606`, 2026-10-27T12:34:31Z). The full reproduction of 2022 through the launcher with the amended adapter gave 108 of 108 per-state files and 13 of 13 derived tables identical byte for byte; no 2026 data were read in it.

| File | SHA-256 | Bytes | Commit |
|---|---|---:|---|
| `docs/15c_estimador_voto_presidencial_adendo.md` (dated addition in §2.4 and item 11.8) | `a827b7bd07069c42fb18a9c965ab2425308e695f037b8f0f3f68cc266538bea4` | 52232 | `cfc188616e` |
| `docs/15c_estimador_voto_presidencial_adendo.en.md` (en-GB) | `8276553010ebb6dabe71c3d43f28e8a14e19d6cd821fa5abd5c15fb948b26d71` | 52499 | `cfc188616e` |
| `docs/versoes/15c_estimador_voto_presidencial_adendo_v3_pre-emenda-D222.md` (copy before the amendment) | `49a95d2dead5a3409383685d0a958772d236b52f0115aa0fa8d3a9f2bec2ecbf` | 49020 | `cfc188616e` |
| `docs/versoes/15c_estimador_voto_presidencial_adendo_v3_pre-emenda-D222.en.md` (copy before the amendment, en-GB) | `a11f2bc0c27a5ed7be99e56ca2e705cf7c8071b99b7e7117695ad162f9c7883c` | 49328 | `cfc188616e` |
| `scripts/camada_c/ep_2026.py` (2026 Senate factor 2; previous version `f822e78341e11934df29f1c3414b61e77675cec0f46ea43e3f166b38bb3eab1e`) | `ead4797ac231d502fd859743dae7f021486d60b6ecfc4770eec9fe1a211a4b75` | 11630 | `cfc188616e` |
| `scripts/camada_c/test_ep_2026_senado.py` (synthetic test of the factor) | `23aa303dea44e37b9f1e49012c63d277bdaa181bc4d22410110d33c0d10d6fc2` | 4525 | `cfc188616e` |
| `scripts/camada_c/ep_2026_teste_reproducao_montagem.py` | `bd722fb4216fc537cf9ef35774dd69251f0d2a4ed9d24ba2480eeda9336d0808` | 5320 | `cfc188616e` |
| `scripts/camada_c/ep_2026_teste_reproducao_2022_completa.py` (full reproduction of 2022) | `7f0ab347276004527cbd599e2af61b12bfbfaa60310b55789b5cb6e4a127a5d1` | 3804 | `0c19af60e4` |
| `scripts/camada_c/ep_2026_manifesto_D222.py` | `5f6a81ecbdc17aa2a6a18ef8a192ab09b174a45b0b6cdb5c38b16e0786edeb8c` | 7701 | `0c19af60e4` |
| `resultados/camada_c/estimador_presidencial/v3/DIFF_ep_2026_D222_20261027.patch` | `c81d9980bddc3908df9a3ad8a72bd31dc76e5c42e7dcf1495821d0f9666fa450` | 4451 | `cfc188616e` |
| `resultados/camada_c/estimador_presidencial/v3/MANIFESTO_adaptador_2026_D222.json` (includes the result of the full reproduction of 2022) | `a1ae9287d621b91b3d4ab06524380eba5d9976c45f47935e96fce211c7935332` | 11491 | `0c19af60e4` |
| `resultados/camada_c/estimador_presidencial/v3/REPRODUCAO_montagem_D222_20261027.csv` (2014, 2018 and 2022: 162 units, 1458 components) | `7879a273cf6e1c6915147de20d2dd83154e2679ccb0c1f04c9eb43afce44a242` | 221031 | `cfc188616e` |
| `resultados/camada_c/estimador_presidencial/v3/REPRODUCAO_montagem_D222_20261027.json` | `d0acdbb884f9d3208d4c113fa1e68d5345f3e6dd5b9a00a192bd42b8f68d1166` | 904 | `cfc188616e` |
| `resultados/camada_c/estimador_presidencial/v3/REPRODUCAO_2022_completa_D222_20261027.csv` (108 per-state files and 13 derived tables, all identical) | `c583f090e6ec4a6cb3452010923e05d30b076cadf912e7bdc3d2b18615e5d3ca` | 28312 | `0c19af60e4` |
| `resultados/camada_c/estimador_presidencial/v3/REPRODUCAO_2022_completa_D222_20261027.json` | `4ffde8c6a0d647c7c3c55976d2c8df3f006971ad60355ed41f02f938eb9f5adc` | 766 | `0c19af60e4` |
| `resultados/camada_c/estimador_presidencial/v3/AUTORIZACAO_2026_alvoA_D222_20261027.md` (supersedes the authorisation `77b6c2f0…d063`) | `0555d89bf0d4bf427448b3bc41f2a175ad8bdd0e6e6dbff78d002d9f0ec97c6c` | 4969 | `cfc188616e` |
| `resultados/camada_c/estimador_presidencial/v3/AUTORIZACAO_2026_hashes.json` | `fb8140a46109ea5431a63a0418fa4bca59cdac9232d056ca747a16c0046219c4` | 1323 | `cfc188616e` |

The launcher `rodar_estimador_presidencial.py` (`f038123f67fe8964f04572778d51d326ced4c9118a50d58bbf937e3b33c44ea8`, Addendum no. 3) and the module `desenhos_n3.py` do **not** change (checked in the commit above).

## 4. What we commit to doing

* **Re-run target A on 2026 only after** the publication of this addendum with the hashes of the correction, of the reproduction test (identical byte for byte in 2014, 2018 and 2022) and of the new written authorisation, and with the independent checking of two sessions of the project.
* Run with **no other change** beyond the 2026 Senate factor.
* Publish **all** the estimator's results, whatever their direction, **including the record of the blocked attempt**, with the label sentence above.
* Not run target B until the section-level second-round data have been published by the official portal, loaded and checked.
* If another stage fails in the re-run, **report it and do not work around it**; the decision belongs to the coordinator and, if there is a change, it goes into a new dated addendum.
* State in the publication that there is a single implementation (no independent reproduction) and that the estimator was written and frozen before any 2026 data, with the two exceptions described in Addenda no. 3 and no. 4.

**What this addendum does not do.** It does not change the status, the declared limits or the publication commitment. It contains no 2026 results. A statistical signal is an anomaly to be investigated, and it does not indicate the cause.

**Licence.** This text is under the CC BY-ND 4.0 licence, like the other texts and documents in the repository.
