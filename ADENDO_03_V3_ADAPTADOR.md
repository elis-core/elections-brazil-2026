# Adendo nº 3 ao compromisso de publicação: prova de data do adaptador de carga de 2026 do estimador do voto presidencial (código, protocolo e relatório do teste de reprodução)

**Adendo ao compromisso de publicação de 24/10/2026.** O compromisso não é alterado. Este adendo complementa os Adendos nº 1 e nº 2 e foi preparado antes de qualquer execução do estimador em dados de 2026. A data e a hora de publicação deste adendo são as do commit público e do upload na OSF.

**O que é.** Uma prova de data. Este adendo registra os SHA-256 do código do adaptador de carga de 2026, do protocolo do seu teste e do relatório do teste de reprodução em 2022. O adaptador **só carrega dados**: não muda o modelo, as dobras, os alvos, os critérios, os limiares nem a regra de sinalização da versão 3. Este adendo **não contém resultados, limiares nem listas de seções**.

**Congelamento da versão 3 (não publicado antes).** Tag anotada `estimador-v3-congelamento-20261025` (objeto `5b162d96aa15df55fed6a9e826c794211ea3156f`), criada em 25/10/2026, 10:09:45Z, sobre o commit `a3575714bedac13f5d9c5c3942ce86211543eccd`. Manifesto de congelamento `MANIFESTO_congelamento_v3.json`, SHA-256 `f68d1b32c87eca713936805dfa700827aa9bd0cdb9c91f5a064d24db65cffc1c`, commit `f17840f2fc0ce059bb34185bdb211864c85e7735` (10:12:28Z), com o SHA-256 dos 19 arquivos identificados no Adendo nº 2. Nenhum desses 19 arquivos foi alterado, exceto o lançador (abaixo).

**Adaptador de carga de 2026.** Commit do repositório: `6f508ce01f50ddc92843ce8cdcff5f4cdd859afb`, de 25/10/2026, 11:17:36Z. O protocolo do teste (commit `cec91d9128ac7001a466dac75f57eb011c5496b8`, 25/10/2026, 10:17:08Z) foi fixado antes de qualquer teste e não foi alterado. Ele estabelece que o adaptador, aplicado a 2022 pelo caminho novo, deve reproduzir as saídas do código congelado **byte a byte**. O relatório do teste informa o resultado.

**Código** (SHA-256 com finais de linha LF; commit `6f508ce01f`):

| Arquivo | SHA-256 (finais de linha LF) | Bytes |
|---|---|---:|
| `scripts/camada_c/ep_2026.py` | `f822e78341e11934df29f1c3414b61e77675cec0f46ea43e3f166b38bb3eab1e` | 8720 |
| `scripts/camada_c/ep_2026_relatorio.py` | `2be703bd2bf2f625fa50123ac5792facbabaac1bc6e853ee7ffc868828dd425d` | 14048 |
| `scripts/camada_c/rodar_estimador_presidencial.py` | `f038123f67fe8964f04572778d51d326ced4c9118a50d58bbf937e3b33c44ea8` | 31425 |

O lançador `rodar_estimador_presidencial.py` é o único dos 19 arquivos congelados que mudou: recebeu o gancho mínimo `--carregador` e a trava do ano 2026. O hash dele na tag é `b8b8550f1eb59827ab9436b38debdd9189dd3cf72aee0198904839357ffc8145`, e a versão da tag continua disponível. O módulo compartilhado `scripts/camada_c/dados.py` não foi alterado.

**Protocolo, relatório e manifestos do teste** (SHA-256 com finais de linha LF; commit `6f508ce01f`):

| Arquivo | SHA-256 (finais de linha LF) | Bytes |
|---|---|---:|
| `resultados/camada_c/estimador_presidencial/v3/PROTOCOLO_adaptador_2026_20261025.md` | `6db00199692052f658aa60dc8f78d22451d1b84a45adc2857d27323110c973cf` | 8296 |
| `resultados/camada_c/estimador_presidencial/v3/RELATORIO_adaptador_2026_20261025.md` | `937bf5c82d108b50e6e1afd154621ea7e9e5ab9056be6848363f218e4be2ea44` | 8151 |
| `resultados/camada_c/estimador_presidencial/v3/RELATORIO_adaptador_2026_20261025.en.md` | `c6e2ba64312edb83167b25e86a0a675aac412ca4cb743c352fef43ea7a898668` | 8531 |
| `resultados/camada_c/estimador_presidencial/v3/MANIFESTO_adaptador_2026.json` | `3d4b846ee79a4e0d48235b024e9ed2d2114ac2a1c5d9e9e707cba4aa4a389640` | 6272 |
| `resultados/camada_c/estimador_presidencial/v3/adaptador_2026_comparacao.csv` | `d8cd53709b692496db3051fcaa5b9a326eabd115dff7877cce2f3c455b5ac08b` | 21151 |
| `resultados/camada_c/estimador_presidencial/v3/adaptador_2026_esquema.json` | `04246c1ecc7fb51d8f8180f454d96caa66cd37254ec2f57d394eb379a015d97b` | 1624 |

**Trava de autorização.** O lançador só aceita o ano 2026 com `--carregador ep2026`, com um arquivo de autorização escrita e com o SHA-256 desse arquivo registrado em `AUTORIZACAO_2026_hashes.json`. Até a data deste adendo esse registro **não existe**, e a execução em 2026 **não foi autorizada**. A trava é um controle de procedimento; a prova de que a regra foi seguida está nos hashes públicos.

**O que nos comprometemos a fazer.**

* Executar o estimador em dados de 2026 apenas com a versão identificada nos Adendos nº 2 e nº 3, sem alteração, e somente depois de autorização escrita do coordenador, que será registrada com o SHA-256 do arquivo de autorização.
* Não usar dado de 2026 para mudar o modelo, as dobras, os alvos, os critérios, os limiares ou a regra de sinalização.
* Publicar o texto do protocolo e **todos** os resultados do estimador (versões 1, 2 e 3, validação extra e 2026), qualquer que seja a direção, junto com os resultados do projeto, conforme o compromisso.
* Declarar, na publicação, que o adaptador foi escrito e testado em 25/10/2026, entre 10:17Z (protocolo) e 11:17Z (entrega), antes do encerramento da votação do 2º turno e da divulgação de qualquer resultado; que o teste usou só dados de 2022 e o esquema das tabelas de 2026; e que há uma única implementação (sem reprodução independente).

**O que este adendo não faz.** Não altera o estatuto, os limites declarados nem o compromisso de publicação. Um sinal estatístico é uma anomalia a investigar, e não indica a causa.

**Licença.** Este texto está sob a licença CC BY-ND 4.0, como os demais textos e documentos do repositório.
