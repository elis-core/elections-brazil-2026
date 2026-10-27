# Adendo nº 4 ao compromisso de publicação: primeira execução do estimador em dados de 2026 bloqueada pela guarda de consistência do Senado; correção datada para as duas vagas de 2026

**Adendo ao compromisso de publicação de 24/10/2026.** O compromisso não é alterado. Este adendo complementa os Adendos nº 1, nº 2 e nº 3. A data e a hora de publicação deste adendo são as do commit público e do upload na OSF.

**O que é.** Uma prova de data **e uma declaração de desvio**. O Adendo nº 3 dizia que o estimador seria executado em dados de 2026 "apenas com a versão identificada nos Adendos nº 2 e nº 3, sem alteração". Este adendo registra que a primeira execução foi bloqueada por uma trava do código congelado, que **nenhum resultado de 2026 foi produzido** e que a trava foi corrigida, **só** quanto ao Senado de 2026, por mudança datada (seção 3), ainda não usada em nenhuma execução de 2026. Não contém resultados, limiares nem listas de seções.

## 1. O que aconteceu em 27/10/2026 (UTC)

* **09:19Z.** O coordenador autorizou por escrito a execução do **alvo A (1º turno de 2026)**. O alvo B (2º turno) continua condicionado à publicação e à conferência dos dados por seção do 2º turno e **não foi executado**.
* **09:58Z a 10:09Z.** Os dados por seção do 1º turno de 2026 (arquivos baixados do site do TSE em 07/10/2026) foram carregados no banco de análise e conferidos contra o detalhe e contra a totalização oficial do TSE do 1º turno. Os dados de 2014, 2018 e 2022 do banco não mudaram.
* **10:26:32Z a 10:27:33Z.** **Primeira execução do alvo A.** Nas 27 UFs, a guarda de consistência do código congelado recusou o cargo de senador, e as 27 UFs ficaram "não avaliáveis". Nenhuma saída por seção, métrica ou sinalização de 2026 foi gravada. **Exposição declarada:** durante essa execução o lançador imprimiu totais de votos por UF, e a razão entre os votos de senador e os de presidente (cerca de 2) foi observada; nenhum resultado do estimador existia. Houve duas chamadas anteriores sem leitura de dados de 2026 (uma recusada pelo monitor de recursos às 09:29Z e uma sem linhas de 2026 no banco às 09:34Z).
* **11:20Z.** O coordenador decidiu corrigir o fator do Senado de 2026.

## 2. A causa e a correção

Em 2026, como em 2018, cada UF elege **dois** senadores e cada eleitor dá **dois** votos para senador. O total de votos de senador é, portanto, cerca do **dobro** do de presidente. A guarda de consistência, escrita apenas para 2018, tolerava o dobro só nesse ano e tratou 2026 como dado suspeito. O número de vagas é um fato do calendário eleitoral, conhecido antes de qualquer dado de 2026.

**A correção (uma mudança de texto):** o `docs/15c` recebe um acréscimo datado ("Emenda datada (27/10/2026, D222)", no §2.4, junto à guarda que tolera "o dobro mais 5% no Senado de 2018", e no item 11.8), que estende o mesmo fator ao Senado de 2026, e o adaptador `ep_2026.py` aplica o fator 2 ao Senado de 2026. `desenhos_n3.py` e a tag `estimador-v3-congelamento-20261025` **não são alterados**. O fator para os demais cargos e para o Senado de 2014 e de 2022 (uma vaga) **não muda**. Método, dobras, alvos, critérios, limiares, parâmetros, validação cruzada e regra de sinalização **não mudam**.

**Natureza pós-hoc, declarada.** A necessidade da correção foi descoberta porque a guarda falhou em dado de 2026. O fator, porém, decorre do número de vagas, e a tolerância é a mesma de 2018. A frase obrigatória do relato de 2026 passa a ser: **"o fator do Senado de 2026 (duas vagas) foi corrigido depois de uma primeira tentativa recusada pela guarda; nenhum parâmetro foi ajustado por resultado"**. A primeira tentativa e todos os seus arquivos entram no relato.

## 3. Hashes (SHA-256 com finais de linha LF)

**Autorização do alvo A (27/10/2026) e estado do banco.**

| Arquivo | SHA-256 | Bytes |
|---|---|---:|
| `resultados/camada_c/estimador_presidencial/v3/AUTORIZACAO_2026_alvoA_20261027.md` | `77b6c2f0812b633a4b7a2c38316a490d32812f42cee9b7cb691cdc9a5696d063` | 5938 |
| `resultados/camada_c/estimador_presidencial/v3/AUTORIZACAO_2026_hashes.json` | `bdb885bcb648496fdd820508cd3524ff7ae128fe8ac60395ea235b222cf7399a` | 749 |
| Banco de análise `elis.duckdb` no momento da primeira execução (depois da carga do 1º turno) | `cd548b3ab25badf57ca686a2228d227083fc07dc7f34ceb47b1405d002e16eeb` | 1615605760 |

