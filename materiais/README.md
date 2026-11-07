# Materiais gerados no Gemini Notebook

Notebook: Fundamentos de Engenharia de Dados: Python, SQL e ETL

Estes dois arquivos são as exportações originais, sem edição posterior. O guia em PDF é saída de IA não editada. Ele precisa de revisão crítica e não é autoridade técnica verificada de forma independente.

## Mapa mental

Título do artefato: “Mapa mental — Fundamentos de Engenharia de Dados (Python, SQL e ETL)”. Exportado pela opção “Download mindmap as image”, com a árvore expandida (ETL/ELT, CSV com `DictReader` e `newline=''`, qualidade, INSERT/COPY e cuidados de arquivo e permissão).

[mapa-mental-fundamentos-engenharia-de-dados.png](mapa-mental-fundamentos-engenharia-de-dados.png)

O mapa não traz citações próprias. As fontes do notebook estão no [README](../README.md#fontes) e em [docs/fontes.md](../docs/fontes.md).

## Guia de estudo

Título do artefato: “Guia de Estudo: Fundamentos de Engenharia de Dados (ETL, ELT, CSV em Python e Carga no PostgreSQL)”. Exportado para o Google Docs pela opção do artefato e transferido como PDF pela interface do Docs. São 11 páginas. O Google Docs exportado ficou privado e não foi compartilhado à parte. O arquivo que abre sem conta do Notebook é o PDF abaixo.

[guia-estudo-fundamentos-engenharia-dados.pdf](guia-estudo-fundamentos-engenharia-dados.pdf)

O guia contém objetivos, resumo de ETL/ELT, CSV em Python, transformação e qualidade, INSERT/COPY no PostgreSQL, cuidados de CSV e localização, erros comuns, 10 perguntas curtas com gabarito separado, cinco perguntas abertas e glossário.

### Leitura crítica do PDF, que permanece sem edição

- Sobre `newline=''`, a seção se chama “A Exigência Operacional de newline=''”. O texto diz que, ao abrir o arquivo com `open()`, “é imperativo declarar o argumento newline=''”, e chama as razões de “esta exigência”. A documentação do módulo `csv`, conferida na pergunta 4, recomenda `newline=''` para o tratamento de quebras de linha do próprio módulo. Isso não é exigência sintática para `open()` funcionar. A resposta corretiva está preservada em [docs/respostas-reais.md](../docs/respostas-reais.md).
- O PDF formula o desempenho do COPY como “geralmente/habitualmente mais rápido” (`usually faster`). Essa formulação está alinhada ao painel da documentação. A resposta original da pergunta 3, anterior ao guia, tinha escrito “significativamente mais rápido”.
- Sobre a conta do sistema, o PDF fala na conta ou no ID sob o qual o servidor executa e ainda associa esse papel, em geral, ao usuário `postgres` (“frequentemente associado” no corpo; “geralmente associada” no gabarito). O nome da conta não precisa ser `postgres`.
- Há dezenas de citações “Nota Salva: …”, entre elas “Nota Salva: Pipelines de Dados”, “Nota Salva: Manipulação CSV Python” e “Nota Salva: Carga no PostgreSQL”. São notas salvas no próprio notebook, não as seis fontes externas.

## Compartilhamento do notebook

No diálogo de compartilhamento da sessão do proprietário, o notebook ficou como “qualquer pessoa com o link pode ver”, sem permissão de edição, com “Permitir cópias” desmarcado e sem pessoas convidadas. Abrir o link exige login do Google. No Chrome anônimo a página foi para o login do Google Accounts e nenhum conteúdo do notebook ficou visível. Não houve tentativa de entrar na conta nem de contornar a tela, e o acesso com outra conta Google já autenticada não foi testado. As capturas, o PDF e o mapa deste repositório podem ser lidos sem conta do Notebook.
