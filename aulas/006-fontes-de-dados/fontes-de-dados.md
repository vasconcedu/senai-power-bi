# Fontes de dados

## Documentação da Microsoft sobre fontes de dados do Power BI 

https://learn.microsoft.com/pt-br/power-bi/connect-data/desktop-data-sources

## Demo: importação de dados de um banco de dados sqlite3

### `cachorros.db`

### Conteúdo do banco de dados 

```
sqlite3 cachorros.db
.tables
pragma table_info(racas_cachorros);
select * from racas_cachorros;
.quit
```

### Importação do banco de dados para o Power BI Desktop (👎 não vai funcionar!) 

`Obter dados` > `Mais...` > Buscar: `ODBC` 

### Instalação do driver ODBC do sqlite3

`Painel de Controle` > `Sistema e Segurança` > `Ferramentas Administrativas` > `ODBC Data Sources (XX-bit)` > `Drivers`

Driver ODBC do sqlite3: http://www.ch-werner.de/sqliteodbc/

**Depois da instalação do driver do sqlite3, fechar o Power BI e abrir novamente!**

### Importação do banco de dados para o Power BI Desktop (✅ agora vai funcionar!) 

`Obter dados` > `Mais...` > Buscar: `ODBC` > `Opções avançadas`

```
database=C:\caminho\para\cachorros.db
```
