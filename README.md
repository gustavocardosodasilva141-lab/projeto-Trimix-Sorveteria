# Trimix Sorveteria — Dicionário de Dados

Documentação interativa do banco de dados do Sistema de Gestão Operacional e Vendas da Trimix Sorveteria.

## Estrutura

```text
.
├── index.html
├── style.css
├── script.js
├── data.json
├── docs/
│   ├── README.md
│   ├── ddl_original.sql
│   ├── revisao_tecnica.md
│   └── Especificacao_Requisitos_Regras_Negocio_BD.pdf  (pendente)
└── assets/
    ├── README.md
    └── der.png  (pendente; PNG ou JPG)
```

## Catálogo

O catálogo foi conferido contra o DDL fornecido: 19 tabelas e 113 colunas, sem divergência nominal. O JSON inclui tipos, nulabilidade, valores default, PK/FK, índices e metadados de relacionamento.

## Recursos

- Pesquisa em tempo real por tabela, coluna e tipo.
- Alternância de tema claro/escuro.
- Detalhes de chaves estrangeiras, índices únicos e nulabilidade.
- Modal do DER com Panzoom.js (zoom e pan), dependente de `assets/der.png` ou `assets/der.jpg`.
- Seções de Data Literacy, LGPD, RBAC e auditoria.

## Publicar no GitHub Pages

1. Abra **Settings → Pages**.
2. Em **Build and deployment**, selecione **Deploy from a branch**.
3. Escolha a branch **main** e a pasta **/(root)**.
4. Clique em **Save** e aguarde o deploy.

URL esperada: https://gustavocardosodasilva141-lab.github.io/projeto-Trimix-Sorveteria/

## Pendências da entrega acadêmica

Antes de entregar, o grupo precisa corrigir as divergências registradas em `docs/revisao_tecnica.md`, exportar o PDF de requisitos atualizado e o DER final em PNG/JPG, e adicionar os arquivos binários nos caminhos exatos acima. A ativação do GitHub Pages também precisa ser confirmada.
