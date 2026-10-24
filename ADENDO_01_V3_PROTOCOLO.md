# Adendo nº 1 ao compromisso de publicação: prova de data do protocolo da versão 3 do estimador do voto presidencial

**Adendo ao compromisso de publicação de 24/10/2026.** O compromisso não é alterado. O protocolo da versão 3 do estimador foi fixado antes de qualquer cálculo dessa versão (ver o commit abaixo). Os cálculos da versão 3 já começaram no momento desta publicação, e nenhum resultado foi publicado. Este adendo é publicado antes do início da votação do 2º turno (25/10/2026); a data e a hora da publicação são as do commit público e do upload na OSF.

**O que é.** Uma prova de data. Este adendo registra o SHA-256 do protocolo da versão 3 do estimador do voto presidencial, fixado **antes de qualquer cálculo dessa versão**. O texto do protocolo **não** é publicado agora: será publicado junto com os resultados do projeto. Este adendo **não contém resultados, limiares nem listas de seções**.

**Contexto.** O estimador é um modelo exploratório, no nível da seção eleitoral, que calcula o valor esperado da composição do voto presidencial a partir dos demais cargos, com intervalo e resíduo por seção. A versão 1 e a versão 2 estão identificadas no compromisso. Depois delas, uma validação extra, com dados de 2014, 2018 e 2022, apontou limites do método. A versão 3 trata esses limites e é, por isso, **posterior** à versão 2 e à validação extra (**pós-hoc**).

**Validação extra (já concluída; relatório ainda não publicado).** Commit do repositório: `d9e5ec873fca1db05d9d5ab7b6500d7d3973a529` (24/10/2026, 17:57:02Z). SHA-256 (finais de linha LF):

| Arquivo | SHA-256 (finais de linha LF) |
|---|---|
| `resultados/camada_c/estimador_presidencial/validacao_extra/PROTOCOLO_20261024.md` | `d47e3ea61a76637001ea0810c7ae9ed3901d11a544be13872e63eea700347952` |
| `resultados/camada_c/estimador_presidencial/validacao_extra/RELATORIO_validacao_extra_20261024.md` | `c53799685c41576100f9be6cd4b61623752467e4002d5279e94dc77406017d9b` |
| `resultados/camada_c/estimador_presidencial/validacao_extra/RELATORIO_validacao_extra_20261024.en.md` | `71cc63b260de55373431e20519466cd8adf03eba5b0e1672fb5068e72fafed68` |

**Protocolo da versão 3.** Commit do repositório: `c35947ede6c6de9af552570f6faa0a12476bf3f9`, de **24/10/2026, 18:35:56Z** (15:35:56 em Brasília). O commit é posterior ao registro da decisão que autorizou a versão 3 (commit `7ba29a0c1d03852ba9c9d9f82b1b61ac21a92246`, 24/10/2026, 18:32:34Z) e anterior a qualquer cálculo da versão 3.

| Arquivo | SHA-256 (finais de linha LF) | Bytes |
|---|---|---:|
| `resultados/camada_c/estimador_presidencial/v3/PROTOCOLO_v3_20261024.md` | `183adf9d33131239b9c754f021f6fbfa6bce18a2754227140407a668ff57421e` | 10515 |

**O que nos comprometemos a fazer.**

* Uma única versão 3, sem novo ciclo de teste e ajuste depois dela.
* Usar só dados de 2014, 2018 e 2022. Nenhum dado de 2026 é usado para desenvolver, escolher o modelo ou fixar critério ou limiar.
* Não mudar nenhum critério ou limiar do protocolo depois de rodar. O que não cumprir os critérios do protocolo não é adotado, e a falha é relatada.
* Publicar o texto do protocolo e **todos** os resultados da versão 3 e da validação extra, qualquer que seja a direção, junto com os resultados do projeto, conforme o compromisso.
* Publicar, em um segundo adendo e até **25/10/2026, 18:00Z**, os SHA-256 do texto, do código e do manifesto da versão 3. Se a versão 3 não puder ser concluída nesse prazo, o segundo adendo diz isso, e valem a versão 2 e a validação extra como estão.

**O que este adendo não faz.** Não altera o estatuto, os limites declarados nem o compromisso de publicação. Um sinal estatístico é uma anomalia a investigar, e não indica a causa.

**Licença.** Este texto está sob a licença CC BY-ND 4.0, como os demais textos e documentos do repositório.