**Primeira execução recusada pela guarda e chamadas anteriores** (commit do repositório `3a17c035fb26038247fff3ed0f78eb0520cfaf6d`, 27/10/2026, 10:36:32Z; pasta `resultados/camada_c/estimador_presidencial/v3/2026/`):

| Arquivo | SHA-256 | Bytes |
|---|---|---:|
| `NOTA_tentativa_guarda_senado_20261027.md` | `831c347344f26e9fbc81a3cffed175b5ea1de97ec80782c798694a258e11e331` | 3954 |
| `MANIFESTO_tentativa_guarda_senado_T1026Z.json` | `f1189b4df289acae5b97654f4b793c4002e1931d4d289b7d4e08b825aa5414b5` | 8215 |
| `ufs_A_2026_tentativa_guarda_senado_T1026Z.json` | `8330c0de800af92a68d88ba4350fb1ab4e168ae05a542d9351fb74308b9727a9` | 7055 |
| `MONITOR_tentativa_guarda_senado_alvoA_20261027T1026Z.json` | `5d5e7030c42fbc48adf8282a222e1936f459507a7c345075bcf5ed0ebe4d5f07` | 1225 |
| `MONITOR_recusa_alvoA_20261027T0929Z.json` | `fb188e2d727c90b81afe3dcb3077a15e2f695cf3fed098b1ce3a745d072e1629` | 803 |
| `MANIFESTO_tentativa_sem_dados_T0933Z.json` | `53e96ed5122c65b6b75101fe137ee86fdda14b5744971cacfa93708d56c6a1b2` | 5099 |
| `ufs_A_2026_tentativa_sem_dados_T0933Z.json` | `4f53cda18c2baa0c0354bb5f9a3ecbe5ed12ab4d8e11ba873c2f11161202b945` | 2 |
| `MONITOR_tentativa_sem_dados_alvoA_20261027T0933Z.json` | `ebdc483b04cd09081f2469d7ae8a503687d43c898bae48e4504698620bb53bb5` | 1127 |

**Correção datada** (commits do repositório `cfc188616edad9c47a873ee97780dc4adf568685`, 2026-10-27T11:57:43Z, e `0c19af60e410d9ea69d367bf9c0e08880737f606`, 2026-10-27T12:34:31Z). A reprodução completa de 2022 pelo lançador com o adaptador emendado deu 108 de 108 arquivos por UF e 13 de 13 tabelas derivadas idênticos byte a byte; nenhum dado de 2026 foi lido nela.

