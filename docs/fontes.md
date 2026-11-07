# Objetivo
Entender, como iniciante em transição para engenheiro de dados júnior, como extrair, transformar e carregar dados (ETL), validar CSV com Python e usar SQL básico (PostgreSQL).

# Fontes (lidas e verificadas em 06/11/2026; todas HTTP 200)

1. "O que é ETL (extrair, transformar, carregar)?" | Alice Gomstyn e Amanda McGrath, IBM Think | https://www.ibm.com/br-pt/think/topics/etl | PT-BR
   - Seções observadas: "ETL definido", "ETL versus ELT" (tabela com ordem das etapas, tipo e volume de dados, velocidade, custos, manutenção e privacidade/PII), "Como funciona o ETL" (Extrair: fontes como bancos relacionais/NoSQL, CRM/ERP, APIs, JSON/XML; Transformar: limpeza, deduplicação, validação, auditoria, formatação para o esquema de destino; Carregar), "ETL tradicional versus de streaming", CDC, zero-ETL, ETLT/ETL reverso/TETL, benefícios, desafios (incluindo gerenciamento de esquemas: colunas renomeadas ou tipos alterados quebram pipelines) e FAQ (área de preparação; cargas inicial, incremental e completa).
   - Confiança: artigo institucional assinado de um fornecedor consolidado de dados. Tem viés comercial nos links finais de produtos IBM.

2. "O que é ETL (extrair, transformar e carregar)?" | AWS (sem autor nomeado) | https://aws.amazon.com/pt/what-is/etl/ | PT
   - Seções observadas: importância e benefícios para BI, evolução (ETL tradicional e moderno, data warehouse e data lake), extração (área de preparação; notificação de atualização, extração gradual, extração completa), transformação básica (limpeza, ex.: campo vazio → 0; deduplicação; revisão de formato) e avançada (derivação, junção, separação, resumo, encriptação), carregamento completo vs incremental (por transmissão ou em lotes), ETL vs ELT, virtualização de dados. As seções finais promovem o AWS Glue e o Marketplace.
   - Confiança: página oficial de um provedor de nuvem e segunda visão para comparar com a IBM. Tem viés comercial nas seções de produto.

3. "csv — Leitura e escrita de arquivos CSV" | Python Software Foundation, documentação do Python 3 (página mostra 3.15.2) | https://docs.python.org/pt-br/3/library/csv.html | PT-BR
   - Trechos observados: csv.reader (um objeto arquivo "deverá ser aberto com newline=''"); csv.DictReader(f, fieldnames=None, restkey=None, restval=None, dialect='excel', ...) mapeia cada linha para dict; Dialect.strict ("Quando True, levanta a exceção Error em uma entrada CSV ruim. O padrão é False"); csv.Sniffer (sniff deduz o dialeto de uma amostra); dialetos e list_dialects/get_dialect.
   - Confiança: documentação oficial (fonte primária). Observação: a página documenta a leitura e o parsing, não regras de validação de negócio (tipos, campos obrigatórios); essas regras não estão nela.

4. "2.4. Populating a Table With Rows" | PostgreSQL Global Development Group, documentação 18 | https://www.postgresql.org/docs/current/tutorial-populate.html | EN
   - Trechos observados: INSERT INTO weather ... (listar as colunas explicitamente é "better style"); alternativa COPY para grandes volumes de arquivos de texto, "usually faster ... while allowing less flexibility than INSERT"; exemplo COPY weather FROM '/home/user/weather.txt'; o arquivo precisa estar na máquina do servidor (backend), não do cliente.
   - Confiança: documentação oficial.

5. "COPY" (página de referência SQL) | PostgreSQL Global Development Group, documentação 18 | https://www.postgresql.org/docs/current/sql-copy.html | EN
   - Trechos observados: "COPY moves data between PostgreSQL tables and standard file-system files"; COPY FROM anexa os dados à tabela, e colunas fora da lista recebem valores padrão; o arquivo precisa ser acessível pelo usuário do servidor; seção "CSV Format"; opções HEADER [boolean | MATCH], DELIMITER, QUOTE, ENCODING, ON_ERROR, REJECT_LIMIT.
   - Confiança: referência oficial (primária) para COPY.

6. Vídeo "What is ETL (Extract, Transform, Load)?" | IBM Technology (canal oficial do YouTube) | https://www.youtube.com/watch?v=OW5OgsLpDCQ | EN | cerca de 4min51s
   - Legendas: os metadados públicos da página do vídeo listam faixas de legenda em inglês (en / en-US) e uma faixa automática (asr). O texto da transcrição não foi lido, então o conteúdo exato do vídeo NÃO foi verificado; confirmar depois de importar no notebook. Título e canal confirmados via oEmbed.
   - Confiança: canal oficial da IBM; é a fonte em formato de vídeo.

# Cobertura de SQL
As fontes 4 e 5 cobrem a criação e a carga. Para consultas básicas, uma opção a acrescentar é "2.5. Querying a Table" (https://www.postgresql.org/docs/current/tutorial-select.html, verificada: SELECT, AS, WHERE com AND/OR/NOT). Essa página não foi adicionada ao notebook. As seis fontes externas continuam sendo as listadas acima.

# Atualização posterior à importação do vídeo

O item 6, acima, registra o estado de 06/11/2026, quando a transcrição ainda não tinha sido lida. Depois da importação, a transcrição foi revista dentro do notebook e confirmada como relevante para o tema. O vídeo não foi assistido de forma independente e completa. O texto integral da transcrição não é republicado neste repositório. Não houve uso de Deep Research.
