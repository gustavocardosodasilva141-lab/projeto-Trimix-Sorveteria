# Auditoria do repositório — Trimix Sorveteria

Data da conferência: 11/11/2026. Fonte de comparação: instruções da atividade, Especificação de Requisitos v1.1, DER em PDF e script SQL fornecidos pelo grupo.

## Inventário conferido

- 19 tabelas no DDL.
- 113 colunas no DDL e no catálogo publicado; comparação de nomes por tabela sem divergências.
- 29 declarações de chave estrangeira.
- 30 triggers e 6 procedures no script SQL.
- O documento de requisitos v1.1 possui quatro entradas no histórico de revisões (0.1, 0.2, 1.0 e 1.1).

## Divergências entre Requisitos e DDL

1. **ON DELETE RESTRICT:** os requisitos exigem explicitamente ON DELETE RESTRICT para 100% das FKs. O DDL não declara cláusula ON DELETE em nenhuma das 29 FKs. O comportamento padrão do InnoDB é restritivo, mas isso não atende à exigência de declaração explícita no script.
2. **Collation:** os requisitos pedem utf8mb4_0900_ai_ci em todas as tabelas. As 19 tabelas do DDL usam utf8mb4_unicode_ci.
3. **CHECK:** os requisitos descrevem constraints CHECK para preços, quantidades, estoque, perfil e situação do caixa. O DDL não declara constraints CHECK. Alguns domínios podem estar sendo validados por ENUM ou triggers, mas isso não substitui as CHECK explicitamente previstas.
4. **Metadados do catálogo:** as 19 tabelas e 113 colunas coincidem nominalmente com o DDL. O catálogo agora exibe tipo, nulabilidade, default, auto incremento, chaves, índices únicos e relacionamentos extraídos do script. Regras de negócio completas ainda exigem validação contra o documento de requisitos.
5. **DER:** o DER foi enviado como PDF, mas a entrega exige exportação em PNG ou JPG e o arquivo final deve ser colocado como assets/der.png (ou der.jpg). A pasta assets do GitHub ainda não contém a imagem.
6. **Documento de requisitos:** o PDF fornecido é versão 1.1, com quatro revisões registradas. O professor solicita atualizar o histórico após aplicar as correções. É necessário registrar a nova revisão depois que o grupo decidir e aplicar as correções nos documentos originais.
7. **Governança RBAC:** a especificação define permissões por perfil. O DDL possui coluna perfil e procedures/triggers, mas não há comandos CREATE ROLE, GRANT ou REVOKE no script fornecido. Portanto, não afirmar que os privilégios do SGBD já foram provisionados.

## Situação do repositório frente à estrutura exigida

- [x] index.html
- [x] style.css
- [x] script.js
- [x] docs/ (pasta existente)
- [ ] docs/Especificacao_Requisitos_Regras_Negocio_BD.pdf — PDF revisado final não está no repositório
- [x] assets/ (pasta existente)
- [ ] assets/der.png ou assets/der.jpg — imagem final não está no repositório

Arquivos auxiliares existentes: data.json, README.md, .nojekyll e docs/revisao_tecnica.md. O DDL original também será mantido em docs/ddl_original.sql para rastreabilidade.

## Recursos web

- Busca em tempo real: implementada.
- Tema claro/escuro: implementado.
- Modal DER: interface e controles de zoom/pan implementados com Panzoom.js; depende do arquivo assets/der.png ou assets/der.jpg existir para exibir o diagrama.
- Tags LGPD/GDPR e RBAC: classificação inicial disponível; não equivale a certificação de conformidade ou provisionamento de permissões.

## Ações necessárias antes da entrega

1. Validar com o grupo as divergências ON DELETE, collation e CHECK e corrigir o DDL, requisitos e DER de forma consistente.
2. Atualizar o histórico de revisões do PDF (mantendo no mínimo quatro entradas; o v1.1 já tem quatro) e exportar o documento revisado.
3. Exportar o DER atualizado em PNG ou JPG e conferir os nomes exatos dos arquivos.
4. Adicionar os dois arquivos binários nas pastas exigidas.
5. Ativar GitHub Pages em Settings → Pages → Deploy from a branch → main → /(root) e verificar a URL pública.

## Limite desta auditoria

A auditoria verifica os artefatos fornecidos e o conteúdo atualmente publicado no repositório. Não executa o banco MySQL nem comprova testes funcionais de procedures, triggers, permissões ou consistência em tempo de execução.
