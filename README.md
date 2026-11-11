# Trimix Sorveteria — Dicionário de Dados

Documentação web do banco de dados do Sistema de Gestão Operacional e Vendas da Trimix Sorveteria.

## Estrutura publicada
- `index.html`: página principal.
- `style.css`: estilos responsivos e tema claro/escuro.
- `script.js`: busca dinâmica e renderização do catálogo.
- `data.json`: metadados das 19 tabelas e 113 colunas extraídos do DDL.
- `docs/revisao_tecnica.md`: pontos de coerência que precisam de validação pelo grupo.

## Publicar no GitHub Pages
1. Abra **Settings → Pages**.
2. Em **Build and deployment**, escolha **Deploy from a branch**.
3. Selecione **main** e **/(root)** e salve.
4. Aguarde o GitHub concluir a publicação.

URL esperada: https://gustavocardosodasilva141-lab.github.io/projeto-Trimix-Sorveteria/

## Pendências documentais
Os arquivos binários originais/revisados (PDF da especificação e imagem DER) ainda precisam ser enviados para:
- `docs/Especificacao_Requisitos_Regras_Negocio_BD.pdf`
- `assets/der.png`

O DDL original também deve ser anexado em `docs/ddl_original.sql` para manter a trilha de auditoria da documentação. Não considere a entrega completa até validar e incluir esses artefatos e conferir o DER atualizado.
