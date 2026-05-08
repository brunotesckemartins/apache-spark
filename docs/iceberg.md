### 3. Arquivo `ICEBERG.md`
```markdown
# 🧊 Apache Iceberg: Tabelas de Alta Performance

O **Apache Iceberg** é um formato de tabela aberto projetado para gerenciar petabytes de dados. Enquanto formatos tradicionais focam em "pastas", o Iceberg foca em **arquivos individuais**.

## 🚀 Diferenciais Tecnológicos
O Iceberg foi criado pela Netflix para resolver problemas de escala que o Hive não conseguia tratar.

### 1. Evolução Total do Esquema
Diferente de outros formatos, no Iceberg você pode:
* Adicionar, remover, renomear ou reordenar colunas.
* Atualizar tipos de dados.
**Tudo isso sem reescrever a tabela inteira**.

### 2. Particionamento Oculto (Hidden Partitioning)
O desenvolvedor não precisa se preocupar em criar filtros manuais de partição. O Iceberg cuida da relação entre a coluna de dados e o particionamento físico automaticamente.

### 3. Snapshot Isolation
As leituras são isoladas das escritas. O usuário sempre vê uma visão consistente da tabela, mesmo que bilhões de linhas estejam sendo inseridas naquele momento.

## 🎯 Caso de Uso: Logística
No sistema de despachos, usamos o Iceberg para o histórico de longo prazo, onde a facilidade de evoluir o esquema da tabela (conforme o app cresce) é uma prioridade.