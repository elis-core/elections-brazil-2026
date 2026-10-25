# Addendum no. 3 to the publication commitment: proof of date of the 2026 data-loading adapter of the presidential-vote estimator (code, protocol and report of the reproduction test)

> **British English version (D31).** This file translates `ADENDO_03_V3_ADAPTADOR.md` (Brazilian Portuguese), **SHA-256 of the pt-BR text, with LF line endings: `ba4cd3ad34eb675f83b79bc4551437eca030e689791455fb61d3179d6705dc55`**. The pt-BR version is the reference and prevails in case of divergence.

---

**Addendum to the publication commitment of 24 October 2026.** The commitment is not changed. This addendum complements Addenda no. 1 and no. 2 and was prepared before any run of the estimator on 2026 data. The date and time of publication of this addendum are those of the public commit and of the upload to the OSF.

**What it is.** A proof of date. This addendum records the SHA-256 of the code of the 2026 data-loading adapter, of the protocol of its test and of the report of the reproduction test on 2022. The adapter **only loads data**: it does not change the model, the folds, the targets, the criteria, the thresholds or the flagging rule of version 3. This addendum **contains no results, thresholds or lists of sections**.

**Freeze of version 3 (not published before).** Annotated tag `estimador-v3-congelamento-20261025` (object `5b162d96aa15df55fed6a9e826c794211ea3156f`), created on 25 October 2026, 10:09:45Z, on commit `a3575714bedac13f5d9c5c3942ce86211543eccd`. Freeze manifest `MANIFESTO_congelamento_v3.json`, SHA-256 `f68d1b32c87eca713936805dfa700827aa9bd0cdb9c91f5a064d24db65cffc1c`, commit `f17840f2fc0ce059bb34185bdb211864c85e7735` (10:12:28Z), with the SHA-256 of the 19 files identified in Addendum no. 2. None of those 19 files was changed, except the launcher (below).

**2026 data-loading adapter.** Repository commit: `6f508ce01f50ddc92843ce8cdcff5f4cdd859afb`, of 25 October 2026, 11:17:36Z. The protocol of the test (commit `cec91d9128ac7001a466dac75f57eb011c5496b8`, 25 October 2026, 10:17:08Z) was fixed before any test and was not changed. It states that the adapter, applied to 2022 through the new path, must reproduce the outputs of the frozen code **byte for byte**. The report of the test gives the result.

**Code** (SHA-256 with LF line endings; commit `6f508ce01f`):

| File | SHA-256 (LF line endings) | Bytes |
|---|---|---:|
| `scripts/camada_c/ep_2026.py` | `f822e78341e11934df29f1c3414b61e77675cec0f46ea43e3f166b38bb3eab1e` | 8720 |
| `scripts/camada_c/ep_2026_relatorio.py` | `2be703bd2bf2f625fa50123ac5792facbabaac1bc6e853ee7ffc868828dd425d` | 14048 |
| `scripts/camada_c/rodar_estimador_presidencial.py` | `f038123f67fe8964f04572778d51d326ced4c9118a50d58bbf937e3b33c44ea8` | 31425 |

The launcher `rodar_estimador_presidencial.py` is the only one of the 19 frozen files that changed: it received the minimal hook `--carregador` and the lock on the year 2026. Its hash in the tag is `b8b8550f1eb59827ab9436b38debdd9189dd3cf72aee0198904839357ffc8145`, and the version in the tag remains available. The shared module `scripts/camada_c/dados.py` was not changed.

**Protocol, report and manifests of the test** (SHA-256 with LF line endings; commit `6f508ce01f`):

| File | SHA-256 (LF line endings) | Bytes |
|---|---|---:|
| `resultados/camada_c/estimador_presidencial/v3/PROTOCOLO_adaptador_2026_20261025.md` | `6db00199692052f658aa60dc8f78d22451d1b84a45adc2857d27323110c973cf` | 8296 |
| `resultados/camada_c/estimador_presidencial/v3/RELATORIO_adaptador_2026_20261025.md` | `937bf5c82d108b50e6e1afd154621ea7e9e5ab9056be6848363f218e4be2ea44` | 8151 |
| `resultados/camada_c/estimador_presidencial/v3/RELATORIO_adaptador_2026_20261025.en.md` | `c6e2ba64312edb83167b25e86a0a675aac412ca4cb743c352fef43ea7a898668` | 8531 |
| `resultados/camada_c/estimador_presidencial/v3/MANIFESTO_adaptador_2026.json` | `3d4b846ee79a4e0d48235b024e9ed2d2114ac2a1c5d9e9e707cba4aa4a389640` | 6272 |
| `resultados/camada_c/estimador_presidencial/v3/adaptador_2026_comparacao.csv` | `d8cd53709b692496db3051fcaa5b9a326eabd115dff7877cce2f3c455b5ac08b` | 21151 |
| `resultados/camada_c/estimador_presidencial/v3/adaptador_2026_esquema.json` | `04246c1ecc7fb51d8f8180f454d96caa66cd37254ec2f57d394eb379a015d97b` | 1624 |

**Authorisation lock.** The launcher accepts the year 2026 only with `--carregador ep2026`, with a written authorisation file and with the SHA-256 of that file recorded in `AUTORIZACAO_2026_hashes.json`. As of the date of this addendum that record **does not exist**, and the run on 2026 data **has not been authorised**. The lock is a procedural control; the proof that the rule was followed lies in the public hashes.

**What we commit to do.**

* Run the estimator on 2026 data only with the version identified in Addenda no. 2 and no. 3, unchanged, and only after a written authorisation by the coordinator, which will be recorded with the SHA-256 of the authorisation file.
* Use no 2026 data to change the model, the folds, the targets, the criteria, the thresholds or the flagging rule.
* Publish the text of the protocol and **all** the results of the estimator (versions 1, 2 and 3, the extra validation and 2026), whatever their direction, together with the results of the project, as the commitment states.
* State, in the publication, that the adapter was written and tested on 25 October 2026, between 10:17Z (protocol) and 11:17Z (delivery), before voting closed in the second round and before any result was released; that the test used only 2022 data and the schema of the 2026 tables; and that there is a single implementation (no independent reproduction).

**What this addendum does not do.** It does not change the status, the declared limits or the publication commitment. A statistical signal is an anomaly to be investigated, and it does not indicate the cause.

**Licence.** This text is under the CC BY-ND 4.0 licence, like the other texts and documents in the repository.