| Arquivo | SHA-256 | Bytes | Commit |
|---|---|---:|---|
| `docs/15c_estimador_voto_presidencial_adendo.md` (acréscimo datado no §2.4 e item 11.8) | `a827b7bd07069c42fb18a9c965ab2425308e695f037b8f0f3f68cc266538bea4` | 52232 | `cfc188616e` |
| `docs/15c_estimador_voto_presidencial_adendo.en.md` (en-GB) | `8276553010ebb6dabe71c3d43f28e8a14e19d6cd821fa5abd5c15fb948b26d71` | 52499 | `cfc188616e` |
| `docs/versoes/15c_estimador_voto_presidencial_adendo_v3_pre-emenda-D222.md` (cópia anterior à emenda) | `49a95d2dead5a3409383685d0a958772d236b52f0115aa0fa8d3a9f2bec2ecbf` | 49020 | `cfc188616e` |
| `docs/versoes/15c_estimador_voto_presidencial_adendo_v3_pre-emenda-D222.en.md` (cópia anterior à emenda, en-GB) | `a11f2bc0c27a5ed7be99e56ca2e705cf7c8071b99b7e7117695ad162f9c7883c` | 49328 | `cfc188616e` |
| `scripts/camada_c/ep_2026.py` (fator 2 do Senado de 2026; versão anterior `f822e78341e11934df29f1c3414b61e77675cec0f46ea43e3f166b38bb3eab1e`) | `ead4797ac231d502fd859743dae7f021486d60b6ecfc4770eec9fe1a211a4b75` | 11630 | `cfc188616e` |
| `scripts/camada_c/test_ep_2026_senado.py` (teste sintético do fator) | `23aa303dea44e37b9f1e49012c63d277bdaa181bc4d22410110d33c0d10d6fc2` | 4525 | `cfc188616e` |
| `scripts/camada_c/ep_2026_teste_reproducao_montagem.py` | `bd722fb4216fc537cf9ef35774dd69251f0d2a4ed9d24ba2480eeda9336d0808` | 5320 | `cfc188616e` |
| `scripts/camada_c/ep_2026_teste_reproducao_2022_completa.py` (reprodução completa de 2022) | `7f0ab347276004527cbd599e2af61b12bfbfaa60310b55789b5cb6e4a127a5d1` | 3804 | `0c19af60e4` |
| `scripts/camada_c/ep_2026_manifesto_D222.py` | `5f6a81ecbdc17aa2a6a18ef8a192ab09b174a45b0b6cdb5c38b16e0786edeb8c` | 7701 | `0c19af60e4` |
| `resultados/camada_c/estimador_presidencial/v3/DIFF_ep_2026_D222_20261027.patch` | `c81d9980bddc3908df9a3ad8a72bd31dc76e5c42e7dcf1495821d0f9666fa450` | 4451 | `cfc188616e` |
| `resultados/camada_c/estimador_presidencial/v3/MANIFESTO_adaptador_2026_D222.json` (inclui o resultado da reprodução completa de 2022) | `a1ae9287d621b91b3d4ab06524380eba5d9976c45f47935e96fce211c7935332` | 11491 | `0c19af60e4` |
| `resultados/camada_c/estimador_presidencial/v3/REPRODUCAO_montagem_D222_20261027.csv` (2014, 2018 e 2022: 162 unidades, 1458 componentes) | `7879a273cf6e1c6915147de20d2dd83154e2679ccb0c1f04c9eb43afce44a242` | 221031 | `cfc188616e` |
| `resultados/camada_c/estimador_presidencial/v3/REPRODUCAO_montagem_D222_20261027.json` | `d0acdbb884f9d3208d4c113fa1e68d5345f3e6dd5b9a00a192bd42b8f68d1166` | 904 | `cfc188616e` |
| `resultados/camada_c/estimador_presidencial/v3/REPRODUCAO_2022_completa_D222_20261027.csv` (108 arquivos por UF e 13 tabelas derivadas, todos idênticos) | `c583f090e6ec4a6cb3452010923e05d30b076cadf912e7bdc3d2b18615e5d3ca` | 28312 | `0c19af60e4` |
| `resultados/camada_c/estimador_presidencial/v3/REPRODUCAO_2022_completa_D222_20261027.json` | `4ffde8c6a0d647c7c3c55976d2c8df3f006971ad60355ed41f02f938eb9f5adc` | 766 | `0c19af60e4` |
| `resultados/camada_c/estimador_presidencial/v3/AUTORIZACAO_2026_alvoA_D222_20261027.md` (substitui a autorização `77b6c2f0…d063`) | `0555d89bf0d4bf427448b3bc41f2a175ad8bdd0e6e6dbff78d002d9f0ec97c6c` | 4969 | `cfc188616e` |
| `resultados/camada_c/estimador_presidencial/v3/AUTORIZACAO_2026_hashes.json` | `fb8140a46109ea5431a63a0418fa4bca59cdac9232d056ca747a16c0046219c4` | 1323 | `cfc188616e` |

O lançador `rodar_estimador_presidencial.py` (`f038123f67fe8964f04572778d51d326ced4c9118a50d58bbf937e3b33c44ea8`, Adendo nº 3) e o módulo `desenhos_n3.py` **não** mudam (conferido no commit acima).

## 4. O que nos comprometemos a fazer

* **Reexecutar o alvo A em 2026 somente depois** da publicação deste adendo com os hashes da correção, do teste de reprodução (idêntico byte a byte em 2014, 2018 e 2022) e da nova autorização escrita, e com a conferência independente de duas sessões do projeto.
* Executar com **nenhuma outra alteração** além do fator do Senado de 2026.
* Publicar **todos** os resultados do estimador, qualquer que seja a direção, **inclusive o registro da tentativa bloqueada**, com a frase de rótulo acima.
* Não executar o alvo B enquanto os dados por seção do 2º turno não estiverem publicados pelo portal oficial, carregados e conferidos.
* Se, na reexecução, outra etapa falhar, **relatar e não contornar**; a decisão é do coordenador e, havendo mudança, ela entra em novo adendo datado.
* Declarar na publicação que há uma única implementação (sem reprodução independente) e que o estimador foi escrito e congelado antes de qualquer dado de 2026, com as duas exceções descritas nos Adendos nº 3 e nº 4.

**O que este adendo não faz.** Não altera o estatuto, os limites declarados nem o compromisso de publicação. Não contém resultados de 2026. Um sinal estatístico é uma anomalia a investigar, e não indica a causa.

**Licença.** Este texto está sob a licença CC BY-ND 4.0, como os demais textos e documentos do repositório.
