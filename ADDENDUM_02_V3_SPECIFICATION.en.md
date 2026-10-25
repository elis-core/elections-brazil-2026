# Addendum no. 2 to the publication commitment: proof of date of version 3 of the presidential-vote estimator (text, code and manifest)

> **British English version (D31).** This file translates `ADENDO_02_V3_ESPECIFICACAO.md` (Brazilian Portuguese), **SHA-256 of the pt-BR text, with LF line endings: `32a51975e0e2646ac8acfcbfcced274a4a6c08863a16b240c163c6ed85638b35`**. The pt-BR version is the reference and prevails in case of divergence.

---

**Addendum to the publication commitment of 24 October 2026.** The commitment is not changed. This addendum complements Addendum no. 1, which recorded the SHA-256 of the protocol for version 3. Version 3 was completed with data from 2014, 2018 and 2022 and no 2026 data. The date and time of publication of this addendum are those of the public commit and of the upload to the OSF.

**What it is.** A proof of date. This addendum records the SHA-256 of the text, the code and the manifests of version 3 of the presidential-vote estimator. The texts and **all the results** of version 3 and of the extra validation will be published together with the results of the project, as the commitment states. This addendum **contains no results, thresholds or lists of sections**.

**Protocol (Addendum no. 1).** The protocol for version 3 was fixed before any calculation of that version: commit `c35947ede6c6de9af552570f6faa0a12476bf3f9`, of 24 October 2026, 18:35:56Z. No criterion or threshold of the protocol was changed afterwards.

**Version 3.** Repository commit: `6de775b3bbb0bdbc5744e09e7ac72424b3d22b97`, of 24 October 2026, 19:18:06Z. Version 3 is later (**post hoc**) than version 2 and the extra validation. It keeps M1, the folds, the structure of M2, targets A and B and criteria C1 to C4. The report says, item by item, what was adopted.

**Dated erratum.** On 24 October 2026, at 19:21:56Z, commit `a3575714bedac13f5d9c5c3942ce86211543eccd` corrected, in the text only, one line of §13 of `docs/15c` (the hash of `scripts/camada_c/manifesto_ep.py`, which was given as that of version 2). The code and the results did not change. The hashes of the two texts of `docs/15c` recorded in commit `6de775b3bb` (pt-BR `60bff166efcb85db04fb16bf2a18b5706d239428d3e9ec76d41f0b6f04602df8`; en-GB `e96fb4ae1587dc080ea58ce784c1c701df29d9f39c6955b723eea0248cdc95a3`) are **superseded** by those in the table below.

**Text, manifests and report of version 3** (SHA-256 with LF line endings; commit `a3575714be` for the text and commit `6de775b3bb` for the others):

| File | SHA-256 (LF line endings) | Bytes |
|---|---|---:|
| `docs/15c_estimador_voto_presidencial_adendo.md` (version 3, with the erratum) | `49a95d2dead5a3409383685d0a958772d236b52f0115aa0fa8d3a9f2bec2ecbf` | 49020 |
| `docs/15c_estimador_voto_presidencial_adendo.en.md` (version 3, with the erratum) | `a11f2bc0c27a5ed7be99e56ca2e705cf7c8071b99b7e7117695ad162f9c7883c` | 49328 |
| `resultados/camada_c/estimador_presidencial/MANIFESTO_especificacao_v3.json` | `c3886da9f25e0efbf9b77fc1e851cb2ff2801c511eee06302a211a69def50624` | 7050 |
| `resultados/camada_c/estimador_presidencial/v3/PROTOCOLO_v3_20261024.md` | `183adf9d33131239b9c754f021f6fbfa6bce18a2754227140407a668ff57421e` | 10515 |
| `resultados/camada_c/estimador_presidencial/v3/MANIFESTO_v3.json` (execution manifest) | `645c623c6a41712c7800971116f613bdfdeb184c83d8fa9570e15d6141e2a5f8` | 29923 |
| `resultados/camada_c/estimador_presidencial/v3/RELATORIO_validacao_v3_20261025.md` (report; not yet published) | `0610101c79759a94bc7da79eeb06213210e03bdbe0abe5a22c7b359f2d0f1b05` | 36608 |
| `resultados/camada_c/estimador_presidencial/v3/RELATORIO_validacao_v3_20261025.en.md` (report; not yet published) | `aeafd8a64ededfa465032f832dd9ea45314687328ceaca5bd1dc8ca0996265e6` | 37199 |

**Code of version 3** (SHA-256 with LF line endings; commit `a3575714be`):

| File | SHA-256 (LF line endings) | Bytes |
|---|---|---:|
| `scripts/camada_c/ep_concorrentes.py` | `be64c009d55e8d1cc32feb84d6dfcd20dc608f83c5aedf5291ae3d79259eb81c` | 5528 |
| `scripts/camada_c/ep_dados.py` | `724edc38972c1e070ede0971c1c1e5e2c89620b1151f5608030956a166b35418` | 9551 |
| `scripts/camada_c/ep_metricas.py` | `be893da9a42cad675a5ce6d900ddb13b240e56bcf121a5e3f3302ab35e6ca2f4` | 6759 |
| `scripts/camada_c/ep_modelo.py` | `edd7ee8f68791453ba05743817ac0cc85d0af1c513416402d7e30e2c712f0161` | 11106 |
| `scripts/camada_c/ep_poder.py` | `6818ce4c22e67513f0df05e7c815622cf5b54f113af04308ebd3b87de07a725d` | 6348 |
| `scripts/camada_c/ep_v3.py` | `ae69d17163f3c2f86d16c0010b58a46b521ba31f63d7123a7f5737b0fb588e46` | 4416 |
| `scripts/camada_c/ep_v3_sinalizacao.py` | `8599b51493d6bb4ae96231f1dd6ed4b19bd70c9f9662622bac29a59e0b51cb5a` | 22525 |
| `scripts/camada_c/ep_v3_relatorio.py` | `25796b51068bb22259509d837b86cc2cb62bb19f491d8d2b09712e1391713b1f` | 16182 |
| `scripts/camada_c/manifesto_ep.py` | `49838804153789d7c68f83aba423ff1b926f6226d6dc3637be087598b7466231` | 5680 |
| `scripts/camada_c/relatorio_ep.py` | `3eb9290ea019ad27136587e0c9b801d6492416ee834a5e294f9414392dbe67a1` | 20473 |
| `scripts/camada_c/rodar_estimador_presidencial.py` | `b8b8550f1eb59827ab9436b38debdd9189dd3cf72aee0198904839357ffc8145` | 29990 |
| `scripts/camada_c/test_estimador_presidencial.py` | `4a6c6ec79a364579db09f116956cc86b8120769cbf35f164cbc97694961bb087` | 9126 |

**What we commit to do.**

* Use no 2026 data to change this version. Any run of the estimator on 2026 data depends on a separate authorisation by the coordinator, after 25 October 2026, and uses the version identified here, unchanged.
* Publish the text of the protocol, the report and **all** the results of version 3 and of the extra validation, whatever their direction, together with the results of the project, as the commitment states.
* State, in the publication, that version 3 is post hoc with respect to the extra validation, that there is a single implementation (no independent reproduction) and that versions 1 and 2 remain published with their results.

**What this addendum does not do.** It does not change the status, the declared limits or the publication commitment. A statistical signal is an anomaly to be investigated, and it does not indicate the cause.

**Licence.** This text is under the CC BY-ND 4.0 licence, like the other texts and documents in the repository.
