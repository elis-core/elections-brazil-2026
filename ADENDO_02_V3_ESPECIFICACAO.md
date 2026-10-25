# Adendo nº 2 ao compromisso de publicação: prova de data da versão 3 do estimador do voto presidencial (texto, código e manifesto)

**Adendo ao compromisso de publicação de 24/10/2026.** O compromisso não é alterado. Este adendo complementa o Adendo nº 1, que registrou o SHA-256 do protocolo da versão 3. A versão 3 foi concluída com dados de 2014, 2018 e 2022 e nenhum dado de 2026. A data e a hora de publicação deste adendo são as do commit público e do upload na OSF.

**O que é.** Uma prova de data. Este adendo registra os SHA-256 do texto, do código e dos manifestos da versão 3 do estimador do voto presidencial. Os textos e **todos os resultados** da versão 3 e da validação extra serão publicados junto com os resultados do projeto, conforme o compromisso. Este adendo **não contém resultados, limiares nem listas de seções**.

**Protocolo (Adendo nº 1).** O protocolo da versão 3 foi fixado antes de qualquer cálculo dessa versão: commit `c35947ede6c6de9af552570f6faa0a12476bf3f9`, de 24/10/2026, 18:35:56Z. Nenhum critério ou limiar do protocolo foi alterado depois.

**Versão 3.** Commit do repositório: `6de775b3bbb0bdbc5744e09e7ac72424b3d22b97`, de 24/10/2026, 19:18:06Z. A versão 3 é posterior (**pós-hoc**) à versão 2 e à validação extra. Ela mantém o M1, as dobras, a estrutura do M2, os alvos A e B e os critérios C1 a C4. O relatório diz, item a item, o que foi adotado.

**Errata datada.** Em 24/10/2026, às 19:21:56Z, o commit `a3575714bedac13f5d9c5c3942ce86211543eccd` corrigiu, só no texto, uma linha do §13 do `docs/15c` (o hash de `scripts/camada_c/manifesto_ep.py`, que constava como o da versão 2). O código e os resultados não mudaram. Os hashes dos dois textos do `docs/15c` registrados no commit `6de775b3bb` (pt-BR `60bff166efcb85db04fb16bf2a18b5706d239428d3e9ec76d41f0b6f04602df8`; en-GB `e96fb4ae1587dc080ea58ce784c1c701df29d9f39c6955b723eea0248cdc95a3`) estão **superados** pelos da tabela abaixo.

**Texto, manifestos e relatório da versão 3** (SHA-256 com finais de linha LF; commit `a3575714be` para o texto e commit `6de775b3bb` para os demais):

| Arquivo | SHA-256 (finais de linha LF) | Bytes |
|---|---|---:|
| `docs/15c_estimador_voto_presidencial_adendo.md` (versão 3, com a errata) | `49a95d2dead5a3409383685d0a958772d236b52f0115aa0fa8d3a9f2bec2ecbf` | 49020 |
| `docs/15c_estimador_voto_presidencial_adendo.en.md` (versão 3, com a errata) | `a11f2bc0c27a5ed7be99e56ca2e705cf7c8071b99b7e7117695ad162f9c7883c` | 49328 |
| `resultados/camada_c/estimador_presidencial/MANIFESTO_especificacao_v3.json` | `c3886da9f25e0efbf9b77fc1e851cb2ff2801c511eee06302a211a69def50624` | 7050 |
| `resultados/camada_c/estimador_presidencial/v3/PROTOCOLO_v3_20261024.md` | `183adf9d33131239b9c754f021f6fbfa6bce18a2754227140407a668ff57421e` | 10515 |
| `resultados/camada_c/estimador_presidencial/v3/MANIFESTO_v3.json` (manifesto de execução) | `645c623c6a41712c7800971116f613bdfdeb184c83d8fa9570e15d6141e2a5f8` | 29923 |
| `resultados/camada_c/estimador_presidencial/v3/RELATORIO_validacao_v3_20261025.md` (relatório; ainda não publicado) | `0610101c79759a94bc7da79eeb06213210e03bdbe0abe5a22c7b359f2d0f1b05` | 36608 |
| `resultados/camada_c/estimador_presidencial/v3/RELATORIO_validacao_v3_20261025.en.md` (relatório; ainda não publicado) | `aeafd8a64ededfa465032f832dd9ea45314687328ceaca5bd1dc8ca0996265e6` | 37199 |

**Código da versão 3** (SHA-256 com finais de linha LF; commit `a3575714be`):

| Arquivo | SHA-256 (finais de linha LF) | Bytes |
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

**O que nos comprometemos a fazer.**

* Não usar dado de 2026 para mudar esta versão. Qualquer execução do estimador em 2026 depende de autorização separada do coordenador, depois de 25/10/2026, e usa a versão aqui identificada, sem alteração.
* Publicar o texto do protocolo, o relatório e **todos** os resultados da versão 3 e da validação extra, qualquer que seja a direção, junto com os resultados do projeto, conforme o compromisso.
* Declarar, na publicação, que a versão 3 é pós-hoc em relação à validação extra, que há uma única implementação (sem reprodução independente) e que as versões 1 e 2 continuam publicadas com os seus resultados.

**O que este adendo não faz.** Não altera o estatuto, os limites declarados nem o compromisso de publicação. Um sinal estatístico é uma anomalia a investigar, e não indica a causa.

**Licença.** Este texto está sob a licença CC BY-ND 4.0, como os demais textos e documentos do repositório.
