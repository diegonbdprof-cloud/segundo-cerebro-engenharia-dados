# Notas de trabalho: segundo cérebro em Engenharia de Dados

## Estado em 07/11/2026

- Notebook real: "Fundamentos de Engenharia de Dados: Python, SQL e ETL", com 6 fontes externas (IBM, AWS, documentação Python csv, PostgreSQL 2.4, PostgreSQL COPY e o vídeo IBM Technology) e uma nota de objetivo do usuário. A nota de objetivo não é fonte independente.
- Link: https://notebook.google.com/notebook/40659bdb-f98b-4c16-b472-d093f14ed343
- Perguntas feitas no chat: 4. Três são perguntas técnicas (ETL/ELT, `DictReader`/`newline=''`, INSERT versus COPY) e a quarta é uma revisão crítica das imprecisões da segunda e da terceira. O arquivo [perguntas.txt](perguntas.txt) tem 5 perguntas planejadas. Essa lista não foi executada por completo.
- As fontes de texto foram lidas. A transcrição do vídeo foi importada e revista no notebook. O vídeo não foi assistido de forma independente e completa. Não houve Deep Research. A interface capturada está em "Investigação rápida".
- Materiais do Estúdio: mapa mental em PNG e guia de estudo em PDF de 11 páginas, exportado via Google Docs. O Docs permaneceu privado. O PDF e o mapa publicados nesta pasta de materiais abrem sem conta do Notebook.

## Acesso ao notebook

Abrir o notebook exige login do Google. Ele não é acessível de forma anônima.

- No Chrome anônimo, o link compartilhado redirecionou para o login do Google Accounts. Nenhum conteúdo do notebook ficou visível. Não houve tentativa de login nem de contorno.
- No diálogo de compartilhamento da sessão já autenticada do proprietário, a configuração foi reconfirmada: qualquer pessoa com o link pode ver, sem edição, com "Permitir cópias" desmarcado e sem convites.
- Não foi testado o acesso com outra conta Google autenticada. A checagem cobre a barreira anônima de login e a configuração de compartilhamento do proprietário.
- Uma nota anterior deste mesmo dia ainda dizia que o acesso externo não tinha sido testado. Essa formulação foi substituída pelo resultado acima.

## Avaliação crítica das respostas e dos materiais

- Pergunta 1: as citações [1], [9] e [16] foram conferidas no painel. As outras não foram abertas uma a uma. O exemplo está marcado como hipotético.
- Pergunta 2: [1] e [4] foram conferidas. Imprecisão preservada no texto original: a resposta diz que se "exige" `newline=''`. A documentação recomenda ("deverá ser aberto com", "é sempre seguro"). `newline=''` orienta o tratamento de quebras de linha do módulo `csv`. Não é exigência sintática para `open()` funcionar.
- Pergunta 3: [3], [5] a [7], [12], [14] e [15] foram conferidas. [8] a [11] e [13] não foram abertas. Imprecisões preservadas: "significativamente mais rápido", enquanto a fonte diz "usually faster" (geralmente mais rápido); e "usuário postgres", enquanto a fonte diz "the user ID the server runs as". O nome da conta do sistema operacional não precisa ser `postgres`.
- Pergunta 4, a correção: confirma "usually faster" em [1], o usuário do sistema como ID do servidor em [2] e [3], e separa `newline=''` de uma restrição de `open()` em [4] e [5]. Essas citações foram conferidas no painel. O comentário do exemplo ainda diz "boa prática exigida", e o corpo ainda fala em "exigência operacional". A leitura que fica de pé é a recomendação do módulo `csv`.
- Guia de estudo, PDF não editado: a seção "A Exigência Operacional de newline=''" diz que "é imperativo declarar" o argumento e trata o ponto como exigência. Várias citações apontam para "Nota Salva: ...", que são notas do próprio notebook, não documentos de origem. O PDF não deve ser lido como autoridade técnica independente. As falhas foram mantidas de propósito.
- Mapa mental: quatro ramos (fluxo ETL/ELT, CSV com Python, transformação e qualidade, carga no PostgreSQL). Está legível e não tem citações próprias. As fontes estão ligadas no README.

## Conferência dos arquivos

- As 13 capturas e o mapa foram inspecionados. As 11 páginas do PDF foram lidas por texto extraído. A contagem ficou entre 74 e 490 palavras por página, nenhuma página em branco, e a última página termina no glossário. Privacidade das capturas: não há e-mail, telefone nem nome completo visível; só o avatar com a inicial "D".
- Limites: a leitura do PDF foi do texto, não uma revisão linha a linha do layout. A captura do guia mostra, no chat, um prompt automático do Estúdio, não as perguntas 1 a 4.
- Os hashes SHA-256 das capturas, do mapa e do PDF conferem com a tabela em [evidencias/MANIFESTO.md](../evidencias/MANIFESTO.md).
