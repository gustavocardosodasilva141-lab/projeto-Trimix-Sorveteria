# Revisão técnica — Trimix Sorveteria

Este arquivo registra pontos para validação do grupo. O DDL é a fonte de referência para os nomes e tipos documentados no catálogo.

1. **Constraints CHECK:** confirmar se as regras de domínio descritas nos requisitos estão implementadas por CHECK, trigger, procedure ou validação da aplicação.
2. **ON DELETE:** o DDL não explicita ON DELETE nas FKs; confirmar se o comportamento padrão do InnoDB atende à regra documental.
3. **Auditoria JSON:** o DER indica JSON para dados_anteriores/dados_novos, enquanto o DDL usa LONGTEXT.
4. **RBAC:** os perfis constam no modelo, mas a implantação de permissões requer configuração de roles/grants no SGBD e na aplicação.
5. **Data/hora:** revisar padronização de UTC_TIMESTAMP e CURRENT_TIMESTAMP entre artefatos.

As observações não representam correções aplicadas ao DDL. A equipe deve validar e atualizar os documentos originais antes da entrega final.
