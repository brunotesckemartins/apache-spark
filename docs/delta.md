# 🌊 Delta Lake: Transações ACID no Data Lake

O **Delta Lake** é uma camada de armazenamento open-source que traz confiabilidade para os Data Lakes. Ele resolve o problema fundamental de que arquivos (Parquet, Avro, JSON) por si só não garantem integridade em escritas simultâneas.

## 💎 Pilares de Confiabilidade
Para o nosso **Sistema de Despachos**, o Delta Lake é vital por causa de:

1. **Transações ACID:** Garante que, se a atualização de uma corrida falhar, o sistema retorne ao estado anterior sem corromper a tabela.
2. **Log de Transações (Delta Log):** Um registro central de todas as mudanças, permitindo auditoria e recuperação de desastres.
3. **Schema Enforcement:** Impede a entrada de dados mal formatados que poderiam quebrar o pipeline de dados.
4. **Upserts (MERGE):** Essencial para o cenário de logística, onde precisamos atualizar o status de um motorista se ele já existir ou inseri-lo se for novo.

## 🕰️ Time Travel
Com o Delta Lake, podemos consultar versões passadas da tabela:
```sql
SELECT * FROM motoristas VERSION AS OF 5;